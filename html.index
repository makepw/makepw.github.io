<랜덤 비밀번호 생성기 >
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>비밀번호 생성기</title>
<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
  }
  .password {
    font-size: 1.5em;
    margin-top: 20px;
    padding: 10px;
    border: 1px solid #ccc;
    width: 300px;
    display: inline-block;
  }
</style>
</head>
<body>
  <h1>Password Generator</h1>
  <button onclick="generatePassword()">비밀번호 생성</button>
  <div id="password" class="password"></div>

<script>
function generatePassword() {
  var length = 8;
  var charset = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789!@#?_";
  var password = "";
  
  for (var i = 0; i < length; i++) {
    var randomIndex = Math.floor(Math.random() * charset.length);
    password += charset[randomIndex];
  }
  
  document.getElementById("password").textContent = password;
}
</script>
</body>
</html>
