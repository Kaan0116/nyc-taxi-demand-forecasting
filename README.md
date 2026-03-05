🚕 NYC Taxi Demand Forecasting & Time-Series Analysis
Bu proje, 2015 ve 2016 yıllarına ait milyonlarca satırlık NYC Yellow Taxi verisini kullanarak taksi talebini tahmin etmek amacıyla geliştirilmiştir. Veri işleme aşamasında yüksek performanslı DuckDB kullanılırken, tahminleme aşamasında modern makine öğrenmesi algoritmaları Optuna ile optimize edilmiştir.

📊 Veri Seti ve İşleme
Kapsam: 2015 ve 2016 yıllarına ait tam veri setleri üzerinde çalışılmıştır.

Veri Mühendisliği: Milyonlarca satırlık verinin hızlı sorgulanması ve aggregate edilmesi için DuckDB kullanılmıştır.

Zaman Serisi Dönüşümü: Ham veriler; saatlik ve günlük periyotlara dönüştürülerek trend, mevsimsellik ve tatil günleri gibi dışsal faktörlerle zenginleştirilmiştir.

🤖 Kullanılan Modeller ve Optimizasyon
Proje kapsamında farklı model mimarilerinin performansları karşılaştırılmıştır:

Gradient Boosting: XGBoost ve LightGBM (Yüksek boyutlu verilerde hızlı ve isabetli sonuçlar).

İstatistiksel Modeller: Facebook Prophet (Mevsimsellik ve trend analizi için).

Lineer Modeller: Ridge Regression (Baseline performans ölçümü için).

Hiperparametre Tuning: Tüm modeller Optuna (Bayesian Optimization) kullanılarak en düşük hata payı (MAE/RMSE) için otomatik olarak optimize edilmiştir.

📈 Öne Çıkan Bulgular
Yıllık Karşılaştırma: 2015 ve 2016 yılları arasındaki talep değişimleri analiz edilmiş, 2016 yılındaki ortalama talep farkları istatistiksel olarak raporlanmıştır.

Hata Dağılımı: Optuna ile optimize edilen modellerin hata dağılımları görselleştirilerek model kararlılığı doğrulanmıştır.

🛠 Teknolojiler
Dil: Python

Veritabanı: DuckDB

ML Frameworks: Scikit-learn, XGBoost, LightGBM, Prophet

Optimization: Optuna

Görselleştirme: Matplotlib, Seaborn
