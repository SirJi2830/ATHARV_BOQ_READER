# Atharv Enterprises BOQ Reader

Android Studio project (Kotlin + Jetpack Compose).

## Current starter capabilities
- Android document picker
- XLS / XLSX / XLSM workbook reading through Apache POI
- Enumerates all sheets, including hidden sheets
- CSV / TSV / TXT reading
- Searchable/text-based PDF extraction
- Basic table-header detection for item description, quantity, unit, rate and amount
- Displays extraction warnings; does not silently claim that uncertain values are exact

## Important limitations
- VBA macros are **not executed**. XLSM cached cell values are read when present.
- Scanned PDFs and image-only BOQs need OCR. ML Kit is included as a dependency for the next OCR implementation, but image/PDF OCR flow is not yet wired.
- DOC/DOCX, XML, HTML, ZIP-contained BOQs, password-protected files and proprietary tender portals are not yet parsed by this starter.
- Online enhancement/backend is not connected. Core workbook/text parsing works locally after dependencies are built into the app.
- PWD templates vary. Always compare extracted totals with the original BOQ before tender submission or payment.

## Build
1. Install Android Studio (Ladybug or newer) with Android SDK Platform 35.
2. Open this folder as a project.
3. Allow Gradle to download dependencies.
4. Build > Build Bundle(s) / APK(s) > Build APK(s).
5. APK output: `app/build/outputs/apk/debug/app-debug.apk`.

Requires JDK 17 and Android Gradle Plugin 8.7.3.
