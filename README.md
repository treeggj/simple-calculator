<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>حاسبة بسيطة</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin-top: 50px; }
        input, button { margin: 10px; }
    </style>
</head>
<body>
    <h1>حاسبة بسيطة</h1>
    <input type="number" id="inputNumber" placeholder="أدخل الرقم" />
    <button onclick="calculate()">احسب</button>
    <p id="result"></p>

    <script>
        function calculate() {
            const number = parseFloat(document.getElementById('inputNumber').value);
            if (isNaN(number)) {
                document.getElementById('result').innerText = 'يرجى إدخال رقم صحيح';
                return;
            }
            const multiplied = number * 2;
            const divided = multiplied / 100;
            const result = divided - number;
            document.getElementById('result').innerText = `النتيجة هي: ${result}`;
        }
    </script>
</body>
</html>
