#  Fast Food Zinciri Günlük İşleyişi Veri Modellemesi ve Sistem Analizi

Bu proje, Dokuz Eylül Üniversitesi Endüstri Mühendisliği Bölümü **END2416 Bilgi Sistemleri Analizi ve Tasarımı** dersi kapsamında hazırladığımız grup dönemi çalışmamızdır. Projede, gerçek zamanlı bir fast food zincirinin operasyonel süreçlerini dijitalleştirmek amacıyla kapsamlı bir veritabanı mimarisi modelledik ve analiz ettik.

## 📌 Proje Kapsamı ve Vaka Açıklaması
İşletme içerisindeki veri akışını düzenli ve kontrol edilebilir hale getirmek için müşterilerin sipariş oluşturma süreçleri, ürün kategorizasyonları, çalışanların operasyonel iş yükleri ve ödeme mekanizmaları veritabanı kısıtlarına uygun şekilde kurgulanmıştır.

### 💡 Tasarlanan Veritabanı Mimarisi ve Normalizasyon:
* **Çoka Çok (M:N) İlişki Çözümü:** Siparişler ve ürünler arasındaki karmaşık ilişkiyi çözmek, ürün adedi ve ara toplam bilgilerini tutabilmek için `Sipariş_Detayı` isimli bir associative entity (ara tablo) kurguladık.
* **Operasyonel Süreç Takibi:** Sipariş hazırlama süreçlerini Foreign Key (FK) yapıları ile çalışanlara bağlayarak performans ve süreç takibini mükemmel hale getirdik.
* **Bütünsel Modelleme:** Veritabanı iskeletinin tam olarak anlaşılabilmesi adına hiyerarşik olarak 3 farklı katmanda ER diyagramı tasarladık: Context ER Diyagramı, Key-Based ER Diyagramı ve Fully Attributed ER Diyagramı.

## 🧠 AI Destekli Veri Modelleme ve Genişletme Çalışması
Projenin ikinci aşamasında, temel modele ek olarak yapay zeka entegrasyonu ile sistemi genişlettik. Fast food sektörünün en kritik operasyonlarından olan **Stok ve Üretim (Reçete) Yönetimi** modülünü sisteme dahil ettik. Ürünler ile hammaddeler arasındaki ilişkiyi çözen `Reçete` tablosunu ve şubeler arası takibi sağlayan `Şube` entitilerini de kurgulayarak normalizasyon kurallarına tam uyumlu, bütünsel bir zincir yönetim altyapısı elde ettik.

## 📁 Klasör İçeriği
* `/BSAT.pdf`: Projenin tüm vaka açıklamalarını, 3 farklı seviyedeki özgün ER diyagramlarını ve AI modelleme yorumlamalarını içeren detaylı akademik raporumuz.

**Proje Ekibi:** Aliye Haznedar, Ata Seymen, Efe Yılmaz, Pınar Hacıoğlu  
**Akademik Danışman:** Prof. Dr. Ali Serdar TAŞAN
