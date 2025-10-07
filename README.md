# 1- Modern Yazılım Geliştirme Pratikleri

## Git Nedir? GitHub Nedir?
Git: Bir kontrol sistemidir. Sistemin anlık görüntüsünü kaydeder ve değişiklik durumunda eski haline referans verir.<br>
GitHub : Git ile yönetilen projeleri internet üzerinde depolamana ve paylaşmana yarayan bir platformdur.

## Temel Git Komutları
1- init : Yeni bir proje başlatır.<br>
2- clone : Başka bir projeyi kopyalar.<br>
3- add : Yapılan değişiklikleri kalıcı hale getirmeden önce sıraya ekler.<br>
4- commit : Yapılan değişiklikleri kalıcı hale getirir.<br>
5- push : Kalıcı değişiklikleri GitHub projesine gönderir.<br>
6- pull : GitHub'daki son değişiklikleri indirir ve yerel projeye ekler.<br>
7- branch : Yeni bir dal(branch) oluşturur veya mevcut dalları listeler.<br>
8- merge : Bir dalda yapılan değişiklikleri başka bir dal ile birleştirir.

## CI/CD Nedir?
CI/CD (Continuous Integration / Continuous Deployment), yazılım geliştirme sürecinde kodun otomatik olarak derlenmesini, test edilmesini ve dağıtılmasını sağlayan bir yaklaşımdır.<br>
  * CI (Continuous Integration): Geliştiricilerin kodlarını sık sık entegre edip otomatik testlerle doğrulamasıdır.<br>
  * CD (Continuous Deployment): Başarılı testlerden sonra kodun otomatik olarak üretim ortamına aktarılmasıdır.

## .NET Projesi için CI/CD
Bir .NET projesinde CI/CD genellikle GitHub Actions veya Azure DevOps Pipelines ile yapılır.<br>
Bu sistemler dotnet restore, dotnet build, dotnet test, dotnet publish komutlarını sırayla çalıştırarak:<br>
1- Kodun bağımlılıklarını yükler.<br>
2- Derler.<br>
3- Test eder.<br>
4- Yayınlanabilir çıktıyı oluşturur.<br>
5- Azure, IIS veya Docker ortamına otomatik olarak dağıtır.

## Software Development Life Cycle (SDLC)
Yazılım geliştirme yaşam döngüsü (SDLC), geliştirme ekiplerinin yüksek kaliteli yazılımlar tasarlamak ve oluşturmak için kullandığı uygun maliyetli ve zaman açısından verimli bir süreçtir. SDLC'nin amacı, üretim sırasında ve sonrasında müşteri beklentilerini karşılamak için ileriye dönük planlamayla proje risklerini en aza indirmektir. Bu döngü belirli adımlar üzerine gerçekleştirilir.

## SLDC Nasıl Çalışır? 
1- Planlama <br>
Planlama aşaması maliyet-fayda analizi, zamanlama, kaynak tahmini ve tahsis gibi görevleri içerir. Geliştirme ekibi, bir yazılım gereksinimi teknik özellikleri belgesi oluşturmak için müşteriler, dahili ve harici uzmanlar ve yöneticiler gibi çeşitli paydaşlardan gereksinimleri toplar. Bu belge, beklentileri belirler ve proje planlamasına yardımcı olan ortak hedefleri tanımlar. Ekip maliyetleri tahmin eder, bir program oluşturur. <br>

2- Tasarım <br>
Tasarım aşamasında, yazılım mühendisleri gereksinimleri analiz eder ve yazılımı oluşturmaya ilişkin en iyi çözümleri belirler. Örneğin, önceden var olan modülleri entegre etmeyi düşünebilir, teknoloji seçimleri yapabilir ve geliştirme araçlarını belirleyebilirler. <br>

3- Uygulama <br>
Uygulama aşamasında, geliştirme ekibi ürünü kodlar. Nihai sonuca ulaşmak için günlük olarak yapabilecekleri daha küçük kodlama görevlerini belirlemek için gereksinimleri analiz ederler.<br>

4- Test Etme <br>
Test aşamasında, yazılımda hata olup olmadığını kontrol etmek için otomasyon ile manuel testler birleştirilir. Kalite analizi, yazılımı hatalara karşı test etmeyi ve yazılımın müşteri gereksinimlerini karşılayıp karşılamadığını kontrol etmeyi içerir.<br>

5- Dağıtım <br>
Dağıtım aşamasında, ürünün son kopyası kullanıcıya verirlir. Bu kopya sistemden ayrıdır ve böylece sistem gelişmeye veya değişmeye devam ederken kullanıcı bu değişikliklerden etkilenmez. Dağıtım aşaması; paketleme, ortam yapılandırması ve kurulum gibi en son oluşturma kopyasını üretim ortamına taşımaya ilişkin çeşitli görevler içerir. <br>

6- Bakım <br>
Bakım aşamasında, diğer görevlerin yanı sıra hatalar düzeltilir, müşteri sorunları çözülür ve yazılım değişiklikleri yönetilir. Ek olarak, mevcut yazılımı iyileştirmenin yeni yollarını belirlemek için genel sistem performansını, güvenliğini ve kullanıcı deneyimini de izlenir.

# 2- .NET Ekosistemi

## .NET Nedir? Neden Kullanılır?
.NET, Microsoft tarafından geliştirilen bir uygulama geliştirme platformudur. C#, VB.NET ve F# gibi dillerle masaüstü, web, mobil, oyun ve bulut uygulamaları geliştirmeyi sağlar.<br>

| Özellik         | .NET Framework            | .NET Core                              | .NET 7/8+                   |
| --------------- | ------------------------- | -------------------------------------- | --------------------------- |
| **Yıl**         | 2002                      | 2016                                   | 2022–2024                   |
| **Platform**    | Sadece Windows            | Cross-platform (Windows, Linux, macOS) | Tek birleşik .NET platformu |
| **Açık Kaynak** | Hayır                     | Evet                                   | Evet                        |
| **Performans**  | Orta                      | Yüksek                                 | Çok yüksek                  |
| **Kapsam**      | Eski Windows uygulamaları | Web, API, microservice                 | Web, API, mobil, bulut, IoT |
| **Durum**       | Artık güncellenmiyor      | Yerini .NET 7/8 aldı                   | En güncel sürümler          |

