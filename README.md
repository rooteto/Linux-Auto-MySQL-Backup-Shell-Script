# Linux Auto MySQL Backup Shell Script (Otomatik MySQL Yedeği Alma)
Bu script ile Linux sunucunuz veya hostlarınızın yedeklerini her gece alabilir ve rahat bir şekilde uyuyabilirsiniz. İleriye dönük yenilikler ekleyeceğim ama şimdilik bu bile çok faydalı bir script.

Hostlarınızın yedeği her zaman önemlidir. Günlük içerik girdiğiniz siteniz varsa bu iş daha önemlidir.

# Kullanımı

Scripti indirdikten sonra, Alttakileri dolduruyoruz. Bilgilere root şifresi de verebilirsiniz. root şifresi kullanıyorsanız bu scripti /root klasöründe gizleyin.

* host user / hosting kullanıcı adı, cpanel kullanıcı adı yada ftp kullanıcı adı.
* user / mysql veritabanı kullanıcı adı
* password / mysql password

Alttakilerin yollarını kendimize göre düzenliyoruz.

* backup_path / dizin yolunu belirtelim. alttaki de aynısı olsun.
* mkdir tarih / dizin yolunu belirtelim.

# Sunucuya cron çalıştırma sırasındayız.

Alttaki kod ile crontab'ı açıyoruz. Nano editörü ile açarsak iyi olur ben ona alışığım :)

```sh
export VISUAL=nano; crontab -e
```

Alttaki kodları sırasıyla hangisi işimize gelirse kullanalım.

1 dakikada bir sürekli çalışması için
```sh
*/1 * * * * /home/kullanici/backup/backup_bash.sh
```

30 dakikada bir sürekli çalışması için
```sh
*/30 * * * * /home/kullanici/backup/backup_bash.sh
```

Her gün gece 3:30 da çalışsın yedek alsın diyorsak
```sh
30 3 * * * /home/kullanici/backup/backup_bash.sh
```


### Küçük bir reklam.
* [Hosteva] - Hosting
* [rooteto] - Teknoloji
 
[Hosteva]: <http://www.hosteva.com>
[rooteto]: <http://rooteto.com>
