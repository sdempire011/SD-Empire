"index.html"

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Affiliate Academy</title>

  <style>
    *{margin:0;padding:0;box-sizing:border-box}
    body{font-family:Arial,sans-serif;color:#18202a;background:#fff}
    a{text-decoration:none;color:inherit}
    .container{width:90%;max-width:1200px;margin:auto}

    header{
      background:#fff;
      border-bottom:1px solid #eee;
      position:sticky;
      top:0;
      z-index:1000;
    }

    .nav{
      height:75px;
      display:flex;
      align-items:center;
      justify-content:space-between;
    }

    .logo{
      font-size:25px;
      font-weight:800;
    }

    .logo span{color:#ff6b35}

    .nav-links{
      display:flex;
      gap:28px;
      align-items:center;
      list-style:none;
    }

    .nav-links a:hover{color:#ff6b35}

    .login{
      border:1px solid #ff6b35;
      padding:11px 20px;
      border-radius:6px;
      color:#ff6b35;
    }

    .hero{
      padding:90px 0;
      background:linear-gradient(120deg,#fff7f2,#f7f9ff);
    }

    .hero-grid{
      display:grid;
      grid-template-columns:1.1fr .9fr;
      gap:50px;
      align-items:center;
    }

    .tag{
      color:#ff6b35;
      font-weight:bold;
      margin-bottom:15px;
    }

    h1{
      font-size:54px;
      line-height:1.08;
      margin-bottom:22px;
    }

    .hero p{
      font-size:18px;
      line-height:1.7;
      color:#667085;
      margin-bottom:30px;
    }

    .btn{
      display:inline-block;
      background:#ff6b35;
      color:white;
      padding:15px 28px;
      border-radius:7px;
      font-weight:bold;
      border:0;
      cursor:pointer;
    }

    .hero-card{
      background:#fff;
      padding:25px;
      border-radius:18px;
      box-shadow:0 15px 45px #00000012;
    }

    .course-image{
      height:270px;
      border-radius:12px;
      background:linear-gradient(135deg,#ff6b35,#ffb347);
      display:flex;
      align-items:center;
      justify-content:center;
      color:#fff;
      font-size:32px;
      font-weight:bold;
    }

    section{padding:75px 0}

    .section-title{text-align:center;margin-bottom:45px}

    .section-title h2{
      font-size:38px;
      margin-bottom:10px;
    }

    .section-title p{color:#667085}

    .courses{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:25px;
    }

    .course{
      border:1px solid #eee;
      border-radius:12px;
      overflow:hidden;
      background:white;
      transition:.25s;
    }

    .course:hover{
      transform:translateY(-5px);
      box-shadow:0 15px 35px #00000010;
    }

    .course-top{
      height:170px;
      background:#f1f5f9;
      display:flex;
      align-items:center;
      justify-content:center;
      font-size:24px;
      font-weight:bold;
    }

    .course-body{padding:22px}

    .course-body h3{margin-bottom:10px}

    .course-body p{
      color:#667085;
      line-height:1.6;
      margin-bottom:18px;
    }

    .price{
      font-size:25px;
      font-weight:bold;
      margin-bottom:18px;
    }

    .old{
      font-size:15px;
      color:#999;
      text-decoration:line-through;
      margin-right:8px;
    }

    .packages{
      background:#f8fafc;
    }

    .package-grid{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:25px;
    }

    .package{
      background:#fff;
      padding:30px;
      border-radius:15px;
      border:1px solid #eee;
      text-align:center;
    }

    .package h3{font-size:24px;margin-bottom:15px}

    .package .big-price{
      font-size:32px;
      font-weight:bold;
      margin:20px 0;
    }

    .features{
      list-style:none;
      line-height:2;
      color:#667085;
      margin-bottom:20px;
    }

    .about-grid{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:50px;
      align-items:center;
    }

    .about-box{
      background:#fff7f2;
      padding:40px;
      border-radius:18px;
    }

    .about-box h2{
      font-size:38px;
      margin-bottom:20px;
    }

    .about-box p{
      color:#667085;
      line-height:1.8;
    }

    .stats{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:20px;
      margin-top:30px;
    }

    .stat{
      text-align:center;
      padding:25px;
      border:1px solid #eee;
      border-radius:10px;
    }

    .stat strong{
      display:block;
      font-size:30px;
      color:#ff6b35;
    }

    .instructors{
      display:grid;
      grid-template-columns:repeat(4,1fr);
      gap:20px;
    }

    .instructor{
      text-align:center;
      padding:25px;
      border:1px solid #eee;
      border-radius:12px;
    }

    .avatar{
      width:100px;
      height:100px;
      margin:0 auto 15px;
      border-radius:50%;
      background:#e2e8f0;
      display:flex;
      align-items:center;
      justify-content:center;
      font-size:30px;
    }

    .instructor p{color:#667085;margin-top:7px}

    .faq{
      max-width:850px;
      margin:auto;
    }

    details{
      border-bottom:1px solid #ddd;
      padding:20px 5px;
    }

    summary{
      cursor:pointer;
      font-weight:bold;
      font-size:17px;
    }

    details p{
      color:#667085;
      line-height:1.7;
      padding-top:15px;
    }

    .journey{
      background:#18202a;
      color:white;
    }

    .journey .section-title p{color:#cbd5e1}

    .journey-grid{
      display:grid;
      grid-template-columns:repeat(4,1fr);
      gap:20px;
    }

    .journey-card{
      padding:25px;
      border:1px solid #ffffff22;
      border-radius:12px;
    }

    .journey-card span{
      color:#ff9b73;
      font-size:28px;
      font-weight:bold;
    }

    .newsletter{
      text-align:center;
      background:#fff7f2;
    }

    .newsletter form{
      display:flex;
      max-width:550px;
      margin:25px auto 0;
    }

    .newsletter input{
      flex:1;
      padding:15px;
      border:1px solid #ddd;
      border-radius:6px 0 0 6px;
    }

    .newsletter button{
      border-radius:0 6px 6px 0;
    }

    footer{
      background:#10151c;
      color:white;
      padding:55px 0 25px;
    }

    .footer-grid{
      display:grid;
      grid-template-columns:2fr 1fr 1fr;
      gap:40px;
    }

    footer p{
      color:#aab2bd;
      line-height:1.7;
      margin-top:15px;
    }

    footer ul{
      list-style:none;
      line-height:2;
      color:#aab2bd;
    }

    .copyright{
      text-align:center;
      border-top:1px solid #ffffff15;
      margin-top:40px;
      padding-top:20px;
      color:#8c96a3;
    }

    /* CHECKOUT MODAL */

    .modal{
      display:none;
      position:fixed;
      inset:0;
      background:#00000088;
      z-index:2000;
      align-items:center;
      justify-content:center;
      padding:20px;
    }

    .modal-box{
      background:white;
      width:100%;
      max-width:480px;
      padding:30px;
      border-radius:15px;
      text-align:center;
      position:relative;
    }

    .close{
      position:absolute;
      right:20px;
      top:15px;
      font-size:25px;
      cursor:pointer;
    }

    .qr{
      width:230px;
      height:230px;
      object-fit:contain;
      margin:20px auto;
      display:block;
      border:1px solid #ddd;
    }

    .modal input{
      width:100%;
      padding:13px;
      margin:7px 0;
      border:1px solid #ddd;
      border-radius:6px;
    }

    @media(max-width:850px){
      .nav-links{display:none}
      .hero-grid,
      .about-grid{grid-template-columns:1fr}
      h1{font-size:40px}
      .courses,
      .package-grid{grid-template-columns:1fr}
      .instructors{grid-template-columns:repeat(2,1fr)}
      .journey-grid{grid-template-columns:1fr 1fr}
      .footer-grid{grid-template-columns:1fr}
    }

    @media(max-width:500px){
      .instructors,
      .journey-grid{grid-template-columns:1fr}
      .newsletter form{display:block}
      .newsletter input,
      .newsletter button{
        width:100%;
        border-radius:6px;
        margin:4px 0;
      }
    }
  </style>
</head>

<body>

<header>
  <div class="container nav">

    <div class="logo">
      Affiliate<span>Academy</span>
    </div>

    <ul class="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#courses">Courses</a></li>
      <li><a href="#packages">Packages</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#faq">FAQ</a></li>
    </ul>

    <a href="#login" class="login">Login / Sign Up</a>

  </div>
</header>


<!-- HERO -->

<section class="hero" id="home">
  <div class="container hero-grid">

    <div>
      <div class="tag">LEARN • BUILD • GROW</div>

      <h1>
        Master Affiliate Marketing
        & Build Your Online Business
      </h1>

      <p>
        Learn affiliate marketing step-by-step with practical lessons,
        strategies and real-world examples.
      </p>

      <button class="btn" onclick="openCheckout()">
        Enroll Now — ₹599
      </button>
    </div>

    <div class="hero-card">
      <div class="course-image">
        AFFILIATE<br>MARKETING
      </div>
    </div>

  </div>
</section>


<!-- COURSES -->

<section id="courses">
  <div class="container">

    <div class="section-title">
      <h2>Trending Courses</h2>
      <p>Learn practical skills from beginner to advanced.</p>
    </div>

    <div class="courses">

      <div class="course">
        <div class="course-top">Affiliate</div>

        <div class="course-body">
          <h3>Affiliate Marketing Mastery</h3>
          <p>
            Complete beginner-to-advanced affiliate marketing course.
          </p>

          <div class="price">
            <span class="old">₹1,999</span> ₹599
          </div>

          <button class="btn" onclick="openCheckout()">
            Buy Now
          </button>
        </div>
      </div>


      <div class="course">
        <div class="course-top">Social Media</div>

        <div class="course-body">
          <h3>Social Media Marketing</h3>
          <p>
            Learn content strategy and audience growth fundamentals.
          </p>

          <div class="price">Coming Soon</div>

          <button class="btn">View Course</button>
        </div>
      </div>


      <div class="course">
        <div class="course-top">Content</div>

        <div class="course-body">
          <h3>Content Creation</h3>
          <p>
            Learn how to plan and create engaging digital content.
          </p>

          <div class="price">Coming Soon</div>

          <button class="btn">View Course</button>
        </div>
      </div>

    </div>
  </div>
</section>


<!-- PACKAGES -->

<section class="packages" id="packages">

  <div class="container">

    <div class="section-title">
      <h2>Our Learning Packages</h2>
      <p>Choose the package that suits your learning journey.</p>
    </div>

    <div class="package-grid">

      <div class="package">
        <h3>Starter</h3>
        <div class="big-price">₹599</div>

        <ul class="features">
          <li>Affiliate Marketing</li>
          <li>Beginner Lessons</li>
          <li>Recorded Videos</li>
          <li>Lifetime Access</li>
        </ul>

        <button class="btn" onclick="openCheckout()">
          Enroll Now
        </button>
      </div>


      <div class="package">
        <h3>Creator</h3>
        <div class="big-price">₹1,499</div>

        <ul class="features">
          <li>Affiliate Marketing</li>
          <li>Content Creation</li>
          <li>Social Media</li>
          <li>Advanced Lessons</li>
        </ul>

        <button class="btn">
          Coming Soon
        </button>
      </div>


      <div class="package">
        <h3>Pro</h3>
        <div class="big-price">₹2,999</div>

        <ul class="features">
          <li>All Courses</li>
          <li>Advanced Training</li>
          <li>Projects</li>
          <li>Bonus Lessons</li>
        </ul>

        <button class="btn">
          Coming Soon
        </button>
      </div>

    </div>
  </div>

</section>


<!-- ABOUT -->

<section id="about">

  <div class="container about-grid">

    <div class="about-box">
      <h2>Learn Skills That Matter</h2>

      <p>
        Affiliate Academy is designed to make online learning simple,
        practical and accessible. Start from the basics and gradually
        build the skills required for digital marketing and affiliate
        business.
      </p>

      <br>

      <button class="btn" onclick="openCheckout()">
        Start Learning
      </button>
    </div>

    <div>

      <div class="stats">

        <div class="stat">
          <strong>1+</strong>
          Course
        </div>

        <div class="stat">
          <strong>10+</strong>
          Modules
        </div>

        <div class="stat">
          <strong>24/7</strong>
          Access
        </div>

      </div>

    </div>

  </div>

</section>


<!-- INSTRUCTORS -->

<section>

  <div class="container">

    <div class="section-title">
      <h2>Meet Our Instructor</h2>
      <p>Learn from practical, easy-to-understand lessons.</p>
    </div>

    <div class="instructors">

      <div class="instructor">
        <div class="avatar">A</div>
        <h3>Your Name</h3>
        <p>Affiliate Marketing</p>
      </div>

      <div class="instructor">
        <div class="avatar">D</div>
        <h3>Digital Expert</h3>
        <p>Digital Marketing</p>
      </div>

      <div class="instructor">
        <div class="avatar">C</div>
        <h3>Content Expert</h3>
        <p>Content Creation</p>
      </div>

      <div class="instructor">
        <div class="avatar">S</div>
        <h3>Sales Expert</h3>
        <p>Sales Strategy</p>
      </div>

    </div>

  </div>

</section>


<!-- FAQ -->

<section id="faq">

  <div class="container">

    <div class="section-title">
      <h2>Frequently Asked Questions</h2>
      <p>Everything you need to know.</p>
    </div>

    <div class="faq">

      <details>
        <summary>What is Affiliate Marketing?</summary>
        <p>
          Affiliate marketing is a performance-based model where
          commissions can be earned by promoting products or services
          through affiliate links.
        </p>
      </details>

      <details>
        <summary>Who can join this course?</summary>
        <p>
          Beginners and learners interested in understanding affiliate
          marketing can join.
        </p>
      </details>

      <details>
        <summary>How do I get course access?</summary>
        <p>
          After your payment is verified, your course access can be
          activated by the administrator.
        </p>
      </details>

      <details>
        <summary>How do I pay?</summary>
        <p>
          Payment can be made using the UPI QR code shown during checkout.
        </p>
      </details>

      <details>
        <summary>Is the course lifetime access?</summary>
        <p>
          You can configure the course access period according to your
          own policy.
        </p>
      </details>

    </div>

  </div>

</section>


<!-- JOURNEY -->

<section class="journey">

  <div class="container">

    <div class="section-title">
      <h2>Start Your Learning Journey</h2>
      <p>Follow a simple path from learning to implementation.</p>
    </div>

    <div class="journey-grid">

      <div class="journey-card">
        <span>01</span>
        <h3>Learn</h3>
        <p>Understand the fundamentals.</p>
      </div>

      <div class="journey-card">
        <span>02</span>
        <h3>Practice</h3>
        <p>Apply what you learn.</p>
      </div>

      <div class="journey-card">
        <span>03</span>
        <h3>Build</h3>
        <p>Create your affiliate system.</p>
      </div>

      <div class="journey-card">
        <span>04</span>
        <h3>Grow</h3>
        <p>Keep improving your skills.</p>
      </div>

    </div>

  </div>

</section>


<!-- NEWSLETTER -->

<section class="newsletter">

  <div class="container">

    <div class="section-title">
      <h2>Stay Updated</h2>
      <p>Get new course announcements and learning updates.</p>
    </div>

    <form onsubmit="subscribe(event)">
      <input type="email" placeholder="Enter your email" required>
      <button class="btn">Subscribe</button>
    </form>

  </div>

</section>


<!-- FOOTER -->

<footer>

  <div class="container footer-grid">

    <div>
      <div class="logo">
        Affiliate<span>Academy</span>
      </div>

      <p>
        Practical online learning for digital skills and affiliate
        marketing.
      </p>
    </div>

    <div>
      <h3>Useful Links</h3>
      <ul>
        <li>Home</li>
        <li>Courses</li>
        <li>About</li>
        <li>FAQ</li>
      </ul>
    </div>

    <div>
      <h3>Contact</h3>
      <p>
        support@example.com
      </p>
      <p>
        India
      </p>
    </div>

  </div>

  <div class="container copyright">
    © 2026 Affiliate Academy. All rights reserved.
  </div>

</footer>


<!-- CHECKOUT -->

<div class="modal" id="checkoutModal">

  <div class="modal-box">

    <div class="close" onclick="closeCheckout()">×</div>

    <h2>Enroll in Affiliate Marketing</h2>

    <h3>₹599</h3>

    <p>Scan the QR code to pay.</p>

    <!-- Replace this file with your own QR -->
    <img src="assets/qr.png" class="qr" alt="UPI QR">

    <input id="buyerName" type="text" placeholder="Full Name">
    <input id="buyerEmail" type="email" placeholder="Email">
    <input id="buyerPhone" type="tel" placeholder="Phone Number">
    <input id="transactionId" type="text" placeholder="Transaction ID">

    <button class="btn" onclick="submitPayment()">
      I Have Paid
    </button>

  </div>

</div>


<script>

function openCheckout(){
  document.getElementById("checkoutModal").style.display="flex";
}

function closeCheckout(){
  document.getElementById("checkoutModal").style.display="none";
}

function submitPayment(){

  const name=document.getElementById("buyerName").value;
  const email=document.getElementById("buyerEmail").value;
  const phone=document.getElementById("buyerPhone").value;
  const transaction=document.getElementById("transactionId").value;

  if(!name || !email || !phone || !transaction){
    alert("Please fill all details.");
    return;
  }

  localStorage.setItem("buyerName",name);
  localStorage.setItem("buyerEmail",email);
  localStorage.setItem("buyerPhone",phone);
  localStorage.setItem("transactionId",transaction);

  alert(
    "Payment details submitted. Your access will be activated after verification."
  );

  closeCheckout();
}

function subscribe(event){
  event.preventDefault();
  alert("Thank you for subscribing!");
}

</script>

</body>
</html>
