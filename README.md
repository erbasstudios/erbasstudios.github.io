# erbasstudios.github.io — site dosyaları

Bu klasör, `erbasstudios/erbasstudios.github.io` reposunun **birebir aynısı** olacak şekilde tutulur. Buradaki
dosyaları olduğu gibi reponun köküne yükle; yapı bozulmaz.

## Yapı

```
/                        https://erbasstudios.github.io/
├── index.html           stüdyo ana sayfası, oyunları listeler
├── app-ads.txt          AdMob yayıncı doğrulaması — ZORUNLU olarak kökte (bu klasörde yok, repoda duruyor)
├── gizlilik.html        Yumo'nun politikası — eski bağlantı, taşıma (Play Console'da kayıtlı)
└── rainroutes/
    └── privacy.html     Rain Routes'un politikası
```

Yeni bir oyun eklerken: köke `<gameid>/privacy.html` aç ve `index.html`'e bir kart ekle. Başka bir şey
gerekmez.

## Kurallar

**Dosya ve klasör adları İngilizce.** Site iki mağazaya ve her ülkeye bakıyor; adres çubuğunda ve mağaza
formlarında görünen her şey İngilizce olur (`privacy.html`, `rainroutes/`). Sayfaların **içeriği** iki dilli
kalır, İngilizce önce. Kökteki `gizlilik.html` bu kuralın dışında: Yumo'nun yayındaki bağlantısı, taşınmıyor.

**`app-ads.txt` kökten çıkmaz.** IAB standardı onu `https://<alan-adı>/app-ads.txt` adresinde arar; alt klasöre
konursa AdMob doğrulaması kırılır. İçindeki yayıncı kimliği bütün oyunlar için ortaktır, oyun eklenince
değişmez.

**Yayında olan bir URL taşınmaz.** `gizlilik.html` Yumo'nun Play Console kaydında duruyor; kökten
`yumo/gizlilik.html`'e taşınırsa o bağlantı kırılır. Taşımak istersen önce Console'daki URL'i güncelle.

**Her oyunun kendi politikası olur.** Oyunlar farklı veri topladığı için ortak politika yanlış beyan olur:
Yumo AdMob kullanıp reklam kimliği topluyor, Rain Routes bugün hiçbir şey toplamıyor.

## Yükleme

GitHub'da repo → Add file → Upload files → bu klasörün içeriğini sürükle → commit. Pages ayarı zaten açık,
değişiklik birkaç dakikada yayına girer.

## Alan adı alınırsa

`erbasstudios.com` gibi bir alan adı alınırsa yapı aynen korunur: repo Settings → Pages → Custom domain'e
yazılır, `app-ads.txt` yeni alan adının kökünde yayınlanır ve AdMob'daki geliştirici sitesi alanı güncellenir.
Politika URL'leri değişeceği için Play Console ve App Store Connect kayıtları da güncellenmelidir.
