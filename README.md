# Ente Metal Plastik — Web Sitesi

<<<<<<< HEAD
=======
<<<<<<< HEAD
>>>>>>> 68af64f364b022d24950fb5c1758e19b1d899d65
## Klasör yapısı
```
ente-metal-plastik/
├── index.html              → Ana sayfa (öne çıkan ürünler + tüm bölümler)
├── urunler.html             → Ayrı ürün kataloğu sayfası (arama + filtre + tüm ürünler)
├── css/style.css            → Tüm tasarım + animasyonlar
├── js/main.js               → Tüm etkileşim/animasyon mantığı (her iki sayfada ortak)
├── data/products.json       → ÜRÜNLER (admin panelinden yönetilir)
├── data/page_blocks.json    → Esnek reklam/duyuru blokları (admin panelinden yönetilir)
├── data/settings/           → Site ayarları, konusuna göre 7 ayrı dosyaya bölünmüş:
│     marka.json               → Logo, favicon, slogan, renkler
│     hero.json                → Ana sayfa giriş (hero) metinleri + sayaçlar
│     hakkimizda.json          → Hakkımızda metni + vizyon maddeleri + hizmet kartları
│     iletisim.json            → Telefon, adres, WhatsApp, harita/konum, sosyal medya
│     urunler_bolumu.json      → Ana sayfadaki "Öne Çıkanlar" bölümü metinleri
│     teklif_formu.json        → Teklif formu ayarları
│     ux.json                  → WhatsApp butonlarının açık/kapalı ayarları
├── images/                  → Ürün görselleri ve logo buraya yüklenir
└── admin/                   → Kod bilmeyen kişi için içerik yönetim paneli
```

## Admin panelinden neler değiştirilebilir?
`siteadresi.com/admin` adresine giren kişi, sol menüde şu bölümleri görür:

- **Site Ayarları** (7 alt bölüme ayrılmıştır, her biri kendi başlığıyla listelenir):
  1. Marka & Görünüm — **logo dahil** her şey (favicon, slogan, ana renkler)
  2. Ana Sayfa Giriş Bölümü (Hero) — büyük başlık, alt yazı, sayaçlar
  3. Hakkımızda & Hizmetlerimiz — açıklama metni, vizyon maddeleri, hizmet kartları
  4. İletişim Bilgileri & Konum — telefon, e-posta, adres, çalışma saatleri, harita
     konumu (**artık sadece adres/konum adını yazmak yeterli**, Google Haritalar'dan
     link kopyalamaya gerek yok), Instagram/LinkedIn linkleri
  5. Ana Sayfa - Ürünler Bölümü Metinleri
  6. Teklif Formu Ayarları
  7. Gelişmiş Ayarlar — WhatsApp butonlarının açık/kapalı durumu
- **Ürün Kataloğu Yönetimi** — ürün ekle/düzenle/sil (fotoğraf, ölçüler, malzeme,
  açıklama, "Ana Sayfada Öne Çıkar" ve "Sıralama" dahil — hepsi form alanı, kod yok).
- **Esnek Sayfa Blokları** — istenirse ana sayfaya ek duyuru/reklam blokları eklenir.

Her alanın üstünde ne işe yaradığını açıklayan bir ipucu (hint) metni vardır.
Bir alanı değiştirdiğinizde sağ tarafta (masaüstünde) canlı bir önizleme paneli
açılır; renkler kutu, görseller küçük resim, açık/kapalı alanlar rozet olarak
gösterilir.

## 1) VS Code'da canlı önizleme (domain almadan)
Bilgisayarında bunu görmek için dosyayı çift tıklayıp tarayıcıda AÇMA — çünkü veriler
<<<<<<< HEAD
=======
=======
## Yeni: Ayrı Ürünler Sayfası + Öne Çıkanlar
- Artık `urunler.html` adında, tüm ürünlerin arama/filtre ile listelendiği **ayrı bir
  katalog sayfası** var.
- Ana sayfadaki "Ürünlerimiz" bölümünde ise sadece admin panelinden **"Ana Sayfada
  Öne Çıkar"** işaretlenen ürünler, açılır-kapanır (spoiler/akordeon) kartlar
  halinde gösterilir. Karta tıklayınca kart aynı sayfada genişler; içindeki
  **"Detayları Gör"** butonu aynı ekranda tam detay penceresini açar,
  **"Yeni Sekmede Aç"** butonu ise o ürünü doğrudan `urunler.html` katalog
  sayfasında, yeni bir sekmede açar.
