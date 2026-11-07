# Türkçe Cümle Mimarisi (Sentaks) ve Morfoloji Kılavuzu

İngilizce eğitimli dil modellerinin Türkçe çıktılarındaki temel sorun kelime dağarcığı değil, **cümle iskeletinin İngilizce (sağa dallanan SVO) kalmasıdır**. Bu kılavuz önce Türkçe cümlenin geometrisini, sonra çeviri kokan yapıları bu geometriye göre onarmanın kurallarını anlatır.

**Etiketler:**
- `[Dil bilgisi]`: Uyulmazsa cümle bozulur ya da anlam kayar. Dil bilgisi kaynaklarında tanımlı bir yapıya dayanır.
- `[Üslup]`: Uyulmazsa cümle yanlış olmaz ama çeviri kokar ya da ağırlaşır. Register'a göre esner.

**Gösterim:** Büyük harfler ünlü uyumu ya da ünsüz değişimiyle farklı biçimlere giren sesleri gösterir: `A` = a/e, `I` = ı/i/u/ü, `D` = d/t, `C` = c/ç. Ayraç içindeki `(y)`, ünlüyle biten kök ve gövdelerde araya giren kaynaştırma ünsüzüdür (`oku-y-up`, `gel-ip`).

**Dayanak:** Göksel ve Kerslake, *Turkish: A Comprehensive Grammar* (Routledge, 2005). Erguvanlı-Taylan, *The Function of Word Order in Turkish Grammar* (University of California Press, 1984). Yazım ve noktalama için TDK Yazım Kılavuzu.

## 0. Türkçe Cümlenin Geometrisi

Türkçe **baş sonda** (head-final) bir dildir: Öbeklerde belirleyen önce, belirlenen sonra gelir. İngilizce ise sıfat tamlaması ve `-'s` iyelik yapısı dışında çoğu öbekte (eylem öbeği, edat öbeği, yan cümle) bunun tersini yapar.

| Yapı | Türkçe dizilim | İngilizce dizilim |
| :--- | :--- | :--- |
| Cümle | tümleçler + yüklem (*Raporu gönderdim.*) | özne + yüklem + nesne (*I sent the report.*) |
| Ad tamlaması | tamlayan + tamlanan (*sunucunun belleği*) | *the memory of the server* |
| Niteleme | niteleyici yan cümle + ad (*dün kurduğumuz sunucu*) | *the server that we set up yesterday* |
| Edat öbeği | ad + son çekim edatı (*toplantıdan sonra*) | *after the meeting* |
| Yan cümle | yan cümle + ana yüklem (*Gecikeceğini söyledi.*) | *He said that he would be late.* |

Türkçe cümlenin ağırlık merkezi sondadır. Okur cümleyi soldan sağa kurar ve anlam yüklemle kapanır. İngilizce iskelet ise ana yüklemi erkenden verip ayrıntıyı sağa ekler. Bu kılavuzdaki kuralların hepsi bu farktan doğar.

### 0.1 Öge Dizilimi ve Bilgi Yapısı `[Dil bilgisi]`

Türkçede öge sırası serbest görünür ama her konumun bir görevi vardır:

| Konum | Görevi | Örnek |
| :--- | :--- | :--- |
| Cümle başı | Konu: bilinen, üzerine konuşulan öge, zaman ve yer çerçevesi | ***Bu sürümde** iki hata düzelttik.* |
| Yüklemin hemen önü | Odak: yeni ya da vurgulanan bilgi. Cümle vurgusu buraya düşer. | *Hatayı **Ayşe** buldu.* |
| Yüklemden sonra | Arka plan: bağlamdan zaten bilinen, ikincil bilgi | *Okumuyor kimse **bu raporları**.* |

- **Nötr sıra eğilimi:** özne, zaman, yer, dolaylı tümleç, nesne, yüklem (*Ekip dün toplantıda müşteriye yeni planı sundu.*).
- **Belirtisiz nesne yüklemden ayrılmaz:** Eksiz (belirtisiz) nesne yüklemin hemen önünde durur. *"Ahmet'e rapor gönderdim"* doğal, *"Rapor Ahmet'e gönderdim"* bozuk. Belirtili nesne (`-(y)I` ekli) daha serbesttir: Hem *"Raporu Ahmet'e gönderdim"* hem de *"Ahmet'e raporu gönderdim"* doğrudur, yalnızca vurgu değişir.
- **İngilizce yarık cümle (cleft) kopyası:** İngilizce vurguyu *"It was X that..."* ya da *"What made this possible was X"* ile verir. Türkçede odak yüklem önüne konur:
  - **Makine:** *"Bunu mümkün kılan şey, ekibin deneyimiydi."*
  - **İnsan:** *"Bunu ekibin deneyimi mümkün kıldı."*

### 0.2 Ağırlık: Uzun Öge Önce `[Üslup]`

