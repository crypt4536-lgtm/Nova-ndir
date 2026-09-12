# Nova Video İndir — Bağımsız Sürüm Gizlilik Politikası

Son güncelleme: 8 Ağustos 2026

Bu belge `independentLite` ve `independentPro` varyantları içindir. Google Play sürümünden farklı olarak bağımsız dağıtım, APK araçları, self-update ve isteğe bağlı dijital pet overlay özelliklerini içerebilir.

## Ortak medya/indirme verileri
Kullanıcının verdiği medya bağlantıları, Nova Browser sayfaları, dosya adı/format/kalite, hedef klasör, indirme geçmişi ve yerel tanılama bilgileri cihazda işlenebilir. Kullanıcı açıkça yapılandırırsa platform çerezleri, PO Token/Visitor Data veya sağlayıcı ayarları cihazın özel alanında saklanabilir.

## APK araçları
Kullanıcı APK indirme/çeviri araçlarını açtığında üçüncü taraf web hizmetleri veya Google Play teslimat protokolüyle ağ iletişimi oluşabilir. APK çeviri özelliği seçilen dosyayı geçici olarak özel önbelleğe kopyalayabilir; çeviri modeli gerekiyorsa Google ML Kit model indirmesi yapabilir. Tamamlanan çıktılar kullanıcı tarafından seçilen/genel indirme klasöründe kalabilir.

## Bağımsız Google Play teslimatı
Bu özellik Google hesabı parolası istemeden anonim/geçici oturum elde etmek için yapılandırılmış bir HTTPS dispenser hizmetine cihaz uyumluluk bilgileri gönderebilir. Paket adı ve cihaz uyumluluk profili Google Play altyapısına iletilebilir. Özellik yalnız bağımsız varyantta bulunur ve üçüncü taraf/belgelenmemiş protokollere bağlı olduğundan kullanılabilirlik garantisi yoktur.

## Güvenli self-update
Kullanıcı otomatik güncelleme denetimini etkinleştirirse uygulama, yapılandırılmış HTTPS manifest adresini kontrol edebilir. İmzalı güncelleme manifesti doğrulanır; APK SHA-256, paket adı ve imza uyuşması kontrol edilir. Android, APK yüklemek için kullanıcıdan “bu kaynaktan yüklemeye izin ver” onayı isteyebilir.

## Dijital pet overlay
Dijital pet yalnız kullanıcı etkinleştirirse `SYSTEM_ALERT_WINDOW` ve `specialUse` foreground service ile çalışır. Kullanıcı Android ayarlarından overlay iznini kaldırabilir veya uygulama içinden özelliği kapatabilir.

## Yerel günlükler, saklama ve silme
Günlükler ve tanılama verileri yereldir ve otomatik olarak Nova sunucusuna gönderilmez. Kullanıcı geçmişi, yarım dosyaları, günlükleri, tarayıcı verilerini, çerez profillerini ve desteklenen eklenti/pet paketlerini silebilir. Genel indirme klasörüne yazılmış dosyalar uygulama kaldırıldığında otomatik silinmez.

## İletişim
Bağımsız dağıtım için `NOVA_INDEPENDENT_PRIVACY_URL` ile ayrı bir herkese açık HTTPS politika adresi yapılandırılabilir. Bu adres boşsa derleme Play gizlilik URL'sini yedek olarak kullanır.
