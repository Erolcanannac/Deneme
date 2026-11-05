# Ders Çevirmeni

Derste hocanın konuşmasını canlı olarak İngilizce (veya Almanca) yazıya döker ve aynı anda Türkçeye çevirir. Biyoloji, biyokimya ve biyoteknoloji terimleri için ayarlanmıştır.

- **Yazıya döküm:** tarayıcının konuşma tanıma özelliği (Web Speech API). Chrome, Edge veya Safari gerekir; Firefox desteklemez. Chrome sesi tanıma için Google sunucularına gönderir.
- **Çeviri:** Claude (Anthropic API), kendi API anahtarınla. Anahtar sadece tarayıcının localStorage'ında durur.
- Önemli terimler vurgulanır ve ilk geçişte İngilizcesi parantez içinde verilir.
- Ayarlar'da dersin konusunu ve kişisel terim sözlüğünü (`terim = çeviri`) girebilirsin.
- Konuşma tanımanın yanlış duyduğu terimleri ("my toe con dria" gibi) Claude bağlama bakarak düzeltir.
- Döküm tarayıcıda saklanır, sayfa yenilense de kaybolmaz. **Dışa aktar** ile Markdown dosyası olarak indirilebilir.

## Kullanım

1. Sayfayı **https** üzerinden aç (örneğin GitHub Pages). Mikrofon izni için https gerekir.
2. **Ayarlar** → API anahtarı (console.anthropic.com), model ve ders konusu.
3. **Dinlemeye başla**'ya bas ve mikrofon iznini ver.

Mikrofonsuz denemek için alttaki kutuya bir cümle yazıp Enter'a basabilirsin.

## Model seçimi

| Model | Ne zaman |
|---|---|
| Claude Opus 5.5 | Varsayılan. En doğru terminoloji |
| Claude Sonnet 5.5 | Dengeli |
| Claude Haiku 5.5 | En hızlı ve en ucuz; çeviri daha az gecikir |
