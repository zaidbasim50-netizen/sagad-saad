# Contributing Guidelines

**منصة التعليم الإنجليزية** - من تطوير أ.د سجاد سعد مهدي

## المساهمة في المشروع

شكراً لاهتمامك بالمساهمة! يرجى اتباع الخطوات التالية:

### 1. Fork المستودع
```bash
git clone <your-fork-url>
cd sajad2
```

### 2. إنشاء فرع جديد
```bash
git checkout -b feature/your-feature-name
```

### 3. إجراء التغييرات
- اتبع معايير الكود الموجودة
- أضف تعليقات واضحة
- اختبر التغييرات

### 4. مراجعة الكود
- تأكد من عدم وجود أخطاء
- اختبر جميع الحالات

### 5. Commit والـ Push
```bash
git add .
git commit -m "Add feature: description"
git push origin feature/your-feature-name
```

### 6. إنشاء Pull Request
- اشرح التغييرات
- أضف اختبارات إن أمكن

## معايير الكود

### JavaScript/Node.js
- استخدم camelCase للمتغيرات
- استخدم const/let بدلاً من var
- أضف JSDoc للدوال المهمة

### React
- استخدم Functional Components
- استخدم Hooks
- اتبع React Conventions

### Dart/Flutter
- استخدم camelCase للمتغيرات
- استخدم const للـ widgets الثابتة
- اتبع Dart Effective Dart Guide

## الإبلاغ عن الأخطاء

1. تحقق من عدم تكرار المشكلة
2. اشرح الخطوات لتكرار المشكلة
3. أرفق لقطات شاشة إن أمكن
4. اذكر إصدار التطبيق

## الميزات الجديدة

- يجب ألا تؤثر على الأداء
- يجب أن تكون موثقة
- يجب أن تتبع معايير الأمان

