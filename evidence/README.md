# Ekran görüntüleri ve gözlemler

**Kurulum fotoğrafları 05–08:** [MIUI, TWRP, Magisk ve root erişimi günlüğü](../docs/kurulum-gunlugu.md).

Paylaşılan 15 ekran fotoğrafı incelendi; güncelleme ve ağ testlerini temsil eden 4 görüntü seçildi. Modem yönetim ekranları ve MAC/IPv6 adreslerini içeren ağ ayrıntıları bu galeriye alınmadı.

Görseller ekran içeriğine kırpıldı; dışarıdaki el, masa, telefon çerçevesi ve gereksiz klavye alanları çıkarıldı. Eğik çekimlerde perspektif düzeltildi. EXIF ve açıklama metaverileri kaldırıldı. Yazılar yeniden üretilmedi; yazıların altındaki ekran yansımaları korundu. Bu dosyalar düzenlenmiş sunum kopyalarıdır; özgün fotoğraflar önceki Git sürümünde bulunur. Aşağıdaki numaralar sunum sırasıdır; çekim zamanının kesin kanıtı değildir.

## 01 — Paket güncelleme çıktısı

<img src="01_nethunter_paket_guncelleme.jpeg" alt="NetHunter paket kurulumu ve hata mesajları" width="640">

`kali-nethunter-full (2026.4.2)` için “Setting up” satırı ve terminal istemine dönüş görünüyor. Bunun yanında `dpkg-realpath` için `/bin` sembolik bağlantı hataları, D-Bus bağlantı hatası ve runlevel uyarısı bulunuyor. Bu görüntü hatasız bir yükseltme veya tüm NetHunter özelliklerinin çalıştığı anlamına gelmez.

## 02 — Misafir ağı bağlantısı

<img src="02_android_misafir_agi.jpeg" alt="Android guest ağı bağlantı durumu" width="640">

Android ağ ayrıntılarında `guest` ağına bağlı durum, 2.4 GHz ve WPA/WPA2-Personal bilgisi görünüyor. Bu ekran bağlantıyı gösterir; ağlar arasında erişim kısıtlamasının etkin olduğunu kanıtlamaz. “Paylaş” simgesi bir bağlantı QR kodu değildir.

## 03 — Ağ geçidine ping

<img src="03_nethunter_ag_gecidi_ping.jpeg" alt="Yerel ağ geçidine dört paketlik ping testi" width="640">

`ping -c 4 192.168.1.1` sonucunda 4 paket gönderilmiş, 4 yanıt alınmış ve %0 paket kaybı görülmüş. Bu test hedefin ICMP ile erişilebilir olduğunu gösterir.

**Komutun amacı:** Yerel hedefe erişimi kontrol etmek. **Flag:** `-c 4`, testi dört istekle sınırlar.

## 04 — İkinci yerel hedefe ping

<img src="04_nethunter_yerel_hedef_ping.jpeg" alt="İki yerel IP adresine başarılı ping sonuçları" width="640">

Ekranda hem `192.168.1.1` hem `192.168.1.5` için 4/4 yanıt ve %0 kayıp görülüyor. İkinci adresin hangi cihaza ait olduğu bu görüntüden tek başına belirlenemez. Eğer bu hedef ana ağdaki bir cihazsa ve test misafir ağından yapıldıysa, sonuç o hedefe ICMP erişiminin engellenmediğini gösterir. Bu nedenle izolasyon başarısı iddia edilmez.

## Dosya bütünlüğü

SHA-256 değerleri yayımlanan, kırpılmış ve metaverisi temizlenmiş sunum kopyalarına aittir.

| Dosya | SHA-256 |
| --- | --- |
| 01_nethunter_paket_guncelleme.jpeg | `69e2f15fbe15556ce3b23ce263a533781cc8765ea67da7fc089174962901aabe` |
| 02_android_misafir_agi.jpeg | `95dd1d5ae189500de8898c389ff8ae5b322b35176ba4f75fff82fb5764319976` |
| 03_nethunter_ag_gecidi_ping.jpeg | `4d86565a60b02bad1233d9f57164f65fd5d3c31b34bb09dd126802dc69681930` |
| 04_nethunter_yerel_hedef_ping.jpeg | `e896b444709552815ccfea850e267dabed0418a3dc746acbac34bad9d6dc0ecc` |

[Proje ana sayfasına dön](../README.md)
