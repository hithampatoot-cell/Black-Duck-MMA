<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Black Duck MMA</title>
    <style>
        body {
            background: black;
            color: white;
            text-align: center;
            font-family: Arial, sans-serif;
            padding-top: 50px;
        }
        input {
            padding: 10px;
            margin: 5px;
            width: 80%;
            max-width: 300px;
            border-radius: 5px;
            border: 1px solid #444;
            background: #222;
            color: white;
        }
        button {
            padding: 10px 20px;
            background: #ff4500;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            margin-top: 10px;
        }
        button:hover {
            background: #ff6347;
        }
        .link-text {
            margin-top: 15px;
            font-size: 0.9em;
            color: #bbb;
        }
        a { color: #ff4500; text-decoration: none; }
    </style>
</head>
<body>

    <h1>🔥 Black Duck MMA 🔥</h1>
    <p>Welcome Fighters 👊</p>

    <form id="authForm">
        <input type="email" placeholder="الايميل (Email)" required><br>
        <input type="password" placeholder="الباسورد (Password)" required><br>
        
        <button type="submit" id="mainBtn">تسجيل الدخول</button>
    </form>

    <div class="link-text" id="toggleText">
        ليس لديك حساب؟ <a href="#" onclick="toggleMode()">إنشاء حساب جديد</a>
    </div>

    <script>
        let isLogin = true;

        function toggleMode() {
            isLogin = !isLogin;
            const mainBtn = document.getElementById('mainBtn');
            const toggleText = document.getElementById('toggleText');
            
            if (isLogin) {
                mainBtn.innerText = "تسجيل الدخول";
                toggleText.innerHTML = 'ليس لديك حساب؟ <a href="#" onclick="toggleMode()">إنشاء حساب جديد</a>';
            } else {
                mainBtn.innerText = "إنشاء حساب جديد";
                toggleText.innerHTML = 'لديك حساب بالفعل؟ <a href="#" onclick="toggleMode()">تسجيل الدخول</a>';
            }
        }

        document.getElementById('authForm').onsubmit = function(e) {
            e.preventDefault();
            const action = isLogin ? "تم تسجيل دخولك يا بطل!" : "تم إنشاء حسابك بنجاح في Black Duck MMA!";
            alert(action);
        };
    </script>

</body>
</html>

