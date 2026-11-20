# دليل النشر — VYPRON v2

1. خذ Backup كامل لقاعدة Supabase الحالية.
2. أنشئ مشروع Supabase تجريبياً، وشغّل `supabase/migrations/001_vypron_multitenant.sql` عليه أولاً.
3. راجع نتائج SQL وتأكد من أن السجلات القديمة رُبطت بمساحات شركات مناسبة.
4. في `config.js` استبدل `YOUR_PROJECT` برابط مشروعك، و`YOUR_PUBLIC_ANON_OR_PUBLISHABLE_KEY` بالمفتاح العام فقط.
5. أنشئ حساباً من الواجهة. بعد تأكيد البريد، نفّذ في SQL Editor أمر Super Admin الموجود في آخر ملف migration بعد تغيير البريد.
6. اختبر بحسابين وشركتين أن كل مستخدم لا يرى بيانات الشركة الأخرى.
7. ارفع محتويات المجلد إلى GitHub واربطه بـ Cloudflare Pages. Framework: None، build command فارغ، output directory جذر المشروع.
8. لا تنشر على قاعدة الإنتاج قبل نجاح اختبارات RLS والنسخ الاحتياطي.

مفاتيح service_role وأسرار مزودي الرياضة وAPI لا توضع في config.js أبداً. يلزم تطوير Edge Functions / API backend للدعوات، MFA الإلزامي، مفاتيح API، Webhooks ومزامنة البيانات قبل الإطلاق التجاري. لا تفعّل عمليات أموال حقيقية قبل التراخيص.
