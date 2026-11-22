# MYRAA — recovered project files (APK v1.0.2)

This folder was reconstructed from the supplied APK.

## What was recovered
- `www/`: packaged web app (HTML, bundled JavaScript, CSS, images, character model/textures, and video assets).
- `recovered-assets/`: Capacitor configuration and native bridge JavaScript.
- `android-original/`: original compiled Android manifest/resources/DEX files and packaged native libraries where present.
- `package.json` and `capacitor.config.json`: starter project metadata.

## Important limitations
The APK contains a compiled/minified web bundle, not the original development repository. Original TypeScript/JSX source modules, comments, build scripts, lockfile, and full Android Studio/Gradle project were not present in the APK. The bundled `www/assets/*.js` is the recoverable application logic, but it is not the original editable source structure. Android `.dex` files are compiled bytecode; they are preserved under `android-original/` but have not been converted into original Java/Kotlin source.

## Preview the recovered web app
Use a local static server from this folder, for example:

```bash
npx serve www
```

## Next step for a full Android Studio project
Use JADX to decompile the DEX files and apktool to decode Android resources/manifest, then integrate the recovered `www/` assets into a matching Capacitor Android project. The exact dependency versions and native plugin configuration should be verified during that process.