- Hiçbir ürün "Ana Sayfada Öne Çıkar" olarak işaretlenmezse, sistem otomatik
  olarak ilk 3 ürünü gösterir — yani hiçbir zaman boş görünmez.

## Klasör yapısı
```
ente-metal-plastik/
├── index.html          → Ana sayfa (öne çıkan ürünler + tüm bölümler)
├── urunler.html         → Ayrı ürün kataloğu sayfası (arama + filtre + tüm ürünler)
├── css/style.css        → Tüm tasarım + zenginleştirilmiş animasyonlar
├── js/main.js           → Tüm etkileşim/animasyon mantığı (her iki sayfada ortak)
├── data/products.json   → ÜRÜNLER (arkadaşın admin panelinden değiştirecek)
├── data/settings.json   → Telefon, adres, WhatsApp no, harita linki, animasyon ayarları vs.
├── images/              → Ürün görselleri buraya yüklenir
└── admin/               → Kod bilmeyen kişi için içerik yönetim paneli
```

## Admin panelinden neler değiştirilebilir?
- **Ürünler** koleksiyonunda her ürün için artık iki yeni alan var:
  - **Ana Sayfada Öne Çıkar** (açık/kapalı): işaretlenirse o ürün ana sayfadaki
    spoiler listede görünür.
  - **Sıralama**: küçük sayı önce gösterilir (hem ana sayfa hem katalogda).
- **Site Ayarları** koleksiyonuna eklenenler:
  - Öne Çıkanlar bölüm başlığı ve açıklaması (ana sayfa metni)
  - "Tüm Ürünler" buton metni
  - Kıvılcım/parçacık animasyonunu açma-kapama (performans veya tercih için)
  - Kalıp dolum animasyon hızı (ms)
- Telefon, adres, WhatsApp, harita linki, çalışma saatleri gibi tüm eski alanlar
  aynen duruyor ve admin panelinden değiştirilebiliyor.

## 1) VS Code'da canlı önizleme (domain almadan)
Bilgisayarında bunu göremek için dosyayı çift tıklayıp tarayıcıda AÇMA — çünkü ürünler
>>>>>>> 80260b39eab52adf43f35ace1fe9d98067357cf9
>>>>>>> 68af64f364b022d24950fb5c1758e19b1d899d65
`fetch` ile JSON'dan okunuyor ve tarayıcılar güvenlik nedeniyle `file://` üzerinden
buna izin vermiyor. Bunun yerine:

1. VS Code'da **"Live Server"** eklentisini kur (Extensions sekmesinden ara, kur).
2. `index.html` dosyasına sağ tıkla → **"Open with Live Server"**.
3. Tarayıcıda `http://127.0.0.1:5500` gibi bir adreste site açılacak.

