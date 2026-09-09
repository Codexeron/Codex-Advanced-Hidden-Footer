# 🌐 Codex Advanced Hidden Footer

Modern, responsive ve etkileşimli bir **çok dilli footer/taskbar component**. Proje; dil değiştirme, karanlık/aydınlık tema, arama ve kategori filtreleme, newsletter aboneliği, toast bildirimleri ve responsive tasarım özelliklerini tek bir frontend yapısında bir araya getirir.

Tamamen **HTML5, CSS3 ve Vanilla JavaScript** ile geliştirilmiştir. Herhangi bir frontend framework'üne ihtiyaç duymaz.

## ✨ Özellikler

* 🌍 **Çoklu dil desteği**

  * 🇹🇷 Türkçe
  * 🇬🇧 English
  * 🇩🇪 Deutsch
  * 🇫🇷 Français
* 🌙 **Dark / Light Mode**
* 💾 Tema ve dil tercihlerinin `localStorage` ile saklanması
* 📂 Açılıp kapanabilen modern footer/taskbar
* 🔎 Gerçek zamanlı içerik arama
* 🏷️ Kategori bazlı filtreleme
* 📊 Dinamik içerik sayacı
* 📧 Newsletter abonelik formu
* 🔔 Toast notification sistemi
* 📱 Responsive tasarım
* ✨ Smooth CSS animasyonları
* 🎨 Glassmorphism tabanlı footer tasarımı
* 📈 Sayfa scroll ilerleme çubuğu
* ♿ Accessibility için temel ARIA desteği
* ⚡ Framework bağımlılığı olmadan hızlı frontend yapısı

## 🛠️ Kullanılan Teknolojiler

| Teknoloji        | Kullanım                                 |
| ---------------- | ---------------------------------------- |
| HTML5            | Sayfa yapısı ve semantik markup          |
| CSS3             | Tasarım, responsive yapı ve animasyonlar |
| JavaScript       | Etkileşim ve uygulama mantığı            |
| LocalStorage API | Dil ve tema tercihlerini saklama         |
| Font Awesome     | İkonlar                                  |
| Google Fonts     | Poppins font ailesi                      |

## 📁 Proje Yapısı

```text
multilingual-footer/
│
├── index.html
└── README.md
```

Tek dosyalı yapı sayesinde proje kolayca indirilebilir ve herhangi bir web sunucusuna ihtiyaç duyulmadan tarayıcıda çalıştırılabilir.

## 🚀 Kurulum

Projeyi klonlayın:

```bash
git clone https://github.com/USERNAME/multilingual-footer.git
```

Proje klasörüne girin:

```bash
cd multilingual-footer
```

Ardından `index.html` dosyasını tarayıcıda açın.

Herhangi bir build işlemi veya paket kurulumu gerekmez.

## 🌍 Dil Sistemi

Çoklu dil sistemi `data-i18n` attribute'ları üzerinden çalışır.

Örnek:

```html
<h1 data-i18n="heroTitle"></h1>
```

JavaScript içerisindeki çeviri sözlüğü:

```javascript
const translations = {
    tr: {
        heroTitle: "Merhaba, Dünya"
    },
    en: {
        heroTitle: "Hello, World"
    },
    de: {
        heroTitle: "Hallo, Welt"
    },
    fr: {
        heroTitle: "Bonjour, Monde"
    }
};
```

Bu yapı sayesinde yeni diller kolayca sisteme eklenebilir.

## 🌙 Tema Sistemi

Tema tercihi `localStorage` üzerinde saklanır.

```javascript
localStorage.setItem("theme", "dark");
```

CSS tarafında tema değişkenleri kullanılır:

```css
:root {
    --bg-primary: #f4f7fc;
    --text-primary: #1e293b;
}

[data-theme="dark"] {
    --bg-primary: #0f172a;
    --text-primary: #f1f5f9;
}
```

Bu yaklaşım sayesinde renk paletinin tamamı merkezi olarak yönetilebilir.

