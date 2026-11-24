# TikTok Developer Portal (GitHub Pages)

Repository **Public** untuk menyajikan URL HTTPS statis dan file verifikasi kepemilikan yang dibutuhkan oleh [TikTok for Developers](https://developers.tiktok.com/).

## Struktur Folder Saat Ini

```text
tiktok-dev-pages/
├── .gitignore                                          # Mencegah file sensitif (.env, secret) ter-commit
├── .nojekyll                                           # Nonaktifkan Jekyll agar file disajikan langsung
├── README.md
├── index.html                                          # Website / Web/Desktop URL
├── styles.css                                          # Stylesheet utama
├── callback.html                                       # OAuth 2.0 Redirect URI
├── tiktokoOJywNJtd2Atox9uxrOUNmdyrwtScjGI.txt          # Verifikasi root (Web/Desktop URL)
├── privacy/
│   ├── index.html                                      # Privacy Policy (/privacy/)
│   └── tiktokH9ltPPSwpZbvhvgwqD3JwT8N6Kx7f7UC.txt      # Verifikasi Privacy Policy
├── privacy.html/
│   ├── index.html                                      # Privacy Policy (/privacy.html/)
│   └── tiktokH9ltPPSwpZbvhvgwqD3JwT8N6Kx7f7UC.txt      # Verifikasi Privacy Policy (.html/)
├── terms/
│   ├── index.html                                      # Terms of Service (/terms/)
│   └── tiktokm3XQpYe04mK09rWFQevqZLd47ChKLCon.txt      # Verifikasi Terms of Service
└── terms.html/
    ├── index.html                                      # Terms of Service (/terms.html/)
    └── tiktokm3XQpYe04mK09rWFQevqZLd47ChKLCon.txt      # Verifikasi Terms of Service (.html/)
```

## Catatan Keamanan: Public vs Private (Hidden)

- **Tidak ada file yang bisa di-hidden di repository GitHub Public:** Semua file yang di-commit ke branch `main` di repo Public otomatis terlihat oleh publik (dan memang dibutuhkan agar TikTok & pengguna bisa membukanya).
- **Semua file di repo ini aman untuk publik:** HTML, CSS, `callback.html` (hanya membaca `code` di sisi browser), serta `tiktok*.txt` (hanya signature verifikasi domain) tidak mengandung rahasia apa pun.
- **Yang wajib Private (jangan pernah taruh di repo ini):** `CLIENT_SECRET`, `access_token`, `refresh_token`, `.env`, dan kode backend. Semua itu sudah diblokir oleh `.gitignore` dan harus disimpan di repository **Private** atau server terpisah.
