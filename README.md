# Saz ü Söz

**Saz ü Söz**, müzisyenler için geliştirilmiş Türkçe bir Android nota ve PDF okuyucusudur. Eserleri listeler hâlinde düzenlemeyi, PDF veya nota dosyalarını görüntülemeyi, sayfalar üzerinde kalıcı notlar almayı ve sayfaları eller serbest biçimde çevirmeyi amaçlar.

Bu depo **v0.1** kaynak kodunu içerir.

## Öne çıkan özellikler

- Tamamen Türkçe arayüz
- Marka renkleri, özel logo ve animasyonlu açılış
- PDF, Guitar Pro ve MusicXML dosyalarını görüntüleme
- Dosyaları yeniden adlandırılabilir ve silinebilir listelerde düzenleme
- Küçük sayfa önizlemeleri ve tam ekran okuma
- Dikey veya yatay sayfa geçişi
- Ekran yönüne uygun “Sayfaya sığdır” davranışı
- İki parmakla yakınlaştırma, uzaklaştırma ve sayfayı taşıma
- Kalem, fosforlu kalem, silgi, geri alma ve çizgi seçme araçları
- Siyah, mavi, kırmızı, yeşil ve beyaz renk paleti
- PDF üzerine yazılan notları sonraki açılışlarda düzenleme veya silme
- Kalem kullanımında gelişmiş avuç içi reddetme
- Yüz hareketleriyle ileri ve geri sayfa kontrolü
- Baş hareketi, göz kırpma ve ağız hareketi seçenekleri
- Bluetooth pedal/klavye ile sayfa çevirme
- Otomatik sayfa çevirme ve ekran zaman aşımı seçenekleri
- Çevrimdışı çalışma; kamera görüntüsü cihaz dışına gönderilmez

## Desteklenen dosya türleri

- PDF: `.pdf`
- Guitar Pro: `.gp`, `.gp3`, `.gp4`, `.gp5`, `.gpx`
- MusicXML: `.musicxml`

## Sistem gereksinimleri

- Android 10 veya üzeri (API 29+)
- ARM64 Android cihaz
- Yüz hareketleri kullanılacaksa ön kamera izni

## Kurulum

1. GitHub **Releases** bölümündeki `Saz-u-Soz-v0.1.apk` dosyasını indirin.
2. Android ayarlarında kullandığınız tarayıcı veya dosya yöneticisi için “Bilinmeyen uygulamaları yükle” iznini açın.
3. APK dosyasını çalıştırıp kurulumu tamamlayın.
4. Uygulamayı açın, bir liste oluşturun ve **Dosya ekle** düğmesiyle belgenizi seçin.

> v0.1 APK’sı doğrudan kurulum ve test için hazırlanmıştır. Daha sonraki bir sürüm farklı imzayla yayımlanırsa önceki test sürümünün kaldırılması gerekebilir.

## Kalem ve notlar

Kalem araçları açıldığında varsayılan olarak siyah kalem seçilir. Notlar belge ve sayfa ile ilişkilendirilerek yerel veritabanında saklanır. Kayıtlı çizgiler yeniden seçilebilir, rengi veya kalınlığı değiştirilebilir, silinebilir ve geri alınabilir.

Kalem algılandığında parmak ve avuç temasları çizime dönüştürülmez. Yakınlaştırma ve taşıma işlemleri iki parmakla yapılabilir.

## Eller serbest kontrol

Yüz hareketleri cihaz kamerası ve MediaPipe kullanılarak cihaz üzerinde değerlendirilir. İleri ve geri hareketler ayrı ayrı seçilebilir ve kalibre edilebilir. Bluetooth pedal veya klavye tuşları da sayfa çevirmek için kullanılabilir.

Hareket algılama; ışık, kamera açısı, cihaz performansı ve kullanıcıya göre değişebilir. Kritik sahne kullanımlarından önce ayarların prova edilmesi önerilir.

## Kaynak koddan derleme

Gereksinimler:

- Android Studio
- JDK 21
- Android SDK 37

Derleme:

```bash
./gradlew :app:assembleDebug
```

Oluşan APK:

```text
app/build/outputs/apk/debug/Saz-u-Soz-v0.1.apk
```

## Gizlilik

Uygulama kullanıcı dosyalarını, notlarını veya kamera görüntülerini bir sunucuya göndermez. Yüz hareketi analizi cihaz üzerinde yapılır. Kamera yalnızca hareket kontrolü etkinleştirildiğinde kullanılır.

## Proje yapısı

- `app`: Uygulama, ana ekran ve dosya listeleri
- `core/annotations`: Kalem ve not araçları
- `core/facegestures`: Yüz hareketi algılama ve kalibrasyon
- `core/reader`: Ortak okuyucu bileşenleri
- `core/settings`: Uygulama ayarları
- `core/ui`: Tema, marka ve ortak arayüz bileşenleri
- `features/pdf`: PDF okuyucu
- `features/alphatab`: Guitar Pro ve MusicXML okuyucu

## Köken ve lisans

Saz ü Söz, açık kaynaklı [ExCoda](https://github.com/appexcoda/excoda) projesi temel alınarak geliştirilmiş bir türev çalışmadır. Arayüz, marka, Türkçeleştirme, PDF okuma deneyimi, hareket seçenekleri ve kalem sistemi üzerinde değişiklikler yapılmıştır.

Proje Apache License 2.0 ile lisanslanmıştır. Üçüncü taraf bileşenler ve atıflar için `NOTICE` dosyasına bakın.

## Sürüm

Güncel sürüm: **v0.1**

Sürüm tarihi: **7 Ekim 2026**
