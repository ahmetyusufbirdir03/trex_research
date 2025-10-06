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

2002: İlk sürüm olan .NET Framework yayınlandı (Windows odaklıydı).
2016: Microsoft, açık kaynaklı ve platformlar arası çalışan .NET Core’u tanıttı.
2020 ve sonrası: Tüm sürümler birleşerek .NET 5, .NET 6, .NET 7, .NET 8 olarak devam etti.

| Özellik         | .NET Framework            | .NET Core                              | .NET 7/8+                   |
| --------------- | ------------------------- | -------------------------------------- | --------------------------- |
| **Yıl**         | 2002                      | 2016                                   | 2022–2024                   |
| **Platform**    | Sadece Windows            | Cross-platform (Windows, Linux, macOS) | Tek birleşik .NET platformu |
| **Açık Kaynak** | ❌ Hayır                  | ✅ Evet                               | ✅ Evet                     |
| **Performans**  | Orta                      | Yüksek                                 | Çok yüksek                  |
| **Kapsam**      | Eski Windows uygulamaları | Web, API, microservice                 | Web, API, mobil, bulut, IoT |
| **Durum**       | Artık güncellenmiyor      | Yerini .NET 7/8 aldı                   | En güncel sürümler          |


