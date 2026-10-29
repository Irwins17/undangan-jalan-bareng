# Undangan Jalan Bareng 💌

Undangan kencan interaktif satu halaman (HTML statis, tanpa build).
Buka amplop → pilih rencana → tiket "JALAN KEGIATAN" dikirim lewat WhatsApp.

## Isi folder
- `index.html` — seluruh aplikasi (HTML + CSS + JS jadi satu file)
- `vercel.json` — konfigurasi kecil untuk Vercel
- `README.md` — file ini

Tidak perlu `npm install` atau build apa pun. Ini situs statis murni.

---

## Cara deploy ke Vercel lewat GitHub

### 1) Taruh di GitHub
1. Buka https://github.com/new, buat repo baru, misal `undangan-jalan-bareng` (boleh Public/Private).
2. Upload isi folder ini (`index.html`, `vercel.json`, `README.md`) ke repo:
   - **Cara mudah:** di halaman repo baru, klik **"uploading an existing file"**, drag ketiga file, lalu **Commit**.
   - **Atau lewat git:**
     ```bash
     git init
     git add .
     git commit -m "undangan jalan bareng"
     git branch -M main
     git remote add origin https://github.com/USERNAME/undangan-jalan-bareng.git
     git push -u origin main
     ```

### 2) Hubungkan ke Vercel
1. Masuk ke https://vercel.com (login pakai akun GitHub).
2. Klik **Add New… → Project**, lalu **Import** repo `undangan-jalan-bareng`.
3. Biarkan semua pengaturan default:
   - **Framework Preset:** `Other`
   - **Build Command:** kosongkan
   - **Output Directory:** kosongkan (root)
4. Klik **Deploy**. Tunggu beberapa detik.
5. Selesai! Kamu dapat link seperti `https://undangan-jalan-bareng.vercel.app`.

Setiap kali kamu ubah `index.html` dan push ke GitHub, Vercel otomatis deploy ulang.

---

## Cara pakai setelah online
1. Buka link Vercel-mu.
2. Isi **Buat siapa**, **Dari siapa**, **Nomor WhatsApp kamu**, lalu **Mulai**.
3. Salin URL di address bar (sudah mengandung data undangan setelah `#...`).
4. Kirim URL itu ke orangnya. Pas dia buka → langsung ke amplop, isi rencana, lalu **Kirim ke WhatsApp** (balasan masuk ke nomor kamu).

## Ganti teks default
Buka `index.html`, cari bagian paling atas `<script>`:
```js
const CONFIG = {
  question: "weekend ini mau jalan bareng aku gak?",
  note:     "oke fix yaa, aku tunggu rencana pilihan kamu. gak boleh kabur wkwk"
};
```
Ubah sesukamu, commit & push — Vercel update otomatis.
