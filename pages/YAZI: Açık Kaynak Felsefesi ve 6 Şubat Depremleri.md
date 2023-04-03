Açık kaynak yazılımdan bahsettiğimizde genelde insanların zihinlerinde kaynak kodunun herkes tarafından görüntülenebileceği, değiştirilebileceği ve yeniden dağıtılabileceği yazılımlar sayesinde paylaşarak büyüyen bir ekosistem gelir. Yazılım geliştirme sürecinde saydamlığı, iş birliğini ve yenilikleri teşvik ederek daha güvenli, daha inovatif ve daha erişilebilir yazılımların oluşmasına katkı sağladığı için önem verdiğimiz açık kaynak felsefesinin, afet anında aynı amaç altında toplanan binlerce yazılımcının birlikte çalışmasını mümkün kılarak arama kurtarma organizasyonun sağlanmasında hatta insan hayatının kurtarılmasında kilit rol oynaması açık kaynağın çok daha fazlası olabileceğini düşünmemiz gerektiğini gösterdi.

6 Şubat’ta gerçekleşen iki büyük deprem sonrasında saatler içerisinde Eser Özvataf ve Furkan Kılıç öncülüğünde her türlü geliştirici ve gönüllünün davet edildiği AYA: Açık Yazılım Ağı Discord kanalı kuruldu. Depremzedelerin yardımına koşmak için bir araya gelen birçok gönüllü geliştirici, açık kaynak yaklaşımıyla hareket ederek bu Discord kanalı üzerinden iletişim kurup ihtiyaç duyulan yazılımları hızlı bir şekilde işlevsel hale getirdi.

Ve sadece 36 saat içerisinde afetbilgi.com, afetharita.com ve beniyiyim.com gibi 3 kocaman proje canlıya alındı. 

Ürettikleri açık yazılımları herkesle paylaşan gönüllü geliştiriciler sayesinde, yardım ekipleri ve depremzedeler arasındaki koordinasyon sağlanarak birçok insanın kurtarılması ve yardımların ilgili yerlere iletilmesi mümkün oldu. Bu sonucun ortaya çıkmasında açık kaynak felsefesinin benimsenmesi kilit rol oynadı ve bu sayede gönüllü geliştiriciler sürece dahil olup hızlı hareket edebildi. 

## Bu süreçte açık kaynak olarak geliştirilen birkaç web sitesi ve platformdan bahsetmek gerekirse:


