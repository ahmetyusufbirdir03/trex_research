# Modern Yazılım Geliştirme Pratikleri

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
CI (Continuous Integration): Geliştiricilerin kodlarını sık sık entegre edip otomatik testlerle doğrulamasıdır.<br>
CD (Continuous Deployment): Başarılı testlerden sonra kodun otomatik olarak üretim ortamına aktarılmasıdır.

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

# .NET Ekosistemi

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

# Backend Geliştirme Temelleri

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

# ASP.NET
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
         🔹 Kullanıcı (Tarayıcı)
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
         🔹 Kullanıcı (Tarayıcı)

```

## MVC mimarisi Kullanım Amaçları ##
1. Separation of Concerns (Kaygıların Ayrılması)
   >Her katman kendi işine odaklanır, İşler karışmaz.
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
