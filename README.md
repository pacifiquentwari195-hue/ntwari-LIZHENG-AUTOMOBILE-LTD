
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>LIZHENG | Premium Car Dealership Rwanda</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;800&display=swap" rel="stylesheet">

<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
   .wallpaper {
      height: 370vh;
      background-image: url("https://hips.hearstapps.com/hmg-prod/images/future-cars-2-6939c3d6c9abe.jpg?crop=0.6989379084967321xw:1xh;center,top&resize=1200:*");
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
    }
  body {
    font-family: "Poppins", sans-serif;
    background: #fafafa;
    color: #222;
    overflow-x: hidden;
  }
  
  header {
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    padding: 15px 8%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: rgba(255,255,255,0.85);
    backdrop-filter: blur(10px);
    box-shadow: 0 0 0 transparent;
    transition: 0.3s;
    z-index: 1000;
  }
  header.scrolled {
    box-shadow: 0 3px 15px rgba(0,0,0,0.1);
  }

  .logo {
    font-size: 1.7rem;
    font-weight: 800;
    color: #e50914;
  }
  .logo span {
    color: #222;
    font-weight: 700;
  }

  nav ul {
    display: flex;
    list-style: none;
    gap: 1.8rem;
  }

  nav ul li a {
    color: #222;
    text-decoration: none;
    font-weight: 600;
    transition: 0.3s;
  }
  nav ul li a:hover {
    color: #e50914;
  }
  .menu-icon {
    display: none;
    font-size: 28px;
    cursor: pointer;
  }

  @media (max-width: 850px) {
    nav ul {
      position: absolute;
      top: 100%;
      right: 0;
      background: #fff;
      width: 100%;
      flex-direction: column;
      text-align: center;
      padding: 20px 0;
      max-height: 0;
      overflow: hidden;
      transition: 0.4s ease;
    }
    nav ul.open {
      max-height: 300px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }
    .menu-icon { display: block; }
  }
  .hero {
    height: 100vh;
    background: 
      linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.7)),
      url('https://images.unsplash.com/photo-1503376780353-7e6692767b70?auto=format&fit=crop&w=2000&q=80') 
      center/cover no-repeat;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 10px;
  }

  .hero h1 {
    font-size: 3rem;
    color: white;
    font-weight: 800;
    margin-bottom: 1rem;
    animation: fadeInDown 1.2s ease;
  }
  .hero p {
    color: #ddd;
    font-size: 1.2rem;
    max-width: 600px;
    margin: auto;
    margin-bottom: 2rem;
    animation: fadeIn 2s ease;
  }

  .btn {
    display: inline-block;
    padding: 0.9rem 2rem;
    background: #e50914;
    color: white;
    font-weight: 700;
    border-radius: 6px;
    text-decoration: none;
    transition: 0.3s;
    animation: fadeInUp 1.2s ease;
  }
  .btn:hover {
    background: #b00610;
  }
  .cars-section {
    padding: 6rem 10%;
    text-align: center;
  }
  .cars-section h2 {
    font-size: 2.4rem;
    font-weight: 800;
    margin-bottom: 2rem;
  }

  .car-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 2rem;
  }

  .car-card {
    background: white;
    border-radius: 14px;
    overflow: hidden;
    box-shadow: 0 8px 18px rgba(0,0,0,0.08);
    transition: 0.3s ease;
  }
  .car-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 12px 22px rgba(0,0,0,0.15);
  }
  .car-card img {
    width: 100%;
    height: 190px;
    object-fit: cover;
    transition: 0.3s;
  }
  .car-card:hover img {
    transform: scale(1.07);
  }
  .car-card h3 {
    margin: 1rem 0 0.3rem;
    font-size: 1.1rem;
    font-weight: 700;
  }
  .car-card p {
    font-weight: 700;
    color: #e50914;
    margin-bottom: 1.2rem;
  }
  .about {
    padding: 5rem 10%;
    background: #fff;
    text-align: center;
  }
  .about h2 { font-size: 2.2rem; font-weight: 800; }
  .about p {
    max-width: 600px;
    margin: auto;
    margin-top: 1rem;
    font-size: 1.1rem;
  }
  .contact {
    padding: 5rem 10%;
    text-align: center;
  }
  .contact-form {
    max-width: 600px;
    margin: auto;
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
  .contact-form input,
  .contact-form textarea {
    padding: 0.9rem;
    border-radius: 6px;
    border: 1.6px solid #ccc;
    font-size: 1rem;
    transition: 0.3s;
  }
  .contact-form input:focus,
  .contact-form textarea:focus {
    border-color: #e50914;
  }
  footer {
    background: #111;
    color: white;
    text-align: center;
    padding: 1.5rem;
    margin-top: 3rem;
    font-weight: 500;
  }
  .whatsapp {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background: #25D366;
    padding: 15px;
    border-radius: 50%;
    font-size: 25px;
    color: white;
    text-align: center;
    cursor: pointer;
    box-shadow: 0 3px 10px rgba(0,0,0,0.2);
    transition: 0.3s;
    z-index: 999;
  }
  .whatsapp:hover { transform: scale(1.1); }
  @keyframes fadeInDown { from {opacity: 0; transform: translateY(-30px);} to {opacity:1; transform: none;} }
  @keyframes fadeInUp { from {opacity: 0; transform: translateY(30px);} to {opacity:1; transform: none;} }
  @keyframes fadeIn { from {opacity: 0;} to {opacity: 1;} }

</style>
</head>

<body>

<header id="header">
  <div class="logo">LIZHENG <span>Automobile Ltd</span></div>

  <div class="menu-icon" onclick="toggleMenu()">☰</div>

  <nav>
    <ul id="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#cars">Inventory</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>
<section class="hero" id="home">
  <div>
    <h1>Drive the Car You Deserve</h1>
    <p>Discover our premium range of modern electric vehicles at unbeatable prices in Rwanda.</p>
    <a href="#cars" class="btn">View Inventory</a>
  </div>
</section>
<section class="cars-section" id="cars">
  <h2>Featured Cars</h2>

  <div class="car-grid">
    <div class="car-card">
      <img src="https://image.made-in-china.com/2f0j00CVvqkazBljoy/2023-Auto-GAC-Aion-V-Plus-2022-Evolution-Edition-New-Energy-Vehicle-High-Speed-185km-H-EV-Electric-Car-Long-Distance-500km.webp">
      <h3>AION V PLUS</h3>
      <p>30,000,000 RWF</p>
    </div>
    <div class="car-card">
      <img src="https://static-content-live.caricarz.com/media_library/post/17281/15167284/conversions/11-full_normal.jpg">
      <h3>2025 TOYOTA BZ3X</h3>
      <p>43,000,000 RWF</p>
    </div>
    <div class="car-card">
      <img src="https://i1.autocango.com/spec/fb47f590193b49c5a663adc75c821da2f486b47ff3ea63dbbfd2e166389eaca7.webp?x-image-process=image/resize,h_900/imageslim">
      <h3>2024 BYD Song Plus</h3>
      <p>39,000,000 RWF</p>
    </div>
    <div class="car-card">
      <img src="https://guangcaiauto.com/wp-content/uploads/2024/08/Chery-iCAR-03-picture-10.webp">
      <h3>Chery iCAR 03</h3>
      <p>32,000,000 RWF</p>
    </div>
    <div class="car-card">
      <img src="https://www.nordiskbil.com/wp-content/uploads/2023/12/BYD-Yuan-UP.jpg">
      <h3>2025 BYD YUAN UP</h3>
      <p>30,000,000 RWF</p>
    </div>
    <div class="car-card">
      <img src="https://br-www-resouce-cdn.gacgroup.com/static/Global/tenant/cms/common/202503/e31a84f7-c224-458a-bd8a-8155e6b88472.jpg">
      <h3>2022 AION Y</h3>
      <p>28,000,000 RWF</p>
    </div>

    <div class="car-card">
      <img src="https://s.auto.drom.ru/i24278/c/photos/fullsize/gac/trumpchi_gs4/gac_trumpchi_gs4_1117659.jpg">
      <h3>2019 TRUMPCHI GS4</h3>
      <p>28,000,000 RWF</p>
    </div>
    <div class="car-card">
      <img src="https://cdn.wheel-size.com/automobile/body/gac-trumpchi-ge3-2017-2018-1596714361.0886333.jpeg">
      <h3>2018 TRUMPCHI GE3</h3>
      <p>21,000,000 RWF</p>
    </div>
    <div class="car-card">
      <img src="https://carnewschina.com/wp-content/uploads/2024/12/2-transformed-10-scaled.jpeg">
      <h3>2025 Chery iCAR V23</h3>
      <p>38,000,000 RWF</p>
    </div>
    <div class="car-card">
      <img src="https://auto.qingdaonews.com/ev/images/2022-09/29/9d31af10-300b-4e37-b7c2-988b756bab53.jpg.2">
      <h3>2022 AION Y PLUS</h3>
      <p>28,500,000 RWF</p>
    </div>

    <div class="car-card">
      <img src="https://www.gacmotor.mx/static/agency-go-virtual/Gac/Emkoo/2024/emkoo-2.jpg">
      <h3>GAC Emkoo Hybrid</h3>
      <p>39,000,000 RWF</p>
    </div>

    <div class="car-card">
      <img src="https://carnewschina.com/wp-content/uploads/2022/04/aeolus-suv-1.jpg">
      <h3>2022 DONG FENG</h3>
      <p>40,000,000 RWF</p>
    </div>
 <div class="car-card">
      <img src="https://api-core.multimotors.by/storage/media/2025/03/05/d171b3e3ce632f6365f7122728f9a53bb2b48468.png">
      <h3>2025 BYD YUAN PLUS</h3>
      <p>36,000,000 RWF</p>
    </div>
     <div class="car-card">
      <img src="https://dolubatarya.com/uploads/2023/01/byd-yangwang-u8-performance.jpg">
      <h3>2024 BYD Yang Wang U8</h3>
      <p>70,000,000 RWF</p>
    </div>
     <div class="car-card">
      <img src="https://carsguide-res.cloudinary.com/image/upload/c_fit,h_810,w_1215,f_auto,t_cg_base/v1/editorial/inline-images/2026-BYD-Sealion-8-SUV-silver-1470x790p-1.jpg">
      <h3>2025 BYD SEALION 8 Plug-in Hybrid</h3>
      <p>58,000,000 RWF</p>
    </div>
  </div>
</section>
<section class="about" id="about">
  <h2>About LIZHENG Automobile Ltd</h2>
  <p>
    We pride ourselves on delivering high-quality electric vehicles with exceptional customer service.
    <br><br><strong>Location:</strong> Kigali - Kicukiro, KK 506 Street <br> or find us on google Maps LIZHENG AUTOMOBILE LTD 

  </p>
</section>
<section class="contact" id="contact">
  <h2>Contact Us</h2>
  <p>
    Phone: +250 781 845 376<br>
    Phone: +250 783 086 346<br>
    Phone: +250 793 368 695<br>
    Phone: +250 796 892 093<br>
    Email: pacifiquentwari195@gmail.com<br>
    Email: karengerafidele9@gmail.com
  </p>

  <h2 style="margin-top:2rem;">Send us a message</h2>

  <form class="contact-form">
    <input type="text" placeholder="Full Name" required>
    <input type="email" placeholder="Email Address" required>
    <textarea placeholder="Your Message" rows="5" required></textarea>
    <button type="submit" class="btn">Send Message</button>
  </form>
</section>

<footer>
  © 2025 LIZHENG Automobile Ltd. All Rights Reserved.
</footer>
<a href="https://wa.me/250796892093" target="_blank" class="whatsapp">💬 Text us</a>
<script>
  function toggleMenu() {
    document.getElementById("nav-links").classList.toggle("open");
  }

  // Header shadow on scroll
  window.addEventListener("scroll", function() {
    document.getElementById("header").classList.toggle("scrolled", window.scrollY > 20);
  });
</script>

</body>
</html>