## 🔎 Arama ve Filtreleme

Kartlar üzerinde gerçek zamanlı arama yapılabilir.

Ayrıca içerikler kategoriye göre filtrelenebilir:

```text
Tümü
Teknoloji
Sağlık
Eğitim
```

Arama ve kategori filtresi aynı anda çalışarak daha hassas sonuçlar üretir.

## 📧 Newsletter

Frontend tarafında e-posta formatı kontrol edilerek kullanıcıya abonelik sonucu gösterilir.

> **Not:** Mevcut demo sürümünde newsletter formu gerçek bir e-posta servisinin veya backend API'sinin yerine geçmez. Production kullanımında backend, veritabanı, e-posta doğrulama, rate limiting ve unsubscribe mekanizması eklenmelidir.

## 🔔 Toast Notification

Kullanıcı işlemleri modern toast bildirimleriyle gösterilir.

Örnek kullanım:

```javascript
showToast(
    "Tema değiştirildi",
    "Karanlık mod aktif."
);
```

Toast sistemi şu işlemlerde kullanılabilir:

* Dil değişikliği
* Tema değişikliği
* Newsletter aboneliği
* Başarılı işlemler
* Hata mesajları

## 📱 Responsive Tasarım

Arayüz farklı ekran boyutlarına uyum sağlar:

```text
Desktop
   ↓
Tablet
   ↓
Mobile
```

Footer kolonları ekran genişliğine göre otomatik olarak yeniden düzenlenir.

## 🎨 Tasarım Yaklaşımı

Proje modern web arayüzlerinden ilham alan bir tasarım anlayışı kullanır:

* Glassmorphism
* Rounded corners
* Soft shadows
* Smooth transitions
* Hover effects
* Minimal color palette
* Responsive grid
* Modern taskbar footer

Amaç, klasik footer yapısından daha etkileşimli ve modern bir kullanıcı deneyimi oluşturmaktır.

## 🔐 Güvenlik Notu

Bu proje frontend ağırlıklı bir demo/component yapısıdır.

Production ortamında aşağıdaki güvenlik önlemleri ayrıca uygulanmalıdır:

* Backend-side input validation
* XSS protection
* CSRF protection
* Rate limiting
* E-mail verification
* Server-side newsletter validation
* Content Security Policy (CSP)
* Secure cookie configuration
* HTTPS
* API authentication

Özellikle kullanıcı tarafından gönderilen veriler doğrudan `innerHTML` içerisine aktarılmamalı; güvenilir olmayan veriler için `textContent` veya uygun escaping yöntemleri kullanılmalıdır.

## 🔮 Gelecek Geliştirmeler

* [ ] Backend newsletter API
* [ ] PostgreSQL entegrasyonu
* [ ] Admin paneli
* [ ] Daha fazla dil
* [ ] Kullanıcı hesabına bağlı dil tercihi
* [ ] Kullanıcı hesabına bağlı tema tercihi
* [ ] GDPR / KVKK uyumlu abonelik sistemi
* [ ] E-posta doğrulama
* [ ] Newsletter yönetim paneli
* [ ] Sosyal medya bağlantılarının yapılandırılması
* [ ] Accessibility iyileştirmeleri
* [ ] `prefers-reduced-motion` desteği
* [ ] PWA desteği

## 📄 Lisans

Bu projenin lisans koşulları için repository içerisindeki lisans dosyasını inceleyin.

## ⭐ Destek

Projeyi faydalı bulduysanız repository'ye ⭐ bırakabilir ve geliştirme önerilerinizi **Issues** bölümünden paylaşabilirsiniz.

---

### 🚀 Proje Özeti

**Multilingual Interactive Footer**, modern web sitelerinde kullanılabilecek yeniden kullanılabilir bir footer/taskbar konseptidir.

**HTML5 + CSS3 + Vanilla JavaScript**

Basit, hızlı, responsive ve geliştirilebilir.
