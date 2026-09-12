# Nova Video İndir — Google Play Data Safety Çalışma Formu

Bu belge Play Console'a otomatik gönderilmez. Checkpoint 038 `playLite` / `playPro` release AAB'lerinin gerçek davranışı ve üçüncü taraf SDK'larıyla son kez karşılaştırılarak Play Console formuna aktarılmalıdır.

## Binary kapsamı
Google Play varyantları:
- reklam/analitik SDK'sı içermez,
- Nova hesabı veya Nova kullanıcı-verisi backend'i içermez,
- APK indirici/çevirici, anonim Play teslimatı ve self-update kaynaklarını derlemez,
- dijital pet overlay servisini/izinlerini derlemez veya manifestte beyan etmez.

## Paketli yürütme bileşenleri
Play Lite/Pro, AAB içinde gelen yt-dlp + yt-dlp-ejs + QuickJS bileşenlerini kullanır. Runtime motor güncellemesi, uzaktan EJS bileşen indirme ve üçüncü taraf Python plugin yükleme Play varyantında devre dışıdır.

## Play Console'da doğrulanacak veri akışları
1. **Kullanıcı tarafından verilen URL/arama-medya girdileri:** Kullanıcının istediği medya sitesine ağ isteği yapmak için kullanılabilir. Üçüncü taraf siteye gönderim, kullanıcının talep ettiği uygulama işlevini yerine getirmek içindir.
2. **WebView/site verileri ve çerezler:** Nova Browser ile ziyaret edilen üçüncü tarafların kendi çerez/site depolaması olabilir. Kullanıcı bu verileri temizleyebilir.
3. **İsteğe bağlı hesap/oturum verileri:** Kullanıcı açıkça içe aktarır veya yapılandırırsa seçili medya sağlayıcısına yapılan istekte kullanılabilir; Nova backend'ine otomatik gönderilmez.
4. **Tanılama:** Yerel günlük/tanılama raporu otomatik yüklenmez; yalnız kullanıcı dışa aktarır ve paylaşım hedefini kendisi seçer.
5. **Dosyalar:** İndirilen içerik cihazda kullanıcının seçtiği konuma yazılır; Nova sunucusuna yüklenmez.

## Formu doldururken kontrol listesi
- “Data collected/shared” cevaplarını yalnız kaynak koda bakarak değil, Play release AAB içindeki tüm SDK davranışlarına göre verin.
- HTTPS üzerinden üçüncü taraf medya sitesine yapılan kullanıcı-işlevli ağ aktarımının Play'in güncel Data Safety tanımlarındaki istisna/kapsamını Play Console açıklamasıyla eşleştirin.
- WebView ve kullanıcı tarafından sağlanan oturum/çerez verilerini ayrıca değerlendirin.
- Veri şifreleme, silme, hesap oluşturma ve çocuk/target-audience cevaplarını mağaza davranışıyla tutarlı tutun.
- `PRIVACY_PLAY.md` ile Data Safety cevapları çelişmemelidir.

## 038'in güvenli varsayımı
Bu dosya kasıtlı olarak “hiç veri toplanmıyor” şeklinde otomatik bir beyan üretmez. Play Data Safety sınıflandırması, gerçek release binary ve Play Console'un o tarihteki soru metinleri görülmeden kesinleştirilmemelidir.
