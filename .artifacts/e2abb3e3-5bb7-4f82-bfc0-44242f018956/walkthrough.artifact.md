# Walkthrough - Layout 3 Gambar (Background, Logo, dan Foto Profil)

## Ringkasan Perubahan

Berhasil memperbarui layout `TugasLogin.kt` agar menerapkan 3 gambar seperti pada contoh asisten dosen (asdos):
1. **Background Image**: Gambar latar belakang yang menutupi seluruh layar dengan transparansi (`alpha = 0.2f`) dan overlay putih agar teks tetap mudah dibaca.
2. **Logo Atas**: Gambar logo utama (`logo_umy`) yang ditampilkan di bagian atas kartu.
3. **Foto Profil Lingkaran**: Gambar foto profil di dalam bingkai lingkaran di bagian bawah.

## Detail Perubahan

### Komponen UI

#### [MODIFY] [TugasLogin.kt](file:///C:/Users/Lenovo/AndroidStudioProjects/Activity2/app/src/main/java/com/example/activity2/ui/theme/TugasLogin.kt)
- Menambahkan `Image` sebagai layer paling belakang di dalam `Box` root dengan `ContentScale.Crop` dan efek overlay semi-transparan.
- Mempertahankan dan menyusun ulang posisi Logo Atas, Teks Identitas (Nama & NIM), serta Foto Profil Lingkaran di dalam `Column`.

## Hasil Verifikasi

### Tes Otomatis
- Gradle build (`:app:assembleDebug`) berhasil dijalankan tanpa error (`success = true`).
