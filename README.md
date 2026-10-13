# Offline Poster Studio

This package contains the compiled web app and GitHub Actions workflow for building the Android APK.

## Build an APK with GitHub
1. Extract the ZIP.
2. Upload the extracted contents, including the hidden `.github/workflows/build-apk.yml` folder, to the root of your repository.
3. Open **Actions** and run **Build APK**.
4. Download the APK artifact from the completed workflow run.

## Research poster layouts
Four original landscape research poster layouts are included: three-column academic, four-column conference, visual evidence/data, and environmental impact. These include sectioned areas for background, methods, results, charts, data summaries, discussion, conclusions, references, and images.

## Text overflow and selection
Long titles are reduced to fit more comfortably. The live poster is rendered as inline SVG so tapping a text element selects it and shows a purple resize handle plus controls for font size, bold, italic, underline, and alignment. Drag the handle to resize. PNG export and Print use the edited preview SVG.

## Validation status
The JavaScript bundle passes `node --check`. This ZIP has not been built into an APK or tested on a physical Android device. Selected SVG text changes are applied to the current preview/export, but are not yet saved as persistent per-element project data when regenerating the poster.
