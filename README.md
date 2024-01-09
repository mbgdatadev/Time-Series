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
***

## Makine Öğrenmesi ile Time Series 
Makine öğrenimi, zaman serisi verileri üzerinde de uygulanabilen bir dizi teknik içerir. Zaman serisi, belirli aralıklarla toplanan veya ölçülen verilerdir ve genellikle zamanla değişen bir deseni veya trendi temsil ederler. Makine öğrenimi, bu zaman serilerindeki desenleri anlamak, tahmin etmek veya analiz etmek için kullanılabilir. İşte EDA'nın temel bileşenleri:

1. ### Problem and Dataset (Problem ve Veri Seti)
    - **Problem**: Zaman serisi analizi çeşitli problemler için kullanılabilir. Tahmin (Forecasting), Anomali Tespiti (Anomaly 
     Detection),Desen Tanıma (Pattern Recognition) gibi problemler olabilir
    - **Dataset**: Zaman serisi analizi için uygun bir dataset, zamanla değişen bir değişkenin periyodik olarak ölçüldüğü veya 
       toplandığı bir veri kümesidir.
2. ### Exploratory Data Analysis (Keşifçi Veri Analizi)
   **Keşifçi Veri Analizi (EDA)**, bir veri kümesini anlamak, keşfetmek ve içindeki desenleri, ilişkileri veya önemli özellikleri 
     belirlemek için kullanılan bir veri analizi yöntemidir. EDA'nın amacı, veri kümesini daha derinlemesine inceleyerek hipotezler 
     oluşturmak ve veri hakkında önemli bilgiler elde etmektir.
   - **Veri Görselleştirme**: Veri görselleştirme, EDA'nın merkezinde yer alır. Grafikler, histogramlar, kutu grafikleri, scatter 
     plotlar gibi görsel araçlar kullanılarak verinin dağılımı, trendleri, ilişkileri gözlemlenir. Bu görsel analizler, veri içindeki 
      desenleri ve anomaliyi daha iyi anlamak için kullanılır.

    - **Merkezi Eğilim ve Dağılım Ölçüleri**: Verinin merkezi eğilimini (ortalama, medyan, mod) ve dağılımını (standart sapma, varyans, 
     çeyrekler) inceleyerek verinin genel özellikleri hakkında bilgi edinilir.

     - **Eksik Veri ve Aykırı Değerlerin İncelenmesi**: Veri kümesinde eksik veriler veya aykırı değerler varsa, bu durumlar incelenir. 
    Eksik verilerin nasıl işleneceği veya aykırı değerlerin model üzerindeki etkisi değerlendirilir.

    - **Değişkenler Arası İlişkilerin İncelenmesi**: Farklı değişkenler arasındaki ilişkileri anlamak için korelasyon, kovaryans gibi 
   istatistiksel metrikler kullanılır. Bu, özellikler arasındaki ilişkileri ve olası bağımlılıkları anlamak için önemlidir.

   - **Özellik Mühendisliği İpuçları**: Veri keşfi sırasında elde edilen bilgiler, yeni özelliklerin oluşturulmasına veya mevcut 
    özelliklerin dönüştürülmesine yönelik ipuçları sağlayabilir. Bu, modelin daha iyi performans göstermesine yardımcı olabilir.
3. ###  Feature Engineering (Değişken Mühendisliği)
     **Feature Engineering (Değişken Mühendisliği)**, makine öğrenimi modellerinin performansını artırmak veya daha iyi sonuçlar elde 
     etmek için mevcut veri özelliklerini veya değişkenlerini (feature) dönüştürme, oluşturma veya seçme sürecidir. Bu, daha anlamlı, 
     daha öngörücü veya daha kolay anlaşılır özellikler oluşturarak veri setinin kalitesini artırmayı hedefler.Feature Engineering'in 
     amacı, modele girecek olan özelliklerin kalitesini ve anlamlılığını artırarak modelin daha iyi performans göstermesini sağlamaktır. 
     Bazı Feature Engineering teknikleri şunları içerir:
   
   - **Özellik Dönüştürme (Feature Transformation)**: Var olan özellikleri başka bir biçime dönüştürmek. Örneğin, logaritmik dönüşüm, 
     normalleştirme, ölçeklendirme gibi.
   - **Özellik Birleştirme (Feature Aggregation)**: Mevcut özelliklerden yeni özellikler oluşturma. Örneğin, ortalama, medyan, toplam 
      gibi istatistiksel özetler oluşturarak özellikleri birleştirmek.
   - **Özellik Seçimi (Feature Selection)**: Önemli veya anlamlı olmayan özellikleri belirleyerek model için sadece en önemli 
     özellikleri seçmek.
   - **Yeni Özellikler Oluşturma (Creating New Features)**: Mevcut özelliklerden yeni özellikler türetmek. Örneğin, kategorik bir 
     değişkeni sayısal bir değişkene dönüştürmek veya tarih/saat özelliklerinden yeni özellikler çıkarmak.
   - **Boyut Azaltma (Dimensionality Reduction)**: Yüksek boyutlu veri setlerinde özellik sayısını azaltmak için teknikler kullanmak.    

