# Time-Series

- **Time series:** Zamana bağlı olarak gözlemlenen verilerin bir dizisidir.
- **Trend:** Bir zaman serisinde uzun vadeli artış veya azalış eğilimini temsil eder.
- **Stationary (Durağanlık):** Zaman serilerinde istatistiksel özelliklerin zamanla değişmemesi durumudur. Ortalama, varyans ve kovaryans gibi özellikler sabit kalır.
- **Seasonality (Mevsimsellik):** Belirli bir zaman diliminde düzenli olarak tekrar eden desenler veya dalgalanmalar anlamına gelir.
- **Cycle:** Uzun vadeli ve genellikle düzensiz bir biçimde gerçekleşen düzenli desenlerdir.
***
  ## Single Exponential Smoothing (Tekli Üstel Düzeltme)
   **Single Exponential Smoothing (Tekli Üstel Düzeltme):** Bir zaman serisinin düzeltilmiş tahminlerini oluşturmak için kullanılan bir zaman serisi tahminleme tekniğidir. Geçmiş verilere ağırlık verilerek, özellikle trend ve mevsimsellik olmayan zaman serilerini düzgün bir şekilde tahmin etmek için kullanılır. Bu yöntem, geçmiş verilere göre ağırlıklandırılmış bir ortalama hesaplar ve gelecekteki değerleri tahmin etmek için bu ortalama kullanır.


## Double Exponential Smoothing (Çift Üstel Düzeltme)

**Double Exponential Smoothing (Çift Üstel Düzeltme)**, zaman serilerinin düzeltilmesi ve tahmin edilmesi için kullanılan bir yöntemdir. Bu yöntem, zaman serilerindeki trend ve mevsimsel değişkenleri yakalamak için birincil üstel düzeltmeye (exponential smoothing) ek olarak geçmiş trendin düzeltilmiş bir versiyonunu kullanır. Bu, zaman serisi verilerindeki dalgalanmaları ve eğilimleri daha iyi modellemeye yardımcı olur.
Çift üstel düzeltme, tek üstel düzeltme yöntemine kıyasla daha karmaşıktır ve trend ile birlikte sezonluk değişkenleri de hesaba katar. Bu, gelecekteki değerleri tahmin etmek için daha kapsamlı bir model oluşturur. Markdown ile yazdığım gibi, çift üstel düzeltme yöntemi zaman serilerinin analizi için oldukça etkili bir araçtır.

## Triple Exponential Smoothing (Holt-Winters)

**Triple Exponential Smoothing veya diğer adıyla Holt-Winters**, zaman serilerini tahmin etmek için kullanılan bir yöntemdir. Bu yöntem, verinin trendi, sezonluk değişimleri ve mevsimsel etkileri dahil olmak üzere üç farklı bileşeni dikkate alır. Holt-Winters, Double Exponential Smoothing'e (Holt's method olarak da bilinir) ek olarak mevsimsel etkileri modellemek için kullanılır. Bu yöntem, trendin yanı sıra verinin mevsimsel dalgalanmalarını da yakalamak için kullanılır. Bu yöntem, zaman serisi verilerindeki trend, mevsimsel etkiler ve düzensizlikleri göz önünde bulundurarak gelecekteki değerleri tahmin etmek için oldukça etkili bir model sağlar. Triple Exponential Smoothing (Holt-Winters), zaman serilerinin analizi ve gelecekteki değerlerin tahmin edilmesi için kullanılan güçlü bir yöntemdir. Bu yöntem, özellikle zaman serilerinin trendleri ve mevsimsel değişimlerini modellemek istendiğinde tercih edilir.
***