Türkçede uzun ve ağır ögeler kısa ögelerden önce gelme eğilimindedir. Kısa öge yükleme yakın kalır:

- **Ağır:** *"Ahmet'e geçen hafta müşterilerden gelen bütün şikâyet e-postalarını ilettim."*
- **Dengeli:** *"Geçen hafta müşterilerden gelen bütün şikâyet e-postalarını Ahmet'e ilettim."*

İki cümle de dil bilgisi açısından doğrudur. İkincisinde uzun nesne önce okunup bitirilir, alıcı da yüklem önündeki vurgu konumuna oturur.

### 0.3 Gömme Derinliği: Sola Dallanmanın Sınırı `[Üslup]`

Sola dallanma Türkçenin doğal yönüdür ama sınırsız değildir. Bir adın önüne iç içe sıfat-fiil yan cümleleri yığılırsa okur yüklemi bulana kadar her şeyi aklında tutmak zorunda kalır. İngilizce iskeleti onarmaya çalışırken bu aşırılığa düşmek de yapay bir metin üretir.

- **Aşırı yığılmış:** *"Geçen ay müşterinin şikâyet ettiği hatayı düzelttiğimiz sürümde ortaya çıkan yeni sorunu inceleyen ekip rapor yazdı."*
- **Dengeli:** *"Geçen ay müşterinin şikâyet ettiği hatayı yeni sürümde düzelttik. Bu sürümde çıkan yeni sorunu inceleyen ekip rapor yazdı."*
- **Kural:** Bir ad öbeğinin önünde en fazla bir sıfat-fiil yan cümlesi bulunsun, onun içinde de en fazla bir gömülü yan cümle. Daha fazlası varsa cümleyi böl ya da yan cümlelerden birini ulaçla ana yükleme bağla.

## 1. Dallanma Yönü: Sağa Dallanmadan Sola Dallanmaya

İngilizce niteleyicileri ve yan cümleleri baş ismin sağına dizer (*We built a system that scans and reports data every night*). Dil modeli bu iskeleti Türkçeye iki yoldan taşır: Cümleyi bölüp işaret zamiriyle tekrarlar ya da `ki` ile bağlanan bir yan cümle kurar. Türkçe ise niteleyici yan cümleyi sıfat-fiille baş ismin önüne yerleştirir.

| Kusur Türü | Makine Türkçesi (Sağa Dallanan / Calque) | İnsan Türkçesi (Sola Dallanan Doğal Yapı) |
| :--- | :--- | :--- |
| **Kuyruk Yan Cümle** | Bir sistem kurduk, bu sistem her gece verileri tarayıp raporluyor. | Her gece verileri tarayıp raporlayan bir sistem kurduk. |
| **`ki` ile Kurulan Tümleç Yan Cümlesi** | Görüyoruz ki kullanıcılar bu özelliği kullanmıyor. | Kullanıcıların bu özelliği kullanmadığını görüyoruz. |

- **`öyle ... ki` bir hata değildir.** *"Öyle bir mimari tasarladık ki yüksek trafikte bile gecikme olmuyor."* yerleşik bir Türkçe sonuç yapısıdır ve sıfat-fiile çevrilince vurgu kaybolur. Sorun ancak metinde sık tekrar ederse ortaya çıkar.
- **`ki` genel bir şüphe işareti değildir.** Derlemde Türk yazarlar `ki` bağlacını dil modellerinden daha sık kullanıyor (1000 kelimede 2,7-3,5, modellerde 0-1,3). En sık kalıplar *var ki, dedi ki, demek ki, öyle ki, kaldı ki, elbette ki, yazık ki*. Şüpheli olan yalnızca İngilizce *that*-tümlecini kopyalayan *"Görüyoruz ki ..."*, *"Belirtmek gerekir ki ..."* tipidir.
- **Sıfat-fiil seçimi `[Dil bilgisi]`:** Nitelenen ad yan cümlenin öznesiyse `-(y)An` kullanılır (*kodu yazan geliştirici*). Nesnesi ya da başka bir ögesiyse `-DIk` veya `-(y)AcAk` ile iyelik eki kullanılır (*geliştiricinin yazdığı kod*, *yarın kuracağımız sunucu*). Bu ikisini karıştırmak cümleyi bozar: *"geliştiricinin yazan kod"* yanlıştır.

## 2. Bağlaç (`ve`) Yerine Ulaç (Zarf-Fiil) Sistemi

İngilizce sıralı eylemleri ve neden-sonuç bağlarını `and`, `and then`, `when`, `as` gibi ayrı kelimelerle bağlar. Türkçe ise **ulaç (zarf-fiil)** ekleriyle (`-(y)Ip`, `-(y)IncA`, `-DIkçA`, `-(y)ArAk`, `-mAdAn`) ve ek eylemin ulacı `-(y)ken` ile iki yüklemi tek akışta birleştirir. `-(y)ken` fiil köküne doğrudan gelmez, zaman ekinden sonra gelir (`ilerle-r-ken`, `çalış-ıyor-ken`).

