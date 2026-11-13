नन्हे सितारे — Corrected Android Build Package
==============================================

यह पैकेज टैबलेट से GitHub पर अपलोड करके GitHub Actions द्वारा Android debug APK बनाने के लिए है।

मुख्य फाइलें:
- index.html : Vite का सही root entry point और पूरा गेम UI/logic
- public/assets/yashvi-nanhe-sitare-splash.png : approved splash artwork
- package.json : Vite और Capacitor dependencies
- capacitor.config.json : Android app identity और webDir
- vite.config.js : web build configuration
- .github/workflows/android-apk.yml : GitHub Actions APK build workflow

GitHub पर अपलोड:
1. Repository में पहले अपलोड की गई ZIP को हटाएँ यदि वह मौजूद है।
2. इस ZIP को टैबलेट में extract करें।
3. GitHub repository के Code > Add file > Upload files में जाएँ।
4. Root files अपलोड करें; public/assets के अंदर splash PNG को उसी path पर रखें।
5. `.github/workflows/android-apk.yml` को सही path के साथ अपलोड करें।
6. सभी files commit करने के बाद Actions tab में workflow run देखें।

APK:
Actions run सफल होने पर Artifacts में Nanhe-Sitare-debug-APK डाउनलोड करें। यह परीक्षण के लिए debug APK है; Play Store release के लिए signed release/AAB और policy review अलग से जरूरी हैं।

महत्वपूर्ण:
- यह शुरुआती prototype है; अभी cloud database, user accounts या online progress sync नहीं है।
- GitHub Pages/hosting पर static web build deploy किया जा सकता है; APK workflow अलग है।
- बच्चों की सुरक्षा के लिए ads, chat, location और tracking शामिल नहीं हैं।
