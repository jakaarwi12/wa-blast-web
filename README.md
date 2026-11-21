# WA Auto Sender — Web Panel

Halaman kontrol web (GitHub Pages) untuk backend Node.js **WA Auto Sender** (Baileys + Express + Socket.IO).

Link: **https://jakaarwi12.github.io/wa-blast-web/**

## Cara pakai

1. Deploy backend Node.js-nya dulu ke hosting yang bisa menjalankan Node (Render, Railway, Firebase Cloud Functions, VPS, dll).
2. Buka link di atas.
3. Isi **URL backend** pada panel **Koneksi Server Node.js**, lalu klik **Simpan & Hubungkan**.
4. Setelah status berubah jadi **TERHUBUNG**, semua tombol (pairing, target, kirim, auto-reject) berfungsi seperti di APK.

Alternatif cepat: buka langsung

```
https://jakaarwi12.github.io/wa-blast-web/?backend=https://alamat-backend-anda
```

## Catatan

- Halaman ini **statik** (GitHub Pages tidak bisa menjalankan Node.js). Proses WhatsApp tetap berjalan di backend.
- Backend harus mengizinkan CORS. Di `index.js` sudah ditambahkan `cors: { origin: '*' }` pada `new Server(server, ...)`.
- Sesi WhatsApp (`sesi_wa`) harus disimpan di storage persisten milik hosting. Free tier Render/Railway bisa hilang saat restart; pakai volume/disk persisten kalau tersedia.
- Kode backend ada di repo privat: `jakaarwi12/wa-blast-app` (folder `nodejs-project`).
