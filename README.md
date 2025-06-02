🌦️ Yağış Tahmini (Rain Prediction) Projesi

Bu proje, Avustralya Meteoroloji Ofisi tarafından sağlanan hava durumu veri seti kullanılarak, ertesi gün yağmur yağıp yağmayacağını tahmin etmek için gerçekleştirilmiştir.
Proje kapsamında, farklı makine öğrenmesi modelleri kullanılarak sınıflandırma problemleri çözülmüş ve modellerin başarıları karşılaştırılmıştır.

🧭 Projenin Amacı

RainTomorrow değişkenini (yarın yağmur yağıp yağmayacağını) tahmin eden bir model geliştirmek.

Farklı algoritmaların (Logistic Regression, Random Forest, Decision Tree) performanslarını karşılaştırmak.

En iyi tahmin yeteneğine sahip modeli belirlemek.

📊 Kullanılan Veri Seti

Kaynak: Kaggle - Weather Dataset

Boyut: ~56.000 satır, 23 sütun

Veri Özellikleri: Sıcaklık, rüzgar yönü, nem, basınç, bulut durumu, yağış miktarı gibi hava durumu bilgileri

Hedef Değişken: RainTomorrow (Yes/No)

🔍 Kullanılan Yöntemler
Veri Ön İşleme:

Eksik verilerin medyan ve mod ile doldurulması

Kategorik değişkenlerin sayısal formatlara dönüştürülmesi (Label Encoding)

Gerekli sütunların çıkarılması

Modelleme:

Logistic Regression (class_weight='balanced' ile dengesizlik problemi çözümü)

Random Forest

Decision Tree

Model Değerlendirme Metrikleri:

Precision

Recall

F1-Score

Accuracy

ROC-AUC Skoru

Görselleştirmeler:

ROC Eğrisi Grafiği

Confusion Matrix (Karışıklık Matrisi) Grafiği

Model Karşılaştırma Bar Grafiği

🚀 Sonuçlar
Random Forest, en yüksek başarıyı göstermiştir (AUC: 0.88, Accuracy: 0.86).

Logistic Regression, dengeli bir performans sunmuştur (AUC: 0.85, Accuracy: 0.78).

Decision Tree, en düşük performansa sahip model olmuştur (AUC: 0.69, Accuracy: 0.78).

Yağmur var sınıfı için Recall değerleri Logistic Regression ve Random Forest modellerinde tatmin edicidir.

Veri setinde sınıf dengesizliği olduğu için, class_weight='balanced' ve stratify=y gibi yöntemler kullanılmıştır.
