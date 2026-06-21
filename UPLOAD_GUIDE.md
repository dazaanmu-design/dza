# Panduan Upload ke GitHub dari ZIP

1. Download dan extract ZIP ini.
2. Masuk ke GitHub, buat repository baru, contoh nama: `sabar-apk`.
3. Klik **Add file** → **Upload files**.
4. Drag semua file dan folder dari hasil extract, bukan folder ZIP-nya.
5. Pastikan yang ikut ter-upload minimal ada:
   - `.github/workflows/build-apk.yml`
   - `app/build.gradle`
   - `app/src/main/AndroidManifest.xml`
   - `settings.gradle`
   - `build.gradle`
6. Klik **Commit changes**.
7. Masuk tab **Actions** → **Build APK** → **Run workflow**.
8. Tunggu sampai hijau, lalu download artifact **SABAR-debug-apk**.

Jika folder `.github` tidak terlihat:
- Windows Explorer: View → Show → Hidden items.
- Mac Finder: tekan `Command + Shift + .`.
