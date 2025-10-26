<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Калькулятор</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #89f7fe, #66a6ff);
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0;
    }
    .calc {
      background: white;
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0 0 15px rgba(0,0,0,0.2);
      text-align: center;
    }
    input {
      width: 80px;
      padding: 8px;
      margin: 5px;
      border: 1px solid #ccc;
      border-radius: 5px;
      text-align: center;
      font-size: 16px;
    }
    select {
      padding: 8px;
      font-size: 16px;
      border-radius: 5px;
    }
    button {
      background: #007bff;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 5px;
      font-size: 16px;
      cursor: pointer;
      margin-top: 10px;
    }
    button:hover {
      background: #0056b3;
    }
    h2 {
      color: #333;
    }
  </style>
</head>
<body>
  <div class="calc">
    <h2>🧮 Простой калькулятор</h2>
    <input type="number" id="num1" placeholder="Число 1">
    <select id="op">
      <option value="+">+</option>
      <option value="-">−</option>
      <option value="*">×</option>
      <option value="/">÷</option>
    </select>
    <input type="number" id="num2" placeholder="Число 2">
    <br>
    <button onclick="calculate()">Посчитать</button>
    <h3 id="result"></h3>
  </div>

  <script>
    function calculate() {
      const num1 = parseFloat(document.getElementById('num1').value);
      const num2 = parseFloat(document.getElementById('num2').value);
      const op = document.getElementById('op').value;
      let res;

      if (isNaN(num1) || isNaN(num2)) {
        res = 'Введите оба числа!';
      } else {
        switch (op) {
          case '+': res = num1 + num2; break;
          case '-': res = num1 - num2; break;
          case '*': res = num1 * num2; break;
          case '/': 
            res = num2 !== 0 ? (num1 / num2).toFixed(2) : 'Деление на 0!';
            break;
        }
      }
      document.getElementById('result').innerText = 'Результат: ' + res;
    }
  </script>
</body>
</html># my-first-site
1
