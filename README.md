# Offline Poster Studio

Offline poster maker for Android (Capacitor). Includes the new app icon.

## Get your APK
1. Upload everything in this folder to a GitHub repository: the `dist` folder, `app-icons.zip` (the app icon - upload it as-is, do not unzip), `package.json`, `capacitor.config.json`, `.gitignore` and the hidden `.github` folder.
   - If `.github` doesn't upload: in GitHub choose Add file > Create new file, name it `.github/workflows/build-apk.yml`, and paste in the contents of `WORKFLOW-build-apk.yml`.
2. Open the repo's Actions tab, pick "Build APK" and press Run workflow (it also runs on every push to main).
3. When it turns green, download the APK from the new Release (Releases section on the repo page), or from the `OfflinePosterStudio-apk` artifact on the run page.

PNG exports from the Android app are saved directly to the phone Gallery in Pictures/Offline Poster Studio, so they appear in Gallery/Photos. SVG exports remain in Documents/PosterStudio. If Gallery saving fails, PNG export falls back to Documents/PosterStudio.

## Background updates
- Landscape poster layouts now also display the selected background treatment.
- In Background library → Textures, choose **Import photo** to select an image from your device. Tap **Apply background** to use it. The imported photo is automatically resized (max 1600 px) so projects still save, and it works offline on that device.

## Upload to GitHub
Upload the contents of this ZIP (not the ZIP file itself) to the root of your repository. Keep the `.github/workflows/build-apk.yml` workflow file and the `dist` folder.

## Gallery photo slots fix
- Gallery templates (including Classroom Highlights) now have six independent photo upload slots. Each photo is placed in its matching frame, can be replaced or removed individually, and is resized to max 900 px and compressed locally so projects keep saving.
- Other templates retain the existing single-photo upload behavior.

## PNG export to Gallery
- On Android, **Export PNG** now saves straight to your phone Gallery (Pictures/Offline Poster Studio). If that is unavailable it falls back to Documents/PosterStudio or the share sheet. The build adds a small native plugin automatically (see `.github/workflows/build-apk.yml`), so keep that file.
