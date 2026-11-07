# Derlem Ölçümleri: İnsan Türkçesi ve Dil Modeli Türkçesi

Bu dosyadaki sayılar skill'in ritim, noktalama ve devrik kurallarının dayanağıdır. Ölçümler Kasım 2026'da yapıldı. Kitap metinleri telif nedeniyle bu depoda yer almaz, yalnızca toplu istatistikler verilir.

## Yöntem

- **İnsan derlemi:** Türkçe yazmış 22 yazardan 24 kitap (17 kurmaca, 7 deneme/anı/inceleme). Çeviri eserler bilerek dışarıda bırakıldı, çünkü çeviri Türkçesi skill'in temizlemeye çalıştığı izleri taşır. Kitapların tamamı değil, her kitaptan %20, %50 ve %80 noktalarındaki 8'er sayfalık pencereler alındı (.txt ve .epub dosyalarında sayfa olmadığı için aynı noktalardan 4.000'er kelime). Ölçülen örneklem toplamı diyalog dâhil yaklaşık 215.000 kelimedir. Yazarlar: Adalet Ağaoğlu, İhsan Oktay Anar, Oğuz Atay, Enis Batur, Fakir Baykurt, Halide Edib Adıvar, Memduh Şevket Esendal, Sait Faik Abasıyanık, Cemil Meriç, Murathan Mungan, Aziz Nesin, Ömer Seyfettin, Orhan Pamuk (2), Peyami Safa (2), Sabahattin Ali, Kemal Tahir, Ahmet Hamdi Tanpınar, Hasan Ali Toptaş, Ayfer Tunç, Ahmet Ümit, Çetin Altan, Attila İlhan.
- **Model derlemi:** Beş modele aynı 8 istek verildi (4 kurmaca, 4 deneme, her biri yaklaşık 400-500 kelime): Gemini 4 Argon, Gemini 3.8 Flash, GPT-OSS 120B, Claude Sonnet 5.5, Claude Opus 5.5. İsteklerde "doğal yaz" ya da "yapay yaz" gibi yönlendirme yoktu.
- **Ölçüm:** Diyalog paragrafları çıkarıldı, yalnızca anlatı cümleleri sayıldı. Ritim, metin boyunca art arda gelen her 5 cümlelik pencerenin değişim katsayısıyla ölçüldü. Kitaplardan çıkarılan metinlerde gerçek paragraf sınırları güvenilir olmadığı için paragraf temelli ölçüm kullanılmadı. Biçim bilgisi (morfoloji) çözümleyicisi kullanılmadı, ölçümler düzenli ifadeye dayalı sezgisel ölçümlerdir. Devrik cümle sezgiseli 40 cümlelik bir doğrulama setinde bağımsız bir okurla %75 uyuştu. Bu yüzden devrik oranları kesin değer değil, göreli karşılaştırma içindir.

## Sonuçlar (ortanca değerler)

| Ölçüm | İnsan kurmaca | İnsan deneme | Uzun ve tekdüze modeller (Gemini 4 Argon, Gemini 3.8 Flash, GPT-OSS) | Kısa ve tekdüze modeller (Claude Sonnet, Claude Opus) |
| :--- | :--- | :--- | :--- | :--- |
| Ortanca cümle uzunluğu (kelime) | 8 | 10 | 12,5-18 | kurmaca 6,5-7, deneme 10,5 |
| 15-22 kelime bandındaki cümle oranı | %13 | %17 | %29-49 | %3-13 |
| 6 kelime ve altı cümle oranı | %40 | %23 | %0-13 | %18-50 |
| 5 cümlelik pencerede CoV (cümle uzunluğu değişim katsayısı) | 0,48 | 0,44 | 0,28-0,41 | 0,35-0,40 |
| CoV'si 0,40'ın altında kalan pencere oranı | %30 | %38 | %47-90 | %51-76 |
| Devrik cümle oranı (sezgisel) | %9,5 | %9 | %1-8 | %3-7 |
| Soru işareti (1000 kelimede) | 13,0 | 3,3 | 0-2,3 | 0-1,5 |
| Ünlem (1000 kelimede) | 6,7 | 0,6 | 0 | 0 |
| Üç nokta (1000 kelimede) | 9,0 | 0,8 | 0-1,2 | 0 |
| İki nokta (1000 kelimede) | 7,1 | 5,6 | 0-6,7 | 1,2-4,0 |
| Noktalı virgül (1000 kelimede) | 2,5 | 2,0 | 6,7-17,9 | 0-5,1 |
| `ki` bağlacı (1000 kelimede) | 2,7 | 3,5 | 0-1,2 | 1,2-1,3 |
| `olarak` (1000 kelimede, deneme) | - | 3,3 | 2,6-8,2 | 3,8 |
| Cümle sonu `-DIr` oranı (deneme) | - | %12 | %15-24 | %16 |

## Yorum

1. **Ortak iz ritimdir, cümle uzunluğu değil.** Bütün modellerde art arda gelen cümlelerin boy değişkenliği insan yazarlarınkinden düşük. En yakın olanlar Claude Opus ve Gemini Flash (kurmacada 0,40-0,41), en uzak olanlar GPT-OSS ve Gemini 4 denemeleri (0,29-0,31). Modellerin bir kısmı uzun cümlelere, bir kısmı kısa cümlelere yığılıyor. Bu yüzden skill'in ritim kuralı "kısa cümle ekle" değil, "ardışık cümlelerin boyunu çeşitlendir" biçiminde yazıldı.
2. **15-22 bandına yığılma Gemini ve GPT tipi modellerin işaretidir.** Claude tipi modeller ise kurmacada insan yazarlardan bile kısa cümle kurar.
3. **Modeller anlatıda neredeyse hiç soru, ünlem ve üç nokta kullanmaz.** Türk yazarların anlatısında bunlar olağandır.
4. **Noktalı virgül tek başına yapay zekâ işareti değildir.** Bazı yazarlar sık kullanır (bir yazarda 1000 kelimede 14). Ama Gemini ve GPT tipi modellerde sıklık 2-6 kat yüksektir.
5. **`ki` bağlacı genel bir şüphe işareti değildir.** Yazarlar modellerden daha sık kullanır, çoğunlukla kalıplaşmış biçimlerde (*demek ki, öyle ki, kaldı ki, dedi ki*).
6. **Sözlükteki tek tek klişelerin ayırt ediciliği modele göre değişir.** *Söz konusu* ve *dönüm noktası* hiçbir modelde sık değil. *Öte yandan* ve *Bununla birlikte* bazı modellerde (GPT-OSS, Claude Sonnet) cümle başında sık, Gemini'de seyrek. Modelleri en tutarlı ayıran şey cümle başı geçiş sözü alışkanlığı (*Oysa, Ancak, Sonuç olarak*) ve ritimdir.

## Skill Deneyi: Etkisi Ne Kadar?

Aynı ölçümler skill uygulanmış metinlere de yapıldı. Model, istemde skill'in tam metniyle çalıştı.

**Yazma modu (Gemini 4, 8 istek):**

| Ölçüm | İnsan | Gemini, skill'siz | Gemini, skill ile |
| :--- | :--- | :--- | :--- |
| 5 cümlelik pencerede CoV | 0,46 | 0,33 | 0,45 |
| CoV'si 0,40'ın altında kalan pencere | %36 | %80 | %30 |
| 15-22 kelime bandı | %13 | %37 | %32 |
| 6 kelime ve altı cümle | %34 | %6 | %23 |
| Soru işareti (1000 kelimede) | 6,7 | 0 | 4,7 |
| `ki` (1000 kelimede) | 2,8 | 0 | 2,4 |
| Noktalı virgül (1000 kelimede) | 2,5 | 7,6 | 6,8 |

Skill sıfırdan yazımda ritmi ve noktalama çeşitliliğini insan düzeyine yaklaştırıyor. Sonuç tekrarlarda da korundu: Gemini 4 ile ikinci çalıştırmada pencere CoV'si 0,44, 15-22 bandı %19 oldu. Gemini Flash ile pencere CoV'si 0,31'den 0,44'e çıktı, 15-22 bandı %41'den %17'ye indi. İki yan etki görüldü: Flash devrik cümleyi abarttı (%29, yazarlarda %9). Noktalı virgül sıklığı ise skill'in açık sınırına rağmen düşmedi (1000 kelimede 7-10). Noktalı virgül alışkanlığı bazı modellerde kurala baskın çıkıyor.

**Onarım modu (Gemini 4 onarıcı, 8 metin):** Kaynak metinlerde pencere CoV'si 0,34. Skill'in eski sürümüyle 0,38, ritim örneği eklenmiş sürümle iki ayrı çalıştırmada 0,39 ve 0,44 oldu. Onarımda etki yazıma göre küçük ve çalıştırmadan çalıştırmaya değişken, çünkü onarıcı kaynak cümlelerine bağlı kalıyor. Etki kaynağa göre de değişiyor: Claude Opus metinlerinde pencere CoV'si 0,38'den 0,43'e çıktı, GPT-OSS metinlerinde 0,31'den 0,33'e çıktı. Onarıcı modelin kendi alışkanlıkları da metne sızıyor: Onarıcı olarak kullanılan Gemini, hiç noktalı virgül içermeyen Opus metinlerine noktalı virgül ekledi.

**Kalite ve sadakat:** Yazma modunda aynı isteğe skill'siz ve skill'le yazılmış Gemini metinleri bağımsız bir model okura (Gemini) körlemesine verildi. Okur 8 isteğin 8'inde skill'le yazılmış metni daha doğal buldu. Onarım modunda aynı okur kaynak ve onarılmış sürümleri körlemesine sıraladı. Onarılmış sürümler 8 metnin 7'sinde kaynağın önüne geçti. Ritmi zorlayan sürüm her zaman daha doğal bulunmadı: Ritim için yeniden kurulan cümlelerde yeni hatalar görüldü. Skill'deki "ritim için yeni ifade icat etme" uyarısı bu yüzden eklendi. Sadakat denetiminde 8 onarımdan 5'i temiz, 3'ünde küçük kayıp vardı. Kayıpların ikisi kuralların yan etkisiydi (negatif paralellik ve kapanış kuralları), iki kurala da sınır eklendi.

## Sınırlamalar

- Model tarafı küçüktür (beş modelden 40 metin, yaklaşık 17.000 kelime). Sayılar yön göstericidir.
- İnsan derlemi edebî ve düşünsel metinlerden oluşur. Teknik metin için ayrı ölçüm gerekir. Kurum dili için 7 kamu belgesi ölçüldü (iki belediye faaliyet raporu, iki Sayıştay denetim raporu, bir yönerge, bir mevzuat metni, bir RAM raporu, toplam yaklaşık 36.000 kelime). Ortanca cümle uzunluğu 20 kelime, cümlelerin %35'i 28 kelimeden uzun, devrik oranı %2. Cümlelerin %34'ü `-mIştIr` ile bitiyor ve aynı ekle biten en uzun seri ortanca 9 cümle. Bu yüzden kurum register'ında ritim kuralı ve "art arda aynı ek" sınırı uygulanmaz.
- OCR ve PDF çıkarımından kaynaklanan hatalar temizlendi ama tamamen giderilemedi. Çıkarımı bozuk dört kitap derlemden çıkarıldı.
