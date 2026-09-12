# Nova Video İndir Checkpoint 053 Raporu

## Kimlik

- Sürüm: `0.53`
- versionCode: `55`
- Checkpoint: `053`
- Ürün adı: `Nova Video İndir`
- Dağıtımlar: `Google Play` ve `Bağımsız`

## Google Play

- `compileSdk=36`, `targetSdk=36`, `minSdk=26`.
- Play Lite/Pro aynı ortak Nova tarayıcı, medya çözümleme, kuyruk, hesap/çerez, galeri, Nova Player ve indirme motorunu taşır.
- APK indirme/yükleme, self-update ve pet overlay Play source-set'inde yoktur.
- Runtime Python plugin import/çalıştırma Play'de yoktur.
- `--remote-components ejs:github` Play'de kullanılmaz.
- Runtime stable/nightly yt-dlp update Play'de kullanılmaz.
- Play motoru AAB ile gelen yt-dlp + yt-dlp-ejs + QuickJS bileşenlerine sabitlenmiştir.
- Play release görevi signing, public HTTPS privacy URL ve merged manifest denetim kapılarına bağlıdır.

## Bağımsız

Bağımsız Lite/Pro, karşılık gelen Google Play Lite/Pro ortak özelliklerinin tamamını taşır. Ek olarak APK araçları, self-update, pet overlay, runtime yt-dlp update/rollback, plugin ve remote-EJS seçenekleri korunur.

## Temiz teslim adları

- `Nova Video İndir 0.53 Google Play Lite.aab`
- `Nova Video İndir 0.53 Google Play Pro.aab`
- `Nova Video İndir 0.53 Bağımsız Lite.apk`
- `Nova Video İndir 0.53 Bağımsız Pro.apk`
- `Nova Video İndir 053 Kaynak.zip`
