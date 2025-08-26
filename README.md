# Simple-Calculator-Using-Javascript
## AIM:
Create a Simple Calculator using HTML, CSS, and JavaScript

## DESCRIPTION:
A basic calculator built using **HTML, CSS, and JavaScript**.  
It allows users to perform four basic arithmetic operations:

 ➕ Addition  
 ➖ Subtraction  
 ✖ Multiplication  
 ➗ Division  

## CODE:

### index.html
```
<!DOCTYPE html>
<html>
<head>
  <title>Simple Calculator</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <div class="calculator">
    <h2 style="color:#0a1cc2">Sanjay Ashwin's</h2>
    <h2>Simple Calculator</h2>

    <input type="number" id="num1" placeholder="Enter first number"><br>
    <input type="number" id="num2" placeholder="Enter second number"><br>

    <div class="buttons">
      <button class="add" onclick="calculate('add')">Add</button>
      <button class="sub" onclick="calculate('sub')">Subtract</button>
      <button class="mul" onclick="calculate('mul')">Multiply</button>
      <button class="div" onclick="calculate('div')">Divide</button>
    </div>

    <div id="result"></div>
  </div>

  <script src="script.js"></script>
</body>
</html>
```
### style.css
```
body {
  font-family: Arial, sans-serif;
  background: linear-gradient(135deg, #6a11cb, #2575fc);
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}
.calculator {
  background: #fff;
  width: 300px;
  padding: 20px;
  border-radius: 15px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.3);
  text-align: center;
}
h2 {
  margin-bottom: 15px;
  color: #444;
}
input {
  width: 90%;
  padding: 10px;
  margin: 8px 0;
  font-size: 16px;
  border: 1px solid #ccc;
  border-radius: 8px;
  outline: none;
}
input:focus {
  border-color: #2575fc;
}
.buttons {
  margin-top: 15px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px;
}
button {
  padding: 10px;
  font-size: 16px;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: 0.2s;
  color: #fff;
}
button:hover {
  opacity: 0.9;
}
.add { background: #28a745; }
.sub { background: #dc3545; }
.mul { background: #ffc107; color: #000; }
.div { background: #007bff; }
#result {
  margin-top: 15px;
  font-size: 18px;
  font-weight: bold;
  color: #222;
}
```
### script.js
```
function calculate(op) {
  let n1 = parseFloat(document.getElementById("num1").value);
  let n2 = parseFloat(document.getElementById("num2").value);
  let result;

  if (isNaN(n1) || isNaN(n2)) {
    result = "Please enter both numbers";
  } else {
    if (op === "add") {
      result = n1 + n2;
    } else if (op === "sub") {
      result = n1 - n2;
    } else if (op === "mul") {
      result = n1 * n2;
    } else if (op === "div") {
      if (n2 !== 0) {
        result = n1 / n2;
      } else {
        result = "Cannot divide by 0";
      }
    }
  }

  document.getElementById("result").innerText = "Result: " + result;
}

```
## OUTPUT:
### ADD
<img width="1919" height="904" alt="image" src="https://github.com/user-attachments/assets/4dc8f648-9210-4948-b826-ef0a8cd60f52" />
### ADDITION
<img width="1911" height="904" alt="image" src="https://github.com/user-attachments/assets/a497d676-83c2-4a14-bf20-5682dc219f18" />
### SUBTRACTION
<img width="1905" height="887" alt="image" src="https://github.com/user-attachments/assets/7196a74e-0278-4646-96bc-bc8c9402c553" />
### MULTIPLICATION
<img width="1892" height="885" alt="image" src="https://github.com/user-attachments/assets/bf3faab9-d952-49c7-8110-29996b72cf68" />
### DIVISION
<img width="1919" height="894" alt="image" src="https://github.com/user-attachments/assets/30fb5562-1638-45a4-9e38-ec3e1bae4147" />