## "dotnet --info" Örneği
```bash
C:\>dotnet --info
```
```yaml
.NET SDK:
 Version:           9.0.302
 Commit:            bb2550b9af
 Workload version:  9.0.300-manifests.183aaee6
 MSBuild version:   17.14.13+65391c53b

Çalışma Zamanı Ortamı:
 OS Name:     Windows
 OS Version:  10.0.26100
 OS Platform: Windows
 RID:         win-x64
 Base Path:   C:\Program Files\dotnet\sdk\9.0.302\

.NET iş yükleri yüklendi:
Görüntülenecek yüklü iş yükü yok.
Yeni bildirimler yüklenirken loose manifests kullanılacak şekilde yapılandırıldı.

Host:
  Version:      9.0.7
  Architecture: x64
  Commit:       3c298d9f00

.NET SDKs installed:
  8.0.403 [C:\Program Files\dotnet\sdk]
  9.0.302 [C:\Program Files\dotnet\sdk]

.NET runtimes installed:
  Microsoft.AspNetCore.App 8.0.10 [C:\Program Files\dotnet\shared\Microsoft.AspNetCore.App]
  Microsoft.AspNetCore.App 8.0.18 [C:\Program Files\dotnet\shared\Microsoft.AspNetCore.App]
  Microsoft.AspNetCore.App 9.0.7 [C:\Program Files\dotnet\shared\Microsoft.AspNetCore.App]
  Microsoft.NETCore.App 6.0.16 [C:\Program Files\dotnet\shared\Microsoft.NETCore.App]
  Microsoft.NETCore.App 8.0.10 [C:\Program Files\dotnet\shared\Microsoft.NETCore.App]
  Microsoft.NETCore.App 8.0.13 [C:\Program Files\dotnet\shared\Microsoft.NETCore.App]
  Microsoft.NETCore.App 8.0.18 [C:\Program Files\dotnet\shared\Microsoft.NETCore.App]
  Microsoft.NETCore.App 9.0.7 [C:\Program Files\dotnet\shared\Microsoft.NETCore.App]
  Microsoft.WindowsDesktop.App 8.0.10 [C:\Program Files\dotnet\shared\Microsoft.WindowsDesktop.App]
  Microsoft.WindowsDesktop.App 8.0.18 [C:\Program Files\dotnet\shared\Microsoft.WindowsDesktop.App]
  Microsoft.WindowsDesktop.App 9.0.7 [C:\Program Files\dotnet\shared\Microsoft.WindowsDesktop.App]

Other architectures found:
  x86   [C:\Program Files (x86)\dotnet]
    registered at [HKLM\SOFTWARE\dotnet\Setup\InstalledVersions\x86\InstallLocation]

Environment variables:
  Not set

global.json file:
  Not found

Learn more:
  https://aka.ms/dotnet/info

Download .NET:
  https://aka.ms/dotnet/download
```
## "dotnet --info" ile Neler Görülüyor?
1. **\.NET SDK (reflecting any global.json)**
    * Aktif SDK sürümü ve commit bilgisini gösterir.
    * **Version:** Aktif .NET SDK sürümü
    * **Commit:** SDK’nın kaynak kod commit ID’si

2. **Runtime Environment**
    * Çalıştığın işletim sistemi ve ortam bilgilerini verir:
    * **OS Name / OS Version / OS Platform:** İşletim sistemi bilgisi
    * **RID (Runtime Identifier):** Platform için benzersiz kimlik (örn. win-x64)
    * **Base Path:** SDK’nın kurulu olduğu dizin

3. **Host**
    * .NET runtime’ın ana sürümü ve commit ID’si.
    * Hata veya destek durumlarında kullanılabilir.

4. **\.NET SDKs installed**
    * Sistemde yüklü tüm SDK sürümleri listelenir.

5. **\.NET runtimes installed**
    * Sistemde yüklü tüm .NET runtime sürümleri listelenir.

## Senkron/Asenkron İşlemler

1. **Senkron (Synchronous)**
    * İşlemler sırayla ve birbirini bekleyerek çalışır. Bir işlem bitmeden diğeri başlamaz.

2. **Asenkron (Asynchronous)**
    * İşlemler bağımsız olarak çalışır. Bir işlem beklerken diğer işlemler devam edebilir.

### Senkron İşlem
```yaml
public void SiparisVer(Siparis siparis)
{
    StokKontrolEt(siparis);           // 2 sn bekle
    OdemeAl(siparis);                 // 3 sn bekle
    FaturaOlustur(siparis);           // 1 sn bekle
    KargoHazirla(siparis);            // 4 sn bekle
    MusteriMailGonder(siparis);       // 2 sn bekle
    
    // TOPLAM: 12 saniye - Kullanıcı ekranda bekliyor! 
}
```
### Asenkron İşlem
```yaml
public async Task SiparisVerAsync(Siparis siparis)
{
    await StokKontrolEtAsync(siparis);     // 2 sn
    await OdemeAlAsync(siparis);            // 3 sn
    
    // Bu işlemler paralel çalışabilir
    var faturaTask = FaturaOlusturAsync(siparis);
    var kargoTask = KargoHazirlaAsync(siparis);
    var mailTask = MusteriMailGonderAsync(siparis);
    
    await Task.WhenAll(faturaTask, kargoTask, mailTask);
    
    // TOPLAM: ~9 saniye - Kullanıcı daha az bekler! 
}
```

# 3- Backend Geliştirme Temelleri

## HTTP Metotları ve Örnekleri

1- GET  <br>
Sunucudan veri almak için kullanılır.
Veriyi sadece okur, hiçbir şeyi değiştirmez.

### Request ###
```bash
GET https://api.example.com/users
```

### Response ###
```bash
[
  { "id": 1, "name": "Ahmet Yusuf" },
  { "id": 2, "name": "Zeynep" }
]

```

