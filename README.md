# Saz Pdf

<p align="center">
  <img src="https://github.com/emrepinarbasi/sazusoz/releases/download/v0.1/ChatGPT.Gorseli.7.Eki.2026.22_16_21.png" alt="Saz ü Söz logosu" width="640">
</p>

**Saz Pdf**, müzisyenler için geliştirilmiş Türkçe bir Android PDF ve nota okuyucusudur. Belgeleri listeler hâlinde düzenlemeyi, sayfalar üzerinde kalıcı notlar almayı ve nota sayfalarını dokunarak, Bluetooth pedal/klavye veya yüz hareketleriyle çevirmeyi sağlar.

Bu depo **Saz Pdf v1.0** kaynak kodunu içerir.

## Öne çıkan özellikler

- Tamamen Türkçe kullanıcı arayüzü
- Saz ü Söz marka tasarımı, özel uygulama simgesi ve animasyonlu açılış
- PDF, Guitar Pro ve MusicXML dosyalarını görüntüleme
- Dosyaları listeler hâlinde düzenleme
- Liste oluşturma, yeniden adlandırma ve silme
- Dikey ve yatay ekran desteği
- Ekran yönünü koruyan **Sayfaya sığdır** davranışı
- İki parmakla yakınlaştırma, uzaklaştırma ve sayfayı taşıma
- Sağdan sola yatay veya yukarıdan aşağıya dikey sayfa geçişi
- Küçük sayfa önizlemeleri ve tam ekran okuma
- Kalem, fosforlu kalem, silgi, geri alma ve çizgi seçme araçları
- Siyah, mavi, kırmızı, yeşil ve beyaz renk seçenekleri
- PDF notlarını sonraki açılışlarda düzenleme veya silme
- Gelişmiş avuç içi reddetme
- Yüz hareketleriyle ileri ve geri sayfa kontrolü
- Bluetooth pedal ve klavye ile sayfa çevirme
- Ayarlanabilir otomatik sayfa çevirme
- Çevrimdışı çalışma

## Desteklenen dosya türleri

- PDF: `.pdf`
- Guitar Pro: `.gp`, `.gp3`, `.gp4`, `.gp5`, `.gpx`
- MusicXML: `.musicxml`

## Sistem gereksinimleri

- Android 10 veya üzeri (API 29+)
- ARM64 Android telefon veya tablet
- Yüz hareketleri kullanılacaksa ön kamera izni

## Kurulum

1. GitHub **Releases** bölümünden `Saz-Pdf-v1.0.apk` dosyasını indirin.
2. Gerekirse tarayıcı veya dosya yöneticiniz için **Bilinmeyen uygulamaları yükle** iznini etkinleştirin.
3. APK dosyasını açıp kurulumu tamamlayın.
4. **Saz Pdf** uygulamasını çalıştırın.
5. Bir liste oluşturun ve **Dosya ekle** seçeneğiyle belgenizi seçin.

Uygulamanın paket kimliği `com.emrepinarbasi.sazusoz` olarak belirlenmiştir. Bu kimlik, ExCoda uygulamasıyla kurulum çakışmasını önler.

## Kalem ve not sistemi

Kalem araçları açıldığında siyah kalem varsayılan olarak seçilir. Çizimler belge ve sayfayla ilişkilendirilerek cihazdaki yerel veritabanında saklanır. Kayıtlı çizgiler daha sonra seçilebilir, düzenlenebilir, silinebilir veya geri alınabilir.

Kalem algılandığında parmak ve avuç temasları çizime dönüştürülmez. Sayfayı yakınlaştırmak, uzaklaştırmak veya taşımak için iki parmak kullanılabilir.

## Eller serbest kontrol

Yüz hareketleri cihaz kamerası ve MediaPipe kullanılarak cihaz üzerinde değerlendirilir. İleri ve geri sayfa hareketleri ayrı ayrı seçilebilir ve kullanıcıya göre kalibre edilebilir. Bluetooth pedal veya klavye tuşları da sayfa çevirmek için kullanılabilir.

Hareket algılama başarımı ışık, kamera açısı, cihaz performansı ve kullanıcıya göre değişebilir. Sahne kullanımından önce ayarların prova edilmesi önerilir.

## Kaynak koddan derleme

Gereksinimler:

- Android Studio
- JDK 21
- Android SDK 37

Derleme komutu:

```bash
./gradlew :app:assembleDebug
```

Oluşan APK:

```text
app/build/outputs/apk/debug/Saz-Pdf-v1.0.apk
```

## Gizlilik

Saz Pdf; kullanıcı dosyalarını, notlarını veya kamera görüntülerini bir sunucuya göndermez. Yüz hareketi analizi cihaz üzerinde gerçekleştirilir. Kamera yalnızca hareket kontrolü etkinleştirildiğinde kullanılır.

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

Saz Pdf, açık kaynaklı [ExCoda](https://github.com/appexcoda/excoda) projesi temel alınarak geliştirilmiştir. Arayüz, marka, Türkçeleştirme, PDF okuma deneyimi, hareket seçenekleri ve kalem sistemi üzerinde değişiklikler yapılmıştır.

Proje Apache License 2.0 ile lisanslanmıştır. Üçüncü taraf bileşenler ve atıflar için `NOTICE` dosyasına bakın.

## Sürüm

Güncel sürüm: **v1.0**

Sürüm tarihi: **8 Ekim 2026**
