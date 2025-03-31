
```html
<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>الإجازات المرضية</title>
  <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Cairo', sans-serif;
    }

    body {
      background-color: #f7f9fc;
      direction: rtl;
      text-align: center;
      color: #333;
    }

    .container {
      max-width: 600px;
      margin: 0 auto;
      padding: 20px;
      background-color: #ffffff;
      border-radius: 8px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.0);
    }

    .logo {
      width: 350px;
      margin: 20px auto;
      display: block;
    }

    h1 {
      color: #005eb8;
      font-size: 40px;
      margin-bottom: 15px;
    }

    p {
      font-size: 15px;
      color: #888eb0;
      margin-bottom: 20px;
      line-height: 1.7;
    }

    input[type="text"] {
      width: 100%;
      padding: 1px;
      margin-bottom: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-size: 16px;
    }

    input::placeholder {
      color: #aaa;
    }

    button {
      width: 40%;
      padding: 0px;
      background-color: #005eb8;
      color: #fff;
      border: none;
      border-radius: 5px;
      font-size: 16px;
      cursor: pointer;
      margin-bottom: 20px;
    }

    button:hover {
      background-color: #004a95;
    }

    .back-button {
      width: 40%;
      padding: 0px;
      background-color: #005eb8;
      color: #fff;
      border: none;
      font-size: 16px;
      cursor: pointer;
    }

    .back-button:hover {
      background-color: #004a95;
    }

    #result {
      display: none;
      margin-top: 25px;
      padding: 25px;
      background-color: #e0e0e0;
      border: 1px solid #e0e0e0;
      border-radius: 4px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }

    .result-item {
      text-align: center;
      margin-bottom: 23px;
    }

    .result-item span {
      display: block;
      font-weight: bold;
      color: #333;
      margin-bottom: 6px;
    }

    .result-item h6 {
      font-size: 16px;
      color: #333;
    }

    footer {
      margin-top: 80px;
      background-color: #005eb8;
      color: #fff;
      padding: 20px;
      font-size: 15px;
      text-align: center;
    }

    footer img {
      width: 100px;
      margin: 30px;
    }

    footer a {
      color: #fff;
      text-decoration: none;
      margin: 0 40px;
    }

    footer a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <div class="container">
    <img src="1001408484.jpg" alt="شعار صحتي" class="logo">
    <h1>الإجازات المرضية</h1>
    <p>خدمة الاستعلام عن الإجازات المرضية تتيح لك الاستعلام عن حالة طلبك للإجازة ويمكنك طباعتها عن طريق تطبيق صحتي.</p>
    
    <form id="sickLeaveForm">
      <input type="text" id="serviceCode" name="serviceCode" placeholder="رمز الخدمة" required>
      <input type="text" id="idNumber" name="idNumber" placeholder="رقم الهوية / الإقامة" required>
      <button type="submit">استعلام</button>
    </form>
    <button type="button" class="back-button">رجوع للاستعلامات</button>

    <div id="result">
      <div class="result-item">
        <span>الاسم:</span>
        <h6>ماجد محمود حيدرة عبدالملك </h6>
      </div>
      <div class="result-item">
        <span>تاريخ إصدار تقرير الإجازة:</span>
        <h6>2025-03-03</h6>
      </div>
      <div class="result-item">
        <span>تبدأ من:</span>
        <h6>2025-03-03</h6>
      </div>
      <div class="result-item">
        <span>وحتى:</span>
        <h6>2025-03-05</h6>
      </div>
      <div class="result-item">
        <span>المدة بالأيام:</span>
        <h6>1</h6>
      </div>
      <div class="result-item">
        <span>اسم الطبيب:</span>
        <h6>سعيد ابو الزيت </h6>
      </div>
      <div class="result-item">
        <span>المسمى الوظيفي:</span>
        <h6>طبيب عام</h6>
      </div>
    </div>
  </div>

  <footer>
    <img src="https://example.com/images/ministry-logo.png" alt="شعار وزارة الصحة">
    <img src="https://example.com/images/lean-logo.png" alt="شعار لين">
    <p>
      منصة صحة معتمدة من قبل وزارة الصحة © 2025
    </p>
    <a href="#">دليل الاستخدام</a> | <a href="#">سياسة الخصوصية وشروط الاستخدام</a>
    <p>
      920002005 | support@seha.sa
    </p>
  </footer>

  <script>
    document.getElementById("sickLeaveForm").addEventListener("submit", function(event) {
      event.preventDefault();
      document.getElementById("result").style.display = "block";
    });

    const serviceCodeInput = document.getElementById("serviceCode");
    const idNumberInput = document.getElementById("idNumber");

    serviceCodeInput.addEventListener("focus", function() {
      serviceCodeInput.placeholder = "";
    });

    serviceCodeInput.addEventListener("blur", function() {
      if (!serviceCodeInput.value) {
        serviceCodeInput.placeholder = "رمز الخدمة";
      }
    });

    idNumberInput.addEventListener("focus", function() {
      idNumberInput.placeholder = "";
    });

    idNumberInput.addEventListener("blur", function() {
      if (!idNumberInput.value) {
        idNumberInput.placeholder = "رقم الهوية / الإقامة";
      }
    });
  </script>
</body>
</html>
```

