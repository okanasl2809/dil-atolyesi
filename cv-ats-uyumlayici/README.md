# CV'ni ilana göre ayarla

Geliştirici: **Okan Asl** · © 2026 Okan Asl · Tüm hakları saklıdır

CV'ni bir kez yükle, her başvuruda iş ilanını ekle. Uygulama CV'ni o şirketin işe alım uzmanı gözüyle değerlendirir, ATS (aday takip sistemi) filtrelerinden geçecek şekilde yeniden yazar, bağımsız bir son taramadan geçirir ve Word ya da PDF olarak indirmeni sağlar.

**Hemen kullan:** https://okanasl2809.github.io/dil-atolyesi/cv-ats-uyumlayici/

Tek bir HTML dosyasıdır. Sunucu, kayıt ya da kurulum yoktur. CV'n ve bilgilerin yalnızca kendi tarayıcında saklanır.

### Telefona ya da bilgisayara uygulama olarak yükle

Sayfa yüklenebilir bir uygulamadır (PWA). Yüklediğinde ana ekranda kendi simgesiyle, tarayıcı çubuğu olmadan açılır.

- **Android (Chrome):** Sayfanın üstündeki **Uygulamayı yükle** düğmesine dokun ya da Chrome menüsünden **Uygulamayı yükle**'yi seç.
- **iPhone / iPad (Safari):** Alttaki **Paylaş** düğmesine dokun ve **Ana Ekrana Ekle**'yi seç.
- **Bilgisayar (Chrome / Edge):** Adres çubuğunun sağındaki yükleme simgesine tıkla.

Uygulama internet olmadan da açılır ve kayıtlı verilerini gösterir; yapay zekâ özellikleri için internet bağlantısı gerekir.

## Neler yapar

**CV hazırla**
- 100 üzerinden uyum puanı ve kırılımı (zorunlu nitelikler, anahtar kelimeler, deneyim, format)
- Aday kriterleri kontrolü (deneyim yılı, eğitim, dil, askerlik, ehliyet)
- Eksik en önemli 5 anahtar kelime ve işe alım müdürünün 10 saniyede göreceği 3 kırmızı bayrak
- Deneyim maddelerinin Google'ın XYZ formülüyle yeniden yazılması
- ATS ve "günde 200 CV okuyan müdür" gözüyle bağımsız son tarama, kalan bayrakların otomatik düzeltilmesi
- **Eksikleri tamamla:** boşlukları rakam uydurmadan açıklayıcı cümlelere çevirir, ilandaki eksik terimleri ekler, ek talimatlarınla tekrar tekrar düzenleyip yeniden puanlar
- Doğruluk kontrolü: yeni CV'deki her rakam ve terim orijinal CV'nle karşılaştırılır
- Tek sütunlu, tablosuz, ATS dostu Word (.docx) ve metni seçilebilir PDF çıktısı
- Ön yazı, LinkedIn mesajı, LinkedIn profil önerisi, mülakat soruları

**Diğer bölümler**
- **İlanları karşılaştır:** 10 ilana kadar hızlı uyum puanı ve "Başvur / Düşün / Geç" önerisi
- **Kariyer envanteri:** CV'ne göre sorulan sorularla rakamlarını ve başarılarını bir kez kaydet, her başvuruda kullanılsın
- **Kariyer.net profili:** Özgeçmiş Havuzu aramalarında öne çıkacak başlık, özet, deneyim açıklamaları ve yetenek etiketleri
- **Mülakat provası:** ilana özel sorular, cevap başına 10 üzerinden puan, geri bildirim ve daha güçlü cevap örneği
- **Başvurularım:** durum takibi, dönüş oranı, 7 gün dönüş gelmeyenler için takip e-postası, görüşme sonrası teşekkür e-postası
- Yedekleme: tüm verini tek dosya olarak indir, başka cihaza taşı

## Uydurma yok

