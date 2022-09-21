## Web Crawler

Amacı linkleri izlemek ve bilgi toplamak, linklerin izlenmesi ve yapının büyümesinden dolayı örümceklere benzetilir.

> Çalışma Mantığı
> 1. web sayfasını indir
> 2. sayfadaki bağlantıları çıkar
> 3. sayfadaki anahtar kelimeleri çıkar
> 4. kelime ve sayfa bilgisini indexer geçir
> 5. bulduğu bağlantılarla devam ederek bu işlemleri tekrar tekrar yapmak

Arama motorları web sayfalarına bot örümcek göndererek web crawler ile linkleri izleyip listeleyip indekslerken web scraping ise isteğe göre sayfadaki belirli bilgilerin toplanması ve işlenmesidir.

![](https://i.imgur.com/YYL3o05.png)

---

### Robots.txt
Arama motoru botlarının web sitemizin hangi bölümlerini ne şekilde tarayacağına dair yönlendirmeleri aktardığımız botların taramasına izin verip engelleme yaptığımız txt dosyasına verdiğimiz isimdir.Sitelerin ana domain dizininde barındırılır.Ancak bu dosyayı pas geçen bot dosyalarıda mevcuttur.Bu durumdan dolayı dosya yönlendirmelerine ek olarak sayfa source kodlarından meta robots işaretlemelerinin kullanılması önerilir.

### Nasıl Çalışır

Web sitesinin url uzantısı bölümüne /robots.txt yazılarak görüntülenebilir.Trendyol robots.txt dosyası örneği   https://www.trendyol.com/robots.txt

Bu dosya arama motoru botları için aslında bir rehberdir. Bağlayıcı bir yapı değildir diyebiliriz yani.Mesela zararlı botların çoğu bu dosyayı görmezden gelir ve serbest tarama gerçekleştirir. Asıl domainde oluşturduğumuz robots.txt dosyası sub domainler için geçerli değildir ayrı ayrı oluşturulması gerekir.

---

### Dosyanın oluşturulması ve kullanımı

Herhangibir text editörü ile oluşturulabiliriz. Arama motoru botlarının anlayabileceği direktifler için kullanılan protokol Robots Exclusion Protocol'dür. Robots.txt dosyaları için kullanılan bir diğer protokol sitemap protokolüdür. Sitemap site içerisinde yer alan urller ile alakalı site haritasını botlara iletir.

---

### User-Agent nedir, nasıl kullanılır ? 

Web üzerinde gezinen kullanıcı veya programlar için user-agent bilgisi vardır bu bilgi ile ilgili sunuculara ziyareti gerçekleştirilen kullanıcı veya program ile ilgili bilgi sağlanır. 

---

### Allow,Disallow Nedir, Nasıl Kullanılır ? 
Hangi sayfaların taramaya açılıp kapanacağını belirleyen protokollerdir.

---

### Özel Direktifler

#### * Direktifi
Tümü hepsi anlamına gelir
User-agent: *
Allow: *
Tüm user agentler için tüm sitenin taranabilir olduğu demektir.

#### $ Direktifi
Arama motoru botları ilgili işlemin belirtilen string ile sınırlı olduğunu anlayacaktır.

*Disallow*: *.webp$ -> ön eki ne olursa olsun yalnızca webp formatına sahip urllerin botlar tarafından taranması istediği bilgisini sağlarız

---

### Web Crawler Sınıflandırılması

**Deep crawling:** sayfanın ne kadar detayını dolaşıcam yani hangi bağlantıları takip edip etmeyeceğim

**Frame Support:** sayfalarda bulunan çerçeveleri destekleyip desteklemediğimiz.

**Meta Robot Tag:** Web sayfalarının üst bölümünde yer alan robot etiketinin desteklenip desteklenmeyeceği

**Fullbody text:** gezilen web sayfasında bütün dökümanın mı yoksa bir kısmının mı çıkarılacağı

**Stop Words:** gezilen sayfadaki arama için anlamsız olan çok yer kaplayan kelimelerin indekslenmemesi

**Meta Description:** html sayfalarının üst kısmında bulunan meta tanım bilgilerinin indexlenip indexlenmemesi

**Meta Keywords:** Html de bulunan anahtar kelimelerin indekslenip indekslenmemesi

**Focused Crawling :** Belirli bir hedefin bulunmasına yönelik geliştirilen crawling.Örneğin yazılımımız aranan bir kelimeye göre tarama yapacaksa veya belirli dosya türlerini dolaşıyorsa dolaşılan verileri indekslemek yerine sadece aranılan kelimeleri indeksleme

**Distrubted Crawling:** Bir tarama işleminin birden fazla bilgisayara bölünmesi durumu. ne gibi durumlarda tercih edilir emekleyiciler birbiriyle senkronize olup farklı kaynakları tararlarsa tutması gereken site ve kaynak azalacağı için depoloma ihtiyacı azalır, işlem yükü azalır.Senkronize çalışması için hashing fonksiyonlar kullanılabilir.

**Desktop Crawlers:** kişisel bilgisayarlarda bulunan dosyaları veya veri kaynaklarını dolaşan crawlerlar 

---

**Kullanılabilecek frameworklar;** Selenium , Requests , Scrapy...






