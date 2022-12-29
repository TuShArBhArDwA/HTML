#Index
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ShoesStore</title>
    <link rel="stylesheet" href="main.css">
 <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<style>

</style>
</head>
<body>
  <p class="navbar-brand" href="#">ShoesStore</p>
<div class="topnav" id="myTopnav">
  <a href="#home" class="active">Home</a>
  <a href="./product.html">Products</a>
  <a href="contact.html" >Contact Us</a>
  <a href="./about.html">About Us</a>
  <a href="javascript:void(0);" class="icon" onclick="myFunction()">
    <i class="fa fa-bars"></i>
  </a>
</div>


    <div class="img-slider">
      <div class="slide active">
        <img src="1.jpg" alt="">
        <div class="info">
   <br><br> <h2>From out store to your feet</h2>
          
        </div>
      </div>
      <div class="slide">
        <img src="2.jpg" alt="">
        <div class="info">
          <h2>The best shoes at the tip of your fingers.</h2>
        </div>
      </div>
      <div class="slide">
        <img src="3.jpg" alt="">
        <div class="info">
          <h2>We made shoes. </h2><h2>You spread the word.</h2>
        </div>
      </div>
      <div class="slide">
        <img src="4.jpg" alt="">
        <div class="info">
          <h2>Feel the earth beneath your feet.</h2>
          
        </div>
      </div>
      <div class="slide">
        <img src="5.jpg" alt="">
        <div class="info">
          <h2>We make every step comfortable.</h2>
          
        </div>
      </div>
      <div class="navigation">
        <div class="btn active"></div>
        <div class="btn"></div>
        <div class="btn"></div>
        <div class="btn"></div>
        <div class="btn"></div>
      </div>
    </div>

    <script type="text/javascript">
    var slides = document.querySelectorAll('.slide');
    var btns = document.querySelectorAll('.btn');
    let currentSlide = 1;

    // Javascript for image slider manual navigation
    var manualNav = function(manual){
      slides.forEach((slide) => {
        slide.classList.remove('active');

        btns.forEach((btn) => {
          btn.classList.remove('active');
        });
      });

      slides[manual].classList.add('active');
      btns[manual].classList.add('active');
    }

    btns.forEach((btn, i) => {
      btn.addEventListener("click", () => {
        manualNav(i);
        currentSlide = i;
      });
    });

    // Javascript for image slider autoplay navigation
    var repeat = function(activeClass){
      let active = document.getElementsByClassName('active');
      let i = 1;

      var repeater = () => {
        setTimeout(function(){
          [...active].forEach((activeSlide) => {
            activeSlide.classList.remove('active');
          });

        slides[i].classList.add('active');
        btns[i].classList.add('active');
        i++;

        if(slides.length == i){
          i = 0;
        }
        if(i >= slides.length){
          return;
        }
        repeater();
      }, 10000);
      }
      repeater();
    }
    repeat();
    </script>
<script>
function myFunction() {
  var x = document.getElementById("myTopnav");
  if (x.className === "topnav") {
    x.className += " responsive";
  } else {
    x.className = "topnav";
  }
}
</script>
  </body>
</html>


#Product tab
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Products</title>
    <style>
    body{
        background-color:  #4e2804;
        font-family:  'Playfair Display', serif;
    }
    
    #our{
        text-align: center;
        font-size: 40px;
        color: white;
    }
    .navbar-brand {
	    color: rgba(255, 192, 167, 0.932);
        font-size: 20px;
        font-family: Georgia, 'Times New Roman', Times, serif;
        letter-spacing: 2px;
        position: absolute;
        top: 20px;
        left: 50px;
}
    #info{
        display: grid;
        grid-template-columns: repeat(auto-fit,minmax(300px,1fr));
        grid-column-gap: 10px;
        grid-row-gap: 10px;
    }
    #info img{
        width: 100%;
    }
    #info img:hover{
        border-top-left-radius: 50px;
    }
    .img{
        box-sizing: border-box;
        box-shadow: 12px 10px 12px rgba(0, 0, 0, 0.5);
    }
    .img:hover{
        box-shadow: none;
        background-color: #fff;
        border-bottom-right-radius: 50px;
        border-top-left-radius: 50px;
    }
    
    button{
        padding: 10px;
        background: rgba(0, 0, 0, 0.5);
        color: #fff;
        border: none;
        box-shadow: 12px 10px 12px rgba(0, 0, 0, 0.5);
    }
    @media (max-width: 710px){

    .navbar-brand {
        font-size: 15px;
        top:20px;
        left:15px;
    }
}
    </style>
</head>
<body>
    <p class="navbar-brand" href="#">ShoesStore</p><br><br>
    <h1 id="our">Our Products</h1>
    <div id="info">
        
