# Nova Video İndir 053 — Google Play Yayın Kontrol Listesi

## Derlemeden önce
- [ ] `NOVA_KEYSTORE`, `NOVA_KEY_ALIAS`, `NOVA_STORE_PASSWORD`, `NOVA_KEY_PASSWORD` ayarlı.
- [ ] `NOVA_PLAY_PRIVACY_URL` herkese açık, erişilebilir bir HTTPS adresi ve `PRIVACY_PLAY.md` ile aynı içerikte.
- [ ] Play Console uygulama kimlikleri planla uyumlu: Lite `com.nova.indir.lite`, Pro `com.nova.indir.pro`.
- [ ] Store listing, destek e-postası/iletişim bilgileri tamam.

## Teknik yayın kapıları
- [ ] `compileSdk=36`, `targetSdk=36`, versionCode=55, checkpoint=053.
- [ ] `:app:bundleNovaPlayRelease` başarılı.
- [ ] `:app:checkNovaPlayMergedManifests` başarılı.
- [ ] `:app:checkNovaPlayPublicationConfig` başarılı.
- [ ] AAB içinde `yt_dlp_ejs/yt/solver/core.min.js` ve ARM64 QuickJS bulunuyor.
- [ ] Play varyantı runtime yt-dlp update, remote EJS ve Python plugin çalıştırmıyor.
- [ ] `VERIFY_PLAY_RELEASE.ps1` sonunda 16 KB raporu `OVERALL RESULT: PASS`.
- [ ] Play AAB içinde bağımsız-only APK/update/overlay sınıfları ve izinleri yok.
- [ ] Play App Signing etkin ve kullanılan upload key güvenli biçimde yedekli.

## Play Console App content
- [ ] Privacy policy URL.
- [ ] Data Safety formu (`DATA_SAFETY_PLAY.md` ile gerçek AAB/SDK davranışı karşılaştırılarak).
- [ ] Foreground Service declaration: yalnız gerçek Play binary'deki `dataSync` kullanım(lar)ı ve demo video.
- [ ] Ads declaration (uygulama reklam göstermiyorsa buna uygun cevap).
- [ ] App access (oturum zorunlu değilse buna uygun cevap; gerekiyorsa inceleme erişimi).
- [ ] Target audience / children policy cevapları.
- [ ] Content rating anketi.
- [ ] News/health/financial vb. özel beyanlar yalnız uygulama kapsamına giriyorsa.

## Test ve yayın
- [ ] Gerçek cihazda Lite + Pro: link çözümleme, İndir düğmesi, kuyruk, foreground bildirim, iptal, tamamlanan dosya.
- [ ] Android 14/15/16 üzerinde kritik akış smoke test.
- [ ] Play Console pre-launch report incelendi.
- [ ] Hesap türü/oluşturulma tarihine göre kapalı test şartı uygulanıyorsa gereken tester/süre tamamlandı.
- [ ] Geliştirici doğrulaması ve paket kaydı Play Console/Android Developer Console'da tamamlandı; 30 Eylül 2026 paket-kayıt gerekliliği gözden geçirildi.

## Son karar
Bu listedeki teknik ve Console maddeleri tamamlanmadan “Google Play'e tam hazır” kabul etmeyin.
