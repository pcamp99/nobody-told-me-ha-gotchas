# Nobody Told Me About My Smart Home

Fixes, configs, and AI starter prompts from the [@NobodyToldMeSmartHome](https://www.youtube.com/@NobodyToldMeSmartHome)
YouTube series — the Home Assistant settings, bugs, and silent failures that
cost real time because no tutorial mentions them.

I'm not a coder. I use Claude for basically everything technical in my home
automation setup, and every video pairs the gotcha with the exact, shown fix —
never just "here's what went wrong."

## Videos

| # | Video | Fix / config | AI starter prompt |
|---|---|---|---|
| 1 | [Home Assistant Can't See Your USB Stick in VirtualBox? Here's the Fix](https://youtu.be/rYE3om9XT7o) | VirtualBox USB passthrough — settings walkthrough, no file | [gist](https://gist.github.com/pcamp99/6803071ff5f06c1563fec8b95cbccfab) |
| 2 | [Home Assistant Wake Word Testing Broke Because of This API Bug](https://youtu.be/hwYkl4HKjqQ) | Always pass an explicit `end_time` — one-parameter fix, no file | [gist](https://gist.github.com/pcamp99/e2b6f54412deb6d61d479d87943fded5) |
| 3 | [How I Trained My Own Wake Word for Home Assistant (No Coding Required)](https://youtu.be/zxDjOOT-gA8) | Training-pipeline traps — no file, see the video | [gist](https://gist.github.com/pcamp99/6f7739117ac55389bcf13778ec14f9ea) |
| 4 | My Home Assistant Watchdog Looked Healthy for Weeks. This Condition Doesn't Fail the Way You Think. *(link added once published)* | [`04-condition-state-raises/integration_watchdog.yaml`](04-condition-state-raises/) | [gist](https://gist.github.com/pcamp99/33d77efcbd5a7867abb6e794e736c9e1) |

## What's an "AI starter prompt"?

A copy-paste prompt for whatever AI assistant you already use (Claude, ChatGPT,
Gemini, doesn't matter) — drop it into a new chat and it primes the assistant
to ask about *your* specific setup before suggesting a fix, instead of assuming
your hardware, hypervisor, or entities match mine exactly.

Every video from here forward gets one.
