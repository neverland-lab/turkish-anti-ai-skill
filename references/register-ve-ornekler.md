# Register (Bağlam) Profilleri ve Uçtan Uca Dönüşüm Örnekleri

Doğal Türkçe tek bir kalıptan oluşmaz. Bir sözleşmedeki devrik cümle özensizlik, bir blog yazısındaki `-mAktAdIr` eki ise robotluk üretir. Bu dosya, metin türlerine göre 9 üslup boyutunun nasıl kalibre edileceğini ve uçtan uca (Before / After) dönüşüm örneklerini içerir.

## 1. Dokuz Boyutlu Register ve Üslup Matrisi

Kullanıcı özel bir yazar örneği (few-shot) vermediğinde aşağıdaki 6 profilden uygun olanı seç. Altıncı profil (kamu ve kurum içi yazışma) tablonun altında ayrıca anlatılır:

| Boyut | 1. Blog / Deneme / Sosyal Medya | 2. Teknik / Mühendislik | 3. Kurumsal / SaaS / İş İletişimi | 4. Akademik / Resmî / Hukuki | 5. Edebî / Anlatı |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Anlatıcı Kimliği** | Masanın karşısından anlatan deneyimli dost | Gece 2'de o hatayı çözmüş kıdemli mühendis | Müşteriye bizzat yazan net ve dürüst kurucu | Konuya hâkim, soğukkanlı araştırmacı/uzman | Düşüncesini yazarken inşa eden usta yazar |
| **Hitap** | Sen veya Siz (tutarlı) | Sen veya nötr 2. çoğul | Siz | 3. şahıs / nötr | Bağlama göre 1. veya 3. şahıs |
| **Cümle Uzunluğu & Burstiness** | Yüksek dalgalanma (4 kelime ile 28 kelime bir arada) | Orta-Yüksek (Kısa net yargılar + ulaçlı açıklamalar) | Orta (10-20 kelime, net ve taranabilir) | Orta-Uzun (15-30 kelime, sola dallanan yan cümleler) | Çok yüksek dalgalanma (nefes ritmine odaklı) |
| **Cümlecik Bağlama** | Ulaçlar (`-Ip, -IncA`) + nokta/virgül | Ulaçlar (`-Ip, -dIkçA, -ArAk`) + iki nokta | Ulaçlar + net sebep-sonuç bağlaçları | Sıfat-fiiller (`-An, -DIk`) + ulaçlar | Ulaçlar + ritmik tekrarlar ve virgül |
| **Kip Dağılımı** | `-yor`, `-DI`, `-mIş` (delil), geniş zaman | Geniş zaman (`-Ir/-Ar` kurallar için), `-DI`, `-mIş` | Geniş zaman, `-yor`, `-DI` | Geniş zaman, `-mAktAdIr` (100 kelimede yaklaşık 0,5-2,5), `-DIr` | Tüm kipler serbest |
| **Söylem Parçacıkları** | `işte, zaten, ise, hani, tabii, daha doğrusu` | `ise, aslında, daha doğrusu, örneğin` | `ise, özellikle, doğrudan` | Yalnızca `ise, nitekim, dolayısıyla` | Doğal akışa göre serbest |
| **Devrik Cümle Oranı** | 400 kelimede 2-3 adet | Sıfır (0) | Sıfır (0) | Sıfır (0) | Anlatı ritmine göre doğal |
| **Terim Tercihi** | Günlük karşılıklar veya okunuşa göre çekimli terim | Yerleşik İngilizce terim olduğu gibi (`endpoint'e`) | Sektör standardı, jargonsuz sade Türkçe | TDK ve alan terimleri (`veri tabanı, alan yazını`) | Türkçe duygu ve imge değeri yüksek sözcükler |
| **Açılış Hamlesi** | Sahne, somut gözlem veya doğrudan soru | Doğrudan problem veya mimari karar | Temel değer önermesi veya ana mesaj | Araştırma problemi veya olgusal çerçeve | Atmosfer, detay veya iç ses |

### 6. Kamu / Kurum İçi Yazışma

Kamu kurumunun iç notları, resmî yazıları, faaliyet raporları ve sunum açıklamaları bu profile girer. Bu register'da dil modeli izleriyle kurum dilinin birçok özelliği örtüşür, çünkü modeller büyük ölçüde bu tür metinlerden öğrenmiştir. Adlaştırma (*"uyku düzeninin bozulması"*), edilgen çatı, `-mAktAdIr` ve kurum terimleri (*süreç, müdahale, farkındalık, danışmanlık hizmeti*) burada çeviri kokusu değil, beklenen biçimdir. Bunları temizlemek metni resmiyetten çıkarır.

