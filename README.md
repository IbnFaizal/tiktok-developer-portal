# TikTok Developer Pages (GitHub Pages)

Template website statis HTTPS menggunakan **GitHub Pages** untuk memenuhi kebutuhan URL saat mendaftarkan aplikasi di [TikTok for Developers](https://developers.tiktok.com/).

## File yang Tersedia

- `index.html` — Halaman utama aplikasi (**Website / App URL**)
- `privacy.html` — Halaman **Privacy Policy URL**
- `terms.html` — Halaman **Terms of Service URL**
- `callback.html` — Halaman **OAuth Redirect URI** (otomatis menampilkan `code`, `state`, dan `scopes`)
- `styles.css` — Styling responsif
- `.nojekyll` — Agar GitHub Pages menyajikan file statis apa adanya

## Cara Menyesuaikan Sebelum Upload

1. Ganti `MyApp` dengan nama aplikasi Anda di semua file `.html`.
2. Ganti `developer@example.com` dengan email kontak Anda yang aktif.
3. Ganti `USERNAME` dan `REPO_NAME` di `index.html` sesuai akun dan nama repository GitHub Anda.

## Cara Deploy ke GitHub Pages (Gratis & HTTPS)

1. Buat repository baru di GitHub (misalnya: `tiktok-dev-pages`), set **Public**.
2. Upload atau push seluruh isi folder ini ke branch `main`:
   ```bash
   git init
   git add .
   git commit -m "Initial TikTok Developer Pages"
   git branch -M main
   git remote add origin https://github.com/USERNAME/REPO_NAME.git
   git push -u origin main
   ```
3. Buka **Settings → Pages** di repository GitHub Anda:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main` / `/ (root)`
   - Klik **Save**.
4. Tunggu 1–2 menit hingga URL aktif:
   - **Website URL**: `https://USERNAME.github.io/REPO_NAME/`
   - **Privacy Policy URL**: `https://USERNAME.github.io/REPO_NAME/privacy.html`
   - **Terms of Service URL**: `https://USERNAME.github.io/REPO_NAME/terms.html`
   - **Redirect URI**: `https://USERNAME.github.io/REPO_NAME/callback.html`

## Verifikasi Domain TikTok (Jika Diminta)

Jika TikTok Developer Portal meminta verifikasi domain dengan file `.txt` (misalnya `tiktokXXXXXXXX.txt`):

1. Download file `.txt` dari dashboard TikTok for Developers.
2. Letakkan file tersebut di folder root repository ini (sejajar dengan `index.html`).
3. Commit dan push ke GitHub, lalu klik **Verify** di dashboard TikTok.