<div class="img">
    <img src="./1/1.jpg">
    <div class="img-desc">
        <h4><b>Name:</b> Blue Canvas Shoes</h4>
        <p><b>Price:</b> Rs. 500/-</p>
        <button>Add to cart</button>
    </div>
</div>

 <div class="img">
    <img src="./1/2.jpg">
    <div class="img-desc">
        <h4><b>Name:</b> White Sports Shoes</h4>
        <p><b>Price:</b> Rs. 700/-</p>
        <button>Add to cart</button>
    </div>
</div>

 <div class="img">
    <img src="./1/3.jpg">
    <div class="img-desc">
        <h4><b>Name:</b>Black Formal Lace Shoes</h4>
        <p><b>Price:</b> Rs. 600/-</p>
        <button>Add to cart</button>
    </div>
</div>

 <div class="img">
    <img src="./1/4.jpg">
    <div class="img-desc">
        <h4><b>Name:</b> Brown Formal Shoes</h4>
        <p><b>Price:</b> Rs. 650/-</p>
        <button>Add to cart</button>
    </div>
</div>

 <div class="img">
    <img src="./1/5.jpg">
    <div class="img-desc">
        <h4><b>Name:</b> White Football Shoes</h4>
        <p><b>Price:</b> Rs. 750/-</p>
        <button>Add to cart</button>
    </div>
</div>

 <div class="img">
    <img src="./1/6.jpg">
    <div class="img-desc">
        <h4><b>Name:</b> Brown Formal Shoes</h4>
        <p><b>Price:</b> Rs. 600/-</p>
        <button>Add to cart</button>
    </div>
</div>

 <div class="img">
    <img src="./1/7.jpg">
    <div class="img-desc">
        <h4><b>Name:</b> Black Sports Shoes</h4>
        <p><b>Price:</b> Rs. 750/-</p>
        <button>Add to cart</button>
    </div>
</div>

 <!-- start item 8 -->
 <div class="img">
    <img src="./1/8.jpg">
    <div class="img-desc">
        <h4><b>Name:</b> Brown Leather shoes</h4>
        <p><b>Price:</b> Rs. 690/-</p>
        <button>Add to cart</button>
    </div>
</div>

 <div class="img">
    <img src="./1/9.jpg">
    <div class="img-desc">
        <h4><b>Name:</b>Brown Formal Lace Shoes</h4>
        <p><b>Price:</b> Rs. 600/-</p>
        <button>Add to cart</button>
    </div>
</div>


<div class="img">
    <img src="./1/10.jpg">
    <div class="img-desc">
        <h4><b>Name:</b> Yellow Sneakers</h4>
        <p><b>Price:</b> Rs. 800/-</p>
        <button>Add to cart</button>
    </div>
</div>
<div class="img">
    <img src="./1/11.png">
    <div class="img-desc">
        <h4><b>Name:</b> Brown Formal Shpes</h4>
        <p><b>Price:</b> Rs. 800/-</p>
        <button>Add to cart</button>
    </div>
</div>
<div class="img">
    <img src="./1/12.png">
    <div class="img-desc">
        <h4><b>Name:</b> Black Formal Shoes</h4>
        <p><b>Price:</b> Rs. 600/-</p>
        <button>Add to cart</button>
    </div>
</div>
    </div>
    
</body>
</html>


#Contact Us Tab
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Contact Us</title>
    <link rel="stylesheet" href="style.css">
    <meta name="viewport" content="width=device-width, initial-scale=1">
     <style>*{
  margin: 0;
  padding: 0;
  font-family: "montserrat",sans-serif;
}
body,html{
height: 100%;
} 
 .navbar-brand {
	    color: rgba(255, 192, 167, 0.932);
        font-size: 20px;
        font-family: Georgia, 'Times New Roman', Times, serif;
        letter-spacing: 2px;
        position: absolute;
        top: 20px;
        left: 50px;
}
.contact-section{
  background: url("bg.png");
background-repeat:  no-repeat;
background-position: center ;
height: 100%;
  background-size: cover;
  /*padding: 40px 0;*/
}
.contact-section h1{
  text-align: center;
  color: #ddd;
}
.border{
  width: 100px;
  height: 10px;
  background: #34495e;
  margin: 40px auto;
}

.contact-form{
  max-width: 600px;
  margin: auto;
  padding: 0 10px;
  overflow: hidden;
}

