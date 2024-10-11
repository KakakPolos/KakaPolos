<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>IMBAS DATA LAMA</title>
        <style>
            body{ 
                background-color: linear-gradient(to right,#ff7e5f,#feb47b);
                display: flex;
                justify-content: center;
                align-items: center;
                height: 100vh;
                margin: 0;
                font-family: Arial, sans-serif;
                flex-direction: column;
            }
            .login-box, .dashboard {
                background-color: greenyellow;
                border: 19px solid green;
                box-shadow:0 0 80px rgba(0,0,0,0)
                padding: 90px 40px;
                width: 600px;
                text-align:center;
                border: radius 90px;
            }
            .dashboard {
                display: none;
            }
            h1 {
                font-size: 36px;
                color:darkblue;
                margin-bottom: 20px;
                font-family: 'segoe UI', sans-serif;
            }
            input [type="text"], input [type="password"]{
                width: 100px;
                padding: 10px;
                margin: 8px 0;
                box-sizing: border-box;
                border: 1px solid #dbdbdb;
                border-radius: 5px;
                font-size: 14px;
                background-color: #fafafa;
            }
           .login.button{
            background-color: white;
            color: white;
            border: none;
            padding: 10px;
            width: 100px;
            border-radius: 5px;
            font-size: 14px;
            margin-top: 10px;
            cursor: pointer;
           }
           .logout-button {
            margin-top: 20px;
            padding: 10px 20px;
            background-color: #ff4757;
            color: white;
            border: none;
            border-radius: 5px;
            cursor:pointer;
           }  
        </style>
<script> 
    function showLogin(){
        document.querySelector('.login-box').style.display = 'block';
        document.querySelector('.dashboard').style.display = 'none';
    }
    function showDashboard(){
        document.querySelector('.login-box').style.display = 'none';
        document.querySelector('.dashboard').style.display = 'block';
    }
    function login(){
        var username=document.getElementById('username').value;
        var username=document.getElementById('password').value;
    if (username && password){
        showDashboard();
    }else{
        alert("sila masukkan nama pengguna dan kata laluan!")
    }
    }
    function logout(){
        showLogin();

    }
    window.onload = function(){
        showLogin();
    }
    </script>
    </head>
<body>
    <div class="login-box">
    <h1>DAPATKAN DATA LAMA</h1>
    <input type="text" id="username" placeholder="Email"/><br>
    <input type="password" id="password" placeholder="Kata Laluan"/><br>
    <button class="login-button" onclick="login()">log masuk</button>
    <p class="small-text"> Belum Ada akaun? Daftar sekarang</p>
</div>
<div class="dashboard">
    <h1>Selamat data anda telah dicuri</h1>
    <div class="content">
        <p>kasihan deh loh</p>
        <button class="logout-button" onclick="logout()">Log Keluar</button>
    </div>
</div>
</body>
</html>
