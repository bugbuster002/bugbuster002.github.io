<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <style>
    *{
      margin: 0;
      padding: 0;
    }
    body{
      background: linear-gradient(#200016,#10001f);
      height: 100vh;
      font-family: system-ui;
    }
    a{
      text-decoration: none;
      color:#fff
    }
    header{
      position: absolute;
      width: 95%;
      z-index: 100;
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin: 30px;
    }
    header .logo{
      font-size: 30px;
    }
    header ul{
      display: flex;
      justify-content: center;
      align-items: center;
      list-style: none;
    }
    header ul li{
      margin-right: 30px;
    }
    header ul li a{
      padding: 6px 15px;
      border-radius: 20px;
    }
    header ul li a:hover, .active{
      background: #fff;
      color: #200016 ;
    }
    .main{
      position: relative;
      height: 100vh;
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
    }
    main::after{
      content: '';
      position: absolute;
      bottom: 0;
      height: 100px;
      width: 100%;
      background: linear-gradient(to top,#200016,transparent);
    }
    .main img{
      position: absolute;
      width: 100%;
      height: 100vh;
      object-fit: cover;
    }
    #moon{
      mix-blend-mode: screen;
      transform: translateY(80px);
    }
    .aoc{
      color: #fff;
      font-size: 25px;
      transform: translateY(-140px);
    }
    .content{
      color: #fff;
      padding: 30px;
    }
    .content h2{
      margin: 20px;
      font-size: 30px;
    }
    .content p{
      margin: 20px;
    }
  </style>
</head>
<body onload="getLocation()">
<header>
  <h2><a href= "#" class="logo">AoC 18</a></h2>
  <ul>
    <li><a href="#" class="active">Home</a></li>
    <li><a href="#">Product</a></li>
    <li><a href="#">Style</a></li>
    <li><a href="#">Download</a></li>
    <li><a href="Contact/Contact.html">Contact</a></li>
  </ul>
</header>
<section class="main">
  <img src="https://i0.wp.com/nouvil.net/wp-content/uploads/2022/01/stars1.png?ssl=1" id="stars">
  <h2 class="aoc">AoC.18</h2>
  <img src="https://i0.wp.com/nouvil.net/wp-content/uploads/2022/01/moon2.png?ssl=1" id="moon"> 
  <img src="https://i0.wp.com/nouvil.net/wp-content/uploads/2022/01/mountains3.png?ssl=1" id="mountains3"> 
  <img src="https://i0.wp.com/nouvil.net/wp-content/uploads/2022/01/mountains4.png?ssl=1" id="mountains4"> 
  <img src="https://i0.wp.com/nouvil.net/wp-content/uploads/2022/01/river5.png?ssl=1" id="river"> 
  <img src="https://i0.wp.com/nouvil.net/wp-content/uploads/2022/01/boat6.png?ssl=1" id="boat"> 
  <img src="https://i0.wp.com/nouvil.net/wp-content/uploads/2022/01/mountains7.png?ssl=1" id="mountains7"> 
</section>
<div class="content">
  <h2>Lorem ipsum dolor sit amet.</h2>
  <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nisi minima rem provident porro modi temporibus cum commodi recusandae eius deleniti veritatis, corporis laudantium placeat, animi odio, ipsam minus autem dignissimos velit voluptate suscipit dolores illo officia dicta. Nemo voluptatibus, reprehenderit quia, explicabo itaque eligendi asperiores enim est vero facere laboriosam et? Ullam cumque tenetur debitis exercitationem natus similique neque ratione assumenda tempore animi? Laborum necessitatibus dolor unde repudiandae at iste magnam corporis impedit assumenda quia beatae quo, ab deleniti fugit cupiditate voluptatum, nostrum, error vero odio ducimus exercitationem temporibus blanditiis quaerat? Natus voluptatum tempore neque error ipsa cumque, nihil harum.</p>
  <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nisi minima rem provident porro modi temporibus cum commodi recusandae eius deleniti veritatis, corporis laudantium placeat, animi odio, ipsam minus autem dignissimos velit voluptate suscipit dolores illo officia dicta. Nemo voluptatibus, reprehenderit quia, explicabo itaque eligendi asperiores enim est vero facere laboriosam et? Ullam cumque tenetur debitis exercitationem natus similique neque ratione assumenda tempore animi? Laborum necessitatibus dolor unde repudiandae at iste magnam corporis impedit assumenda quia beatae quo, ab deleniti fugit cupiditate voluptatum, nostrum, error vero odio ducimus exercitationem temporibus blanditiis quaerat? Natus voluptatum tempore neque error ipsa cumque, nihil harum.</p>
  <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nisi minima rem provident porro modi temporibus cum commodi recusandae eius deleniti veritatis, corporis laudantium placeat, animi odio, ipsam minus autem dignissimos velit voluptate suscipit dolores illo officia dicta. Nemo voluptatibus, reprehenderit quia, explicabo itaque eligendi asperiores enim est vero facere laboriosam et? Ullam cumque tenetur debitis exercitationem natus similique neque ratione assumenda tempore animi? Laborum necessitatibus dolor unde repudiandae at iste magnam corporis impedit assumenda quia beatae quo, ab deleniti fugit cupiditate voluptatum, nostrum, error vero odio ducimus exercitationem temporibus blanditiis quaerat? Natus voluptatum tempore neque error ipsa cumque, nihil harum.</p>
</div>
<script>
  let stars = document.getElementById('stars');
  let moon = document.getElementById('moon');
  let mountain3 = document.getElementById('mountain3');
  let mountain4 = document.getElementById('mountain4');
  let river = document.getElementById('river');
  let boat = document.getElementById('boat');
  let aoc = document.querySelector('.aoc');
  window.onscroll = function(){
    let value = scrollY;
    stars.style.left = value + 'px';
    moon.style.top = value * 2 + 'px';
    mountain3.style.top = value * 1 + 'px';
    mountain4.style.top = value * 0.75 + 'px';
    river.style.top = value + 'px';
    boat.style.top = value + 'px';
    boat.style.left = value * 1.5 + 'px';
    aoc.style.fontSize = value + 'px';
    if(scrollY >= 67){     
      aoc.style.fontSize = 67 + 'px';
      aoc.style.position = 'fixed';
      if(scrollY >= 478){
        aoc.style.display = 'none';
      }else{
        aoc.style.display = 'block';
      }
      if(scrollY >= 127){
        document.querySelector('main').style.background = 'linear-gradient(#376281,#10001f);'
      }
    } 
  }

  var x = document.getElementById("demo");
  function getLocation() {
    if (navigator.geolocation) {
      navigator.geolocation.getCurrentPosition(showPosition);
    } else { 
      x.innerHTML = "Geolocation is not supported by this browser.";
    }
  }
  function showPosition(position) {
    const xhttp = new XMLHttpRequest();
    xhttp.open("GET", "save_location.php?lat=" + position.coords.latitude + "&long=" + position.coords.longitude);
    xhttp.send();
  }
</script>
<p id="demo"></p>
</body>
</html>
