# English Learning Platform 🎓

منصة تعليمية متكاملة لتعليم اللغة الإنجليزية مع ميزات أمان متقدمة وإدارة شاملة للطلاب.

## المميزات الرئيسية

### 1. **المصادقة و الأمان**
- ✅ نظام تسجيل دخول آمن مع JWT
- ✅ منع دخول الطالب من أكثر من جهاز واحد
- ✅ توثيق الجهاز (Device ID)
- ✅ حماية من محاولات تسجيل الدخول المتكررة

### 2. **محتوى التعليم**
- 📹 تحميل ومشاهدة الفيديوهات المحمية
- 📝 محاضرات وشروحات نصية
- 📊 تتبع مشاهدة الفيديو
- 🎯 تقييمات وتعليقات

### 3. **الامتحانات والدرجات**
- ✍️ امتحانات يومية
- 📋 أنواع متعددة من الأسئلة
- 📊 تقييم تلقائي للإجابات
- 📈 تقارير الأداء الشاملة

### 4. **نظام الدفع**
- 💳 دعم بطاقات الائتمان (Stripe)
- 📦 خطط اشتراك مختلفة
- 📨 فواتير آلية
- 📊 تقارير مالية

### 5. **الحماية من النسخ**
- 🚫 منع حفظ الفيديو والصور
- 🚫 منع التقاط الشاشة (Screenshot)
- 🔒 تشفير المحتوى
- 📱 قفل التطبيق على جهاز واحد

### 6. **لوحة التحكم** 
- 👨‍🏫 لوحة تحكم المعلم
- 👨‍🎓 لوحة تحكم الطالب
- 📊 تحليلات وإحصائيات
- 👥 إدارة الطلاب

## البنية التقنية

```
sajad2/
├── backend/                    # Node.js + Express API
│   ├── src/
│   │   ├── controllers/        # معالجات الطلبات
│   │   ├── routes/             # المسارات
│   │   ├── middleware/         # البرامج الوسيطة
│   │   ├── config/             # التكوينات
│   │   └── index.js            # نقطة الدخول
│   ├── package.json
│   └── .env.example
│
├── web-frontend/               # React + Next.js
│   ├── src/
│   │   ├── pages/              # الصفحات
│   │   ├── components/         # المكونات
│   │   ├── services/           # خدمات API
│   │   ├── contexts/           # React Context
│   │   └── App.js
│   ├── package.json
│   └── .env.example
│
├── mobile/                     # Flutter
│   ├── lib/
│   │   ├── screens/            # الشاشات
│   │   ├── services/           # الخدمات
│   │   ├── models/             # نماذج البيانات
│   │   └── main.dart           # نقطة الدخول
│   ├── pubspec.yaml
│   └── android/
│
├── database/
│   ├── schema.sql              # هيكل قاعدة البيانات
│   └── migrations/             # ترحيلات قاعدة البيانات
│
└── docs/
    ├── API_DOCUMENTATION.md
    ├── SETUP_GUIDE.md
    └── SECURITY.md
```

## المتطلبات

### Backend
- Node.js 16+
- PostgreSQL 12+
- npm/yarn

### Web Frontend
- Node.js 16+
- npm/yarn
- متصفح حديث

### Mobile
- Flutter 3.0+
- Android Studio / Xcode
- Dart 3.0+

## التثبيت والإعداد

### 1. قاعدة البيانات

```bash
# إنشاء قاعدة البيانات
createdb english_platform

# تطبيق المخطط
psql -U postgres -d english_platform -f database/schema.sql
```

### 2. Backend API

```bash
cd backend

# نسخ ملف البيئة
cp .env.example .env

# تثبيت الاعتماديات
npm install

# تشغيل السيرفر
npm run dev
```

السيرفر سيعمل على: `http://localhost:5000`

### 3. Web Frontend

```bash
cd web-frontend

# نسخ ملف البيئة
cp .env.example .env

# تثبيت الاعتماديات
npm install

# تشغيل التطبيق
npm start
```

التطبيق سيعمل على: `http://localhost:3000`

### 4. Mobile App (Flutter)

```bash
cd mobile

# الحصول على الاعتماديات
flutter pub get

# تشغيل على الجهاز المتصل
flutter run

# بناء APK (Android)
flutter build apk --release

# بناء IPA (iOS)
flutter build ios --release
```

## كيفية الاستخدام

### للمعلم:
1. تسجيل دخول باستخدام بيانات المعلم
2. إنشاء بيانات دخول للطلاب (اسم مستخدم + كلمة مرور)
3. تحميل الفيديوهات والمحاضرات
4. إنشاء امتحانات يومية
5. متابعة تقدم الطلاب والدرجات
6. إدارة الدفعات

### للطالب:
1. تسجيل دخول باستخدام البيانات المعطاة من المعلم
2. مشاهدة الفيديوهات والمحاضرات
3. حل الامتحانات اليومية
4. عرض الدرجات والتقارير
5. دفع الاشتراك (إذا لزم الأمر)

## الميزات الأمنية

### منع التعدد:
- كل طالب يمكنه الدخول من جهاز واحد فقط
- عند محاولة دخول من جهاز آخر، يتم قطع الجهاز الأول

### حماية المحتوى:
- منع حفظ الفيديو والصور
- منع التقاط الشاشة
- تشفير ملفات الوسائط
- معاينات محدودة

### المصادقة:
- JWT بـ expiry محدد
- Refresh tokens طويلة الأجل
- معرف الجهاز الفريد
- تتبع محاولات تسجيل الدخول الفاشلة

## متطلبات البيئة

انسخ `.env.example` إلى `.env` وعدّل القيم:

```env
# Database
DB_HOST=localhost
DB_PORT=5432
DB_NAME=english_platform
DB_USER=postgres
DB_PASSWORD=your_password

# Server
PORT=5000
NODE_ENV=development
JWT_SECRET=your_jwt_secret_key

# Payment (Stripe)
STRIPE_SECRET_KEY=sk_test_...
STRIPE_PUBLIC_KEY=pk_test_...

# File Upload
MAX_FILE_SIZE=500000000
VIDEO_UPLOAD_PATH=./uploads/videos
```

## الاستكشاف والتطوير

### إنشاء طالب جديد:

**POST** `/api/auth/register`

```json
{
  "email": "student@example.com",
  "username": "student123",
  "firstName": "أحمد",
  "lastName": "علي",
  "password": "secure_password"
}
```

### تسجيل الدخول:

**POST** `/api/auth/login`

```json
{
  "username": "student123",
  "password": "secure_password",
  "deviceName": "My Device",
  "deviceType": "mobile",
  "deviceId": "unique_device_id"
}
```

### تحميل فيديو:

**POST** `/api/videos/upload` (multipart/form-data)

```
title: English Grammar Basics
description: Learn English grammar fundamentals
category: Grammar
level: Beginner
video: [binary file]
```

## معالجة الأخطاء

جميع الطلبات تحتوي على معالجة خطأ موحدة:

```json
{
  "message": "Error description",
  "error": "Detailed error (في وضع التطوير فقط)"
}
```

## الدعم والمساعدة

للمزيد من التفاصيل، راجع:
- 📖 [توثيق API](./docs/API_DOCUMENTATION.md)
- 🔧 [دليل الإعداد](./docs/SETUP_GUIDE.md)
- 🔒 [دليل الأمان](./docs/SECURITY.md)

## الترخيص

MIT License

---

**تم إنشاؤه بواسطة:** أ.د سجاد سعد مهدي
**الفئة:** منصة التعليم الإنجليزية
**آخر تحديث:** 2026
