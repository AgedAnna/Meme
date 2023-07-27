# Pedido de Namoro com JS
<h1>HTML :</h1>

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <link rel="stylesheet" href="stely.css">
    <link rel="icon" type="image/svg" href="https://images.vexels.com/media/users/3/318413/isolated/preview/17ff412266bfeec2285f267cc98920e4-capivara-usando-um-belo-chapa-u.png"/>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Namora</title>
</head>
<body>
    <div class="box">
        <p>Quer Namorar Comigo ?</p>
        <div class="buttons-container">
            <button>
                <a href="parabenms/parabens.html">Sim</a>
            </button>
            <button id="no">Não</button>
        </div>
    </div>

<script src="main.js"></script>

</body>
</html>
```
<h1>CSS :</h1>

```css
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500&display=swap');

body {
    font-family: 'Poppins', sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

a {
    text-decoration: none;
}

.box {
    font-size: 20px;
    color: white;
    height: 250px;
    width: 350px;
    border-radius: 10px;
    background: linear-gradient(45deg, #c300ff, #ff00c8, #0000ff, #ff0000);
    flex-direction: column;
    display: flex;
    align-items: center;
    justify-content: center;
    background-size: 400% 400%;
    animation: gradientAnimation 10s ease infinite;
}

@keyframes gradientAnimation {
    0% {
        background-position: 0% 50%;
    }
    50% {
        background-position: 100% 50%;
    }
    100% {
        background-position: 0% 50%;
    }
}


.buttons-container {
    display: flex;
    justify-content: space-around;
    height: 50px;
    width: 150px;
}

button {
    height: 30px;
    width: 50px;
    background: white;
    border-radius: 5px;
    color: rgb(255, 0, 0);
    font-weight: 600;
}
```
<h1>JS :</h1>

```js
let button = document.getElementById('no');
let height = window.innerHeight - 50;
let width = window.innerWidth - 50;

button.addEventListener('mouseover', function(){
    button.style.position = "absolute";
    button.style.top = Math.random() * height + "px";
    button.style.left = Math.random() * width + "px";
})
```