2- POST  <br>
Sunucuya yeni veri göndermek / eklemek için kullanılır.
Veri, isteğin gövdesinde (body) gönderilir.

### Request ###
```bash
POST https://api.example.com/users
Content-Type: application/json

{
  "name": "Mehmet",
  "email": "mehmet@example.com"
}
```

### Response ###
```bash
{
  "id": 3,
  "name": "Mehmet",
  "email": "mehmet@example.com",
  "message": "Kullanıcı başarıyla eklendi."
}

```

3- PUT  <br>
Var olan bir veriyi tamamen güncellemek için kullanılır.
Gönderilen veri, eski kaydın yerini alır.

### Request ###
```bash
PUT https://api.example.com/users/3
Content-Type: application/json

{
  "name": "Mehmet Ali",
  "email": "mehmetal@example.com"
}

```

### Response ###
```bash
{
  "id": 3,
  "name": "Mehmet Ali",
  "email": "mehmetal@example.com",
  "message": "Kullanıcı bilgileri güncellendi."
}

```

4- DELETE  <br>
Sunucudaki belirli bir veriyi silmek için kullanılır.

### Request ###
```bash
DELETE https://api.example.com/users/3

```

### Response ###
```bash
{
  "message": "Kullanıcı (ID: 3) başarıyla silindi."
}

```

## API Türleri ve Farkları ##

1. REST (Representational State Transfer)
    * HTTP protokolü üzerinde çalışır.
    * Kaynaklar (resources) URL’lerle tanımlanır.
    * İşlemler için HTTP metodları (GET, POST, PUT, DELETE...) kullanılır.
    * Veriler genellikle JSON formatında döner.
    * “Stateless” (durumsuz) bir mimaridir — her istek bağımsızdır.
      
2. SOAP (Simple Object Access Protocol)
    * XML tabanlı iletişim protokolüdür.
    * REST’e göre daha katı ve standartlaştırılmıştır.
    * HTTP dışında da (örneğin SMTP, TCP) çalışabilir.
    * Güvenlik, kimlik doğrulama, hata yönetimi gibi konular için WS- standartlarını* kullanır.
    * Genelde kurumsal sistemlerde (bankacılık, sigorta, ERP) tercih edilir.
      
3. GraphQL
    * Facebook tarafından geliştirildi (2015).
    * İstemci (client), tam olarak hangi alanları istediğini söyler.
    * Tek bir endpoint üzerinden çalışır (örn. /graphql).
    * Veri formatı: JSON
    * Gereksiz veri transferini önler (REST’e göre daha optimize).

### Karşılaştırma ###
| Özellik                 | **REST**                      | **SOAP**                 | **GraphQL**                  |
| ----------------------- | ----------------------------- | ------------------------ | ---------------------------- |
| **Veri Formatı**        | JSON, XML                     | XML                      | JSON                         |
| **Çalışma Prensibi**    | HTTP üzerinden kaynak tabanlı | XML tabanlı protokol     | Tek endpoint, sorgu tabanlı  |
| **Performans**          | Hızlı                         | Ağır / yavaş             | Çok hızlı (isteğe göre veri) |
| **Karmaşıklık**         | Basit                         | Karmaşık                 | Orta                         |
| **Güvenlik**            | HTTPS ile sağlanır            | WS-Security standartları | HTTPS ile sağlanır           |
| **Kullanım Alanı**      | Web & mobil API’ler           | Kurumsal sistemler       | Modern, dinamik frontend’ler |
| **Endpoint Sayısı**     | Her kaynak için farklı        | Tek endpoint             | Tek endpoint                 |
| **Örnek Cevap Formatı** | JSON                          | XML                      | JSON                         |
| **Kullanım Kolaylığı**  | Çok kolay                     | Zor                      | Orta                         |
| **Standartlaştırma**    | Esnek                         | Yüksek düzeyde standart  | Esnek                        |

## JSON Verisi 

```yaml
{
  "status": "success",
  "message": "Kullanıcı başarıyla eklendi.",
  "data": {
    "id": 4,
    "name": "Ali Veli",
    "email": "ali@example.com",
    "createdAt": "2025-10-06T11:25:00Z"
  }
}
```
Bu bir JSON nesnesidir ve içerisinde anahtar-değer çiftleri bulundurur. Bu değerler sırasıyla status, message ve data değerleridir.<br>
### status ###
  * Bu alan api isteiğinin durumunu belirtir. Burada başarılı(success) veya hata(error) gibi değerler olabilmektedir.
### message ### 
  * Bu kısım insan okuyucu içindir.
  * Çoğu zaman geliştiriciye bazen de kullanıcıya geri bildirim vermek için kullanılır.
  * Hatanın sebebini veya işlem sonucunu anlatır. 
### data ### 
  * Bu kısım asıl veriyi içerir.
  * data genellikle bir nesne (object) ya da bazen dizi (array) olur.
  * Burada API bize oluşturulan kullanıcı nesnesini döndürüyor.

# 4- ASP.NET
### ASP.NET Nedir? ###
 * ASP.NET, Microsoft tarafından geliştirilmiş bir web uygulama geliştirme framework’üdür.
 * İlk olarak 2002 yılında çıktı ve .NET Framework üzerinde çalışır.
 * Yani sadece Windows işletim sisteminde çalışır. 

### ASP.NET Core Nedir? ### 
 * ASP.NET Core, Microsoft’un 2016’da yayınladığı yenilenmiş ve açık kaynaklı (open-source) sürümüdür.
 * Tamamen sıfırdan yazılmıştır.
 * ASP.NET Core, .NET Core veya .NET 5+ platformu üzerinde çalışır.

