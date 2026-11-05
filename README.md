# Ders Çevirmeni

Derste hocanın konuşmasını canlı olarak İngilizce (veya Almanca) yazıya döker ve Türkçeye çevirir. Ders bittikten sonra döküm, Claude ile biyoloji, biyokimya ve biyoteknoloji terminolojisine uygun şekilde düzeltilir.

Uygulama: https://erolcanannac.github.io/Deneme/

## Ücretsiz kullanım (varsayılan)

1. **Derste:** Ders Çevirmeni'ni aç ve **Dinlemeye başla**'ya bas.
   - **Varsayılan: Groq** (ücretsiz hesap, kredi kartı istemez). Ses tanımayı Groq'un sunucularındaki büyük **Whisper large-v3** modeli yapar; ders konusu, terim listesi ve önceki cümleler modele ipucu olarak verilir. Canlı Türkçe çeviriyi Groq'taki açık kaynaklı bir model (varsayılan Llama 3.3 70B) yapar. Anahtar: console.groq.com → API Keys. Günlük ücretsiz kota dolarsa çeviri daha küçük Llama 3.1 8B modeline geçer. Ses ve metin Groq'a gönderilir.
   - **Hesapsız seçenekler:** Whisper cihazda (iPad'de zayıf kalır) ya da tarayıcının kendi konuşma tanıması. Canlı çeviri hesapsız sadece masaüstü Chrome'da (yerleşik çevirici) var; diğer cihazlarda metin tek sütunda akar.
2. **Dersten sonra:** **Dışa aktar** ile dökümü indir. Sonra [Claude ile düzelt](https://claude.ai/artifact/DmsbvJBDFTF34xARpxWwRn) sayfasında dosyayı yükle. Bu sayfa claude.ai içinde açılır ve kendi Claude hesabını kullanır, API anahtarı gerekmez. Claude şunları yapar:
   - yanlış duyulan terimleri düzeltir ("like collie sis" → glycolysis),
   - metni Türkçe ders kitabı terminolojisiyle çevirir,
   - dersin terim listesini İngilizce, Türkçe ve Almanca (artikeliyle) olarak, kısa açıklamalarla çıkarır.

   Terim listesini **Sözlük olarak kopyala** ile Ders Çevirmeni'nin kişisel sözlüğüne aktarabilirsin.

## Ücretli seçenekler (isteğe bağlı)

Ayarlar'dan açılır, kendi API anahtarlarını ister. Anahtarlar sadece tarayıcının localStorage'ında durur.

- **Deepgram Nova-3 ses tanıma:** Ders terimlerinden bir liste verilebilir (en fazla 100). Bilimsel terimlerde Chrome'dan daha isabetli. Anahtar: console.deepgram.com
- **Claude canlı çeviri:** Derste de terimleri doğru çevirir. Anahtar: console.anthropic.com

Kaba maliyet tahmini, saatlik ders başına: Deepgram yaklaşık 0,45 $, Claude Haiku 5.5 yaklaşık 0,10 $, Sonnet 5.5 yaklaşık 2 $, Opus 5.5 yaklaşık 4 $.

## Diğer

- Döküm tarayıcıda saklanır, sayfa yenilense de kaybolmaz.
- Mikrofonsuz denemek için alttaki kutuya bir cümle yazıp Enter'a basabilirsin.
- Sayfanın https üzerinden açılması gerekir (mikrofon izni için).
