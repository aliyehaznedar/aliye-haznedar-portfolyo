# CAFECO A.Ş. Çok Dönemli Üretim, Blending ve Taşıma Optimizasyonu (MILP)

Bu proje, Dokuz Eylül Üniversitesi Endüstri Mühendisliği Bölümü **END3519 Yöneylem Araştırması 1** dersi kapsamında geliştirdiğim çalışmamdır. Projede, çok dönemli ve çok kademeli bir tedarik zinciri ağında; hammadde satın alma, kalite (blending) kısıtları altında karışım formülasyonu, depo yeri seçimi ve dağıtım kararlarını bütünsel olarak ele aldım.

## 📌 Problemin Tanımı ve Matematiksel Altyapı
Model, Karışık Tamsayılı Doğrusal Programlama (MILP) yapısında kurgulanmış olup toplam 230 kısıt ve 259 karar değişkeninden oluşmaktadır. Altın (GOLD) ve Klasik (CLASSIC) ürünlerin hedef asidite, gövde ve aroma standartlarını doğrusal karışım denklemleri ile sağlarken normal, fazla mesai ve fason üretim modları arasında maliyet optimizasyonu yaptım.

## 📊 Optimal Çözüm ve Temel Bulgular
Modeli hem LINGO hem de Python (GUROBI) solver sistemleri ile test ederek doğrulanmış global optimal sonuca ulaştım:
* **Optimal Toplam Maliyet:** 533,840.14 TL
* **Lojistik Ağ Tasarımı:** Ankara ve Konya depoları kapatılarak, ilk yatırım ve işletme maliyetini en küçükleyen stratejik Bursa Deposu (Depo2) merkezi dağıtım üssü olarak seçilmiştir.
* **Üretim Dağılımı:** Düşük birim maliyet avantajı nedeniyle İzmir Fabrikası ana üretim üssü yapılmış, İzmir Normal ve Fazla Mesai kapasiteleri %100 kullanım oranına (darboğaza) ulaştığı için Gaziantep normal vardiyası destekleyici güç olarak devreye alınmıştır.

## 📈 Duyarlılık ve Gölge Fiyat Analizleri
* **En Kritik Darboğaz:** İzmir normal vardiya kapasitesi mutlak en yüksek marjinal değere sahiptir (Shadow Price = 6 TL/kg). Bu kaynağın 1 kg artırılması toplam maliyeti marjinal olarak 6 TL iyileştirmektedir.
* **Maliyet Baskısı:** M3 (Gaziantep) müşterisinin GOLD ürün talebi, 49.14 TL/kg marjinal maliyetle sistemdeki en pahalı pazar segmenti olarak saptanmıştır.

## 📁 Klasör İçeriği
* `/CAFECO_Data.xlsx`: Üretim modları, taşıma maliyetleri, hammadde kaliteleri ve müşteri taleplerini içeren girdi dosyası.
* `/yöneylem1 proje.pdf`: LINGO kod yapısını, matematiksel notasyonu, duyarlılık çıktı raporlarını ve stratejik yönetimsel önerileri içeren detaylı proje raporum.
* `/GUROBI_sonuc.pdf`: GUROBI solver çıktısı ve detaylı sonuç raporu.

**Geliştiren:** Aliye Haznedar  
**Akademik Danışman:** Prof. Dr. Şeyda Ayşe Yıldız
