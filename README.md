# ⭐️ Amazon Ürün Yorumlarını Sıralama Projesi

Bu projede, Amazon üzerinden satılan bir ürünün yorumları incelenmiş, analiz edilmiş ve en faydalı yorumlar istatistiksel yöntemlerle sıralanmıştır.

---

## 📌 Proje Amacı

- Ürün detay sayfasında gösterilecek **en güvenilir 20 yorumu** belirlemek.
- Yorumları:
  - Tarihe göre ağırlıklı puanlama
  - Kullanıcı davranışına göre ağırlıklı puanlama
  - Wilson Lower Bound gibi istatistiksel yöntemlerle sıralamak.

---

## 📂 Veri Seti

- **Kaynak:** [Amazon](https://www.amazon.com/)
- **İçerik:** Ürün puanları, yorumlar, oylama sayıları, tarih bilgileri
- `reviewText`, `overall`, `reviewTime`, `helpful` gibi sütunları içerir.

---

## 🔍 Uygulanan Analizler

### 1. Ortalama Ürün Puanı
- Tüm yorumların basit ortalaması alınmıştır.

### 2. Zaman Ağırlıklı Ortalama
- Yeni yorumlar daha yüksek ağırlıkla puanlamaya dahil edilmiştir.

### 3. Kullanıcı Ağırlıklı Ortalama
- Kurs/ürün ilerleme yüzdesine göre farklı ağırlıklarla puanlama yapılmıştır.

### 4. Wilson Lower Bound Skoru
- Yorumun **kaç kişi tarafından faydalı bulunduğu** ve **toplam oylama sayısı** dikkate alınarak istatistiksel olarak güvenilir bir sıralama yapılmıştır.

---

## 🥇 En Faydalı 20 Yorum

Yorumlar, **wilson_lower_bound** skoruna göre sıralanmış ve ürün sayfasında gösterilmek üzere en faydalı ilk 20 yorum belirlenmiştir.

---

## 🛠 Kullanılan Kütüphaneler

- `pandas`
- `scipy`
- `datetime`
- `sklearn.preprocessing` (MinMaxScaler)

---

## 📈 Elde Edilen Skorlar

Her yorum için aşağıdaki skorlar hesaplandı:

- `score_pos_neg_diff`: Yararlı – Yararsız
- `score_average_rating`: Oran bazlı faydalı oylama
- `wilson_lower_bound`: Güven aralığına göre en güvenilir skor

---

## 📌 Notlar

> Bu proje, veri bilimi ve makine öğrenmesi uygulamalarında veri önceliklendirme ve sıralama algoritmalarının anlaşılması amacıyla geliştirilmiştir.

---

## 👩‍💻 Hazırlayan

**İrem Gürdal**  
Data Scientist & MIS/Health Information Specialist  
📧 https://www.kaggle.com/iremgurdal
https://www.linkedin.com/in/irem-g%C3%BCrdal-/
https://medium.com/@iremgurdal97

---

## 📎 Lisans

MIT Lisansı  
