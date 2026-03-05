🚕 NYC Taxi Demand Forecasting & Time-Series Analysis
Bu proje, 2015 ve 2016 yıllarına ait milyonlarca satırlık NYC Yellow Taxi verisini kullanarak taksi talebini tahmin etmek amacıyla geliştirilmiştir. Veri işleme aşamasında yüksek performanslı DuckDB kullanılırken; tahminleme aşamasında modern makine öğrenmesi algoritmaları Optuna ile optimize edilmiştir.

🔗 Veri Kaynağı
Projede kullanılan ham verilere NYC Taxi & Limousine Commission (TLC) Trip Record Data adresinden ulaşılabilir.

📊 Veri Seti ve İşleme
Kapsam: 2015 ve 2016 yıllarına ait tam veri setleri üzerinde çalışılmıştır.

Veri Mühendisliği: Milyonlarca satırlık verinin (Yellow Taxi) hızlı sorgulanması, temizlenmesi ve aggregate edilmesi için DuckDB kullanılmıştır.

Zaman Serisi Dönüşümü: Ham veriler; saatlik ve günlük periyotlara dönüştürülerek trend, mevsimsellik ve tatil günleri gibi dışsal faktörlerle zenginleştirilmiştir.

🤖 Kullanılan Modeller ve Optimizasyon
Proje kapsamında farklı model mimarilerinin performansları karşılaştırılmıştır:

Gradient Boosting: XGBoost ve LightGBM (Yüksek boyutlu verilerde hızlı ve isabetli sonuçlar).

İstatistiksel Modeller: Facebook Prophet (Mevsimsellik ve trend analizi için).

Lineer Modeller: Ridge Regression (Baseline performans ölçümü için).

Hiperparametre Tuning: Tüm modeller Optuna (Bayesian Optimization) kullanılarak en düşük hata payı (MAE/RMSE) için otomatik olarak optimize edilmiştir.

📈 Öne Çıkan Bulgular
Yıllık Karşılaştırma: 2015 ve 2016 yılları arasındaki talep değişimleri analiz edilmiştir. (Örn: 2015 ortalaması ~16,668 iken 2016'da ~14,926 seviyelerine düşüş gözlemlenmiştir).

Hata Dağılımı: Optuna ile optimize edilen modellerin (XGBoost, LightGBM, Prophet, Ridge) hata dağılımları histogramlar aracılığıyla görselleştirilerek model kararlılığı doğrulanmıştır.

🛠 Kurulum ve Kullanım
Repoyu klonlayın.

pip install -r requirements.txt ile gerekli kütüphaneleri kurun.

main.ipynb dosyasını çalıştırarak analiz ve modelleme adımlarını izleyin.
