# 🏛️ Roma Tarihi Portali - Ebedi Gorkem Dijital Platformu

Bu dökümantasyon, Web Tasarım Ödevi kapsamında geliştirilen 
"Roma Tarihi Portalı" web uygulamasının mimari yapısını, 
kullanılan ileri seviye CSS3/JavaScript teknolojilerini 
ve responsive arayüz isterlerine yönelik teknik çözümleri 
en ince ayrıntısına kadar açıklamaktadır.

---

## 📂 BOLUM 1: Odev Sahibi ve Gelistirici Bilgileri

* **Gelisitirici Adi Soyadi:** Caner Mercan
* **Odev Statusu:** Web Tasarim Odevi (Donem Ici Standart Odev Calismasi)
* **Odev Temasi:** Antik Roma'nın Tarihsel Dönemlerini 
  (Krallik, Cumhuriyet, Bati Roma, Bizans) ve Tarihe Yon Veren 
  Liderlerini Sergileyen Cok Sayfali (Multi-Page) Dijital Portal

---

## 🛠️ BOLUM 2: Kullanilan Teknolojiler ve Versiyon Kontrolu

Odevin on yuz mimarisi ve versiyon takibi tamamen modern 
web standartlarina ve endustriyel pratiklerine uygun olarak 
yapilandirilmistir:

* **HTML5:** nav, header, main, section, footer gibi 
  anlamsal (Semantic) etiketler kullanilarak SEO ve 
  erisilebilirlik standartlarina uygun arayuz iskeleti kurulmustur.
* **CSS3:** Moduler stil yonetimi, ozel animasyonlar, 
  geometrik kesim algoritmalari ve responsive katmanlar 
  sifardan kodlanmistir. Herhangi bir harici UI kütüphanesi 
  yuku bindirilmedigi icin maksimum performans elde edilmistir.
* **Modern JavaScript (ES6+):** Tarayici olay tetikleyicileri 
  (Event Listeners), kaydirma vektoru takibi (Scroll Tracking) 
  ve dinamik sinif manipulasyonlari etkin olarak kullanilmistir.
* **Git & GitHub:** Ödevin tüm geliştirme süreçleri lokalde 
  Git yazılımı ile takip edilmiş ve GitHub üzerinde uzak depoya 
  güvenli bir şekilde aktarılmıştır.

---

## 💻 BOLUM 3: Terminal Uzerinden Git Sürüm Kontrol Yönetimi

Projenin yerel bilgisayardaki geliştirme aşamalarından 
itibaren terminal üzerinde aşağıdaki komut mimarisi 
sırasıyla işletilerek sürüm kontrolü yapılmıştır:

> 📂 **1. Yerel Deponun Başlatılması**
> ```bash
> git init
> # Proje kok dizininde bos bir Git
> # reposu olusturuldu. Degisiklikler
> # anlik olarak izlenmeye baslandi.
> ```

> 🔍 **2. Dosyaların Takip Listesine Alınması**
> ```bash
> git add .
> # Projedeki tum HTML, CSS ve resim
> # dosyalari hazirlik alanina
> # guvenle dahil edildi.
> ```

> 💾 **3. Değişikliklerin Yerel Depoya Kaydedilmesi**
> ```bash
> git commit -m "Roma Tarihi Portali"
> # Hazirlik alanindaki tum dosyalar
> # yerel Git veritabanina kalici
> # olarak muhurlendi.
> ```

> 🔗 **4. Uzak Depo Bağlantısı ve Push**
> ```bash
> git branch -M main
> git remote add origin https://github.com/caner-mercan/web_tasarim_final_odevi.git
> git push -u origin main
> # Ana dal main yapildi, GitHub
> # uzak sunucu adresi baglandi ve
> # tum kodlar yuklendi.
> ```

---

## 🔄 BOLUM 4: Donanim Ivmeli Giriş Animasyonlari (keyframes Architecture)

Kullanıcının siteye giriş anındaki ilk etkileşim kalitesini 
ve akıcılığı (FPS) artırmak amacıyla tarayıcının donanım ivmesini 
tetikleyen bir giriş katmanı kurgulanmıştır:

* **fadeInPage Mekanizmasi:** Sayfa govdesi (body) yuklendigi 
  anda calisan bu animasyon, tum DOM agacini dikey eksende 
  translateY(30px) konumundan translateY(0) konumuna dogru 
  yumusak bir interpolasyonla tasir.
* **Opaklik Gecisi:** Es zamanli olarak elemanların gorunurlugu 
  (opacity) 0'dan 1'e yukselerek 1.2 saniyelik bir zaman zarfinda 
  sayfaya sinematik bir derinlik kazandırır.

