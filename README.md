# Ngerti AI Studio

Aplikasi produksi script & SEO untuk channel YouTube Ngerti AI.  
Ditenagai Gemini API, di-deploy di Vercel (gratis).

## Cara Deploy ke Vercel

### Langkah 1 — Upload ke GitHub

1. Buka [github.com](https://github.com) → klik **New repository**
2. Nama repo: `ngerti-ai-studio`
3. Biarkan kosong (jangan centang apapun) → klik **Create repository**
4. Upload semua file dari folder ini ke repo tersebut

### Langkah 2 — Dapat Gemini API Key

1. Buka [aistudio.google.com/apikey](https://aistudio.google.com/apikey)
2. Klik **Create API key**
3. Copy API key-nya (simpan, jangan share ke siapapun)

### Langkah 3 — Deploy ke Vercel

1. Buka [vercel.com](https://vercel.com) → login dengan GitHub
2. Klik **Add New Project** → pilih repo `ngerti-ai-studio`
3. Sebelum klik Deploy, buka bagian **Environment Variables**
4. Tambahkan:
   - **Name:** `GEMINI_API_KEY`
   - **Value:** paste API key dari langkah 2
5. Klik **Deploy**
6. Tunggu ~1 menit → aplikasi live di URL Vercel kamu

### Langkah 4 — Pakai

Buka URL Vercel → pilih tipe → isi input → generate script → generate SEO.

## Struktur File

```
ngerti-ai-studio/
├── api/
│   └── generate.js     ← server function (panggil Gemini API)
├── public/
│   └── index.html      ← tampilan aplikasi
├── vercel.json         ← konfigurasi Vercel
├── package.json
└── .gitignore
```

## Update Prompt

Kalau mau ubah prompt script atau SEO, edit file `api/generate.js` bagian atas (konstanta `PROMPT_TUTORIAL`, `PROMPT_NEWS`, `PROMPT_SEO`).  
Setelah edit dan push ke GitHub, Vercel otomatis re-deploy.
