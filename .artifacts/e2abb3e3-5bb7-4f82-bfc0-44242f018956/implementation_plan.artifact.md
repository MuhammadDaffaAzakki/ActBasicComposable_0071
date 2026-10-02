# Implement 3-Image UI Layout (Background, Top Logo, and Circle Profile Image)

## Goal
Update `TugasLogin.kt` to match the teaching assistant's example which features 3 images:
1. **Background Image**: Covers the entire screen behind the content.
2. **Top Logo Image**: Displayed near the top header.
3. **Circle Profile Image**: Displayed inside a circular frame further down the screen.

## User Review Required

> [!NOTE]
> Since the project currently has `logo_umy.webp` and `notasibalok.xml` in `res/drawable`, `logo_umy` will be used for the top logo and profile image (or background), and you can easily drop your own background image (e.g., `bg_login.webp`) and profile image into `res/drawable` whenever needed.

## Proposed Changes

### UI Components

#### [MODIFY] [TugasLogin.kt](file:///C:/Users/Lenovo/AndroidStudioProjects/Activity2/app/src/main/java/com/example/activity2/ui/theme/TugasLogin.kt)
- Wrap the main content in a root `Box` containing:
  1. A background `Image` (or styled background container) filling `Modifier.fillMaxSize()`.
  2. A semi-transparent overlay (optional, to make text readable over the background image).
  3. A `Column` with `contentAlignment = Alignment.Center` holding:
     - Header text ("KARTU TANDA MAHASISWA", etc.)
     - Top Logo `Image` (`logo_umy`)
     - Personal data text ("DATA PRIBADI", Name, NIM)
     - Circle Profile `Image` (`logo_umy` or `notasibalok`)

## Verification Plan

### Automated Tests
- Run Gradle build (`:app:assembleDebug`) to ensure no compilation errors.

### Manual Verification
- Deploy and check the UI on an emulator/device to verify all 3 image layers (background, top logo, and circle profile image) render correctly.