| İlişki Türü | Makine Türkçesi (Mekanik Bağlaçlı) | İnsan Türkçesi (Ulaçlı Doğal Akış) | Kullanılan Ulaç Eki |
| :--- | :--- | :--- | :--- |
| **Ardışık Eylem** | Veriyi çektik ve sonra temizledik. | Veriyi çekip temizledik. | `-(y)Ip` |
| **Zaman / Tetikleme** | Cache doldu ve istekler yavaşlamaya başladı. | Cache dolunca istekler yavaşlamaya başladı. | `-(y)IncA` |
| **Orantı / Süreç** | Trafik arttı ve buna bağlı olarak hata oranı da yükseldi. | Trafik arttıkça hata oranı da yükseldi. | `-DIkçA` |
| **Yöntem / Araç** | Maliyetleri düşürdük ve bu sayede kârlılığı artırdık. | Maliyetleri düşürerek kârlılığı artırdık. | `-(y)ArAk` |
| **Zıtlık / Eş Zamanlılık** | Birinci grup hızlı ilerler ve ikinci grup geride kalır. | Birinci grup hızlı ilerlerken ikincisi geride kalır. | `-Ar` + `-ken` |

- **Sadakat sınırı `[Dil bilgisi]`:** Ulaç iki olay arasında zaman ya da neden bağı kurar. Kaynakta iki cümle yalnızca yan yana duruyorsa ulaçla bağlayıp yeni bir nedensellik uydurma. Virgülle ya da ayrı cümle olarak bırak.
- **Gizli özne `[Dil bilgisi]`:** Ulaçlı yan cümlenin öznesi söylenmemişse okur onu ana cümlenin öznesi sanar. *"Veriyi çekip sistem çöktü."* cümlesi, veriyi sistemin çektiğini söyler. Özne farklıysa ya açıkça yaz ya da iki cümle kur: *"Veriyi çektik, ardından sistem çöktü."*
- **Olumsuzluk kapsamı `[Dil bilgisi]`:** Ana yüklemdeki olumsuzluk `-(y)Ip` ile bağlanan eyleme de yayılabilir. *"Raporu okuyup onaylamadı."* hem "okudu ama onaylamadı" hem de "ikisini de yapmadı" diye anlaşılabilir. Yalnızca ikinci eylem olumsuzsa açık yaz: *"Raporu okudu ama onaylamadı."*
- **Zıtlık ulaçla kurulmaz `[Dil bilgisi]`:** `-(y)Ip` sıralama ve bağlama bildirir, zıtlık bildirmez. *"Komşunun sesini duyuyoruz ama adını bilmiyoruz."* cümlesi *"Komşunun sesini duyup adını bilmiyoruz."* olursa karşıtlık kaybolur. Zıtlık için *ama*, *oysa* ya da `-(y)ken` kullan (*"Sesini duyarken adını bilmiyoruz."*).
- **Virgül `[TDK]`:** Ulaçtan sonra virgül konmaz. Yalnızca art arda gelen ulaçlar virgülle ayrılır.

## 3. Ek Eylem (`-DIr`) ve `-mAktAdIr`: İki Ayrı Sorun

Bu iki yapı sık karıştırılır ama farklı yerlerde çalışır, onarımları da farklıdır.

### A. `-mAktAdIr` (eylem çekimi)

`-mAktA` (`-mAk` + `-DA`) resmî üslupta süren eylemi bildirir, bildirme eki `-DIr` ile birleşince *artmaktadır, sağlamaktadır* olur. İngilizce şimdiki ve geniş zamanın resmî Türkçeye refleks çevirisidir.

- Akademik, hukuki ve resmî yazışma dışındaki register'larda `-(I)yor` ya da `-Ar/-Ir` kullan.
- **Makine:** *"Bu yöntem geliştiricilere büyük kolaylık sağlamaktadır."*
- **İnsan:** *"Bu yöntem geliştiricilerin işini kolaylaştırıyor."*

### B. Ad cümlesinde bildirme eki `-DIr`

Ad soylu yüklemde `-DIr` ek eylemin bildirme ekidir (*Bu yöntem etkilidir.*). Fiildeki `-mAktAdIr` gibi `-Ar/-Ir` ya da `-(I)yor` ile değiştirilemez. İki seçenek vardır: eki korumak ya da düşürmek.

- **Tanım ve sınıflandırma cümlelerinde korunur:** *"Redis bir anahtar-değer veri tabanıdır."* Ek düşerse (*"Redis bir anahtar-değer veri tabanı."*) cümle yanlış olmaz ama konuşma diline kayar. Belge ve kılavuz metninde ek kalsın.
- **Anlatı ve sohbet akışında seyreltilir:** Art arda her ad cümlesini `-DIr` ile bitirmek metni ders kitabına çevirir.
  - **Makine:** *"Bu yöntem oldukça etkilidir. Burası sistemin en kritik parçasıdır."*
  - **İnsan (blog):** *"Bu yöntem oldukça etkili. Burası da sistemin en kritik parçası."*
