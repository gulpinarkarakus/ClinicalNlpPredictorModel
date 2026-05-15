Clinical NLP Predictor Model

Bu proje, BERT tabanlı doğal dil işleme modeli kullanarak medikal metinlerden hastalık tahmini yapmayı amaçlamaktadır. Model, House MD dizisinden türetilmiş semptom/hastalık verisi ile eğitilmiştir.

📌 Proje Amacı

Girilen bir metin (semptom açıklaması) üzerinden, hastalığın hangi organa veya sistemle ilişkili olabileceğini tahmin eden bir makine öğrenmesi sistemi geliştirmek.

📊 Kullanılan Veri Seti
House MD dizisindeki vaka senaryolarından türetilmiştir
Farklı hastalık ve semptom örnekleri içerir
Veri seti manuel olarak oluşturulmuş ve temizlenmiştir
🧹 Veri Ön İşleme

Model performansını artırmak için kapsamlı veri temizleme işlemleri uygulanmıştır:

🔁 Tekrar eden veriler silindi
✂️ Çok kısa ve anlamsız cümleler çıkarıldı
🔤 Noktalama işaretleri düzeltildi
🧼 Gürültü azaltma (noise reduction) yapıldı
📊 Veri dengesi iyileştirildi
🔄 Veri Artırma (Data Augmentation)

Modelin genelleme yeteneğini artırmak için veri artırma teknikleri uygulanmıştır:

✏️ Basit Augmentation Teknikleri
Cümle içinde kelimeler rastgele yer değiştirilerek yeni örnekler üretildi
Aynı veri farklı varyasyonlarla çoğaltıldı
🤖 BERT Masked Language Modeling
Cümlelerde rastgele kelimeler maskelendi
BERT modeli ile bu boşluklar tahmin edilerek yeni cümleler üretildi
Böylece daha zengin ve çeşitli veri seti oluşturuldu
📈 Özellik Çıkarımı

Model girişleri için farklı temsil yöntemleri kullanıldı:

🧾 TF-IDF (Term Frequency - Inverse Document Frequency)
🤖 BERT embedding tabanlı temsil
🧠 Model
Model: BERT (Transformer tabanlı NLP modeli)
Görev: Çok sınıflı sınıflandırma (multi-class classification)
Çıktı: Girilen semptomun hangi organa/hastalığa ait olabileceği
🎯 Sonuçlar
📊 Accuracy: %86
Model, temizlenmiş ve artırılmış veri sayesinde daha stabil sonuçlar vermektedir
TF-IDF ve BERT birlikte kullanılarak performans artırılmıştır
🧪 Kullanım

Model, kullanıcıdan alınan metin girdisine göre:

"Hangi organ veya hastalık ile ilişkili olabilir?"

sorusuna tahmin üretir.
