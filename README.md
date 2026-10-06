# recall-topics

RECALL ilovasi uchun "Tayyor mavzular" ro'yxati. Bu repo faqat kontent
saqlaydi — ilovaning kodi bilan aralashmaydi.

## O'rnatish (bir martalik)

1. GitHub'da yangi repo yarating — nomi muhim emas, lekin **PUBLIC** bo'lishi shart
   (aks holda ilova fayllarni o'qiy olmaydi).
2. Shu papkadagi hamma narsani (`catalog.json`, `topics/`) o'sha repo'ga push qiling.
3. RECALL loyihasidagi `config.js` faylini oching va `CATALOG_BASE_URL`ni
   repo manzilingizga moslang:

   ```
   const CATALOG_BASE_URL = 'https://raw.githubusercontent.com/<USERNAME>/<REPO>/main/';
   ```

   `<USERNAME>` va `<REPO>` o'rniga o'zingiznikini yozing (branch nomi `main`
   bo'lmasa, uni ham moslang). Oxirida `/` bo'lishi shart.
4. `npm run dist` bilan ilovani qayta quring (yoki `npm start` bilan sinab ko'ring) —
   sidebar'dagi "Tayyor mavzular" endi shu repo'dan o'qiydi.

## Yangi mavzu qo'shish

1. `topics/` ichiga yangi `.csv` fayl qo'shing. Ustunlar tartibi:
   **Xorijiy so'z, Tarjima, Misol** (misol ixtiyoriy). Birinchi qator sarlavha
   hisoblanib, ilova tomonidan o'tkazib yuboriladi.
2. `catalog.json`ga bitta qator qo'shing:

   ```json
   { "id": "noyob-id", "name": "Ko'rinadigan nomi", "file": "topics/fayl-nomi.csv", "count": 10 }
   ```

   `id` — har doim bir xil va takrorlanmas bo'lishi kerak (buni o'zgartirmang,
   aks holda foydalanuvchilar uchun "Yangilash" ishlamay qoladi). `count` —
   ixtiyoriy, ro'yxatda so'zlar sonini ko'rsatish uchun.
3. GitHub'ga push qiling — tayyor. Ilovani yangilash shart emas, u har safar
   ro'yxatni jonli o'qiydi.

## Namuna

Bu papkada ikkita tayyor misol bor: `hayvonlar.csv` va `kasblar.csv` — formatni
ko'rish uchun shularga qarang.