- **Anlam farkı:** Konuşma dilinde `-DIr` tahmin de bildirir. Bu kullanım ad soylu yükleme de çekimli fiile de gelir (*"Şimdi evdedir."*, *"Yorulmuştur."*). Gündelik metne eklenen her `-DIr` cümleye ya resmîlik ya da belirsizlik katar.

### C. Grup çekimi (ek eksiltme) `[Üslup]`

Aynı eki alan sıralı yüklemlerde Türkçe eki yalnızca sonuncuya getirir. Eki her yüklemde tekrarlamak İngilizce `is ... and is` dizilişinin kopyasıdır.

- **Makine:** *"Bu yöntem hızlıdır ve güvenilirdir."*
- **İnsan:** *"Bu yöntem hızlı ve güvenilirdir."*

### D. Doz

Akademik register'da `-mAktAdIr` ve `-DIr` korunur. Ölçülen makalelerde 100 kelimede ortanca 1 `-mAktAdIr` var (2016-2019 ve 2026 DergiPark örneklemleri, çeyrekler 0,5-1,6), skill'in 0,5-2,5 aralığı bununla uyuşuyor. Art arda üç dört cümlenin aynı ekle (`-mektedir`, `-mıştır`, `-dır`) bitmesi insan akademik yazısında olağandır: ChatGPT öncesi 19 makalenin 14'ünde üçlü `-mAktAdIr` serisi var, en uzun seri ortanca 5. Yediyi geçen seriyi geniş zaman (`-Ar/-Ir`), `-DI` ya da ad cümlesiyle kır. Ayrıntı: `derlem-olcumleri.md`.

## 4. Vurgu Yuvası (Yüklem Önü) ve Devrik Cümle

İngilizce sabit dizilimde vurguyu cümleyi yararak (*It is X that...*) ya da kelimeyi **kalın** yazarak verir. Dil modeli bunu Türkçeye *"İşte tam da bu noktada..."*, *"Asıl önemli olan şey şudur ki..."* gibi dolgu kalıplarıyla taşır.

Türkçede vurgu yüklemin hemen önündeki ögeye düşer. Aynı ögeleri yeniden dizmek yeterlidir:

- *"Raporu dün **Ahmet'e** gönderdim."* (Kime gönderildiği öne çıkıyor.)
- *"Raporu dün Ahmet'e **ben** gönderdim."* (Gönderenin kim olduğu öne çıkıyor.)
- *"Raporu Ahmet'e **dün** gönderdim."* (Ne zaman gönderildiği öne çıkıyor.)
- *"Dün Ahmet'e **raporu** gönderdim."* (Neyin gönderildiği öne çıkıyor.)

### Devrik Cümle

Yüklemden sonraki konum, bağlamdan bilinen ve ikinci planda kalan bilgiye ayrılmıştır. Gündelik, edebî ve blog Türkçesinde yüklemi öne almak metne konuşma sıcaklığı katar:

- **Düz:** *"Kimse bu uzun hata raporlarını sonuna kadar okumuyor."*
- **Devrik (blog):** *"Kimse sonuna kadar okumuyor bu uzun hata raporlarını."* (Raporlar bağlamda zaten geçtiği için yüklemden sonraya alınabilir.)
- **Sınır `[Dil bilgisi]`:** Yeni bilgi ve belirtisiz nesne yüklemden sonraya alınmaz. *"Ahmet'e gönderdim rapor."* bozuk bir cümledir.
- **Kota `[Üslup]`:** Teknik, kurumsal ve akademik register'larda devrik cümle kullanma. Blog/deneme ve anlatı register'ında devrik cümleyi seyrek tut, her cümleyi devrik yapmak yeni bir yapay tike dönüşür. 22 Türk yazarının 24 kitabından oluşan derlemde anlatı cümlelerinin yaklaşık %9,5'i, deneme cümlelerinin %7'si devrik, model metinlerinde %1-8 (sezgisel ölçüm, `derlem-olcumleri.md`). Yazarlarda yüklemden sonra gelen kısım %83 oranında 1-2 kelimedir: zamir (*beni, ona*), işaret sözü (*bu*), özel ad ya da *belki, zaten, hiç* gibi bir zarf.

## 5. Zamir Düşürme (Pro-Drop) ve `"Bir"` / `"Kendi"` Yoğunluğu

### A. Kişi ve İşaret Zamiri Düşürme

Türkçe özneyi yüklemdeki kişi ekiyle (`-(y)Im/-m`, `-sIn/-n`, `-(y)Iz/-k`, `-sInIz/-nIz`, `-lAr`), aitliği iyelik ekiyle zaten bildirir. İngilizcedeki zorunlu `I, we, they, it, this` zamirlerini her cümleye taşımak metni ağırlaştırır:

