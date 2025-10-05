
🕌 Moschee TV Display – Kurulum Rehberi (Graz)

Bu paket, cami TV ekranında NAMAZ VAKİTLERİ + DUYURULAR + HAVA DURUMU göstermek için hazırlandı.
Dosya: index.html (tek sayfa) – internet bağlantısı gerektiği anda Aladhan ve Open-Meteo'dan verileri çeker.

1) Kullanım (en basit yol – Windows):
   - Klasörü bir yere kopyalayın (ör. C:\MoscheeTV).
   - index.html dosyasını çift tıklayıp açın.
   - Tam ekran için: F11 (Chrome/Edge).
   - Bilgisayar açıldığında otomatik başlatmak için: Win+R → shell:startup → bu klasöre index.html kısayolu koyun.
   - İsterseniz Chrome kiosk modu: 
       chrome --kiosk --app="file:///C:/MoscheeTV/index.html"

2) Raspberry Pi (kiosk):
   - Chromium kuruluysa şu komutla başlatın:
       chromium-browser --kiosk file:///home/pi/MoscheeTV/index.html
   - Otomatik başlatma için LXDE autostart içine aynı komutu ekleyin.

3) Özelleştirme:
   - Duyurular: config.json içindeki "announcements" ve "ticker" metinlerini değiştirin.
   - Şehir/ülke/koordinat: index.html içindeki CONFIG bölümünde Graz ayarlarını göreceksiniz. Şehriniz değişirse güncelleyin.
   - Tasarım renkleri CSS içindedir (sayfanın üst kısmında).

4) Veri Kaynakları:
   - Namaz vakitleri: Aladhan API (method=13 Diyanet). Şehir: Graz, Ülke: Austria.
   - Hava durumu: open-meteo.com (ücretsiz). Zaman dilimi: Europe/Vienna.

5) Sorun Giderme:
   - Ekranda veri gelmiyorsa internet yoktur veya siteler engellenmiştir.
   - Güncellemenin gelmesi için 15 dakikada bir otomatik yenile vardır; isterseniz sayfayı yenileyin (F5).
   - Yazı tipi çok küçük/büyükse CSS'teki font boyutlarını ayarlayın.

Hazırlayan: Sizin için ChatGPT özel paket.
