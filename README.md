# CALCULATOR

## AIM
To design and develop a simple calculator using HTML, CSS, and JavaScript.

## PROGRAM
```html
<!DOCTYPE html>
<html>
<head>
  <title>Calculator</title>
  <style>
    body { display: flex; justify-content: center; margin-top: 40px; }
    .calculator { width: 260px; background: #222; padding: 15px; border-radius: 10px; }
    #display { width: 100%; height: 50px; font-size: 24px; text-align: right; margin-bottom: 10px; box-sizing: border-box; }
    .buttons { display: grid; grid-template-columns: repeat(4, 1fr); gap: 8px; }
    button { height: 50px; font-size: 20px; border: none; border-radius: 6px; cursor: pointer; }
  </style>
</head>
<body>
  <div class="calculator">
    <input type="text" id="display" disabled>
    <div class="buttons">
      <button onclick="add('7')">7</button>
      <button onclick="add('8')">8</button>
      <button onclick="add('9')">9</button>
      <button onclick="add('/')">/</button>
      <button onclick="add('4')">4</button>
      <button onclick="add('5')">5</button>
      <button onclick="add('6')">6</button>
      <button onclick="add('*')">*</button>
      <button onclick="add('1')">1</button>
      <button onclick="add('2')">2</button>
      <button onclick="add('3')">3</button>
      <button onclick="add('-')">-</button>
      <button onclick="add('0')">0</button>
      <button onclick="add('.')">.</button>
      <button onclick="calculate()">=</button>
      <button onclick="add('+')">+</button>
      <button onclick="clearDisplay()" style="grid-column: span 4;">C</button>
    </div>
  </div>

  <script>
    const display = document.getElementById("display");

    function add(value) {
      display.value += value;
    }

    function calculate() {
      try {
        display.value = eval(display.value);
      } catch {
        display.value = "Error";
      }
    }

    function clearDisplay() {
      display.value = "";
    }
  </script>
</body>
</html>
```

## OUTPUT
<img width="580" height="490" alt="image" src="https://github.com/user-attachments/assets/a1bb3886-0f7c-4270-8b43-f0afb1ebf117" />


## RESULT
Thus, a JavaScript-based calculator was successfully designed and developed.
