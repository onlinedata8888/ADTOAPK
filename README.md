# AdStripper

Android app that strips ad SDKs out of any APK, on-device.

- Rewrites classes*.dex with dexlib2 (no apktool, no PC).
- Banner loadAd -> setVisibility(GONE) + return; full-screen load/show -> no-op.
- Repacks APK, re-aligns .so to 4096 and resources.arsc to 4, strips old
  META-INF signatures, signs v1+v2+v3 with apksig.
- Output: Downloads/<name>-noads.apk
