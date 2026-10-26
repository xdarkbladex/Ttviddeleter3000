# Only You Helper (Android)

A small, local Android accessibility helper for assisting with TikTok's per-post audience controls.

## Honest scope
- It does **not** bulk-select all posts.
- It does **not** log in, ask for, or store your TikTok password.
- It has no Internet permission.
- When armed and TikTok is the foreground app, it looks for the exact `Only you` / `Only me` audience option and attempts to select it.
- It never clicks Save/Done/Post/Delete. You must review the audience and save each post yourself.
- TikTok's UI can change; this is best-effort and may not work on all versions or languages.
- Accessibility permission is powerful. Enable it only if you trust the source. Pause the helper when not using it.

## Build an APK
This environment did not have the Android SDK/Gradle installed, so an APK could not be compiled here. The included GitHub Actions workflow builds the APK in the cloud.

1. Create a private GitHub repository.
2. Upload the contents of this folder to the repository's `main` branch.
3. Open **Actions** → **Build Android APK** → **Run workflow** (or wait for the push build).
4. Open the completed workflow run and download the `only-you-helper-debug-apk` artifact.
5. Extract the artifact ZIP to get `app-debug.apk`.
6. Transfer the APK to your Android phone and install it. Android may ask you to allow installation from that source.

This is a debug APK, not a Play Store release. Do not share it as a trusted app without reviewing/signing the code yourself.

## Use
1. Open Only You Helper.
2. Tap **Enable Android accessibility service**, then enable Only You Helper in Android Accessibility settings.
3. Return to the helper and tap **Arm helper**.
4. Open TikTok and navigate manually to one of your own posts' audience controls.
5. If the exact `Only you` option appears, the helper may select it. Verify it and tap TikTok's own Save/Done control yourself.
6. Repeat for each post, then pause the helper.

No post deletion or automatic saving is implemented.
