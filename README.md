<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>LIZHENG | Premium Car Dealership</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Poppins', sans-serif;
      color: #222;
      background-color: #fcfbfb;
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* ---------- HEADER ---------- */
    header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: rgba(235, 222, 222, 0.95);
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 5%;
      z-index: 10;
    }

    .logo {
      font-size: 1.6rem;
      font-weight: 700;
      color: #111;
    }

    .logo span {
      color: #fbf7f7;
    }

    .nav-links {
      list-style: none;
      display: flex;
      gap: 2rem;
    }

    .nav-links a {
      text-decoration: none;
      color: #333;
      font-weight: 500;
      transition: 0.3s;
    }

    .nav-links a:hover {
      color: #e50914;
    }

    .hero {
      height: 100vh;
      background: url('https://images.unsplash.com/photo-1503376780353-7e6692767b70?auto=format&fit=crop&w=1920&q=80') center/cover no-repeat;
      display: flex;
      justify-content: center;
      align-items: center;
      color: #fff;
      text-align: center;
      position: relative;
    }

    .hero::after {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.5);
    }

    .hero-content {
      position: relative;
      z-index: 1;
      max-width: 600px;
    }

    .hero h1 {
      font-size: 3rem;
      margin-bottom: 1rem;
      animation: fadeInDown 1s ease;
    }

    .hero p {
      font-size: 1.1rem;
      margin-bottom: 2rem;
      animation: fadeIn 2s ease;
    }

    .btn {
      display: inline-block;
      padding: 0.75rem 1.5rem;
      background: #e50914;
      color: #fff;
      text-decoration: none;
      border-radius: 4px;
      transition: 0.3s;
      font-weight: 600;
      animation: fadeInUp 1.5s ease;
    }

    .btn:hover {
      background: #b0060f;
    }

    /* ---------- FEATURED CARS ---------- */
    .cars-section {
      padding: 5rem 10%;
      text-align: center;
    }

    .cars-section h2 {
      font-size: 2rem;
      margin-bottom: 2rem;
    }

    .car-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
    }

    .car-card {
      background: #f9f9f9;
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      transition: transform 0.3s;
    }

    .car-card:hover {
      transform: translateY(-5px);
    }

    .car-card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }

    .car-card h3 {
      margin: 1rem 0 0.5rem;
    }

    .car-card p {
      color: #e50914;
      font-weight: 600;
      margin-bottom: 1rem;
    }

    /* ---------- ABOUT ---------- */
    .about {
      background: #ebe9e9;
      padding: 5rem 10%;
      text-align: center;
    }

    .about-content {
      max-width: 700px;
      margin: auto;
    }

    .about h2 {
      margin-bottom: 1rem;
    }

    /* ---------- CONTACT ---------- */
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
      padding: 1rem;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-size: 1rem;
    }

    .contact-form button {
      border: none;
      cursor: pointer;
    }

    /* ---------- FOOTER ---------- */
    footer {
      background: #111;
      color: #fff;
      text-align: center;
      padding: 1.5rem 0;
    }

    /* ---------- ANIMATIONS ---------- */
    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }

    @keyframes fadeInUp {
      from {opacity: 0; transform: translateY(20px);}
      to {opacity: 1; transform: translateY(0);}
    }

    @keyframes fadeInDown {
      from {opacity: 0; transform: translateY(-20px);}
      to {opacity: 1; transform: translateY(0);}
    }

    /* ---------- RESPONSIVE ---------- */
    @media (max-width: 768px) {
      .hero h1 {
        font-size: 2.2rem;
      }
      .nav-links {
        gap: 1rem;
      }
    }
  </style>
</head>

