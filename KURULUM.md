# Dil Atölyesi: telefona kurulum

1. Bu klasördeki 8 dosyanın hepsini GitHub'da yeni bir depoya yükle (depo adı: dil-atolyesi, Public).
2. Depoda Settings › Pages › Branch: main, / (root) › Save.
3. 1–2 dakika sonra adres: https://KULLANICIADIN.github.io/dil-atolyesi/
4. Adresi telefonda aç:
   - Android: Chrome › sağ üstteki üç nokta › "Uygulamayı yükle" ya da "Ana ekrana ekle".
   - iPhone: Safari › Paylaş › "Ana Ekrana Ekle".
5. Eski ilerlemeyi taşımak için: Claude linkinde Defter › Yedekle › "Yedek kodunu kopyala";
   yeni uygulamada aynı ekranda kodu yapıştır › "Yapıştırılan kodu yükle".

Güncelleme: Yeni bir index.html geldiğinde depodaki eski dosyanın üzerine yükle.
Uygulama açılınca altta "Yeni sürüm hazır, yenile" düğmesi çıkar.

## Güncelleme butonu
Uygulamada "🔄 Uygulamayı güncelle" butonu var (YDS Akademi: ana ekranın altı; Dil Atölyesi: Defter › Uygulama).
Basınca en yeni sürüm indirilir ve uygulama yenilenir. İlerleme silinmez.
Yeni sürüm yayınlandığında uygulama bunu kendisi fark eder ve altta "Yeni güncelleme var" uyarısı çıkar.

Yeni sürüm yayınlarken: index.html içindeki APP_VER ile version.json içindeki "v" değerini
aynı yeni değere getir (örn. 2026.10.20-1). Uyarı bu iki değer farklı olunca çıkar.