- **Makine:** *"Biz önce veri tabanını yedekledik, sonra biz migration script'ini çalıştırdık. O sorunsuz tamamlandı."*
- **İnsan:** *"Önce veri tabanını yedekledik, ardından migration script'ini çalıştırdık. İşlem sorunsuz tamamlandı."*
- **Anlam `[Dil bilgisi]`:** Türkçede açıkça söylenen özne zamiri karşıtlık ya da vurgu bildirir. *"Ben gittim."* cümlesi "başkası değil, ben" anlamına kayar. Bu yüzden gereksiz zamir yalnızca ağırlık değil, istenmeyen bir vurgu da ekler.

### B. `"Bir"` Yoğunluğu

Sıfat ile ad arasındaki `bir`, Türkçenin kendi belirsizlik işaretidir: *güzel bir gün*, *iyi bir insan*, *derin bir iz bıraktı* doğal Türkçedir. Sorun tek tek kullanımlar değil, **yoğunluktur**. Dil modeli her sıfat tamlamasına İngilizce `a/an` karşılığı olarak `bir` ekler:

- **Makine:** *"Bu güncelleme **büyük bir önem** taşıyor ve **yüksek bir performans** ile **iyi bir kullanıcı deneyimi** sunuyor."*
- **İnsan:** *"Bu güncelleme **büyük önem** taşıyor, **yüksek performans** ve **iyi kullanıcı deneyimi** sunuyor."* (Pazarlama dili kaynağın kendi içeriğidir. Bu örnekte onarılan yalnızca `bir` yoğunluğudur.)
- **Kural `[Üslup]`:** Önce kalıplaşmış birleşik eylemlerin içindeki `bir`i at (*önem taşımak*, *artış göstermek*, *rol oynamak*). Bir cümlede birden fazla *sıfat + bir + soyut ad* varsa seyrelt. Tekil ve somut bir olayı anlatan `bir`e dokunma.

### C. İngilizce `his/her/its own` Çevirisi Olan Gereksiz `"Kendi"`

- **Makine:** *"Her servis **kendi veri tabanına** bağlanır ve **onun kendi** yapılandırmasını okur."*
- **İnsan:** *"Her servis kendi veri tabanına bağlanıp yapılandırmasını okur."* (İyelik eki `-(s)I` zaten aitliği verir. Karşıtlık yoksa `kendi` tekrarlanmaz.)

## 6. Edilgen Çatı (`tarafından`), Adlaştırma ve Kof Yardımcı Fiil

### A. `"tarafından"`

Edilgen çatı Türkçenin kendi yapısıdır ve bilgi yapısını taşır. *"Köprü Mimar Sinan tarafından yapıldı."* kusursuz bir cümledir: Konu köprüdür, yeni bilgi Mimar Sinan'dır. Etkene çevirmek konuyu değiştirir. Çeviri kokusu iki durumda ortaya çıkar:

1. Eyleyen yazarın kendisi ya da kendi kurumu olduğunda:
   - **Makine:** *"Yeni kimlik doğrulama modülü güvenlik ekibimiz tarafından test edilmiş ve onaylanmıştır."*
   - **İnsan:** *"Güvenlik ekibimiz yeni kimlik doğrulama modülünü test edip onayladı."*
2. `tarafından` kof bir eylemle birlikte geldiğinde (*tarafından gerçekleştirilmiştir*, *tarafından sağlanmaktadır*).

### B. Adlaştırma Zincirleri `[Üslup]`

Dil modeli eylemi ada çevirip ardından bir yardımcı eylemle yeniden eyleme bağlar: *"-mAsI gerekmektedir"*, *"-mAsI sağlanmalıdır"*, *"-mAsI önem arz etmektedir"*. Türkçede eylem çoğu zaman doğrudan çekimlenebilir:

- **Makine:** *"Verilerin düzenli olarak yedeklenmesinin sağlanması gerekmektedir."*
- **İnsan:** *"Veriler düzenli olarak yedeklenmeli."*

### C. Kof Yardımcı Fiiller

Tek eylemle söylenebilecek işler ad + yardımcı eylem öbekleriyle şişirilir. Bu öbeklerin çoğu Türkçede yerleşiktir, sorun **sıklık** ve `-mAktAdIr` ile birlikte kullanımdır:

