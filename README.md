# Modern Yazılım Geliştirme Pratikleri

## Git Nedir? GitHub Nedir?
Git: Bir kontrol sistemidir. Sistemin anlık görüntüsünü kaydeder ve değişiklik durumunda eski haline referans verir.<br>
GitHub : Git ile yönetilen projeleri internet üzerinde depolamana ve paylaşmana yarayan bir platformdur.

## Temel Git Komutları
init : Yeni bir proje başlatır.
clone : Başka bir projeyi kopyalar.
add : Yapılan değişiklikleri kalıcı hale getirmeden önce sıraya ekler.
commit : Yapılan değişiklikleri kalıcı hale getirir.
push : Kalıcı değişiklikleri GitHub projesine gönderir.
pull : GitHub'daki son değişiklikleri indirir ve yerel projeye ekler.
branch : Yeni bir dal(branch) oluşturur veya mevcut dalları listeler.
merge : Bir dalda yapılan değişiklikleri başka bir dal ile birleştirir.

## CI/CD Nedir?
CI/CD (Continuous Integration / Continuous Deployment), yazılım geliştirme sürecinde kodun otomatik olarak derlenmesini, test edilmesini ve dağıtılmasını sağlayan bir yaklaşımdır.<br>
CI (Continuous Integration): Geliştiricilerin kodlarını sık sık entegre edip otomatik testlerle doğrulamasıdır.<br>
CD (Continuous Deployment): Başarılı testlerden sonra kodun otomatik olarak üretim ortamına aktarılmasıdır.

## .NET Projesi için CI/CD
Bir .NET projesinde CI/CD genellikle GitHub Actions veya Azure DevOps Pipelines ile yapılır.
Bu sistemler dotnet restore, dotnet build, dotnet test, dotnet publish komutlarını sırayla çalıştırarak:
1- Kodun bağımlılıklarını yükler,
2- Derler,
3- Test eder,
4- Yayınlanabilir çıktıyı oluşturur ve
5- Azure, IIS veya Docker ortamına otomatik olarak dağıtır.