| Boyut | Kamu / Kurum İçi Yazışma |
| :--- | :--- |
| **Anlatıcı Kimliği** | Kurum adına yazan, nesnel uzman |
| **Hitap** | 3. kişi ya da kurumsal "biz" (*Belediyemiz ... olarak*). İç yazışmada okura doğrudan seslenilmez |
| **Cümle Uzunluğu & Burstiness** | Uzun (kamu belgelerinde ortanca 20 kelime, cümlelerin %35'i 28 kelimeden uzun). Ritim kuralı uygulanmaz |
| **Cümlecik Bağlama** | Ad-eylem, sıfat-fiil ve edat öbekleri (*nedeniyle, amacıyla, kapsamında*) |
| **Kip Dağılımı** | `-mAktAdIr`, `-DIr`, `-mIştIr`, geniş zaman ve edilgen. Faaliyet ve denetim raporlarında art arda `-mIştIr` ile biten cümleler olağandır (7 kamu belgesinde cümlelerin %34'ü `-mIştIr` ile bitiyor) |
| **Söylem Parçacıkları** | Yok |
| **Devrik Cümle Oranı** | Sıfır (0) |
| **Terim Tercihi** | Kurum ve mevzuat terimleri korunur |
| **Açılış Hamlesi** | Konu ve gerekçe |

**Onarımın kapsamı:** Yalnızca gerçek kusurlar düzeltilir: koşutluk ve ortak öge hataları, yanlış noktalama ve TDK yazım hataları, slogan biçimli başlıklar, sahneleme girişleri (*"... günümüzde"*), dolgu kalıpları (*"İşte bu noktada"*), şişirmeler (*"hayati bir önem"*) ve kapanış klişeleri (*"bu yolculukta ilk adımı"*). Adlaştırma, edilgen çatı ve `-mAktAdIr` temizlenmez.

## 2. Aynı İddianın 4 Farklı Register'daki Doğal Yazımı

- **Ham AI Çıktısı (Makine Türkçesi):**
  > *"Cache stratejisinin doğru bir şekilde belirlenmesi, sistem performansı açısından kritik bir öneme sahiptir ve gecikme sürelerinin azaltılmasında yadsınamaz bir rol oynamaktadır."*
- **Akademik / Resmî Register:**
  > *"Önbellekleme stratejisinin doğru belirlenmesi, sistem performansını ve yanıt sürelerini belirlemektedir."*
- **Teknik / Mühendislik Register:**
  > *"Cache stratejisini doğru kurmak performansı artırır ve gecikmeyi düşürür."*
- **Kurumsal / Ürün Register:**
  > *"Doğru önbellek stratejisi, sisteminizi hızlandırırken yanıt sürelerini kısaltır."*
- **Blog / Deneme Register:**
  > *"Performansı belirleyen şeylerden biri cache stratejisi. Doğru kurarsanız gecikme de azalıyor."*
  >
  > (Kaynak "yarı yarıya", "%40" gibi bir miktar vermediği için çıktı da vermez.)

## 3. Uçtan Uca (Before / After) Dönüşüm Örnekleri

### Örnek 1: Kurumsal / LinkedIn / Blog Yazısı

**Önce (Tipik AI Türkçesi):**
> Günümüzün hızla değişen iş dünyasında, uzaktan çalışma modeli sadece geçici bir trend değil, aynı zamanda kurumsal kültürün temel bir yapı taşı haline gelmiştir ve bu durumun önemi yadsınamaz. Şirketler tarafından gerçekleştirilen araştırmalar göstermektedir ki, çalışanlara esneklik sağlamak verimlilik üzerinde kritik bir rol oynamaktadır. Bununla birlikte, iletişim kopukluklarını önlemek adına bütüncül bir yaklaşım benimsenmelidir. Sonuç olarak, geleceğin çalışma dünyasında başarılı olmak isteyen kurumlar bu dönüşüme ayak uydurmak zorundadır.

**Yakalanan AI Sinyalleri:**
1. *"Günümüzün hızla değişen iş dünyasında"* (Sahneleme / Boş giriş - P0)
2. *"sadece X değil, aynı zamanda Y"* (Negatif paralellik - P0)
3. *"önemi yadsınamaz"* (Tier-1 klişe - P0)
4. *"Şirketler tarafından gerçekleştirilen araştırmalar göstermektedir ki"* (Edilgen çatı + kof fiil + belirsiz otorite + Hint-Avrupa `ki` - P1)
5. *"esneklik sağlamak ... kritik bir rol oynamaktadır"* (Kof fiil + Tier-1 klişe + `-mAktAdIr` şişmesi - P1)
6. *"Bununla birlikte ... bütüncül bir yaklaşım"* (Mekanik bağlaç + kurumsal jargon - P2)
7. *"Sonuç olarak ... ayak uydurmak zorundadır"* (Vaaz veren özet kapanış - P0)

**Sonra (Doğal İnsan Türkçesi - Blog/Deneme Register):**
> Uzaktan çalışma artık şirket kültürünün kalıcı bir parçası. Araştırmalar da aynı şeyi söylüyor: Çalışanlara esneklik tanıdığınızda verimlilik artıyor. İşin zor kısmı, ekip aynı ofisi paylaşmazken iletişimi koparmamak. Kalıcı çözüm ise çalışma düzenini baştan sona bu yeni ritme göre kurmak.

### Örnek 2: Teknik / Yazılım Mühendisliği Dokümanı

**Önce (Tipik AI Türkçesi):**
> ## Cache Stampede Problemi Ve Çözüm Yöntemleri
> Bir önbellek (cache) anahtarının süresi dolduğunda, aynı anda gelen birçok istek veritabanına yönlendirilir ve bu durum sistemde adeta bir darboğaz yaratmaktadır. Bu sorun özellikle yüksek bir trafiğe sahip olan uç noktalarda (endpoints) kritik bir öneme sahiptir. Bu problemi çözmek için dağıtık kilit (distributed lock) mekanizması kullanılabilir, ama bu yöntem gecikme süresini artırabilir.

**Yakalanan AI Sinyalleri:**
1. Başlıkta `Ve` bağlacının büyük yazılması ve klasik *"X Nedir ve Çözüm Yöntemleri"* şablonu (P2)
2. *"yönlendirilir ve bu durum ... yaratmaktadır"* (Ulaç yerine `ve bu durum` + `-mAktAdIr` - P1)
3. *"adeta bir darboğaz"*, *"yüksek bir trafiğe sahip olan"*, *"uç noktalarda"*, *"kritik bir öneme sahiptir"* (Tier-1 klişeler + gereksiz `"bir"` + zorlama teknik çeviri `"uç nokta"` - P0/P1)
4. `..., ama` (Karşıtlık bağlacı öncesi virgül - P2)

**Sonra (Doğal İnsan Türkçesi - Teknik Register):**
> ## Cache stampede sorunu ve çözümü
> Bir `cache` anahtarının süresi dolduğu anda gelen istekler hep birlikte veritabanına yönelip darboğaz oluşturur. Bu sorun özellikle yüksek trafikli `endpoint`'lerde önem kazanır. Dağıtık kilit (`distributed lock`) kullanabilirsiniz ama bu yöntem gecikmeyi artırabilir.

**Sadakat notu:** Kaynak "birçok istek" diyor, çıktı "yüzlerce" demez. Kaynak "artırabilir" diyor, çıktı ihtiyatı silip "artırır" demez. Kaynakta "kesinti" veya "kilitlenme" yok, çıktı bunları eklemez. Terim tutarlılığı için başlıkta ve gövdede aynı terim (`cache`) kullanılır.

### Örnek 3: Akademik / Analitik Metin (Olgusal Sadakat ve Dozaj Korunarak)

**Önce (Tipik AI Türkçesi):**
> Türkiye'de 2020-2024 yılları arasında yenilenebilir enerji yatırımları sadece artış göstermekle kalmamış, aynı zamanda enerji arz güvenliğinde de çığır açan bir dönüm noktası olmuştur. Enerji Bakanlığı tarafından paylaşılan verilere göre, güneş enerjisi kurulu gücü %112 oranında bir büyüme gerçekleştirmiştir ki bu durum sektörün dinamik yapısının en büyük kanıtıdır.

**Sonra (Doğal İnsan Türkçesi - Akademik Register):**
> Türkiye'de 2020-2024 döneminde hız kazanan yenilenebilir enerji yatırımları, enerji arz güvenliğinin yapısını da dönüştürmüştür. Enerji Bakanlığının verilerine göre güneş enerjisi kurulu gücü bu dönemde %112 büyümüştür.

### Örnek 5: Ritim Onarımı (Cümle Boyları Gösterilerek)

Dil modelinin ritim kusuru tek tek cümlelerde değil, paragrafın bütününde görünür. Kural okumak yetmez, cümle boylarını gerçekten saymak gerekir.

**Önce (deneme, cümle boyları: 18, 19, 18, 23 kelime, paragraf içi CoV yaklaşık 0,10):**
> Modern insanın en büyük paradoksu, sınırsız özgürlük ve seçenek bolluğu içinde derin bir yersiz yurtsuzluk hissiyle kuşatılmış olmasıdır. Her şeyin hızla tüketildiği, kimliklerin bile anlık tercihlere indirgendiği bu sıvılaşmış çağda birey, varoluşsal bir ağırlık merkezine ihtiyaç duyar. İşte gelenek, tam da bu noktada bir sığınak veya kaçış alanı olarak değil, bir "zemin" olarak devreye girer. İnsana dünyaya fırlatılmış yalnız bir atom olmadığını, kendisinden önce başlayan ve kendisinden sonra da devam edecek olan büyük bir anlatının parçası olduğunu hatırlatır.

**Sonra (cümle boyları: 13, 5, 16, 7, 20 kelime, paragraf içi CoV yaklaşık 0,46):**
> Modern insan sınırsız özgürlüğün ve seçenek bolluğunun ortasında derin bir yersiz yurtsuzluk duyuyor. En büyük paradoksu da bu. Her şeyin hızla tüketildiği, kimliklerin bile anlık tercihlere indirgendiği bu çağda birey bir ağırlık merkezi arar. Gelenek burada bir zemin olarak devreye girer. İnsana dünyaya fırlatılmış yalnız bir atom olmadığını, kendisinden önce başlayıp kendisinden sonra da sürecek büyük bir anlatının parçası olduğunu hatırlatır.

**Yöntem:**
1. Paragraftaki cümlelerin kelime sayısını yaz.
2. Art arda iki ya da üç cümle birbirine yakın uzunluktaysa birinin yargısını kısa bir cümleye ayır (*"En büyük paradoksu da bu."*) ya da iki cümleyi ulaçla birleştir.
3. Süsü at, yargıyı bırak: *"İşte ... tam da bu noktada"* dolgusu ve *"sığınak değil, zemin"* negatif paralelliği silindi, *"zemin"* yargısı kaldı.
4. Kaynakta olmayan cümle ekleme. Kısa cümle kaynaktaki bir yargıdan (*"en büyük paradoksu"*) çıkarıldı.

### Örnek 4: Kamu / Kurum İçi Yazışma (Kurum Dili Korunarak)

**Önce (Tipik AI Türkçesi):**
> Dijital Dünyada Kaybolmadan: Gençlerde Ekran Bağımlılığında Erken Farkındalık ve Aile Desteği
>
> Teknolojinin günlük yaşamın merkezinde yer aldığı günümüzde, gençlerin ekran karşısında geçirdiği süre giderek artıyor. [...] İşte bu noktada, sorunu henüz derinleşmeden fark etmek hayati bir önem taşıyor. Uyku düzeninin bozulması, ders başarısında düşüş, yüz yüze iletişimden kaçınma ve ekran süresine müdahale edildiğinde aşırı öfkelenme gibi belirtiler, erken uyarı sinyalleridir. [...] Yasaklayıcı ve suçlayıcı yaklaşımlar yerine; anlayışlı, kapsayıcı ve ailece yürütülen bir değişim süreci çok daha kalıcı sonuçlar verir. Ailenin sürece dahil olması [...]

**Sonra (Kamu / Kurum İçi Register):**
> Gençlerde Ekran Bağımlılığında Erken Farkındalık ve Aile Desteği
>
> Gençlerin ekran karşısında geçirdiği süre giderek artmaktadır. [...] Bu nedenle sorunun henüz derinleşmeden fark edilmesi büyük önem taşır. Gencin uyku düzeninin bozulması, ders başarısının düşmesi, yüz yüze iletişimden kaçınması ve ekran süresine müdahale edildiğinde aşırı öfkelenmesi gibi belirtiler erken uyarı işaretleridir. [...] Yasaklayıcı ve suçlayıcı yaklaşımlar yerine anlayışlı, kapsayıcı ve ailece yürütülen bir değişim süreci çok daha kalıcı sonuçlar verir. Ailenin sürece dâhil olması [...]

**Ne korundu, ne değişti:** Adlaştırmalar, `-mAktAdIr`, "süreç" ve "müdahale" gibi kurum terimleri olduğu gibi kaldı. Değişenler slogan başlık, sahneleme girişi, *"İşte bu noktada"* dolgusu, *"hayati"* şişirmesi, belirtiler listesinin biçim birliği (ad-eylem ile isim karışıktı), *"yerine;"* noktalı virgülü ve *"dahil"* yazımı. *"gibi belirtiler"* ifadesi korundu. Listeyi kapalı bir sayıma çevirmek kaynakta olmayan bir kesinlik eklerdi.
