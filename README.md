<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Password Generator</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #0366D6;
            font-family: Arial, sans-serif;
        }
        .container {
            text-align: center;
            background-color: #fff;
            padding: 50px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            max-width: 400px; /* 크기 고정 */
            width: 100%;
        }
        .password-input {
            font-size: 16px;
            padding: 10px;
            width: 90%;
            box-sizing: border-box;
            margin-bottom: 20px;
            border: 1px solid #ccc;
            border-radius: 4px;
            outline: none;
        }
        .generate-button {
            font-size: 16px;
            padding: 10px 20px;
            cursor: pointer;
            background-color: #4CAF50;
            color: #fff;
            border: none;
            border-radius: 4px;
        }
        .generate-button:hover {
            background-color: #45a049;
        }
        .generated-password {
            font-size: 18px;
            font-weight: bold;
            padding: 20px;
            margin-top: 20px;
            word-break: break-all;
            background-color: #f9f9f9;
            border: 1px solid #ccc;
            border-radius: 4px;
            height: 100px; /* 크기 고정 */
            width: 100%; /* 크기 고정 */
            overflow: auto; /* 텍스트가 넘칠 때 스크롤 */
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>비밀번호 생성기</h2>
        <input type="number" id="lengthInput" class="password-input" min="1" max="50" placeholder="비밀번호 길이 입력">
        <button onclick="generatePassword()" class="generate-button">비밀번호 생성</button>
        <div id="generatedPassword" class="generated-password">여기에 비밀번호가 표시됩니다.</div>
    </div>

    <script>
        function generatePassword() {
            var length = document.getElementById("lengthInput").value;
            var password = generateRandomPassword(length);
            document.getElementById("generatedPassword").textContent = password;
        }

        function generateRandomPassword(length) {
            var charset = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789!@#?$%^&*";
            var password = "";
            for (var i = 0; i < length; i++) {
                var randomIndex = Math.floor(Math.random() * charset.length);
                password += charset[randomIndex];
            }
            return password;
        }
    </script>
</body>
</html>
