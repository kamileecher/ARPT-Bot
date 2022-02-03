
# Sürüm notları

v2.0.9

rclone'un çağırma yöntemini değiştirin ve rc http api çağrısı olarak değiştirin.

[RcloneNg](https://github.com/ElonH/RcloneNg) için destek eklendi.

rclone rc'yi eşleyin, rclone rc'de özel işlemi destekleyin, lütfen [rclone rc öğreticisine] bakın(https://rclone.org/rc/)

***
Bu sürümden sonra otomatik güncellemeler desteklenmektedir.Python dosyalarındaki değişiklikler sadece yeniden başlatılarak güncellenebilir ve diğer donanım güncellemeleri docker üzerinden güncellenecektir.

aria2 panelinde eklenen görevler ile yerel dosyanın silinmesine neden olan conf dosyasının yapılandırması arasındaki çakışmayı düzeltin [#18](https://github.com/666wcy/ARPT-Bot/issues/18)[ #16](https://github .com/666wcy/ARPT-Bot/issues/16)

Odprivate komutunun geçersiz kılınmasını düzeltin (sonraki komutlarla çakışma olması komutun başarısız olmasına neden olur) [#17](https://github.com/666wcy/ARPT-Bot/issues/17)

Varsayılan panel hesabı şifresini onarın varsayılandır, bir güvenlik riski vardır, bunu hesaba değiştirin: `admin`, şifre: ayarladığınız `Aria2_secret` değeri


Boyut tg api gereksinimlerini karşılamadığından ve boyutu karşılamayan görüntülerin gönderilmesi iptal edildiğinden pixiv tg'ye gönderildiğinde oluşan bir hata düzeltildi.

İndirme kartının %99 olasılık sorununu çözmeye çalışın, etkisi bilinmiyor.

NetEase Cloud Music indirmesi eklendi, şu anda arama indirmeyi, kimlik indirmeyi, tüm oynatma listesini indirmeyi destekliyor, tg'ye göndermeyi ve ağ diskine yüklemeyi destekliyor. API arayüzü projesi: [NeteaseCloudMusicApi](https://github.com/Binaryify/NeteaseCloudMusicApi), şu anda kendi API'mi kullanıyor, vinil üyeler var ve gelecekte özel API adreslerini destekleyecek.

QQ Music'in kararlı bir arayüz projesi varsa, Bot ile yerleştirmeyi de önerebilirsiniz.

![](https://cdn.jsdelivr.net/gh/666wcy/img_share@main/img/xxx.6kk2hr659yw0.png)

![](https://cdn.jsdelivr.net/gh/666wcy/img_share@main/img/image.l6bobb2z9vk.png)

![](https://cdn.jsdelivr.net/gh/666wcy/img_share@main/img/image.7b3nuhohe4o0.png)

v1.1.6

将pixivtop命令更改为pixivtopall,优化按键选择方式，新增插画榜和男性榜、女性榜、新人榜、原创榜，支持指定日期榜单下载

![](https://cdn.jsdelivr.net/gh/666wcy/img_share@main/img/image.1q6zlq2sggow.png)

v1.1.5

pixivuser, pixivusertg, pixivuserphoto, pixivusertele'yi iptal et

Tek bir komutla optimize edildi pixivauthor

![](https://cdn.jsdelivr.net/gh/666wcy/img_share@main/img/image.7huyt6u0ne40.png)

Pixiv sıralamalarının indirilmesi eklendi (günlük, aylık, haftalık) ve gelecekte illüstrasyonlar, erkek ve kadın sıralamaları eklenecek

![](https://cdn.jsdelivr.net/gh/666wcy/img_share@main/img/image.1iniuqwtbojk.png)

v1.1.4

Dosya yolunun Aria2'ye gönderilmesini sağlayarak OneDrive genel paylaşım bağlantısındaki dosyaların indirilmesi eklendi. Proje adresi: [OneDriveShareLinkPushAria2](https://github.com/gaowanliang/OneDriveShareLinkPushAria2)

**downtgfile** komutunun videoyu indiremediği hatayı düzeltin

/rclone komutunun görüntüsünü optimize edin

</details>


# tanıtım

Python3 tabanlı bir Bot. Şu anda Docker yolu ile vps üzerinde konuşlandırılması desteklenmektedir.

[![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=666wcy&repo=ARPT-Bot)](https://github.com/666wcy/ARPT-Bot)

Ana işlev:

- [X] Dosya yönetimi
  - [X] Ana arayüzü [filebrowser](https://github.com/filebrowser/filebrowser) olarak değiştirin, hesap **admin**, şifre 'Aria2_secret' sizin tarafınızdan belirlenir, ana arayüz yolu: http:// /ip:port, lütfen şifreyi kendiniz değiştirin

- [X] Web Paneli
  - [X] https://ip:port/ng/ adresinde [AriaNg](https://github.com/mayswind/AriaNg) panelini destekleyin
  - [X] Daha hafif olan orijinal Python Flask'ı değiştirmek için dahili bağlantı noktası olarak **Nginx** kullanın
- [X] Destek [RcloneNg](https://github.com/ElonH/RcloneNg), oturum açma adresi 'http://ip:port', lütfen 'ip' ve 'port'u değiştirin, kullanıcı adı root'tur , şifre `Aria2_secret` sizin tarafınızdan belirlenir


- [X] Aria2
  - [X] Aria2'nin otomatik kurulumu, özel anahtar
  - [X] Bot ile basit Aria2 kontrolü (görev ekle, görevi duraklat, görevi sil)
  - [X] Toplu ekleme görevlerini destekleyin
  - [X] İndirme ilerlemesini göster
  - [X] Görev tamamlandıktan sonra rclone üzerinden yükleyin (**yükleme ilerlemesini görüntüleyin**), rclone'un en son sürümü zaten 21Vianet'i destekliyor
  - [X] aria2 panel aracı rpc bağlantısını destekler (al, gönder)
  - [X] Panel araçlarının rpc bağlantısıyla eklenen görevlerin otomatik olarak yüklenmesini destekler (ilerlemeyi gösterme). Panel üzerinden eklenen görevin yükleme yöntemini P boyutunda yükleme komut dosyasına değiştirin ve orijinal yolu koruyun.
  - [X] İzleyicileri otomatik olarak eklemek için P-büyük konfigürasyonu kullanın.
  - [X] Dosyaları OneDrive'da indirin, ortak paylaşım bağlantılarını paylaşın, dosya yolunu koruyun ve Aria2'ye gönderin. Proje adresi: [OneDriveShareLinkPushAria2](https://github.com/gaowanliang/OneDriveShareLinkPushAria2)
  - [ ] Rss otomatik olarak indirilir, bitmiş ürün zaten mevcuttur, ancak henüz bağlanmamıştır

- [X] Rclone
  - [X] rclone resmi lsd, lsf yöntem uyarlaması
  - [X] rclone kopyasının uyarlanması, yani iki disk arasında karşılıklı aktarım, aktarım ilerlemesini görüntüleme desteği
  - [X] Dosyaları rclone copyurl ile yükleyin, ilerlemeyi gerçek zamanlı olarak görüntüleyin
  - [X] aria2 panel aracı rpc bağlantısını destekler (al, gönder)
  - [ ] rclone dizinini görüntülemek için TG düğmesi
  - [ ] Geçerli dizin dosyasını emby tarama formatı olarak adlandırın
  - [ ] Robot aracılığıyla rclone yapılandırması ekleyin ve rclone yapılandırmasını temizleyin
  - [ ] Tekli veya çoklu klasörlerin paylaşım bağlantısını (gd,od) alın
  
- [X] Pixiv
  - [X] pid'e göre görüntü al
  - [X] Sanatçının tüm eserlerini indirin, ağ diskine yüklemeyi destekleyin, tg'yi paketleyin ve gönderin, resim ile tg gönderin ve telgrafla resim gönderin (web sayfası). Paketleme formatı zip şeklindedir.
  - [X] Günlük sıralamaları, haftalık sıralamaları, aylık sıralamaları indirin, ağ diskine paket yüklemeyi destekleyin, tg'yi paketleyin ve gönderin, tg'yi resim olarak gönderin ve telgrafla (web sayfası) resim gönderin. Paketleme formatı zip şeklindedir.
  - [X] Belirtilen tarihte destek listesi indirme

- [X] Videoyla ilgili
  - [X] Videoları indirmek, ağ diskine yüklemeyi desteklemek veya tg'ye göndermek için YouTube-dl'yi kullanın. Şu anda YouTube ve Bilibili'ye mükemmel şekilde uyarlanmış varsayılan en yüksek resim kalitesi (hayran dramaları hariç)
  - [X] Netease bulut müzik indirme, destek kimliği indirme, indirme arama, tüm oynatma listesini indirme, tg'ye gönderme ve ağ diskine yükleme desteği
  - [X] Göndermek ve yüklemek için videoyu MP3 formatına dönüştürme eklendi
  - [ ] Video ve altyazı karışımı
  - [ ] Yaygın olarak kullanılan ses ve video biçimleri

- [X] Telgraf
  - [X] Yalnızca geçerli kullanıcının komutu geçerli olur
  - [X] Dosyayı almak için dosya kimliği gönder
  - [X] Dosya kimliğini almak için dosya gönder
  - [X] Ağ diskine yüklemek için TG dosyası gönder
  - [X] Bot'un çalışma süresini ve kalan alanı görüntülemek için destek komutu
  - [X] Gruplar içinde kullanımı destekler. Not: Bir grup versiyonu var ve nasıl karıştırıp adapte edeceğimi düşünüyorum
  - [ ] Bot beyaz listesi ekle

- [X] Resimle ilgili
  - [X] Birleştirilmiş [Arama Botu](https://github.com/666wcy/search_photo-telegram-bot-heroku), destek [saucenao](https://saucenao.com/), [WhatAnime](https : //trace.moe/), [ascii2d](https://ascii2d.net/), [iqdb](http://www.iqdb.org/)
  - [X] Bika'nın kitabını arayın ve indirin, TG'ye göndermek ve ağ diskine yüklemek için ZIP dosya biçimini destekleyin
  - [X] [nhentai](https://github.com/RicterZ/nhentai) ile bağlantı, nhentai kitabını indirin ve TG'yi ZIP dosya formatında göndermeyi, ağ diskini ZIP formatında yüklemeyi ve TG'ye web sayfası formatında göndermeyi destekler
  - [X] Kitap arama, beeka, ehentai, nhentai desteği
  - [X] soapnao arama haritası hızlı aramayı destekler

 




# <p align=center>```ARPT-Heroku```</p>
<p align=center><a href="https://dashboard.heroku.com/new?button-url=https://github.com/kamileecher/TEST/Rclone-Heroku&template=https://github.com/kamileecher/TEST"><img src="https://www.herokucdn.com/deploy/button.svg" width="200"></a></p>

> 1. Tek zorluk, [buradan](https://my.telegram.org) başvuruyu kaydettikten sonra TG'nin APP kimliği ve hash'i için başvurmak olabilir.
> 2. Telegram_user_id Kullanıcının @userinfobot'tan alınabilecek TG kimliği.Grup kimliğine ayarlanırsa, grubun tüm üyeleri kullanılabilir olacaktır.Bot'un grup iznini ayarlamanız gerekir
> 3. Rclone_share boş bırakılabilir, True, ağ diskini yükledikten sonra paylaşım bağlantısını (onedrive) döndürmek anlamına gelir, False bu işlevi kapatmak anlamına gelir, bu değişken ayarlanmamışsa varsayılan olarak kapalıdır
> 4. Error_user_info boş bırakılabilir.Kullanıcıların mesaj göndermesine izin verilmediğinde bir istem ayarlayabilirsiniz.Bu değişken ayarlanmazsa, varsayılan ifade kullanılacaktır.
> 5. Kalan sorunlar: 1. Web sayfası şifre sorunu 2.rclone.conf sorunu 3.jsonrpc sorunu
> 6. İyileştirmeler: 1. Büyük bir P ile aira2'ye geçin 2. Web sayfaları çalışabilir 3. jsonrpc çalışabilir
> 7. Bekleyip görmeye devam edin, sorunlar olmalı
---
Komutu @BotFather'da ayarlayarak (kaynak kodun eski versiyonu, karşılık gelen komut mevcut olmayabilir)
```
start - Bot durumunu görüntüle
help - Bot'u kullanmak için yardım alın
pixivauthor - pixiv sanatçılarının eserlerini değiştir
pixivtopall - pixiv skor tablolarında çalıştır
pixivtopillust - Illustrator Lider Tablolarını Değiştir
pixivpid - pixiv'e bu kimliğe sahip resmi gönder
magfile - torrent dosyasını aria2'ye itin ve ağ diskine yükleyin
mirror - aria2'ye doğrudan bağlantı gönder, indir ve ağ diskine yükle
mirrortg - aria2'yi indirmek için doğrudan bağlantıyı itin ve TG'ye gönderin
magnet - indirmek ve ağ diskine yüklemek için bir mıknatıs bağlantısını aria2'ye itin
downtgfile - TG dosyası gönder ve ağ diskine yükle
rclonecopy - rclone ile ağ diskleri arasında aktarım
rclonelsd - Ağ disk klasörlerini rclone ile görüntüle
rclone - Klasör ayrıntılarını rclone ile görüntüle
rclonecopyurl - Düz zincir dosyalarını doğrudan rclonecopyurl ile yükleyin
getfileid - dosya kimliğini almak için dosya gönderir
getfile - dosyayı almak için fileid gönder
video - bir video bağlantısı gönder
neteaseid - kimliğe göre şarkı bilgisi al
searchsong - NetEase Bulut Müzik Şarkılarını Ara
playlist - çalma listesi bilgilerini al
odshare - Herkese açık od, sp paylaşım bağlantı dosyalarını indirin ve ağ diskine yükleyin
odprivate - İndirme alanındaki od ve sp paylaşım bağlantılarını indirin ve ağ diskine yükleyin
nhentai - nhentai'deki kimliğe karşılık gelen kitabı indir
ehentai - nhentai'deki kimliğe karşılık gelen kitabı indir
picacgsearch - Kitabı Bika'da arayın, ağ diskine ZIP yüklemesini destekleyin ve TG'ye gönderin
ehentaisearch - ehentai'de kitap arayın, ağ diskine ZIP yüklemesini destekleyin ve TG'ye gönderin, web sayfası gönderin
nhentaisearch - nhentai'de kitap arayın, ağ diskine ZIP yüklemesini destekleyin ve TG'ye gönderin, web sayfası gönderin
```
