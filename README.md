# 💊 دواك — Dawak
## منصة الدواء الذكي لليمن 🇾🇪

---

### نبذة
**دواك** هي منصة ويب تربط المرضى بالصيدليات في اليمن. تتيح البحث عن الدواء ومعرفة أي صيدلية قريبة تمتلكه وبأي سعر، مع نظام وصفات طبية رقمية.

### التقنيات
- **Backend:** Laravel 11 + PHP 8.3
- **Database:** MySQL 8
- **Auth:** Laravel Sanctum
- **Search:** Laravel Scout
- **Frontend:** Blade + Tailwind CSS

### التثبيت السريع

```bash
# 1. استنساخ المشروع
git clone <repo-url> dawak
cd dawak

# 2. تثبيت الحزم
composer install

# 3. إعداد البيئة
cp .env.example .env
php artisan key:generate

# 4. إنشاء قاعدة البيانات
# أنشئ قاعدة بيانات باسم dawak_db في MySQL

# 5. تشغيل الترحيلات والبذور
php artisan migrate --seed

# 6. تشغيل الخادم
php artisan serve
```

### بيانات الدخول التجريبية

| الدور | البريد | كلمة المرور |
|-------|--------|-------------|
| مدير | admin@dawak.ye | password |
| طبيب | doctor@dawak.ye | password |
| مريض | patient@dawak.ye | password |
| صيدلاني | pharmacist1@dawak.ye | password |

### API Endpoints

Base URL: `/api/v1`

| Method | Endpoint | الوصف |
|--------|----------|-------|
| POST | /auth/register | تسجيل مستخدم جديد |
| POST | /auth/login | تسجيل الدخول |
| GET | /medicines | البحث عن الأدوية |
| GET | /medicines/{id} | تفاصيل دواء |
| GET | /pharmacies | قائمة الصيدليات |
| GET | /pharmacies/nearby | صيدليات قريبة |
| POST | /prescriptions | إنشاء وصفة (طبيب) |
| POST | /reservations | إنشاء حجز (مريض) |

### ⚠️ تنبيه أخلاقي
> هذه المنصة للإرشاد فقط لمعرفة مكان الدواء وسعره. استشر طبيبك أو صيدلانيك قبل تناول أي دواء.

---
*Dawak v1.0 — Built for Yemen 🇾🇪*
