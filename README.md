# Ders Çevirmeni

Derste hocanın konuşmasını canlı olarak İngilizce (veya Almanca) yazıya döker ve aynı anda Türkçeye çevirir. Biyoloji, biyokimya ve biyoteknoloji terimleri için ayarlanmıştır.

- **Yazıya döküm:** iki seçenek var.
  - **Deepgram Nova-3** (varsayılan): Ders terimlerinden oluşan bir liste verilebiliyor (en fazla 100 terim). Deepgram bu terimleri duymayı bekliyor ve doğru yazıyor. Ayrı bir Deepgram API anahtarı gerekir (console.deepgram.com). Ücreti dakika başına.
  - **Tarayıcı** (ücretsiz): Chrome/Edge/Safari'nin kendi konuşma tanıması. Terim listesi verilemiyor, bilimsel terimlerde daha çok hata yapar.
- **Çeviri:** Claude (Anthropic API), kendi API anahtarınla. Anahtar sadece tarayıcının localStorage'ında durur.
- Önemli terimler vurgulanır ve ilk geçişte İngilizcesi parantez içinde verilir.
- Ayarlar'da dersin konusunu, ses tanımaya öğretilecek terimleri ve kişisel terim sözlüğünü (`terim = çeviri`) girebilirsin. **Konudan terim öner** düğmesi, Claude'a ders konusuna göre 60 terimlik bir liste hazırlatır. Sözlükteki terimler de Deepgram'a otomatik gönderilir.
- Konuşma tanımanın yanlış duyduğu terimleri ("my toe con dria" gibi) Claude bağlama bakarak düzeltir.
- Döküm tarayıcıda saklanır, sayfa yenilense de kaybolmaz. **Dışa aktar** ile Markdown dosyası olarak indirilebilir.

## Kullanım

1. Sayfayı **https** üzerinden aç (örneğin GitHub Pages). Mikrofon izni için https gerekir.
2. **Ayarlar** → Anthropic API anahtarı (console.anthropic.com), Deepgram API anahtarı, model ve ders konusu. Sonra **Konudan terim öner**'e basıp listeyi kontrol et ve kaydet.
3. **Dinlemeye başla**'ya bas ve mikrofon iznini ver.

Mikrofonsuz denemek için alttaki kutuya bir cümle yazıp Enter'a basabilirsin.

## Model seçimi

| Model | Ne zaman |
|---|---|
| Claude Opus 5.5 | Varsayılan. En doğru terminoloji |
| Claude Sonnet 5.5 | Dengeli |
| Claude Haiku 5.5 | En hızlı ve en ucuz; çeviri daha az gecikir |
