<div align="center">

# ⚡ QARZLARIM

### `NEON LEDGER • v2.5`

**Qarzlarni nazorat qilish. Penyani tushunish. Moliyaviy erkinlik sari har bir qadamni kuzatish.**

[![Version](https://img.shields.io/badge/version-2.5-00e5ff?style=for-the-badge&labelColor=070b18)](./CHANGELOG.md)
![HTML5](https://img.shields.io/badge/HTML5-single--file-ff6a3d?style=for-the-badge&labelColor=070b18)
![Firebase](https://img.shields.io/badge/Firebase-Realtime_DB-ffb300?style=for-the-badge&labelColor=070b18)
![Responsive](https://img.shields.io/badge/UI-mobile_%2B_desktop-b35aff?style=for-the-badge&labelColor=070b18)

[🌐 **Saytni ochish**](https://hirokasimov.github.io/Qarz-ar-trackeri/) · [📋 **Changelog**](./CHANGELOG.md) · [🐛 **Issues**](https://github.com/HiroKasimov/Qarz-ar-trackeri/issues)

</div>

---

## 💠 Loyiha haqida

**Qarzlarim** — bank, bo‘lib to‘lash, skuter va shaxsiy qarzlarni bir joyda boshqarish uchun yaratilgan **shaxsiy moliyaviy tracker**. Ilova bitta `index.html` faylda ishlaydi; ma’lumotlar **Firebase Realtime Database** bilan sinxronlanadi.

Dizayn: **dark cyberpunk**, neon cyan / purple / pink, yumshoq glow effektlari va telefon hamda kompyuterga mos interfeys.

> [!IMPORTANT]
> Bu **shaxsiy hisob-kitob vositasi**. U bank, kredit tashkiloti yoki sudning rasmiy qarzdorlik hisoboti emas. Ayniqsa penya va to‘lovni taqsimlash tartibini kreditorning haqiqiy ko‘rsatkichlari bilan solishtiring.

## ✨ Imkoniyatlar

| Modul | Nima qila oladi? |
| :--- | :--- |
| 🏠 **Asosiy** | Umumiy qoldiq, faol qarzlar soni, eng yaqin to‘lov va tezkor harakatlar |
| ▤ **Qarzlar** | Bo‘limlar bo‘yicha qarz qo‘shish, tahrirlash, to‘lash va yopish |
| ◷ **To‘lovlar** | Navbatdagi to‘lov sanasi va summasi, oylik to‘lovlar ko‘rinishi |
| ↶ **Tarix** | To‘lov/penya operatsiyalari, so‘nggi mos amalni bekor qilish, yopilgan qarzlar |
| ◎ **Maqsad** | Boshlang‘ich qarzga nisbatan **90% kamaytirish** progressi |
| ⚙ **Sozlamalar** | JSON backup/restore, Google login va Firebase xavfsizligi bo‘yicha yordam |

**Qo‘shimcha imkoniyatlar:**
- O‘zing yaratadigan, nomini va rangini o‘zgartiradigan qarz bo‘limlari.
- Bank/servis qarzi va shaxsiy/oilaviy qarzlarni alohida belgilash.
- Ma’lumotlarni sahifa yangilanganda qayta yuklash va Firebase orqali sinxronlash.
- Balans va operatsiyalarni Firebase **transaction** yordamida yangilash.
- Neon interfeys, responsive tuzilma va mustaqil GitHub Pages sahifasi.

## 🔥 v2.5: kunlik penya tizimi

Har bir qarz uchun endi quyidagilarni alohida saqlash mumkin:

- **Asosiy qarz** — penya qo‘shilmagan qoldiq.
- **Kunlik penya foizi** — masalan, `0.5` → kuniga `0,5%`.
- **Joriy penya** — hozirgacha hisobga yozilgan penya.
- **Penya boshlanish sanasi** — penya qaysi kundan boshlab yurishi.
- **Hisobiy yangi penya** — bugungi Toshkent sanasigacha hisoblangan, lekin hali bazaga yozilmagan qism.
- **Jami qoldiq** — asosiy qarz + yozilgan penya + hisobiy yangi penya.

### 🧮 Hisoblash formulasi

```text
Kunlik penya = asosiy qarz × (kunlik foiz / 100)
Yangi penya  = kunlik penya × o'tgan kunlar
Jami qoldiq = asosiy qarz + yozilgan penya + yangi penya
```

Misol (`5` kun o‘tgan, stavka o‘zgarmagan):

```text
Asosiy qarz:           1 000 000 so‘m
Kunlik foiz:                   0,5%
1 kunlik penya:           5 000 so‘m
5 kunlik penya:          25 000 so‘m
-----------------------------------
Hisobiy jami:        1 025 000 so‘m
```

**Muhim qoidalar:**
1. Hisob **oddiy foiz** asosida; penyaning o‘ziga qayta foiz qo‘shilmaydi.
2. Boshlanish kunining o‘zi hisoblanmaydi; undan keyingi kunlar hisoblanadi.
3. Hisoblash **`Asia/Tashkent`** kalendar sanasi bilan ishlaydi.
4. Sahifada jami qoldiq avtomatik yangilanadi, **ammo saytni ochishning o‘zi Firebase'ga penya yozmaydi**.
5. **«Penyani qayd etish»** yoki **to‘lov kiritish** amali hisobiy penyani Firebase balansiga o‘tkazadi. Oxirgi hisoblangan sana qayd etilib, bir davr ikkinchi marta hisoblanishining oldi olinadi.
6. Ilova to‘lovni **avval penyadan, keyin asosiy qarzdan** kamaytiradi. Kreditorning haqiqiy tartibi boshqacha bo‘lsa, balansni rasmiy ma’lumotlarga moslang.
7. Foiz yoki boshlanish sanasi kiritilmagan qarzda avtomatik penya ishlamaydi.

> [!WARNING]
> Ayrim banklarda penya **foiz, qat’iy summa, cheklov, murakkab formula yoki shartnoma bo‘yicha boshqa asos** bilan hisoblanishi mumkin. Ilovadagi hisob **taxminiy**, majburiyatning rasmiy miqdori emas.

## 🚀 Ishga tushirish

### GitHub Pages orqali

1. Loyihani fork qiling yoki o‘z repository'ingizga `index.html` faylini yuklang.
2. **Settings → Pages → Build and deployment** ga kiring.
3. **Source:** `Deploy from a branch`, **Branch:** `main`, **Folder:** `/(root)` ni tanlang.
4. `Save` tugmasini bosing; deploy muvaffaqiyatli tugagach sahifani oching.

**Repository:** https://github.com/HiroKasimov/Qarz-ar-trackeri  
**Pages manzili:** https://hirokasimov.github.io/Qarz-ar-trackeri/

> Pages’da `index.html` ning aynan **v2.5** nusxasi joylanganini alohida tekshiring; README yangilanishi sayt kodini avtomatik almashtirmaydi.

### Firebase'ga ulash

Bu loyiha **Firebase JavaScript SDK 10.12.0**, **Realtime Database** va **Firebase Authentication (Google)** bilan ishlaydi.

1. O‘zingizning Firebase loyihangizni yarating va **Realtime Database** ni sozlang.
2. `index.html` ichidagi `firebaseConfig` obyektini **o‘z loyihangiz** ma’lumotlariga moslang.
3. **Authentication → Sign-in method** da Google provayderini yoqing.
4. **Authentication → Settings → Authorized domains** da foydalanayotgan domenni tekshiring.
5. **Realtime Database Rules** ni faqat ruxsat berilgan akkaunt o‘qiydigan/yozadigan qilib sozlang va sinovdan o‘tkazing.

Ma’lumotlar asosan quyidagi yo‘llarda saqlanadi:

```text
qarzlar/
qarzSections/
qarzArchive/
qarzEvents/
oylikTarix/
qarzSettings/
```

**Eslatma:** repository'dagi `firebaseConfig` loyiha identifikatorlarini o‘z ichiga oladi. Bu o‘z-o‘zidan maxfiy server kaliti emas; **ma’lumotlarni haqiqatan himoyalaydigan qatlam — Realtime Database Rules**.

## 🛡️ Xavfsizlik va backup

- **Shaxsiy qarz summalari, chek, PIN, karta raqami, JSON backup yoki foydalanuvchi ma’lumotlarini public repository'ga joylamang.**
- Faqat Google orqali kirish tugmasi ma’lumotlarni himoyalamaydi; Database Rules mustaqil tekshirilishi shart.
- Bitta Firebase bazasi boshqa ilovalarda ham ishlatilsa, umumiy Rules'ni almashtirishdan avval ta’sirini baholang.
- **Sozlamalar → Backup olish** orqali JSON zaxira oling, ayniqsa versiya yangilashdan oldin.
- **Restore** mavjud oltita ma’lumot yo‘lini zaxiradagi holatga almashtiradi va yangi operatsiyalarni yo‘qotishi mumkin. Oldin yangi backup oling.
- Test to‘lovlari uchun haqiqiy qarz ma’lumotlari o‘rniga **alohida sinov Firebase loyihasi** ishlatish tavsiya etiladi.

## 🧩 Texnologiyalar

`HTML5` · `CSS3` · `JavaScript (ES Modules)` · `Firebase Realtime Database` · `Firebase Authentication` · `GitHub Pages`

**Backend server talab qilinmaydi:** brauzer Firebase xizmatlariga ulanadi. Google Fonts va Firebase SDK uchun internet ulanishi kerak.

## 🗺️ Versiyalar

| Versiya | Asosiy yangilik |
| --- | --- |
| **v2.5** | Kunlik penya sanasi/foizi, hisobiy penya, qayd etish, to‘lov va Undo mosligi |
| **v2.4** | Asosiy qarz va penyani alohida ko‘rsatish prototipi |
| **v2.3** | 6 ta sahifali navigatsiya: Asosiy, Qarzlar, To‘lovlar, Tarix, Maqsad, Sozlama |
| **v2.2** | Tranzaksiyali operatsiyalar, maqsad, backup/restore, xavfsizlik sozlamalari |
| **v2.1 / v2.0** | Dastlabki qarz tracker'i va bosqichma-bosqich yaxshilanishlar |

Batafsil o‘zgarishlar: **[CHANGELOG.md](./CHANGELOG.md)**.

## 👨‍💻 Muallif

**[@HiroKasimov](https://github.com/HiroKasimov)** — shaxsiy moliyaviy boshqaruv uchun yaratilgan loyiha.

<div align="center">

---

**`TRACK • PLAN • PAY OFF • REPEAT`**

*Har bir yopilgan qarz — moliyaviy erkinlikka yana bir qadam.* 💙

</div>
