# Audiation Trainer — GitHub APK build

## Files to put in the repository root
Upload these files individually:
- `index.html`
- `icon.png`
- `package.json`
- `capacitor.config.json`

Do not upload `build.yml` to the repository root as a workflow. It is included here as the source to paste into the workflow path below.

## Create the GitHub Actions workflow
In the repository, choose **Add file → Create new file**.
For the filename, enter exactly:

`.github/workflows/build.yml`

Paste the complete contents of the included `build.yml`, then commit.

GitHub creates the `.github/workflows` folders from that path. You do not need to upload folders.

## Build and download
1. Open the repository's **Actions** tab.
2. Select **Build Audiation Trainer APK**.
3. Choose **Run workflow**.
4. When it finishes successfully, open the run and find **Artifacts**.
5. Download `Audiation-Trainer-debug-apk`.
6. Extract the downloaded ZIP and install `app-debug.apk` on the Android phone.

## Notes
- This workflow builds a debug APK; it is suitable for installing/testing, not a Play Store release.
- The app requests microphone access for pitch detection. Allow microphone permission when Android asks.
- Test microphone pitch detection on the installed app. Android/WebView permission behavior can vary by device.
- The uploaded HTML's session, pitch detection, progress storage and lesson logic are preserved as supplied.
