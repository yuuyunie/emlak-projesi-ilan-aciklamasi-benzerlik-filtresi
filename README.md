# Emlak İlanları Benzerlik Filteri

Bu proje, satılım emlak ilan açıklamalarını karşılaştırarak **yinelenen** ilanların tespit edilmesini amaçlamaktadır. TF-IDF ve Word2Vec yöntemleri ile ilan açıklamaları arasındaki **metinsel benzerlik** ölçülmektedir.

---

## Modelin nasıl oluşturulacağı
1.**Veri Hazırlığı** 

-Google üzerinden Web Scraper eklentisi yardımıyla emlakjet.com ve hepsiemlak.com'dan ilan açıklamaları toplanır.

-Açıklamalar CSV dosyasına kaydedilir.

2.**Ön İşleme**

-Noktalama işaretleri ve durak kelimeleri temizlenir.

-Lemmatizasyon ve stem işlemleri uygulanarak iki ayrı dosyada temizlenmiş veriler kaydedilir.

3.**Zipf yasası kontrolü(Tercihen)**

-Kelime frekansları analiz edilerek doğal dile uygunluk kontrol edilir.

4.**Vektörleştirme**

-TF-IDF yöntemiyle ilan açıklamaları sayısal vektörlere dönüştürülür.

-Alternatif olarak Word2Vec modeli eğitilerek benzerlik ilişkileri oluşturulur.

5.**Benzerlik Hesaplama**

-TF-IDF için "cosine similarity" ile açıklamalar arası benzerlik oranları hesaplanır.

-Word2Vec ile kelimeler arası anlamsal yakınlık ölçülür.

6.**Sonuçların Analizi**

-Belirli bir eşik değeri üzerinde benzer ilan çiftleri tespit edilerek raporlanır.

## Veri Setinin Kullanılabileceği Amaçlar

- Aynı evin birden fazla ilana düşüp düşmediğini kontrol etme

- Emlak sitelerinde veri temizliği ve filtreleme

- İlan metinleri arasında anlamsal benzerlik analizleri yapma

- Doğal dil işleme projelerinde Türkçe veri örneği olarak değerlendirme

> 📎 Veri setine [buradan ulaşabilirsiniz]()
> Not: Veri yalnızca eğitim ve araştırma amaçlıdır. Ticari kullanımlar için ilgili web sitelerinin kullanım koşulları dikkate alınmalıdır.


## Gerekli Kütüphaneler ve Kurulum
