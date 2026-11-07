# Derlem Ölçümleri: İnsan Türkçesi ve Dil Modeli Türkçesi

Bu dosyadaki sayılar skill'in ritim, noktalama ve devrik kurallarının dayanağıdır. Ölçümler Kasım 2026'da yapıldı. Kitap metinleri telif nedeniyle bu depoda yer almaz, yalnızca toplu istatistikler verilir.

## Yöntem

- **İnsan derlemi:** Türkçe yazmış 22 yazardan 24 kitap (17 kurmaca, 7 deneme/anı/inceleme). Çeviri eserler bilerek dışarıda bırakıldı, çünkü çeviri Türkçesi skill'in temizlemeye çalıştığı izleri taşır. Kitapların tamamı değil, her kitaptan %20, %50 ve %80 noktalarındaki 8'er sayfalık pencereler alındı (.txt ve .epub dosyalarında sayfa olmadığı için aynı noktalardan 4.000'er kelime). Ölçülen örneklem toplamı diyalog dâhil yaklaşık 215.000 kelimedir. Yazarlar: Adalet Ağaoğlu, İhsan Oktay Anar, Oğuz Atay, Enis Batur, Fakir Baykurt, Halide Edib Adıvar, Memduh Şevket Esendal, Sait Faik Abasıyanık, Cemil Meriç, Murathan Mungan, Aziz Nesin, Ömer Seyfettin, Orhan Pamuk (2), Peyami Safa (2), Sabahattin Ali, Kemal Tahir, Ahmet Hamdi Tanpınar, Hasan Ali Toptaş, Ayfer Tunç, Ahmet Ümit, Çetin Altan, Attila İlhan.
- **Akademik derlem:** Aynı yöntemle 8 Türkçe akademik ve inceleme kitabı (tarih, felsefe, siyaset bilimi, iktisat, bilim tartışması): Bahriye Üçok, Ahmet Cevizci, Tarık Zafer Tunaya, Doğan Avcıoğlu, Asaf Savaş Akat, İsmail Cem, Ahmet Yüksel Özemre, Aydın Topaloğlu. Örneklem toplamı yaklaşık 75.000 kelime. Kitaplar 1960'lardan 2000'lere uzanır, çoğu 2000 öncesidir, bugünkü dergi makalesi dilini tam temsil etmez.
- **Model derlemi:** Beş modele aynı 8 istek verildi (4 kurmaca, 4 deneme, her biri yaklaşık 400-500 kelime): Gemini 4 Argon, Gemini 3.8 Flash, GPT-OSS 120B, Claude Sonnet 5.5, Claude Opus 5.5. İsteklerde "doğal yaz" ya da "yapay yaz" gibi yönlendirme yoktu.
- **Ölçüm:** Diyalog paragrafları çıkarıldı, yalnızca anlatı cümleleri sayıldı. Ritim, metin boyunca art arda gelen her 5 cümlelik pencerenin değişim katsayısıyla ölçüldü. Kitaplardan çıkarılan metinlerde gerçek paragraf sınırları güvenilir olmadığı için paragraf temelli ölçüm kullanılmadı. Sabit genişlikte kırılmış satırlar cümle ortasında bölünmesin diye noktalamayla bitmeyen satırlar ölçümden önce bir sonraki satırla birleştirildi. (Bu düzeltme ilk ölçümde yoktu. Eklenince kurmaca değerleri neredeyse hiç değişmedi, deneme değerleri değişti: ortanca cümle 10'dan 12'ye, 15-22 bandı %17'den %23'e çıktı.) Biçim bilgisi (morfoloji) çözümleyicisi kullanılmadı, ölçümler düzenli ifadeye dayalı sezgisel ölçümlerdir. Devrik cümle sezgiseli 40 cümlelik bir doğrulama setinde bağımsız bir okurla %75 uyuştu. Bu yüzden devrik oranları kesin değer değil, göreli karşılaştırma içindir.

## Sonuçlar (ortanca değerler)

| Ölçüm | İnsan kurmaca | İnsan deneme | İnsan akademik | Uzun ve tekdüze modeller (Gemini 4 Argon, Gemini 3.8 Flash, GPT-OSS) | Kısa ve tekdüze modeller (Claude Sonnet, Claude Opus) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Ortanca cümle uzunluğu (kelime) | 8 | 12 | 14,5 | 12,5-18 | kurmaca 6,5-7, deneme 10,5 |
| 15-22 kelime bandındaki cümle oranı | %14 | %23 | %25 | %29-49 | %3-13 |
| 6 kelime ve altı cümle oranı | %37 | %17 | %16 | %0-13 | %18-50 |
| 5 cümlelik pencerede CoV (cümle uzunluğu değişim katsayısı) | 0,49 | 0,46 | 0,47 | 0,28-0,41 | 0,35-0,40 |
| CoV'si 0,40'ın altında kalan pencere oranı | %33 | %36 | %33 | %47-90 | %51-76 |
| Devrik cümle oranı (sezgisel) | %9,5 | %7 | ölçülemedi (bkz. yorum 7) | %1-8 | %3-7 |
| Soru işareti (1000 kelimede) | 13,0 | 3,3 | 1,1 | 0-2,3 | 0-1,5 |
| Ünlem (1000 kelimede) | 6,7 | 0,6 | 0,2 | 0 | 0 |
| Üç nokta (1000 kelimede) | 9,0 | 0,8 | 0,3 | 0-1,2 | 0 |
| İki nokta (1000 kelimede) | 7,1 | 5,6 | 4,9 | 0-6,7 | 1,2-4,0 |
| Noktalı virgül (1000 kelimede) | 2,5 | 2,0 | 5,6 | 6,7-17,9 | 0-5,1 |
| `ki` bağlacı (1000 kelimede) | 2,7 | 3,5 | 1,6 | 0-1,2 | 1,2-1,3 |
| `olarak` (1000 kelimede, deneme ve akademik) | - | 3,2 | 3,4 | 2,6-8,2 | 3,8 |
| Cümle sonu `-DIr` oranı (deneme ve akademik) | - | %12 | %25 | %15-24 | %16 |
| `-mAktAdIr` (100 kelimede) | 0 | 0,02 | 0,35 | 0 | 0 |

## Yorum

1. **Ortak iz ritimdir, cümle uzunluğu değil.** Bütün modellerde art arda gelen cümlelerin boy değişkenliği insan yazarlarınkinden düşük. En yakın olanlar Claude Opus ve Gemini Flash (kurmacada 0,40-0,41), en uzak olanlar GPT-OSS ve Gemini 4 denemeleri (0,29-0,31). Modellerin bir kısmı uzun cümlelere, bir kısmı kısa cümlelere yığılıyor. Bu yüzden skill'in ritim kuralı "kısa cümle ekle" değil, "ardışık cümlelerin boyunu çeşitlendir" biçiminde yazıldı.
2. **15-22 bandına yığılma Gemini ve GPT tipi modellerin işaretidir.** Claude tipi modeller ise kurmacada insan yazarlardan bile kısa cümle kurar.
3. **Modeller anlatıda neredeyse hiç soru, ünlem ve üç nokta kullanmaz.** Türk yazarların anlatısında bunlar olağandır.
4. **Noktalı virgül tek başına yapay zekâ işareti değildir.** Bazı yazarlar sık kullanır (bir yazarda 1000 kelimede 14). Ama Gemini ve GPT tipi modellerde sıklık 2-6 kat yüksektir.
5. **`ki` bağlacı genel bir şüphe işareti değildir.** Yazarlar modellerden daha sık kullanır, çoğunlukla kalıplaşmış biçimlerde (*demek ki, öyle ki, kaldı ki, dedi ki*).
6. **Sözlükteki tek tek klişelerin ayırt ediciliği modele göre değişir.** *Söz konusu* ve *dönüm noktası* hiçbir modelde sık değil. *Öte yandan* ve *Bununla birlikte* bazı modellerde (GPT-OSS, Claude Sonnet) cümle başında sık, Gemini'de seyrek. Modelleri en tutarlı ayıran şey cümle başı geçiş sözü alışkanlığı (*Oysa, Ancak, Sonuç olarak*) ve ritimdir.
7. **Akademik metin cümle boyunda modellere yaklaşır, ritimde yaklaşmaz.** Akademik kitaplarda 15-22 bandı %25 (en yüksek %30), noktalı virgül 1000 kelimede 5,6 (aralık 0,8-8,5). Bu iki ölçüt akademik metinde tek başına yapay zekâ işareti sayılmamalı. Pencere CoV'si ise kurmaca ve denemeyle aynı düzeyde (ortanca 0,47, kitaplar arasında 0,42-0,55). Akademik register'da da en güvenilir ayırt edici ölçüt ritimdir. Devrik sezgiseli akademik metinde %5-8 verdi ama elle bakılan 25 örneğin neredeyse hepsi hatalıydı: dipnot numaraları, kaynak gösterimleri ve yüklemi düşmüş ad cümleleri devrik sayılmıştı. Gerçek devrikler yalnızca alıntı şiir çevirilerindeydi. Akademik register'da devrik kullanılmaz kuralı bu yüzden korundu. `-mAktAdIr` bu kitaplarda beklenenden seyrek (100 kelimede ortanca 0,35, en yüksek 1,4). Ölçülen kitapların çoğu eski olduğu için bu sayı bugünkü makale dili için alt sınır sayılmalı.

## Akademik Makale Ölçümü (DergiPark)

Akademik kitapların çoğu eski olduğu için ayrıca güncel makale ölçüldü. DergiPark'ın açık arşivinden iki örneklem alındı. Her dergiden bir makale alındı ve alanlar karışık tutuldu (hukuk, tarih, eğitim, tıp, ziraat, iktisat, matematik, sosyoloji, ilahiyat). İlk örneklem ChatGPT öncesinde, 2016-2019 arasında yayımlanmış 19 makaledir (yaklaşık 106.000 kelime). İkinci örneklem 2026'da yayımlanmış 25 makaledir (yaklaşık 147.000 kelime). Ölçüm yalnızca "Giriş" ile "Kaynakça" arasındaki gövdeye yapıldı. İngilizce özet satırları, tablolar ve parantez içi atıflar çıkarıldı.

| Ölçüm | Makale 2016-2019 | Makale 2026 | Akademik kitap |
| :--- | :--- | :--- | :--- |
| `-mAktAdIr` (100 kelimede) | 1,0 (çeyrekler 0,5-1,2) | 1,0 (çeyrekler 0,6-1,6) | 0,35 |
| Ortanca cümle uzunluğu (kelime) | 18 | 19 | 14,5 |
| 15-22 kelime bandı | %26 | %30 | %25 |
| 5 cümlelik pencerede CoV | 0,46 | 0,42 | 0,47 |
| Cümle sonu `-DIr` oranı | %23 | %13 | %25 |
| Cümle sonu `-mIştIr` oranı | %17 | %22 | %15 |
| Art arda aynı ekle biten en uzun cümle serisi | 5 (çeyrekler 5-6) | 8 (çeyrekler 5-12) | - |
| Art arda üç `-mAktAdIr` serisi bulunan makale | 19'da 14 | 25'te 19 | 8'de 5 |
| Noktalı virgül (1000 kelimede) | 3,7 | 3,6 | 5,6 |

Yorum:

1. **Skill'in akademik `-mAktAdIr` aralığı (100 kelimede 0,5-2,5) makalelerle uyuşuyor.** İki örneklemde de ortanca 1,0. Kitaplardaki düşük değer (0,35) türden kaynaklanıyor: Makale dili kitap dilinden daha resmî.
2. **Art arda üç cümlenin aynı ekle bitmesi akademik yazıda olağandır.** ChatGPT öncesi makalelerin çoğunda üçlü `-mAktAdIr`, `-mIştIr` ya da `-DIr` serisi var. Bu yüzden "art arda üç cümle aynı ekle bitmez" kuralı akademik register'dan kaldırıldı. Dedektör akademik register'da yedi ve üstü seriyi işaretliyor. Bu sınırla 2016-2019 makalelerinin 19'unda 3'ü, 2026 makalelerinin 25'inde 19'u uyarı aldı.
3. **2026 makaleleri ChatGPT öncesi makalelerden farklı.** Cümle sonu `-DIr` oranı yarıya inmiş (fark anlamlı, permütasyon testi p<0,001), aynı ekle biten seriler uzamış (p≈0,02), pencere CoV'si düşmüş (p≈0,07). Bu fark yapay zekâ destekli yazımın izi olabilir. Ama örneklemler küçük ve alan dağılımları birebir eşleşmiyor. Bu yüzden bu bir kanıt değil, bir gözlemdir. Akademik insan referansı olarak 2026 makaleleri değil, 2016-2019 makaleleri kullanılmalı.

## Skill Deneyi: Etkisi Ne Kadar?

Aynı ölçümler skill uygulanmış metinlere de yapıldı. Model, istemde skill'in tam metniyle çalıştı.

**Yazma modu (Gemini 4, 8 istek):**

| Ölçüm | İnsan (kurmaca ve deneme, 24 kitap) | Gemini, skill'siz | Gemini, skill ile |
| :--- | :--- | :--- | :--- |
| 5 cümlelik pencerede CoV | 0,48 | 0,33 | 0,45 |
| CoV'si 0,40'ın altında kalan pencere | %33 | %80 | %30 |
| 15-22 kelime bandı | %17 | %37 | %32 |
| 6 kelime ve altı cümle | %33 | %6 | %23 |
| Soru işareti (1000 kelimede) | 8,2 | 0 | 4,7 |
| `ki` (1000 kelimede) | 2,7 | 0 | 2,4 |
| Noktalı virgül (1000 kelimede) | 2,3 | 7,6 | 6,8 |

Skill sıfırdan yazımda ritmi ve noktalama çeşitliliğini insan düzeyine yaklaştırıyor. Sonuç tekrarlarda da korundu: Gemini 4 ile ikinci çalıştırmada pencere CoV'si 0,44, 15-22 bandı %19 oldu. Gemini Flash ile pencere CoV'si 0,31'den 0,44'e çıktı, 15-22 bandı %41'den %17'ye indi. Claude Sonnet ile de aynı sonuç alındı: pencere CoV'si 0,36'dan 0,45'e çıktı, CoV'si 0,40'ın altında kalan pencere oranı %62'den %36'ya indi (insan yazarlarda %33), soru işareti 1000 kelimede 1,2'den 5,8'e çıktı. İki yan etki görüldü: Flash devrik cümleyi abarttı (%29, yazarlarda %8-9). Noktalı virgül sıklığı ise skill'in açık sınırına rağmen düşmedi (1000 kelimede 6,8-10). Noktalı virgül alışkanlığı bazı modellerde kurala baskın çıkıyor. Skill'in sonraki sürümüyle (derlem sayıları ve ritim örneğiyle) Gemini 4 iki kez yeniden yazdığında noktalı virgül 1000 kelimede 8,7'den 3,9 ve 5,7'ye indi, pencere CoV'si 0,45-0,49 oldu, devrik oranı %14-15'e çıktı (yazarlarda %9,5). Devrik cümleleri saydırıp sınırı aşanları düzelttiren bir talimat denendi, oran değişmedi, talimat eklenmedi. Skill'le yazan modellerde devriğin biçimi yazarlarınkine benziyor: Yüklemden sonraki kuyruk devriklerin %76-93'ünde 1-2 kelime (yazarlarda %83). Fark yalnızca sıklıkta: Gemini 4 %11-14, Flash %29, Claude Sonnet %8 (yazarlarda %9). Körlemesine okur iki skill sürümünü 4-4 berabere sıraladı, skill'siz metin 8 isteğin 8'inde sonuncu oldu.

**Akademik yazma (Gemini 4, 4 istek: tarih, felsefe, sosyoloji, iktisat):** Skill'siz Gemini akademik metinde çok düz yazdı: pencere CoV'si 0,23, bütün pencereler 0,40'ın altında, ortanca cümle 24 kelime, cümlelerin %74'ü `-mIştIr` ile bitiyor (yazarlarda %14), cümle başında sık sık *Sonuç olarak* ve *Öte yandan*. Skill'le iki çalıştırmada pencere CoV'si 0,35-0,36'ya çıktı ama model bütün uzun cümleleri orta boya indirdi: 28 kelimeyi aşan cümleler %35'ten %3-4'e düştü (yazarlarda %17), 15-22 bandı %38-44'te kaldı. Skill'e "akademik metinde uzun cümleyi koru, yanına kısa cümle koy" notu denendi. Üç çalıştırmada pencere CoV'si 0,39-0,42, uzun cümle oranı %6-12 oldu. Ama körlemesine okur (Gemini, akademik editör gözüyle) notlu metinleri daha doğal bulmadı: Üç sıralamada notsuz skill metni 12 karşılaştırmanın 9'unda birinci oldu, notun son sürümü girdiği 8 karşılaştırmanın hiçbirinde birinci olmadı. Okur, ritim için eklenen kısa cümleleri ("Öğrenme süreci böyle işler.") mekanik buldu, tarih anlatısında geniş zamana kaymayı da kusur saydı. Bu yüzden not skill'e eklenmedi. Akademik metinde ritim değişkenliğini zorlamak kaliteyi artırmıyor. Skill'siz metin ise 8 karşılaştırmanın 7'sinde sonuncu oldu, yani skill akademik metinde de işe yarıyor.
**Onarım modu (Gemini 4 onarıcı, 8 metin):** Kaynak metinlerde pencere CoV'si 0,34. Skill'in eski sürümüyle 0,38, ritim örneği eklenmiş sürümle iki ayrı çalıştırmada 0,39 ve 0,44 oldu. Onarımda etki yazıma göre küçük ve çalıştırmadan çalıştırmaya değişken, çünkü onarıcı kaynak cümlelerine bağlı kalıyor. Etki kaynağa göre de değişiyor: Claude Opus metinlerinde pencere CoV'si 0,38'den 0,43'e çıktı, GPT-OSS metinlerinde 0,31'den 0,33'e çıktı. Onarıcı model de belirleyici: Aynı 8 metni Claude Sonnet onardığında pencere CoV'si hiç değişmedi (0,34'ten 0,33'e), Gemini onardığında 0,38-0,44'e çıktı. Sonnet onarımda kaynak cümlelere çok sadık kalıyor. Bu, sadakat için iyi ama ritmi düzeltmiyor. Ritim onarımı isteniyorsa kullanıcıdan açıkça "cümle boylarını da düzelt" denmesi gerekebilir. Onarıcı modelin kendi alışkanlıkları da metne sızıyor: Onarıcı olarak kullanılan Gemini, hiç noktalı virgül içermeyen Opus metinlerine noktalı virgül ekledi.

**Kalite ve sadakat:** Yazma modunda aynı isteğe skill'siz ve skill'le yazılmış Gemini metinleri bağımsız bir model okura (Gemini) körlemesine verildi. Okur 8 isteğin 8'inde skill'le yazılmış metni daha doğal buldu. Onarım modunda aynı okur kaynak ve onarılmış sürümleri körlemesine sıraladı. Onarılmış sürümler 8 metnin 7'sinde kaynağın önüne geçti. Onarımda ritim kontrolünün de geçerli olduğu talimatı eklendikten sonra aynı 8 metin yeniden onarıldı (Gemini onarıcı) ve eski onarımla birlikte körlemesine sıralandı. İki sürüm 4-4 berabere kaldı, kaynak metin hiçbir sıralamada birinci olmadı. Ritim aynı düzeyde kaldı (pencere CoV'si 0,44 ve 0,43). Yeni sürümde noktalı virgül yarıya indi (1000 kelimede 5,3'ten 2,8'e), devrik oranı %12'den %7'ye döndü. Ritmi zorlayan sürüm her zaman daha doğal bulunmadı: Ritim için yeniden kurulan cümlelerde yeni hatalar görüldü. Skill'deki "ritim için yeni ifade icat etme" uyarısı bu yüzden eklendi. Sadakat denetiminde 8 onarımdan 5'i temiz, 3'ünde küçük kayıp vardı. Kayıpların ikisi kuralların yan etkisiydi (negatif paralellik ve kapanış kuralları), iki kurala da sınır eklendi.

