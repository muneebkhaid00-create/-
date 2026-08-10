<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>طلب سكن في بكين</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Cairo', 'Tahoma', sans-serif;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" opacity="0.05"><path d="M10 50 Q 25 25 50 50 T 90 50" stroke="%231e3c72" stroke-width="2" fill="none"/><path d="M10 70 Q 30 45 60 70 T 90 70" stroke="%231e3c72" stroke-width="2" fill="none"/><circle cx="20" cy="20" r="4" fill="%231e3c72"/><circle cx="80" cy="80" r="4" fill="%231e3c72"/></svg>');
            background-color: #f0f4f9;
        }

        .container {
            max-width: 720px;
            width: 100%;
            background: rgba(255, 255, 255, 0.88);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            padding: 45px 40px;
            border-radius: 40px;
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.12);
            border: 1px solid rgba(255, 255, 255, 0.5);
            transition: 0.4s ease;
        }

        .container:hover {
            box-shadow: 0 40px 80px rgba(0, 0, 0, 0.15);
        }

        .header {
            text-align: center;
            margin-bottom: 30px;
        }

        .header .icon {
            font-size: 48px;
            background: #1e3c72;
            color: white;
            width: 80px;
            height: 80px;
            line-height: 80px;
            border-radius: 30px;
            display: inline-block;
            margin-bottom: 10px;
            box-shadow: 0 12px 25px rgba(30, 60, 114, 0.25);
        }

        .header h1 {
            font-size: 30px;
            font-weight: 700;
            color: #0b2447;
        }

        .header .sub {
            color: #4a5b6e;
            font-size: 17px;
            margin-top: 4px;
        }

        .form-group {
            margin-bottom: 22px;
        }

        .form-group label {
            display: block;
            font-weight: 600;
            color: #0b2447;
            margin-bottom: 6px;
            font-size: 15px;
        }

        .form-group label .star {
            color: #d9534f;
            margin-right: 2px;
        }

        .form-group select,
        .form-group input {
            width: 100%;
            padding: 14px 18px;
            border: 2px solid #e2e8f0;
            border-radius: 18px;
            font-size: 16px;
            font-family: 'Cairo', sans-serif;
            background: #ffffff;
            color: #1a2a3a;
            transition: 0.25s ease;
            outline: none;
        }

        .form-group select:focus,
        .form-group input:focus {
            border-color: #1e3c72;
            box-shadow: 0 0 0 4px rgba(30, 60, 114, 0.12);
        }

        .form-group select {
            appearance: none;
            background-image: url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='20' height='20' viewBox='0 0 24 24' fill='none' stroke='%231e3c72' stroke-width='2'><polyline points='6 9 12 15 18 9'/></svg>");
            background-repeat: no-repeat;
            background-position: left 15px center;
            background-size: 18px;
        }

        .radio-group {
            display: flex;
            flex-direction: column;
            gap: 12px;
            background: #f8faff;
            padding: 18px 20px;
            border-radius: 20px;
            border: 2px solid #e2e8f0;
            transition: 0.3s;
        }

        .radio-group:focus-within {
            border-color: #1e3c72;
            box-shadow: 0 0 0 4px rgba(30, 60, 114, 0.08);
        }

        .radio-option {
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 16px;
            font-weight: 500;
            color: #1a2a3a;
            cursor: pointer;
            padding: 6px 0;
        }

        .radio-option input[type="radio"] {
            width: 20px;
            height: 20px;
            accent-color: #1e3c72;
            cursor: pointer;
            flex-shrink: 0;
        }

        .radio-option input[type="radio"]:checked {
            transform: scale(1.1);
        }

        .budget-row {
            display: flex;
            gap: 15px;
            align-items: center;
            flex-wrap: wrap;
        }

        .budget-row .budget-item {
            flex: 1;
            min-width: 140px;
            display: flex;
            align-items: center;
            gap: 8px;
            background: #ffffff;
            border: 2px solid #e2e8f0;
            border-radius: 18px;
            padding: 0 18px;
            transition: 0.25s ease;
        }

        .budget-row .budget-item:focus-within {
            border-color: #1e3c72;
            box-shadow: 0 0 0 4px rgba(30, 60, 114, 0.12);
        }

        .budget-row .budget-item .currency-symbol {
            font-size: 18px;
            font-weight: 700;
            color: #1e3c72;
            flex-shrink: 0;
            padding-left: 4px;
        }

        .budget-row .budget-item input {
            width: 100%;
            padding: 14px 0;
            border: none;
            border-radius: 0;
            font-size: 16px;
            font-family: 'Cairo', sans-serif;
            background: transparent;
            color: #1a2a3a;
            outline: none;
            box-shadow: none;
        }

        .budget-row .budget-item input:focus {
            box-shadow: none;
        }

        .budget-row .budget-item input::placeholder {
            color: #aab3c0;
            font-weight: 300;
        }

        .budget-row .budget-separator {
            font-size: 18px;
            font-weight: 700;
            color: #1e3c72;
            padding: 0 4px;
            user-select: none;
            flex-shrink: 0;
        }

        .budget-hint {
            font-size: 13px;
            color: #8a9aa8;
            margin-top: 6px;
            display: block;
        }

        .contact-row {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .contact-row .form-group {
            flex: 1;
            min-width: 200px;
        }

        .divider {
            display: flex;
            align-items: center;
            text-align: center;
            margin: 8px 0 16px;
            color: #8a9aa8;
            font-size: 14px;
        }

        .divider::before,
        .divider::after {
            content: '';
            flex: 1;
            border-bottom: 2px dashed #dce2ea;
        }

        .divider::before {
            margin-left: 15px;
        }
        .divider::after {
            margin-right: 15px;
        }

        .btn-submit {
            width: 100%;
            padding: 16px;
            margin-top: 10px;
            background: linear-gradient(145deg, #1e3c72, #142d52);
            color: white;
            border: none;
            border-radius: 60px;
            font-size: 20px;
            font-weight: 700;
            font-family: 'Cairo', sans-serif;
            cursor: pointer;
            transition: 0.3s ease;
            box-shadow: 0 12px 28px rgba(30, 60, 114, 0.35);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
        }

        .btn-submit:hover {
            transform: translateY(-4px);
            box-shadow: 0 18px 40px rgba(30, 60, 114, 0.45);
            background: linear-gradient(145deg, #244b7a, #1a345a);
        }

        .btn-submit:active {
            transform: scale(0.97);
        }

        #messageBox {
            margin-top: 22px;
            padding: 16px 20px;
            border-radius: 20px;
            text-align: center;
            font-weight: 600;
            font-size: 16px;
            display: none;
        }

        .success {
            background: #e6f9ed;
            color: #0f5c3a;
            border: 1px solid #b8e6cd;
            display: block !important;
        }

        .error {
            background: #fce8e8;
            color: #a12b2b;
            border: 1px solid #f5c6c6;
            display: block !important;
        }

        .footer-note {
            margin-top: 28px;
            text-align: center;
            font-size: 14px;
            color: #6a7b8c;
            background: #f1f6fc;
            padding: 14px;
            border-radius: 30px;
            border: 1px solid #e6edf6;
        }

        .footer-note span {
            font-weight: 600;
            color: #1e3c72;
        }

        .credit {
            text-align: center;
            margin-top: 20px;
            font-size: 13px;
            color: #a0aeba;
        }

        .hidden-field {
            display: none;
            animation: fadeIn 0.3s ease;
        }

        .hidden-field.show {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @media (max-width: 500px) {
            .container {
                padding: 30px 20px;
            }
            .header h1 {
                font-size: 24px;
            }
            .header .icon {
                width: 65px;
                height: 65px;
                font-size: 36px;
                line-height: 65px;
            }
            .btn-submit {
                font-size: 17px;
                padding: 14px;
            }
            .contact-row {
                flex-direction: column;
            }
            .budget-row {
                flex-direction: row;
            }
            .budget-row .budget-item {
                min-width: 110px;
                padding: 0 12px;
            }
        }
    </style>
</head>
<body>

<div class="container">
    <div class="header">
        <div class="icon">🏠</div>
        <h1>طلب سكن في بكين</h1>
        <p class="sub">نبحث عن شقة أحلامك في العاصمة</p>
    </div>

    <form id="requestForm">
        <div class="form-group">
            <label>📍 المنطقة المفضلة <span class="star">*</span></label>
            <select id="area" required>
                <option value="">-- اختر المنطقة --</option>
                <option value="تشاويانغ">تشاويانغ (朝阳)</option>
                <option value="هايديان">هايديان (海淀)</option>
                <option value="دونغتشنغ">دونغتشنغ (东城)</option>
                <option value="شيتشنغ">شيتشنغ (西城)</option>
                <option value="فنغتاي">فنغتاي (丰台)</option>
                <option value="تونغتشو">تونغتشو (通州)</option>
                <option value="أخرى">أخرى (اكتب في الملاحظات)</option>
            </select>
        </div>

        <div class="form-group">
            <label>📐 المساحة المطلوبة (م²) <span class="star">*</span></label>
            <select id="size" required>
                <option value="">-- اختر المساحة --</option>
                <option value="30-50">30 – 50 م²</option>
                <option value="50-80">50 – 80 م²</option>
                <option value="80-120">80 – 120 م²</option>
                <option value="120-180">120 – 180 م²</option>
                <option value="180+">أكثر من 180 م²</option>
            </select>
        </div>

        <div class="form-group">
            <label>🛏️ عدد الغرف <span class="star">*</span></label>
            <select id="rooms" required>
                <option value="">-- اختر عدد الغرف --</option>
                <option value="استوديو">استوديو</option>
                <option value="1 غرفة">1 غرفة</option>
                <option value="2 غرف">2 غرف</option>
                <option value="3 غرف">3 غرف</option>
                <option value="4 غرف فأكثر">4 غرف فأكثر</option>
            </select>
        </div>

        <div class="form-group">
            <label>💰 الإيجار الشهري المتوقع (باليوان الصيني ¥) <span class="star">*</span></label>
            <div class="budget-row">
                <div class="budget-item">
                    <span class="currency-symbol">¥</span>
                    <input type="number" id="budgetMin" placeholder="الحد الأدنى" min="0" step="100" required>
                </div>
                <span class="budget-separator">—</span>
                <div class="budget-item">
                    <span class="currency-symbol">¥</span>
                    <input type="number" id="budgetMax" placeholder="الحد الأقصى" min="0" step="100" required>
                </div>
            </div>
            <span class="budget-hint">💡 مثال: 3000 — 8000 يوان شهرياً</span>
        </div>

        <div class="form-group">
            <label>🏫 القرب من جهة تعليمية <span class="star">*</span></label>
            <div class="radio-group" id="locationTypeGroup">
                <label class="radio-option">
                    <input type="radio" name="locationType" value="school" checked>
                    🏫 قريب من المدرسة السعودية في بكين
                </label>
                <label class="radio-option">
                    <input type="radio" name="locationType" value="university">
                    🎓 قريب من الجامعة
                </label>
            </div>
        </div>

        <div class="form-group hidden-field" id="universityField">
            <label>📚 اسم الجامعة <span class="star">*</span></label>
            <input type="text" id="universityName" placeholder="مثال: جامعة بكين، جامعة تسينغهوا، إلخ...">
        </div>

        <div class="divider">📱 وسائل التواصل</div>

        <div class="contact-row">
            <div class="form-group">
                <label>📧 البريد الإلكتروني</label>
                <input type="email" id="email" placeholder="name@example.com">
            </div>
            <div class="form-group">
                <label>💚 WeChat ID</label>
                <input type="text" id="wechat" placeholder="أدخل معرف WeChat">
            </div>
        </div>

        <div class="form-group">
            <label>📝 ملاحظات إضافية</label>
            <input type="text" id="notes" placeholder="مثل: قريب من المترو، مفروش، طابق مرتفع...">
        </div>

        <button type="button" class="btn-submit" id="submitBtn">
            <span>📩</span> إرسال الطلب
        </button>
    </form>

    <div id="messageBox"></div>

    <div class="footer-note">
        ⏳ سيتم التواصل معك خلال <span>24 ساعة</span> عبر الإيميل أو WeChat
    </div>
    <div class="credit">© 2026 – خدمة السكن في بكين</div>
</div>

<script>
    // ====== إظهار/إخفاء حقل اسم الجامعة ======
    const radioButtons = document.querySelectorAll('input[name="locationType"]');
    const universityField = document.getElementById('universityField');
    const universityInput = document.getElementById('universityName');

    radioButtons.forEach(radio => {
        radio.addEventListener('change', function() {
            if (this.value === 'university') {
                universityField.classList.add('show');
                universityInput.setAttribute('required', 'required');
            } else {
                universityField.classList.remove('show');
                universityInput.removeAttribute('required');
                universityInput.value = '';
            }
        });
    });

    // ====== زر الإرسال ======
    document.getElementById('submitBtn').addEventListener('click', function() {
        const area = document.getElementById('area').value;
        const size = document.getElementById('size').value;
        const rooms = document.getElementById('rooms').value;
        const budgetMin = document.getElementById('budgetMin').value.trim();
        const budgetMax = document.getElementById('budgetMax').value.trim();
        const email = document.getElementById('email').value.trim();
        const wechat = document.getElementById('wechat').value.trim();
        const notes = document.getElementById('notes').value;
        const msg = document.getElementById('messageBox');

        // نوع القرب
        let locationType = '';
        let locationDetail = '';
        radioButtons.forEach(radio => {
            if (radio.checked) {
                locationType = radio.value;
            }
        });

        if (locationType === 'university') {
            locationDetail = document.getElementById('universityName').value.trim();
        } else {
            locationDetail = 'المدرسة السعودية في بكين';
        }

        // التحقق من الحقول الأساسية
        if (area === '' || size === '' || rooms === '') {
            msg.className = 'error';
            msg.textContent = '⚠️ الرجاء تعبئة المنطقة، المساحة، وعدد الغرف.';
            return;
        }

        if (budgetMin === '' || budgetMax === '') {
            msg.className = 'error';
            msg.textContent = '⚠️ الرجاء إدخال الحد الأدنى والحد الأقصى للإيجار الشهري.';
            return;
        }

        const minVal = parseInt(budgetMin);
        const maxVal = parseInt(budgetMax);
        if (isNaN(minVal) || isNaN(maxVal) || minVal < 0 || maxVal < 0) {
            msg.className = 'error';
            msg.textContent = '⚠️ الرجاء إدخال أرقام صحيحة للإيجار.';
            return;
        }
        if (minVal > maxVal) {
            msg.className = 'error';
            msg.textContent = '⚠️ الحد الأدنى يجب أن يكون أقل من أو يساوي الحد الأقصى.';
            return;
        }

        if (locationType === 'university' && locationDetail === '') {
            msg.className = 'error';
            msg.textContent = '⚠️ الرجاء كتابة اسم الجامعة.';
            return;
        }

        if (email === '' && wechat === '') {
            msg.className = 'error';
            msg.textContent = '⚠️ الرجاء إدخال إما البريد الإلكتروني أو WeChat ID للتواصل.';
            return;
        }

        if (email !== '') {
            const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (!emailPattern.test(email)) {
                msg.className = 'error';
                msg.textContent = '❌ البريد الإلكتروني غير صحيح (مثل: name@example.com).';
                return;
            }
        }

        // ====== بناء البيانات للإرسال ======
        const formData = {
            المنطقة: area,
            المساحة: size,
            عدد_الغرف: rooms,
            الإيجار_الشهري_الحد_الأدنى: minVal + ' ¥',
            الإيجار_الشهري_الحد_الأقصى: maxVal + ' ¥',
            القرب_من: locationType === 'school' ? 'المدرسة السعودية' : 'الجامعة',
            اسم_الجامعة: locationType === 'university' ? locationDetail : 'غير مطلوب',
            الإيميل: email || 'غير مقدم',
            WeChat: wechat || 'غير مقدم',
            ملاحظات: notes || 'لا يوجد'
        };

        // ====== إرسال البيانات إلى بريدك عبر Formspree ======
        fetch('https://formspree.io/f/movevqgr', {
            method: 'POST',
            headers: {
                'Content-Type': 'application/json'
            },
            body: JSON.stringify(formData)
        })
        .then(response => {
            if (response.ok) {
                msg.className = 'success';
                msg.textContent = '✅ تم إرسال المتطلبات بنجاح! سنتواصل معك خلال 24 ساعة.';
                console.log('📋 تم الإرسال إلى البريد:', formData);
                // إعادة تعيين النموذج (اختياري)
                // document.getElementById('requestForm').reset();
            } else {
                msg.className = 'error';
                msg.textContent = '❌ حدث خطأ في الإرسال، حاول مرة أخرى.';
                console.error('❌ خطأ في الإرسال:', response.status);
            }
        })
        .catch(error => {
            msg.className = 'error';
            msg.textContent = '❌ مشكلة في الاتصال، تأكد من الإنترنت.';
            console.error('❌ مشكلة في الاتصال:', error);
        });
    });
</script>

</body>
</html>