Uygulama sende olmayan deneyim, araç, rakam ya da sertifika eklemez. Unvan, şirket, tarih, okul, dil seviyesi ve sertifikalar sen değiştirmedikçe aynen kalır. Dayanağı belirsiz eklemeler onayına sunulur. Amaç, mülakatta savunabileceğin bir CV'dir.

## Nasıl çalıştırılır

**1. Claude içinde (API anahtarı gerekmez).** Sayfayı claude.ai'de bir artifact olarak açarsan uygulama Claude hesabını kullanır.

**2. Tarayıcıda, kendi API anahtarınla.** Yukarıdaki GitHub Pages linkini aç ve [Claude Console](https://platform.claude.com)'dan aldığın Anthropic API anahtarını gir.
- Anahtar yalnızca senin tarayıcında saklanır ve istekler doğrudan Anthropic API'ye gider; arada başka bir sunucu yoktur.
- Kullanım ücreti kendi API hesabından düşer. Bir CV hazırlığı, CV ve ilan uzunluğuna göre birkaç çağrı yapar.
- Ortak kullanılan bilgisayarlarda "Bu tarayıcıda hatırla" seçeneğini kapat ya da işin bitince "Anahtarı sil" de.

## Gizlilik

- CV'n, kariyer envanterin ve başvuru kayıtların yalnızca tarayıcının yerel depolamasında durur.
- Analiz için CV ve ilan metni Anthropic'e (Claude) gönderilir. Başka hiçbir yere gönderilmez.
- Uygulama TC kimlik no, kan grubu, medeni hal gibi gereksiz kişisel verileri CV'den çıkarmayı önerir.

## Bilinmesi gerekenler

- Puan, yapay zekânın ilana bakarak yaptığı bir tahmindir; gerçek bir ATS puanı değildir. Her şirketin sistemi farklı çalışır. Puanı "iyileşme oldu mu" diye kıyaslamak için kullan.
- Göndermeden önce CV'ni mutlaka oku. Özellikle "Kontrol etmen gereken eklemeler" kartına bak.
- Kendi testin: İndirdiğin Word dosyasını Kariyer.net ya da LinkedIn'de "özgeçmişten otomatik doldur" ile yükle. Bilgiler doğru alanlara düşüyorsa ATS'ler CV'ni doğru okuyor demektir.

## Teknik

- Uygulama tek dosyadır: `index.html`. Derleme adımı yok. `manifest.webmanifest`, `sw.js` ve `icons/` yüklenebilir uygulama (PWA) içindir.
- Kullanılan kütüphaneler (jsDelivr üzerinden): pdf.js (PDF okuma), mammoth (Word okuma), jsPDF (PDF üretme). Word dosyası uygulamanın içinde üretilir.
- Modeller: `claude-sonnet-5-5`, CV yeniden yazımı için `claude-opus-5-5`.

## English

A single-file web app that tailors your CV to a job posting for ATS screening: fit score, missing keywords, red flags, XYZ-formula rewriting, an independent ATS/recruiter audit, fact checking against your original CV, and ATS-friendly Word/PDF export. Also includes job triage, a career inventory, Kariyer.net profile texts, mock interviews and application tracking. The interface is in Turkish; CVs can be produced in Turkish or English. Runs inside Claude, or on GitHub Pages with your own Anthropic API key (stored only in your browser).

## Lisans

© 2026 Okan Asl ([@okanasl2809](https://github.com/okanasl2809)). **Tüm hakları saklıdır.**

Uygulamayı kendi iş başvuruların için ücretsiz kullanabilirsin; ürettiğin CV ve ön yazılar sana aittir. Kodu kopyalamak, değiştirip yayınlamak ya da ticari amaçla kullanmak için önceden yazılı izin gerekir. Ayrıntılar için [LICENSE](LICENSE) dosyasına bak.

All rights reserved. Free to use for your own job applications; copying, modification, redistribution and commercial use require prior written permission. See [LICENSE](LICENSE).