## Sınırlamalar

- İnsan derleminin çoğu 20. yüzyıl yazarlarıdır. Ayrı bir denetim için iki çağdaş romandan (Alev Alatlı, Ayla Kutlu) örnek ölçüldü: Pencere CoV'si ikisinde de 0,50, soru işareti 1000 kelimede 8-15. Ritim bulgusu çağdaş romanda da geçerli görünüyor.
- Model tarafı küçüktür (beş modelden 40 metin, yaklaşık 17.000 kelime). Sayılar yön göstericidir.
- İnsan derlemi edebî ve düşünsel metinlerden oluşur. Teknik metin için ayrı ölçüm gerekir. Kurum dili için 7 kamu belgesi ölçüldü (iki belediye faaliyet raporu, iki Sayıştay denetim raporu, bir yönerge, bir mevzuat metni, bir RAM raporu, toplam yaklaşık 36.000 kelime). Ortanca cümle uzunluğu 20 kelime, cümlelerin %35'i 28 kelimeden uzun, devrik oranı %2. Cümlelerin %34'ü `-mIştIr` ile bitiyor ve aynı ekle biten en uzun seri ortanca 9 cümle. Bu yüzden kurum register'ında ritim kuralı ve "art arda aynı ek" sınırı uygulanmaz.
- OCR ve PDF çıkarımından kaynaklanan hatalar temizlendi ama tamamen giderilemedi. Çıkarımı bozuk dört kitap derlemden çıkarıldı.
