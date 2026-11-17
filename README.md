# World of GAR

Website server Minecraft statis. Bagian **Berita Terbaru** mengambil data dari `news.json` dan menampilkan maksimal tiga berita paling baru. Bagian **Hadiah Kenaikan Level** menampilkan milestone reward level 5–100 beserta rentang rank pemain.

## Alamat server

- **Java Edition:** `mc.argust.my.id` (tanpa port)
- **Bedrock Edition:** `mc.argust.my.id`, port `22137`

Status online/offline Java dan Bedrock ditampilkan otomatis melalui widget **MCStatus.io**. Hasil dapat mengikuti cache penyedia status, jadi perubahan server mungkin tidak langsung terlihat.

## Menambahkan berita

Edit `news.json`, lalu tambahkan objek berita ke dalam array:

```json
[
  {
    "date": "2026-11-14",
    "category": "UPDATE",
    "title": "Judul update server",
    "summary": "Ringkasan singkat untuk ditampilkan di halaman utama.",
    "details": ["Informasi lengkap berita ditampilkan saat kartu diklik."]
  }
]
```

- `date`: tanggal format `YYYY-MM-DD`; berita diurutkan dari yang terbaru.
- `category`: label pendek seperti `UPDATE`, `EVENT`, atau `INFO`.
- `title`: judul berita.
- `summary`: ringkasan berita.
- `details`: daftar paragraf detail untuk modal berita; opsional.

Jika belum ada berita, halaman menampilkan pesan bahwa update akan muncul di sana. Karena berita dibaca menggunakan `fetch`, buka website melalui web server atau hosting statis, bukan langsung lewat `file://`.
