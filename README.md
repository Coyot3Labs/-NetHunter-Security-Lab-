# NetHunter Security Lab

Coyot3Labs kapsamında Redmi Note 8 üzerinde yürütülen Kali NetHunter kurulum ve öğrenme çalışmalarının kaydı.

## Amaç

- Mobil güvenlik ve Linux temellerini öğrenmek.
- Kurulum sorunlarını ve çözümlerini tekrar kullanılabilir notlara dönüştürmek.
- İzinli laboratuvar çalışmalarını sonuçlarıyla birlikte belgelemek.

Testler yalnızca sahip olunan veya açıkça izin verilen sistemlerde yapılır.

## Laboratuvar ortamı

| Bileşen | Çalışma kaydı |
| --- | --- |
| Telefon | Xiaomi Redmi Note 8 (`ginkgo`) |
| İşletim sistemi | ArrowOS, Android 13 |
| Recovery | TWRP 3.7.1_12-0, ginkgo |
| Root yönetimi | Magisk 31.1 |
| Terminal ortamı | Termux ve NetHunter terminali |
| Kali erişimi | Kali terminalinin açıldığı ve `uid=0` çıktısı alındığı kullanıcı tarafından bildirildi |

## Kurulum ve sorun giderme özeti

1. TWRP dosyasının SHA-256 doğrulaması yapıldı; ArrowOS Android 13 kuruldu.
2. Magisk kuruldu. Termux root erişimindeki izin sorunu, superuser izninin düzenlenmesiyle giderildi.
3. NetHunter Store ve BusyBox NDK v1.36.1 indirildi. İndirilmiş olmaları, tüm bileşenlerin kurulu ve etkin olduğunu tek başına doğrulamaz.
4. NetHunter uygulamalarının görünürlüğü ve terminal erişimi üzerinde çalışıldı. Ana uygulamanın uygulamalar listesinde görünmesine rağmen ana ekranda görünmemesi ve başlangıçta terminal uygulamasının bulunmaması kaydedilen sorunlardı.
5. NetHunter terminali eklendi; Kali terminaline erişim sağlandı. Root kullanıcı kontrolünde `uid=0` görüldüğü bildirildi.
6. Paket güncelleme çalışması yapıldı. Tüm yükseltmelerin başarıyla tamamlandığı bu kayıtta doğrulanmış değildir.
7. Ev ağı için misafir ağı üzerinden ayırma konusu ele alındı. Ana ağdan izolasyon henüz doğrulanmış bir test sonucu olarak kaydedilmemiştir.

## Doğrulama sınırları

Kali terminalinin açılması ve `uid=0` görülmesi, NetHunter Full özelliklerinin tamamının çalıştığını kanıtlamaz.

| Özellik | Durum |
| --- | --- |
| Kali terminaline erişim | Kullanıcı bildirimiyle çalışıyor |
| Terminalde root erişimi | `uid=0` görüldüğü bildirildi |
| Özel NetHunter kernel kurulumu | Doğrulanmadı |
| Wi-Fi monitor mode | Doğrulanmadı |
| Wi-Fi paket enjeksiyonu | Doğrulanmadı |
| USB HID desteği | Doğrulanmadı |
| Misafir ağı izolasyonu | Doğrulanmadı |

## Sıradaki çalışmalar

- [ ] Kernel sürümünü ve NetHunter sürümünü kaydetmek.
- [ ] Paket güncelleme durumunu kontrol etmek.
- [ ] Misafir ağı ile ana ağ arasındaki izolasyonu izinli laboratuvar kapsamında doğrulamak.
- [ ] Desteklenen donanım özelliklerini ayrı ayrı test edip sonuçlarını belgelemek.
- [x] Güncelleme ve ağ testlerinden seçilmiş 4 ekran fotoğrafını inceleyip açıklamalarıyla eklemek.

## Kanıt ve kayıt durumu

Bu özet, çalışma sırasında paylaşılan kurulum bilgileri ve kullanıcı bildirimlerinden hazırlanmıştır; cihazın canlı denetimi değildir. Seçilmiş 4 ekran fotoğrafı açıklamalarıyla [kanıt galerisinde](evidence/README.md) yayımlanmıştır. Ham terminal metinleri henüz eklenmemiştir. Kesin nedenleri belirlenmemiş hata mesajları için çözüm veya kök neden iddiasında bulunulmaz.

Paylaşılacak kanıtlarda parola, erişim anahtarı, oturum bilgisi ve kişisel ağ tanımlayıcıları bulunmamalıdır.

## Ekran görüntüleri

[Numaralı kanıt galerisini aç](evidence/README.md).

Galeri; paket güncelleme çıktısı, misafir ağı bağlantısı ve iki yerel ping testini içerir. Güncelleme çıktısındaki hata mesajları korunmuştur; misafir ağı izolasyonu başarılı olarak değerlendirilmemiştir.

Son dokümantasyon güncellemesi: 3 Kasım 2026.
