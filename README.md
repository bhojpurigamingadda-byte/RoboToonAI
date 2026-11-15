# RoboToon AI Android starter (v0.1)

This is the first Android Studio project foundation for a script-to-animation app.

## Included in this prototype
- Script input screen
- Animation style selection: Roblox 3D, Stickman, 2D Cartoon, 3D Cartoon
- Fast and Pro quality selection
- Voice-over preference selection
- Caption style selection
- Local project-settings preview

## Important: what is not connected yet
This starter does **not** generate an MP4 yet. Real generation requires backend services:
1. Script-to-scene planner (turn script into scenes, dialogue, shot prompts)
2. Character/animation generation or licensed 3D animation assets
3. Text-to-speech voice generation
4. Caption timing/alignment
5. Video renderer and MP4 storage/delivery

Do not put private API keys inside the Android app. Add a backend and keep provider keys server-side.

## Build an APK
1. Install Android Studio (current stable) and Android SDK 35.
2. Open this folder in Android Studio.
3. Let Gradle sync complete.
4. Choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. The debug APK will be under `app/build/outputs/apk/debug/`.

## Suggested next milestone
Create a backend API such as `POST /projects` that accepts script, style, quality, voice and caption style, then returns a project ID. Add job status polling and a final MP4 URL. Implement authentication, rate limits, moderation, cost limits and storage before public launch.


## Build an APK from an Android phone (cloud build)

This ZIP includes a GitHub Actions workflow at `.github/workflows/build-apk.yml`.
You can start a cloud build without installing Android Studio on your phone:

1. Create/sign in to a GitHub account and create a new **public or private** repository.
2. Upload the contents of this ZIP to the repository (GitHub mobile app or browser).
3. Open the repository's **Actions** tab.
4. Select **Build RoboToon AI APK** and tap **Run workflow** (or push to `main`).
5. When the run succeeds, open the run and download the `RoboToonAI-debug-apk` artifact.
6. Extract the downloaded artifact and install the debug APK on your Android phone.

The workflow is prepared but has not been executed here. A successful APK is only confirmed
after GitHub Actions completes the build. This is a prototype APK; AI video generation,
voice-over, animation, captions and MP4 export are not connected yet.
