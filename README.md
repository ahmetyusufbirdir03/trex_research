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

## "dotnet --info" Örneği ve İşlevi
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

.NET Geliştirme Ortamı
🔧 SDK Bilgileri
ÖzellikDeğerVersiyon9.0.302Commitbb2550b9afWorkload Version9.0.300-manifests.183aaee6MSBuild Version17.14.13+65391c53b
💻 Çalışma Zamanı Ortamı
ÖzellikDeğerİşletim SistemiWindows 10.0.26100PlatformWindows (x64)RIDwin-x64Base PathC:\Program Files\dotnet\sdk\9.0.302\
🏠 Host Bilgileri
ÖzellikDeğerVersion9.0.7Architecturex64Commit3c298d9f00
📦 Yüklü SDK'lar
.NET 8.0.403
.NET 9.0.302
🚀 Yüklü Runtime'lar
Microsoft.AspNetCore.App
8.0.10
8.0.18
9.0.7
Microsoft.NETCore.App
6.0.16
8.0.10
8.0.13
8.0.18
9.0.7
Microsoft.WindowsDesktop.App
8.0.10
8.0.18
9.0.7


  