### .NET vs .NET Core ###
| Özellik                     | ASP.NET (.NET Framework)            | ASP.NET Core                                                |
| --------------------------- | ----------------------------------- | ----------------------------------------------------------- |
|  **Platform**             | Sadece Windows                      | Windows, Linux, macOS (Cross-platform)                        |
|  **Performans**           | Daha yavaş, eski mimari             | Çok hızlı, optimize edilmiş Kestrel web server                |
|  **Modülerlik**           | System.Web bağımlı (monolitik)      | Modüler, sadece gereken paketler yüklenir                     |
|  **Web Server**           | IIS (Internet Information Services) | Kestrel (yerleşik), istenirse IIS/Nginx/Apache ile birlikte   |
|  **Proje Yapısı**         | MVC, Web API ayrı projeler          | MVC + Web API + Razor Pages tek çatı altında                  |
|  **Dependency Injection** | Harici kütüphane gerekir            | Yerleşik DI desteği                                           |
|  **Açık Kaynak**          | Kapalı kaynak                       | Tamamen açık kaynak (GitHub’da)                               |
|  **Bulut Uyumluluğu**     | Kısıtlı                             | Azure ve diğer cloud servislerle uyumlu                       |
|  **Sürüm**                | .NET Framework 4.x                  | .NET 6, .NET 7, .NET 8 (en yeni sürümler)                     |

## MVC Nedir? ##
MVC, yazılım geliştirmede kullanılan bir mimari tasarım desenidir. Uygulamanın farklı sorumluluklarını üç ana bileşene ayırarak kod organizasyonunu ve bakımını kolaylaştırır.
### 1- Model (M) ###
Ne işe yarar? Uygulamanın veri ve iş mantığını yönetir.

### View (V) ###
Ne işe yarar? Kullanıcıya gösterilen arayüzü oluşturur.

### Controller (C) ###
Ne işe yarar? Model ve View arasında köprü görevi görür.

```yaml
          Kullanıcı (Tarayıcı)
                 │
                 │ 1️- HTTP isteği gönderir (örneğin: /User/Details/1)
                 ▼
        ┌──────────────────────────┐
        │      Controller          │
        │ (örnek: UserController)  │
        └──────────────────────────┘
                 │
                 │ 2️- İstek verisini işler
                 │ 3️- Gerekirse Model üzerinden veritabanına erişir
                 ▼
        ┌──────────────────────────┐
        │         Model            │
        │ (veritabanı, entity,     │
        │  iş mantığı, data access)│
        └──────────────────────────┘
                 │
                 │ 4️- Veriyi geri döndürür
                 ▼
        ┌──────────────────────────┐
        │      Controller          │
        └──────────────────────────┘
                 │
                 │ 5️- Veriyi View’e yollar
                 ▼
        ┌──────────────────────────┐
        │          View            │
        │ (HTML, Razor, UI)        │
        └──────────────────────────┘
                 │
                 │ 6️- Kullanıcıya sayfa olarak döner
                 ▼
          Kullanıcı (Tarayıcı)

```

## MVC mimarisi Kullanım Amaçları ##
1. Kaygıların Ayrılması(Separation of Concerns)
   * Her katman kendi işine odaklanır, İşler karışmaz.
2. Bakım Kolaylığı
   * Kodlar anlaşılır
   * Hataları bulmak kolaydır
   * Kod parçaları birbirinden izoledir
3. Takım Çalışması
   * Frontend developer view üzerinde çalışırken, backend developer model ve controller üzerinde çalışırlar ve birbirlerni engellemezler.
4. Test Edilebilirlik
   * Kodlar izole halde olduğundan test eilebilirlik kolaylaşır
5. Yeniden Kullanılabilirlik
   * Aynı model farklı view'lerde kullanılabilir

## Middleware Nedir?
Middlware, bir programda istek(request) ve cevap(response) arasında yapılan kontrol işlem birimleirdir. Burada giriş yetkisi, erişim yetkisi veya gereksinime özel yapılacak kontrol işlemleri yapılır ve en sonunda cevap oluşturulur. Cevap oluştuktan sonra her middleware tersten bir sıra ile çalışır. Middleware'lar belirli bir sıra ile çalışırlar. Bu sebeple middleware yapılarının program.cs veya startup.cs içerisindeki sıralaması önemlidir. Aksi durumda beklenmeyen hatalar oluşur. 
 * Örneğin; giriş yetkisinden önce erişim yetkisi kontrol edilmesi durumunda sisteme giriş izni olmayan birinin erişimi yapılmış olur.
 * Başka bir örnek olarak; hata kontrolü yapılmadan önce diğer kontroller yapılırsa hata uygulama çöker.

```yaml
 HTTP Request (Kullanıcıdan gelen istek)
        │
        ▼
 ┌──────────────────────────────┐
 │ Middleware 1 (Logging)       │ → isteği loglar
 └──────────────────────────────┘
        │
        ▼
 ┌──────────────────────────────┐
 │ Middleware 2 (Authentication)│ → kullanıcıyı doğrular
 └──────────────────────────────┘
        │
        ▼
 ┌──────────────────────────────┐
 │ Middleware 4 (Authorization) │ → kullanıcının erişim yetkisini doğrular
 └──────────────────────────────┘
        │
        ▼
 ┌──────────────────────────────┐
 │ Middleware 5 (Routing)       │ → hangi Controller'a gideceğine karar verir
 └──────────────────────────────┘
        │
        ▼
      Controller / Endpoint
        │
        ▼
 ┌──────────────────────────────────┐
 │ Response geri döner              │
 │ (middleware’ler tersten çalışır) │
 └──────────────────────────────────┘
        │
        ▼
 HTTP Response (Kullanıcıya dönen cevap)

```
## Bağımlılık Enjeksiyonu(Dependency Injection) Nedir?
Bağımlılık iki parçanın birbirine doğrudan bağlanmasıyla ve bu bağlanmanın sonucunda bir parçadaki değişimin diğer parçayı etkilemesiyle oluşur. Bağımlılık enjeksiyonu, birbiriyle bağımlılık oluşturan parçaların birbirinden ayrılarak dolaylı yollardan birbirleriyle haberleştirilmesidir. Örnek olarak;
   * Birbirinden farklı 3 sınıf A,B,C olsun. İlk durumda A sınıfında herhangi bir noktada B sınıfının bir nesnesi çağırılırsa bu durumda A sınıfı B sınıfına bağımlı olur. Bunun sebebi şudur: eğer A sınıfının ihtiyacının B yerine C olması halinde kaynak kodda değişim yapılması gerekir.
   * Ancak A sınıfı doğrudan B veya C sınıflarını kullanmak yerine B ve C sınıflarının çağıracak farklı bir çağırıcı kullanır ise, B veya C sınıflarından birine ihtiyacı değişirse veya B ve C sınıflarının yapıları değişirse, Asınıfında değişiklik yapılmak durumunda kalınmayacağından bağımlılık azaltılmış, enjekte edilmiş olur.

