DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <title>Form Đăng Nhập</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f2f2f2;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .login-box {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px gray;
            width: 300px;
        }

        h2 {
            text-align: center;
        }

        input {
            width: 100%;
            padding: 8px;
            margin: 8px 0;
        }

        button {
            width: 100%;
            padding: 8px;
            background: blue;
            color: white;
            border: none;
            border-radius: 5px;
        }

        button:hover {
            background: darkblue;
        }
    </style>
</head>
<body>

<div class="login-box">
    <h2>Đăng Nhập</h2>
    <form>
        <label>Tên đăng nhập:</label>
        <input type="text" placeholder="Nhập tên đăng nhập" required>

        <label>Mật khẩu:</label>
        <input type="password" placeholder="Nhập mật khẩu" required>

        <button type="submit">Đăng nhập</button>
    </form>
</div>

</body>
</html>
