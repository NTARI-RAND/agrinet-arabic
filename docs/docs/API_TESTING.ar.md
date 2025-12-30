# دليل اختبار واجهة برمجة التطبيقات (API)

## مقدمة
هذا الدليل يشرح كيفية اختبار نقاط نهاية واجهة برمجة التطبيقات (API) في نظام أغرينيت باستخدام أداة curl.

## المتطلبات
- curl مثبت على نظامك
- - نقطة نهاية API تعمل (عادة على http://localhost:8000)
  - - البيانات المطلوبة للاختبار
   
    - ## أمثلة الاختبار
   
    - ### اختبار طلب GET بسيط
    - ```bash
      curl http://localhost:8000/api/endpoint
      ```

      ### اختبار طلب POST مع البيانات
      ```bash
      curl -X POST http://localhost:8000/api/endpoint \
        -H "Content-Type: application/json" \
        -d '{"key": "value"}'
      ```

      ### اختبار مع المصادقة
      ```bash
      curl -H "Authorization: Bearer YOUR_TOKEN" \
        http://localhost:8000/api/protected
      ```

      ## الاختبار المتقدم
      - استخدام رؤوس مخصصة
      - - إرسال الملفات
        - - التعامل مع استجابات الخطأ
         
          - ## الخلاصة
          - يمكن استخدام curl لاختبار جميع نقاط نهاية API بكفاءة وسهولة.
          - 
