# TikTok Developer Portal (GitHub Pages)

Repository **Public** untuk menyajikan URL HTTPS statis yang dibutuhkan oleh [TikTok for Developers](https://developers.tiktok.com/).

## Struktur Folder

```text
tiktok-dev-pages/
├── .gitignore
├── .nojekyll
├── README.md
├── index.html                                          # Website / App URL
├── styles.css                                          # Stylesheet utama
├── terms.html                                          # Terms of Service URL
├── callback.html                                       # OAuth 2.0 Redirect URI
├── tiktokH9ltPPSwpZbvhvgwqD3JwT8N6Kx7f7UC.txt          # Verifikasi domain root
└── privacy.html/
    ├── index.html                                      # Privacy Policy URL
    └── tiktokH9ltPPSwpZbvhvgwqD3JwT8N6Kx7f7UC.txt      # Verifikasi prefix privacy.html/
```

## Pembagian Public vs Private

### 1. Yang HARUS di Public (Repository GitHub Pages ini)
Seluruh file di repo ini memang dirancang untuk diakses publik oleh server TikTok dan pengguna:
- `index.html` — `https://ibnfaizal.github.io/tiktok-developer-portal/`
- `privacy.html/` — `https://ibnfaizal.github.io/tiktok-developer-portal/privacy.html/`
- `terms.html` — `https://ibnfaizal.github.io/tiktok-developer-portal/terms.html`
- `callback.html` — `https://ibnfaizal.github.io/tiktok-developer-portal/callback.html` *(aman di publik karena hanya membaca `code` dari URL browser, tanpa menyimpan secret)*
- `tiktok*.txt` — File verifikasi kepemilikan URL untuk TikTok

### 2. Yang HARUS di Private (JANGAN taruh di repo ini!)
Simpan di **repository Private terpisah** atau **server/backend pribadi** Anda:
- `CLIENT_SECRET` dari TikTok Developer Portal
- `access_token` dan `refresh_token` pengguna
- File `.env`, kredensial API, atau database
- Backend service yang menukar `authorization code` menjadi `access_token`
