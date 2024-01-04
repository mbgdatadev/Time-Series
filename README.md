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

## ARIMA
**ARIMA**, otoregresif bütünleşik hareketli ortalama anlamına gelir (Autoregressive Integrated Moving Average). Zaman serisi analizinde kullanılan bir modeldir. ARIMA modelleri, zaman serilerindeki yapısal örüntüleri anlamak, gelecekteki değerleri tahmin etmek veya verilerdeki trendleri ve döngüleri analiz etmek için kullanılır.

**AR (p)**: Otoregresif terimi, geçmiş zamandaki değerlerin, bugünkü değeri tahmin etmede kullanılmasıyla ilgilidir. "p" değeri, kaç önceki değerin modelde kullanılacağını belirtir. Örneğin, AR(2) bir ARIMA modeli, son iki zaman aralığının etkilerini içerir.

**I (d)**: Bütünleşik terimi, zaman serisinin ne kadar farklılaştırılacağını belirtir. Düzgünleştirme yaparak verinin sabit bir seviyeye getirilmesine yardımcı olur. "d" değeri, bu farkın kaç kez alınacağını ifade eder. Örneğin, d=1 ise veri bir kez fark alınmış demektir.

**MA (q)**: Hareketli ortalama terimi, zaman serisindeki rastgele bir şokun, geçmiş hataların bir kombinasyonuyla modeli etkileyebileceğini ifade eder. "q" değeri, modelde kullanılacak hareketli ortalama terimlerinin sayısını belirtir.

Bu parametrelerle birlikte, ARIMA modeli zaman serisindeki trendleri, sezgisel örüntüleri ve yapısal değişimleri modellemek için kullanılır. Bu model, gelecekteki değerleri tahmin etmek veya zaman serisindeki desenleri anlamak için kullanılabilir.

***
## SARIMA

**SARIMA**, Mevsimsel Otoregresif Bütünleşik Hareketli Ortalama (Seasonal Autoregressive Integrated Moving Average) modelidir. SARIMA, ARIMA modelinin mevsimsel bileşenleri de içeren genişletilmiş bir versiyonudur.

**(p, d, q)**: Bunlar ARIMA'nın temel parametreleriyle aynıdır ve zaman serisinin otoregresif, bütünleşik ve hareketli ortalama bileşenlerini ifade eder.

**(P, D, Q)**: Bu parametreler, mevsimsel bileşenlerin otoregresif, bütünleşik ve hareketli ortalama terimlerini belirtir.

**m**: Mevsimsel döngünün periyodunu ifade eder. Örneğin, aylık verilerde m=12 olabilir çünkü yıllık bir mevsimsellik var.

SARIMA, zaman serilerindeki mevsimsel desenleri modellemek ve tahmin etmek için kullanılır. Mevsimsel etkileri olan veri setleri için uygun bir seçenek olabilir. Örneğin, periyodik bir deseni olan aylık satış verileri veya mevsimsel olarak değişen bir ekonomik gösterge gibi veri setleri üzerinde kullanılabilir.

Bu model, hem mevsimsel hem de genel trendleri dikkate alarak zaman serisi verilerini analiz etmeye olanak tanır. SARIMA, ARIMA modeline benzer bir şekilde, zaman serilerindeki yapısal örüntüleri anlamak ve gelecekteki değerleri tahmin etmek için kullanılır. Ancak, SARIMA modeli, mevsimsel etkileri de dahil ederek daha kapsamlı bir analiz sunar.