## Katmanlı Mimari ##

Katmanlı mimari, yazılım sistemlerini ayrı sorumluluklara sahip katmanlara bölerek tasarlama yaklaşımıdır. Amaç, kodun okunabilirliğini, sürdürülebilirliğini ve test edilebilirliğini artırmaktır.
1. Presentation Layer (Sunum Katmanı) 
   * Kullanıcıyla iletişim kuran katmandır.
     > Örnek: Web uygulamalarında MVC’de Controller ve View, veya API’de Controller.
   * Görevleri:
      > Kullanıcıdan gelen verileri almak
      > İş katmanına iletmek
      > İş katmanından gelen sonucu kullanıcıya göstermek
      > Hiçbir iş kuralı burada olmamalıdır.

2. Business Layer (İş Katmanı / Service Layer) 
   * Sistemin iş kurallarının uygulandığı katmandır.
      > Örnek: Bir e-ticaret sisteminde sipariş oluşturma, stok kontrolü.
   * Bu katmanda genellikle Service sınıfları bulunur.
      > Örn: OrderService, PaymentService
   * Görevleri:
      > İş mantığını uygulamak
      > Veri doğrulama
      > Veri katmanı ile sunum katmanı arasında köprü görevi görmek

3. Data Access Layer (Veri Erişim Katmanı / Repository Layer) 
   * Veritabanı veya başka veri kaynaklarına erişim sağlamak için kullanılır.
      > Örnek: Entity Framework, Dapper, SQL sorguları.
   * Bu katman genellikle Repository pattern ile kullanılır.
   * Repository, veri kaynağı ile iş katmanı arasındaki soyutlamadır.
      > Örn: OrderRepository sınıfı veritabanından siparişleri alır veya ekler.

## Service & Repository Pattern ##
* Service Pattern: İş katmanındaki sınıfların belirli bir iş sürecini yönetmesini sağlar.
* Repository Pattern: Veri erişimi soyutlar. İş katmanı, veri kaynağına doğrudan bağımlı olmaz.
  * Örnek akış:
 ```yaml
+--------------------------+
|  KULLANICI (Uygulama)    |  
+--------------------------+
             |
             | 1. Sipariş Ekle
             v
+---------------------------------+
|  Presentation Layer(Controller) |
+---------------------------------+
             |
             | 2. OrderService Çağır
             v
+-------------------------------+
|  Business Layer(OrderService) |
+-------------------------------+
             |
             | 3. OrderRepository Çağır & Veri İste
             v
+-------------------------------------+
|  Data Access Layer(OrderRepository) |
+-------------------------------------+
             |
             | 4. Veriyi Kaydet (SQL/NoSQL)
             v
+--------------------------+
|       Veritabanı         |
+--------------------------+
             |
             | 5. Kayıt Başarısı Sonucunu Dön
             v
+-------------------------------------+
|  Data Access Layer(OrderRepository) |
+-------------------------------------+
             |
             | 5. Sonucu Service'e İlet
             v
+--------------------------------+
|  Business Layer (OrderService) |
+--------------------------------+
             |
             | 5. Sonucu Controller'a İlet
             v
+---------------------------------+
|  Presentation Layer(Controller) |
+---------------------------------+
             |
             | 6. Sonucu Kullanıcıya Dön
             v
+--------------------------+
|  KULLANICI (Uygulama)    |
+--------------------------+
```

## Clean Architecture ##
Clean Architecture, bağımlılıkların ve sorumlulukların kontrol altında tutulduğu daha modern bir yaklaşımdır. Robert C. Martin’in (Uncle Bob) geliştirdiği bir mimaridir.

### Katmanlar ###
1. Domain (Alan / Core Katmanı)
  * İş kuralları ve domain modelleri burada bulunur.
  * Hiçbir dış bağımlılık içermez.
    > Örnek: Order, Customer entity’leri, domain servisleri.
  * Önemli: Diğer katmanlar domain’e bağımlı olabilir, ama domain hiçbir katmana bağımlı olmamalıdır.
2. Application (Uygulama Katmanı)
  * Use-case’ler burada uygulanır.
  * Domain katmanındaki modelleri kullanarak iş süreçlerini yönetir.
    > Örnek: CreateOrderUseCase, CalculateInvoiceUseCase
3. Infrastructure (Altyapı Katmanı)
  * Veritabanı, dosya sistemi, API çağrıları, üçüncü parti servisler gibi dış bağımlılıkları içerir.
  * Repository implementasyonları, mail servisleri vb.
4. API / Presentation Katmanı
  * Kullanıcı veya sistemle iletişimi sağlar (Controller, API, UI)
  * Application katmanındaki use-case’leri çağırır

## Bağımlılıkların Dışa Akması İlkesi (Dependency Rule / Dependency Inversion) ##
* İç katmanlar dış katmanlara bağımlı olamaz.
* Dış katmanlar iç katmanlara bağımlıdır.
* Interface’ler kullanılarak bağımlılıklar ters çevrilir:
   >Örnek: IOrderRepository interface’i domain veya application katmanında tanımlanır, infrastructure katmanı bunu implement eder.
* Bu sayede:
    * Test edilebilirlik artar
    * Teknoloji bağımlılığı azalır
    * Kod değişiklikleri diğer katmanları etkilemez
 