4. ### Lag/Shifted Features (Gecikme/Değiştirilmiş Özellikler)
     **Lag veya shifted features**, veri setindeki bir değişkenin önceki zaman noktalarına göre kaydırılmış veya gecikmiş 
        versiyonlarıdır. Bu versiyonlar, zaman serisi verilerinde veya sıralı veri setlerinde bir değişkenin geçmiş değerlerini temsil 
        eder. Bu işlem aşırı öğrenmenin önüne geçmek içiçnde kullanılır. Örneğin, bir zaman serisi verisinde bir değişkenin değerleri 
        gün bazında kaydedilmiş olabilir. Bir değişkenin bir gün önceki, bir hafta önceki veya daha önceki zamanlardaki değerleri, 
        gelecekteki bir değişkenin değerlerini tahmin etmek veya ilişkileri incelemek için kullanılabilir. Bu gecikmiş özellikler, 
        genellikle tahmin modelleri veya zaman serisi analizinde kullanılır. Geçmiş zamanlardaki değişken değerlerinin şu anki zaman 
        için etkisinin modelleme sürecinde dikkate alınması, daha iyi tahminler yapmaya veya ilişkileri anlamaya yardımcı olabilir.
        Gecikmiş özellikler, bir değişkenin önceki zamanlardaki değerlerini temsil ettiği için, özellikle zaman serisi verileri veya 
        sıralı veri setlerinde geçmişin bugünkü veya gelecekteki durumu anlamak için önemli bir araçtır. Bu tür özellikler, Feature 
        Engineering adımında model performansını artırmak için kullanılabilir.

5. ### Rolling Mean Features (Hareketli Ortalama Özellikleri)

   **Hareketli ortalama özellikleri**, zaman serisi verilerindeki değişkenin belirli bir zaman dilimindeki ortalamasını temsil eden 
     özelliklerdir. Bu özellikler, bir değişkenin zamanla değişen trendlerini veya düzensizliklerini daha yumuşatmak veya vurgulamak 
     için kullanılır. Hareketli ortalama, belirli bir pencere veya dönem boyunca değişkenin değerlerinin ortalamasını alarak her zaman 
     aralığı için yeni bir değer oluşturur. Örneğin, 10 günlük hareketli ortalama, her 10 günlük periyotta değişkenin ortalamasını 
     hesaplar. Her yeni zaman noktası için, son 10 günün değerlerinin ortalaması o zaman noktasının hareketli ortalamasıdır.
     Hareketli ortalama özellikleri, veri setindeki ani dalgalanmaları düzleştirerek trendleri veya genel eğilimleri daha net bir 
     şekilde göstermeye yardımcı olabilir. Özellikle zaman serisi verilerindeki gürültüyü azaltmak veya değişkenin daha genel bir 
     davranışını anlamak için kullanılırlar. Örneğin, hisse senedi fiyatları analizinde, kapanış fiyatları üzerindeki 50 günlük 
     hareketli ortalama, fiyatların kısa vadeli dalgalanmalarını azaltarak genel bir trendi daha net bir şekilde gösterir. Bu tür 
     özellikler, tahmin modelleri veya analizler için kullanılabilecek önemli bir araçtır.

6. ### Exponentially Weighted Features (Üstel Ağırlıklı Ortalama Özellikleri)
     **Üstel Ağırlıklı Ortalama (Exponentially Weighted Average, EWA)**, zaman serisi verilerindeki değişkenin geçmiş değerlerinin 
     ağırlıklı ortalamasını hesaplayan bir yöntemdir. Bu yöntemde, son gözlemlere daha fazla ağırlık verilirken, daha eski gözlemlere 
     azalan bir şekilde ağırlık verilir. Üstel Ağırlıklı Ortalama, geçmiş değerlerin ağırlığının zamanla azaldığı bir sürekli bir 
     süreçtir. Her bir yeni gözlem için, önceki ağırlıklı ortalamaya, yeni gözlemin ağırlıklı bir versiyonu eklenir. Bu, mevcut 
     değerlerin yanı sıra önceki değerlerin değişik oranlarda dikkate alınmasına olanak tanır. Bu teknik, daha eski gözlemlerin 
     etkisini zamanla azaltırken, daha yakın zamandaki gözlemlerin daha fazla etkili olmasını sağlar. Bu da değişkenin trendlerini veya 
     genel eğilimlerini anlamak için kullanışlı olabilir. Özellikle, üstel ağırlıklı ortalama, ani dalgalanmaların azaltılmasına veya 
     gürültünün düzeltilmesine yardımcı olabilir. Bu yöntem, zaman serisi verileri üzerinde düzenli ve sürekli bir şekilde 
     kullanılabilir ve değişkenlerin zamanla nasıl değiştiğini daha iyi anlamak için kullanılır. 

