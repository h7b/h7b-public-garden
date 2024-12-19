---
{"dg-publish":true,"permalink":"/notes/sideload-apps-ios/","title":"How to sideload apps to iPhones?","created":"2023-03-16T07:43:52+07:00","updated":"2024-12-19T10:46:00+07:00"}
---

# How to sideload apps to iPhones?

When referring to iOS apps, "sideloading" means installing an app in IPA format onto an Apple device, usually through the use of a computer program such as Cydia Impactor, Xcode, on the actual device using a jailbreak method or using a signing service instead of through Apple's App Store.[^1]

## Free

Known options:
- [AltStore](https://altstore.io/)
- [Sideloadly](https://sideloadly.io/)
- [SideStore](https://sidestore.io/)
- [Scarlet](https://usescarlet.com/)

Limitations of sideloading with my own free Apple developer account
- sideloaded apps are subjected to the 7-day signing restrictions
- max 3 apps per device.
    - 2024-12-02 discover SparseRestore which can bypass the 3-app limit. Source: [reddit](https://www.reddit.com/r/jailbreak/comments/1g0w1j8/using_sparserestore_the_3app_limit_as_been/)

However, if I have a [paid Apple developer account](https://developer.apple.com/support/compare-memberships/) (USD 99/year), the signing lasts longer (1 year) and there is unlimited number of sideloaded apps.

### SideStore

[SideStore](https://sidestore.io/)is a fork of AltStore. Their unique selling points, compared to AltStore, is that SideStore allows re-sign apps without the needs of connecting to a PC (wirelessly or not).

Cons:
- I can sideload max 2 apps with SideStore
- cannot install large-size apps (1GB+)

Pros:
- The SideStore app itself can be re-signed wirelessly (but must have connection with my PC), while the other sideloaded apps can be re-signed without connection to my PC (wirelessly or not)

Note:
- For the reason of convenience, I have replaced Sideloadly with SideStore since 2023-10-24.
- The [instruction to install on their homepage](https://sidestore.io/)which use SideServer, does not work at the moment of testing (2023-10-23). I can sideload SideStore into iDevice, but cannot pair iDevice with my PC.
- Hence I followed [this guide in the SideStore wiki](https://wiki.sidestore.io/guides/getting-started/). It uses AltServer and Jitterbugpair. I can successfully re-sign (wirelessly via wifi) both the SideStore and other sideloaded apps.
- Since 2024-08-20, the SideStore app can't be opened on ios devices to refresh sideloaded apps. Need to manually sideload the SideStore app via altserver from PC.
    - 2024-10-01, while lurking the SideStore discord, i found [a discussion](https://discord.com/channels/949183273383395328/1285553743752069141/1287528615361384510) in which they advised to use the SideStore ios app (installed via altserver) to open/sideload the SideStore ipa file itself again. This trick will eradicate the bug where SideStore ios app can't be opened
- 2024-08-27 a repo to install unlimited apps (10 apps limit of free developer account do not apply here!). [GitHub - khanhduytran0/LiveContainer: Run iOS app without actually installing it!](https://github.com/khanhduytran0/LiveContainer?tab=readme-ov-file)
- 2024-12-02 learn the existence of [iOS Shortcut to Auto Refresh Sidestore](https://www.youtube.com/watch?v=16gZztB8E2U). Tried this on my devices.
- 2024-12-02 read [Common SideStore annoyances and how to fix them](https://www.reddit.com/r/sideloaded/comments/1bxywa5/common_sidestore_annoyances_and_how_to_fix_them/)
    - Issue 1: SideStore stops opening/crashes on open a couple of days into a fresh install
    - Issue 2: SideStore crashes after the first successful app refresh/before it can refresh all apps
    - Issue 3: SideStore’s “refresh all apps” action in the Shortcuts app is broken - errors/log say “the file cannot be found”

### Sideloadly

I have good experiences with [Sideloadly](https://sideloadly.io/) using a free Apple developer account.

Pros:
- Can sideload apps that are not available on Apple's App Store, such as: [uYouPlus](https://github.com/qnblackcat/uYouPlus), [CercubePlus](https://github.com/qnblackcat/CercubePlus), [NineAnimator](https://github.com/SuperMarcus/NineAnimator), [Wolf for Facebook](https://appdb.to/app/cydia/1900000698), [Spotify++](https://appdb.to/app/cydia/1900000540), [PlexTweak](https://appdb.to/app/cydia/1900000472)
- Also works with large-size apps (1GB+), where Alstore and SideStore encounter errors in installation step
- I can sideload max 3 apps with Sideloadly

Cons:
- Sideloadly has convenient features (like: automatically re-sign apps when connecting iDevices to PC, re-sign apps wirelessly) but I cannot enable/use these 2 features.
- Must connect iDevices to PC via cable.

### AltStore

I come to [AltStore](https://altstore.io/), with the expectation that I can re-sign sideloaded apps wirelessly via my PC, but I haven't yet made it happened (until now 2023-10-24).

Cons:
- I can sideload max 2 apps with Altstore, because it already took 1 sideload slot on iDevice
- cannot install large-size apps (1GB+)

## Paid services

If purchasing a paid Apple developer account is quite steep, redditors also recommend some 3rd-party UDID Signing services to consider.

- [Signtunes](https://signtunes.co/): USD 12/year
- [Signulous](https://www.signulous.com/): [USD 20/year](https://www.signulous.com/register)
- [UDID Registrations](https://www.udidregistrations.com/): [USD 10-20/year](https://www.udidregistrations.com/buy)
- [Signum](https://signum.fun/): [GBP 12-18/year](https://signum.fun/purchase/)
- [Maplesign](https://maplesign.ca/): USD 7.25/year

## Sideloaded iOS apps

- [uYouPlus](https://github.com/qnblackcat/uYouPlus)
- [CercubePlus](https://github.com/qnblackcat/CercubePlus): inactive
- [YTLitePlus](https://github.com/YTLitePlus/YTLitePlus)
- [NineAnimator](https://github.com/SuperMarcus/NineAnimator)
- [Wolf for Facebook](https://appdb.to/app/cydia/1900000698)
- [Spotify tweak from appdb](https://appdb.to/?name=Spotify)
- [SpotveeC](https://github.com/SpotCompiled/SpotveeC): compiled ipa files of [EeveeSpotify](https://github.com/whoeevee/EeveeSpotify)
- [PlexTweak](https://appdb.to/app/cydia/1900000472): inactive

## Related resources

- [idownloadblog | How to sideload apps to iPhones, iPads, and Apple Silicon Macs with Sideloady](https://www.idownloadblog.com/2022/03/28/sideload-apps-iphone-ipad-apple-silicon-macs-sideloady/)
- [xda-developers | How to easily sideload apps on any iPhone using AltStore](https://www.xda-developers.com/how-to-sideload-apps-on-iphone/)
- [How's the general state of iOS sideloading? : r/sideloaded](https://www.reddit.com/r/sideloaded/s/QcJNpnSyIh)
- [How to sideload (all methods) : r/sideloaded](https://www.reddit.com/r/sideloaded/s/LIUfyvga4k)
- [How to sideload on iOS without jailbreak or expiry period for free in the easiest way possible? – Avieshek's Blog](https://avieshek.wordpress.com/2024/06/11/how-to-sideload-on-ios/)
- [Best Guide for Sideloading on iOS](https://sideloading.vercel.app/#title)
- [Best IPA Sideload Techniques on iPhone & iPad (2024) - YouTube](https://www.youtube.com/watch?v=fJD9A6d8Pr4)

[^1]: [Wikipedia](https://en.wikipedia.org/wiki/Sideloading#:~:text=When%20referring%20to%20iOS%20apps,of%20through%20Apple%27s%20App%20Store.)