.contact-form-text{
  display: block;
  width: 100%;
  box-sizing: border-box;
  margin: 16px 0;
  border: 0;
  background: #4e2804;
  padding: 20px 40px;
  outline: none;
  color: rgb(255, 255, 255);
  transition: 0.5s;
}
.contact-form-text:focus{
  box-shadow: 0 0 10px 4px  rgba(255, 192, 167, 0.932);;
}
textarea.contact-form-text{
  resize: none;
  height: 120px;
}
.contact-form-btn{
  background-color :#4e2804;
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
}

.contact-form-btn:hover{
  background:#f59f7d;
}
</style> 
 </head>
  <body>

<div class="contact-section">
  <p class="navbar-brand" href="#">ShoesStore</p><br><br>

<br><br>
  <h1>Contact Us</h1>
 <br><br>
  <form class="contact-form" action="index.html" method="post">
    <input type="text" class="contact-form-text" placeholder="Your name">
    <input type="email" class="contact-form-text" placeholder="Your email">
    <input type="text" class="contact-form-text" placeholder="Your phone">
    <textarea class="contact-form-text" placeholder="Your message"></textarea>
    <input type="submit" class="contact-form-btn" value="Send">
  </form>
</div>


  </body>
</html>


#Contac us Tab
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <title>About Us</title>
        <meta name="viewport" content="width=device-width, initial-scale=1">
       
        <script src="https://kit.fontawesome.com/dbed6b6114.js" crossorigin="anonymous"></script>
        <style>
            @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&display=swap');

*{
    box-sizing: border-box;
    padding: 0;
    margin: 0;
    
}
html,body{
    font-family: 'Playfair Display', serif;
    display: grid;
    background-color: #4e2804;
    align-content: center;
    min-height: 100vh;
    height: 100%;
}
.navbar-brand {
	    color: rgba(255, 192, 167, 0.932);
        font-size: 20px;
        font-family: Georgia, 'Times New Roman', Times, serif;
        letter-spacing: 2px;
        position: absolute;
        top: 20px;
        left: 50px;
}
section{
    display: grid;
    grid-template-columns: 1fr 1fr;
    min-height: 70vh;
    width: 95vw;
    margin: 0 auto;
}
.image{
    background: url("./2.jpg") center/cover no-repeat;
}
.content{
    background: #fff;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
}
.content h2{
    text-transform: uppercase;
    font-size: 36px;
    letter-spacing: 6px;
    opacity: 0.9;
}
.content span{
    height: 0.5px;
    width: 100px;
    background: #777;
    margin: 20px 0;
}
.content p{
    top: 60px;
    padding-bottom: 15px;
    font-weight: 100;
    opacity: 0.7;
    width: 90%;
    text-align: center;
    margin: 0 auto;
    line-height: 1.7;
}

.vertical-line{
    height: 30px;
    width: 0.5px;
    background: #777;
    margin: 0 auto;
}
.icons{
    display: flex;
    padding: 15px 0;
}
.icons li{
    display: block;
    padding: 5px;
    margin: 5px;
}
.icons li i{
    font-size: 26px;
    opacity: 0.8;
}
.icons li i:hover{
    color: #4e2804;
}
.button {
  background-color :#4e2804;
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
}
.button:hover{
    background-color: #f59f7d;
}

/*****************/

@media(max-width: 992px){
    .navbar-brand{
        font-size: 15px;
        top:10px;
        left:15px; 
    }
    section{
        grid-template-columns: 1fr;
        width: 100%;
    }
    .image{
        height: 100vh;
    }
    .content{
        height: 100vh;
    }
    .content h2{
        font-size: 20px;
        margin-top: 50px;
    }
    .content span{
        margin: 20px 0;
    }
    .content p{
        font-size: 14px;
    }
    
}
        </style>
    </head>
    <body>
        <p class="navbar-brand" href="#">ShoesStore</p><br><br>
        <section>
            <div class = "image">
                
            </div>

            <div class = "content">
                <h2>About Us</h2>
                <span><!-- line here --></span>

                <p>For each one of those shoe sweethearts out there, ‘ShoesStore’ offer the one-stop goal to pick the correct match of footwear. To satisfy the affection for shoes, we offer heaps of alternatives from driving footwear marks, all under one rooftop. Gone are the days when you needed to go from store to store to locate the correct style and size for yourself. At ‘ShoesStore’ , you can locate a vast accumulation of dashing footwear in all sizes and styles, all inside a couple of snaps.</p>

                <a href="./product.html" class="button">Let's Shop</a>

                <ul class = "icons">
                    <li>
                        <i class = "fa fa-twitter"></i>
                    </li>
                    <li>
                        <i class = "fa fa-facebook"></i>
                    </li>
                    <li>
                        <i class = "fa fa-instagram"></i>
                    </li>
                    <li>
                        <i class = "fa fa-pinterest"></i>
                    </li>
                </ul>
            </div>
        </section>
        
    </body>
</html>
