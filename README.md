<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Secure Login</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family: Consolas, monospace;
}

body{
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:#0f0f0f;
    color:#fff;
}

.box{
    width:350px;
    padding:35px;
    background:#1a1a1a;
    border-radius:12px;
    box-shadow:0 0 20px rgba(0,255,150,0.1);
}

h2{
    text-align:center;
    margin-bottom:25px;
    font-weight:normal;
    letter-spacing:1px;
}

input{
    width:100%;
    padding:10px;
    margin:10px 0;
    background:#111;
    border:1px solid #333;
    border-radius:6px;
    color:#fff;
}

input:focus{
    outline:none;
    border-color:#00ffaa;
}

button{
    width:100%;
    padding:10px;
    margin-top:15px;
    background:#00ffaa;
    border:none;
    border-radius:6px;
    color:#000;
    font-weight:bold;
    cursor:pointer;
    transition:0.3s;
}

button:hover{
    opacity:0.8;
}

.message{
    text-align:center;
    margin-top:15px;
    font-size:14px;
}
</style>
</head>

<body>

<div class="box">
    <h2>ACCESS SYSTEM</h2>

    <input type="text" id="user" placeholder="Username">
    <input type="password" id="pass" placeholder="Password">

    <button onclick="login()">LOGIN</button>

    <div class="message" id="msg"></div>
</div>

<script>
let savedUser = "admin";
let savedPass = "123456";

function login(){
    let u = document.getElementById("user").value;
    let p = document.getElementById("pass").value;

    if(u === savedUser && p === savedPass){
        document.getElementById("msg").innerHTML = "ACCESS GRANTED";
        document.getElementById("msg").style.color = "#00ffaa";
    }else{
        document.getElementById("msg").innerHTML = "ACCESS DENIED";
        document.getElementById("msg").style.color = "red";
    }
}
</script>

</body>
</html>