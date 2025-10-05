

---

### **Bölüm 1: What is Cloud Computing? (Bulut Bilişim Nedir?)**

#### **Traditional IT Overview (Geleneksel BT'ye Genel Bakış)**

*   **Nedir? (What?)**: Şirketlerin kendi sunucularını, depolama ünitelerini ve ağ altyapılarını kendi veri merkezlerinde (on-premise) satın alıp, kurup, yönettikleri modeldir.
*   **Neden Önemlidir? (Why?)**: Bulut bilişimin getirdiği avantajları anlamak için geleneksel modelin zorluklarını bilmek gerekir. Geleneksel BT, yüksek başlangıç maliyetleri (CapEx - Capital Expenditure), uzun tedarik süreleri, kapasite planlama zorlukları ve esnek olmama gibi dezavantajlara sahiptir.
*   **Nasıl Çalışır? (How?)**: Donanım satın alınır, fiziksel olarak kurulur, işletim sistemleri ve yazılımlar yüklenir ve tüm bakım, soğutma, elektrik gibi sorumluluklar şirkete ait olur.
*   **Sınav İpucu**: Sınavda "CapEx" (Sermaye Gideri) ve "OpEx" (Operasyonel Gider) karşılaştırması sıkça çıkar. Geleneksel BT **CapEx** ağırlıklıdır; bulut bilişim ise **OpEx** ağırlıklıdır. Yani, peşin para verip sunucu almak yerine, kullandığın kadar ödersin.

#### **What is Cloud Computing? (Bulut Bilişim Nedir?)**