## Katmanlı Mimari vs Clean Architecture ##
| Özellik / Mimari   | Katmanlı Mimarî                                             | Clean Architecture                                              |
| ------------------ | ----------------------------------------------------------- | --------------------------------------------------------------- |
| Katmanlar          | Presentation, Business, Data Access                         | Domain, Application, Infrastructure, API                        |
| Bağımlılık Yönü    | Genellikle yukarıdan aşağı (Presentation → Business → Data) | İç katmanlar bağımlı değil, dış katmanlar iç katmanlara bağımlı |
| Soyutlama          | Service & Repository                                        | Interface + Dependency Inversion                                |
| Test Edilebilirlik | Orta                                                        | Yüksek                                                          |
| Esneklik           | Orta                                                        | Yüksek (teknoloji bağımsız)                                     |

# Veritabanı ve ORM #

## SQL Nedir? ##
SQL (Structured Query Language), veritabanlarıyla iletişim kurmak için kullanılan bir sorgulama dilidir. Veri tabanı üzerinde okuma, yazma, silme, ekleme ve diğer tablo işlemleri yapılmasını sağlar. Kısaca veri ne yapılması gerektiğini anlatır.
* Örnek;<br>
> Veritabanındaki Students tablosundan yaşı 18'in üzerinde olan tüm kayıtları çeken sorgu;
```bash
SELECT * FROM Students WHERE Age > 18;
```
## Veritabanı İlişkileri ##
### İlişkisel Veritabanları ###
* İlişkisel veritabanları, yapılandırılmış verileri birbirleri ile bağlantılı tablolar halinde tutan yapılardır. 
* İlişkisel veritabanlarınad bağlantılar ortak anahtarlar(Birincil veya yabancıl anahtar) ile yapılır. 
* Çoğunlukla SQL sorgu dili kullanılır. 
* Yüksesk veri bütünlüğü sağlayabilirler.
### İlişkisel Olmayan Veritabanları ###
* İlişkisel olmayan veritabanları genellikle NoSQL olarak adlandırılır.
* Veriyi tablolar yerine farklı yapı ve formatlarda depolarlar
   > Formatlar : Belge(JSON vb), Anahtar-Değer çiftleri, Sütun Aileleri, Graph'lar
* Genellikle daha esnek bir şemaya sahip olan sistemlerdir
* Büyük hacimli, hızlı değişen ve yapılandırılmamış verileri yönetmek için ortaya çıkmışlardır.

## ORM Nedir? ##
ORM(Object Relational Mapping) nesne tabanlı programlama dilleri ile ilişkisel veritabanları arasında iletişim kurmaya yarayan yapıdır. Kod içindeki class'ları veri tabanındaki tablolara dönüştürür. Böylece sorgu yazmak yerine kod ile veri işlemleri yapılabilir.
## EF Core (ORM Kütüphanesi) ##
Entity Framework Core, .NET platformu için geliştirilmiş modern bir ORM kütüphanesidir. EF Core'un sağladıkları:
  * SQL sorguları yazmadan C# ile veritabanı işlemleri yapılır.
  * Code-First veya Database-First yaklaşımlarıyla tablo ve modeller otomatik oluşturulur.
  * Farklı veritabanı sistemleri (SQL Server, PostgreSQL, SQLite vb.) desteklenir.<br>
  * Örnek;
  > C# kodundaki bu kısmı;
```bash
var students = _context.Students.Where(s => s.Age > 18).ToList();
```
> Arkaplanda aşağıdaki kısma çevirir
```bash
SELECT * FROM Students WHERE Age > 18;
```
## DbContext ##
DbContext, Entity Framework’te veritabanı ile etkileşimi yöneten ana sınıftır. Veri tabanı ile olan bağlantıyı temsil eder. Veri ile işlemler yapılacağı zaman çağrılır ve CRUD (Create, Read, Update, Delete) işlemlerini gerçekleştirir.
## LINQ Nedir? ##
LINQ (Language Integrated Query), C# içerisine gömülü bir sorgulama dilidir. EF Core ile birlikte veritabanı sorgularını C# sözdizimiyle yazmamızı sağlar.<br>
* Bazı metodlar ve sql karşılıkları;

| LINQ Metodu            | Açıklama                                                    | SQL Karşılığı   |
| ---------------------- | ----------------------------------------------------------- | --------------- |
| `.Where()`             | Belirtilen bir koşula göre filtreleme yapar.                | `WHERE`         |
| `.Select()`            | Sonuç kümesinden hangi kolonların seçileceğini belirler.    | `SELECT`        |
| `.OrderBy()`           | Sonuçları artan sırada (ascending) sıralar.                 | `ORDER BY ASC`  |
| `.OrderByDescending()` | Sonuçları azalan sırada (descending) sıralar.               | `ORDER BY DESC` |
| `.FirstOrDefault()`    | Koşulla eşleşen ilk kaydı döndürür, yoksa varsayılan döner. | `SELECT TOP 1`  |
| `.Any()`               | Belirtilen koşula uygun kayıt olup olmadığını kontrol eder. | `EXISTS`        |
| `.Count()`             | Koşulu sağlayan kayıt sayısını hesaplar.                    | `COUNT(*)`      |
| `.Join()`              | Ortak bir anahtar (key) kullanarak iki tabloyu birleştirir. | `JOIN`          |


> Örnek;
```bash
var adults = context.Students
    .Where(s => s.Age > 18)
    .OrderBy(s => s.Name)
    .Select(s => new { s.Name, s.Age })
    .ToList();
```
## Code-First ve Database-First Yaklaşımı ##
Veritabanı ile uygulama kodunun nasıl yönetileceğine dair iki ana yaklaşım vardır. 
### Code First ###
Uygulamadaki sınıflar (modeller) yazılır ve veritabanı şeması bu sınıflara göre otomatik olarak oluşturulur.
### Database First ###
Veritabanı mevcuttur ve ORM veritabanındaki şemaya göre koddaki sınıfları oluşturur. 

## Code-First vs Database-First ##
| Yaklaşım           | Açıklama                                                                        | Kullanım Durumu                                 |
| ------------------ | ------------------------------------------------------------------------------- | ----------------------------------------------- |
| **Code-First**     | Önce C# modellerini (class) yazarsın, EF bu modellerden veritabanını oluşturur. | Yeni projelerde tercih edilir.                  |
| **Database-First** | Var olan veritabanından EF otomatik olarak C# modellerini üretir.               | Mevcut bir veritabanına bağlanırken kullanılır. |

