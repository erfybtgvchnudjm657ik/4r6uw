<!DOCTYPE html>
<html>
<head>
    <title>Azzam's Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        .calculator {
            width: 300px;
            margin: 0 auto;
            padding: 20px;
            border: 2px solid #ccc;
            border-radius: 10px;
        }
        input {
            margin: 5px;
            padding: 5px;
        }
        button {
            margin: 10px;
            padding: 5px 15px;
            cursor: pointer;
        }
        #result {
            margin-top: 20px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>Azzam's Website for Calculations</h1>
    <div class="calculator">
        <input type="number" id="num1" placeholder="Enter first number">
        <select id="operator">
            <option value="+">+</option>
            <option value="-">-</option>
            <option value="*">×</option>
            <option value="/">÷</option>
        </select>
        <input type="number" id="num2" placeholder="Enter second number">
        <br>
        <button onclick="calculate()">Calculate</button>
        <div id="result">Result will appear here</div>
    </div>

    <script>
        let attempts = 0;
        const messages = [
            "Azzam did not program me to do this.",
            "I forgot.",
            "Use your mobile calculator.",
            "I told you to use your mobile calculator.",
            "Get out of here, now.",
            "I will not work again. You have annoyed me."
        ];

        function calculate() {
            const num1 = document.getElementById('num1').value;
            const num2 = document.getElementById('num2').value;
            const operator = document.getElementById('operator').value;
            
            if (attempts >= 5) {
                document.querySelector('.calculator').innerHTML = messages[5];
                return;
            }

            document.getElementById('result').textContent = messages[attempts];
            attempts++;
        }
    </script>
</body>
</html>