<<<<<<< HEAD
=======
<<<<<<< HEAD
>>>>>>> 68af64f364b022d24950fb5c1758e19b1d899d65
## 2) Netlify'a yükleme ve domain bağlama
1. Bu proje klasörünü bir GitHub reposuna yükle.
2. [netlify.com](https://netlify.com) üzerinde hesap aç, **"Add new site" → "Import an
   existing project"** ile bu repoyu bağla. Build ayarı gerekmiyor (statik site),
   direkt yayınlanır. Sana ücretsiz bir `.netlify.app` linki verir.
3. **Site settings → Identity** kısmından Identity'yi aktif et.
4. Aynı yerde **Identity → Services → Git Gateway**'i de aktif et.
5. Identity sekmesinden yönetecek kişiye e-posta ile davet gönder ("Invite users").
   Davet linkine tıklandığında "Failed to load settings" gibi bir hata alınırsa,
   Identity'yi aktif ettikten SONRA yeniden davet göndermek genelde sorunu çözer;
   ayrıca reklam engelleyici eklentiler (uBlock, Brave Shields vb.) bu isteği
   engelleyebilir, gizli sekmede denemek işe yarar.
6. Kendi domainini (`entemetalplastik.com` gibi) **Domain settings** kısmından bu
   siteye bağlayabilirsin — kod hiç değişmez, domaini bağladıktan sonra Identity
   otomatik olarak yeni domainde de çalışır.

> Domaini Netlify'a bağladıktan sonra, admin daveti göndermeden önce Identity ve
> Git Gateway'in aktif olduğundan emin ol; sıra karışırsa "Trigger deploy → Clear
> cache and deploy site" ile yeni bir deploy tetiklemek genelde sorunu çözer.

## 3) WhatsApp numarasını değiştirme
Admin panelinden **Site Ayarları → İletişim Bilgileri & Konum** kısmından,
başında + ve boşluk OLMADAN, ülke kodlu numarayı gir. Örnek: `905551112233`

## 4) Google Haritalar konumu
Artık iframe/embed linki kopyalamaya gerek yok. **Site Ayarları → İletişim
Bilgileri & Konum** kısmındaki "Haritada Görünecek Konum" alanına firma adını
veya adresini yazman yeterli, harita otomatik oluşur.

## 5) Ürün görselleri
Admin panelinden ürün eklerken/düzenlerken fotoğrafı sürükle-bırak ile
yüklemen yeterli, otomatik olarak `images/` klasörüne kaydedilir.

---
Herhangi bir adımda takılırsan (Netlify kurulumu, GitHub'a yükleme, domain
bağlama, Identity/Git Gateway hataları) söyle, birlikte adım adım çözelim.
<<<<<<< HEAD
=======
=======
## 2) Ücretsiz canlı link ile paylaşma (domain almadan)
Domain almadan, gerçek bir linkle (ör. `ente-metal-plastik.netlify.app`) tasarımı
görmek/paylaşmak istersen:

1. [netlify.com](https://netlify.com) üzerinde ücretsiz hesap aç.
2. Bu proje klasörünü bir GitHub reposuna yükle (VS Code içinden "Source Control"
   sekmesinden kolayca yapılır — söylersen adım adım anlatırım).
3. Netlify'da **"Add new site" → "Import an existing project"** ile bu repoyu bağla.
   Build ayarı gerekmiyor (statik site), direkt yayınlanır.
4. Sana ücretsiz bir `.netlify.app` linki verir. Sonra istediğin zaman kendi
   domainini (`entemetalplastik.com` gibi) bu siteye bağlayabilirsin — kod hiç değişmez.

## 3) Arkadaşının kod bilmeden içerik eklemesi (admin panel kurulumu)
Bu adımlar **bir kereliğine** yapılır, sonrasında arkadaşın sadece `siteadresi.com/admin`
adresine girip formu dolduracak.

1. Site Netlify'a bağlandıktan sonra, Netlify panelinde **Site settings → Identity** kısmından
   Identity özelliğini aktif et.
2. Aynı yerde **"Git Gateway"** kısmını da aktif et.
3. Identity sekmesinden arkadaşına e-posta ile davet gönder ("Invite users").
4. Arkadaşın maildeki linke tıklayıp şifresini belirleyecek.
5. Artık `siteadresi.com/admin` adresine girip:
   - **Ürünler** kısmından yeni ürün ekleyebilir/düzenleyebilir/silebilir (ad, ölçüler,
     malzeme, açıklama, fotoğraf yükleme — hepsi form alanları, kod yok).
   - **Site Ayarları** kısmından telefon, adres, WhatsApp numarası, harita linkini
     güncelleyebilir.
6. Kaydettiği her değişiklik otomatik olarak siteye yansır (birkaç saniye - 1 dakika içinde).

> Bu adımı ben senin yerine yapamam çünkü Netlify hesabı ve GitHub reposu senin
> kontrolünde olmalı — ama istersen ekran ekran, adım adım birlikte kurarız.

## 4) WhatsApp numarasını değiştirme
`data/settings.json` içindeki `whatsapp_numara` alanına, başında + ve boşluk
OLMADAN, ülke kodlu numarayı yaz. Örnek: `905551112233`
(Bunu admin panelinden de değiştirebilecek.)

## 5) Google Haritalar linkini gerçek adresle değiştirme
1. [Google Maps](https://maps.google.com) üzerinde firmanın konumunu bul.
2. **Paylaş → Harita Göm (Embed a map)** seçeneğine tıkla.
3. Verilen `<iframe src="...">` içindeki `src="..."` linkini kopyala.
4. `data/settings.json` içindeki `harita_gomme_linki` alanına yapıştır.

## 6) Ürün görselleri
`images/` klasörüne fotoğrafları at, `data/products.json` içindeki `gorsel`
alanına dosya adını yaz (örn: `images/urun-4.jpg`). Admin panelinden eklerken
bu otomatik halloluyor, fotoğrafı sürükle bırak yeterli.

---
Herhangi bir adımda takılırsan (Netlify kurulumu, GitHub'a yükleme, domain
bağlama) söyle, o adımı birlikte ekran ekran yapalım.
>>>>>>> 80260b39eab52adf43f35ace1fe9d98067357cf9
>>>>>>> 68af64f364b022d24950fb5c1758e19b1d899d65
