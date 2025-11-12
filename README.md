
# 🧠 Gözetimli Öğrenme Kapanış Projesi

Bu proje, **Makine Öğrenmesi - Gözetimli Öğrenme** konularında hem *sınıflandırma* hem de *regresyon* uygulamalarını kapsar.
İki farklı veri seti kullanılarak modellerin performansları karşılaştırılmıştır.

---

## 📁 Kullanılan Veri Setleri

### 1️⃣ `telecom_churn.csv`

Müşteri kaybı (churn) tahminine yönelik sınıflandırma veri setidir.

* **Amaç:** Bir müşterinin hizmetten ayrılıp ayrılmayacağını tahmin etmek.
* **Hedef değişken:** `Churn` (Yes → 1, No → 0)
* **Kullanılan modeller:**

  * RandomForestClassifier
  * XGBoostClassifier

**Değerlendirme metrikleri:**

* Accuracy (Doğruluk)
* Precision, Recall, F1-score
* Confusion Matrix

---

### 2️⃣ `winequality-white.csv`

Şarap kalitesinin tahmin edilmesine yönelik regresyon veri setidir.

* **Amaç:** Fiziksel ve kimyasal özelliklerden şarap kalitesini tahmin etmek.
* **Hedef değişken:** `quality` (0–10 arası kalite puanı)
* **Kullanılan modeller:**

  * Linear Regression
  * XGBoost Regressor

**Değerlendirme metrikleri:**

* R² (Determination Coefficient)
* RMSE (Root Mean Squared Error)

---

## ⚙️ Kullanılan Teknolojiler

* Python 3.11
* Pandas, NumPy
* Scikit-learn
* XGBoost
* Matplotlib, Seaborn

---

## 🧩 Adımlar

1. **Veri Ön İşleme**

   * Eksik verilerin doldurulması
   * Kategorik değişkenlerin dönüştürülmesi (`get_dummies`)
   * Hedef değişkenlerin 0/1 biçimine çevrilmesi

2. **Eğitim / Test Ayrımı**

   ```python
   X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
   ```

3. **Modelleme**

   * Sınıflandırmada: Random Forest & XGBoost
   * Regresyonda: Linear & XGBRegressor

4. **Değerlendirme**

   * Classification: Accuracy ve F1-score
   * Regression: R² ve RMSE

---

## 📊 Örnek Çıktılar

```text
Random Forest Doğruluk: 0.93
XGBoost Doğruluk: 0.95

Linear Regression R2: 0.27
XGBoost Regressor R2: 0.51
```

---

## 🚀 Sonuç

* XGBoost modelleri her iki görevde de daha yüksek başarı sağlamıştır.
* Veri ön işleme adımları model performansını belirgin biçimde artırmıştır.
* Bu proje, gözetimli öğrenme tekniklerinin gerçek veri setlerinde uygulanmasını göstermektedir.

---

## 🧾 Lisans

Bu çalışma eğitim amaçlıdır.
Kullanılan veri setleri [Kaggle](https://www.kaggle.com/datasets/kashnitsky/mlcourse) üzerinden sağlanmıştır.

---

İstersen buna küçük bir **“Görseller”** bölümü ekleyip confusion matrix ve feature importance grafiği örneği de koyabiliriz.
Ekleyeyim mi {Quicksilver}? 📊
