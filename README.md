# CKAM Android shell (ARM64)

This is an Android Studio project that wraps the CKAM web messenger at `https://ckaam.xsph.ru/` in a WebView.

## Build APK
1. Install Android Studio (current stable) and Android SDK 35.
2. Open this folder in Android Studio (`File > Open`).
3. Wait for Gradle sync; allow Android Studio to download dependencies.
4. Use `Build > Build Bundle(s) / APK(s) > Build APK(s)`.
5. Find the debug APK at `app/build/outputs/apk/debug/app-debug.apk`.

## Notes
- ABI filter is ARM64 (`arm64-v8a`) as requested.
- WebView is restricted to the CKAM HTTPS domain for in-app navigation; other http(s) links open externally.
- Camera and microphone permissions are requested when the web page requests them.
- File upload picker is supported.
- This project has not been built or tested on a device in this environment. WebRTC/video-call compatibility depends on the website's current implementation and Android WebView behavior.
- Before public release, review account deletion, security, backups, privacy policy, and server-side access controls. Do not place secrets in the APK.