<body>
  <header>
    <div class="logo">LIZHENG<span>Automobile ltd-Rwanda </span></div>
    <nav>
      <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#cars">Inventory</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>
  <section class="hero" id="home">
    <div class="hero-content">
      <h1>Drive the Car You Deserve</h1>
      <p>Explore our premium collection of new and pre-owned vehicles at unbeatable prices at LIZHENG Automobile.</p>
      <a href="#cars" class="btn">View Inventory</a>
    </div>
  </section>

  <!-- FEATURED CARS -->
  <section class="cars-section" id="cars">
    <h2>Featured Cars</h2>
    <div class="car-grid">
      <div class="car-card">
        <img src="https://cdn.globalso.com/centuryautomobile/AION-LX-zhu_3.jpg" alt="Audi R8">
        <h3>AION V PLUS</h3>
        <p>$17,500</p>
      </div>
      <div class="car-card">
        <img src="https://static-content-live.caricarz.com/media_library/post/17281/15167284/conversions/11-full_normal.jpg" alt="BMW M4">
        <h3>2025 TOYOTA BZ3X</h3>
        <p>$28,000</p>
      </div>
      <div class="car-card">
        <img src="https://i1.autocango.com/spec/fb47f590193b49c5a663adc75c821da2f486b47ff3ea63dbbfd2e166389eaca7.webp?x-image-process=image/resize,h_900/imageslim" alt="Mercedes AMG GT">
        <h3>2024 BYD song plus</h3>
        <p>$22,000</p>
      </div>
      <div class="car-card">
        <img src="https://guangcaiauto.com/wp-content/uploads/2024/08/Chery-iCAR-03-picture-10.webp" alt="Mercedes AMG GT">
        <h3>Chery iCAR 03</h3>
        <p>$21,000</p>
      </div>
       <div class="car-card">
        <img src="https://image.made-in-china.com/2f0j00LmVbaIEsCKkP/2024-Byd-Yuan-up-New-Energy-Vehicles-New-Sedan-SUV-Cars-Left-Drive-Cheap-Price-High-Speed-Fwd-Long-Range-401km-301km-Auto-EV-Second-Hand-Vehicle-for-Sale-China.webp" alt="Mercedes AMG GT">
        <h3>2025 BYD YUAN UP</h3>
        <p>$21,500</p>
      </div>
       <div class="car-card">
        <img src="https://br-www-resouce-cdn.gacgroup.com/static/Global/tenant/cms/common/202503/e31a84f7-c224-458a-bd8a-8155e6b88472.jpg" alt="Mercedes AMG GT">
        <h3>2025 AION Y</h3>
        <p>$18,500</p>
      </div>
       <div class="car-card">
        <img src="https://s.auto.drom.ru/i24278/c/photos/fullsize/gac/trumpchi_gs4/gac_trumpchi_gs4_1117659.jpg" alt="Mercedes AMG GT" sizes="2">
        <h3>2019 TRUMPSHI GS4</h3>
        <p>$16,500</p>
      </div>
       <div class="car-card">
        <img src="https://cdn.wheel-size.com/automobile/body/gac-trumpchi-ge3-2017-2018-1596714361.0886333.jpeg" alt="Mercedes AMG GT" sizes="2">
        <h3>2018 TRUMPSHI GE3</h3>
        <p>$16,000</p>
      </div>
      <div class="car-card">
        <img src="https://carnewschina.com/wp-content/uploads/2024/12/2-transformed-10-scaled.jpeg" alt="Mercedes AMG GT" sizes="2">
        <h3>2025 Chery iCAR V23</h3>
        <p>$21,000</p>
      </div>
      <div class="car-card">
        <img src="https://img.pcauto.com/model/images/modelPic/my/2024/09/691/447808378_1726299535534_600x400.jpg" alt="Mercedes AMG GT" sizes="2">
        <h3>2022 AION Y</h3>
        <p>$17,500</p>
      </div>
      <div class="car-card">
        <img src="https://www.gacmotor.mx/static/agency-go-virtual/Gac/Emkoo/2024/emkoo-2.jpg" alt="Mercedes AMG GT" sizes="2">
        <h3>GAC Emkoo Hybrid</h3>
        <p>$18,000</p>
      </div>
      <div class="car-card">
        <img src="https://carnewschina.com/wp-content/uploads/2022/04/aeolus-suv-1.jpg" alt="Mercedes AMG GT" sizes="2">
        <h3>2022 DONG FENG</h3>
        <p>$23,000</p>
      </div>
    </div>
  </section>
  <section class="about" id="about">
    <div class="about-content">
      <h2>About LIZHENG Automobile ltd</h2>
      <p>At LIZHENG Automobile ltd, we pride ourselves on delivering top-quality vehicles paired with unmatched customer service. Our mission is to help you find the perfect electric car that fits your lifestyle, budget, and performance needs. <br><strong><u>Location</u> <br>Here in Kigali-Kicukiro <br>KK 506 st</strong> </p>
    </div>
  </section>
  <section class="contact" id="contact">
    <h2><u>Contact Us</u>  <br> </h2>Phone :+250 781 845 376<br>Email: pacifiquentwari195@gmail.com
    <h2><u> send us a message</u></h2>
    <form class="contact-form">
      <input type="text" placeholder="Full Name" required>
      <input type="email" placeholder="Email Address" required>
      <textarea placeholder="Your Message" rows="5" required></textarea>
      <button type="submit" class="btn">Send Message</button>
    </form>
  </section>
  <footer>
    <p>© 2025 LIZHENG Automobile ltd. All Rights Reserved.</p>
  </footer>
</body>
</html>
