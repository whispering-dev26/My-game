Mening HTML, CSS va JavaScriptda yozilgan ushbu 5x5 boshqotirma (match-3) o'yinimga quyidagi ikkita funksiyani to'liq qo'shib ber:

1. Google AdMob (Interstitial / To'liq ekranli reklama) integratsiyasi:
- Loyiha tuzilishini tekshir (Capacitor, Cordova yoki oddiy Android WebView ekanligini aniqlab, shunga mos kod yoz):
  * AdMob App ID: ca-app-pub-1275271216332471~8126283781
  * Interstitial Ad Unit ID: ca-app-pub-1275271216332471/2280941065
- JavaScript ichida `showAdMobInterstitial()` funksiyasini yarat:
  * Agar Capacitor (`@capacitor-community/admob`) yoki Cordova (`admob-plus-cordova`) ulangan bo'lsa, reklama shu plagin orqali ko'rsatilsin va oldindan yuklab (prepare/preload) qo'yilsin.
  * Agar oddiy WebView bo'lsa, `window.Android.showInterstitial()` ko'prigini (bridge) chaqirsin, brauzerda test qilinganda esa xato bermasdan konsolga xabar chiqarib o'tib ketsin.
- Ushbu `showAdMobInterstitial()` funksiyasi o'yinchining har bir "Yangi" tugmasini bosganida va har 3 marta "Aralashtir" tugmasini ishlatganida ishga tushsin.

2. O'zbek (UZ) va Rus (RU) tillari tizimi:
- Yuqori panelga (yulduzcha va tangalar yoniga) chiroyli, o'yin dizayniga mos `UZ / RU` til almashtirish tugmasini qo'sh va tanlangan tilni `localStorage` da saqla.
- Barcha HTML elementlar va JS bildirishnomalarini ikki tilga o'tkaz:
  * "Sehr ishlatildi!" <-> "Магия использована!"
  * "Aralashtir" <-> "Перемешать"
  * "Sehr" <-> "Магия"
  * "Yangi" <-> "Новая игра"
  * "Tangalar yetarli emas!" <-> "Недостаточно монет!"
  * "Yurishlar qolmadi!" <-> "Нет ходов!"

Iltimos, barcha o'zgarishlarni mavjud dizayn va o'yin mexanikasini buzmasdan, to'liq ishlaydigan holatda yozib ber.
