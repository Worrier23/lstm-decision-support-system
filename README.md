
# LSTM Tabanlı Karar Destek Sistemi

Bu proje, zaman serisi verileri kullanarak geleceğe yönelik tahminler üretmek amacıyla geliştirilmiş bir derin öğrenme uygulamasıdır.
📈 LSTM-Based Stock Price Prediction: THY (THYAO.IS)Bu proje, Sakarya Üniversitesi Bilişim Sistemleri Mühendisliği Yüksek Lisans Programı Derin Öğrenme dersi final ödevi kapsamında geliştirilmiştir. Bir Database Specialist bakış açısıyla, ham borsa verilerinin temizlenmesi, zenginleştirilmesi ve LSTM mimarisi ile modellenmesi sürecini içerir.

🚀 Proje Özeti ve Amaç Çalışmanın temel amacı, borsa verilerindeki doğrusal olmayan ve karmaşık hareketleri derin öğrenme yöntemleriyle modelleyerek bir Karar Destek Sistemi oluşturmaktır. THY (THYAO.IS) hisse senedinin 5 yıllık verileri üzerinde trend analizi ve gelecek fiyat tahmini yapılmıştır.

🛠️ Teknik Yığın ve ÖzelliklerDil: Python Kütüphaneler: TensorFlow/Keras, Pandas, NumPy, Scikit-Learn, Matplotlib, YFinance Model: İki katmanlı Stacked LSTM (100 & 50 Nöron) Regülarizasyon: %20 Dropout ve Batch Normalization ile aşırı öğrenme (overfitting) kontrolü Optimizasyon: Adam Optimizer ve Huber Loss fonksiyonu 

⚙️ Teknik Zorluklar ve Mühendislik ÇözümleriProje geliştirme sürecinde karşılaşılan kritik hatalar ve uygulanan çözümler:Veri Temizliği (Infinity/NaN): İndikatör hesaplamalarındaki sıfıra bölünme hataları, "Database Cleaning" teknikleri ve dropna() yöntemleriyle giderilmiştir.Huber Loss Entegrasyonu: Keras'ta karşılaşılan tanımlayıcı hatası, tensorflow.keras.losses.Huber sınıfının doğrudan import edilmesiyle çözülmüştür.Inverse Transform Hatası: Tahmin edilen 0-1 aralığındaki değerlerin TL bazına dönüştürülmesi aşamasındaki boyut uyumsuzluğu, np.repeat fonksiyonuyla doğru yapıya kavuşturulmuştur.

📊 Performans ve ÇıktılarModelin başarımı, hiç görülmemiş "Test Seti" verileri üzerinde ölçülmüştür:MAE (Mean Absolute Error): 24.73 TL Hata Oranı: ~300 TL seviyesindeki hisse için yaklaşık %8 sapma Tahmin Analizi Grafiği https://github.com/Worrier23/lstm-decision-support-system/issues/1#issue-4273820982
[Görsel Sonuçlar: Siyah çizgi gerçek fiyatları, kırmızı çizgi modelin tahminlerini temsil eder. Modelin trend dönüşlerini yakalamadaki başarısı net bir şekilde görülmektedir.]
📂 Dosya Yapısı/notebooks: Projenin tüm kodlarını içeren Jupyter Notebook dosyası /presentation: Sakarya Üniversitesi için hazırlanan 15 slaytlık PDF sunumu requirements.txt: Gerekli kütüphane listesi 

🔮 Gelecek VizyonuNLP Entegrasyonu: Haber başlıklarının duygu analizi (Sentiment Analysis) skorlarının modele yeni bir özellik (feature) olarak eklenmesi planlanmaktadır.
⚠️ Yasal Not Bu proje tamamen akademik bir çalışma olup, kesinlikle yatırım tavsiyesi niteliği taşımamaktadır.
Hazırlayan: Mücahit Kahveci 