| Şişirilmiş Öbek | Doğal Seçenek | Örnek Dönüşüm |
| :--- | :--- | :--- |
| **gerçekleştirmek / icra etmek** | yapmak, düzenlemek, kurmak, tamamlamak | *"Toplantı gerçekleştirdik"* -> *"Toplantı yaptık"* / *"Analiz gerçekleştirdi"* -> *"Analiz etti"* |
| **sağlamak** (aşırı kullanım) | vermek, kazandırmak, doğrudan oldurgan ya da ettirgen çatı (`-DIr`, `-t`) | *"Hız artışı sağlar"* -> *"Sistemi hızlandırır"* / *"Destek sağlar"* -> *"Destek verir"* |
| **katkıda bulunmak** (aşırı kullanım) | desteklemek, yararı dokunmak | *"Büyümesine katkıda bulunmaktadır"* -> *"Büyümesini destekliyor"*. `Katkıda bulunmak` TDK Güncel Türkçe Sözlük'te yer alan yerleşik bir deyimdir. Onun yerine sözlükte yer almayan `katkı sunmak` önerme. |
| **sahip olmak** (`have / has` çevirisi) | `-lI` eki, `var`, `içermek`, `taşımak` | *"Yüksek hıza sahiptir"* -> *"Çok hızlıdır"* / *"Üç katmana sahiptir"* -> *"Üç katmandan oluşur"* |
| **ev sahipliği yapmak** (`host / feature`) | barındırmak, yer almak | *"Bölge birçok tarihî yapıya ev sahipliği yapmaktadır"* -> *"Bölgede pek çok tarihî yapı var"* |
| **rol oynamak** (`play a role`) | belirlemek, etkilemek | *"Kritik bir rol oynamaktadır"* -> *"Sonucu belirler"* |
| **yer almak / bulunmak** (`-mAktAdIr` ile) | `var`, bulunma eki `-DA` | *"Raporda üç bölüm yer almaktadır"* -> *"Raporda üç bölüm var"* |
| **olan** (gereksiz sıfat-fiil) | `olan`ı düşür | *"Önemli olan bir adım"* -> *"Önemli bir adım"* |
| **olarak** (zincirleme kullanım) | `-DA`, `-CA` veya doğrudan yüklem | *"İlk adım olarak veriyi sildik"* -> *"İlk adımda veriyi sildik"*. *"Sonuç olarak"* resmî metinde olağandır. Hedef, her paragrafın sonuna refleksle eklenen özet etiketidir. |

## 7. Kanıtsallık (`-mIş`) ve Zaman Seçimi

- **Görülen ve öğrenilen geçmiş (`-DI` ve `-mIş`):** Türkçe, olayı görüp görmediğini fiil çekiminde ayırır. İngilizce bunu yapmaz (*The server crashed at 3 AM*). Dil modeli bu yüzden neredeyse hiç `-mIş` kullanmaz. Olay sonradan öğrenilmiş ya da kayıttan çıkarılmışsa, özellikle gündelik ve blog register'ında `-mIş` doğaldır:
  - **Düz anlatım:** *"Gece yarısı bellek sızıntısı oldu ve servis kapandı. Sabah log'lara baktığımızda fark ettik."*
  - **Kanıtsal anlatım:** *"Gece yarısı bellek sızıntısı olmuş, servis de kapanmış. Sabah log'lara bakınca fark ettik."*
  - **Sınır `[Üslup]`:** Olay sonrası raporlarında ve resmî tutanaklarda, kayıtla kesinleşmiş olgu için `-DI` olağandır. `-mIş` ekini zorla yayma.
- **Geniş zaman (`-Ar/-Ir`) ve şimdiki zaman (`-(I)yor`):** Genel doğrular için ikisi de doğal Türkçedir (*"Dünya Güneş'in çevresinde dönüyor."*). Geniş zaman daha tanımsal ve resmî bir ton verir.
  - **Teknik tanım ve şartnamede** geniş zamanı tercih et: *"Redis veriyi bellekte tutar, diske ise asenkron yazar."*
  - **Kural `[Üslup]`:** Aynı paragrafta aynı türden bilgiyi anlatırken ikisini karıştırma.

## 8. Ad Tamlaması Zincirlerini Kırma `[Üslup]`

İngilizce teknik ve kurumsal ad öbeklerini (*customer segmentation module performance optimization process*) Türkçeye belirtisiz ad tamlamalarıyla üst üste zincirleyerek aktarmak okunabilirliği yok eder. Tamlayan eki almadan art arda dizilen adların sayısı üçü geçmesin, fazlasını sıfat-fiil ya da hâl ekleriyle çöz:

- **Makine:** *"Müşteri segmentasyon modülü performans iyileştirme çalışması sonuç raporu"*
- **İnsan:** *"Müşteri segmentasyon modülünün performansını iyileştirme çalışmasının sonuç raporu"* (Kaynakta çalışmayı kimin yaptığı yazmıyor, bu yüzden "yaptığımız" gibi bir özne eklenmez.)

## 9. Cümleler Arası Bağlantı

### A. `"Bu da ... anlamına gelir"` Kalıbı `[Üslup]`

İngilizcedeki *which means* ve *this means that* yapıları Türkçeye cümle başında `Bu da` ile başlayan ikinci bir cümle olarak taşınır. Bağlantı çoğu zaman tek cümlede kurulabilir:

- **Makine:** *"Cache süresi kısa tutuldu. Bu da veri tabanı yükünün artması anlamına geliyor."*
- **İnsan:** *"Cache süresi kısa tutulduğu için veri tabanı yükü artıyor."*

