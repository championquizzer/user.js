# user.js

A `user.js`, which resides in the root directory of a Firefox profile, is used to set preferences for that profile when Firefox starts. Preferences are settings that control Firefox's behavior. Some can be set from the Options interface and all can be found in about:config, except for what are called hidden preferences which will only show when they are set by the user.

1. `privacy.firstparty.isolate = true` : this preference isolates all browser identifier sources (e.g. cookies) to the first party domain, with the goal of preventing tracking across different domains.
2. `privacy.resistFingerprinting = true` : this preference makes Firefox more resistant to browser fingerprinting.
3. `privacy.trackingprotection.fingerprinting.enabled = true` : blocks Fingerprinting.
4. `privacy.trackingprotection.cryptomining.enabled = true` : blocks CryptoMining.
5. `privacy.trackingprotection.enabled = true` : Mozilla's new built-in tracking protection. One of it's benefits is blocking tracking (i.e. Google Analytics) on privileged pages where add-ons that usually do that are disabled.
6. `browser.send_pings = false` : the attribute would be useful for letting websites track visitors' clicks.
7. `browser.urlbar.speculativeConnect.enabled = false` : disable preloading of autocomplete URLs. Firefox preloads URLs that autocomplete when a user types into the address bar, which is a concern if URLs are suggested that the user does not want to connect to.
8. `dom.event.clipboardevents.enabled = false` : disable that websites can get notifications if you copy, paste, or cut something from a web page, and it lets them know which part of the page had been selected.
9. `media.eme.enabled = false` : disables playback of DRM-controlled HTML5 content, which, if enabled, automatically downloads the Widevine Content Decryption Module provided by Google Inc. DRM-controlled content that requires the Adobe Flash or Microsoft Silverlight NPAPI plugins will still play, if installed and enabled in Firefox.
10. `media.gmp-widevinecdm.enabled = false` : disables the Widevine Content Decryption Module provided by Google Inc., used for the playback of DRM-controlled HTML5 content.
11. `media.navigator.enabled = false` : websites can track the microphone and camera status of your device.
12. `network.cookie.cookieBehavior = 1` : disable cookies ; 0 = Accept all cookies by default ; 1 = Only accept from the originating site (block third-party cookies) ; 2 = Block all cookies by default
13. `webgl.disabled = true` : WebGL is a potential security risk.
14. `browser.sessionstore.privacy_level = 2` : this preference controls when to store extra information about a session: contents of forms, scrollbar positions, cookies, and POST data. ; 0 = Store extra session data for any site ; 1 = Store extra session data for unencrypted (non-HTTPS) sites only ; 2 = Never store extra session data.
15. `beacon.enabled = false` : disables sending additional analytics to web servers.
16. `browser.safebrowsing.downloads.remote.enabled = false` : prevents Firefox from sending information about downloaded executable files to Google Safe Browsing to determine whether it should be blocked for safety reasons.  
17. Disable Firefox prefetching pages it thinks you will visit next. Prefetching causes cookies from the prefetched site to be loaded and other potentially unwanted behavior:  
17.1 `network.dns.disablePrefetch = true`  
17.2 `network.dns.disablePrefetchFromHTTPS = true` 
17.3 `network.predictor.enabled = false`  
17.4 `network.predictor.enable-prefetch = false`  
17.5 `network.prefetch-next = false`

## References and further reading:
1. ["about:config tweaks" for Firefox by privacytools.io](https://privacytools.io/browsers/#about_config)
2. [arkenfox user.js on GitHub](https://github.com/arkenfox/user.js)
3. [mozillaZine](http://kb.mozillazine.org/User.js_file)
