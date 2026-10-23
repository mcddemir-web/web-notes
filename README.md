# Web Notları (PWA)

Web'de gördüğün önemli şeyleri (metin, bağlantı, ekran görüntüsü) kategorilere ayırıp **private** bir GitHub deposuna Markdown olarak kaydeder.

Bu depo yalnızca uygulamanın kodudur, içinde not verisi yoktur. Notlar ayrı bir private depoda (`web-notes`) tutulur.

## Kurulum

1. **Not deposu:** GitHub'da `web-notes` adında **Private** bir depo oluştur ("Add a README file" işaretli olsun).
2. **Uygulama deposu:** `web-notes-app` adında **Public** bir depo oluştur, bu klasördeki dosyaları yükle (index.html, manifest.webmanifest, sw.js, *.png).
3. **Pages:** `web-notes-app` > Settings > Pages > Source: *Deploy from a branch* > `main` / `(root)`. Adres: `https://mcddemir-web.github.io/web-notes-app/`
4. **Token:** GitHub > Settings > Developer settings > Fine-grained tokens > Generate new token.
   - Repository access: *Only select repositories* > `web-notes`
   - Permissions: *Contents: Read and write* (Metadata otomatik)
5. Telefonda adresi aç, **Ayarlar** sekmesine token'ı yapıştır, "Kaydet ve dene" de.
6. **Ana ekrana ekle:**
   - Android (Chrome): menü > *Uygulamayı yükle / Ana ekrana ekle*
   - iOS (Safari): Paylaş > *Ana Ekrana Ekle*

## Kullanım

- **Yeni not:** kategori seç, metni yapıştır, görsel ekle (galeri/kamera veya metin kutusuna yapıştır), Kaydet.
- **Android paylaşım menüsü:** uygulama yüklendikten sonra Chrome'da Paylaş > *Notlar* ile sayfa bağlantısı/seçili metin doğrudan forma gelir.
- **Çevrimdışı:** internet yoksa not cihazda bekler, bağlantı gelince otomatik gönderilir.
- **Notlar sekmesi:** kategoriye göre notları listeler, dokununca GitHub'da açar.

## Depo düzeni (`web-notes`)

```
kategoriler.json
notlar/<kategori>/2026-10-24-020600-baslik.md
ekler/2026/2026-10-24-020600-1.png
```