---

## 💻 BOLUM 5: Yon Duyarli Akilli Navigasyon ve JavaScript DOM Manipulasyonu

Kullanici deneyimini (UX) maksimize etmek ve icerik okuma alanini 
genisletmek amaciyla JavaScript tabanli anlik scroll izleme motoru 
yazilmistir:

* **Yon Algilama Algoritmasi:** Tarayicinin dikey eksendeki 
  hareketleri window.addEventListener("scroll") olayı ile yakalanır. 
  pageYOffset veya document.documentElement.scrollTop degerleri 
  uzerinden bir onceki kaydırma konumu ile anlik konum karsilastirilir.
* **Dinamik Sinif Enjeksiyonu:** Eger kullanici sayfayi asagi 
  kaydiriyorsa ve dikey esik 100px'i gecmisse, JavaScript DOM 
  manipulasyonu ile nav etiketine .nav-hidden sinifi eklenir. 
  Kullanici yukari kaydırmaya basladigi anda bu sinif kaldirilir 
  ve menu ekrana geri gelir.

---

## 🎨 BOLUM 6: Asimetrik Geometrik Kesimler ve Gorsel Bölücüler (clip-path)

Web arayuzundeki dogrusal monotonlugu kirmak ve tarihsel kirilma 
anlarini gorsel olarak vurgulamak amaciyla matematiksel kesim 
modelleri uygulanmistir:

* **M.S. 395 Bolunme Ayraci:** Ana sayfada Imparatorlugun ikiye 
  ayrilisini temsil eden .dual-wrap alani, ust and alt bolumlerdeki 
  geometrik yerlesimlerle sayfaya dinamik bir akis hissi katmistir. 
  Klasik duz cizgiler yerine CSS3'ün modern yerleşim sinirlari 
  kullanilmistir.

---

## 🔁 BOLUM 7: Esnek Odakli Indeks Modulu (Dual-Wrap Flex Interactivity)

Bati Roma ve Doğu Roma (Bizans) medeniyetlerinin karsilastirildigi 
interaktif alan, CSS Flexbox esnekligi and animasyon senkronizasyonu 
ile insa edilmistir:

* **Dengeli Dagilim:** Genis ekranlarda .dual-wrap kapsayicisi 
  icindeki .side elemanlari flex: 1 degeriyle ekrani tam olarak 
  yari yariya (%50 - %50) paylasir.
* **Hover Odaklanma Dinamiği:** Fare ile herhangi bir kanadın 
  (Bati veya Doğu) uzerine gelindiğinde (:hover), ilgili elementin 
  esneklik katsayısı ve genisligi yumusak bir gecisle artar. 
  Bu mikro etkileşim ekran odağını ilgili medeniyete kaydırır.

---

## 💾 BOLUM 8: Parallaks Arka Plan ve Katmanli Derinlik Yonetimi

Gorsel zenginligin web performansini dusurmesini engellemek 
adina CSS tabanli hafif bir katmanlama teknik kullanilmistir:

* **Fixed Arka Plan:** Imparatorlugun yuzyillar icindeki sinir 
  degisimlerini gosteren detayli harita gorseli (image_4.jpg), 
  background-attachment: fixed niteliğiyle tarayıcı penceresine 
  kilitlenmiştir.
* **Parallaks Illuzyonu:** Kullanici sayfayı dikey eksende 
  kaydırdıkça, ön plandaki metin kutuları, butonlar ve şeffaf 
  kart katmanları hareket ederken arka plandaki harita sabit kalır. 
  Bu durum kullanıcıya web sitesinde üç boyutlu bir derinlik algısı sunar.

---

## 📱 BOLUM 9: Coklu Ekran Adaptasyonu (Responsive Grid & Flexbox)

Portalin tum cihaz jenerasyonlarinda (Mobil, Tablet, Masaüstü) 
gorsel bir kirilma yasamadan calismasi esnek yerlesim 
algoritmalariyla garanti altina alinmistir:

* **Duyarlı Izgara Sistemi:** Tarihe yon verenler galerisi 
  (.people-grid) ve donem kesif kartlari (.card-grid), esnek 
  sarma (flex-wrap: wrap) ve dinamik genislik kontroluyle tasarlanmistir.
* **Medya Sorguylari (Media Queries):** Mobil dikey ekranlarda 
  tek sütun halinde listelenen yapılar, ekran genisligi arttığı 
  anda otomatik olarak yan yana çoklu matris düzenine adapte olur 
  ve taşmaları engeller.

---

## 📂 BOLUM 10: Detayli Klasor ve Proje Dosya Yapısı

