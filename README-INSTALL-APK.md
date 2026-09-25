# Anton Service POS — Build APK dengan GitHub Actions

Workflow ini khusus untuk membuat APK Android dari proyek React/Vite Anton Service POS.

## Penting

Jangan gunakan workflow **Jekyll site CI** atau template **Gradle/Android CI** bawaan GitHub untuk proyek ini. ZIP sumber tidak memiliki folder `android/`/Gradle; workflow ini membuat proyek Android Capacitor secara otomatis.

## Cara pakai

1. Salin `.github/workflows/android-apk.yml` ke repository.
2. Salin `capacitor.config.ts` ke root repository.
3. Commit dan push ke branch `main`.
4. Buka **Actions → Anton Service POS - Android APK**.
5. Jalankan **Run workflow**.
6. Jika berhasil, buka hasil run dan bagian **Artifacts**.
7. Unduh `anton-service-pos-debug-apk` lalu ekstrak untuk mendapatkan file `.apk`.

Workflow sengaja memiliki langkah `Locate APK` dan `if-no-files-found: error`, sehingga workflow tidak akan berstatus berhasil jika file APK benar-benar tidak dibuat.
