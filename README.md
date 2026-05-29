# NEXUS ARENA 2225 — Kurulum Rehberi

## Klasör Yapısı
```
arena-project/
├── public/
│   └── index.html       ← Ana site dosyası
├── api/
│   └── chat.js          ← Backend (API anahtarını gizler)
├── vercel.json          ← Vercel ayarları
└── README.md
```

## Deploy Adımları

### 1. GitHub'a Yükle
1. github.com'a giriş yap
2. Sağ üstte "+" → "New repository" tıkla
3. Repository adı: `nexus-arena`
4. "Public" seç → "Create repository" tıkla
5. Açılan sayfada "uploading an existing file" linkine tıkla
6. Tüm dosyaları sürükle-bırak (klasör yapısını koru)
7. "Commit changes" tıkla

### 2. Vercel'e Bağla
1. vercel.com'a giriş yap
2. "Add New Project" tıkla
3. GitHub'daki `nexus-arena` reposunu seç → "Import"
4. Deploy et — henüz API anahtarı yok ama devam et

### 3. API Anahtarını Ekle
1. Vercel'de projeye gir → "Settings" → "Environment Variables"
2. Name: `GEMINI_API_KEY`
3. Value: Google AI Studio'dan aldığın uzun kodu yapıştır
4. "Save" tıkla
5. Üstte "Deployments" → en son deployment → "Redeploy"

### 4. Kullanıcı Adı ve Şifre Belirle
`public/index.html` dosyasını aç, şu satırları bul ve değiştir:
```
const VALID_USERNAME = "KULLANICI_ADINIZI_YAZIN";
const VALID_PASSWORD = "SIFRENIZI_YAZIN";
```
Kendi kullanıcı adı ve şifreni yaz, kaydet, GitHub'a tekrar yükle.

### 5. Hazır!
Vercel sana `.vercel.app` uzantılı ücretsiz bir URL verir.
Sadece sen girebilirsin.
