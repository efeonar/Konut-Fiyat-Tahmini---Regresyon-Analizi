# 🏠 Ev Fiyatı Tahmini: Makine Öğrenmesi ile Regresyon Analizi

Bu proje, gayrimenkul verileri (metrekare, oda sayısı, kat sayısı, yapım yılı ve lokasyon) kullanılarak ev fiyatlarının makine öğrenmesi regresyon modelleriyle tahmin edilmesini ve sentetik veri setlerindeki korelasyon eksikliğinin model performansına etkisini incelemektedir[cite: 9, 10, 13].

---

## 🎯 Problem Tanımı ve Amaç
Gayrimenkul sektöründe evlerin temel fiziksel ve lokasyon özelliklerine dayanarak nihai satış fiyatlarının insan müdahalesi olmadan öngörülüp öngörülemeyeceğini test etmek, uçtan uca bir regresyon iş akışı (EDA, ön işleme, modelleme ve hata analizi) uygulamaktır[cite: 9, 10].

## 📊 Veri Seti ve Ön İşleme
* **Veri Seti:** [Kaggle – House Price Prediction Dataset](https://www.kaggle.com/datasets/zafarali27/house-price-prediction-dataset) (2.000 satır)[cite: 9, 10]
* **Bağımsız Değişkenler:** `Area`, `Bedrooms`, `Bathrooms`, `Floors`, `YearBuilt`, `Location`[cite: 9, 10]
* **Hedef Değişken:** `Price`[cite: 9, 10]
* **Ön İşleme Adımları:**
  * Matematiksel etkisi olmayan `Id` sütunu veri setinden çıkarılmıştır[cite: 9, 11].
  * Kategorik değişkenler **One-Hot Encoding** ile sayısallaştırılmıştır[cite: 9, 11].
  * Veri seti **%80 Eğitim (Train)** ve **%20 Test** olarak bölünmüştür[cite: 9, 11].

## 🤖 Kullanılan Modeller ve Performans Sonuçları
Sürekli bir hedef değişken tahmin edildiği için **Scikit-Learn** kütüphanesi ile doğrusal ve doğrusal olmayan iki farklı regresyon modeli karşılaştırılmıştır[cite: 9, 11]:

| Model | MAE | RMSE | $R^2$ Skoru |
| :--- | :---: | :---: | :---: |
| **Linear Regression** | 243,241.98 | 279,859.73 | -0.01 |
| **Random Forest Regressor** | 252,518.03 | 292,059.89 | -0.10 |

*(Kaynak: Proje değerlendirme sonuçları[cite: 9, 12])*

## 🔍 Keşifçi Veri Analizi (EDA) ve Hata Analizi
Yapılan görselleştirme ve değerlendirme sonucunda şu teknik bulgulara ulaşılmıştır:
* **Korelasyon Eksikliği:** Metrekare veya oda sayısı arttıkça fiyatın artması gibi temel piyasa dinamikleri bu veri setinde gözlemlenmemiştir[cite: 9, 10].
* **Underfitting Teşhisi:** Modellerde ezberleme (overfitting) yerine, verinin sentetik yapısı ve özellikler ile fiyat arasında gerçekçi bir ilişki bulunmaması nedeniyle öğrenememe (**underfitting**) durumu yaşanmıştır[cite: 9, 13].
* **Çıkarım:** Veri bilimi süreçlerinde algoritmadan önce **veri kalitesi ve özellik korelasyonunun** kritik öneme sahip olduğu görsel ve istatistiksel olarak ortaya konmuştur[cite: 9, 12, 13].

## 🔗 Proje Bağlantıları ve Dosyalar
* **Google Colab Notebook:** [Kodları Colab Üzerinde Görüntüle](https://colab.research.google.com/drive/1oEt3fGnXf3ay7tYrGjeacCcezPD7S199?usp=sharing)[cite: 9, 13]
* `Makine_ve_Derin_Ogrenme_Uygulamalari_Egitimi_EfeOnar.pdf`: Grafiklerin ve detaylı hata analizinin yer aldığı proje raporu[cite: 10, 11, 12, 13].

## 👤 Geliştirici
**Efe Onar**  
[Portfolyo](https://efeonar.com) | [GitHub](https://github.com/efeonar)
