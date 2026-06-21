# SABAR WebView APK

Project Android WebView untuk mengubah link Google Apps Script menjadi APK Android melalui GitHub Actions.

## Link WebView

```text
https://script.google.com/macros/s/AKfycbxU1p8pGrKpci6bZk5xvDGpaxTZIzUMH_L_YFQv-KFU2lviP3Fgn0rGACChmgLSWYQl/exec
```

## Fitur yang sudah dibuat

- WebView fullscreen portrait.
- Splash screen background putih dengan logo diperbesar.
- App icon memakai logo yang dilampirkan.
- JavaScript, DOM Storage, cookies, dan third-party cookies aktif agar Google Apps Script lebih aman berjalan.
- Support upload gambar/file dari halaman WebView.
- Tombol back mengikuti riwayat halaman WebView.
- Halaman error sederhana jika koneksi gagal.
- Build otomatis APK melalui GitHub Actions.

## Cara build APK di GitHub

1. Buat repository baru di GitHub.
2. Upload semua isi folder project ini ke repository tersebut.
3. Pastikan folder `.github/workflows/build-apk.yml` ikut ter-upload. Jika folder `.github` tidak terlihat di Windows, aktifkan **Show hidden files**.
4. Buka tab **Actions** di repository.
5. Pilih workflow **Build APK**.
6. Klik **Run workflow**.
7. Setelah selesai, buka hasil workflow lalu download artifact **SABAR-debug-apk**.
8. File APK ada di dalam artifact dengan nama `SABAR.apk`.

## Cara mengganti nama aplikasi

Edit file:

```text
app/src/main/res/values/strings.xml
```

Ubah bagian:

```xml
<string name="app_name">SABAR</string>
```

## Cara mengganti link WebView

Edit 2 file berikut agar konsisten:

```text
app/src/main/res/values/strings.xml
app/src/main/java/com/daynite/sabar/MainActivity.java
```

Ubah URL lama menjadi URL baru.

## Catatan install di HP Android

APK yang dibuat adalah debug APK sehingga bisa langsung dipakai untuk testing. Saat install, Android biasanya meminta izin **Install unknown apps / sumber tidak dikenal**.
