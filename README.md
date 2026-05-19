# Voltcore - Legal Pages

Bu repo, **Voltcore** mobil oyununun yasal sayfalarını (Privacy Policy + Terms of Service) içerir.

## 🚀 Vercel'e Deploy

### Yöntem 1: Vercel Dashboard (Önerilen, en kolay)

1. [vercel.com](https://vercel.com) → **New Project**
2. **Import Git Repository** → bu GitHub repo'sunu seç
3. Framework Preset: **Other** (statik HTML)
4. Build Settings: **boş bırak** (statik dosyalar)
5. **Deploy** tıkla
6. ~30 saniye sonra hazır → URL: `https://[proje-adi].vercel.app`

### Yöntem 2: Vercel CLI

```bash
npm install -g vercel
cd neon-grid-legal
vercel
```

## 📋 Adımlar (Detaylı)

### 1. GitHub'a Push

```bash
cd neon-grid-legal

# Eğer ilk kez:
git init
git add .
git commit -m "Initial commit - Voltcore legal pages"
git branch -M main
git remote add origin https://github.com/[KULLANICI_ADI]/neon-grid-legal.git
git push -u origin main
```

### 2. E-posta Adresini Güncelle

Her 3 HTML dosyasında **`[YOUR_EMAIL_HERE]`** placeholder'ını gerçek e-postanla değiştir:

```bash
# Mac/Linux'ta hepsini birden değiştir:
sed -i '' 's/\[YOUR_EMAIL_HERE\]/sizin@example.com/g' *.html
```

### 3. Vercel'e Deploy

Yukarıdaki Yöntem 1'i takip et.

### 4. App Store Connect'e URL'leri Gir

Apple App Store Connect → My Apps → Voltcore → **App Information**:
- **Privacy Policy URL**: `https://[proje-adi].vercel.app/privacy.html`
- **Marketing URL** (opsiyonel): `https://[proje-adi].vercel.app`

## 📁 Dosya Yapısı

```
neon-grid-legal/
├── index.html        # Ana sayfa (Privacy + Terms link'leri)
├── privacy.html      # Gizlilik Politikası (TR + EN)
├── terms.html        # Kullanım Koşulları (TR + EN)
├── vercel.json       # Vercel yapılandırması
└── README.md         # Bu dosya
```

## 🌐 URL Yapısı (Deploy sonrası)

- `/` → Ana sayfa
- `/privacy.html` → Gizlilik Politikası
- `/terms.html` → Kullanım Koşulları

## ✏️ Özelleştirme

Sayfalar otomatik olarak tarayıcı diline (TR/EN) göre açılır. Kullanıcı dil değiştirme butonu da var.

Renkler / tasarım: Oyunla aynı neon cyan + magenta gradient teması.

## 📝 Notlar

- Bu sayfalar **App Store yayını için ZORUNLUDUR** (Apple Privacy Policy URL ister)
- Tüm sayfalar **mobile responsive**
- **Hiçbir analitik/tracking yok** (oyunla tutarlı)