**-afetharita.com:** Yapay zeka ve makine öğrenimi teknolojileri kullanılarak sosyal medyadaki yardım talepleri okunaklı verilere dönüştürüldü ve elde edilen veriler, afetharita.com üzerinde görselleştirildi. Daha sonrasında afet ile ilgili ihtiyaç duyulabilecek önemli verilerin ilgili kurumlardan toplanıp haritaya eklenmesi sağlanarak 35 milyon toplam istek ve 627 bin özel ziyaretçi rakamlarına ulaşıldı. STK'lar, gönüllüler ve afetzedelerin afet ile ilgili önemli verilere ulaşmasında büyük etki sağladılar.
 
 ![afetharita](https://miro.medium.com/v2/resize:fit:720/format:webp/1*20USbTHR9zXa3SvRjOC8uA.png)

Geliştirilme sürecinin başında hızlı çalışan, basit bir kullanıcı deneyimi olan ve sürekli ayakta kalabilen bir uygulama geliştirmeye karar verdiler. Böylelikle düşük internet hızında ve telefondan erişim durumunda dahi STK gönüllüleri hızlıca bu bildirilen konumları görebilecek ve depremzedelere yardım edebilecekti. Bu yüzden harita için Leaflet teknolojisini kullanmaya karar verdiler. İlk 12 saat doğru konumlama üzerine çalıştılar. Bu süreçte alt ekiplere ayrılarak hızlı bir şekilde geliştirme sürecine başladılar. Geliştirme sürecinde test ekipleri henüz oluşturulmadığı için kullanıcı geri bildirimlerine önem verdiler. Hangi renklerin hangi verileri gösterdiğini belirtmek için haritaya lejant eklediler. Büyük veri kümelerinde harita üzerindeki işlemlerin daha hızlı ve akıcı gerçekleşebilmesi için Leaflet.markercluster isimli eklentiyi kullandılar. 

37 saat sonra testleri biten afetharita.com’u canlıya aldılar. 72 saat içerisinde AKUT gibi STK’lar bu kanalı değerlendirmeye aldılar ve ihbar yönetimine entegre ettiler. Backend kısmında yaşanan aksaklıklar sonucu API tarafı Emre Savcı liderliğinde yeniden yazıldı, backend ve frontend ekipleri senkronize çalışmaya başladı. 

Daha sonra uygulamayı iyileştirmek için zoom her değiştiğinde istek atmasını engellemek için Google Haritalar’dan esinlendikleri “Alanı Tara” butonu eklendi. Eğitilen yapay zeka modeli artık paylaşımların niyetini de ayırt edebilir hale geldiği için filtreleme özellikleri eklendi.

144 saat sonrasında ekipler koordineli olarak çalışıyor, arka tarafta Go ile yazılmış yeni API ile hız probleminin önüne geçilmiş ve fazlasıyla optimize edilmiş bir sistem kurulmuştu. STK, dernek, yardım kuruluşları, hastaneler vb. tarafından paylaşılan konum ve diğer bilgiler haritaya eklenmeye devam etti. Çoklu dil seçeneği ve harita ayarlarında uydu- arazi seçenekleri gibi yeni özellikleri eklemeye devam ettiler.
 
![afetharita2](https://user-images.githubusercontent.com/119361280/229272456-2619c664-5e67-4015-b614-fa6dd281b939.png)

1 hafta sonra afetharita.com milyonlarca istek alıp insanlara fayda sağlıyordu. Diğer ülkelerdeki yardım toplama noktalarını ve detaylarını gösterebilmek için afetharita.com üzerinden yurtdışına da veri ve bilgi aktarımı yapılmaya başlandı. Geliştiricilerinin hedefi bu uygulamanın baştan sona indirilip kurulabilen bir programa dönüştürülebilmesi ve tüm dünyaya ücretsiz olarak hizmet sunarak herhangi bir afet durumunda özelleştirilip kullanılabilir olması.

Sitenin geliştirilmesinde Lead Developer olan Eray Gündoğmuş’un tüm geliştirme sürecini ve discord’daki organizasyonu detaylarıyla anlattığı [yazısını](https://gundogmuseray.medium.com/afetharita-com-binlerce-depremzedeye-nas%C4%B1l-yard%C4%B1m-etti-f3ec0cd4adbe) okumanızı tavsiye ederim.

**-beniyiyim.com :** Enkaz altında kalan insanların durumlarının iyi veya kötü olduğunu adres bilgileri ile girebilecekleri ve diğer insanlara bildirebilecekleri bir form projesidir.

**-afetbilgi.com:** Deprem sonrası geçici barınma alanları, güvenli toplanma alanları, para-eşya bağışı imkanları, kan bağışı noktaları gibi gereken tüm özet bilgilere ulaşabileceğiniz web sitesidir.

**-deprem.io ve depremyardim.com:** Deprem İmece Platformu tarafından geliştirilen ulaşılamayan kişilerin bilgisinin girilebildiği iki farklı ortak platformdur. Aynı zamanda yardım iste & yardım sağla sisteminde yardım akışının yönetilmesine katkı sağlar. Bilgileri Ahbap, AKUT ve AFAD ile paylaşır, ayrıca Twitter’dan yayınlanan tweetleri yapay zeka ile adres bilgilerini alıp sisteme ekleyebilir.

**-https://huggingface.co/deprem-ml:** Kısaca altında birçok yazılım uzmanının çalıştığı, depremle ilgili bir yapay zeka açık kaynak platformudur. Depremin ilk gününde, depremzedelerin yardım çağrılarını yazılı bir şekilde Instagram hikayesi veya tweet olarak paylaştıklarını gözlemlediler. Bu verileri otomatik olarak çekip anlamlı hale getirmek amacıyla makine öğrenimi tabanlı uygulamalar oluşturmak ve ayrıca modeller ve veri setleri için bir registry’e ihtiyaçları olduğuna düşündükleri için Hugging Face organizasyon hesabını açtılar. 

![huggingfacedepremml](https://user-images.githubusercontent.com/119361280/229272662-e36f7d7b-48fc-49d6-adfb-94f44d7abbef.png)

Bu platformda depremzedelerin paylaşımlarındaki ekran görüntülerinden OCR ile metinleri çekip ardından bu metinlerden açık kaynaklı kendi eğittikleri adres modelini kullanarak adresleri, isimleri ve telefon numaralarını (daha sonra anonim hale getirildi) içeren etiketli verileri veri tabanına aktardılar. İlk adres çıkarma modelini eğittiler ve daha sonra adresleri ayrıştırmak için “afetharita”da kullandılar.

Daha sonra her tweet’te birden fazla ihtiyaç (barınma, yiyecek, lojistik gibi) olduğu için bu verilerden depremzedelerin ihtiyaçlarını sınıflandırmak için niyet sınıflandırma modeli geliştirdiler.

Uzaktan algılama tarafında çalışan ekipler, arama kurtarma operasyonlarını yönlendirmek amacıyla altyapı ve binaların aldığı hasarı değerlendirmek için uzaktan algılama uygulamaları üzerinde çalıştılar fakat depremin ilk 48 saatinde elektriğin ve sabit mobil ağların olmaması, çöken yollarla birleştiğinde, hasarın boyutunun ve nerede yardıma ihtiyaç duyulduğunun değerlendirilmesini son derece zorlaştırdı.
 
 ![uzaktanalgılama](https://user-images.githubusercontent.com/119361280/229272721-4616541c-8238-4004-a88e-e2dce786d4d5.png)
 
Bu sorunları ele almak ve gelecekte kullanılabilecek açık kaynak araçları oluşturabilmek amacıyla aynı bölgeden toplanan deprem öncesi ve sonrası görüntülerdeki ayakta kalan bina sayılarını karşılaştırarak hasarın boyutunu değerlendirdiler. Bireysel gönüllülere ek olarak bazı şirketler, uydu verilerini, binalar ve altyapı için hasar yok, yıkıldı, hasarlı, hasarsız tesis gibi daha ayrıntılı açıklamalarla etiketlemek için gönüllü oldu. 
Eğittikleri modeller, kişisel veri içermeyen veri setleri ve uygulamaları şu an Hugging Face organizasyon hesabında bulunuyor. Gelecekte dünya çapındaki arama ve kurtarma operasyonlarını hızlandırabilecek kapsamlı bir açık kaynak veri seti yayınlamayı hedefliyorlar.
Geliştiricilerinden Merve Noyan ve Alara Dirik’in bu süreci kapsamlı bir şekilde anlattıkları [yazısını](https://merveenoyan.medium.com/a%C3%A7%C4%B1k-yaz%C4%B1l%C4%B1m-a%C4%9F%C4%B1nda-geli%C5%9Ftirdi%C4%9Fimi-makine-%C3%B6%C4%9Frenmesi-uygulamalar%C4%B1-dbbe10d7f736) okumanızı tavsiye ederim.

Arya Zeynep Mete

This work is licensed under the Creative Commons Atıf 4.0 Uluslararası License. To view a copy of this license, visit
http://creativecommons.org/licenses/by/4.0/.