## Temel SQL Sorguları ##
| Komut      | Açıklama         | Örnek                                                    |
| ---------- | ---------------- | -------------------------------------------------------- |
| **SELECT** | Veriyi okur      | `SELECT * FROM Students;`                                |
| **INSERT** | Yeni kayıt ekler | `INSERT INTO Students (Name, Age) VALUES ('Ahmet', 23);` |
| **UPDATE** | Kayıt günceller  | `UPDATE Students SET Age = 23 WHERE Name = 'Ahmet';`     |
| **DELETE** | Kayıt siler      | `DELETE FROM Students WHERE Name = 'Ahmet';`             |

# Güvenlik ve Performans #
## Authentication Nedir? ##
Sisteme giriş yapmaya çalışan kullanıcının kim olduğunu doğrulayan sisteme denir.Kullanıcı bir sisteme erişmeye çalıştığında, sistem kullanıcının kimliğini doğrulamak için kullanıcıdan bazı bilgiler ister. Örneğin banka hesabına giriş yaparken kullanıcı adı ve şifresisin doğrulanmasıdır.
## Authorization Nedir? ##
Sistemde giriş yapmış kullanıcıların erişim izinlerini kontrol eder. Kullanıcının dosya, sayfa veya fonksiyonlar gibi çeşitli kaynaklardan hangileri ile işlem yapacağğını kontrol eder. Sistem rol, izin vb. tabanlı yöntemler ile erişimleri kontrol eder.

## Authentication vs Authorization ##
| Kavram                                | Açıklama                                                  | Örnek                                                    |
| ------------------------------------- | --------------------------------------------------------- | -------------------------------------------------------- |
| **Authentication (Kimlik Doğrulama)** | Kullanıcının **kim olduğunu** doğrular. (Login işlemi)    | Kullanıcı adın ve şifren doğru mu?                       |
| **Authorization (Yetkilendirme)**     | Doğrulanan kullanıcının **neyi yapabileceğini** belirler. | Kullanıcı admin mi, sadece kendi profilini mi görebilir? |

## JSON Web Token ##
Kullanan tarafların birbirleri arasındaki veri alışverişini ve bunun doğrulamasını sağlayan JSON tabanlı tanımlanmış açık bir standarttır. Bu standarda göre bir sunucu, bir kullanıcının yönetici olduğu bilgilerini içeren bir token değeri üretebilir, bu token'ı kullanıcıya gönderebilir, kullanıcı bu token'ı kullanarak yönetici özelliklerini kullanabilir.

### JWT Yapısı ###
| Bölüm         | Açıklama                               | Örnek                              |
| ------------- | -------------------------------------- | ---------------------------------- |
| **Header**    | Algoritma ve token tipi bilgisi        | `{ "alg": "HS256", "typ": "JWT" }` |
| **Payload**   | Kullanıcı bilgileri (claims)           | `{ "userId": 1, "role": "Admin" }` |
| **Signature** | Token’ın bozulmadığını kanıtlayan imza | SHA256 algoritmasıyla oluşturulur  |

### JWT Nasıl Çalışır ###
Örnek bir senaryo için;<br>
1. Kullanıcı giriş yapmak için sisteme kullanıcı adı ve şifre bilgilerini girer.
2. Sistem bu bilgileri doğrular
3. Bilgiler doğru ise sistem bu bilgileri içeren bir JWT oluşturur ve frontende gönderir.
4. Frontend kısmında bu token değerinu localstorage veya cookie'de saklar
5. Sonraki isteklerde kullanıcı bu token sunucuya gönderilir ve sunucu bu token'i doğrular.

##	OAuth, OAuth2.0, OpenIddict, OpenID ##
### 1- OAuth Nedir? ###
OAuth (Open Authorization), üçüncü taraf uygulamaların kullanıcı adına erişim sağlamasına izin veren bir yetkilendirme protokolüdür.
* Örnek:
   * Kullanıcı Google hesabıyla başka bir siteye giriş yaparsa,
   * Site kullanıcının şifresini görmez.
   * Google kullanıcıya “Bu uygulama e-postalarına erişebilir mi?” diye sorar.
   * Kullanıcı izin verirse, Google o siteye sınırlı bir erişim token’ı verir.

### 2- OAuth 2.0 Nedir? ###
OAuth 2.0, orijinal OAuth’un geliştirilmiş ve modern versiyonudur. 2.0 ile farklı platformlarda kullanılabilen bir özellik haline gelmiş ve OAuth protokolü daha esnek hale gelmiştir.
### 3- OpenID Connect (OIDC) Nedir? ###
OpenID veya modern versiyonu OpenID Connect (OIDC) bir kimlik doğrulama protokolüdür. Amacı kullanıcının farklı sitelere tek bir dijital kimlik ile girişini sağlamaktır. Örneğin her e-ticaret sitesine girip kişisel bilgileri doldurmak yerine üçüüncü taraf platformlar (Google vb.) ile giriş yapıldğında bu platformlardaki kişisel bilgileriniz ile oluşturulmuş kimlik ile giriş yapılır.

### 4- OpenIddict Nedir? ###
OpenIddict, .NET Core ve ASP.NET Core platformları için tasarlanmış açık kaynaklı bir kütüphanedir. Görevi, uygulamanızın kendi OAuth 2.0 Yetkilendirme Sunucusunu (Authorization Server) ve OpenID Connect Sağlayıcısını (Identity Provider) oluşturmasına izin vermektir.

