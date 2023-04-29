<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>page main</title>
    <link rel="stylesheet" href="abc.css">
    
</head>
<body>
    <section>
        <div class="login">
            <div class="title">Hello!</div>
            <div class="des">
                Welcome back you've<br>
                been missed!
            </div>
            <div class="group">
                <input type="text" id="username"
                    placeholder="Enter username">
            </div>
            <div class="group">
                <input type="password" id="password"
                    placeholder="Password">
                <span id="showPassword">
                    <ion-icon name="eye-outline"></ion-icon>
                    <ion-icon name="eye-off-outline"></ion-icon>
                </span>
            </div>
            <div class="recovey">
                <a href="Recovery password"></a>
            </div>
            <div class="signIn">
                <button>Sign In</button>
            </div>
            <div class="or">Or continue with</div>
            <div class="list">
                <div class="item">
                    <img src="google.webg" alt="">
                </div>
                <div class="item">
                    <img src="fb.png" alt="">
                </div>
                <div class="item">
                    <img src="twitter.png" alt="">
                </div>
            </div>
            <div class="register">
                Not a member? <a href="">Register now</a>
            </div>
        </div>
        
    </section>
<script src="abc.js"></script>
<script type = "module" src = "https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.esm.js" > </script> 
<script nomodule src = "https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.js"></script>
</body>
</html>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@700&display=swap');
body{
    font-family: 'Roboto', sans-serif;
    color:#222;
    background-image: 
    linear-gradient(
        200deg, #7045d3, #ab65f0
    );
    margin: 0;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}
a{
    text-decoration: none;
    color: #1364df;   
}
.login{
    background-color: #efefef;
    width: 270px;
    text-align: center;
    border: 2px solid #efefef;
    border-radius: 30px;
    padding: 50px 30px;
    box-shadow: 0 50px 150px #5553;
}
.login .title{
    font-size: x-large;
    font-weight: bold;
    margin-bottom: 20px;
}
.login .des{
    margin-bottom: 20px;
}
.login .group{
    background-color: #fff;
    border-radius: 10px;
    height: 50px;
    margin-bottom: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
}
.login .group input{
    width: 100%;
    height: 100%;
    background-color: transparent;
    border: none;
    outline: none;
    padding: 20px;
    font-family: 'Roboto',sans-serif;
}
.login .group span{
    color: #777;
    display: flex;
    margin-right: 15px;
    cursor: pointer;
}
.login .group span ion-icon:nth-child(2){
    display: none;
}
.login .group span.show ion-icon:nth-child(2){
    display: block;
}
.login .group span.show ion-icon:nth-child(1){
    display: none;
}
.login .recovery{
    text-align: right;
    margin-bottom: 20px;
    font-size: small;
}
.login .signIn button{
    background-color: #fa6a69;
    width: 100%;
    height: 50px;
    border-radius: 10px;
    border: none;
    font-family: 'Roboto', sans-serif;
    color: #fff;
    box-shadow: 0 10px 20px #fa6a6999;
    margin-bottom: 40px;
    transition: 0.5s;
}
.login .signIn button:active{
    transform: translateY(5px);
    box-shadow: none;
}
.login .or{
    font-size: small;
    margin-bottom: 20px;
    position: relative;
}
.login .or::after,.login .or::before{
    position: absolute;
    width: 50px;
    height: 1px;
    content: '';
    background-image: 
        linear-gradient(
            to left, #444, transparent
    );
    top: 50%;
    left: 20px;
}
.login .or::after{
    left: unset;
    right: 20px;
    background-image: 
        linear-gradient(
            to right, #444, transparent
    );
}
.login .list img{
    width: 30px;
}
.login .list{
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 40px;
    gap: 20px;
    margin-bottom: 20px;
}
.login .item{
    border: 1px solid #fff;
    border-radius: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
}
.login .registor{
    font-size: small;
}
let showPassword = document.getElementById('showPassword');
let inputPassword = document.getElementById('password');
showPassword.onclick = function(){
    if(inputPassword.type == 'password'){
        inputPassword.type = 'text';
        showPassword.classList.add('show');
    }
    else{
        inputPassword.type = 'password';
        showPassword.classList.remove('show');
    }
}
