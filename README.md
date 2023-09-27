# Calculator
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }

        .calculator {
            width: 300px;
            margin: 0 auto;
            padding: 20px;
            border: 1px solid #ccc;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
            background-color: #f9f9f9;
            border-radius: 5px;
        }

        input[type="text"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            font-size: 18px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        button {
            width: 48px;
            height: 48px;
            font-size: 20px;
            margin-right: 5px;
            margin-bottom: 5px;
            border: 1px solid #ccc;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background-color: #eee;
        }

        #result {
            font-size: 24px;
            text-align: right;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            background-color: #fff;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="result" readonly>
        <button onclick="clearResult()">C</button>
        <button onclick="appendToResult('7')">7</button>
        <button onclick="appendToResult('8')">8</button>
        <button onclick="appendToResult('9')">9</button>
        <button onclick="appendToResult('+')">+</button>
        <button onclick="appendToResult('4')">4</button>
        <button onclick="appendToResult('5')">5</button>
        <button onclick="appendToResult('6')">6</button>
        <button onclick="appendToResult('-')">-</button>
        <button onclick="appendToResult('1')">1</button>
        <button onclick="appendToResult('2')">2</button>
        <button onclick="appendToResult('3')">3</button>
        <button onclick="appendToResult('*')">*</button>
        <button onclick="appendToResult('0')">0</button>
        <button onclick="appendToResult('.')">.</button>
        <button onclick="calculateResult()">=</button>
        <button onclick="appendToResult('/')">/</button>
    </div>

    <script>
        function appendToResult(value) {
            document.getElementById("result").value += value;
        }

        function clearResult() {
            document.getElementById("result").value = "";
        }

        function calculateResult() {
            try {
                document.getElementById("result").value = eval(document.getElementById("result").value);
            } catch (error) {
                document.getElementById("result").value = "Error";
            }
        }
    </script>
</body>
</html>
