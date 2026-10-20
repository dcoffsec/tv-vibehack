# The prompt

My Android TV is slow and full of ads. Help me safely debloat it over Wi-Fi and replace its default home screen with a fast, minimal Apple TV-style launcher.

First, inspect the repository and reuse its existing launcher, scripts, and device-specific examples wherever possible. Do not rebuild working components from scratch.

CONNECT

Discover the TV on my local network, or ask me for its IP address if discovery fails.
Check which ADB connection method my TV supports. Use Wireless debugging and pairing when required, or network ADB when supported.
If macOS blocks the standard ADB binary, try the repository's Python ADB client if available.
Never bypass pairing, authorization, or security prompts.

BACK UP AND DEBLOAT

Before making changes, back up the installed-package list, currently disabled packages, relevant system settings, device model, Android version, and firmware information.
Inspect package names and their purposes before proposing changes.
Identify manufacturer advertising, telemetry, recommendation services, and unnecessary preinstalled apps.
Prefer reversible per-user disabling. Never uninstall packages or modify system partitions.
Ask me before disabling streaming apps, Google services, casting, voice assistants, firmware updates, input services, accessibility features, or anything whose purpose is uncertain.
Never apply a generic debloat list blindly. Tailor changes to my exact TV model.
Record every change and generate a restore script that reverses only the changes made.

LAUNCHER

Reuse the existing launcher if the repository contains one.
Create a lightweight, native Android TV home screen inspired by Apple TV: a black background, customizable favorite-app dock, clean app grid, clock, date, and nature wallpapers.
Optimize for low-memory TVs and reliable D-pad navigation.
Keep the stock launcher available until the replacement has been installed and tested.
Inspect Home-button handling and verify that the new launcher remains usable before disabling any stock home or setup component.
Never disable com.google.android.tungsten.setupwraith or another potentially critical package without verifying its presence, investigating device-specific risks, and getting my explicit approval.

VERIFY

After each major step, verify the command's result rather than assuming it succeeded.
Capture and inspect TV screenshots where supported; if capture fails, report that limitation.
Test Home, Back, D-pad navigation, app launching, the on-screen keyboard, HDMI inputs, Wi-Fi, and the remote.
Stop and restore the last known working configuration if a critical feature breaks.

DELIVER

Provide the final launcher, installation instructions, a change log, a backup, and a tested restore script.
Explain which packages were disabled and why, any known limitations, and how to customize the dock and wallpapers.
Ask me before making consequential or ambiguous changes. Do not claim anything is verified unless you have actually tested it.

Start by inspecting the repository, identifying my TV model and supported ADB connection method, and presenting a plan. Wait for my approval before modifying the TV.

"If you cloned [this repo](https://github.com/dcoffsec/tv-vibehack.git), run Claude Code inside it. It
can reuse the launcher and scripts instead of writing them from scratch."
