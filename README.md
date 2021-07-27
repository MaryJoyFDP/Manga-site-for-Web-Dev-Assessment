# Manga-site-for-Web-Dev-Assessment

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Basic Manga</title>
    <link rel="stylesheet" href="index.css">
    <link rel="stylesheet" href="carousel.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
</head>

<body>
    <h1 style="font-size:24px" class="fa">&#xf07a;</h1>
    <nav class="nav_h2">
        <h2> B a s i c M a n g a</h2>
    </nav>

    <hr style="height:2px;border-width:0;color:gray;background-color:gray">

    <div class="slideshow-container">

        <div class="mySlides fade">
            <div class="numbertext">1 / 3</div>
            <img src="slide1.png" style="width:1000px" height="370px">

        </div>

        <div class="mySlides fade">
            <div class="numbertext">2 / 3</div>
            <img src="slide2.jpg" style=" width:1000px" height="370px">

        </div>

        <div class="mySlides fade">
            <div class="numbertext">3 / 3</div>
            <img src="slide3.jpg" style="width:1000px" height="370px">

        </div>

        <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
        <a class="next" onclick="plusSlides(1)">&#10095;</a>

    </div>
    <br>

    <div style="text-align:center">
        <span class="dot" onclick="currentSlide(1)"></span>
        <span class="dot" onclick="currentSlide(2)"></span>
        <span class="dot" onclick="currentSlide(3)"></span>
    </div>


    <div class="grid-container">
        <div class="card">
            <img src="cart1.png" style="width:100%">
            <h3>One Piece V98</h3>
            <p class="select">
            <p class="price">$19.99</p>
            <p>Japanese manga series <br>
                written and illustrated by Eiichiro Oda.</p>
            <p><button>Add to Cart</button></p>
            </p>
        </div>
        <div class="card">
            <img src="cart4.jpg" style="width:100%">
            <h3>Tokyo Ghoul v3</h3>
            <p class="price">$2.99</p>
            <p>Japanese dark fantasy manga series <br>
                written and illustrated by Sui Ishida.</p>
            <p><button>Add to Cart</button></p>
        </div>
        <div class="card">
            <img src="cart5.jpg" style="width:100%">
            <h3>Hero Academia V36</h3>
            <p class="price">$9.99</p>
            <p>Japanese superhero manga series written <br>
                and illustrated by Kōhei Horikoshi</p>
            <p><button>Add to Cart</button></p>
        </div>
        <br>
        <div class="card">
            <img src="cart6.jpg" style="width:100%">
            <h3>Sword Art Online</h3>
            <p class="price">$10.99</p>
            <p>is a Japanese light novel series written by Reki Kawahara</p>
            <p><button>Add to Cart</button></p>
        </div>
        <div class="card">
            <img src="cart7.jpg" style="width:100%">
            <h3>Demon Slayer V20</h3>
            <p class="price">$15.99</p>
            <p>series written and illustrated by Koyoharu Gotōge</p>
            <p><button>Add to Cart</button></p>
        </div>
        <div class="card">
            <img src="cart8.jpg" style="width:100%">
            <h3>Hunter X Hunter V10</h3>
            <p class="price">$7.99</p>
            <p>Japanese manga series written and illustrated by Yoshihiro Togashi</p>
            <p><button>Add to Cart</button></p>
        </div>
    </div>
    <div class="select">

    </div>


</body>
<script type="text/javascript" src="carousel.js"></script>
<script type="text/javascript" src="main.js"></script>


</html>


// JS Codes:

var noti = document.querySelector('h1');
var select = document.querySelector('.select');
var button = document.getElementsByTagName('button');
for (var but of button) {
    but.addEventListener('click', (e) => {
        var add = Number(noti.getAttribute('data-count') || 0);
        noti.setAttribute('data-count', add + 1);
        noti.classList.add('zero')

        var parent = e.target.parentNode;
        var clone = parent.cloneNode(true);
        select.appendChild(clone);
        clone.lastElementChild.innerText = "One Piece V98";
        if (clone) {
            noti.onclick = () => {
                select.classList.toggle('display');
            }
            window.onclick = function (event) {
                if (event.target == modal) {
                    modal.style.display = "none";
                }
            }

        }

    })
}


CSS Code:

body{
    margin: 0;
    background-color: rgb(243, 216, 167);
    
}
section{
    margin: 0%;
   
    height: 350px;
    width: 1280px;
}
h2{
    font-size: 30px;
    font-family: Copperplate Gothic Light;
    text-align: center;
}
.nav_h2{
    top: 1;
    left: 0;
    right: 0;
    bottom: 0;
    padding: 0;
    margin: 0; 
    background-color: rgb(243, 216, 167);   
}

.card {
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    max-width: 200px;
    margin: 10px;
    text-align: center;
    font-family: Century Gothic;
    display: inline-block;
    padding: auto;
}
  
.price {
color: green;
font-size: 22px;
}
  
.card button {
border: hidden;
outline: 0;
padding: 12px;
color: white;
background-color: #000;
text-align: center;
cursor: pointer;
width: 100%;
font-size: 15px;
}
  
  .card button:hover {
    opacity: 0.7;
  }
  .class-grid{
      margin: 30px;
  }
  .grid-container{
    margin: auto;
    width: 60%;
    padding: 10px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
img{
    width: 80px;
    height: 250px;
  }
button{
    max-width: 200px;
}
h1{
margin: 0%;
width: 3%;
position: relative;
top: 60px;
left: 90%;
cursor: pointer;
    
}
h1:before{
    content: attr(data-count);
    color: white;
    position: absolute;
    right: 16px;
    font-size: 15px;
    text-align: center;
    top: -12px;
    width: 20px;
    height: 20px;
    background: red;
    border-radius: 50%;
    opacity: 0;
}
h1.zero:before{
    opacity: 1;
}

.select{
    width: 60%;
    height: 580px;
    padding: 5%;
    background: #222;
    position: absolute;
    top: -1000px;
    left: 20%;
    transition: 0.5s;
    overflow-y: auto;
    margin: auto;
}
.select.display{
    top: 0;
}
.select div{
    width: 100%;
    height: 200px;
    display: flex;
    padding: 5px;
    border: 1px solid white;
    position: relative;
    margin: 5px auto;
}
.select div img{
    width: 300px;
    height: 100%;
}
.select div p{
    padding: 35px;
    color: white;
}
.select div h6,
.select div button{
    position: absolute;
    left: 45%;
    top: 50%;
    color: white;
}
.select div button{
    left: 60%;
    top: 55%;
}
.select div span{
    display: none;
}
  


