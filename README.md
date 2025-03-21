# Atık Yönetiminde Bulanık Mantık Tabanlı Karar Destek Sistemi

## 📌 Proje Açıklaması
Bu proje, **atık yönetimi süreçlerinde belirsizliği azaltmak ve daha etkili bir toplama süreci tasarlamak amacıyla** geliştirilmiş bir **bulanık mantık tabanlı karar destek sistemi** sunmaktadır. Sistemin temel amacı, **atık miktarı, depolama kapasitesi ve geri dönüşüm maliyeti** gibi kritik değişkenleri değerlendirerek **toplama sıklığını belirlemektir**.

Bu sistem, MATLAB ortamında geliştirilmiş olup, **Mamdani Tip-1 Bulanık Çıkarım Yöntemi** kullanılarak çalışmaktadır. Farklı **test senaryoları** uygulanarak sonuçlar görselleştirilmiştir.

---

## 🚀 Kullanılan Teknolojiler

- **MATLAB** – Bulanık mantık modelleme ve simülasyon için kullanıldı.
- **Fuzzy Logic Toolbox** – Bulanık mantık çıkarımı ve kuralların oluşturulması için kullanıldı.
- **MATLAB Visualization** – Çıktıların analiz edilmesi ve görselleştirilmesi.

---

## 🎯 Proje İçeriği

### 1️⃣ Neden Bulanık Mantık Kullanıldı?
Atık yönetimi sürecinde **geleneksel karar mekanizmaları**, atık miktarındaki belirsizlikleri yönetmekte yetersiz kalmaktadır. **Bulanık mantık**, insan düşünme sistemine benzeyen çıkarımlar yaparak **esnek ve daha doğru tahminler** sunar. 

Projede ele alınan **temel sorunlar** şunlardır:

- **Atık Miktarı Belirsizliği** 🗑️: Mevsimsel değişiklikler ve bireysel davranışlar nedeniyle atık miktarı değişkenlik gösterir.
- **Depolama Kapasitesi Kısıtları** 📦: Sınırlı alanlar nedeniyle hatalı kararlar çevresel risklere neden olabilir.
- **Geri Dönüşüm Maliyeti** ♻️: Enerji ve iş gücü maliyetleri optimize edilmelidir.

---

### 2️⃣ Sistemin Çalışma Prensibi

1. **Bulanıklaştırma (Fuzzification)** 🔍
   - Atık miktarı, depolama kapasitesi ve geri dönüşüm maliyeti gibi **giriş değişkenleri** bulanık küme fonksiyonlarına dönüştürüldü.
   - **Trapezoidal, Gaussian ve Üçgen Üye Fonksiyonları** kullanıldı.

2. **Kuralların Oluşturulması** 📜
   - **35 farklı kural** tanımlandı.
   - Kurallar, **"Eğer... ise"** şeklinde modellenerek, **toplama sıklığını** belirlemek için kullanıldı.

3. **Çıkarım Yöntemi (Inference Method)** 🔄
   - **Mamdani Tip-1 Bulanık Çıkarım Sistemi** kullanıldı.
   - **Max-Min** yöntemi tercih edilerek, sistemin **daha stabil ve hızlı** çalışması sağlandı.

4. **Durulaştırma (Defuzzification)** 🎯
   - Çıkarım sonucunda oluşan bulanık değerler **kesin sayısal** verilere dönüştürüldü.
   - **Ağırlık Merkezi (Centroid) yöntemi** kullanıldı.

---

### 3️⃣ Kullanılan Değişkenler ve Çıktılar

📌 **Giriş Değişkenleri:**
- **Atık Miktarı** (Düşük, Orta, Yüksek)
- **Depolama Kapasitesi** (Düşük, Orta, Yüksek)
- **Geri Dönüşüm Maliyeti** (Düşük, Orta, Yüksek)

📌 **Çıkış Değişkeni:**
- **Toplama Sıklığı** (Az, Orta, Sık)

---

## 🔬 Deneysel Çalışma ve Test Senaryoları

**📌 Senaryo 1 – En Yüksek Stres Senaryosu**
| Değişken | Değer |
|----------|--------|
| Atık Miktarı | Yüksek |
| Depolama Kapasitesi | Düşük |
| Geri Dönüşüm Maliyeti | Yüksek |
| **Beklenen Çıktı** | **Sık** |

![image](https://github.com/user-attachments/assets/8215bbde-1661-4923-89bf-7300e40db4c9)


**📌 Senaryo 2 – Düşük Yoğunluk Senaryosu**
| Değişken | Değer |
|----------|--------|
| Atık Miktarı | Düşük |
| Depolama Kapasitesi | Yüksek |
| Geri Dönüşüm Maliyeti | Düşük |
| **Beklenen Çıktı** | **Az** |

![image](https://github.com/user-attachments/assets/a2e82cae-9905-4ef7-a8ee-8876a417180f)


⚡ **Sonuç:** Farklı senaryolar üzerinden yapılan testlerde, **bulanık mantık tabanlı sistemin kararları gerçekçi ve optimize edilmiş çıktı vermektedir**.

---

## 📊 MATLAB Sonuçları ve Görselleştirmeler
Proje kapsamında elde edilen sonuçlar MATLAB kullanılarak görselleştirilmiştir.

📌 **Örnek Çıktılar:**
- **Atık Miktarı – Depolama Kapasitesi Grafiği**
- ![image](https://github.com/user-attachments/assets/eef87be2-c98b-4811-91eb-121101217e57)

- **Atık Miktarı – Geri Dönüşüm Maliyeti Grafiği**
- ![image](https://github.com/user-attachments/assets/f72a3b45-87cd-4143-bb6c-3942b638091b)

- **Depolama Kapasitesi – Geri Dönüşüm Maliyeti Grafiği**
- ![image](https://github.com/user-attachments/assets/ad3cd577-f7f0-42f7-8373-2034da017d6f)


Bu grafikler, sistemin verdiği kararların doğruluğunu ve **bulanık mantık tabanlı karar mekanizmasının etkinliğini göstermektedir**.

---

## 🔗 Gelecekteki Geliştirmeler

✅ **Gerçek Zamanlı Veri Kullanımı** 🚀
- **Sensör verileri** ile entegre edilerek **gerçek zamanlı atık takibi** sağlanabilir.

✅ **Makine Öğrenmesi Entegrasyonu** 📈
- **Makine öğrenmesi algoritmaları** ile geçmiş verilere dayalı olarak **daha akıllı kural önerileri** oluşturulabilir.

✅ **Ekstra Girdi Değişkenleri** 📊
- **Mevsimsel etkiler, araç kapasiteleri, rota planlama faktörleri** gibi değişkenler eklenerek **daha dinamik bir sistem** oluşturulabilir.

---

## 📜 Kaynakça
1. Zadeh, L. A. (1965). *Fuzzy sets*. Information and Control.
2. MATLAB Documentation - Fuzzy Logic Toolbox.
3. Atık yönetimi ve geri dönüşüm ile ilgili ulusal raporlar ve çalışmalar.

---