Proje dizini, tarayıcıların ve bulut sunucuların hiyerarşik 
olarak dosyaları kayıpsız okuyabilmesi için kök dizinde 
şu yapıda organize edilmiştir:

* **index.html:** Portal Giriş Kapısı (Ana Zaman Çizelgesi ve Özet Alanları)
* **krallar.html:** Roma Krallığı Dönemi Alt Bilgi Sayfası
* **cumhuriyet.html:** Roma Cumhuriyeti Dönemi Alt Bilgi Sayfası
* **bati-roma.html:** Batı Roma İmparatorluğu Alt Bilgi Sayfası
* **bizans.html:** Doğu Roma / Bizans İmparatorluğu Alt Bilgi Sayfası
* **style.css:** Tipografi, Renk Teorisi, Animasyon ve Layout Yönetim Dosyası
* **image_0.jpg:** Krallık Dönemi Temsili Görseli
* **image_1.jpg:** Doğu Roma / Konstantinopolis Görseli
* **image_2.jpg:** Cumhuriyet Dönemi Zafer Alayı Görseli
* **image_3.jpg:** Roma Forumu ve Çöküş Temalı Görsel
* **image_4.jpg:** Arka Planda Kullanılan Büyük Tarihi Roma Haritası
* **roman_1.jpg:** Tarihe Yön Verenler: Jül Sezar Portresi
* **roman_2.jpg:** Tarihe Yön Verenler: Caesar Augustus Portresi
* **roman_3.jpg:** Tarihe Yön Verenler: İmparator Neron Portresi
* **roman_4.jpg:** Tarihe Yön Verenler: İmparator Justinianus Portresi

---

## 💻 BOLUM 11: Lokal Geliştirme ve Dağıtım Ortamı Simülasyonu

Projenin yerel bilgisayarlarda (localhost) sorunsuz bir sekilde 
test edilebilmesi ve tarayici dosya protokolü kısıtlamalarına 
takılmamasi için iki temel simülasyon stratejisi belirlenmiştir:

> 📄 **File Protokolu Kisitlamalari (file:///)**
> Proje, saf HTML5 ve CSS3 mimarisiyle kuruldugu icin kok dizindeki 
> index.html dosyasina cift tiklanarak herhangi bir modern tarayicida 
> dogrudan calistirilabilir. Ancak kok dizin referanslarinin ve bazi 
> asenkron tarayici politikalarinin (CORS/Fetch yapilari) yerelde 
> hata vermemesi adina HTTP protokolu simulasyonu onerilir.

> 🔌 **Yerel HTTP Sunucusu (VS Code Live Server)**
> Gelistirme ortamında Visual Studio Code editoru ve yerlesik 
> Live Server Extension (Ritwick Dey) eklentisi kullanilmistir. 
> Bu mekanizma, index.html dosyasinin bulundugu dizini kok kabul 
> ederek yerel bir ağ soketi acar ([http://127.0.0.1:5500](http://127.0.0.1:5500)) ve koddaki 
> her dosya kaydetme isleminde (Ctrl+S) tarayiciya otomatik yenileme 
> (Hot-Reload) sinyali gonderir. Bu sayede canli sunucu davranisi 
> lokalde birebir simule edilir.

---

## 🔗 BOLUM 12: CI/CD Pipeline, Otomasyon ve Canli Yayin Mimari Baglantilari

Projenin internet ortamindaki dagitimi (deployment), endustriyel 
standartlarda kabul goren bulut tabanli bir surekli entegrasyon 
hatti ile kurgulanmıştır:

> ⚙️ **Otomatik Dagitim Hatti (CI/CD)**
> Projenin canli sunucu altyapisi için Netlify platformu tercih 
> edilmiştir. GitHub deposundaki main dali (branch) ile Netlify 
> arasinda guvenli bir Webhook entegrasyonu (OAuth 2.0) kurulmustur. 
> Gelistirici bilgisayarından uzak depoya atılan her git push komutu, 
> Netlify sunucularında bir derleme (build tetiklemesi) baslatir ve 
> projenin en guncel hali saniyeler icinde sifir kesintiyle 
> (Zero-Downtime Deployment) yayina alinir.

> 🚀 **Canli Onizleme Adresi (Netlify Pipeline)**
> 👉 [Roma Tarihi Portali Canli Önizleme](https://cheery-bubblegum-45d678.netlify.app/)

> 🌐 **Sunucu Yapilandirma Modeli**
> Projenin statik varliklari (assets) ve resim dosyaları (.jpg), 
> tarayıcı önbellekleme (browser caching) kurallarına ve CDN 
> (Content Delivery Network) dağıtım ağına uygun olarak Netlify 
> kenar sunucularında (edge nodes) optimize edilmiş şekilde saklanır.
