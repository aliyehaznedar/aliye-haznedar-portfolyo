# 🚀 Çok Amaçlı Yapay Arı Kolonisi (MOABC) ile Üretim Çizelgeleme ve Enerji Maliyeti Optimizasyonu

Bu proje, Dokuz Eylül Üniversitesi Endüstri Mühendisliği Bölümü **END3614 Üretim Planlama ve Kontrol** dersi kapsamında geliştirilmiştir. Çalışmada, akıllı şebeke ve sürdürülebilir üretim kısıtları altında endüstriyel tesislerin maliyet yükünü azaltmaya yönelik meta-sezgisel bir karar destek sistemi tasarlanmıştır.

## 📌 Problemin Tanımı (DHRHFSP-SDST)
Projede, coğrafi olarak dağıtılmış ve birbirinden farklı (heterojen) makine parkurlarına sahip fabrikalarda; yeniden girişli (re-entrant) iş akışları, sıraya bağlı hazırlık süreleri (SDST) ve fabrika uygunluk kısıtları altında en uygun çizelgeleme aranmıştır. Optimizasyon, Zaman Kullanım (TOU) elektrik fiyatlandırması (On-Peak, Mid-Peak, Off-Peak) senaryoları altında yapılmıştır.

### 🎯 Optimizasyon Hedefleri:
1. **Maksimum Tamamlanma Süresi ($C_{max}$):** Toplam üretim süresini (termin süresi) minimize ederek operasyonel hızı korumak.
2. **Toplam Enerji Maliyeti (TC):** Makinelerin işleme (active), boşta bekleme (idle) ve hazırlık (setup) durumlarında harcadığı elektrik faturasını en küçüklemek.

## 🛠️ Çözüm Yaklaşımı ve Algoritma
* **Temel Model (MOABC1):** Standart çok amaçlı yapay arı kolonisi mimarisi kurulmuş, işler mümkün olan en erken sürelerde atanmıştır.
* **Geliştirilmiş Model (MOABC):** Üretim termin süresini hiçbir şekilde geciktirmeden, kritik yolu etkilemeyen operasyonları akıllıca elektriğin ucuz olduğu "Off-Peak" saatlerine kaydıran **Sağa Kaydırma Stratejisi (ESRS)** entegre edilmiştir.

## 📊 Elde Edilen Ölçülebilir Sonuçlar
Yapılan simülasyon ve deneysel analizler sonucunda:
* Her iki algoritma da üretimi tam **134.00 saatte** tamamlayarak termin sürelerine sadık kalmıştır.
* Geliştirilen ESRS operatörünün devreye girmesiyle, operasyonların akıllıca yönetilmesi sağlanmış ve **Toplam Enerji Maliyetinde %6.67 (188.98 CNY) net tasarruf** elde edilmiştir.

## 📁 Depo İçeriği
* `/MOABC_DHRHFSP_SDST_FAST_FIXED.m`: Geliştirilmiş, ESRS tasarruf operatörlü ana MATLAB kod bloğu.
* `/DHRHFSP_SDST_dataset_2.xlsx`: Fabrika, makine, işleme süreleri ve TOU elektrik tarifesi parametrelerini içeren girdi veri seti.
* `/UPK_SONRAPOR_2.pdf`: Projenin tüm matematiksel formülasyonunu, Gantt şemalarını ve endüstriyel analizlerini içeren detaylı akademik rapor[cite: 6, 10].
* `/Proje_Sunumu.pdf`: Proje sunum slaytları[cite: 11].

## 👥 Proje Sahibi
Aliye Haznedar
*Danışman:* Prof. Dr. Gökalp Yıldız