### B. Öz Düzeltme ve Söylem Parçacıkları

Makine Türkçesi her şeyi baştan mutlak bir kesinlikle biliyormuş gibi yazar. İnsan yazar düşünürken cümleyi daraltır, çekince koyar ve Türkçenin söylem parçacıklarını (`ise`, `zaten`, `de`, `yani`, `bir de`, `tabii`, `daha doğrusu`) yerli yerinde kullanır:

- **Makine:** *"Silme işlemi idempotenttir, bu nedenle dağıtık sistemlerde tercih edilir."*
- **İnsan:** *"Silme işlemi idempotent. Dağıtık sistemlerde tercih edilmesinin nedeni de bu."* (Parçacık ve cümle bölme ritmi değiştirir ama kaynağa yeni bir iddia eklemez.)
- **Makine:** *"Birinci yöntem hızlıdır, ikinci yöntem yavaştır."*
- **İnsan:** *"Birinci yöntem hızlı, ikincisi ise yavaş."*
- **Sınır `[Üslup]`:** Her parçacık silme testinden geçmeli. Kaldırıldığında anlamdan ya da tondan bir şey eksilmiyorsa o parçacık süstür, silinir.

## 10. Koşutluk: Cümlenin Simetrisi

`ve`, virgül ya da ikili bağlaçla (`hem ... hem`, `ne ... ne`) bağlanan ögeler aynı görevi taşıyorsa aynı biçimde kurulur. Birden fazla yükleme ortak bağlanan öge de her yüklemin istediği biçime uymalıdır. Türkçe dil bilgisi kitaplarında bu hatalar "anlatım bozukluğu" başlığı altında geçer.

Dil modeli bu hataları sık yapar, çünkü İngilizcede ad hâl eki almaz. *"We review and include user feedback"* cümlesinde iki eylem tek nesneyi rahatça paylaşır. Türkçede ise her yüklem nesnesine kendi hâl ekini dayatır.

### A. Ortak öge her yüklemin hâline uymalı `[Dil bilgisi]`

Bir ögeyi iki yükleme ortak bağlamak ancak iki yüklem de aynı hâli istiyorsa mümkündür. Biri belirtme (`-(y)I`), öteki yönelme (`-(y)A`) istiyorsa ikinci yükleme ögeyi zamirle yeniden bağla:

- **Bozuk:** *"Kullanıcı geri bildirimlerini inceliyor ve yol haritamızda yer veriyoruz."* (`incelemek` neyi, `yer vermek` neye ister.)
- **Doğru:** *"Kullanıcı geri bildirimlerini inceliyor ve bunlara yol haritamızda yer veriyoruz."*
- **Bozuk:** *"Açık kaynak kütüphanelere güveniyoruz ama güvenlik taramasından geçirmeden kullanmıyoruz."*
- **Doğru:** *"Açık kaynak kütüphanelere güveniyoruz ama onları güvenlik taramasından geçirmeden kullanmıyoruz."*

Hâl ekleri aynı olsa bile ortak öge ikinci yükleme anlamca uymayabilir:

- **Anlam kayması:** *"Müşteri verilerinin gizliliğini önemsiyor ve üçüncü taraflarla paylaşmıyoruz."* (Paylaşılmayan şey gizlilik olur.)
- **Doğru:** *"Müşteri verilerinin gizliliğini önemsiyor ve bu verileri üçüncü taraflarla paylaşmıyoruz."*

### B. Ortak özne her yüklemin çatısına uymalı `[Dil bilgisi]`

Aynı özne bir etken, bir edilgen yükleme birlikte bağlanamaz. Ulaçlı yan cümlede de durum aynıdır (bkz. Bölüm 2, gizli özne):

- **Bozuk:** *"Sistem gelen istekleri doğruladıktan sonra veri tabanına kaydedilir."* (Kaydedilen sistem olur.)
- **Doğru:** *"Sistem gelen istekleri doğruladıktan sonra veri tabanına kaydeder."*
- **Bozuk:** *"Şirketimiz karbon ayak izini azaltarak sürdürülebilirlik hedeflerine katkı sağlandı."*
- **Doğru:** *"Şirketimiz karbon ayak izini azaltarak sürdürülebilirlik hedeflerine katkıda bulundu."*
- **Hata olmayan durum:** Öznesi ayrı iki cümle farklı çatıda olabilir. *"Ekip testleri tamamladı ve yeni sürüm yayına alındı."* doğrudur.

### C. Ortak ek ancak her kanada uyuyorsa düşürülür `[Dil bilgisi]`

Grup çekimi (Bölüm 3C) ekin bütün kanatlarda aynı olmasını gerektirir. Kişi eki ya da olumsuzluk farklıysa ek düşürülemez:

