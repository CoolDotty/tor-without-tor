# tor-without-tor
Privacy-conscious web browsing without high-latency.

## Why?
When trying to make your web browsing more private, there isn't much to try other than Joe Blow's Firefox config. Surely there's more nuance to it than `privacy.resistFingerprinting: true` right? Why not trust those who have been hardening Firefox for years.

Why skip tunneling? Well, we're all only human. Privacy doesn't appeal to the monkey brain as much as lower latency does. This project may not normalize web traffic from exit nodes, but it at least helps normalize the Tor browser's fingerprint.

## Installing
Download the latest version of [Tor Browser](https://www.torproject.org/download/) and extract it into this repo.

Effectively, this should put `firefox.cfg` in the `/Browser` directory and `autoconfig.js` in the `/Browser/defaults/pref` directory.

You should probably rename any shortcuts with "Tor (No Tunneling)" as a courtesy.

These are all temporary changes of course, so if you ever want to start tunneling again you just need to move/rename the mentioned files and restart the browser.

Test out your fingerprint! I personally test using [Cover Your Tracks by the EFF](https://coveryourtracks.eff.org/). This is especially important if customize your browser in any way. Toolbar density, installing new extensions, even aero-snapping your browser to half size in Windows gave me a unique fingerprint.

As of now, I use normal density, [uBlock Origin](https://ublockorigin.com/), and maximise the window with letterboxing on and do not have a unique fingerprint.

## Alright I'm down, except for one thing ...
Yeah, if you're already making concessions, there's one more you're likely to consider. Changing `privacy.resistFingerprinting.letterboxing` to `false` in `about:config` is what you're looking for. I keep it on and have gotten used to it. If it's a deal-breaker though, disabling it will still let you reap all the other benefits of the browser.

## That's about it
Some stuff for the future is a guide for setting Tor as a default browser and doing a proper fork of the project. For now, I'm just seeing how much attention this gets since what's currently out there is for Tor 9.0 or earlier.