## Sistem Performansı ##
Bir sistemin, kullanıcılara daha iyi ve hızlı cevap vermesi için yüksek performansa sahip olması gerekir. Bu sebeple sistemin prformansını arttıracak değişiklikler gerekebilir.
### 1- AsNoTracking() ###
EF Core’da bir entity veritabanından alındığında Change Tracker tarafından izlenir.Ama sadece okuma yapılacaksa, bu gereksiz bir maliyettir.
* Örnek;
```bash
var students = _context.Students.AsNoTracking().ToList();
```
AsNoTracking Kullanıldğında takip edilmez ve performansa artar.
### 2- Asenkron Programlama ve Akış Yönetimi ###
Modern uygulamalar I/O (Giriş/Çıkış) operasyonlarında (veritabanı, ağ) beklememek için asenkron çalışmalıdır. Örneğin büyük bir veri seti çekilceği zaman sistemin kilitlenmemesi için bu işlem asenkron yapılmalıdır.
* Örnek;
```bash
await foreach (var student in _context.Students.AsAsyncEnumerable())
{
    Console.WriteLine(student.Name);
}
```
### 3-Caching(Önbellekleme) ###
Sistemde sık kullanılan ya da değişmeyen veriler, veri tabanına yük bindirmemesi için bellekte(veya dış sistemlerde) saklanır.
1. Memory Caching<br>
Verinin, uygulamanın çalıştığı sunucunun RAM'inde (belleğinde) geçici olarak tutulmasıdır. En hızlı önbellekleme türüdür.
2. Redis<br>
Bellek içi (In-memory), dağıtık bir anahtar-değer (Key-Value) veritabanıdır. Veriyi uygulamanın belleğinden ayrı, merkezi bir yerde tutar.
* Örnek;
```bash
var students = memoryCache.GetOrCreate("students", entry =>
{
    entry.AbsoluteExpirationRelativeToNow = TimeSpan.FromMinutes(10);
    return _context.Students.ToList();
});
```
### 4-Performans Analizi ve İzleme ###
Optimizasyona başlamadan önce, sistemi zorlayan kod parçalarını bulmak için yapılan işlemlerdir.
1. Profiling (Profil Çıkarma)
Kodun hangi bölümlerinin ne kadar zaman ve kaynak (CPU, bellek) tükettiğini analiz etme sürecidir.
2. Monitoring (İzleme)
Uygulamanın ve altyapının üretim ortamındaki performansını sürekli izlenmesidir.

## OWASP TOP 10 ##
| **Kod ve Başlık** | **Açıklama** |
|--------------------|---------------|
| **A01:2021 - Bozuk Erişim Kontrolü (Broken Access Control)** | Kullanıcıların yetkili olmadıkları verilere veya işlevlere (örneğin, başka bir kullanıcının hesabı, yönetici sayfaları) erişmesine olanak tanıyan hatalı yetkilendirme uygulamalarıdır. |
| **A02:2021 - Kriptografik Hatalar (Cryptographic Failures)** | Hassas verilerin (şifreler, kredi kartları) yetersiz veya hatalı şifrelenmesi ya da hiç şifrelenmemesi sonucu bu verilerin ifşa olma riskidir. |
| **A03:2021 - Enjeksiyon (Injection)** | Kullanıcının sağladığı güvenilmeyen verilerin bir komut veya sorgu parçası olarak yorumlanmasıdır (örneğin, SQL Enjeksiyonu). |
| **A04:2021 - Güvenli Olmayan Tasarım (Insecure Design)** | Uygulama mimarisindeki veya tasarımındaki eksiklikler nedeniyle oluşan zafiyetlerdir; tasarım aşamasında güvenlik gereksinimlerinin yeterince ele alınmamasıdır. |
| **A05:2021 - Güvenlik Yanlış Yapılandırması (Security Misconfiguration)** | Varsayılan ayarların kullanılmaması, gereksiz özelliklerin açık bırakılması, yanlış yapılandırılmış HTTP başlıkları veya bulut hizmetleri gibi hatalı yapılandırmalardır. |
| **A06:2021 - Zafiyetli ve Güncel Olmayan Bileşenler (Vulnerable and Outdated Components)** | Uygulamada kullanılan kütüphaneler, framework'ler veya diğer üçüncü taraf bileşenlerin bilinen güvenlik açıklarını içermesidir. |
| **A07:2021 - Kimlik Doğrulama ve Hata Yönetimi Hataları (Identification and Authentication Failures)** | Kullanıcı kimlik doğrulama veya oturum yönetimi işlevlerindeki hatalar nedeniyle saldırganların geçici olarak başka bir kullanıcının kimliğine bürünmesi riskidir. |
| **A08:2021 - Yazılım ve Veri Bütünlüğü Hataları (Software and Data Integrity Failures)** | Uygulamanın güncelleme, kritik veri akışı veya CI/CD boru hattı gibi yerlerdeki bütünlüğe güvenmesi; genellikle doğrulama (verification) yapılmamasıdır. |
| **A09:2021 - Güvenlik Kaydı ve İzleme Hataları (Security Logging and Monitoring Failures)** | Kritik olayların (başarısız girişler, erişim hataları) yetersiz veya hiç kaydedilmemesi ve bu kayıtların gerçek zamanlı olarak izlenip uyarılmamasıdır. |
| **A10:2021 - Sunucu Taraflı İstek Sahteciliği (Server-Side Request Forgery - SSRF)** | Bir saldırganın, zafiyetli sunucuyu kullanarak sunucunun erişebildiği herhangi bir dahili veya harici başka bir adrese istek göndermeye zorlamasıdır. |


# Logging ve Hata Yönetimi #
## Logging Nedir? Neden Yapılır? ##
Loglama (Logging), uygulamanın çalışması sırasında gerçekleşen olayları kayıt altına alma işlemidir. Amaç, hataları, performans sorunlarını, kullanıcı davranışlarını veya sistem olaylarını izleyebilmek ve gerektiğinde geriye dönük analiz yapmaktır.<br><br>
Neden Loglama Yapılır?
* Hata tespiti: Exception’lar ve beklenmeyen durumlar kaydedilir.
* Performans izleme: İşlem süreleri, servis yanıt süreleri vb. takip edilir.
* Güvenlik: Yetkisiz erişim denemeleri gibi olaylar raporlanır.
* Debug / geliştirme: Geliştirici uygulamanın hangi adımda ne yaptığını görebilir.
* Audit (denetim): Sistem kim tarafından, ne zaman, ne yaptı gibi olayları kaydeder.