*   **Nedir? (What?)**: Sunucu, depolama, veritabanı gibi BT kaynaklarının internet üzerinden, "kullandığın kadar öde" (pay-as-you-go) fiyatlandırmasıyla, talep üzerine (on-demand) sunulmasıdır.
*   **Neden Önemlidir? (Why?)**: AWS'in "6 Avantajı" olarak bilinen faydaları sağlar:
    1.  Sermaye giderini (CapEx) operasyonel gidere (OpEx) dönüştürme.
    2.  Büyük ölçekli ekonomilerden faydalanma (AWS'in alım gücü sayesinde maliyetler düşer).
    3.  Kapasite tahmin etme zorunluluğunu ortadan kaldırma.
    4.  Hız ve çevikliği artırma.
    5.  Veri merkezlerini yönetme maliyetinden kurtulma.
    6.  Dakikalar içinde küresel çapta yayılma (Go global in minutes).
*   **Sınav İpucu**: Bu 6 avantajı mutlaka ezberle. Özellikle "Trade CapEx for OpEx" ve "Go global in minutes" anahtar ifadelerdir.

#### **The Different Types of Cloud Computing (Bulut Bilişim Türleri)**

*   **Nedir? (What?)**: Üç ana hizmet modeli vardır:
    1.  **IaaS (Infrastructure as a Service)**: Temel altyapı (sanal sunucular, depolama, ağ) sağlanır. Yönetimin çoğu kullanıcıdadır. Örnek: Amazon EC2.
    2.  **PaaS (Platform as a Service)**: Kullanıcının uygulama geliştirmesi için gereken platform sağlanır. Alttaki altyapıyı AWS yönetir. Örnek: AWS Elastic Beanstalk.
    3.  **SaaS (Software as a Service)**: Kullanıma hazır yazılımlardır. Kullanıcı sadece yazılımı kullanır. Örnek: Gmail, Dropbox.
*   **Neden Önemlidir? (Why?)**: Farklı ihtiyaçlara farklı seviyelerde yönetim sorumluluğu sunar.
*   **Sınav İpucu**: Sınavda "Shared Responsibility Model" (Paylaşılan Sorumluluk Modeli) ile bu hizmet türleri ilişkilendirilir. IaaS'de sorumluluğun çoğu sizdeyken, SaaS'de neredeyse tamamı sağlayıcıdadır.

#### **AWS Cloud Overview (AWS Bulutuna Genel Bakış)**

*   **Nedir? (What?)**: AWS'in küresel altyapısını oluşturan temel yapı taşlarıdır.
*   **Nasıl Çalışır? (How?)**:
    *   **Regions (Bölgeler)**: Dünyanın farklı coğrafi konumlarındaki fiziksel yerlerdir (Örn: Frankfurt, İrlanda). Her Region, diğerlerinden tamamen izoledir.
    *   **Availability Zones (AZ - Kullanılabilirlik Alanları)**: Bir Region içindeki bir veya daha fazla veri merkezinden oluşan, birbirinden izole alanlardır. Bir AZ'de sorun olsa bile diğerleri çalışmaya devam eder. Yüksek erişilebilirlik (High Availability) için kritik öneme sahiptir.
    *   **Edge Locations (Uç Konumlar)**: Son kullanıcılara daha yakın noktalarda bulunan ve içeriği önbelleğe alarak (caching) gecikmeyi azaltan veri merkezleridir. Amazon CloudFront (CDN) ve Route 53 (DNS) servisleri tarafından kullanılır.
*   **Sınav İpucu**: Bir Region, en az üç AZ'den oluşur. Yüksek erişilebilirlik (High Availability) için uygulamalarınızı birden fazla AZ'ye dağıtmalısınız. Edge Location'ların amacı düşük gecikme (low latency) sağlamaktır.

#### **Shared Responsibility Model & AWS Acceptable Policy (Paylaşılan Sorumluluk Modeli ve AWS Kabul Edilebilir Politikası)**

*   **Nedir? (What?)**: Güvenlik ve uyumluluk sorumluluklarının AWS ile müşteri arasında nasıl paylaşıldığını tanımlayan modeldir.
*   **Nasıl Çalışır? (How?)**:
    *   **AWS'in Sorumluluğu (Security *OF* the Cloud)**: AWS, bulutun kendisinin güvenliğinden sorumludur. Bu, donanım, yazılım, ağ ve AWS servislerini çalıştıran küresel altyapıyı içerir.
    *   **Müşterinin Sorumluluğu (Security *IN* the Cloud)**: Müşteri, bulutun *içinde* ne yaptığıyla ilgili güvenlikten sorumludur. Bu, verilerin şifrelenmesi, kullanıcı erişim yönetimi (IAM), işletim sistemi güncellemeleri ve güvenlik duvarı (Security Group) yapılandırmalarını içerir.
*   **Sınav İpucu**: Bu, sınavın en önemli konularından biridir. "Müşteri verilerinin güvenliği kimin sorumluluğunda?" -> Müşteri. "EC2 sunucusuna yama (patch) yapmak kimin sorumluluğunda?" -> Müşteri. "Veri merkezinin fiziksel güvenliği kimin sorumluluğunda?" -> AWS. Veri merkezlerinin fiziksel erişimi, iklimlendirme, güç kaynağı ve yangın söndürme sistemleri, "Veri merkezinin kapılarını kilitlemek kimin işi?" → AWS. Region'lar, Availability Zone'lar (AZ'ler) ve Edge Location'ların (Uç Konumlar) donanım ve yazılımları, "Bir AZ'de bir sunucunun elektrik kesintisi yaşaması kime aittir?" → AWS. AWS tarafindan yönetilen Servisler, AWS'in temel servislerini çalıştırmak ve yamalamak. (Örnek: S3, DynamoDB). Sınav İpucu: S3'ün kendisinin (yani servisin kendisinin) yamalanması → AWS. (Encryption)	Müşteri	S3'e yüklenen verilerin şifrelenmesi (hem aktarım sırasında hem de beklerken), EBS volume şifrelemesi, "Hassas verileri korumak için S3 bucket politikası ayarlamak kimin sorumluluğundadır?" → Müşteri. Ağ Kontrolleri, Security Group'lar (Güvenlik Grupları) ve Ağ Erişim Kontrol Listeleri (NACL'ler) yapılandırmaları, "Bir EC2 sunucusuna SSH erişimini açmak/kapatmak?" → Müşteri. (IAM) Kullanıcılar, gruplar, roller ve bu kaynaklara tanınan izinler, "Şirket içi kullanıcının AWS konsoluna hangi izinlerle erişeceğini belirlemek?" → Müşteri. (OS) EC2 içindeki işletim sisteminin (Linux/Windows) yamalanması, güncellenmesi ve anti-virüs kurulumu, "EC2 içindeki Apache web sunucusuna yama yapmak?" → Müşteri.
Uygulama Güvenliği,	Müşterinin EC2'ye yüklediği uygulamanın içindeki güvenlik açıkları, loglama ve konfigürasyonlar, "Web sitemdeki SQL enjeksiyon açığını düzeltmek?" → Müşteri.

---

### **Bölüm 2: IAM - Identity and Access Management (Kimlik ve Erişim Yönetimi)**

#### **IAM Introduction: Users, Groups, Policies (IAM'e Giriş: Kullanıcılar, Gruplar, Politikalar)**

*   **Nedir? (What?)**: AWS kaynaklarına erişimi güvenli bir şekilde yönetmenizi sağlayan küresel bir servistir. Kimin (authentication) neye (authorization) erişebileceğini kontrol eder.
*   **Nasıl Çalışır? (How?)**:
    *   **Users (Kullanıcılar)**: AWS ile etkileşime giren kişiler veya uygulamalardır.
    *   **Groups (Gruplar)**: Kullanıcı koleksiyonlarıdır. Bir gruba izin atadığınızda, o gruptaki tüm kullanıcılar bu izinlere sahip olur. Yönetimi kolaylaştırır.
    *   **Policies (Politikalar)**: İzinleri tanımlayan JSON formatındaki belgelerdir. "Bu kullanıcı S3'te sadece okuma yapabilir" gibi kurallar içerir.
    *   **Roles (Roller)**: Belirli izinlere sahip, herhangi bir kullanıcı veya servis tarafından geçici olarak üstlenilebilen kimliklerdir. Uzun süreli şifreler (access keys) yerine kullanılması en iyi pratiktir.
*   **Sınav İpucu**: IAM **küreseldir** (global), yani bir Region'a özel değildir. **Root User** (hesabı ilk açan kullanıcı) ile günlük işler yapılmamalıdır. Her zaman **Principle of Least Privilege** (En Az Ayrıcalık Prensibi) uygulanmalıdır; yani bir kullanıcıya sadece işini yapması için gereken minimum izinler verilmelidir.

#### **IAM Policies (IAM Politikaları)**

*   **Nedir? (What?)**: Bir kimliğe (kullanıcı, grup, rol) veya kaynağa eklenen ve izinleri tanımlayan nesnelerdir.
*   **Neden Önemlidir? (Why?)**: AWS kaynakları üzerinde granüler (ayrıntılı) kontrol sağlar.
*   **Nasıl Çalışır? (How?)**: JSON formatında yazılırlar ve `Effect` (Allow/Deny), `Action` (izin verilen eylem, örn: `s3:GetObject`), `Resource` (eylemin uygulanacağı kaynak, örn: bir S3 bucket'ı) gibi elemanlar içerirler.
*   **Sınav İpucu**: Bir işlem için hem `Allow` hem de `Deny` politikası varsa, **`Deny` her zaman kazanır**.

#### **IAM MFA Overview (IAM MFA'ya Genel Bakış)**

*   **Nedir? (What?)**: Multi-Factor Authentication (Çok Faktörlü Kimlik Doğrulama). Kullanıcıların şifrelerine ek olarak, genellikle bir mobil uygulamadan (Google Authenticator gibi) aldıkları tek kullanımlık bir kodu girmelerini gerektiren bir güvenlik katmanıdır.
*   **Neden Önemlidir? (Why?)**: Şifreler çalınsa bile hesabınıza yetkisiz erişimi engeller.
*   **Sınav İpucu**: AWS, **Root User** ve tüm IAM kullanıcıları için MFA kullanılmasını şiddetle tavsiye eder. Bu bir güvenlik en iyi pratiğidir (best practice).

#### **AWS Access Keys, CLI and SDK (AWS Erişim Anahtarları, CLI ve SDK)**

*   **Nedir? (What?)**: AWS kaynaklarına programatik olarak (kod veya komut satırı üzerinden) erişmek için kullanılan araçlardır.
    *   **Access Keys**: Access Key ID ve Secret Access Key'den oluşan uzun süreli kimlik bilgileridir.
    *   **CLI (Command Line Interface)**: Komut satırından AWS servislerini yönetmek için bir araçtır.
    *   **SDK (Software Development Kit)**: Çeşitli programlama dilleri (Python, Java, .NET vb.) için AWS servislerini kod içinden kullanmayı sağlayan kütüphanelerdir.
*   **Neden Önemlidir? (Why?)**: Otomasyon ve uygulama entegrasyonu için gereklidir.
*   **Sınav İpucu**: Access Key'leri kodun içine doğrudan yazmak (hardcode) çok kötü bir pratiktir. Bunun yerine, özellikle EC2 gibi servislerde çalışacak uygulamalar için **IAM Roles** kullanılmalıdır.

#### **AWS CloudShell**

*   **Nedir? (What?)**: AWS konsolu üzerinden tek tıkla erişilebilen, tarayıcı tabanlı bir komut satırı arayüzüdür.
*   **Neden Önemlidir? (Why?)**: Kendi bilgisayarınıza CLI kurmadan veya kimlik bilgilerinizi yapılandırmadan hızlıca komut çalıştırmanızı sağlar.
*   **Nasıl Çalışır? (How?)**: Konsolda oturum açtığınız kullanıcı kimliğiyle otomatik olarak çalışır ve içinde AWS CLI gibi araçlar kurulu gelir.

#### **IAM Roles for AWS Services (AWS Servisleri için IAM Rolleri)**

*   **Nedir? (What?)**: Bir AWS servisinin (örn: EC2) başka bir AWS servisine (örn: S3) erişmesi gerektiğinde kullanılan güvenli bir yöntemdir.
*   **Neden Önemlidir? (Why?)**: EC2 sunucusuna Access Key koymak yerine, ona bir rol atayarak geçici ve güvenli kimlik bilgileri almasını sağlar. Bu, en iyi güvenlik pratiğidir.
*   **Sınav İpucu**: Sınavda "Bir EC2 instance'ının S3'e güvenli bir şekilde erişmesi için ne yapılmalıdır?" sorusunun cevabı her zaman **IAM Role**'dür.

#### **IAM Security Tools (IAM Güvenlik Araçları)**

*   **Nedir? (What?)**: IAM yapılandırmanızdaki güvenliği artırmak için kullanılan iki önemli araçtır:
    *   **IAM Credentials Report**: Hesabınızdaki tüm kullanıcıların bir listesini ve şifre, access key, MFA durumu gibi bilgilerini içeren bir rapordur.
    *   **IAM Access Advisor**: Bir kullanıcı veya rolün en son ne zaman hangi servislere eriştiğini gösterir. Kullanılmayan izinleri tespit edip kaldırmak için (least privilege) çok faydalıdır.
*   **Sınav İpucu**: Credentials Report hesap seviyesinde, Access Advisor ise kullanıcı/rol seviyesinde denetim sağlar.

#### **IAM Best Practices (IAM En İyi Pratikleri)**

*   **Nedir? (What?)**: IAM'i en güvenli ve etkili şekilde kullanmak için AWS tarafından önerilen kurallardır.
*   **Neden Önemlidir? (Why?)**: Güvenlik ihlallerini önler ve yönetimi kolaylaştırır.
*   **Nasıl Çalışır? (How?)**:
    1.  Root hesabınızı kilitleyin (sadece hesap yönetimi için kullanın, MFA ekleyin).
    2.  Bireysel IAM kullanıcıları oluşturun.
    3.  İzinleri yönetmek için gruplar kullanın.
    4.  En az ayrıcalık prensibini (least privilege) uygulayın.
    5.  Access Key'ler yerine IAM Rolleri'ni tercih edin.
    6.  Kullanıcılar için güçlü bir şifre politikası belirleyin.
    7.  Tüm kullanıcılarda MFA'yı etkinleştirin.
*   **Sınav İpucu**: Bu maddelerin hepsi sınavda soru olarak karşınıza çıkabilir. Özellikle "root user" ve "least privilege" konularına dikkat edin.

---

### **Bölüm 3: EC2 - Elastic Compute Cloud**

#### **AWS Budget Setup (AWS Bütçe Kurulumu)**

*   **Nedir? (What?)**: AWS maliyetlerinizi ve kullanımınızı takip etmek için özel bütçeler oluşturmanızı sağlayan bir araçtır.
*   **Neden Önemlidir? (Why?)**: Maliyetleriniz belirlediğiniz eşiği aştığında veya aşması beklendiğinde sizi uyararak sürpriz faturaları önler.
*   **Nasıl Çalışır? (How?)**: Belirli bir servis, etiket (tag) veya tüm hesap için aylık, üç aylık veya yıllık bütçeler tanımlayabilirsiniz. Bütçenin %85'ine ulaşıldığında e-posta ile uyar gibi alarmlar kurabilirsiniz.
*   **Sınav İpucu**: AWS Budgets sizi uyarır, ancak kaynakları **durdurmaz**.

#### **EC2 Basics (EC2 Temelleri)**

*   **Nedir? (What?)**: Amazon Elastic Compute Cloud (EC2), bulutta yeniden boyutlandırılabilir işlem kapasitesi (sanal sunucular) sağlayan bir web servisidir.
*   **Neden Önemlidir? (Why?)**: Geliştiricilere web ölçeğinde bilişim işlemlerini kolaylaştırır. İhtiyaca göre kapasiteyi artırıp azaltma (elasticity) imkanı sunar.
*   **Nasıl Çalışır? (How?)**: Kullanıcılar, Amazon Machine Image (AMI) adı verilen önceden yapılandırılmış şablonlardan sanal sunucular (instance) başlatır. Instance'ların işlemci, bellek, depolama gibi özelliklerini (instance type) seçebilirler.
*   **Sınav İpucu**: EC2, bir **IaaS** (Infrastructure as a Service) örneğidir.

#### **EC2 Instance Types Basics (EC2 Instance Türleri Temelleri)**

*   **Nedir? (What?)**: Farklı kullanım senaryoları için optimize edilmiş çeşitli EC2 instance aileleridir. (Örn: Genel Amaçlı - T ve M serisi, Hesaplama Optimize - C serisi, Bellek Optimize - R serisi).
*   **Neden Önemlidir? (Why?)**: İş yükünüze en uygun donanımı seçerek hem performans hem de maliyet optimizasyonu yapmanızı sağlar.
*   **Sınav İpucu**: Sınavda size bir senaryo verip (örn: "Yüksek performanslı bir veritabanı için hangi instance ailesi uygundur?"), doğru aileyi (Bellek Optimize - R) seçmeniz istenebilir.
*   Maliyet ve Esneklik (Küçük Web Sitesi, Dev/Test)	T (Burst)	General Purpose (Burstable)
Dengeli Performans (Orta Web Sunucusu, Uygulama Sunucusu)	M	General Purpose
Yüksek RAM İhtiyacı (Veritabanı, Önbellek)	R	Memory Optimized
Sürekli Yüksek CPU (Kodlama, Ağır Analiz)	C	Compute Optimized
Grafik/Makine Öğrenimi (GPU)	P / G	Accelerated Computing

#### **Security Groups & Classic Ports Overview (Güvenlik Grupları ve Klasik Portlara Genel Bakış)**

*   **Nedir? (What?)**: Security Group, bir EC2 instance'ı için sanal bir güvenlik duvarı (firewall) görevi görür ve gelen (inbound) ve giden (outbound) trafiği kontrol eder.
*   **Neden Önemlidir? (Why?)**: Instance'larınıza kimin, hangi port üzerinden erişebileceğini kontrol ederek temel ağ güvenliğini sağlar.
*   **Nasıl Çalışır? (How?)**: Belirli IP adreslerinden veya başka Security Group'lardan gelen trafiğe izin veren (Allow) kurallar tanımlanır. Örneğin, sadece 80 (HTTP) ve 443 (HTTPS) portlarından gelen trafiğe izin verebilirsiniz.
*   **Sınav İpucu**: Security Group'lar **stateful**'dur. Yani, bir gelen trafiğe izin verdiyseniz, o trafiğin geri dönüşüne (giden) otomatik olarak izin verilir. Varsayılan olarak tüm gelen trafiği reddeder, tüm giden trafiğe izin verir. **Deny kuralı yoktur**, sadece Allow kuralı ekleyebilirsiniz.

#### **SSH Overview (SSH'a Genel Bakış)**

*   **Nedir? (What?)**: Secure Shell (SSH), Linux ve macOS tabanlı EC2 instance'larına güvenli bir şekilde komut satırı üzerinden bağlanmak için kullanılan bir protokoldür.
*   **Neden Önemlidir? (Why?)**: Sunucuları uzaktan yönetmek için şifreli ve güvenli bir yol sağlar.
*   **Nasıl Çalışır? (How?)**: EC2 instance'ı oluşturulurken bir anahtar çifti (key pair) oluşturulur. Public key instance'da kalır, private key ise kullanıcı tarafından indirilir. Bağlantı bu private key kullanılarak yapılır.
*   **Sınav İpucu**: Windows sunucular için genellikle RDP (Remote Desktop Protocol) kullanılırken, Linux için SSH kullanılır. SSH, varsayılan olarak **22 numaralı portu** kullanır.

#### **EC2 Instance Connect**

*   **Nedir? (What?)**: Tarayıcı üzerinden EC2 instance'larınıza güvenli bir şekilde SSH bağlantısı yapmanızı sağlayan bir servistir.
*   **Neden Önemlidir? (Why?)**: SSH anahtarlarını yönetme veya kendi bilgisayarınızda bir SSH istemcisi bulundurma ihtiyacını ortadan kaldırır.

#### **EC2 Instance Purchasing Options (EC2 Satın Alma Seçenekleri)**

*   **Nedir? (What?)**: Farklı ihtiyaç ve bütçelere yönelik EC2 instance'ları için çeşitli fiyatlandırma modelleridir.
    1.  **On-Demand**: Kullandığın kadar öde. En esnek ama en pahalı model.
    2.  **Reserved Instances (RI)**: 1 veya 3 yıllık taahhüt karşılığında On-Demand'e göre ciddi indirim sağlar. Sürekli çalışacak sunucular için idealdir.
    3.  **Savings Plans**: 1 veya 3 yıllık belirli bir kullanım taahhüdü (örn: saatte $10) karşılığında indirim sağlar. RI'dan daha esnektir.
    4.  **Spot Instances**: AWS'in boşta kalan EC2 kapasitesini çok büyük indirimlerle (%90'a varan) sunduğu modeldir. Ancak AWS bu instance'ları 2 dakika önceden haber vererek geri alabilir. Kesintiye uğrayabilecek işler için uygundur.
    5.  **Dedicated Hosts**: Tamamen size adanmış fiziksel sunuculardır. Lisanslama veya uyumluluk gereksinimleri için kullanılır. En pahalı seçenektir.
*   **Sınav İpucu**: "Kesintiye uğrayabilecek, acil olmayan ve maliyetin çok önemli olduğu iş yükleri için en uygun seçenek hangisidir?" -> **Spot Instances**. "Sürekli çalışacak ve öngörülebilir bir iş yükü için en uygun maliyetli seçenek hangisidir?" -> **Reserved Instances** veya **Savings Plans**.

---

### **Bölüm 4: EC2 Instance Storage (EC2 Örnek Depolama)**

#### **EBS Overview (EBS'ye Genel Bakış)**

*   **Nedir? (What?)**: Amazon Elastic Block Store (EBS), EC2 instance'ları ile kullanılmak üzere tasarlanmış, kalıcı (persistent) ve yüksek performanslı blok depolama hizmetidir. Onu, buluttaki bir USB bellek veya harici hard disk gibi düşünebilirsin.
*   **Neden Önemlidir? (Why?)**: EBS, verilerinizi EC2 instance'ının ömründen bağımsız olarak saklamanızı sağlar. Yani, instance'ı durdursanız veya sonlandırsanız bile EBS volümündeki verileriniz kaybolmaz. Bu, veritabanları, dosya sistemleri ve uygulamalar için kritik öneme sahiptir.
*   **Nasıl Çalışır? (How?)**: Bir EBS volümü oluşturur ve onu belirli bir Availability Zone (AZ) içindeki bir EC2 instance'ına bağlarsınız. Farklı performans ihtiyaçları için farklı türleri vardır (gp3 - Genel Amaçlı SSD, io2 - Yüksek Performanslı SSD vb.).
*   **Sınav İpucu**: Anahtar kelimeler: **Persistent Block Storage** (Kalıcı Blok Depolama). Bir EBS volümü, oluşturulduğu **AZ'ye özgüdür** ve sadece aynı AZ'deki bir instance'a bağlanabilir.

#### **About EBS Multi-Attach (EBS Multi-Attach Hakkında)**

*   **Nedir? (What?)**: Belirli türdeki (Provisioned IOPS SSD - io1/io2) bir EBS volümünün, aynı Availability Zone içindeki birden fazla EC2 instance'ına aynı anda bağlanmasına olanak tanıyan bir özelliktir.
*   **Neden Önemlidir? (Why?)**: Yüksek erişilebilirlik gerektiren, kümelenmiş (clustered) uygulamaların paylaşılan depolamaya erişmesini sağlar.
*   **Sınav İpucu**: Bu, "bir EBS volümü sadece bir instance'a bağlanabilir" kuralının bir istisnasıdır. Sınavda "birden fazla instance'ın aynı block storage'a yazması gerekiyor" senaryosu geçerse, cevap **EBS Multi-Attach**'tir.

#### **EBS Snapshots Overview (EBS Anlık Görüntülerine Genel Bakış)**

*   **Nedir? (What?)**: Bir EBS volümünün belirli bir anlık yedeğidir (point-in-time backup).
*   **Neden Önemlidir? (Why?)**: Veri yedekleme ve felaket kurtarma (disaster recovery) için temel bir araçtır. Ayrıca, bir snapshot'tan yeni EBS volümleri oluşturabilir veya mevcut volümleri geri yükleyebilirsiniz.
*   **Nasıl Çalışır? (How?)**: İlk snapshot volümün tam bir kopyasıdır. Sonraki snapshot'lar ise **artımlıdır (incremental)**; yani sadece son snapshot'tan bu yana değişen veri bloklarını kaydeder. Bu, depolama maliyetlerinden tasarruf sağlar. Snapshot'lar arka planda Amazon S3'te saklanır.
*   **Sınav İpucu**: Snapshot'ların **artımlı** olduğunu unutmayın. Felaket kurtarma senaryoları için snapshot'ları farklı **Region'lara kopyalayabilirsiniz**.

#### **AMI Overview (AMI'ye Genel Bakış)**

*   **Nedir? (What?)**: Amazon Machine Image (AMI), bir EC2 instance'ı başlatmak için gereken bilgileri içeren bir şablondur. İçinde işletim sistemi, uygulamalar ve yapılandırmalar bulunur.
*   **Neden Önemlidir? (Why?)**: Aynı yapılandırmaya sahip birden fazla instance'ı hızlı ve tutarlı bir şekilde başlatmanızı sağlar. Kendi özel AMI'lerinizi oluşturarak yazılım kurulum sürecini otomatikleştirebilirsiniz.
*   **Nasıl Çalışır? (How?)**: Mevcut bir EC2 instance'ından bir AMI oluşturabilirsiniz. Bu işlem, instance'ın root EBS volümünün bir snapshot'ını almayı içerir.
*   **Sınav İpucu**: AMI'ler **Region'a özgüdür**. Bir AMI'yi başka bir Region'da kullanmak için önce o Region'a kopyalamanız gerekir.

#### **EC2 Image Builder Overview (EC2 Görüntü Oluşturucuya Genel Bakış)**

*   **Nedir? (What?)**: Güvenli ve güncel Linux ve Windows AMI'lerinin oluşturulmasını, bakımını ve dağıtımını otomatikleştiren bir servistir.
*   **Neden Önemlidir? (Why?)**: AMI'leri manuel olarak güncelleme ve yamama zahmetini ortadan kaldırır. Güvenlik standartlarına uygun imajlar oluşturmayı kolaylaştırır.
*   **Sınav İpucu**: Anahtar kelime: **Otomasyon**. "AMI oluşturma ve yamama sürecini otomatikleştirmek için hangi servis kullanılır?" sorusunun cevabı EC2 Image Builder'dır.

#### **EC2 Instance Store**

*   **Nedir? (What?)**: EC2 instance'ını barındıran fiziksel sunucuya doğrudan bağlı olan geçici (temporary) depolama alanıdır.
*   **Neden Önemlidir? (Why?)**: Fiziksel olarak bağlı olduğu için çok yüksek G/Ç (I/O) performansı ve düşük gecikme sunar. Önbellekler (caches), geçici dosyalar gibi veriler için idealdir.
*   **Nasıl Çalışır? (How?)**: Bazı instance türleri bu depolama seçeneğiyle birlikte gelir.
*   **Sınav İpucu**: En önemli özelliği **geçici (ephemeral/non-persistent)** olmasıdır. Eğer instance **durdurulur (stop)**, **sonlandırılır (terminate)** veya alttaki donanımda bir arıza olursa, Instance Store üzerindeki **tüm veriler silinir**. EBS ile en temel farkı budur.

#### **EFS Overview (EFS'ye Genel Bakış)**

*   **Nedir? (What?)**: Amazon Elastic File System (EFS), EC2 instance'ları için tasarlanmış, tam yönetilen, ölçeklenebilir bir paylaşılan dosya sistemidir (NFS gibi).
*   **Neden Önemlidir? (Why?)**: **Birden fazla EC2 instance'ının aynı anda aynı dosya sistemine erişmesine** olanak tanır. Dosya ekledikçe veya sildikçe kapasitesi otomatik olarak büyür ve küçülür.
*   **Nasıl Çalışır? (How?)**: Bir EFS dosya sistemi oluşturur ve bunu farklı AZ'lerdeki EC2 instance'larınıza "mount" edersiniz.
*   **Sınav İpucu**: Anahtar kelimeler: **Shared File Storage** (Paylaşılan Dosya Depolama), **NFS**. EFS, bir Region içindeki **birden fazla AZ'den** erişilebilir. "Birden fazla Linux sunucusunun ortak bir alana dosya yazması gerekiyor" senaryosunun cevabı EFS'dir.

#### **Amazon FSx Overview (Amazon FSx'e Genel Bakış)**

*   **Nedir? (What?)**: Popüler ticari ve açık kaynaklı dosya sistemlerini çalıştırmayı kolaylaştıran bir servistir.
*   **Neden Önemlidir? (Why?)**: EFS'in kapsamadığı özel ihtiyaçlara yönelik çözümler sunar.
*   **Nasıl Çalışır? (How?)**: İki ana türü vardır:
    *   **FSx for Windows File Server**: Tamamen yönetilen, yerel bir Microsoft Windows dosya sistemi sunar.
    *   **FSx for Lustre**: Yüksek performanslı bilgi işlem (HPC - High-Performance Computing) iş yükleri için optimize edilmiş, çok hızlı bir dosya sistemidir.
*   **Sınav İpucu**: Soruda **Windows** ve **paylaşılan dosya depolama** geçiyorsa cevap **FSx for Windows**'tur. Soruda **HPC** veya **yüksek performanslı analiz** geçiyorsa cevap **FSx for Lustre**'dır.

---

### **Bölüm 5: ELB & ASG - Elastic Load Balancing & Auto Scaling Groups**

#### **High Availability, Scalability, Elasticity (Yüksek Erişilebilirlik, Ölçeklenebilirlik, Esneklik)**

*   **Nedir? (What?)**: Bulut mimarisinin üç temel direğidir.
    *   **High Availability (Yüksek Erişilebilirlik)**: Bir sistemin, bileşenlerinden birinde arıza olsa bile çalışmaya devam etme yeteneğidir. AWS'de bu, kaynakları en az iki Availability Zone'a dağıtarak sağlanır.
    *   **Scalability (Ölçeklenebilirlik)**: Bir sistemin artan iş yükünü karşılama kapasitesidir. Dikey (Scale Up: daha güçlü bir sunucu) veya Yatay (Scale Out: daha fazla sunucu) olabilir.
    *   **Elasticity (Esneklik)**: Talebe göre kaynakları otomatik olarak artırma (scale out) *ve* azaltma (scale in) yeteneğidir.
*   **Sınav İpucu**: Yüksek Erişilebilirlik = **Multiple AZs**. Esneklik (Elasticity), sadece büyümek değil, aynı zamanda küçülerek maliyet tasarrufu sağlamaktır. Auto Scaling, esnekliğin en iyi örneğidir.

#### **Elastic Load Balancing (ELB) Overview (Elastik Yük Dengelemeye Genel Bakış)**

*   **Nedir? (What?)**: Gelen uygulama trafiğini, birden fazla Availability Zone'daki EC2 instance'ları gibi hedeflere otomatik olarak dağıtan bir servistir.
*   **Neden Önemlidir? (Why?)**: Uygulamanızın hata toleransını ve erişilebilirliğini artırır. Tek bir sunucuya olan bağımlılığı ortadan kaldırır ve kullanıcılara tek bir DNS adresi üzerinden hizmet verir.
*   **Nasıl Çalışır? (How?)**: Gelen istekleri dinler ve bu istekleri "health check" (sağlık kontrolü) ile sağlıklı olduğunu doğruladığı hedeflere yönlendirir.
*   **Sınav İpucu**: ELB, **Yüksek Erişilebilirlik** ve **Ölçeklenebilirlik** için kilit bir servistir.

#### **Application Load Balancer (ALB) (Uygulama Yük Dengeleyici)**

*   **Nedir? (What?)**: ELB'nin bir türüdür ve uygulama katmanında (Layer 7) çalışır. HTTP ve HTTPS trafiğini dengelemek için idealdir.
*   **Neden Önemlidir? (Why?)**: "Akıllı" bir yük dengeleyicidir. Gelen isteğin içeriğine (URL yolu, host adı vb.) göre yönlendirme kararları verebilir. Bu, mikroservis mimarileri için çok kullanışlıdır.
*   **Nasıl Çalışır? (How?)**: Örneğin, `site.com/images` adresine gelen istekleri resim sunucularına, `site.com/api` adresine gelenleri ise uygulama sunucularına yönlendirebilir.
*   **Sınav İpucu**: Soruda **URL path-based routing** (URL yoluna göre yönlendirme) veya **host-based routing** (host adına göre yönlendirme) ifadeleri geçiyorsa, cevap **Application Load Balancer (ALB)**'dir.

#### **Auto Scaling Groups (ASG) Overview (Otomatik Ölçeklendirme Gruplarına Genel Bakış)**

*   **Nedir? (What?)**: Uygulamanızın iş yükünü karşılamak için doğru sayıda EC2 instance'ına sahip olmanızı sağlayan bir servistir.
*   **Neden Önemlidir? (Why?)**: **Esneklik (Elasticity)** sağlar. Talep arttığında otomatik olarak yeni instance'lar ekler (scale out), talep azaldığında ise instance'ları kaldırır (scale in). Bu sayede hem performansı optimize eder hem de gereksiz maliyetleri önler. Ayrıca, arızalanan bir instance'ı otomatik olarak yenisiyle değiştirerek hata toleransını artırır.
*   **Nasıl Çalışır? (How?)**: Bir `Launch Template` (ne tür bir instance başlatılacağını tanımlar) ve bir `Auto Scaling Group` (minimum, maksimum ve istenen instance sayısını belirtir) tanımlarsınız.
*   **Sınav İpucu**: ASG ve ELB birlikte mükemmel çalışır. ASG instance sayısını ayarlar, ELB ise gelen trafiği bu instance'lara dağıtır.

#### **Auto Scaling Groups (ASG) Strategies (Otomatik Ölçeklendirme Grubu Stratejileri)**

*   **Nedir? (What?)**: Ölçeklendirme eylemlerini tetikleme yöntemleridir.
    *   **Dynamic Scaling**: Değişen talebe göre otomatik ölçeklendirme. Genellikle CloudWatch metriklerine (örn: CPU kullanımı) dayanır.
    *   **Target Tracking Scaling**: En basit dinamik ölçeklendirme türü. "Tüm grubun ortalama CPU kullanımını %60'ta tut" gibi bir hedef belirlersiniz.
    *   **Scheduled Scaling**: Belirli zamanlarda ölçeklendirme. Örneğin, "her Cuma akşamı sunucu sayısını azalt".
    *   **Predictive Scaling**: Gelecekteki trafiği tahmin etmek için makine öğrenimini kullanır ve kaynakları önceden hazırlar.
*   **Sınav İpucu**: Gerçek esnekliği sağlayan en yaygın yöntem **Dynamic Scaling**'dir.

---

### **Bölüm 6: Amazon S3**

#### **S3 Overview (S3'e Genel Bakış)**

*   **Nedir? (What?)**: Amazon Simple Storage Service (S3), internet için oluşturulmuş bir **nesne depolama (object storage)** hizmetidir. Neredeyse sınırsız miktarda veriyi saklamak için tasarlanmıştır. Onu internetin hard diski gibi düşünebilirsin.
*   **Neden Önemlidir? (Why?)**: İnanılmaz derecede dayanıklı ve ölçeklenebilirdir. AWS, S3 için **%99.999999999 (11 tane 9) dayanıklılık (durability)** garantisi verir, bu da verilerinizin neredeyse hiç kaybolmayacağı anlamına gelir. Web siteleri, mobil uygulamalar, yedekleme, arşivleme ve büyük veri analizi gibi çok çeşitli senaryolarda kullanılır.
*   **Nasıl Çalışır? (How?)**: Veriler, **Bucket (Kova)** adı verilen konteynerlerde saklanır. Her bucket'ın adı tüm AWS genelinde **benzersiz (globally unique)** olmalıdır. Bucket'ların içine koyduğunuz dosyalara ise **Object (Nesne)** denir. Her nesne bir dosya (key) ve onun içeriğinden (value) oluşur.
*   **Sınav İpucu**: S3'ün **Object Storage** olduğunu, EBS'nin ise **Block Storage** olduğunu unutma. Sınavda "11 nines of durability" ifadesini görürseniz, bu kesinlikle S3 ile ilgilidir. Bucket isimlerinin küresel olarak benzersiz olması da önemli bir detaydır.

#### **S3 Security: Bucket Policy (S3 Güvenliği: Kova Politikası)**

*   **Nedir? (What?)**: Doğrudan bir S3 bucket'ına eklenen ve o bucket'taki nesnelere kimin, hangi koşullarda erişebileceğini tanımlayan JSON formatında bir izin belgesidir.
*   **Neden Önemlidir? (Why?)**: Verilerinize granüler (ayrıntılı) erişim kontrolü sağlar. Örneğin, belirli bir IP adresinden gelen isteklere izin verebilir veya başka bir AWS hesabının sizin bucket'ınıza dosya yüklemesini sağlayabilirsiniz.
*   **Sınav İpucu**: Varsayılan olarak, oluşturulan **tüm S3 bucket'ları ve içindeki nesneler özeldir (private)**. Onlara erişimi açmak için bilinçli olarak Bucket Policy veya ACL (Access Control List) gibi mekanizmaları kullanmanız gerekir.

#### **S3 Website Overview (S3 Web Sitesine Genel Bakış)**

*   **Nedir? (What?)**: S3'ün, sunucu yönetimi gerektirmeyen **statik web sitelerini** (HTML, CSS, JavaScript dosyalarından oluşan) barındırma yeteneğidir.
*   **Neden Önemlidir? (Why?)**: Son derece düşük maliyetli, yüksek erişilebilir ve ölçeklenebilir bir web sitesi barındırma çözümü sunar. Sunucu kurma, güncelleme gibi dertleriniz olmaz.
*   **Sınav İpucu**: Anahtar kelime: **Statik Web Sitesi**. Sınavda size PHP, .NET gibi sunucu taraflı kodlama gerektiren dinamik bir site sorulursa, S3 doğru cevap değildir. Sadece statik içerik için kullanılır.

#### **S3 Versioning Overview (S3 Sürümlemeye Genel Bakış)**

*   **Nedir? (What?)**: Bir bucket içinde aynı nesnenin tüm sürümlerini korumanızı sağlayan bir özelliktir. Bir nesneyi her değiştirdiğinizde, S3 eski sürümü silmek yerine yeni bir sürüm olarak kaydeder.
*   **Neden Önemlidir? (Why?)**: Nesnelerin yanlışlıkla silinmesine veya üzerine yazılmasına karşı güçlü bir koruma sağlar. Silinen bir nesneyi kolayca geri getirmenize olanak tanır.
*   **Nasıl Çalışır? (How?)**: Bucket seviyesinde etkinleştirilir. Bir nesneyi sildiğinizde, S3 aslında onu kalıcı olarak silmez, üzerine bir "silme işareti" (delete marker) koyar. Bu sayede nesnenin önceki sürümüne hala erişilebilir.
*   **Sınav İpucu**: Sürümleme (Versioning) etkinleştirildikten sonra **devre dışı bırakılamaz**, sadece **askıya alınabilir (suspended)**.

#### **S3 Replication Overview (S3 Replikasyonuna Genel Bakış)**

*   **Nedir? (What?)**: Nesneleri bir kaynak S3 bucket'ından bir veya daha fazla hedef bucket'a otomatik olarak kopyalama işlemidir.
*   **Neden Önemlidir? (Why?)**: Felaket kurtarma (disaster recovery), uyumluluk gereksinimleri ve farklı coğrafi konumlardaki kullanıcılara daha düşük gecikme süresiyle veri sunmak için kullanılır.
*   **Nasıl Çalışır? (How?)**: İki türü vardır:
    *   **CRR (Cross-Region Replication)**: Nesneleri farklı bir AWS Region'ındaki bir bucket'a kopyalar.
    *   **SRR (Same-Region Replication)**: Nesneleri aynı AWS Region'ındaki bir bucket'a kopyalar.
*   **Sınav İpucu**: Replikasyonun çalışabilmesi için kaynak ve hedef bucket'larda **Versioning'in etkinleştirilmiş olması zorunludur**.

#### **S3 Storage Classes Overview (S3 Depolama Sınıflarına Genel Bakış)**

*   **Nedir? (What?)**: Farklı erişim sıklığı ve maliyet gereksinimleri için tasarlanmış çeşitli depolama katmanlarıdır.
*   **Neden Önemlidir? (Why?)**: Verilerinizi kullanım amacına en uygun ve en uygun maliyetli katmanda saklayarak ciddi tasarruf yapmanızı sağlar.
*   **Nasıl Çalışır? (How?)**: Başlıca sınıflar:
    *   **S3 Standard**: Sık erişilen veriler için varsayılan sınıf. En düşük gecikme, en yüksek performans.
    *   **S3 Intelligent-Tiering**: Erişim desenleri bilinmeyen veya değişken olan veriler için idealdir. Verileri otomatik olarak sık ve seyrek erişim katmanları arasında taşıyarak maliyeti optimize eder.
    *   **S3 Standard-IA (Infrequent Access)**: Seyrek erişilen ancak ihtiyaç duyulduğunda hızlıca erişilmesi gereken veriler için (örn: yedekler). Depolama maliyeti daha düşük, ancak veri çekme ücreti vardır.
    *   **S3 One Zone-IA**: Standard-IA ile aynıdır, ancak verileri tek bir Availability Zone'da saklar. Bu nedenle daha ucuzdur ama AZ'nin başına bir şey gelirse veri kaybolabilir. Yeniden oluşturulabilir veriler için uygundur.
    *   **S3 Glacier Instant Retrieval**: Arşivlenen verilere milisaniyeler içinde erişim gerektiren durumlar için.
    *   **S3 Glacier Flexible Retrieval**: Uzun süreli arşivleme için. Veri çekme işlemi dakikalar veya saatler sürebilir.
    *   **S3 Glacier Deep Archive**: En ucuz depolama sınıfı. Veri çekme işlemi 12 saat veya daha uzun sürebilir.
*   **Sınav İpucu**: Bu konu sınavın en önemli kısımlarından biridir. "Erişim deseni bilinmiyor" -> **Intelligent-Tiering**. "Yeniden oluşturulabilir, seyrek erişilen veri" -> **One Zone-IA**. "En ucuz arşiv" -> **Glacier Deep Archive**. Bu sınıflar arasında otomatik geçiş yapmak için **S3 Lifecycle Policies** kullanılır.

#### **S3 Express One Zone**

*   **Nedir? (What?)**: En yüksek performansı ve en düşük gecikmeyi sunan yeni bir S3 depolama sınıfıdır.
*   **Neden Önemlidir? (Why?)**: Özellikle makine öğrenmesi eğitimi veya finansal modelleme gibi tek haneli milisaniye gecikme gerektiren, performansa duyarlı uygulamalar için tasarlanmıştır.
*   **Sınav İpucu**: Anahtar kelime: **single-digit millisecond latency**. En hızlı S3 seçeneğidir.

#### **S3 Encryption (S3 Şifreleme)**

*   **Nedir? (What?)**: S3'te depolanan verilerinizi (data at rest) korumak için kullanılan şifreleme yöntemleridir.
*   **Nasıl Çalışır? (How?)**:
    *   **Server-Side Encryption (SSE - Sunucu Tarafı Şifreleme)**: Veri S3'e yazılırken AWS tarafından şifrelenir.
        *   **SSE-S3**: AWS'in kendi yönettiği anahtarlarla şifreleme. En basit yöntem.
        *   **SSE-KMS**: AWS Key Management Service (KMS) ile yönetilen anahtarlarla şifreleme. Anahtar kullanımı üzerinde daha fazla kontrol ve denetim kaydı sağlar.
        *   **SSE-C**: Müşterinin kendi şifreleme anahtarlarını sağladığı model.
    *   **Client-Side Encryption (İstemci Tarafı Şifreleme)**: Veriyi S3'e göndermeden *önce* kendi tarafınızda şifrelersiniz.
*   **Sınav İpucu**: Verilerin S3'e giderken korunması (in transit) için **SSL/TLS (HTTPS)** kullanılır. Verilerin S3'te dururken korunması (at rest) için ise SSE veya istemci tarafı şifreleme kullanılır.

#### **AWS Snow Family Overview (AWS Snow Ailesine Genel Bakış)**

*   **Nedir? (What?)**: Çok büyük miktardaki verileri (terabaytlarca, petabaytlarca) AWS'e taşımak veya AWS'ten çıkarmak için kullanılan fiziksel cihazlardır. İnternet bağlantısının yavaş veya pahalı olduğu durumlar için idealdir.
*   **Nasıl Çalışır? (How?)**:
    *   **AWS Snowcone**: En küçük, taşınabilir cihaz (yaklaşık 8-14 TB).
    *   **AWS Snowball Edge**: Daha büyük kapasiteli (yaklaşık 80 TB) ve üzerinde işlem yapma (compute) yeteneği de olan bir cihaz.
    *   **AWS Snowmobile**: Exabyte ölçeğindeki verileri taşımak için kullanılan, tır büyüklüğünde bir mobil veri merkezi.
*   **Sınav İpucu**: Soruda **petabyte (PB)** veya **terabyte (TB)** ölçeğinde veri transferi ve yavaş ağ bağlantısından bahsediliyorsa, cevap kesinlikle **Snow Family** üyelerinden biridir.

#### **Storage Gateway Overview (Depolama Ağ Geçidine Genel Bakış)**

*   **Nedir? (What?)**: Şirket içi (on-premises) uygulamalarınızı AWS bulut depolama hizmetlerine sorunsuz bir şekilde bağlayan bir **hibrit bulut** depolama hizmetidir.
*   **Neden Önemlidir? (Why?)**: Şirket içindeki mevcut altyapınızı değiştirmeden bulutun neredeyse sınırsız depolama kapasitesinden faydalanmanızı sağlar.
*   **Nasıl Çalışır? (How?)**: Üç ana türü vardır:
    *   **File Gateway**: S3 bucket'larınızı şirket ağınızda bir dosya paylaşımı (NFS veya SMB) olarak gösterir.
    *   **Volume Gateway**: Bulut tabanlı depolamayı şirket içi sunucularınıza iSCSI blok depolama birimleri (EBS gibi) olarak sunar.
    *   **Tape Gateway**: Fiziksel teyp yedekleme altyapınızı, S3 ve Glacier tarafından desteklenen sanal bir teyp kütüphanesiyle değiştirir.
*   **Sınav İpucu**: Anahtar kelime: **Hibrit**. "On-premises uygulamaları AWS depolama ile entegre etme" senaryosunun cevabı **Storage Gateway**'dir.

---

### **Bölüm 7: Databases & Analytics (Veritabanları ve Analitik)**

#### **Databases Introduction (Veritabanlarına Giriş)**

*   **Nedir? (What?)**: AWS, farklı veri modelleri ve ihtiyaçlar için geniş bir veritabanı portföyü sunar. Bunlar temel olarak ikiye ayrılır:
    *   **Relational (SQL)**: Geleneksel, tablo tabanlı veritabanlarıdır. Veriler satır ve sütunlardan oluşur ve aralarında önceden tanımlanmış ilişkiler vardır. Örnek: MySQL, PostgreSQL, Oracle.
    *   **Non-Relational (NoSQL)**: Esnek veri modellerine sahiptir. Tablo yapısı zorunlu değildir. Büyük ölçekli, yüksek performanslı ve esnek uygulamalar için idealdir. Örnekler: Key-Value, Document, Graph, In-Memory.
*   **Sınav İpucu**: Hangi veritabanı türünün hangi senaryoya uygun olduğunu bilmek kritiktir. Örneğin, karmaşık sorgular ve raporlama için SQL; esnek şema ve yatay ölçeklenebilirlik için NoSQL tercih edilir.

#### **RDS & Aurora Overview (RDS ve Aurora'ya Genel Bakış)**

*   **Nedir? (What?)**:
    *   **Amazon RDS (Relational Database Service)**: Bulutta ilişkisel veritabanları kurmayı, işletmeyi ve ölçeklendirmeyi kolaylaştıran yönetilen bir hizmettir. MySQL, PostgreSQL, MariaDB, Oracle ve SQL Server gibi popüler veritabanı motorlarını destekler.
    *   **Amazon Aurora**: AWS tarafından geliştirilmiş, MySQL ve PostgreSQL ile uyumlu, bulut için optimize edilmiş, yüksek performanslı bir ilişkisel veritabanıdır.
*   **Neden Önemlidir? (Why?)**: RDS, veritabanı yönetimiyle ilgili zaman alıcı görevleri (yedekleme, yazılım yamalama, donanım sağlama) otomatikleştirir, böylece siz uygulamanıza odaklanabilirsiniz. Aurora ise standart MySQL'den 5 kat, standart PostgreSQL'den 3 kat daha fazla performans sunduğunu iddia eder ve ticari veritabanlarının performansını açık kaynak maliyetleriyle sunar.
*   **Nasıl Çalışır? (How?)**: RDS, **Multi-AZ** dağıtımı ile yüksek erişilebilirlik (High Availability) sağlar. Birincil veritabanında bir sorun olursa, otomatik olarak başka bir AZ'deki yedek (standby) veritabanına geçiş (failover) yapar. **Read Replicas (Okuma Replikaları)** ise okuma yoğunluklu iş yüklerini ana veritabanından alarak performansı artırmak için kullanılır.
*   **Sınav İpucu**: "Yüksek erişilebilirlik" ve "otomatik failover" için **Multi-AZ**. "Okuma performansını artırmak" için **Read Replicas**. Aurora, AWS'in kendi optimize ettiği, en performanslı ilişkisel veritabanı seçeneğidir.

#### **ElastiCache Overview (ElastiCache'e Genel Bakış)**

*   **Nedir? (What?)**: Popüler açık kaynaklı bellek içi (in-memory) veri depoları olan **Redis** ve **Memcached**'i bulutta kurmayı ve yönetmeyi kolaylaştıran bir hizmettir.
*   **Neden Önemlidir? (Why?)**: Veritabanlarından veya API'lerden sıkça istenen verileri bellekte (RAM) önbelleğe alarak (caching) uygulama performansını önemli ölçüde artırır ve gecikmeyi azaltır.
*   **Nasıl Çalışır? (How?)**: Uygulama bir veriye ihtiyaç duyduğunda önce ElastiCache'e bakar. Veri oradaysa (cache hit), çok hızlı bir şekilde alır. Orada değilse (cache miss), veritabanına gider, veriyi alır ve bir kopyasını da ElastiCache'e koyar ki bir sonraki istek hızlı olsun.
*   **Sınav İpucu**: Anahtar kelimeler: **Caching**, **In-Memory**, **Low Latency**. "Veritabanı yükünü azaltmak ve uygulama yanıt süresini iyileştirmek için hangi servis kullanılır?" sorusunun cevabı **ElastiCache**'tir.

#### **DynamoDB Overview (DynamoDB'ye Genel Bakş)**

*   **Nedir? (What?)**: AWS'in tam yönetilen, sunucusuz (serverless), **NoSQL Key-Value ve Document** veritabanı hizmetidir.
*   **Neden Önemlidir? (Why?)**: Neredeyse her ölçekte tek haneli milisaniye (single-digit millisecond) performans sunar. Otomatik olarak ölçeklenir, yani kapasite planlaması yapmanıza gerek kalmaz. Mobil, web, oyun ve IoT gibi yüksek trafikli uygulamalar için mükemmeldir.
*   **Nasıl Çalışır? (How?)**: Veriler, birincil anahtar (primary key) ile erişilen öğelerden (items) oluşan tablolarda (tables) saklanır.
*   **Sınav İpucu**: Anahtar kelimeler: **NoSQL**, **Serverless**, **Fully Managed**, **Single-digit millisecond latency**. DynamoDB, verileri otomatik olarak **birden fazla AZ'ye** yayarak yüksek erişilebilirlik sağlar.

#### **Redshift Overview (Redshift'e Genel Bakış)**

*   **Nedir? (What?)**: Tam yönetilen, petabayt ölçeğinde bir **veri ambarı (data warehouse)** hizmetidir.
*   **Neden Önemlidir? (Why?)**: Büyük miktardaki yapılandırılmış veriler üzerinde karmaşık analitik sorgular çalıştırmak için optimize edilmiştir. İş zekası (Business Intelligence - BI) ve raporlama araçlarıyla entegre çalışır.
*   **Nasıl Çalışır? (How?)**: Sütun tabanlı (columnar) depolama ve paralel işleme teknolojilerini kullanarak sorgu performansını en üst düzeye çıkarır.
*   **Sınav İpucu**: Anahtar kelimeler: **Data Warehousing**, **Business Intelligence (BI)**, **Analytics**. Geleneksel veritabanları (OLTP) işlem odaklıyken, Redshift (OLAP) analiz odaklıdır.

#### **EMR Overview (EMR'ye Genel Bakış)**

*   **Nedir? (What?)**: Amazon EMR (Elastic MapReduce), Apache Spark, Hadoop, Hive ve Presto gibi büyük veri (big data) çerçevelerini kullanarak büyük miktarda veriyi işlemeyi ve analiz etmeyi kolaylaştıran bir bulut platformudur.
*   **Neden Önemlidir? (Why?)**: Büyük veri kümelerinin işlenmesi için gereken altyapıyı hızlı bir şekilde kurmanızı ve yönetmenizi sağlar.
*   **Sınav İpucu**: Anahtar kelimeler: **Big Data**, **Hadoop**, **Spark**.

#### **Athena Overview (Athena'ya Genel Bakış)**

*   **Nedir? (What?)**: Amazon S3'teki verileri doğrudan standart SQL kullanarak analiz etmeyi kolaylaştıran **etkileşimli bir sorgu hizmetidir**.
*   **Neden Önemlidir? (Why?)**: **Sunucusuzdur (Serverless)**. Altyapı yönetimi gerektirmez ve yalnızca çalıştırdığınız sorgular için ödeme yaparsınız. Verileri S3'ten başka bir yere yüklemenize gerek kalmaz.
*   **Sınav İpucu**: Anahtar kelimeler: **Serverless**, **Query data in S3**, **Standard SQL**. "S3'teki log dosyalarını SQL ile hızlıca analiz etmek için hangi servis kullanılır?" sorusunun cevabı **Athena**'dır.

#### **QuickSight Overview (QuickSight'a Genel Bakış)**

*   **Nedir? (What?)**: AWS'in bulut tabanlı, sunucusuz **İş Zekası (Business Intelligence - BI)** hizmetidir.
*   **Neden Önemlidir? (Why?)**: Verilerinizi kolayca görselleştirmenize, etkileşimli panolar (dashboards) oluşturmanıza ve bu panoları kuruluşunuzdaki diğer kişilerle paylaşmanıza olanak tanır.
*   **Sınav İpucu**: Anahtar kelimeler: **BI**, **Dashboards**, **Visualization**.

#### **DocumentDB Overview (DocumentDB'ye Genel Bakış)**

*   **Nedir? (What?)**: **MongoDB ile uyumlu**, hızlı, ölçeklenebilir ve tam yönetilen bir **belge (document)** veritabanı hizmetidir.
*   **Neden Önemlidir? (Why?)**: MongoDB iş yüklerini AWS'e kolayca taşımak ve bulutun avantajlarından faydalanmak isteyenler için tasarlanmıştır.
*   **Sınav İpucu**: Soruda **MongoDB** ve **document database** geçiyorsa, cevap **DocumentDB**'dir.

#### **Neptune Overview (Neptune'a Genel Bakış)**

*   **Nedir? (What?)**: Tam yönetilen bir **graf (graph)** veritabanı hizmetidir.
*   **Neden Önemlidir? (Why?)**: Sosyal ağlar, öneri motorları ve dolandırıcılık tespiti gibi yüksek düzeyde bağlantılı veri kümeleriyle çalışan uygulamalar oluşturmak için optimize edilmiştir.
*   **Sınav İpucu**: Anahtar kelimeler: **Graph Database**, **Social Networking**, **Recommendation Engines**.

#### **Managed Blockchain Overview (Yönetilen Blockchain'e Genel Bakış)**

*   **Nedir? (What?)**: Hyperledger Fabric ve Ethereum gibi popüler açık kaynak çerçevelerini kullanarak ölçeklenebilir blockchain ağları oluşturmayı ve yönetmeyi kolaylaştıran tam yönetilen bir hizmettir.
*   **Sınav İpucu**: Soruda **Blockchain** veya **Ledger** geçiyorsa, bu servisi aklınıza getirin.

#### **Glue Overview (Glue'ye Genel Bakış)**

*   **Nedir? (What?)**: Analitik için verileri keşfetmeyi, hazırlamayı ve birleştirmeyi kolaylaştıran tam yönetilen bir **ETL (Extract, Transform, Load - Ayıkla, Dönüştür, Yükle)** hizmetidir.
*   **Neden Önemlidir? (Why?)**: Farklı kaynaklardan (örn: S3, RDS) veri alıp, bunları analiz için uygun bir formata dönüştürüp, hedef veri deposuna (örn: Redshift) yükleme sürecini otomatikleştirir.
*   **Sınav İpucu**: Anahtar kelime: **ETL**. Glue Data Catalog, verilerinizin meta verilerini (şema, veri türleri vb.) depolayan merkezi bir depodur.

#### **DMS Overview (DMS'ye Genel Bakış)**

*   **Nedir? (What?)**: Amazon Database Migration Service (DMS), veritabanlarını AWS'e hızlı ve güvenli bir şekilde taşımanıza yardımcı olan bir hizmettir.
*   **Neden Önemlidir? (Why?)**: Taşıma sırasında kaynak veritabanı tamamen çalışır durumda kalır, bu da kesinti süresini en aza indirir. Oracle'dan Aurora'ya gibi farklı veritabanı motorları arasında (heterojen) geçiş yapmayı da destekler.
*   **Sınav İpucu**: Anahtar kelime: **Database Migration**. "Şirket içi Oracle veritabanını minimum kesintiyle AWS Aurora'ya taşımak için hangi servis kullanılır?" sorusunun cevabı **DMS**'dir.

---

### **Bölüm 8: Other Compute Services (Diğer Bilişim Servisleri)**

#### **What is Docker? (Docker Nedir?)**

*   **Nedir? (What?)**: Docker, uygulamaları ve bağımlılıklarını **konteyner (container)** adı verilen hafif, taşınabilir ve kendi kendine yeten birimler halinde paketlemeyi sağlayan bir platformdur.
*   **Neden Önemlidir? (Why?)**: "Benim bilgisayarımda çalışıyordu" sorununu çözer. Bir konteyner, içinde çalışan uygulama için gereken her şeyi (kod, kütüphaneler, ayarlar) barındırır. Bu sayede, geliştirme ortamından test ortamına ve oradan da production'a geçerken tutarlılık sağlar. Sanal makinelere (VM) göre çok daha hızlı başlarlar ve daha az kaynak tüketirler.
*   **Sınav İpucu**: Docker, AWS'in bir servisi değildir, ancak AWS'in ECS ve EKS gibi konteyner servislerinin temelini oluşturan teknolojidir. Anahtar kelimeler: **Container**, **Portability**, **Consistency**.

#### **ECS, Fargate & ECR Overview (ECS, Fargate ve ECR'ye Genel Bakış)**

*   **Nedir? (What?)**: AWS'in konteyner yönetimi (orchestration) ekosistemidir.
    *   **Amazon ECS (Elastic Container Service)**: AWS'in kendi geliştirdiği, Docker konteynerlerini çalıştırmak, durdurmak ve yönetmek için kullanılan yüksek performanslı bir konteyner orkestrasyon hizmetidir.
    *   **Amazon ECR (Elastic Container Registry)**: Docker konteyner imajlarınızı depolamak, yönetmek ve dağıtmak için kullanılan tam yönetilen bir Docker kayıt defteri hizmetidir. Docker Hub'ın AWS'teki karşılığıdır.
    *   **AWS Fargate**: ECS ve EKS için **sunucusuz (serverless)** bir işlem motorudur. Fargate ile, konteynerlerinizi çalıştırmak için alttaki EC2 instance'larını yönetmenize gerek kalmaz. Sadece konteynerinizi tanımlarsınız ve Fargate onu çalıştırır.
*   **Neden Önemlidir? (Why?)**: Bu servisler, konteyner tabanlı uygulamaları AWS üzerinde kolayca ve ölçeklenebilir bir şekilde çalıştırmanızı sağlar. Fargate, altyapı yönetim yükünü tamamen ortadan kaldırarak en basit konteyner çalıştırma deneyimini sunar.
*   **Sınav İpucu**: "Konteyner imajlarını nerede saklarım?" -> **ECR**. "Konteynerleri orkestre etmek için AWS'in kendi servisi nedir?" -> **ECS**. "EC2 sunucularını yönetmeden konteyner çalıştırmak istiyorum" -> **Fargate**. Fargate, sunucusuz konteyner çalıştırma modelidir.

#### **Amazon EKS (Elastic Kubernetes Service)**

*   **Nedir? (What?)**: AWS üzerinde **Kubernetes**'i çalıştırmayı kolaylaştıran yönetilen bir hizmettir.
*   **Neden Önemlidir? (Why?)**: Kubernetes, konteyner orkestrasyonu için endüstri standardı haline gelmiş açık kaynaklı bir platformdur. EKS, Kubernetes'in kontrol düzlemini (control plane) kurma ve yönetme karmaşıklığını ortadan kaldırır, böylece siz uygulamalarınıza odaklanabilirsiniz.
*   **Sınav İpucu**: Soruda **Kubernetes** geçiyorsa, cevap her zaman **EKS**'dir. ECS, AWS'in kendi çözümü iken, EKS açık kaynaklı Kubernetes'i yönetilen bir hizmet olarak sunar.

#### **Serverless Introduction (Sunucusuz Mimarilere Giriş)**

*   **Nedir? (What?)**: Geliştiricilerin sunucuları düşünmeden uygulama ve hizmetler oluşturmasına olanak tanıyan bir bulut bilişim modelidir. Sunucu yoktur anlamına gelmez; sunucuların yönetimi, yamalanması, ölçeklendirilmesi gibi görevlerin tamamının AWS tarafından yapıldığı anlamına gelir.
*   **Neden Önemlidir? (Why?)**: Altyapı yönetimini ortadan kaldırır, otomatik ölçeklendirme sağlar ve "kullandığın kadar öde" modelini en saf haliyle uygular (kodunuz çalışmıyorsa hiçbir ücret ödemezsiniz).
*   **Sınav İpucu**: AWS Lambda, sunucusuz (serverless) mimarinin en temel yapı taşıdır. Fargate, Athena, DynamoDB gibi servisler de sunucusuz kategorisine girer.

#### **Lambda Overview (Lambda'ya Genel Bakış)**

*   **Nedir? (What?)**: Sunucuları yönetmeden kodunuzu çalıştırmanızı sağlayan bir **sunucusuz (serverless) işlem hizmetidir**.
*   **Neden Önemlidir? (Why?)**: Sadece kodunuzu yüklersiniz ve Lambda, kodunuzu çalıştırmak ve ölçeklendirmek için gereken her şeyi yüksek erişilebilirlikle yönetir. Olay tabanlı (event-driven) mimariler için mükemmeldir.
*   **Nasıl Çalışır? (How?)**: Kodunuzu bir "Lambda fonksiyonu" olarak yüklersiniz. Bu fonksiyon, bir olay (event) tarafından tetiklenir. Örneğin, bir S3 bucket'ına yeni bir dosya yüklendiğinde, bir API Gateway'e istek geldiğinde veya bir DynamoDB tablosu güncellendiğinde bir Lambda fonksiyonu otomatik olarak çalışabilir.
*   **Sınav İpucu**: Anahtar kelimeler: **Serverless**, **Function as a Service (FaaS)**, **Event-driven**. Lambda'nın fiyatlandırması, fonksiyonun çalışma süresi (milisaniye cinsinden) ve istek sayısına göredir. Maksimum çalışma süresi 15 dakikadır.

#### **API Gateway Overview (API Ağ Geçidine Genel Bakış)**

*   **Nedir? (What?)**: Geliştiricilerin her ölçekte API'ler oluşturmasını, yayınlamasını, bakımını yapmasını, izlemesini ve güvenliğini sağlamasını kolaylaştıran tam yönetilen bir hizmettir.
*   **Neden Önemlidir? (Why?)**: Uygulamanızın "ön kapısı" gibi davranır. Gelen istekleri alır ve bunları AWS Lambda, EC2 veya diğer web servisleri gibi arka uç (backend) hizmetlerine yönlendirir.
*   **Nasıl Çalışır? (How?)**: RESTful API'ler ve WebSocket API'leri oluşturmanızı sağlar. İstekleri yönetme, trafik kontrolü (throttling), güvenlik (yetkilendirme), önbelleğe alma (caching) ve izleme gibi özellikleri kutudan çıktığı gibi sunar.
*   **Sınav İpucu**: Genellikle **Lambda** ile birlikte kullanılır ve sunucusuz uygulamaların temelini oluşturur. "Sunucusuz bir uygulama için bir REST API'si nasıl oluşturulur?" sorusunun cevabı **API Gateway + Lambda** ikilisidir.

#### **Batch Overview (Batch'e Genel Bakış)**

*   **Nedir? (What?)**: Geliştiricilerin, bilim insanlarının ve mühendislerin on binlerce, hatta yüz binlerce **toplu iş (batch computing)** işini AWS üzerinde verimli bir şekilde çalıştırmasını sağlayan tam yönetilen bir hizmettir.
*   **Neden Önemlidir? (Why?)**: İş yükünüze göre işlem kaynaklarını (EC2 veya Spot Instance'lar gibi) dinamik olarak sağlar ve yönetir. Bu, altyapı yönetimi karmaşıklığı olmadan büyük ölçekli hesaplama yapmanızı sağlar.
*   **Sınav İpucu**: Anahtar kelime: **Batch Computing**.

#### **Lightsail Overview (Lightsail'e Genel Bakış)**

*   **Nedir? (What?)**: Bir sanal özel sunucu (Virtual Private Server - VPS) başlatmak için gereken her şeyi içeren, kullanımı kolay bir bulut platformudur.
*   **Neden Önemlidir? (Why?)**: AWS'e yeni başlayanlar veya basit uygulamalar ve web siteleri için tasarlanmıştır. Sanal makine, SSD tabanlı depolama, veri transferi, DNS yönetimi ve statik IP gibi bileşenleri öngörülebilir, düşük ve aylık bir fiyata paket halinde sunar.
*   **Nasıl Çalışır? (How?)**: EC2, EBS, Route 53 gibi temel AWS servislerini arka planda kullanarak basitleştirilmiş bir arayüz sunar.
*   **Sınav İpucu**: Anahtar kelimeler: **VPS**, **Simple**, **Low, predictable price**. AWS'in en basit ve başlangıç dostu bilişim hizmetidir.

---

### **Bölüm 9: Deployments & Managing Infrastructure at Scale (Dağıtımlar ve Altyapıyı Ölçekte Yönetme)**

#### **CloudFormation Overview (CloudFormation'a Genel Bakış)**

*   **Nedir? (What?)**: AWS kaynaklarınızı **kod olarak (Infrastructure as Code - IaC)** modellemenizi ve kurmanızı sağlayan bir hizmettir.
*   **Neden Önemlidir? (Why?)**: Altyapınızı bir metin dosyası (YAML veya JSON formatında bir şablon) içinde tanımlayarak, kaynaklarınızı otomatik, tekrarlanabilir ve güvenli bir şekilde oluşturmanızı sağlar. Bu, manuel hataları azaltır ve tutarlılık sağlar.
*   **Nasıl Çalışır? (How?)**: Bir şablon oluşturursunuz, bu şablonda istediğiniz tüm kaynakları (EC2, S3, VPC vb.) ve özelliklerini belirtirsiniz. CloudFormation bu şablonu okur ve tüm kaynakları sizin için doğru sırada oluşturur.
*   **Sınav İpucu**: Anahtar kelime: **Infrastructure as Code (IaC)**. "AWS altyapısını şablon kullanarak otomatikleştirmek" senaryosunun cevabı **CloudFormation**'dır.

#### **CDK Overview (CDK'ye Genel Bakış)**

*   **Nedir? (What?)**: AWS Cloud Development Kit (CDK), Python, JavaScript, TypeScript, Java gibi tanıdık programlama dillerini kullanarak bulut altyapınızı kod olarak tanımlamanızı sağlayan bir açık kaynaklı yazılım geliştirme çerçevesidir.
*   **Neden Önemlidir? (Why?)**: CloudFormation'ın gücünü, programlama dillerinin ifade yeteneği ve araçlarıyla birleştirir. Bu, daha az kodla daha karmaşık altyapılar oluşturmayı ve yeniden kullanılabilir bileşenler yaratmayı kolaylaştırır.
*   **Sınav İpucu**: CDK, yazdığınız kodu arka planda **CloudFormation şablonlarına** dönüştürür. CloudFormation'a göre daha modern ve geliştirici dostu bir IaC yaklaşımıdır.

#### **Beanstalk Overview (Beanstalk'a Genel Bakış)**

*   **Nedir? (What?)**: Java, .NET, PHP, Node.js, Python, Ruby, Go ve Docker gibi teknolojilerle geliştirilmiş web uygulamalarını ve hizmetlerini dağıtmak ve ölçeklendirmek için kullanılan, kullanımı kolay bir **PaaS (Platform as a Service)** hizmetidir.
*   **Neden Önemlidir? (Why?)**: Sadece kodunuzu yüklersiniz ve Elastic Beanstalk, kapasite sağlama, yük dengeleme, otomatik ölçeklendirme ve uygulama sağlığı izleme gibi dağıtım ayrıntılarını otomatik olarak yönetir.
*   **Nasıl Çalışır? (How?)**: Arka planda CloudFormation, EC2, S3, ELB, ASG gibi servisleri sizin için otomatik olarak yapılandırır.
*   **Sınav İpucu**: Anahtar kelime: **PaaS**. "Altyapıyı yönetmeden sadece kodumu yükleyerek bir web uygulaması dağıtmak istiyorum" senaryosunun cevabı **Elastic Beanstalk**'tır. CloudFormation'dan farkı, Beanstalk'un uygulama odaklı, CloudFormation'ın ise altyapı odaklı olmasıdır.

#### **CodeDeploy, CodeCommit, CodeBuild, CodePipeline Overview (Code* Servislerine Genel Bakış)**

*   **Nedir? (What?)**: AWS'in **CI/CD (Continuous Integration/Continuous Deployment - Sürekli Entegrasyon/Sürekli Dağıtım)** araç setidir.
    *   **CodeCommit**: Tam yönetilen bir **kaynak kontrol (source control)** hizmetidir. Git tabanlıdır. GitHub/GitLab'in AWS'teki karşılığıdır.
    *   **CodeBuild**: Kaynak kodunu derleyen, testler çalıştıran ve dağıtıma hazır yazılım paketleri üreten tam yönetilen bir **derleme (build)** hizmetidir.
    *   **CodeDeploy**: EC2, Fargate, Lambda ve şirket içi sunucular gibi çeşitli işlem hizmetlerine uygulama dağıtımlarını **otomatikleştiren** bir hizmettir.
    *   **CodePipeline**: Yazılımınızı yayınlamak için gereken adımları (derleme, test, dağıtım) modellemenizi, görselleştirmenizi ve otomatikleştirmenizi sağlayan tam yönetilen bir **sürekli teslimat (continuous delivery)** hizmetidir. Tüm bu Code* servislerini bir araya getirip bir iş akışı oluşturur.
*   **Sınav İpucu**: "Kodumu nerede saklarım?" -> **CodeCommit**. "Kodumu nasıl derlerim ve test ederim?" -> **CodeBuild**. "Uygulamamı sunuculara nasıl dağıtırım?" -> **CodeDeploy**. "Tüm bu CI/CD sürecini nasıl otomatikleştirebilirim?" -> **CodePipeline**.

#### **Systems Manager (SSM) Overview (Sistem Yöneticisine Genel Bakış)**

*   **Nedir? (What?)**: AWS kaynaklarınız üzerinde operasyonel görünürlük ve kontrol sağlayan bir yönetim hizmetidir.
*   **Neden Önemlidir? (Why?)**: EC2 instance'larınıza ve şirket içi sunucularınıza yama (patch) yapma, yazılım yükleme, yapılandırmaları yönetme gibi görevleri otomatikleştirebilirsiniz.
*   **Nasıl Çalışır? (How?)**:
    *   **SSM Session Manager**: Sunucularınıza SSH veya RDP portlarını açmadan, tarayıcı üzerinden veya CLI ile güvenli bir şekilde komut satırı erişimi sağlar.
    *   **SSM Parameter Store**: Parolalar, veritabanı bağlantı dizeleri gibi yapılandırma verilerini ve sırları güvenli bir şekilde depolamak için kullanılır.
*   **Sınav İpucu**: "Sunucularıma SSH portunu açmadan nasıl bağlanırım?" -> **SSM Session Manager**. "Uygulama sırlarımı (secrets) nerede güvenle saklarım?" -> **SSM Parameter Store** (veya AWS Secrets Manager).

---

### **Bölüm 10: Leveraging the AWS Global Infrastructure (AWS Küresel Altyapısından Yararlanma)**

#### **Why Global Applications? (Neden Küresel Uygulamalar?)**

*   **Nedir? (What?)**: Uygulamaları tek bir coğrafi bölge yerine birden fazla AWS Region'ına dağıtarak küresel bir kullanıcı kitlesine hizmet verme stratejisidir.
*   **Neden Önemlidir? (Why?)**:
    1.  **Reduced Latency (Düşük Gecikme)**: İçeriği kullanıcılara coğrafi olarak daha yakın sunuculardan sunarak uygulama yanıt süresini iyileştirir.
    2.  **Disaster Recovery (Felaket Kurtarma)**: Bir Region'ın tamamını etkileyen bir felaket durumunda, uygulamanızın başka bir Region'da çalışmaya devam etmesini sağlar.
    3.  **Compliance (Uyumluluk)**: Bazı ülkelerin veri egemenliği yasaları, verilerin o ülke sınırları içinde kalmasını gerektirir. Küresel mimari bu gereksinimleri karşılamaya yardımcı olur.
*   **Sınav İpucu**: Küresel bir uygulama tasarlamanın temel motivasyonları düşük gecikme ve felaket kurtarmadır.

#### **Route 53 Overview (Route 53'e Genel Bakış)**

*   **Nedir? (What?)**: Amazon Route 53, yüksek erişilebilir ve ölçeklenebilir bir bulut **Alan Adı Sistemi (Domain Name System - DNS)** web hizmetidir.
*   **Neden Önemlidir? (Why?)**: Üç ana işlevi vardır:
    1.  **Domain Registration (Alan Adı Kaydı)**: `example.com` gibi alan adlarını kaydetmenizi sağlar.
    2.  **DNS Routing (DNS Yönlendirme)**: `www.example.com` gibi kullanıcı dostu isimleri, bilgisayarların birbirleriyle iletişim kurmak için kullandığı 192.0.2.1 gibi sayısal IP adreslerine çevirir.
    3.  **Health Checks (Sağlık Kontrolleri)**: Kaynaklarınızın (web sunucuları gibi) sağlığını izler ve bir kaynak sağlıksız hale gelirse trafiği otomatik olarak sağlıklı kaynaklara yönlendirir.
*   **Nasıl Çalışır? (How?)**: Kullanıcı bir web sitesine gitmek istediğinde, Route 53 bu isteği alır ve kullanıcıyı coğrafi konumuna, sunucu sağlığına veya diğer politikalara göre en uygun sunucuya yönlendirir.
*   **Sınav İpucu**: Route 53, **küresel (global)** bir servistir. Adındaki "53", DNS'in çalıştığı TCP/UDP port numarasından gelir. Sınavda "DNS" veya "domain" ile ilgili bir soru gördüğünüzde, cevap büyük ihtimalle **Route 53**'tür.

#### **CloudFront Overview (CloudFront'a Genel Bakış)**

*   **Nedir? (What?)**: Düşük gecikme ve yüksek veri aktarım hızları ile içeriği (web siteleri, videolar, API'ler) küresel olarak güvenli bir şekilde sunan bir **İçerik Dağıtım Ağı (Content Delivery Network - CDN)** hizmetidir.
*   **Neden Önemlidir? (Why?)**: Kullanıcılarınıza içeriği, coğrafi olarak onlara en yakın olan **Edge Location (Uç Konum)**'lardan sunarak web sitenizin ve uygulamanızın yüklenme hızını önemli ölçüde artırır.
*   **Nasıl Çalışır? (How?)**: İçeriğinizin bir kopyasını (önbelleğe alınmış - cached) dünya geneline yayılmış Edge Location'larda saklar. Bir kullanıcı içeriğinize erişmek istediğinde, CloudFront onu isteğin yapıldığı yere en yakın Edge Location'a yönlendirir. Bu, içeriğin ana sunucudan (Origin) gelmesi için bekleme süresini azaltır.
*   **Sınav İpucu**: Anahtar kelimeler: **CDN**, **Edge Location**, **Low Latency**, **Caching**. CloudFront, DDoS saldırılarına karşı koruma sağlamak için AWS Shield ile entegre çalışır. S3'teki statik içerik veya EC2'deki dinamik içerik için bir "ön katman" olarak kullanılabilir.

#### **S3 Transfer Acceleration**

*   **Nedir? (What?)**: Uzak mesafelerden S3 bucket'ınıza dosya yüklemeyi hızlandıran bir özelliktir.
*   **Neden Önemlidir? (Why?)**: Dünyanın farklı yerlerindeki kullanıcıların veya ofislerin, genel internet yerine AWS'in optimize edilmiş küresel ağ altyapısını kullanarak S3'e çok daha hızlı veri yüklemesini sağlar.
*   **Nasıl Çalışır? (How?)**: Veriler, kullanıcıya en yakın Edge Location'a yüklenir ve oradan AWS'in özel ağı üzerinden S3 bucket'ına aktarılır.
*   **Sınav İpucu**: Bu özellik, **gelen (upload)** trafiği hızlandırmak içindir. İçerik **dağıtımını (download)** hızlandırmak için CloudFront kullanılır.

#### **AWS Global Accelerator**

*   **Nedir? (What?)**: Uygulamalarınızın küresel kullanıcılar için erişilebilirliğini ve performansını artıran bir ağ hizmetidir.
*   **Neden Önemlidir? (Why?)**: CloudFront gibi içeriği önbelleğe almaz, bunun yerine kullanıcı trafiğini AWS'in sıkışık olmayan, yüksek performanslı küresel ağı üzerinden en uygun AWS uç noktasına (endpoint) yönlendirir.
*   **Nasıl Çalışır? (How?)**: Size, uygulamanız için dünya genelinde herhangi bir yerden erişilebilen iki adet statik IP adresi verir. Kullanıcı trafiği en yakın Edge Location'dan AWS ağına girer ve oradan uygulamanızın çalıştığı Region'a en optimize yoldan gider.
*   **Sınav İpucu**: CloudFront, önbelleğe alınabilir (statik) içerik için idealdir. Global Accelerator ise önbelleğe alınamayan (dinamik) içerikler, oyun, VoIP gibi TCP/UDP tabanlı uygulamalar için daha uygundur. Anahtar farkı: **Statik IP adresleri** sağlamasıdır.

#### **AWS Outposts**

*   **Nedir? (What?)**: AWS altyapısını, servislerini, API'lerini ve araçlarını neredeyse her veri merkezine, ortak yerleşim alanına veya şirket içi (on-premises) tesise genişleten tam yönetilen bir hizmettir.
*   **Neden Önemlidir? (Why?)**: Çok düşük gecikme gerektiren (örn: fabrika otomasyonu) veya yerel veri işleme ve depolama ihtiyacı olan (örn: veri egemenliği yasaları) uygulamalar için **hibrit bir deneyim** sunar.
*   **Nasıl Çalışır? (How?)**: AWS, kendi veri merkezlerinde kullandığı donanımın aynısını sizin tesisinize kurar ve yönetir. Siz bu donanım üzerinde EC2, EBS, RDS gibi tanıdık AWS servislerini çalıştırırsınız.
*   **Sınav İpucu**: Anahtar kelimeler: **Hybrid**, **On-premises**, **Low Latency**. "AWS servislerini kendi veri merkezimde çalıştırmak istiyorum" senaryosunun cevabı **Outposts**'tur.

#### **AWS WaveLength**

*   **Nedir? (What?)**: AWS işlem ve depolama hizmetlerini 5G ağlarının uç noktalarına yerleştiren bir altyapı teklifidir.
*   **Neden Önemlidir? (Why?)**: Mobil cihazlardan ve son kullanıcılardan gelen uygulama trafiğinin 5G ağından ayrılmasına gerek kalmadan, ultra düşük gecikmeli (ultra-low-latency) uygulamalar geliştirmeyi sağlar.
*   **Sınav İpucu**: Soruda **5G** ve **ultra-low-latency mobile applications** geçiyorsa, cevap **WaveLength**'tir.

#### **AWS Local Zones**

*   **Nedir? (What?)**: AWS işlem, depolama, veritabanı ve diğer belirli hizmetleri büyük nüfus ve endüstri merkezlerine, yani son kullanıcılara coğrafi olarak daha yakın bir yere konumlandıran bir AWS altyapı dağıtım türüdür.
*   **Neden Önemlidir? (Why?)**: Bir AWS Region'ının bir uzantısıdır ve son kullanıcılara tek haneli milisaniye gecikme süresi gerektiren uygulamaları çalıştırmayı kolaylaştırır.
*   **Sınav İpucu**: Outposts sizin veri merkezinize gelir, Local Zones ise AWS'in belirli şehirlerde kurduğu küçük altyapı noktalarıdır. İkisinin de amacı gecikmeyi azaltmaktır.

---

### **Bölüm 11: Cloud Integrations (Bulut Entegrasyonları)**

#### **Cloud Integrations Overview & SQS Overview (Bulut Entegrasyonlarına ve SQS'e Genel Bakış)**

*   **Nedir? (What?)**: Uygulamaları **ayrıştırmak (decoupling)**, modern bulut mimarilerinin temel prensiplerinden biridir. Bu, bir uygulamanın farklı bileşenlerinin birbirine sıkı sıkıya bağlı olmadan, bağımsız olarak çalışabilmesi anlamına gelir. AWS'in entegrasyon servisleri bu ayrıştırmayı sağlar.
*   **Amazon SQS (Simple Queue Service)**: Tam yönetilen bir **mesaj kuyruklama (message queuing)** hizmetidir.
*   **Neden Önemlidir? (Why?)**: SQS, uygulama bileşenleri arasında mesaj gönderip almanızı sağlar. Bir bileşen (producer) mesajı bir kuyruğa (queue) gönderir, diğer bileşen (consumer) ise kendi hızında bu mesajı kuyruktan alıp işler. Bu, bileşenler arasında doğrudan bir bağlantı olmamasını sağlar. Eğer consumer çökerse, mesaj kuyrukta güvende kalır ve consumer tekrar ayağa kalktığında işlenebilir. Bu, sistemin **güvenilirliğini (reliability)** ve **hata toleransını (fault tolerance)** artırır.
*   **Sınav İpucu**: Anahtar kelimeler: **Decoupling**, **Message Queue**. "İki uygulama bileşenini birbirinden ayrıştırmak için hangi servis kullanılır?" sorusunun cevabı **SQS**'dir.

#### **Kinesis Overview (Kinesis'e Genel Bakış)**

*   **Nedir? (What?)**: **Gerçek zamanlı (real-time)** akan verileri (streaming data) toplamak, işlemek ve analiz etmeyi kolaylaştıran bir hizmet ailesidir.
*   **Neden Önemlidir? (Why?)**: IoT cihazlarından, log dosyalarından, sosyal medya akışlarından gelen sürekli veri akışını işlemenizi sağlar.
*   **Sınav İpucu**: Anahtar kelimeler: **Real-time**, **Streaming Data**. SQS genellikle bireysel mesajlar için kullanılırken, Kinesis büyük hacimli ve sürekli veri akışları için tasarlanmıştır.

#### **SNS Overview (SNS'ye Genel Bakış)**

*   **Nedir? (What?)**: Amazon Simple Notification Service (SNS), tam yönetilen bir **yayınla/abone ol (publish/subscribe - pub/sub)** mesajlaşma hizmetidir.
*   **Neden Önemlidir? (Why?)**: Bir mesajı bir "konuya" (topic) gönderirsiniz ve bu konuya abone olan tüm uç noktalara (endpoints) bu mesaj anında iletilir.
*   **Nasıl Çalışır? (How?)**: Bir "producer" mesajı bir SNS topic'ine yayınlar. Bu topic'e abone olan SQS kuyrukları, Lambda fonksiyonları, HTTP/S uç noktaları, e-posta adresleri ve mobil anlık bildirim (push notification) servisleri gibi birden fazla "subscriber" bu mesajı aynı anda alır.
*   **Sınav İpucu**: SQS'ten temel farkı: SQS'te bir mesaj genellikle **tek bir consumer** tarafından işlenir (point-to-point). SNS'te ise bir mesaj **birden fazla subscriber**'a gönderilir (fan-out). "Bir olayı birden fazla farklı servise aynı anda bildirmek için ne kullanılır?" -> **SNS**.

#### **Amazon MQ Overview (Amazon MQ'ye Genel Bakış)**

*   **Nedir? (What?)**: Apache ActiveMQ ve RabbitMQ gibi popüler açık kaynaklı mesaj aracılarını (message brokers) bulutta kurmayı ve yönetmeyi kolaylaştıran yönetilen bir hizmettir.
*   **Neden Önemlidir? (Why?)**: Mevcut uygulamalarını bu standart mesajlaşma protokollerini (JMS, AMQP vb.) kullanarak AWS'e taşımak isteyen kuruluşlar için tasarlanmıştır.
*   **Sınav İpucu**: SQS ve SNS, bulut için tasarlanmış, özel protokollere sahip servislerdir. Eğer soruda **ActiveMQ**, **RabbitMQ** veya **mevcut mesajlaşma altyapısını taşıma (migration)** gibi ifadeler geçiyorsa, cevap **Amazon MQ**'dur.

---

### **Bölüm 12: Cloud Monitoring (Bulut İzleme)**

#### **CloudWatch Metrics & CloudWatch Alarms Overview (CloudWatch Metrikleri ve Alarmlarına Genel Bakış)**

*   **Nedir? (What?)**:
    *   **Amazon CloudWatch**: AWS kaynaklarınız, uygulamalarınız ve şirket içi sunucularınız için bir **izleme ve gözlemlenebilirlik (monitoring and observability)** hizmetidir.
    *   **Metrics (Metrikler)**: CloudWatch'un temel konseptidir. Bir kaynağın zaman içindeki performansını temsil eden veri noktalarıdır. Örneğin, bir EC2 instance'ının CPU kullanımı (CPUUtilization) bir metriktir. AWS servisleri, kendi metriklerini otomatik olarak CloudWatch'a gönderir.
    *   **Alarms (Alarmlar)**: Belirli bir metrik, tanımladığınız bir eşiği aştığında (veya altına düştüğünde) otomatik olarak eylemler gerçekleştirir.
*   **Neden Önemlidir? (Why?)**: Sistemlerinizin sağlığını ve performansını proaktif olarak izlemenizi sağlar. Bir sorun oluştuğunda (örn: CPU kullanımı %90'ı geçtiğinde), bir alarm tetiklenir ve bu alarm bir SNS konusuna bildirim gönderebilir, bir Auto Scaling eylemini tetikleyebilir veya bir EC2 instance'ını yeniden başlatabilir.
*   **Sınav İpucu**: CloudWatch, AWS'in ana izleme aracıdır. "EC2 CPU kullanımını izlemek" veya "bir metrik belirli bir seviyeye ulaştığında bildirim almak" gibi senaryoların cevabı **CloudWatch**'tur. Auto Scaling gruplarının dinamik ölçeklendirme kararları genellikle CloudWatch alarmlarına dayanır.

#### **CloudWatch Logs Overview (CloudWatch Günlüklerine Genel Bakış)**

*   **Nedir? (What?)**: EC2 instance'larınızdan, AWS CloudTrail'den, Route 53'ten ve diğer kaynaklardan gelen günlük (log) dosyalarını izlemenizi, depolamanızı ve bunlara erişmenizi sağlayan bir CloudWatch özelliğidir.
*   **Neden Önemlidir? (Why?)**: Uygulama ve sistem günlüklerinizi merkezi bir yerde toplayarak sorun gidermeyi (troubleshooting) ve analiz yapmayı kolaylaştırır.
*   **Nasıl Çalışır? (How?)**: Sunucularınıza **CloudWatch Agent**'ı kurarak uygulama logları, sistem logları gibi dosyaların otomatik olarak CloudWatch Logs'a gönderilmesini sağlayabilirsiniz.
*   **Sınav İpucu**: **Metrikler** performans verileridir (sayılar), **Loglar** ise olay kayıtlarıdır (metin). "Uygulama hatalarını analiz etmek için logları nerede toplarım?" sorusunun cevabı **CloudWatch Logs**'tur.

#### **EventBridge Overview (formerly CloudWatch Events) (EventBridge'e Genel Bakış)**

*   **Nedir? (What?)**: Kendi uygulamalarınızdan, SaaS uygulamalarından ve AWS hizmetlerinden gelen olayları (events) kullanarak olay tabanlı (event-driven) uygulamalar oluşturmanızı kolaylaştıran **sunucusuz bir olay veri yolu (serverless event bus)** hizmetidir.
*   **Neden Önemlidir? (Why?)**: AWS ortamınızdaki durum değişikliklerini (örn: bir EC2 instance'ının durması, bir S3 nesnesinin oluşturulması) temsil eden olayları merkezi olarak yönetmenizi sağlar. Bu olaylara göre kurallar tanımlayarak Lambda fonksiyonları, SQS kuyrukları gibi hedefleri tetikleyebilirsiniz.
*   **Nasıl Çalışır? (How?)**: Bir olay kaynağı (source) bir olay yayınlar, EventBridge bu olayı alır ve tanımladığınız kurallara (rules) göre ilgili hedeflere (targets) yönlendirir.
*   **Sınav İpucu**: CloudWatch Alarms, metrik eşiklerine göre tepki verir. EventBridge ise **olaylara (durum değişikliklerine)** göre tepki verir. "Her saat başı bir Lambda fonksiyonunu çalıştırmak" (zamanlanmış olay) veya "bir CodePipeline başarılı olduğunda bir SNS bildirimi göndermek" (durum değişikliği olayı) gibi senaryolar için **EventBridge** kullanılır.

#### **CloudTrail Overview (CloudTrail'e Genel Bakış)**

*   **Nedir? (What?)**: AWS hesabınızdaki **API çağrılarını** kaydeden ve bu kayıtları size sunan bir hizmettir. Hesabınızda yapılan her eylemin denetim kaydını (audit trail) tutar.
*   **Neden Önemlidir? (Why?)**: **Yönetişim (governance), uyumluluk (compliance) ve operasyonel/risk denetimi** için temel bir araçtır. "Kim, ne zaman, nereden, ne yaptı?" sorularının cevabını verir.
*   **Nasıl Çalışır? (How?)**: Bir kullanıcı konsoldan bir EC2 instance'ı başlattığında, bir uygulama SDK kullanarak bir S3 nesnesi sildiğinde veya bir servis IAM rolü üstlendiğinde, CloudTrail bu API çağrısını bir olay olarak kaydeder. Bu olaylar CloudTrail konsolunda görüntülenebilir ve uzun süreli saklama için bir S3 bucket'ına gönderilebilir.
*   **Sınav İpucu**: **CloudWatch** kaynakların **performansını** izler. **CloudTrail** ise hesap **aktivitesini (API çağrılarını)** izler. "Hesabımda bir S3 bucket'ını kimin sildiğini nasıl bulurum?" sorusunun cevabı **CloudTrail**'dir.

#### **X-Ray Overview (X-Ray'e Genel Bakış)**

*   **Nedir? (What?)**: Geliştiricilerin, özellikle mikroservis mimarileriyle oluşturulmuş dağıtık uygulamaları analiz etmelerine ve hatalarını ayıklamalarına yardımcı olan bir hizmettir.
*   **Neden Önemlidir? (Why?)**: Bir isteğin uygulamanızın farklı bileşenlerinden (API Gateway, Lambda, DynamoDB vb.) geçerken izlediği yolu görselleştirir. Performans darboğazlarını ve hataların nerede meydana geldiğini tespit etmeyi kolaylaştırır.
*   **Sınav İpucu**: Anahtar kelimeler: **Distributed Tracing**, **Performance Bottlenecks**, **Microservices**.

#### **CodeGuru Overview (CodeGuru'ya Genel Bakış)**

*   **Nedir? (What?)**: Kod kalitesini artırmak ve uygulama performansını optimize etmek için akıllı öneriler sunan bir geliştirici aracıdır.
*   **Nasıl Çalışır? (How?)**: İki ana bileşeni vardır:
    *   **CodeGuru Reviewer**: Kodunuzdaki kritik sorunları, güvenlik açıklarını ve AWS en iyi pratiklerinden sapmaları tespit etmek için makine öğrenimini kullanır.
    *   **CodeGuru Profiler**: Üretimdeki (production) uygulamanızın performansını analiz eder ve en "pahalı" (en çok CPU tüketen) kod satırlarını bularak optimizasyon önerileri sunar.
*   **Sınav İpucu**: "Kodumdaki hataları ve güvenlik açıklarını otomatik olarak bulmak" -> **CodeGuru Reviewer**. "Uygulamamın performansını optimize etmek" -> **CodeGuru Profiler**.

#### **AWS Health Dashboard**

*   **Nedir? (What?)**: AWS hizmetlerinin genel durumu hakkında bilgi sağlayan ve sizin kullandığınız kaynakları etkileyen olaylar hakkında kişiselleştirilmiş bir görünüm sunan bir araçtır.
*   **Nasıl Çalışır? (How?)**: İki ana görünümü vardır:
    *   **Service Health Dashboard**: Tüm AWS hizmetlerinin tüm Region'lardaki genel durumunu gösterir.
    *   **Personal Health Dashboard**: Sizin AWS hesabınızı ve kaynaklarınızı etkileyebilecek olaylar (planlı bakımlar, bir EC2 instance'ınızın çalıştığı donanımda sorun olması vb.) hakkında size özel uyarılar ve rehberlik sağlar.
*   **Sınav İpucu**: Genel AWS hizmet durumu için Service Health Dashboard, size özel olaylar için **Personal Health Dashboard** kullanılır.

---

### **Bölüm 13: VPC & Networking (VPC ve Ağ)**

#### **VPC Overview (VPC'ye Genel Bakış)**

*   **Nedir? (What?)**: Amazon Virtual Private Cloud (VPC), AWS bulutunda mantıksal olarak izole edilmiş kendi sanal ağınızı oluşturmanızı sağlayan bir hizmettir.
*   **Neden Önemlidir? (Why?)**: Kendi IP adresi aralığınızı seçme, alt ağlar (subnets) oluşturma, yönlendirme tabloları (route tables) ve ağ geçitleri (gateways) yapılandırma dahil olmak üzere sanal ağ ortamınız üzerinde tam kontrol sahibi olmanızı sağlar. Geleneksel, şirket içi ağınıza çok benzer bir yapı sunar.
*   **Sınav İpucu**: VPC, **Region** seviyesinde bir kaynaktır. Bir VPC oluşturduğunuzda, o Region'ın tüm Availability Zone'larını kapsar.

#### **IP Addresses in AWS (AWS'te IP Adresleri)**

*   **Nedir? (What?)**: VPC içindeki kaynakların birbirleriyle ve internetle iletişim kurmak için kullandığı adreslerdir.
    *   **Private IP**: VPC içinde iletişim için kullanılır, internetten erişilemez.
    *   **Public IP**: İnternetten erişilebilir bir adrestir. EC2 instance'ı durdurulup başlatıldığında değişebilir.
    *   **Elastic IP**: Hesabınıza tahsis edilen statik bir Public IP adresidir. Instance'lar arasında taşınabilir ve instance durdurulsa bile aynı kalır.
*   **Sınav İpucu**: Bir EC2 instance'ı için sabit, değişmeyen bir genel IP adresine ihtiyacınız varsa, **Elastic IP** kullanmalısınız.

#### **VPC, Subnet, Internet Gateway & NAT Gateways (VPC, Alt Ağ, İnternet Ağ Geçidi ve NAT Ağ Geçitleri)**

*   **Nedir? (What?)**: VPC'nin temel yapı taşlarıdır.
    *   **Subnet (Alt Ağ)**: Bir VPC'nin IP adresi aralığının bir bölümüdür. Kaynaklarınızı (EC2 gibi) alt ağların içine yerleştirirsiniz. Subnet'ler **Availability Zone'a özgüdür**.
    *   **Public Subnet**: Rota tablosunda bir **Internet Gateway (IGW)**'e giden bir rotası olan alt ağdır. Bu alt ağdaki kaynaklar internete doğrudan erişebilir.
    *   **Private Subnet**: Rota tablosunda bir Internet Gateway'e giden bir rotası olmayan alt ağdır. Bu alt ağdaki kaynaklar internetten doğrudan erişilemez.
    *   **Internet Gateway (IGW)**: VPC'niz ile internet arasında iletişimi sağlayan, yatay olarak ölçeklenen, yedekli ve yüksek erişilebilir bir VPC bileşenidir.
    *   **NAT Gateway (Network Address Translation)**: **Private Subnet**'teki instance'ların internete (örn: yazılım güncellemeleri için) çıkış yapmasına izin veren, ancak internetten bu instance'lara doğrudan bir bağlantı başlatılmasını engelleyen bir hizmettir.
*   **Sınav İpucu**: "Veritabanı gibi güvenli olması gereken kaynakları hangi alt ağa koymalıyım?" -> **Private Subnet**. "Private Subnet'teki bir sunucunun internetten yama indirmesi gerekiyor, bunu nasıl sağlarım?" -> **NAT Gateway**.

#### **Security Groups & Network Access Control List (NACL) (Güvenlik Grupları ve Ağ Erişim Kontrol Listesi)**

*   **Nedir? (What?)**: VPC'nizdeki güvenliği sağlamak için kullanılan iki farklı güvenlik duvarı katmanıdır.
    *   **Security Group**: **Instance seviyesinde** çalışır. Sadece `Allow` kuralları vardır ve **Stateful**'dur (giden yanıta otomatik izin verilir).
    *   **NACL (Network ACL)**: **Subnet seviyesinde** çalışır. Hem `Allow` hem de `Deny` kuralları vardır ve **Stateless**'tir (hem gelen hem de giden trafik için ayrı ayrı kurallar tanımlanmalıdır).
*   **Sınav İpucu**: Bu ikisinin karşılaştırması klasik bir sınav sorusudur. Security Group'lar ilk savunma hattı, NACL'ler ise ikinci savunma hattı olarak düşünülebilir. Bir `Deny` kuralına ihtiyacınız varsa, NACL kullanmalısınız.

#### **VPC Flow Logs & VPC Peering (VPC Akış Günlükleri ve VPC Eşleştirme)**

*   **Nedir? (What?)**:
    *   **VPC Flow Logs**: VPC'nizdeki ağ arayüzlerine giren ve çıkan IP trafiği hakkında bilgi yakalamanızı sağlayan bir özelliktir.
    *   **VPC Peering**: İki VPC'nin özel IP adreslerini kullanarak birbirleriyle iletişim kurmasını sağlayan bir ağ bağlantısıdır. Sanki aynı ağdaymış gibi davranırlar.
*   **Sınav İpucu**: "VPC'mdeki belirli bir IP'den gelen trafiği kimin engellediğini nasıl anlarım?" -> **VPC Flow Logs**. "İki farklı VPC'deki uygulamaların özel olarak haberleşmesi gerekiyor" -> **VPC Peering**.

#### **VPC Endpoints (VPC Uç Noktaları)**

*   **Nedir? (What?)**: VPC'niz ile S3 ve DynamoDB gibi desteklenen AWS hizmetleri arasında **genel internete çıkmadan**, özel ve güvenli bir bağlantı kurmanızı sağlar.
*   **Neden Önemlidir? (Why?)**: Güvenliği artırır çünkü trafik AWS ağı içinde kalır.
*   **Sınav İpucu**: "Private Subnet'teki bir EC2 instance'ının internete çıkmadan S3'e erişmesi gerekiyor" -> **VPC Endpoint**.

#### **PrivateLink**

*   **Nedir? (What?)**: Kendi VPC'leriniz, diğer AWS hesaplarının VPC'leri ve şirket içi ağlar arasında özel bağlantı sağlamayı basitleştiren bir teknolojidir.
*   **Sınav İpucu**: VPC Peering'e göre daha ölçeklenebilir ve yönetimi daha kolay bir alternatiftir.

#### **Direct Connect & Site-to-Site VPN (Direct Connect ve Siteden Siteye VPN)**

*   **Nedir? (What?)**: Şirket içi (on-premises) veri merkeziniz ile AWS VPC'niz arasında özel bir ağ bağlantısı kurmanın iki yoludur.
    *   **Site-to-Site VPN**: Genel internet üzerinden şifrelenmiş bir tünel (IPsec VPN) oluşturur. Kurulumu hızlı ve daha düşük maliyetlidir.
    *   **Direct Connect (DX)**: Şirket içi ağınızdan AWS'e özel, adanmış bir fiber optik ağ bağlantısıdır. İnterneti tamamen bypass eder.
*   **Neden Önemlidir? (Why?)**: Hibrit bulut mimarileri için temel bağlantı yöntemleridir.
*   **Sınav İpucu**: **Direct Connect**, VPN'e göre daha **yüksek bant genişliği**, daha **tutarlı performans** ve daha **yüksek güvenlik** sunar, ancak daha pahalıdır ve kurulumu daha uzun sürer. "Tutarlı ve yüksek performanslı bir bağlantı gerekiyor" -> **Direct Connect**. "Hızlı ve düşük maliyetli bir bağlantı gerekiyor" -> **Site-to-Site VPN**.

#### **Client VPN & Transit Gateway (İstemci VPN ve Transit Ağ Geçidi)**

*   **Nedir? (What?)**:
    *   **Client VPN**: Kullanıcıların (örn: evden çalışanlar) kendi bilgisayarlarından AWS veya şirket içi ağ kaynaklarına güvenli bir şekilde bağlanmasını sağlayan yönetilen bir hizmettir.
    *   **Transit Gateway**: Onlarca, hatta yüzlerce VPC'yi ve şirket içi ağı tek bir merkezi noktadan birbirine bağlamanızı sağlayan bir **ağ geçiş merkezidir (network transit hub)**.
*   **Sınav İpucu**: Çok sayıda VPC'yi birbirine bağlamak için karmaşık VPC Peering bağlantıları kurmak yerine, hepsini bir **Transit Gateway**'e bağlamak çok daha basit ve ölçeklenebilirdir.

---

### **Bölüm 14: Security & Compliance (Güvenlik ve Uyumluluk)**

#### **Shared Responsibility Model: Reminders & Examples (Paylaşılan Sorumluluk Modeli: Hatırlatmalar ve Örnekler)**

*   **Nedir? (What?)**: Bu modelin tekrar altını çizmek önemli. AWS, **bulutun güvenliğinden** (Security *OF* the Cloud) sorumludur. Bu, donanım, küresel altyapı ve yönetilen servislerin (S3, DynamoDB, RDS gibi) temel güvenliğini içerir. Müşteri ise **bulutun içindeki güvenliğinden** (Security *IN* the Cloud) sorumludur.
*   **Örnekler**:
    *   **Müşteri Sorumluluğu**: IAM kullanıcı yönetimi, verilerin istemci tarafında veya sunucu tarafında şifrelenmesi, işletim sistemi güncellemeleri ve yamaları, Security Group ve NACL kuralları, ağ trafiğinin korunması.
    *   **AWS Sorumluluğu**: Fiziksel veri merkezi güvenliği, ağ altyapısı, donanım, sanallaştırma katmanı.
*   **Sınav İpucu**: Sınavda size bir senaryo verilir ve bu senaryodaki güvenlik sorumluluğunun kime ait olduğu sorulur. Örneğin, "Bir EC2 instance'ına antivirüs yazılımı kurmak kimin sorumluluğundadır?" Cevap: **Müşteri**. "RDS veritabanının işletim sistemini yamalamak kimin sorumluluğundadır?" Cevap: **AWS** (çünkü RDS yönetilen bir hizmettir).

#### **DDoS Protection: WAF & Shield (DDoS Koruması: WAF ve Shield)**

*   **Nedir? (What?)**: Dağıtık Hizmet Reddi (Distributed Denial-of-Service - DDoS) saldırılarına karşı koruma sağlayan servislerdir.
    *   **AWS Shield**: Yönetilen bir DDoS koruma hizmetidir. İki katmanı vardır:
        *   **Shield Standard**: Tüm AWS müşterilerine **ek ücret olmadan** otomatik olarak sağlanır ve en yaygın, ağ katmanı (Layer 3/4) DDoS saldırılarına karşı koruma sağlar.
        *   **Shield Advanced**: Daha karmaşık ve büyük ölçekli DDoS saldırılarına karşı ek koruma, 7/24 erişilebilir DDoS Müdahale Ekibi (DRT) ve mali koruma (saldırı nedeniyle artan faturalara karşı) sunan ücretli bir hizmettir.
    *   **AWS WAF (Web Application Firewall)**: Web uygulamalarınızı, web açıklarından (web exploits) ve botlardan koruyan bir **web uygulaması güvenlik duvarıdır**. Uygulama katmanında (Layer 7) çalışır.
*   **Neden Önemlidir? (Why?)**: Uygulamalarınızın erişilebilirliğini ve güvenliğini tehdit eden yaygın siber saldırıları engeller.
*   **Nasıl Çalışır? (How?)**: WAF, CloudFront, Application Load Balancer veya API Gateway'in önüne yerleştirilir. Gelen HTTP/S isteklerini, SQL injection veya Cross-Site Scripting (XSS) gibi yaygın saldırı modellerini içeren kurallara göre inceler ve zararlı istekleri engeller.
*   **Sınav İpucu**: **Shield**, DDoS saldırılarına karşı korur. **WAF**, SQL injection gibi **web uygulaması saldırılarına** karşı korur. Shield Standard ücretsizdir ve otomatiktir.
*   AWS Shield Advanced provides expanded DDoS attack protection for web applications running on the following resources: Amazon Elastic Compute Cloud, Elastic Load Balancing (ELB), Amazon CloudFront, Amazon Route 53, AWS Global Accelerator.

#### **AWS Network Firewall & AWS Firewall Manager (AWS Ağ Güvenlik Duvarı ve AWS Güvenlik Duvarı Yöneticisi)**

*   **Nedir? (What?)**:
    *   **AWS Network Firewall**: Tüm Amazon VPC'leriniz için temel ağ korumalarını dağıtmayı kolaylaştıran yönetilen bir ağ güvenlik duvarı hizmetidir.
    *   **AWS Firewall Manager**: Kuruluşunuzdaki tüm hesaplar ve uygulamalar için güvenlik duvarı kurallarını (WAF, Shield Advanced, Network Firewall) merkezi olarak yapılandırmanızı ve yönetmenizi sağlayan bir güvenlik yönetimi hizmetidir.
*   **Sınav İpucu**: **Network Firewall**, VPC seviyesinde daha geleneksel bir ağ güvenliği sağlar. **Firewall Manager** ise birden fazla hesaptaki güvenlik duvarı kurallarını **merkezi olarak yönetmek** içindir.

#### **Penetration Testing (Sızma Testi)**

*   **Nedir? (What?)**: AWS, müşterilerinin kendi AWS altyapılarına karşı güvenlik açıklarını ve zafiyetlerini test etmek için sızma testleri yapmalarına izin verir.
*   **Neden Önemlidir? (Why?)**: Güvenlik duruşunuzu proaktif olarak test etmenizi ve zayıf noktaları saldırganlardan önce bulmanızı sağlar.
*   **Sınav İpucu**: Sızma testi yapmadan önce AWS'in politikasını kontrol etmeniz ve bazı durumlarda izin almanız gerekebilir. Ancak birçok servis için artık önceden izin gerekmemektedir.

#### **Encryption with KMS & CloudHSM (KMS ve CloudHSM ile Şifreleme)**

*   **Nedir? (What?)**: Şifreleme anahtarlarını yönetmek için kullanılan iki anahtar yönetim hizmetidir.
    *   **AWS KMS (Key Management Service)**: Şifreleme anahtarları oluşturmayı, yönetmeyi ve kullanmayı kolaylaştıran yönetilen bir hizmettir. Birçok AWS hizmetiyle (S3, EBS, RDS vb.) entegre çalışır.
    *   **AWS CloudHSM (Hardware Security Module)**: Bulutta size adanmış bir donanım güvenlik modülü (HSM) sağlar. Bu, şifreleme anahtarlarınız üzerinde tam kontrol sahibi olmanızı ve en katı yasal ve uyumluluk gereksinimlerini karşılamanızı sağlar.
*   **Neden Önemlidir? (Why?)**: Veri şifrelemesi için kritik olan anahtarların güvenli bir şekilde saklanmasını ve yönetilmesini sağlarlar.
*   **Sınav İpucu**: Çoğu kullanım durumu için **KMS** yeterlidir ve daha kolay bir seçenektir. Eğer soruda "FIPS 140-2 Level 3" gibi çok katı uyumluluk standartları veya "anahtarlar üzerinde tek ve tam kontrol" gibi ifadeler geçiyorsa, cevap **CloudHSM**'dir.

#### **AWS Certificate Manager (ACM) Overview (AWS Sertifika Yöneticisine Genel Bakış)**

*   **Nedir? (What?)**: AWS hizmetleri ve dahili bağlı kaynaklarınızla kullanmak üzere **genel (public) ve özel (private) SSL/TLS sertifikalarını** sağlamayı, yönetmeyi ve dağıtmayı basitleştiren bir hizmettir.
*   **Neden Önemlidir? (Why?)**: Web siteniz için HTTPS'i etkinleştirmeyi çok kolaylaştırır. ELB ve CloudFront gibi AWS hizmetleriyle entegre edilen **genel sertifikalar ücretsizdir** ve AWS bu sertifikaları sizin için otomatik olarak yeniler.
*   **Sınav İpucu**: Anahtar kelimeler: **SSL/TLS Certificates**, **HTTPS**. "Web sitem için ücretsiz SSL sertifikası nasıl alırım ve otomatik yenilenmesini nasıl sağlarım?" sorusunun cevabı **ACM**'dir.

#### **Secrets Manager Overview (Sırlar Yöneticisine Genel Bakış)**

*   **Nedir? (What?)**: Veritabanı kimlik bilgileri, API anahtarları ve diğer sırlar gibi hassas bilgileri yaşam döngüleri boyunca yönetmenize, almanıza ve **otomatik olarak döndürmenize (rotate)** yardımcı olan bir hizmettir.
*   **Neden Önemlidir? (Why?)**: Sırları kodun içine yazmak (hardcoding) gibi kötü güvenlik pratiklerini ortadan kaldırır. Sırların düzenli olarak değiştirilmesini (rotation) otomatikleştirerek güvenliği artırır.
*   **Sınav İpucu**: SSM Parameter Store ile benzerdir, ancak **otomatik sır döndürme (automatic rotation)** özelliği Secrets Manager'ın en önemli ayırt edici özelliğidir. "Veritabanı parolalarını her 30 günde bir otomatik olarak değiştirmek istiyorum" senaryosunun cevabı **Secrets Manager**'dır.

#### **GuardDuty Overview (GuardDuty'ye Genel Bakış)**

*   **Nedir? (What?)**: AWS hesabınızdaki ve iş yüklerinizdeki kötü amaçlı etkinlikleri ve yetkisiz davranışları sürekli olarak izleyen bir **tehdit algılama (threat detection)** hizmetidir.
*   **Neden Önemlidir? (Why?)**: Makine öğrenimi, anomali tespiti ve entegre tehdit istihbaratını kullanarak potansiyel güvenlik risklerini akıllıca tespit eder.
*   **Nasıl Çalışır? (How?)**: CloudTrail logları, VPC Flow logları ve DNS logları gibi veri kaynaklarını analiz eder. Örneğin, bir EC2 instance'ının bilinen bir kötü amaçlı IP adresiyle iletişim kurduğunu veya normalde yapmadığı bir şekilde API çağrıları yapmaya başladığını tespit edebilir.
*   **Sınav İpucu**: Anahtar kelimeler: **Threat Detection**, **Intelligent**. GuardDuty, hesabınızda olup biten şüpheli şeyleri size bildiren bir "akıllı güvenlik kamerası" gibidir.

#### **Inspector Overview (Inspector'a Genel Bakış)**

*   **Nedir? (What?)**: AWS iş yüklerinizdeki **güvenlik açıklarını (vulnerabilities)** ve en iyi pratiklerden sapmaları tarayan otomatik bir güvenlik değerlendirme hizmetidir.
*   **Neden Önemlidir? (Why?)**: EC2 instance'larınızdaki ve konteyner imajlarınızdaki yazılım güvenlik açıklarını (örn: güncel olmayan kütüphaneler) veya istenmeyen ağ erişimlerini proaktif olarak bulmanızı sağlar.
*   **Sınav İpucu**: **GuardDuty** hesabınızdaki **aktiviteleri** izler. **Inspector** ise kaynaklarınızın **yapılandırmasını** ve **içindeki yazılımları** tarayarak güvenlik açığı arar.

#### **Config Overview (Config'e Genel Bakış)**

*   **Nedir? (What?)**: AWS kaynaklarınızın yapılandırmalarını değerlendirmenize, denetlemenize ve incelemenize olanak tanıyan bir hizmettir.
*   **Neden Önemlidir? (Why?)**: Kaynak yapılandırmalarınızı sürekli olarak izler ve bunları istediğiniz yapılandırmalarla karşılaştırır. Bir kaynak, kurallarınıza uymayan bir şekilde değiştirilirse (örn: bir S3 bucket'ının herkese açık hale getirilmesi), AWS Config bunu tespit edip sizi uyarabilir.
*   **Sınav İpucu**: Anahtar kelimeler: **Configuration History**, **Compliance**, **Auditing**. "Bir Security Group kuralının geçmişte kim tarafından değiştirildiğini nasıl öğrenirim?" veya "Tüm EBS volümlerimin şifreli olduğundan nasıl emin olurum?" sorularının cevabı **AWS Config**'dir.

#### **Macie Overview (Macie'ye Genel Bakış)**

*   **Nedir? (What?)**: Amazon S3'teki **hassas verileri (sensitive data)** keşfetmek ve korumak için makine öğrenimini kullanan tam yönetilen bir veri güvenliği ve veri gizliliği hizmetidir.
*   **Neden Önemlidir? (Why?)**: S3 bucket'larınızda yanlışlıkla açığa çıkmış kişisel kimlik bilgileri (PII - Personally Identifiable Information), kredi kartı numaraları veya finansal veriler gibi hassas verileri otomatik olarak bulur.
*   **Sınav İpucu**: Soruda **S3** ve **hassas veri (PII, sensitive data) keşfi** geçiyorsa, cevap **Macie**'dir.

#### **Security Hub Overview (Güvenlik Merkezine Genel Bakış)**

*   **Nedir? (What?)**: AWS'deki güvenlik durumunuz hakkında kapsamlı bir görünüm sunan ve güvenlik endüstrisi standartlarına ve en iyi pratiklere uygunluğunuzu kontrol etmenize yardımcı olan bir hizmettir.
*   **Neden Önemlidir? (Why?)**: GuardDuty, Inspector, Macie gibi çeşitli AWS güvenlik servislerinden gelen bulguları ve uyarıları **tek bir merkezi yerde** toplar.
*   **Sınav İpucu**: Anahtar kelime: **Centralized View of Security Alerts**.

#### **Amazon Detective Overview (Amazon Detective'e Genel Bakış)**

*   **Nedir? (What?)**: Potansiyel güvenlik sorunlarının veya şüpheli etkinliklerin temel nedenini daha kolay analiz etmenizi, araştırmanızı ve hızlı bir şekilde belirlemenizi sağlayan bir hizmettir.
*   **Neden Önemlidir? (Why?)**: GuardDuty tarafından bulunan bir güvenlik sorununu araştırmak için kullanılır. İlgili log verilerini otomatik olarak toplar ve bunları etkileşimli bir grafikte görselleştirerek olayın kapsamını ve etkisini anlamanızı kolaylaştırır.
*   **Sınav İpucu**: **GuardDuty** bir sorunu bulur, **Detective** ise o sorunu **araştırmanıza** yardımcı olur.

---

### **Bölüm 15: Machine Learning (Makine Öğrenmesi)**

*Bu bölümdeki servisler için temel olarak "Nedir?" ve "Ne işe yarar?" (sınav ipucu) formatında ilerlemek daha akılda kalıcı olacaktır. Derin teknik detaylar Practitioner sınavı kapsamında değildir.*

#### **Rekognition Overview (Rekognition'a Genel Bakış)**

*   **Nedir? (What?)**: Görüntü ve video analizi yapmayı kolaylaştıran bir makine öğrenmesi hizmetidir.
*   **Ne İşe Yarar? (Sınav İpucu)**: Bir resimdeki nesneleri, kişileri, metinleri, sahneleri ve etkinlikleri tanımlayabilir. Örneğin, bir fotoğraftaki ünlü bir kişiyi tanıyabilir veya uygunsuz içeriği tespit edebilir. Anahtar kelimeler: **Image Analysis**, **Video Analysis**, **Object Detection**.

#### **Transcribe Overview (Transcribe'a Genel Bakış)**

*   **Nedir? (What?)**: Konuşmayı metne dönüştüren (speech-to-text) bir otomatik konuşma tanıma (ASR - Automatic Speech Recognition) hizmetidir.
*   **Ne İşe Yarar? (Sınav İpucu)**: Ses dosyalarını (örn: müşteri hizmetleri görüşmeleri, podcast'ler) otomatik olarak yazılı metne çevirir. Anahtar kelime: **Speech-to-Text**.

#### **Polly Overview (Polly'ye Genel Bakış)**

*   **Nedir? (What?)**: Metni kulağa doğal gelen konuşmaya dönüştüren (text-to-speech) bir hizmettir.
*   **Ne İşe Yarar? (Sınav İpucu)**: Yazılı metinleri (örn: makaleler, kitaplar) sesli hale getirir. Farklı dillerde ve seslerde onlarca seçenek sunar. Anahtar kelime: **Text-to-Speech**.

#### **Translate Overview (Translate'e Genel Bakış)**

*   **Nedir? (What?)**: Hızlı, yüksek kaliteli ve uygun maliyetli dil çevirisi sunan bir sinirsel makine çevirisi (neural machine translation) hizmetidir.
*   **Ne İşe Yarar? (Sınav İpucu)**: Metinleri bir dilden diğerine çevirir. Anahtar kelime: **Language Translation**.

#### **Lex + Connect Overview (Lex ve Connect'e Genel Bakış)**

*   **Nedir? (What?)**:
    *   **Amazon Lex**: Ses ve metin kullanarak uygulamalarda sohbete dayalı arayüzler (conversational interfaces - chatbots) oluşturmaya yönelik bir hizmettir. Amazon Alexa'yı güçlendiren teknolojinin aynısını kullanır.
    *   **Amazon Connect**: Bulutta, kullanımı kolay bir **iletişim merkezi (contact center)** hizmetidir.
*   **Ne İşe Yarar? (Sınav İpucu)**: **Lex**, chatbot'lar oluşturmak için kullanılır. **Connect** ise şirketlerin dakikalar içinde müşteri hizmetleri için bir çağrı merkezi kurmasını sağlar. Genellikle Lex, Connect içinde akıllı bir sanal asistan oluşturmak için kullanılır. Anahtar kelimeler: **Chatbot** (Lex), **Contact Center** (Connect).

#### **Comprehend Overview (Comprehend'e Genel Bakış)**

*   **Nedir? (What?)**: Metin içindeki içgörüleri ve ilişkileri bulmak için makine öğrenimini kullanan bir doğal dil işleme (NLP - Natural Language Processing) hizmetidir.
*   **Ne İşe Yarar? (Sınav İpucu)**: Bir metnin dilini, anahtar ifadelerini, yerlerini, kişilerini, markalarını ve hatta duygu durumunu (sentiment - pozitif/negatif/nötr) anlayabilir. Örneğin, sosyal medya yorumlarının genel olarak olumlu mu olumsuz mu olduğunu analiz etmek için kullanılır. Anahtar kelimeler: **NLP**, **Sentiment Analysis**.

#### **SageMaker AI Overview (SageMaker AI'a Genel Bakış)**

*   **Nedir? (What?)**: Geliştiricilerin ve veri bilimcilerin makine öğrenmesi (ML) modellerini hızlı bir şekilde oluşturmasını, eğitmesini ve dağıtmasını sağlayan tam yönetilen bir platformdur.
*   **Ne İşe Yarar? (Sınav İpucu)**: Makine öğrenmesi sürecinin tüm adımlarını (veri etiketleme, model oluşturma, eğitim, optimizasyon, dağıtım) tek bir çatı altında toplar. Bu, diğer AI servisleri gibi hazır bir çözüm sunmak yerine, kendi özel ML modellerinizi oluşturmanız için bir **platform** sağlar. Anahtar kelime: **Platform for building, training, and deploying ML models**.

#### **Kendra, Personalize, Textract Overview (Kendra, Personalize, Textract'e Genel Bakış)**

*   **Nedir? (What?)**:
    *   **Amazon Kendra**: Kurumlar için tasarlanmış, makine öğrenmesi destekli, akıllı bir **kurumsal arama (enterprise search)** hizmetidir.
    *   **Amazon Personalize**: Geliştiricilerin uygulamalarında kişiselleştirilmiş öneriler oluşturmasını kolaylaştıran bir makine öğrenmesi hizmetidir. Amazon.com'da kullanılan teknolojinin aynısıdır.
    *   **Amazon Textract**: Taranmış belgelerden, formlardan ve tablolardan metin, el yazısı ve verileri otomatik olarak çıkaran bir hizmettir.
*   **Ne İşe Yarar? (Sınav İpucu)**:
    *   **Kendra**: "Şirket içi belgelerimde doğal dilde arama yapmak istiyorum" -> Kendra.
    *   **Personalize**: "Kullanıcılarıma 'bunu alanlar bunu da aldı' gibi ürün önerileri sunmak istiyorum" -> Personalize.
    *   **Textract**: "PDF veya resim formatındaki bir faturadan tablo verilerini otomatik olarak çıkarmak istiyorum" -> Textract. Bu, basit OCR'dan (Optical Character Recognition) daha fazlasıdır çünkü belgenin yapısını (formlar, tablolar) anlar.

---

### **Bölüm 16: Account Management, Billing & Support (Hesap Yönetimi, Faturalandırma ve Destek)**

#### **Organizations Overview (Organizations'a Genel Bakış)**

*   **Nedir? (What?)**: Birden fazla AWS hesabını merkezi olarak yönetmenizi (govern) ve idare etmenizi (manage) sağlayan bir hizmettir.
*   **Neden Önemlidir? (Why?)**: Şirketlerin, farklı departmanlar veya projeler için oluşturdukları çok sayıda AWS hesabını tek bir yerden yönetmelerini sağlar.
*   **Nasıl Çalışır? (How?)**: Tüm hesapları bir "Organizasyon" altında toplarsınız. Bir ana hesap (management account) ve üye hesaplar (member accounts) bulunur. **Service Control Policies (SCPs)** kullanarak üye hesapların kullanabileceği AWS servislerini ve eylemlerini kısıtlayabilirsiniz.
*   **Sınav İpucu**: **Consolidated Billing (Birleştirilmiş Faturalandırma)**, Organizations'ın en önemli özelliklerinden biridir. Tüm üye hesapların faturaları ana hesapta toplanır. Bu, toplu kullanım indirimlerinden (volume discounts) faydalanmayı kolaylaştırır. **SCP'ler izin vermez, sadece kısıtlama yapar**. Bir kullanıcıya izin vermek için yine IAM kullanılmalıdır.

#### **AWS Control Tower Overview (Control Tower'a Genel Bakış)**

*   **Nedir? (What?)**: Güvenli, çok hesaplı bir AWS ortamı kurmanın ve yönetmenin en kolay yoludur.
*   **Neden Önemlidir? (Why?)**: AWS Organizations, IAM, Service Catalog gibi servisleri kullanarak, AWS'in en iyi pratiklerine dayalı bir temel (landing zone) oluşturma sürecini otomatikleştirir.
*   **Sınav İpucu**: "Çok hesaplı bir ortamı en iyi pratiklere göre hızlıca kurmak istiyorum" senaryosunun cevabı **Control Tower**'dır.

#### **Pricing Models of the Cloud (Bulutun Fiyatlandırma Modelleri)**

*   **Nedir? (What?)**: AWS'in temel fiyatlandırma felsefesini özetler:
    1.  **Pay as you go (Kullandığın kadar öde)**: Kullandığınız kaynaklar için saniye veya saat bazında ödeme yaparsınız.
    2.  **Save when you commit (Taahhüt edince tasarruf et)**: Reserved Instances veya Savings Plans gibi modellerle belirli bir kullanım için taahhüt vererek indirim alırsınız.
    3.  **Pay less by using more (Daha çok kullanarak daha az öde)**: Veri transferi ve depolama gibi bazı servislerde, kullanımınız arttıkça birim başına ödediğiniz ücret düşer (volume discounts).
*   **Sınav İpucu**: Bu üç temel prensibi bilmek önemlidir.

#### **Billing & Costing Tools Overview (Faturalandırma ve Maliyetlendirme Araçlarına Genel Bakış)**

*   **Nedir? (What?)**: AWS maliyetlerinizi anlamanıza, kontrol etmenize ve optimize etmenize yardımcı olan araçlardır.
    *   **AWS Cost Explorer**: Maliyet ve kullanım verilerinizi zaman içinde görselleştirmenizi, anlamanızı ve yönetmenizi sağlayan bir arayüzdür.
    *   **AWS Budgets**: Maliyetleriniz belirli bir eşiği aştığında sizi uyaran alarmlar kurmanızı sağlar.
    *   **AWS Cost and Usage Report (CUR)**: En detaylı maliyet ve kullanım verilerini içeren bir dosyadır. Genellikle analiz için kullanılır.
    *   **AWS Pricing Calculator**: AWS'de kurmayı planladığınız bir çözümün tahmini maliyetini hesaplamanızı sağlayan bir web aracıdır.
*   **Sınav İpucu**: "Gelecekteki bir projenin maliyetini tahmin etmek" -> **Pricing Calculator**. "Geçmiş maliyetlerimi detaylı olarak analiz etmek" -> **Cost Explorer**. "Maliyetlerim bütçeyi aşarsa uyarılmak" -> **AWS Budgets**.

#### **AWS Trusted Advisor**

*   **Nedir? (What?)**: AWS ortamınızı en iyi pratiklere göre inceleyen ve kaynaklarınızı optimize etmek için size gerçek zamanlı öneriler sunan bir çevrimiçi araçtır.
*   **Neden Önemlidir? (Why?)**: Beş ana kategoride öneriler sunar:
    1.  **Cost Optimization (Maliyet Optimizasyonu)**: Atıl EC2 instance'ları, boşta kalan EBS volümleri gibi gereksiz maliyetleri bulur.
    2.  **Performance (Performans)**: Yüksek kullanımlı EC2 instance'ları gibi performans darboğazlarını tespit eder.
    3.  **Security (Güvenlik)**: Herkese açık S3 bucket'ları, MFA'nın etkinleştirilmediği root hesabı gibi güvenlik açıklarını bildirir.
    4.  **Fault Tolerance (Hata Toleransı)**: Multi-AZ kullanılmayan RDS instance'ları, alınmamış EBS snapshot'ları gibi riskleri belirtir.
    5.  **Service Limits (Servis Limitleri)**: AWS hesap limitlerinize yaklaştığınızda sizi uyarır.
*   **Sınav İpucu**: Trusted Advisor, proaktif bir danışman gibidir. Özellikle **Maliyet Optimizasyonu** ve **Güvenlik** kategorilerindeki kontrolleri sınavda sıkça sorulur.

#### **Support Plans for AWS (AWS için Destek Planları)**

*   **Nedir? (What?)**: Farklı ihtiyaç seviyeleri için tasarlanmış AWS teknik destek paketleridir.
    *   **Basic**: Ücretsizdir, tüm hesaplarla gelir. Sadece faturalandırma ve hesap sorunları için destek alabilirsiniz.
    *   **Developer**: Teknik destek için e-posta ile erişim sağlar. İş saatleri içinde yanıt verilir.
    *   **Business**: 7/24 telefon, e-posta ve sohbet ile teknik destek sunar. Daha hızlı yanıt süreleri vardır. Trusted Advisor'ın tüm kontrollerine erişim sağlar.
    *   **Enterprise**: Business planındaki her şeye ek olarak, size özel bir **Teknik Hesap Yöneticisi (Technical Account Manager - TAM)** atanır. En hızlı yanıt sürelerini (kritik sorunlar için <15 dakika) sunar.
*   **Sınav İpucu**: Planlar arasındaki temel farkları (yanıt süreleri, iletişim kanalları, TAM varlığı) bilmek önemlidir. "Size özel bir danışman (TAM) hangi planda bulunur?" -> **Enterprise**.

---

### **Bölüm 17: Advanced Identity (Gelişmiş Kimlik)**

#### **Security Token Service (STS) Overview (STS'ye Genel Bakış)**

*   **Nedir? (What?)**: AWS kaynaklarına erişim için **geçici (temporary), sınırlı ayrıcalıklara sahip kimlik bilgileri** oluşturmanızı ve sağlamanızı sağlayan bir web hizmetidir.
*   **Neden Önemlidir? (Why?)**: IAM rollerinin arkasındaki temel teknolojidir. Bir kullanıcı veya uygulama bir rolü üstlendiğinde (assume role), STS onlara belirli bir süre (varsayılan 1 saat) için geçerli olan geçici güvenlik kimlik bilgileri (access key, secret key, session token) verir. Bu, uzun süreli anahtarlar kullanmaktan çok daha güvenlidir.
*   **Sınav İpucu**: Anahtar kelimeler: **Temporary Credentials**, **Assume Role**.

#### **Cognito Overview (Cognito'ya Genel Bakış)**

*   **Nedir? (What?)**: Web ve mobil uygulamalarınız için **kullanıcı kaydı (sign-up), oturum açma (sign-in) ve erişim kontrolü** sağlamayı kolaylaştıran bir hizmettir.
*   **Nasıl Çalışır? (How?)**: İki ana bileşeni vardır:
    *   **User Pools**: Uygulamanız için bir kullanıcı dizini (user directory) sağlar. Kullanıcıların e-posta/şifre ile kaydolmasını ve oturum açmasını yönetir.
    *   **Identity Pools**: Kullanıcılara (hem Cognito User Pools'daki kullanıcılar hem de Facebook, Google gibi sosyal medya sağlayıcıları üzerinden giriş yapanlar) AWS kaynaklarına erişmek için geçici kimlik bilgileri (STS aracılığıyla) sağlar.
*   **Sınav İpucu**: "Mobil uygulamama Facebook ile giriş (social login) özelliğini nasıl eklerim?" veya "Uygulama kullanıcılarımı yönetmek için bir servis arıyorum" senaryolarının cevabı **Cognito**'dur.

#### **AWS IAM Identity Center (formerly AWS SSO)**

*   **Nedir? (What?)**: Birden fazla AWS hesabına ve iş uygulamasına (örn: Salesforce, Office 365) **tek bir yerden oturum açma (Single Sign-On - SSO)** erişimini merkezi olarak yönetmeyi kolaylaştıran bir hizmettir.
*   **Neden Önemlidir? (Why?)**: Kullanıcıların, şirket içi Active Directory gibi mevcut kimlik kaynaklarındaki kimlik bilgileriyle AWS hesaplarına ve uygulamalarına erişmelerini sağlar. Her hesap için ayrı IAM kullanıcısı oluşturma ihtiyacını azaltır.
*   **Sınav İpucu**: Anahtar kelimeler: **Single Sign-On (SSO)**, **Centralized Access to Multiple Accounts**.

---

### **Bölüm 18: Other Services (Diğer Servisler)**

Bu bölüm, belirli bir kategoriye tam olarak girmeyen ancak AWS'in sunduğu çeşitli ve önemli hizmetleri kapsamaktadır.

*   **WorkSpaces Overview**
    *   **Nedir? (What?)**: Yönetilen, güvenli bir **Bulut Masaüstü (Desktop-as-a-Service - DaaS)** hizmetidir. Kullanıcılara internet üzerinden erişebilecekleri sanal bir Windows veya Linux masaüstü ortamı sunar.
    *   **Sınav İpucu**: Kullanıcılara tam bir sanal masaüstü deneyimi sunmak gerektiğinde kullanılır. "Uzaktan çalışanlar için sanal masaüstü sağlama" senaryosunun cevabı **WorkSpaces**'tir.

*   **AppStream 2.0 Overview**
    *   **Nedir? (What?)**: Masaüstü uygulamalarını herhangi bir bilgisayardaki bir web tarayıcısına güvenli bir şekilde aktaran (stream) tam yönetilen bir hizmettir.
    *   **Sınav İpucu**: WorkSpaces'ten farkı, tam bir masaüstü yerine **sadece belirli bir uygulamayı** (örn: 3D modelleme yazılımı, CAD programı) kullanıcıya sunmasıdır. Kullanıcıların yerel bilgisayarlarına uygulama kurma ihtiyacını ortadan kaldırır.

*   **IoT Core Overview**
    *   **Nedir? (What?)**: Milyarlarca bağlı cihazın (sensörler, akıllı cihazlar vb.) bulut uygulamaları ve diğer cihazlarla kolayca ve güvenli bir şekilde etkileşim kurmasını sağlayan yönetilen bir hizmettir.
    *   **Sınav İpucu**: "Nesnelerin İnterneti (IoT)" cihazlarını AWS'e bağlamak, yönetmek ve onlardan veri toplamak için kullanılan ana hizmettir.

*   **AppSync**
    *   **Nedir? (What?)**: **GraphQL API'leri** geliştirerek veri erişimini ve birleştirmeyi basitleştiren yönetilen bir hizmettir. Mobil ve web uygulamalarının birden fazla kaynaktan (DynamoDB, Lambda, diğer API'ler) veri çekmesini kolaylaştırır.
    *   **Sınav İpucu**: Soruda **GraphQL** anahtar kelimesi geçiyorsa, cevap **AppSync**'tir.

*   **Amplify**
    *   **Nedir? (What?)**: Güvenli ve ölçeklenebilir mobil ve web uygulamaları oluşturmak için bir geliştirme platformudur. Kimlik doğrulama, depolama, API'ler gibi arka uç (backend) özelliklerinin yapılandırılmasını basitleştirir.
    *   **Sınav İpucu**: "Mobil veya web uygulaması arka ucunu hızlıca kurmak ve yönetmek" için kullanılan bir araç setidir.

*   **AWS Application Composer**
    *   **Nedir? (What?)**: Sunucusuz (serverless) uygulamaların mimarisini görsel olarak tasarlamanızı ve oluşturmanızı sağlayan bir araçtır. Sürükle-bırak arayüzü ile Lambda, API Gateway, SQS gibi servisleri birbirine bağlayarak altyapı kodunu (CloudFormation) otomatik olarak üretir.
    *   **Sınav İpucu**: "Sunucusuz uygulamaları görsel olarak tasarlamak" için kullanılır.

*   **Device Farm Overview**
    *   **Nedir? (What?)**: Mobil uygulamalarınızı AWS tarafından barındırılan çok sayıda gerçek fiziksel telefonda ve tablette test etmenizi sağlayan bir uygulama test hizmetidir.
    *   **Sınav İpucu**: Uygulamanızın farklı cihazlarda, işletim sistemi sürümlerinde ve ekran boyutlarında nasıl çalıştığını test etmek için kullanılır. Anahtar kelime: **Mobile App Testing on Real Devices**.

*   **AWS Backup Overview**
    *   **Nedir? (What?)**: AWS hizmetlerindeki (EBS, RDS, DynamoDB, EFS vb.) ve şirket içi verilerinizi yedeklemeyi **merkezi olarak yönetmenizi ve otomatikleştirmenizi** sağlayan tam yönetilen bir hizmettir.
    *   **Sınav İpucu**: Farklı servislerin yedekleme işlemlerini tek bir yerden, ortak politikalarla yönetmek için kullanılır. Anahtar kelime: **Centralized Backup**.

*   **Disaster Recovery Strategies (Felaket Kurtarma Stratejileri)**
    *   **Nedir? (What?)**: Bir felaket durumunda iş sürekliliğini sağlamak için kullanılan, maliyet ve kurtarma süresine göre sıralanan yöntemlerdir: **Backup and Restore** (en ucuz, en yavaş), **Pilot Light**, **Warm Standby**, **Multi-site / Hot-Hot** (en pahalı, en hızlı).
    *   **Sınav İpucu**: Bu dört stratejiyi ve aralarındaki maliyet/kurtarma süresi (RTO/RPO) farkını bilmek önemlidir.
    *   Disaster Recovery Strategies (Felaket Kurtarma Stratejileri)
Felaket Kurtarma (DR) stratejileri, bir kesinti (doğal afet, siber saldırı, büyük sistem hatası vb.) durumunda iş sürekliliğini sağlamak ve operasyonları mümkün olan en kısa sürede geri yüklemek için kullanılan yaklaşımlardır. Bu stratejiler, belirlenen iki ana hedefe göre maliyet ve karmaşıklık açısından sıralanır:
RTO (Recovery Time Objective - Kurtarma Süresi Hedefi): Kesintiden sonra sistemlerin ne kadar sürede tekrar çalışır duruma gelmesi gerektiğini belirtir. Ne kadar hızlı?
RPO (Recovery Point Objective - Kurtarma Noktası Hedefi): Bir felaket anında ne kadarlık bir veri kaybını kabul edebileceğimizi gösterir. Ne kadar veri kaybedilebilir?
İşte maliyet ve hız sırasına göre temel DR stratejileri:
1. Backup and Restore (Yedekle ve Geri Yükle)
Açıklama: Verilerin düzenli olarak yedeklenmesi ve bir felaket durumunda bu yedeklerden geri yüklenmesidir.
Maliyet: En ucuz. Sadece yedek depolama maliyeti ve yedekleme mekanizması vardır.
Hız/Karmaşıklık: En yavaş/En yüksek RTO ve RPO. Geri yükleme işlemi zaman alıcı olabilir ve son yedeklemeden sonraki veriler kaybolur.
AWS Örnekleri: Amazon S3'te yedeklemek, AWS Backup hizmetini kullanmak.

2. Pilot Light (Kılavuz Işık)
Açıklama: Kritik olmayan sistemleri kapatıp sadece temel işlevsellik için gereken minimum kaynakları (veritabanı gibi) çalışır durumda tutmaktır. Bir felaket anında, geri kalan uygulama ve sunucular (bir "pilot ışık"tan tam bir ateşe dönüşmek gibi) hızlıca devreye alınır.
Maliyet: Düşük. DR bölgesi tam kapasite çalışmadığı için maliyet düşüktür.
Hız/Karmaşıklık: Orta. Yedekle-Geri Yükle'den daha hızlıdır çünkü veritabanı önceden senkronize edilmiştir ve bazı altyapı hazırdır.

3. Warm Standby (Sıcak Bekleme)
Açıklama: Üretim ortamının ölçeklendirilmiş, çalışan bir kopyasının DR bölgesinde sürekli hazır tutulmasıdır. Bu kopya, gelen trafiği karşılayacak kapasiteye tam olarak sahip değildir ancak bir felaket anında hızla ölçeklendirilebilir.
Maliyet: Orta-Yüksek. Pilot Light'tan daha pahalıdır çünkü daha fazla kaynak sürekli çalışır haldedir.
Hız/Karmaşıklık: Hızlı. RTO/RPO hedefleri düşüktür. Tamamen devreye alma süresi Pilot Light'tan daha kısadır.

4. Multi-site / Hot-Hot (Çoklu Bölge / Aktif-Aktif)
Açıklama: Üretim ortamının tam, ölçeklendirilmiş bir kopyasının başka bir AWS Bölgesinde (Region) aktif olarak çalıştırılmasıdır. Her iki bölge de trafiği aynı anda işleyebilir. Bir bölge çökerse, tüm trafik anında diğer bölgeye yönlendirilir.
Maliyet: En pahalı. Aynı anda iki tam kapasiteli ortam çalıştırmak demektir.
Hız/Karmaşıklık: En hızlı/En düşük RTO ve RPO. Kesinti süresi neredeyse sıfırdır (saniyeler mertebesinde). Uygulamalar yüksek erişilebilirlik (High Availability) ve DR sağlar.
AWS Örnekleri: Amazon Route 53 ile trafiği sağlıklı bölgeler arasında dağıtmak.

*   **AWS Elastic Disaster Recovery (DRS)**
    *   **Nedir? (What?)**: Şirket içi ve bulut tabanlı uygulamalarınızın AWS'e hızlı ve güvenilir bir şekilde kurtarılmasını sağlayan bir felaket kurtarma hizmetidir.
    *   **Sınav İpucu**: Kaynak sunucuları AWS'de düşük maliyetli bir bekleme alanına sürekli olarak çoğaltır (replicate). Bir felaket anında, uygulamalarınızı dakikalar içinde AWS üzerinde tam kapasiteyle başlatmanızı sağlar. **Pilot Light** stratejisini otomatikleştirmek için idealdir.

*   **AWS DataSync**
    *   **Nedir? (What?)**: Şirket içi depolama ile AWS depolama servisleri arasında **çevrimiçi (online)** veri aktarımını otomatikleştiren ve hızlandıran bir hizmettir.
    *   **Sınav İpucu**: Ağ üzerinden büyük miktarda veriyi hızlı ve güvenilir bir şekilde taşımak için kullanılır.

*   **Cloud Migration Strategies - The 7Rs (Bulut Taşıma Stratejileri - 7R)**
    *   **Nedir? (What?)**: Uygulamaları buluta taşırken izlenebilecek yedi yaygın stratejidir: **Rehost** (Lift-and-Shift), **Replatform** (Lift-and-Tinker), **Repurchase** (Drop-and-Shop), **Refactor/Re-architect**, **Retire**, **Retain**, **Relocate**.
    *   Strateji (R)	Açıklama	Ne Zaman Kullanılır?	Maliyet/Süre
1. Rehost	(Lift-and-Shift - Kaldır ve Taşı) Uygulamayı olduğu gibi, minimum değişiklik veya optimizasyon ile buluta taşımaktır.	Hızlı bir başlangıç gerektiğinde veya uygulamada kod değişikliği istenmediğinde.	Hızlı, en az maliyetli ilk adım.
2. Replatform	(Lift-and-Tinker - Kaldır ve Oynama) Uygulamanın temel mimarisi korunur ancak bazı bulut faydaları için optimizasyonlar yapılır (örneğin, şirket içi veritabanını AWS RDS'e geçirmek).	Bulutun yönetilen hizmetlerinden yararlanmak istendiğinde.	Rehost'tan daha fazla çaba gerektirir.
3. Repurchase	(Drop-and-Shop - Bırak ve Alışveriş Et) Lisanslı bir uygulamayı bırakıp yerine bulut tabanlı bir SaaS (Yazılım Hizmeti) çözümü (örneğin, CRM için Salesforce veya Office 365) almaktır.	Uygulamanın bakımı ve yönetimi dış kaynaklara devredilmek istendiğinde.	Uzun vadede operasyonel yükü en aza indirir.
4. Refactor / Re-architect	Uygulamanın bulutun yerel yeteneklerinden (Cloud Native) tam olarak yararlanması için kod ve mimarisini tamamen değiştirmek (örneğin, monolitik bir uygulamayı mikro hizmetlere dönüştürmek).	Uygulamanın ölçeklenebilirlik, esneklik ve inovasyon potansiyelini en üst düzeye çıkarmak için.	En yüksek çaba ve maliyet, ancak uzun vadede en büyük fayda.
5. Retire	Artık işe yaramayan ve buluta taşınmasına gerek olmayan uygulamaları kapatmak/devre dışı bırakmaktır.	Kaynak israfını önlemek ve taşıma kapsamını daraltmak için.	Anında maliyet tasarrufu sağlar.
6. Retain	Henüz buluta taşınamayacak veya taşınması mantıklı olmayan (yasal gereklilikler, çok yeni yatırım vb.) uygulamaları şirket içinde tutmaktır.	Henüz amorti edilmemiş donanım veya çok sıkı yasal kısıtlamalar olduğunda.	-
7. Relocate	Sadece VMware Cloud on AWS (VMC on AWS) ile ilgili bir stratejidir. Mevcut VMware iş yüklerini VMC on AWS'e taşımak, donanım değiştirme ihtiyacını ortadan kaldırır.	VMC ortamını korumak ve AWS'in altyapısından yararlanmak istendiğinde.
    *   **Sınav İpucu**: Bu stratejilerin ne anlama geldiğini temel düzeyde bilmek faydalıdır. En yaygın olanı, uygulamayı olduğu gibi buluta taşımak anlamına gelen **Rehost**'tur.

*   **Application Discovery Service & Application Migration Service (MGN)**
    *   **Nedir? (What?)**:
        *   **Application Discovery Service**: Şirket içi sunucularınız hakkında bilgi (performans, bağımlılıklar vb.) toplayarak taşıma planlamanıza yardımcı olur.
        *   **Application Migration Service (MGN)**: **Rehost (Lift-and-Shift)** stratejisi için önerilen birincil taşıma hizmetidir. Şirket içi sunucuları minimum kesintiyle AWS'e taşımayı otomatikleştirir.
    *   **Sınav İpucu**: "Sunucuları olduğu gibi AWS'e taşımak" için **Application Migration Service (MGN)** kullanılır.

*   **AWS Migration Evaluator**
    *   **Nedir? (What?)**: Mevcut şirket içi iş yüklerinizi AWS'de çalıştırmanın tahmini maliyetini hesaplayarak bir taşıma kararı vermenize yardımcı olan ücretsiz bir hizmettir.
    *   **Sınav İpucu**: Taşıma öncesi **maliyet tahmini** yapmak için kullanılır.

*   **AWS Migration Hub**
    *   **Nedir? (What?)**: Birden fazla AWS ve iş ortağı taşıma aracından gelen taşıma ilerlemesini **tek bir merkezi yerden izlemenizi** sağlayan bir hizmettir.
    *   **Sınav İpucu**: Taşıma projeleriniz için bir "kontrol paneli" (dashboard) görevi görür.

*   **AWS Fault Injection Simulator (FIS)**
    *   **Nedir? (What?)**: AWS'deki uygulamalarınız üzerinde kontrollü deneyler yaparak, sistemlerinizin beklenmedik durumlara (örn: bir sunucunun çökmesi, ağ gecikmesi) nasıl tepki verdiğini test etmenizi sağlayan bir hizmettir.
    *   **Sınav İpucu**: Bu, **Kaos Mühendisliği (Chaos Engineering)** pratiğini uygulamak için kullanılır. Amacı, sistemin zayıf noktalarını üretimde bir sorun yaşanmadan önce bulmaktır.

*   **Step Functions**
    *   **Nedir? (What?)**: Birden fazla AWS hizmetini (Lambda, SQS, SNS vb.) içeren dağıtık uygulamaları ve mikroservisleri görsel iş akışları (workflows) olarak koordine etmenizi sağlayan sunucusuz bir orkestrasyon hizmetidir.
    *   **Sınav İpucu**: Karmaşık bir sürecin adımlarını (örn: video işleme, sipariş tamamlama) sıralamak, dallandırmak ve yönetmek için kullanılır.

*   **Ground Station**
    *   **Nedir? (What?)**: Uydularla iletişim kurmak için tam yönetilen bir yer istasyonu ağıdır. Uydu verilerini AWS'e indirmenizi sağlar.
    *   **Sınav İpucu**: Çok niş bir hizmettir. Soruda **uydu (satellite)** geçiyorsa, cevap **Ground Station**'dır.

*   **AWS Pinpoint**
    *   **Nedir? (What?)**: Müşterilerle etkileşim kurmak için kullanılan bir dijital pazarlama iletişim hizmetidir. E-posta, SMS, anlık bildirim (push notification) gibi kanallar üzerinden hedefli kampanyalar göndermenizi sağlar.
    *   **Sınav İpucu**: "Uygulama kullanıcılarına hedefli anlık bildirimler göndermek" gibi pazarlama senaryoları için kullanılır.

---

### **Bölüm 19: AWS Architecting & Ecosystem (AWS Mimarisi ve Ekosistemi)**

Bu bölüm, AWS'de sağlam ve verimli sistemler kurmanıza yardımcı olan çerçeveleri, araçları ve topluluk kaynaklarını kapsar.

*   **AWS Well-Architected Framework**
    *   **Nedir? (What?)**: Bulutta en iyi mimarileri oluşturmak için AWS tarafından geliştirilmiş bir dizi en iyi pratik ve yol gösterici prensiptir. **Altı temel sütundan (Pillar)** oluşur.
    *   **Sınav İpucu**: Bu altı sütunu ve ne anlama geldiklerini mutlaka bilmelisiniz:
        1.  **Operational Excellence (Operasyonel Mükemmellik)**
        2.  **Security (Güvenlik)**
        3.  **Reliability (Güvenilirlik)**
        4.  **Performance Efficiency (Performans Verimliliği)**
        5.  **Cost Optimization (Maliyet Optimizasyonu)**
        6.  **Sustainability (Sürdürülebilirlik)**

*   **AWS Well-Architected Tool**
    *   **Nedir? (What?)**: AWS konsolunda bulunan ve iş yüklerinizi Well-Architected Framework'ün en iyi pratiklerine göre değerlendirmenizi sağlayan ücretsiz bir araçtır.
    *   **Sınav İpucu**: Size bir dizi soru sorar ve cevaplarınıza göre mimarinizin güçlü ve zayıf yönlerini belirleyerek iyileştirme önerileri sunar.

*   **AWS Customer Carbon Footprint Tool**
    *   **Nedir? (What?)**: AWS kullanımınızla ilişkili karbon emisyonlarını ölçmenizi ve raporlamanızı sağlayan bir araçtır.
    *   **Sınav İpucu**: **Sustainability (Sürdürülebilirlik)** sütunu ile doğrudan ilişkilidir. Şirketlerin çevresel etki hedeflerini takip etmelerine yardımcı olur.

*   **AWS Cloud Adoption Framework (CAF)**
    *   **Nedir? (What?)**: Kuruluşların buluta geçiş süreçlerini hızlandırmak için kapsamlı bir rehberlik sunan bir çerçevedir. İş, İnsan, Yönetişim, Platform, Güvenlik ve Operasyonlar gibi farklı perspektifleri ele alır.
    *   **Sınav İpucu**: Well-Architected Framework teknik mimariye odaklanırken, **CAF** buluta geçişin **iş ve organizasyonel yönlerine** odaklanır.

*   **Right Sizing (Doğru Boyutlandırma)**
    *   **Nedir? (What?)**: Bir iş yükünün performans ve kapasite gereksinimlerini karşılayan en düşük maliyetli kaynakları seçme pratiğidir.
    *   **Sınav İpucu**: **Cost Optimization (Maliyet Optimizasyonu)** sütununun temel bir konseptidir. AWS Cost Explorer ve Trusted Advisor gibi araçlar doğru boyutlandırma önerileri sunabilir.

*   **AWS Ecosystem (AWS Ekosistemi)**
    *   **Nedir? (What?)**: AWS'in kendi servislerinin yanı sıra, müşterilere yardımcı olan iş ortakları (APN), yazılım satıcıları (Marketplace) ve danışmanlık hizmetlerini (Professional Services) içeren geniş bir yapıdır.
    *   **Sınav İpucu**: AWS'in tek başına bir platform olmadığını, geniş bir destekleyici topluluk ve iş ortağı ağına sahip olduğunu anlamak önemlidir.

*   **AWS IQ & re:Post**
    *   **Nedir? (What?)**:
        *   **AWS IQ**: Müşterilerin, küçük veya büyük projeler için AWS Sertifikalı üçüncü taraf uzmanları bulup onlarla çalışmasını sağlayan bir platformdur.
        *   **AWS re:Post**: AWS tarafından yönetilen, AWS ile ilgili teknik sorularınızı sorabileceğiniz ve topluluktan ve AWS uzmanlarından cevaplar alabileceğiniz bir **soru-cevap (Q&A)** hizmetidir.
    *   **Sınav İpucu**: **re:Post**, eski AWS Forumlarının yerini almıştır ve topluluk tabanlı teknik destek için birincil kaynaktır.

*   **AWS Knowledge Center**
    *   **Nedir? (What?)**: AWS müşterilerinin sıkça sorduğu sorulara ve karşılaştığı sorunlara yönelik AWS uzmanları tarafından hazırlanmış makaleler ve video kılavuzları içeren bir kütüphanedir.
    *   **Sınav İpucu**: Bir sorunla karşılaştığınızda veya bir konuyu öğrenmek istediğinizde başvurabileceğiniz, pratik çözümler sunan bir kaynaktır.

*   **AWS Managed Services (AMS)**
    *   **Nedir? (What?)**: AWS altyapınızı sizin adınıza işleten bir hizmettir. Yamalama, yedekleme, izleme gibi operasyonel görevleri üstlenir ve altyapınızın en iyi pratiklere uygun ve güvenli kalmasını sağlar.
    *   **Sınav İpucu**: Kendi operasyon ekibini kurmak istemeyen veya bu konuda uzmanlığı olmayan şirketler için "anahtar teslim" bir altyapı yönetimi çözümü sunar.