- **Bozuk (kişi):** *"Pazarlama ekibi yeni kampanyalara, siz ise müşteri bağlılığına odaklanacak."*
- **Doğru:** *"Pazarlama ekibi yeni kampanyalara odaklanacak, siz ise müşteri bağlılığına odaklanacaksınız."*
- **Bozuk (olumsuzluk):** *"Model hızlı ve doğruluğu yeterli değildi."* (`değil` grup çekiminde bütün kanatlara yayılır, cümle modelin hızlı olmadığını da söyler.)
- **Doğru:** *"Model hızlıydı ama doğruluğu yeterli değildi."*

### D. Sıralanan ögeler aynı biçimde kurulmalı `[Dil bilgisi]`

Eş görevli ögeler yalın ad-eylem (`-mAk`), iyelik eki almış ad-eylem (`-mAsI`, `-(y)IşI`) ve ad öbeği arasında karışırsa liste dağılır, ögelerden biri ya da birkaçı ortak yükleme bağlanamaz:

- **Bozuk:** *"Bu güncellemenin amaçları arayüzü hızlandırmak, bellek sızıntılarının giderilmesi ve daha kolay bir kurulum."*
- **Doğru:** *"Bu güncellemenin amaçları arayüzü hızlandırmak, bellek sızıntılarını gidermek ve kurulumu kolaylaştırmak."*
- **Bozuk:** *"İyi bir uzaktan çalışma düzeni için düzenli iletişim kurmak, görev dağılımında şeffaflık ve çalışanların motivasyonunu korumamız gerekir."*
- **Doğru:** *"İyi bir uzaktan çalışma düzeni için düzenli iletişim kurmak, görevleri şeffaf dağıtmak ve çalışanların motivasyonunu korumak gerekir."*

### E. İkili bağlaçlarda kanatlar denk olmalı `[Dil bilgisi]`

`hem ... hem`, `ne ... ne`, `ya ... ya`, `ister ... ister` bağlaçlarının iki kanadı aynı türden ögelerle kurulur:

- **Bozuk:** *"Arayüz hem kullanıcı dostu bir deneyim sunuyor hem de erişilebilirlik standartlarına tam uyumluluk."* (İlk kanat yüklem, ikincisi ad öbeği.)
- **Doğru:** *"Arayüz hem kullanıcı dostu bir deneyim sunuyor hem de erişilebilirlik standartlarına tam uyuyor."*
- **Bozuk:** *"İster bulut sunucusu kiralayın ister kendi donanımınıza yatırım yaparak süreci yönetmek mümkün."*
- **Doğru:** *"İster bulut sunucusu kiralayarak ister kendi donanımınıza yatırım yaparak süreci yönetebilirsiniz."*

`ne ... ne` yargıyı kendisi olumsuz yapar, yüklem olumlu çekimlenir. Konuşmada olumsuz yüklemle de duyulur ama yazı dilinde anlatım bozukluğu sayılır:

- **Bozuk:** *"Bu strateji ne sunucu maliyetini düşürmedi ne de yanıt süresini kısaltmadı."* (Biri olumlu biri olumsuz iki yüklem, *"ne ... düşürdü ne de ... kısaltmadı"*, daha da açık bir bozukluktur.)
- **Doğru:** *"Bu strateji ne sunucu maliyetini düşürdü ne de yanıt süresini kısalttı."*

### F. Yapay Simetri `[Üslup]`

Dil modeli cümleleri anlamın gerektirmediği bir simetriyle kurar. En sık görülen üç biçim:

- **Ayna karşıtlık:** *"Teknoloji insan için vardır, insan teknoloji için değil."*
- **Zincirleme tekrar:** *"Veriyi anlamak geleceği anlamaktır, geleceği anlamak değişimi yönetmektir."*
- **Aynı kalıba dökülmüş üçlü:** *"Bu platform hızıyla zamanı, güvenliğiyle veriyi, esnekliğiyle geleceği korur."*

Bunlar slogan dilidir ve çoğu zaman somut bilgi taşımaz. Onarımda süsü at ve geriye kalan somut iddiayı söyle:

- **Makine:** *"Bu platform hızıyla zamanı, güvenliğiyle veriyi, esnekliğiyle geleceği korur."*
- **İnsan:** *"Bu platform hızlı, güvenli ve esnek."* (Kaynakta üç özellik var, üçü de kalır. Sorun üçlü liste değil, üç ögenin aynı kalıba dökülmesidir.)

Kaynakta somut bir iddia yoksa onu uydurma. Cümleyi sil ya da `[somut veri: ...]` yer tutucusu bırak. Aynı tik paragraf düzeyinde de görülür: Her paragraf aynı iskeletle (iddia, açıklama, özet cümlesi) kurulur. Paragrafların biçimini içerik belirlesin.

- **Sınır:** Simetri silme testinden geçiyorsa korunur. Gerçek bir karşıtlığı (*"Birinci yöntem hızlı, ikincisi ise yavaş."*) ya da gerçekten koşut iki olguyu anlatan simetri Türkçenin doğal bir aracıdır.
