<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Be My Valentine</title>

<style>
body{
    font-family: Arial, sans-serif;
    background:#0f2027;
    color:white;
    text-align:center;
    margin-top:100px;
}

.container{
    background:white;
    color:black;
    padding:30px;
    border-radius:10px;
    width:350px;
    margin:auto;
}

button{
    padding:10px 20px;
    border:none;
    border-radius:5px;
    cursor:pointer;
    font-size:16px;
}

.yes-button{
    background:#ff2d75;
    color:white;
}

.no-button{
    background:#ccc;
}

img{
    width:120px;
}
</style>
</head>

<body>

<h1>Be My Valentine ❤️</h1>

<div class="container">

<img src="https://media.tenor.com/kqjL17yufz4AAAAi/love-bear.gif">

<p>Will you be my Valentine?</p>

<button class="yes-button" onclick="handleYesClick()">Yes</button>
<button class="no-button" onclick="handleNoClick()">No</button>

</div>

<script>

let messages = [
"Are you sure?",
"Really sure?",
"Think again 😢",
"Please say yes ❤️",
"I'll be sad...",
"Last chance!"
];

let messageIndex = 0;

function handleNoClick() {

const noButton = document.querySelector('.no-button');
const yesButton = document.querySelector('.yes-button');

noButton.textContent = messages[messageIndex];

messageIndex = (messageIndex + 1) % messages.length;

const currentSize = parseFloat(window.getComputedStyle(yesButton).fontSize);

yesButton.style.fontSize = `${currentSize * 1.4}px`;

}

function handleYesClick(){
window.location.href = "yes.html";
}

</script>

</body>
</html>
