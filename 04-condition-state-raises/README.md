# Video 4 — the fix

Video: https://youtu.be/VVcF6ITRZYw
AI starter prompt for this one: https://gist.github.com/pcamp99/33d77efcbd5a7867abb6e794e736c9e1

`integration_watchdog.yaml` is the corrected version of the automation from the
video — a health-check/watchdog pattern that checks several integrations on a
schedule and reloads whichever one broke.

**The gotcha it fixes:** `condition: state` against an entity that no longer
exists doesn't evaluate `false` — it raises an error. Inside an `if:` action
block, that error gets caught and skips just that one check, but the
automation's own status still reads "on" with a fresh last-triggered
timestamp. It looks perfectly healthy while one check has been silently
broken, possibly for weeks.

**The fix:** `condition: template` with `states()` instead of
`condition: state` — `states()` returns the string `"unknown"` for a missing
entity instead of raising. Plus a self-check block that specifically alerts
when a sentinel entity stops *existing*, not just when it goes unavailable.

Copy the shape, swap in your own entities, config entry IDs, and notify
service.
