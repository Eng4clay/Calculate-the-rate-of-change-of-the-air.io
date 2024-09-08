# Calculate-the-rate-of-change-of-the-air.io
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>https://eng4clay.github.io/Calculate-the-rate-of-change-of-the-air.io/</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            direction: rtl;
            text-align: right;
            margin: 20px;
        }
        .container {
            max-width: 600px;
            margin: auto;
            padding: 20px;
            border: 1px solid #ddd;
            border-radius: 8px;
            background-color: #f9f9f9;
        }
        h1 {
            text-align: center;
        }
        label {
            display: block;
            margin: 10px 0 5px;
        }
        input {
            width: 100%;
            padding: 8px;
            margin-bottom: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        button {
            width: 100%;
            padding: 10px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        .result {
            margin-top: 20px;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            background-color: #e7f3e7;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>حساب معدل تغير الهواء</h1>
        <label for="cfm">معدل تدفق الهواء (CFM):</label>
        <input type="number" id="cfm" placeholder="أدخل معدل تدفق الهواء بالقدم المكعب في الدقيقة">
       <label for="length">طول الغرفة (قدم):</label>
        <input type="number" id="length" placeholder="أدخل طول الغرفة بالقدم">
           <label for="width">عرض الغرفة (قدم):</label>
        <input type="number" id="width" placeholder="أدخل عرض الغرفة بالقدم">
         <label for="height">ارتفاع الغرفة (قدم):</label>
        <input type="number" id="height" placeholder="أدخل ارتفاع الغرفة بالقدم">
          <button onclick="calculateACH()">احسب معدل تغير الهواء</button>
           <div class="result" id="result"></div>
    </div>
  <script>
        function calculateACH() {
            const cfm = document.getElementById('cfm').value;
            const length = document.getElementById('length').value;
            const width = document.getElementById('width').value;
            const height = document.getElementById('height').value;
                 if (cfm && length && width && height) {
                const roomVolume = length * width * height;
                const ach = (cfm * 60) / roomVolume;
                document.getElementById('result').innerHTML = `معدل تغير الهواء: ${ach.toFixed(2)} مرات في الساعة`;
            } else {
ة           document.getElementById('result').innerHTML = 'يرجى إدخال جميع القيم المطلوبة.';
                 } 
  </script>
</body>
</html>
