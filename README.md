<!DOCTYPE html>
<html>
<head>
<title>For Keerthiga 🌹</title>
<style>
body{
text-align:center;
font-family:Arial;
background:#ffe6f0;
}

#step2,#result{
display:none;
}

button{
padding:10px 20px;
font-size:18px;
margin:10px;
cursor:pointer;
}

#noBtn{
position:absolute;
}

.petals{
position:fixed;
top:-10px;
color:red;
font-size:20px;
animation:fall 5s linear infinite;
}

@keyframes fall{
0%{transform:translateY(-10px);}
100%{transform:translateY(100vh);}
}
</style>
</head>

<body>

<h1>Hi Keerthiga 🌹🤍</h1>

<div id="step1">
<p>Click next...</p>
<button onclick="next1()">Next</button>
</div>

<div id="step2">
<p>I want to ask you something...</p>
<button onclick="showQuestion()">Next</button>
</div>

<div id="result">
<h2>Will you be mine? 💖</h2>

<button onclick="yes()">Yes</button>
<button id="noBtn" onmouseover="move()">No</button>
</div>

<script>

function next1(){
document.getElementById("step1").style.display="none";
document.getElementById("step2").style.display="block";
}

function showQuestion(){
document.getElementById("step2").style.display="none";
document.getElementById("result").style.display="block";
}

function move(){
let btn=document.getElementById("noBtn");
btn.style.top=Math.random()*400+"px";
btn.style.left=Math.random()*400+"px";
}

function yes(){
alert("Yay! Keerthiga said YES 💖");
}

function createPetal(){
let petal=document.createElement("div");
petal.className="petals";
petal.innerHTML="🌹";
petal.style.left=Math.random()*100+"vw";
petal.style.animationDuration=(Math.random()*3+2)+"s";
document.body.appendChild(petal);

setTimeout(()=>{petal.remove()},5000);
}

setInterval(createPetal,300);

</script>

</body>
</html>
