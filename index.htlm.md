
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gửi đến người đặc biệt ❤️</title>

<style>

body{
margin:0;
padding:0;
display:flex;
justify-content:center;
align-items:center;
height:100vh;
background:#ffe6e6;
font-family:Arial;
overflow:hidden;
}

.container{
text-align:center;
background:white;
padding:40px;
border-radius:20px;
box-shadow:0 10px 25px rgba(0,0,0,0.1);
width:400px;
max-width:90%;
}

h1{
color:#ff4d4d;
}

.gif-container img{
width:150px;
margin-bottom:20px;
}

.btn-group{
margin-top:30px;
display:flex;
justify-content:center;
gap:20px;
}

button{
padding:10px 30px;
font-size:18px;
border:none;
border-radius:50px;
cursor:pointer;
}

#yesBtn{
background:#ff4d4d;
color:white;
}

#noBtn{
background:#e0e0e0;
}

.hidden{
display:none;
}

.success-message{
color:#ff4d4d;
font-size:24px;
margin-top:20px;
}

</style>
</head>

<body>

<div class="container">

<div class="gif-container">
<img src="https://media.giphy.com/media/MDJ9IbxxvDUQM/giphy.gif">
</div>

<h1 id="question">Bạn có ghét tớ không?</h1>

<div class="btn-group">

<button id="yesBtn" onmouseover="moveYes()">Có</button>
<button id="noBtn" onclick="notHate()">Không</button>

</div>

<div id="success" class="hidden success-message">

<h2>Yay! Yêu bạn nhiều ❤️</h2>

<img src="https://media.giphy.com/media/26BRv0ThflsHCqDrG/giphy.gif">

</div>

</div>

<script>

const question=document.getElementById("question")
const yesBtn=document.getElementById("yesBtn")
const noBtn=document.getElementById("noBtn")
const success=document.getElementById("success")

function moveYes(){

const x=Math.random()*(window.innerWidth-100)
const y=Math.random()*(window.innerHeight-50)

yesBtn.style.position="fixed"
yesBtn.style.left=x+"px"
yesBtn.style.top=y+"px"

}

function notHate(){

question.innerText="Vậy làm người yêu tớ nhé? ❤️"

yesBtn.innerText="Có ❤️"
noBtn.innerText="Không 😆"

yesBtn.onclick=acceptLove
yesBtn.onmouseover=null

noBtn.onmouseover=moveNo

}

function moveNo(){

const x=Math.random()*(window.innerWidth-100)
const y=Math.random()*(window.innerHeight-50)

noBtn.style.position="fixed"
noBtn.style.left=x+"px"
noBtn.style.top=y+"px"

}

function acceptLove(){

question.innerText="Tớ biết mà ❤️"

yesBtn.style.display="none"
noBtn.style.display="none"

success.classList.remove("hidden")

}

</script>
</body>
</html>