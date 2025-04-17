<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=0.50"/>
  <title>FMC GUEST CAFE Menu</title>
  <link href="l.jpg" rel="stylesheet">
  <style>
    :root {
      --primary: #0083a0;
      --bg: #f4f7fa;
      --white: #fff;
      --dark: #222;
      --glass: rgba(255, 255, 255, 0.75);
      --border: rgba(0,0,0,0.05);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Open Sans', sans-serif;
      background-color: var(--bg);
      color: var(--dark);
      overflow-x: hidden;
    }

    header {
      background: url('l.jpg') center/cover no-repeat;
      color: white;
      text-align: center;
      padding: 80px 20px 100px;
      position: relative;
    }

    header::after {
      content: "";
      position: absolute;
      top: 0; left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.4);
      z-index: 1;
    }

    header h1 {
      position: relative;
      z-index: 2;
      font-family: 'Playfair Display', serif;
      font-size: 75px;
      font-weight: 600;
    }

    .langs {
      position: sticky;
      top: 0;
      z-index: 99;
      background: var(--primary);
      padding: 10px 0;
      text-align: center;
    }

    .langs button {
      margin: 0 6px;
      padding: 10px 18px;
      font-size: 18px;
      border: none;
      border-radius: 4px;
      background: white;
      color: var(--primary);
      font-weight: 600;
      cursor: pointer;
      transition: 0.3s;
    }

    .langs button:hover {
      background: #006b87;
      color: white;
    }

    .menu {
      max-width: 1500px;
      margin: 20px auto;
      padding: 0 20px;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 20px;
    }

    .menu-card {
      background: var(--glass);
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 13px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.1);
      backdrop-filter: blur(10px);
      transition: transform 0.3s ease;
      overflow: auto;
    }

    .menu-card:hover {
      transform: translateY(-5px);
    }

    .menu-card h3 {
      color: var(--primary);
      font-size: 20px;
      margin-bottom: 8px;
    }

    .menu-card .price {
      color: #333;
      font-weight: bold;
      font-size: 16px;
    }

    .menu-card img {
      float: right;
    height: 100px;
      width: 150px;
     
      margin-left: 10px;
      border-radius: 10px;
    }

    .section-title {
      text-align: center;
      font-size: 32px;
      color: var(--primary);
      font-weight: 600;
      margin-top: 40px;
    }

    .lang-content {
      display: none;
      animation: fadeIn 0.3s ease-in-out;
    }

    .lang-content.active {
      display: block;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    footer {
      background-color: var(--primary);
      color: white;
      text-align: center;
      padding: 15px 10px;
      font-size: 14px;
      margin-top: 60px;
    }

    @media (max-width: 600px) {
      header h1 {
        font-size: 36px;
      }
    }
  </style>

  <script>
    function switchLang(lang) {
      document.querySelectorAll('.lang-content').forEach(el => el.classList.remove('active'));
      document.getElementById(lang).classList.add('active');
      localStorage.setItem('fmc_lang', lang);
    }

    window.onload = () => {
      const lang = localStorage.getItem('fmc_lang') || 'en';
      switchLang(lang);
    };
  </script>
</head>

<body>

<header>
  <h1>FMC GUEST CAFE MENU</h1>
</header>

<div class="langs">
  <button onclick="switchLang('en')">English</button>
  <button onclick="switchLang('ku')">کوردی</button>
  <button onclick="switchLang('ar')">العربية</button>
</div>

<!-- 🔤 English Menu -->
<div class="lang-content active" id="en">
  <h2 class="section-title">Breakfast</h2>
  <div class="menu">
    <div class="menu-card"> <img src="e.jpg" alt="Fried Eggs"><h3>boiled eggs</h3><div class="price">1500</div><div class="price">2 boiled eggs</div></div>
    <div class="menu-card"> <img src="3.jpg" alt="Fried Eggs"><h3>fried eggs</h3><div class="price">2000 </div></div>
    <div class="menu-card"> <img src="o.jpg" alt="Fried Eggs"><h3>omlette</h3><div class="price">2000 </div></div>
    <div class="menu-card"> <img src="m.jpg" alt="Fried Eggs"><h3>mekhlama</h3><div class="price">3000</div></div>
    <div class="menu-card"> <img src="nisk.jpg" alt="Fried Eggs"><h3>Lentil soup </h3><div class="price">1000</div></div>
    <div class="menu-card"> <img src="kchese.jpg" alt="Fried Eggs"><h3>kurdish cheese</h3><div class="price">2000 </div></div>
    <div class="menu-card"> <img src="kiri.jpg" alt="Fried Eggs"><h3>kiri cheese</h3><div class="price">500</div></div>
    <div class="menu-card"> <img src="kraft.jpg" alt="Fried Eggs"><h3>kraft cheese</h3><div class="price">2000</div></div>
    <div class="menu-card"> <img src="ksy.jpg" alt="Fried Eggs"><h3>kurdish sweet yogurt</h3><div class="price">2000 </div></div>
    <div class="menu-card"> <img src="ksoy.jpg" alt="Fried Eggs"><h3>kurdish sour yogurt </h3><div class="price">2000 </div></div>
    <div class="menu-card"> <img src="kala.jpg" alt="Fried Eggs"><h3>factory yogurt</h3><div class="price">1000</div></div>
    <div class="menu-card"> <img src="mr.jpg" alt="Fried Eggs"><h3>jam</h3><div class="price">500</div></div>
    <div class="menu-card"> <img src="nut.jpg" alt="Fried Eggs"><h3>walnut</h3><div class="price">1000</div></div>
    <div class="menu-card"> <img src="rashi.jpg" alt="Fried Eggs"><h3>tahini and date syrup</h3><div class="price">1000 </div></div>
    <div class="menu-card"> <img src="olv.jpg" alt="Fried Eggs"><h3>olive </h3><div class="price">1000 </div></div>
    <div class="menu-card"> <img src="m.jpg" alt="Fried Eggs"><h3>breakfast meal</h3><div class="price">7000</div></div>
    <div class="menu-card"> <img src="toast.jpg" alt="Fried Eggs"><h3>cheese toast</h3><div class="price">1000</div></div>
    <div class="menu-card"> <img src="sand.jpg" alt="Fried Eggs"><h3>cheese sandwich</h3><div class="price">1000 </div></div>
   
  
  </div>
 


  <h2 class="section-title">Fast Foods</h2>
  <div class="menu">
    <div class="menu-card"> <img src="burger.jpg" alt="Fried Eggs"><h3>cheese beef burger</h3><div class="price">9000</div></div>
    <div class="menu-card"> <img src="burger.jpg" alt="Fried Eggs"><h3>beef burger</h3><div class="price">8000</div></div>
    <div class="menu-card"> <img src="burger.jpg" alt="Fried Eggs"><h3>cheese Chicken burger</h3><div class="price">8000</div></div>
    <div class="menu-card"> <img src="burger.jpg" alt="Fried Eggs"><h3>Chicken burger</h3><div class="price">8000</div></div>
    <div class="menu-card"> <img src="fngr.jpg" alt="Fried Eggs"><h3>fries</h3><div class="price">3000 </div></div>
    <div class="menu-card"> <img src="steak.jpg" alt="Fried Eggs"><h3>steak</h3><div class="price">10000 </div></div>
    <div class="menu-card"> <img src="fahita.jpg" alt="Fried Eggs"><h3>fahita</h3><div class="price">10000</div></div>
    <div class="menu-card"> <img src="kntaki.jpg" alt="Fried Eggs"><h3>kentucky</h3><div class="price">10000</div></div>
    <div class="menu-card"> <img src="crispy.jpg" alt="Fried Eggs"><h3>crispy</h3><div class="price">10000 </div></div>
    <div class="menu-card"> <img src="pizza.jpg" alt="Fried Eggs"><h3>mix pizza</h3><div class="price">8000 </div></div>
    <div class="menu-card"> <img src="fahita.jpg" alt="Fried Eggs"><h3>Chicken pizza</h3><div class="price">8000</div></div>
    <div class="menu-card"> <img src="burger.jpg" alt="Fried Eggs"><h3>beef pizza</h3><div class="price">8000</div></div>
    <div class="menu-card"> <img src="fngr.jpg" alt="Fried Eggs"><h3>margrita pizza</h3><div class="price">7000 </div></div>
    <div class="menu-card"> <img src="skalop.jpg" alt="Fried Eggs"><h3>Chicken Escalope</h3><div class="price">10000 </div></div>
    <div class="menu-card"> <img src="fahita.jpg" alt="Fried Eggs"><h3>alfredo pasta</h3><div class="price">10000</div></div>
    </div>
 

  <h2 class="section-title">drinks</h2>
  <div class="menu">
    <div class="menu-card"> <img src="es.jpg" alt="Fried Eggs"><h3>espresso</h3><div class="price">3000</div></div>
    <div class="menu-card"> <img src="amer.jpg" alt="Fried Eggs"><h3>americano</h3><div class="price">4000 </div></div>
    <div class="menu-card"> <img src="cap.jpg" alt="Fried Eggs"><h3>capuccino</h3><div class="price">5000 </div></div>
    <div class="menu-card"> <img src="latte.jpg" alt="Fried Eggs"><h3>latte</h3><div class="price">5000</div></div>
    <div class="menu-card"> <img src="double.jpg" alt="Fried Eggs"><h3>double espresso</h3><div class="price">5000 </div></div>
    <div class="menu-card"> <img src="nes.jpg" alt="Fried Eggs"><h3>nescafe</h3><div class="price">2000 </div></div>
    <div class="menu-card"> <img src="or.jpg" alt="Fried Eggs"><h3>orange juice</h3><div class="price">5000</div></div>
    <div class="menu-card"> <img src="apj.jpg" alt="Fried Eggs"><h3>apple juice</h3><div class="price">5000</div></div>
    <div class="menu-card"> <img src="lemon.jpg" alt="Fried Eggs"><h3>lemon juice</h3><div class="price">5000</div></div>
    <div class="menu-card"> <img src="carot.jpg" alt="Fried Eggs"><h3>carrot juice</h3><div class="price">5000</div></div>
    <div class="menu-card"> <img src="or.jpg" alt="Fried Eggs"><h3>cocktail juice</h3><div class="price">5000</div></div>
    <div class="menu-card"> <img src="tea.jpg" alt="Fried Eggs"><h3>tea</h3><div class="price">500</div></div>
    <div class="menu-card"> <img src="water.jpg" alt="Fried Eggs"><h3>water</h3><div class="price">500</div></div>


 
  </div>

  <h2 class="section-title">sweets</h2>
  <div class="menu">
    <div class="menu-card"> <img src="cake.jpg" alt="Fried Eggs"><h3>cake</h3><div class="price">3000</div></div>
    <div class="menu-card"> <img src="tralicha.jpg" alt="Fried Eggs"><h3>tres laches cake</h3><div class="price">3000 </div></div>
    <div class="menu-card"> <img src="crwason.jpg" alt="Fried Eggs"><h3>Croissant</h3><div class="price">3000 </div></div>
    <div class="menu-card"> <img src="cinama.jpg" alt="Fried Eggs"><h3>Cinnamon Roll
    </h3><div class="price">3500</div></div>
    <div class="menu-card"> <img src="sans.jpg" alt="Fried Eggs"><h3>san sebastian cake</h3><div class="price">6000</div></div>
    <div class="menu-card"> <img src="kwlicha.jpg" alt="Fried Eggs"><h3>kliecha</h3><div class="price">2500 </div></div>
    <div class="menu-card"> <img src="shaklama.jpg" alt="Fried Eggs"><h3>shakrlama</h3><div class="price">2500 </div></div>
    <div class="menu-card"> <img src="mahalabi.jpg" alt="Fried Eggs"><h3>mahalabia</h3><div class="price">2000</div></div>
    <div class="menu-card"> <img src="cupc.jpg" alt="Fried Eggs"><h3>cup cake</h3><div class="price">3000 </div></div>
    </div>
  </div>

</div>









<!-- 🌐 Kurdish Menu -->
<div class="lang-content" id="ku" dir="rtl">
  <h2 class="section-title">نانی بەیانی</h2>
  <div class="menu">
    <div class="menu-card"> <img src="e.jpg" alt="Fried Eggs"><h3>هێلکەی کوڵاو</h3><div class="price">١٥٠٠ </div></div>
    <div class="menu-card"> <img src="3.jpg" alt="Fried Eggs"><h3>هێلکەی سورەوکراو</h3><div class="price">٢٠٠٠ </div></div>
    <div class="menu-card"> <img src="o.jpg" alt="Fried Eggs"><h3>ئۆملێت</h3><div class="price">٢٠٠٠ </div></div>
    <div class="menu-card"> <img src="m.jpg" alt="Fried Eggs"><h3>مەخلەمە</h3><div class="price">٣٠٠٠ </div></div>
    <div class="menu-card"> <img src="nisk.jpg" alt="Fried Eggs"><h3>Lentil soup </h3><div class="price">1000</div></div>
    <div class="menu-card"> <img src="kchese.jpg" alt="Fried Eggs"><h3>kurdish cheese</h3><div class="price">2000 </div></div>
    <div class="menu-card"> <img src="kiri.jpg" alt="Fried Eggs"><h3>kiri cheese</h3><div class="price">500</div></div>
    <div class="menu-card"> <img src="kraft.jpg" alt="Fried Eggs"><h3>kraft cheese</h3><div class="price">2000</div></div>
    <div class="menu-card"> <img src="ksy.jpg" alt="Fried Eggs"><h3>kurdish sweet yogurt</h3><div class="price">2000 </div></div>
    <div class="menu-card"> <img src="ksoy.jpg" alt="Fried Eggs"><h3>kurdish sour yogurt </h3><div class="price">2000 </div></div>
    <div class="menu-card"> <img src="kala.jpg" alt="Fried Eggs"><h3>factory yogurt</h3><div class="price">1000</div></div>
    <div class="menu-card"> <img src="mr.jpg" alt="Fried Eggs"><h3>jam</h3><div class="price">500</div></div>
    <div class="menu-card"> <img src="nut.jpg" alt="Fried Eggs"><h3>walnut</h3><div class="price">1000</div></div>
    <div class="menu-card"> <img src="rashi.jpg" alt="Fried Eggs"><h3>tahini and date syrup</h3><div class="price">1000 </div></div>
    <div class="menu-card"> <img src="olv.jpg" alt="Fried Eggs"><h3>olive </h3><div class="price">1000 </div></div>
    <div class="menu-card"> <img src="m.jpg" alt="Fried Eggs"><h3>breakfast meal</h3><div class="price">7000</div></div>
    <div class="menu-card"> <img src="toast.jpg" alt="Fried Eggs"><h3>cheese toast</h3><div class="price">1000</div></div>
    <div class="menu-card"> <img src="sand.jpg" alt="Fried Eggs"><h3>cheese sandwich</h3><div class="price">1000 </div></div>
  </div>


<h2 class="section-title">Fast Foods</h2>
<div class="menu">
  <div class="menu-card"> <img src="burger.jpg" alt="Fried Eggs"><h3>cheese beef burger</h3><div class="price">9000</div></div>
  <div class="menu-card"> <img src="burger.jpg" alt="Fried Eggs"><h3>beef burger</h3><div class="price">8000</div></div>
  <div class="menu-card"> <img src="burger.jpg" alt="Fried Eggs"><h3>cheese Chicken burger</h3><div class="price">8000</div></div>
  <div class="menu-card"> <img src="burger.jpg" alt="Fried Eggs"><h3>Chicken burger</h3><div class="price">8000</div></div>
  <div class="menu-card"> <img src="fngr.jpg" alt="Fried Eggs"><h3>fries</h3><div class="price">3000 </div></div>
  <div class="menu-card"> <img src="steak.jpg" alt="Fried Eggs"><h3>steak</h3><div class="price">10000 </div></div>
  <div class="menu-card"> <img src="fahita.jpg" alt="Fried Eggs"><h3>fahita</h3><div class="price">10000</div></div>
  <div class="menu-card"> <img src="kntaki.jpg" alt="Fried Eggs"><h3>kentucky</h3><div class="price">10000</div></div>
  <div class="menu-card"> <img src="crispy.jpg" alt="Fried Eggs"><h3>crispy</h3><div class="price">10000 </div></div>
  <div class="menu-card"> <img src="pizza.jpg" alt="Fried Eggs"><h3>mix pizza</h3><div class="price">8000 </div></div>
  <div class="menu-card"> <img src="fahita.jpg" alt="Fried Eggs"><h3>Chicken pizza</h3><div class="price">8000</div></div>
  <div class="menu-card"> <img src="burger.jpg" alt="Fried Eggs"><h3>beef pizza</h3><div class="price">8000</div></div>
  <div class="menu-card"> <img src="fngr.jpg" alt="Fried Eggs"><h3>margrita pizza</h3><div class="price">7000 </div></div>
  <div class="menu-card"> <img src="skalop.jpg" alt="Fried Eggs"><h3>Chicken Escalope</h3><div class="price">10000 </div></div>
  <div class="menu-card"> <img src="fahita.jpg" alt="Fried Eggs"><h3>alfredo pasta</h3><div class="price">10000</div></div>
  </div>

  <h2 class="section-title">drinks</h2>
  <div class="menu">
    <div class="menu-card"> <img src="es.jpg" alt="Fried Eggs"><h3>espresso</h3><div class="price">3000</div></div>
    <div class="menu-card"> <img src="amer.jpg" alt="Fried Eggs"><h3>americano</h3><div class="price">4000 </div></div>
    <div class="menu-card"> <img src="cap.jpg" alt="Fried Eggs"><h3>capuccino</h3><div class="price">5000 </div></div>
    <div class="menu-card"> <img src="latte.jpg" alt="Fried Eggs"><h3>latte</h3><div class="price">5000</div></div>
    <div class="menu-card"> <img src="double.jpg" alt="Fried Eggs"><h3>double espresso</h3><div class="price">5000 </div></div>
    <div class="menu-card"> <img src="nes.jpg" alt="Fried Eggs"><h3>nescafe</h3><div class="price">2000 </div></div>
    <div class="menu-card"> <img src="or.jpg" alt="Fried Eggs"><h3>orange juice</h3><div class="price">5000</div></div>
    <div class="menu-card"> <img src="apj.jpg" alt="Fried Eggs"><h3>apple juice</h3><div class="price">5000</div></div>
    <div class="menu-card"> <img src="lemon.jpg" alt="Fried Eggs"><h3>lemon juice</h3><div class="price">5000</div></div>
    <div class="menu-card"> <img src="carot.jpg" alt="Fried Eggs"><h3>carrot juice</h3><div class="price">5000</div></div>
    <div class="menu-card"> <img src="or.jpg" alt="Fried Eggs"><h3>cocktail juice</h3><div class="price">5000</div></div>
    <div class="menu-card"> <img src="tea.jpg" alt="Fried Eggs"><h3>tea</h3><div class="price">500</div></div>
    <div class="menu-card"> <img src="water.jpg" alt="Fried Eggs"><h3>water</h3><div class="price">500</div></div>


 
  </div>

  <h2 class="section-title">sweets</h2>
  <div class="menu">
    <div class="menu-card"> <img src="cake.jpg" alt="Fried Eggs"><h3>cake</h3><div class="price">3000</div></div>
    <div class="menu-card"> <img src="tralicha.jpg" alt="Fried Eggs"><h3>tres laches cake</h3><div class="price">3000 </div></div>
    <div class="menu-card"> <img src="crwason.jpg" alt="Fried Eggs"><h3>Croissant</h3><div class="price">3000 </div></div>
    <div class="menu-card"> <img src="cinama.jpg" alt="Fried Eggs"><h3>Cinnamon Roll
    </h3><div class="price">3500</div></div>
    <div class="menu-card"> <img src="sans.jpg" alt="Fried Eggs"><h3>san sebastian cake</h3><div class="price">6000</div></div>
    <div class="menu-card"> <img src="kwlicha.jpg" alt="Fried Eggs"><h3>kliecha</h3><div class="price">2500 </div></div>
    <div class="menu-card"> <img src="shaklama.jpg" alt="Fried Eggs"><h3>shakrlama</h3><div class="price">2500 </div></div>
    <div class="menu-card"> <img src="mahalabi.jpg" alt="Fried Eggs"><h3>mahalabia</h3><div class="price">2000</div></div>
    <div class="menu-card"> <img src="cupc.jpg" alt="Fried Eggs"><h3>cup cake</h3><div class="price">3000 </div></div>
    </div>
  </div>

</div>




<!-- 🌐 Arabic Menu -->
<div class="lang-content" id="ar" dir="rtl">
  <h2 class="section-title">فطور</h2>
  <div class="menu">
    <div class="menu-card"> <img src="e.jpg" alt="Fried Eggs"><h3>هێلکەی کوڵاو</h3><div class="price">١٥٠٠ </div></div>
    <div class="menu-card"> <img src="3.jpg" alt="Fried Eggs"><h3>هێلکەی سورەوکراو</h3><div class="price">٢٠٠٠ </div></div>
    <div class="menu-card"> <img src="o.jpg" alt="Fried Eggs"><h3>ئۆملێت</h3><div class="price">٢٠٠٠ </div></div>
    <div class="menu-card"> <img src="m.jpg" alt="Fried Eggs"><h3>مەخلەمە</h3><div class="price">٣٠٠٠ </div></div>
    <div class="menu-card"> <img src="nisk.jpg" alt="Fried Eggs"><h3>Lentil soup </h3><div class="price">1000</div></div>
    <div class="menu-card"> <img src="kchese.jpg" alt="Fried Eggs"><h3>kurdish cheese</h3><div class="price">2000 </div></div>
    <div class="menu-card"> <img src="kiri.jpg" alt="Fried Eggs"><h3>kiri cheese</h3><div class="price">500</div></div>
    <div class="menu-card"> <img src="kraft.jpg" alt="Fried Eggs"><h3>kraft cheese</h3><div class="price">2000</div></div>
    <div class="menu-card"> <img src="ksy.jpg" alt="Fried Eggs"><h3>kurdish sweet yogurt</h3><div class="price">2000 </div></div>
    <div class="menu-card"> <img src="ksoy.jpg" alt="Fried Eggs"><h3>kurdish sour yogurt </h3><div class="price">2000 </div></div>
    <div class="menu-card"> <img src="kala.jpg" alt="Fried Eggs"><h3>factory yogurt</h3><div class="price">1000</div></div>
    <div class="menu-card"> <img src="mr.jpg" alt="Fried Eggs"><h3>jam</h3><div class="price">500</div></div>
    <div class="menu-card"> <img src="nut.jpg" alt="Fried Eggs"><h3>walnut</h3><div class="price">1000</div></div>
    <div class="menu-card"> <img src="rashi.jpg" alt="Fried Eggs"><h3>tahini and date syrup</h3><div class="price">1000 </div></div>
    <div class="menu-card"> <img src="olv.jpg" alt="Fried Eggs"><h3>olive </h3><div class="price">1000 </div></div>
    <div class="menu-card"> <img src="m.jpg" alt="Fried Eggs"><h3>breakfast meal</h3><div class="price">7000</div></div>
    <div class="menu-card"> <img src="toast.jpg" alt="Fried Eggs"><h3>cheese toast</h3><div class="price">1000</div></div>
    <div class="menu-card"> <img src="sand.jpg" alt="Fried Eggs"><h3>cheese sandwich</h3><div class="price">1000 </div></div>
   
  </div>





  <h2 class="section-title">Fast Foods</h2>
  <div class="menu">
    <div class="menu-card"> <img src="burger.jpg" alt="Fried Eggs"><h3>cheese beef burger</h3><div class="price">9000</div></div>
    <div class="menu-card"> <img src="burger.jpg" alt="Fried Eggs"><h3>beef burger</h3><div class="price">8000</div></div>
    <div class="menu-card"> <img src="burger.jpg" alt="Fried Eggs"><h3>cheese Chicken burger</h3><div class="price">8000</div></div>
    <div class="menu-card"> <img src="burger.jpg" alt="Fried Eggs"><h3>Chicken burger</h3><div class="price">8000</div></div>
    <div class="menu-card"> <img src="fngr.jpg" alt="Fried Eggs"><h3>fries</h3><div class="price">3000 </div></div>
    <div class="menu-card"> <img src="steak.jpg" alt="Fried Eggs"><h3>steak</h3><div class="price">10000 </div></div>
    <div class="menu-card"> <img src="fahita.jpg" alt="Fried Eggs"><h3>fahita</h3><div class="price">10000</div></div>
    <div class="menu-card"> <img src="kntaki.jpg" alt="Fried Eggs"><h3>kentucky</h3><div class="price">10000</div></div>
    <div class="menu-card"> <img src="crispy.jpg" alt="Fried Eggs"><h3>crispy</h3><div class="price">10000 </div></div>
    <div class="menu-card"> <img src="pizza.jpg" alt="Fried Eggs"><h3>mix pizza</h3><div class="price">8000 </div></div>
    <div class="menu-card"> <img src="fahita.jpg" alt="Fried Eggs"><h3>Chicken pizza</h3><div class="price">8000</div></div>
    <div class="menu-card"> <img src="burger.jpg" alt="Fried Eggs"><h3>beef pizza</h3><div class="price">8000</div></div>
    <div class="menu-card"> <img src="fngr.jpg" alt="Fried Eggs"><h3>margrita pizza</h3><div class="price">7000 </div></div>
    <div class="menu-card"> <img src="skalop.jpg" alt="Fried Eggs"><h3>Chicken Escalope</h3><div class="price">10000 </div></div>
    <div class="menu-card"> <img src="fahita.jpg" alt="Fried Eggs"><h3>alfredo pasta</h3><div class="price">10000</div></div>
    </div>
  
    <h2 class="section-title">drinks</h2>
    <div class="menu">
      <div class="menu-card"> <img src="es.jpg" alt="Fried Eggs"><h3>espresso</h3><div class="price">3000</div></div>
      <div class="menu-card"> <img src="amer.jpg" alt="Fried Eggs"><h3>americano</h3><div class="price">4000 </div></div>
      <div class="menu-card"> <img src="cap.jpg" alt="Fried Eggs"><h3>capuccino</h3><div class="price">5000 </div></div>
      <div class="menu-card"> <img src="latte.jpg" alt="Fried Eggs"><h3>latte</h3><div class="price">5000</div></div>
      <div class="menu-card"> <img src="double.jpg" alt="Fried Eggs"><h3>double espresso</h3><div class="price">5000 </div></div>
      <div class="menu-card"> <img src="nes.jpg" alt="Fried Eggs"><h3>nescafe</h3><div class="price">2000 </div></div>
      <div class="menu-card"> <img src="or.jpg" alt="Fried Eggs"><h3>orange juice</h3><div class="price">5000</div></div>
      <div class="menu-card"> <img src="apj.jpg" alt="Fried Eggs"><h3>apple juice</h3><div class="price">5000</div></div>
      <div class="menu-card"> <img src="lemon.jpg" alt="Fried Eggs"><h3>lemon juice</h3><div class="price">5000</div></div>
      <div class="menu-card"> <img src="carot.jpg" alt="Fried Eggs"><h3>carrot juice</h3><div class="price">5000</div></div>
      <div class="menu-card"> <img src="or.jpg" alt="Fried Eggs"><h3>cocktail juice</h3><div class="price">5000</div></div>
      <div class="menu-card"> <img src="tea.jpg" alt="Fried Eggs"><h3>tea</h3><div class="price">500</div></div>
      <div class="menu-card"> <img src="water.jpg" alt="Fried Eggs"><h3>water</h3><div class="price">500</div></div>
  
  
   
    </div>


  <h2 class="section-title">sweets</h2>
  <div class="menu">
    <div class="menu-card"> <img src="cake.jpg" alt="Fried Eggs"><h3>cake</h3><div class="price">3000</div></div>
    <div class="menu-card"> <img src="tralicha.jpg" alt="Fried Eggs"><h3>tres laches cake</h3><div class="price">3000 </div></div>
    <div class="menu-card"> <img src="crwason.jpg" alt="Fried Eggs"><h3>Croissant</h3><div class="price">3000 </div></div>
    <div class="menu-card"> <img src="cinama.jpg" alt="Fried Eggs"><h3>Cinnamon Roll
    </h3><div class="price">3500</div></div>
    <div class="menu-card"> <img src="sans.jpg" alt="Fried Eggs"><h3>san sebastian cake</h3><div class="price">6000</div></div>
    <div class="menu-card"> <img src="kwlicha.jpg" alt="Fried Eggs"><h3>kliecha</h3><div class="price">2500 </div></div>
    <div class="menu-card"> <img src="shaklama.jpg" alt="Fried Eggs"><h3>shakrlama</h3><div class="price">2500 </div></div>
    <div class="menu-card"> <img src="mahalabi.jpg" alt="Fried Eggs"><h3>mahalabia</h3><div class="price">2000</div></div>
    <div class="menu-card"> <img src="cupc.jpg" alt="Fried Eggs"><h3>cup cake</h3><div class="price">3000 </div></div>
    </div>
  </div>

</div>

<footer>
  <p>&copy; 2025 FMC CAFE. All rights reserved.</p>
  <p>📞 1048</p>
</footer>

</body>
</html>
