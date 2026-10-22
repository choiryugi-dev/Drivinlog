# 🌿 D-rive

> Catatan berkendara untuk mobil **bensin & listrik (EV)** — jarak sekali isi/charge, rute pemberhentian, waktu tempuh, efisiensi, biaya per km, pencatatan tol, dan pengingat servis/pajak.
> A driving log for **petrol & EV** cars — distance per fill/charge, stop-by-stop routes, travel time, efficiency, cost per km, toll logging, and service/tax reminders.

Satu halaman HTML, tanpa server, tanpa akun. Semua data tersimpan di perangkat (localStorage) dan bisa jalan offline sebagai PWA.
A single HTML page — no server, no account. All data lives on your device (localStorage) and works offline as a PWA.

---

## ✨ Fitur / Features

- **Mobil bensin & EV** — merek, tipe, range per charge/tangki, ikon emoji atau foto URL.
- **Sesi isi/charge** — tanggal pengisian, kWh/%/liter, biaya; otomatis hitung **jarak sekali isi**, efisiensi **km/kWh · km/L**, dan **biaya per km**.
- **Mulai–Selesai berkendara** — jarak & waktu tempuh, opsi **ukur jarak via GPS**.
- **Sisa range** — catat saat berangkat & tiba → **konsumsi nyata** vs klaim pabrik.
- **Jeda / Mampir** — catat tempat pemberhentian (makan, belanja, charge, istirahat, dll).
- **Pencatatan tol** — catat tiap gerbang + tarif sambil jalan, tanpa menjeda.
- **Statistik** — grafik tren efisiensi, biaya 6 bulan, jangkauan nyata.
- **Pengingat** — servis (km/tanggal) & pajak/STNK.
- **Rute Google Maps** — navigasi multi-stop + peta sematan.
- **Bilingual** 🇮🇩 / 🇬🇧, ekspor **CSV** & backup **JSON**.

---

## 🚀 Deploy

### Netlify (tersambung ke GitHub) — otomatis
1. Fork / push repo ini ke GitHub.
2. Netlify → **Add new site → Import an existing project** → pilih repo ini.
3. Build command: *(kosongkan)* · Publish directory: `.`
4. Deploy. Setiap `git push` otomatis update situs. (`netlify.toml` sudah disertakan.)

### GitHub Pages
1. Repo → **Settings → Pages**.
2. Source: **Deploy from a branch** → branch `main`, folder `/ (root)`.
3. Simpan. Situs terbit di `https://<user>.github.io/<repo>/`.

### Lokal / Local
Buka `index.html` langsung di browser. Catatan: fitur **GPS** & **install PWA** hanya aktif di koneksi **HTTPS** (mis. setelah di-deploy), bukan dari `file://`.

---

## 🔧 Sebelum deploy / Before deploy

Di `index.html`, ganti placeholder `https://d-rive.com` (2 baris bertanda komentar) dengan domain finalmu agar preview link/WhatsApp & kanonik benar. Opsional untuk sekadar menjalankan.

---

## 📁 Struktur / Structure

```
index.html            # seluruh aplikasi (HTML + CSS + JS)
manifest.webmanifest  # metadata PWA
sw.js                 # service worker (offline)
og.png                # preview gambar sosial (1200×630)
icon-192.png          # ikon PWA
icon-512.png          # ikon PWA
netlify.toml          # konfigurasi Netlify
```

## 🔒 Privasi / Privacy
Tidak ada data yang dikirim ke mana pun. Semua tersimpan lokal di browser perangkatmu.
No data is sent anywhere. Everything is stored locally in your device's browser.

## 📄 Lisensi / License
MIT — lihat [LICENSE](LICENSE).
