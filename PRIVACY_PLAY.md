# Nova Video İndir — Google Play Sürümü Gizlilik Politikası

Son güncelleme: 8 Ağustos 2026

Bu belge yalnız Google Play'e gönderilen `playLite` ve `playPro` varyantları içindir.

## Genel ilke
Nova Video İndir Google Play sürümü reklam SDK'sı, davranışsal analiz/telemetri SDK'sı, Nova hesabı veya Nova'ya ait zorunlu bir uzak kullanıcı-verisi sunucusu içermez. İndirme ve medya çözümleme işlemleri kullanıcının açık eylemiyle başlatılır.

## Cihazda işlenen veriler
- Kullanıcının verdiği medya bağlantıları ve Nova Browser içinde açtığı sayfalar.
- Dosya adı, format/kalite, indirme durumu ve seçilen hedef klasör.
- Kullanıcı açıkça yapılandırırsa platform çerez profilleri ile ilgili oturum verileri.
- Kullanıcı açıkça yapılandırırsa YouTube PO Token/Visitor Data gibi sağlayıcıya özgü değerler.
- Yerel hata günlükleri ve yalnız kullanıcı isterse oluşturulan tanılama raporu.

## Ağ iletişimi
Bir medya bağlantısı çözümlenirken veya indirirken uygulama, kullanıcının seçtiği üçüncü taraf site/sağlayıcı ile HTTPS üzerinden iletişim kurabilir. Bu sitelerin kendi gizlilik koşulları geçerlidir. Nova Video İndir bu sitelerin sunucularını işletmez.

## Yerel günlükler ve tanılama
Yerel günlükler uygulamanın özel alanında tutulur. Gizli belirteçler, çerezler, Authorization başlıkları ve tam hassas URL değerleri günlüklenmeden önce maskelenmeye çalışılır. Tanılama raporu yalnız kullanıcı tarafından dışa aktarılır; Nova'ya otomatik gönderilmez.

## Depolama ve silme
Uygulama ayarları, geçmiş ve geçici işler cihazda tutulur. Kullanıcı uygulama içinden geçmişi, günlükleri, tarayıcı verilerini ve desteklenen yerel verileri silebilir. Android, uygulama kaldırıldığında uygulamanın özel alanını normal şekilde siler. Kullanıcının genel İndirilenler klasörüne kaydettiği tamamlanmış dosyalar uygulama kaldırıldığında otomatik silinmez.

## Paketli motor ve çalışma zamanı kod politikası
Google Play varyantı yalnız uygulama paketiyle birlikte dağıtılan yt-dlp, yt-dlp-ejs ve QuickJS bileşenlerini çalıştırır. Uygulama Google Play sürümünde stable/nightly yt-dlp binary güncellemesi yapmaz, GitHub üzerinden EJS bileşeni indirmez ve kullanıcı tarafından içe aktarılan Python yt-dlp eklentilerini çalıştırmaz.

## Google Play sürümünde bulunmayan özellikler
Google Play varyantları şunları içermez/etkinleştirmez:
- APK indirme ve APK çeviri araçları,
- üçüncü taraf anonim Google Play teslimat istemcisi,
- uygulama dışından APK ile self-update/yükleme akışı,
- `SYSTEM_ALERT_WINDOW` isteyen dijital pet overlay servisi,
- `REQUEST_INSTALL_PACKAGES` ve `FOREGROUND_SERVICE_SPECIAL_USE` izinleri.

## İzinler
Google Play sürümü kişi, konum, kamera, mikrofon veya telefon kimliği izni istemez. İndirme görevleri için internet/ağ erişimi, bildirim, wake lock ve kullanıcı tarafından başlatılan indirmeyi görünür biçimde sürdürmek için `dataSync` foreground service izinleri kullanılabilir. Eski Android sürümlerinde genel depolama uyumluluğu için `WRITE_EXTERNAL_STORAGE` yalnız `maxSdkVersion=28` ile sınırlıdır.

## İletişim ve herkese açık politika adresi
Play Console'a gönderilecek sürümde `NOVA_PLAY_PRIVACY_URL` herkese açık bir HTTPS adresine ayarlanmalıdır. Uygulama Ayarlar ekranı bu adresi gösterebilir. Yayıncı iletişim bilgileri ve politika URL'si Play Console mağaza kaydıyla aynı tutulmalıdır.
