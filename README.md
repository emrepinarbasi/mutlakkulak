# Mutlak Kulak

<p align="center">
  <img src="app/src/main/res/drawable-nodpi/mutlak_kulak_logo.png" alt="Mutlak Kulak logosu" width="520">
</p>

<p align="center">
  Android için sade, hızlı ve ekran boyutuna uyum sağlayan kromatik akort uygulaması.
</p>

Mutlak Kulak, çaldığınız sesi cihazın mikrofonundan dinleyerek temel frekansı ve en yakın kromatik notayı belirler. Ölçülen sesin hedef notaya göre farkını hem cent hem de Hz cinsinden gösterir.

## Ekran görüntüsü

<p align="center">
  <img src="screenshots/mutlak-kulak-dark-turquoise-logo.png" alt="Mutlak Kulak koyu tema görünümü" width="760">
</p>

## Özellikler

- Otomatik kromatik nota ve oktav algılama
- Anlık frekans, hedef frekans ve Hz farkı gösterimi
- `-60` ile `+60` cent aralığında görsel akort göstergesi
- Hızlı A4 referans seçenekleri: 438 Hz, 440 Hz ve 442 Hz
- 400–480 Hz arasında özel A4 referans frekansı
- Açık ve koyu tema desteği
- Koyu temada yüksek görünürlüklü turkuaz logo
- Telefon, tablet ve katlanabilir cihazlara uyumlu arayüz
- Dikey ve yatay ekran yönü desteği
- Akort sırasında ekranın uykuya geçmesini engelleme
- Çevrimdışı çalışma; uygulamada internet izni bulunmaz

## Kullanım

1. Uygulamayı açın ve mikrofon iznini verin.
2. Gerekirse A4 referans frekansını seçin.
3. **Dinlemeyi Başlat** düğmesine dokunun.
4. Enstrümanınızda tek bir nota çalın.
5. Nota adı, frekans ve cent sapmasını izleyerek sesi merkeze yaklaştırın.
6. İşiniz bittiğinde **Dinlemeyi Durdur** düğmesine dokunun.

En temiz ölçüm için cihazı enstrümana yakın tutun ve mümkün olduğunca sessiz bir ortam kullanın.

## Kurulum

Hazır APK dosyasını GitHub sayfasındaki **Releases** bölümünden indirin. Android, GitHub üzerinden indirilen APK için kurulum izni isteyebilir.

Gereksinimler:

- Android 7.0 veya üzeri (API 24+)
- Mikrofon erişimi

## Kaynak koddan derleme

Projeyi güncel Android Studio sürümüyle açın ve Gradle eşitlemesinin tamamlanmasını bekleyin. Komut satırından hata ayıklama APK'sı üretmek için:

```bash
./gradlew assembleDebug
```

Çıktı:

```text
app/build/outputs/apk/debug/app-debug.apk
```

Yayın derlemesi için:

```bash
./gradlew assembleRelease
```

> GitHub'a yüklemeye veya son kullanıcıya dağıtmaya yönelik yayın APK'sı, size ait güvenli bir Android imzalama anahtarıyla imzalanmalıdır. İmzalama anahtarlarını ve parolaları depoya eklemeyin.

## Teknik bilgiler

- Kotlin
- Jetpack Compose
- Material 3
- Android `AudioRecord`
- Minimum SDK: 24
- Hedef SDK: 37
- Uygulama kimliği: `com.emre.mutlakkulak`

## İzinler ve gizlilik

Uygulama yalnızca akort ölçümü yapabilmek için `RECORD_AUDIO` iznini ister. İnternet izni bulunmaz ve mikrofon verisini bir sunucuya göndermez. Ses, frekans tespiti amacıyla cihaz üzerinde anlık olarak işlenir.

## Proje yapısı

```text
app/src/main/java/com/emre/mutlakkulak/
├── MainActivity.kt        # Uygulama başlangıcı ve uyarlanabilir ölçekleme
├── AkordAleti.kt          # Arayüz, ses yakalama ve frekans analizi
└── ui/theme/Theme.kt      # Açık/koyu tema renkleri

app/src/main/res/
├── drawable-nodpi/        # Açık tema logo ve uygulama simgesi
└── drawable-night-nodpi/  # Koyu tema logosu
```

## Güncel sürüm

`v1.0.2` — Koyu tema logo görünürlüğü ve farklı ekran biçimlerindeki yerleşim iyileştirmeleri.

