# 📋 CHANGELOG — QARZLARIM

Qarzlarim rivojlanish tarixi. Yangi funksiyalar, yaxshilanishlar va hisob yuritishdagi muhim o‘zgarishlar shu yerda qayd etiladi.

Versiyalash: `MAJOR.MINOR` — shaxsiy loyiha uchun ishlatiladigan versiya belgilari; rasmiy SemVer kafolati emas.

---

## [2.5] — 2026-10-22 · 🔥 PENALTY LEDGER

### ✨ Added
- **Kunlik penya foizi (`%/kun`)** — har qarz uchun alohida.
- **Penya boshlanish sanasi** — hisoblash davrini aniq belgilash.
- **Asosiy qarz / yozilgan penya / hisobiy penya** tafsilotlari.
- Qarz qo‘shish va tahrirlash oynasida **live preview**: jami qoldiq hamda taxminiy kunlik penya.
- **«Penyani qayd etish»** — hisoblangan penyani Firebase balansiga tranzaksiya orqali yozish.
- Qarz kartasida yozilmagan hisobiy penya va kunlar sonini ko‘rsatish.

### ⚙️ Changed
- Umumiy qoldiq endi **Firebase'ga yozilgan balans + hali qayd etilmagan hisobiy penya** asosida ko‘rsatiladi.
- Kunlar **`Asia/Tashkent` kalendar sanasi** bo‘yicha hisoblanadi; boshlanish kuni hisoblanmaydi.
- Hisoblash modeli: **asosiy qarzga nisbatan oddiy kunlik foiz**, penyaning o‘ziga foiz yuritilmaydi.
- To‘lov kiritilganda shu paytgacha hisoblangan penya avval qayd qilinadi, keyin to‘lov **penya → asosiy qarz** tartibida ajratiladi.
- Kun o‘zgarganida ilova ochiq tursa, hisobiy qoldiq qayta chiziladi; Firebase'ga o‘zboshimchalik bilan yozilmaydi.
- Eski qarz yozuvlari uchun hisobiy penya sozlamalari **majburiy emas**; foiz va sana kiritilmaguncha avtomatik hisob yurmaydi.

### 🛠️ Improved
- Operatsiyalar uchun **Firebase transaction**, oxirgi amalni **Undo** qilishda penya va asosiy balansni qayta tiklash.
- Tahrir paytida boshqa tab/qurilma ma’lumotni o‘zgartirgan bo‘lsa, eskirgan qiymat ustiga yozib yubormaslik tekshiruvi.
- Mobil interfeysda penya kartalari va inputlarning moslashuvi.

### ⚠️ Known limitations
- Penya **bank yoki sudning rasmiy hisobi emas**: oddiy kunlik foiz modeli ishlatiladi.
- **Avtomatik ko‘rsatish** ≠ **avtomatik Firebase'ga yozish**: faqat tasdiqlangan amal penyani bazaga qayd qiladi.
- To‘lov avval penyadan ayriladi; shartnoma bo‘yicha taqsimlash boshqa bo‘lsa, ma’lumotni rasmiy qoldiqqa moslash kerak.
- Yangi Firebase loyiha/Google login/Database Rules sozlamalari deployment'ning alohida bosqichi.

---

## [2.4] — 2026-10 · 🧪 PENALTY SPLIT (PROTOTYPE)

- Qarzning **asosiy summasi** va **penya summasi** alohida yuritiladigan prototip.
- **Kunlik penya foizi** inputi va bir kunlik penya taxmini.
- Qarz kartasida asosiy qarz, penya va jami qoldiqni farqlashga zamin yaratildi.
- **Eslatma:** ushbu bosqichda sana asosida to‘liq kunlik accrual hali joriy etilmagan edi; u v2.5’da qo‘shildi.

---

## [2.3] — 2026-10 · 🧭 NAVIGATION UPDATE

- **6 ta mustaqil bo‘lim:** Asosiy / Qarzlar / To‘lovlar / Tarix / Maqsad / Sozlama.
- Qarzlar uchun alohida ko‘rinish, kategoriya filtri va boshqaruv.
- To‘lov taqvimi, tarix/arxiv, maqsad va sozlamalar orasida aniq navigatsiya.
- GitHub Pages'da ishlash uchun mustaqil HTML sahifa tuzilmasi.

---

## [2.2] — 2026-10 · ☁️ CLOUD & SAFETY UPDATE

- Firebase Realtime Database'da **tranzaksiyali to‘lov va penya** operatsiyalari.
- **Operatsiyalar tarixi** va oxirgi mos amalni qaytarish imkoniyati.
- Qarzni yopish va tarixda kuzatish imkoniyatlari.
- **JSON backup / restore** — 6 ta asosiy Firebase yo‘li bilan.
- **Google Auth** integratsiyasi va Database Rules xavfsizligi haqida qo‘llanma.
- **90% qarz kamaytirish maqsadi**, shaxsiy qarzlarni belgilash va oylik to‘lovlar ko‘rinishi.

---

## [2.1 / 2.0] — 2026-10 · ⚡ FOUNDATION

- Dastlabki **dark neon** qarz boshqaruv interfeysi.
- Qarzlarni bo‘limlar bo‘yicha saqlash, tahrirlash va yig‘indi chiqarish.
- To‘lov sanasi va qarzlarni boshqarish bo‘yicha bosqichma-bosqich yaxshilanishlar.
- Firebase ma’lumotlar omboriga ulanish.

---

## 🔜 Rejalashtirilishi mumkin bo‘lgan ishlar

Quyidagilar **joriy funksiyalar emas**, keyingi versiyalar uchun g‘oyalar:

- Bank shartnomasiga qarab penya modeli yoki limitini sozlash.
- Alohida test ma’lumotlari (demo mode).
- To‘lovlarni import qilish va yaxshiroq solishtirish.
- Qarzlar kesimida batafsil tahlil va grafiklar.

---

[⬅️ README'ga qaytish](./README.md)
