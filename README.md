<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>DYP Tours & Travels - Explore the World</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Book your dream vacation with DYP Tours & Travels">
  <meta name="theme-color" content="#000000">

  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
  <!-- Font Awesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  
  <style>
    :root {
      --primary-color: #69cef0;
      --secondary-color: #f40404;
      --text-color: #f3e9e9;
      --bg-color: #000000;
    }
    
    body {
      background-color: var(--bg-color);
      color: var(--text-color);
      font-family: 'Segoe UI', Roboto, 'Helvetica Neue', sans-serif;
      line-height: 1.6;
      -webkit-text-size-adjust: 100%;
      min-width: 320px;
      overflow-x: hidden;
    }
    
    /* Header & Navigation */
    .navbar {
      background-color: var(--primary-color);
      padding: 0.8rem 1rem;
      position: sticky;
      top: 0;
      z-index: 1000;
    }
    
    .navbar-brand {
      font-weight: 700;
      font-size: 1.3rem;
      color: var(--secondary-color);
      display: flex;
      align-items: center;
    }
    
    .navbar-brand i {
      margin-right: 8px;
    }
    
    .nav-link {
      color: var(--secondary-color);
      font-weight: 600;
      padding: 0.5rem 1rem;
      margin: 0 0.2rem;
      border-radius: 4px;
      transition: all 0.3s ease;
    }
    
    .nav-link:hover {
      background-color: rgba(255, 243, 243, 0.897);
    }
    
    .navbar-toggler {
      border: none;
      padding: 0.5rem;
    }
    
    .navbar-toggler:focus {
      box-shadow: none;
    }
    
    /* Main Content */
    .main-header {
      padding: 2rem 0;
      text-align: center;
    }
    
    #heading1 {
      font-size: 2rem;
      margin-bottom: 1.5rem;
      animation: float 4s ease-in-out infinite;
    }
    
    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-15px); }
    }
    
    .hero-img {
      width: 100%;
      max-height: 60vh;
      object-fit: cover;
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.3);
    }
    
    /* Sections */
    .section-title {
      font-size: 1.8rem;
      margin-bottom: 1.5rem;
      text-align: center;
      position: relative;
      padding-bottom: 0.5rem;
    }
    
    .section-title::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translateX(-50%);
      width: 80px;
      height: 3px;
      background-color: var(--primary-color);
    }
    
    .card-img {
      height: 180px;
      object-fit: cover;
      border-radius: 8px 8px 0 0;
      transition: transform 0.3s ease;
    }
    
    .card {
      border: none;
      border-radius: 8px;
      overflow: hidden;
      background-color: #e9eb73;
      transition: all 0.3s ease;
      margin-bottom: 1.5rem;
      height: 100%;
    }
    
    .card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 20px rgba(233, 227, 227, 0.2);
    }
    
    .card-body {
      padding: 1.2rem;
    }
    
    .card-title {
      font-size: 1.1rem;
      font-weight: 600;
      margin-bottom: 0.5rem;
      text-align: center;
    }
    
    /* Contact Form */
    .contact-form {
      background-color: #423e3e;
      padding: 1.5rem;
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
    }
    
    .form-control {
      background-color: #e8dfdf;
      border: 1px solid #1f1f1f;
      color: white;
      padding: 0.8rem 1rem;
      margin-bottom: 1rem;
    }
    
    .form-control:focus {
      background-color: #ffffff;
      color: rgb(0, 0, 0);
      border-color: var(--primary-color);
      box-shadow: 0 0 0 0.25rem rgb(125, 134, 255);
    }
    
    .btn-primary {
      background-color: var(--primary-color);
      border: none;
      padding: 0.8rem 1.5rem;
      font-weight: 600;
      width: 100%;
    }
    
    .btn-primary:hover {
      background-color: #5ab8d9;
    }
    
    .contact-info {
      padding: 1.5rem;
    }
    
    .contact-item {
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
    }
    
    .contact-icon {
      width: 40px;
      height: 40px;
      background-color: var(--primary-color);
      color: white;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-right: 1rem;
      flex-shrink: 0;
    }
    
    /* Footer */
    footer {
      background-color: #8e8b8b;
      padding: 2rem 0;
      margin-top: 3rem;
    }
    
    .social-icons {
      display: flex;
      justify-content: center;
      margin: 1.5rem 0;
    }
    
    .social-icon {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      background-color: #211e1e;
      color: rgb(255, 251, 251);
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 0.5rem;
      transition: all 0.3s ease;
    }
    
    .social-icon:hover {
      background-color: var(--primary-color);
      transform: translateY(-3px);
    }
    
    .copyright {
      text-align: center;
      font-size: 0.9rem;
      opacity: 0.8;
    }
    
    /* Responsive Adjustments */
    @media (max-width: 768px) {
      #heading1 {
        font-size: 1.6rem;
      }
      
      .section-title {
        font-size: 1.5rem;
      }
      
      .navbar-brand {
        font-size: 1.1rem;
      }
      
      .hero-img {
        max-height: 40vh;
      }
      
      .card-img {
        height: 150px;
      }
      
      .contact-item {
        flex-direction: column;
        text-align: center;
      }
      
      .contact-icon {
        margin-right: 0;
        margin-bottom: 0.5rem;
      }
    }
    
    @media (max-width: 576px) {
      .navbar-nav {
        margin-top: 1rem;
      }
      
      .nav-link {
        margin: 0.2rem 0;
        text-align: center;
      }
      
      #heading1 {
        font-size: 1.4rem;
      }
      
      .section-title {
        font-size: 1.3rem;
      }
    }
  </style>
</head>
<body>
  <!-- Navigation -->
  <nav class="navbar navbar-expand-lg navbar-light">
    <div class="container">
      <a class="navbar-brand" href="#">
        <i class="fas fa-plane"></i>DYP Tours & Travels
      </a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item">
            <a class="nav-link" href="#home">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#places">Places</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#stay">Stay</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#adventure">Adventure</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#contact">Contact</a>
          </li>
        </ul>
        <form class="d-flex ms-lg-3 mt-3 mt-lg-0">
          <input class="form-control me-2" type="search" placeholder="Search..." aria-label="Search">
          <button class="btn btn-outline-primary" type="submit">Search</button>
        </form>
      </div>
    </div>
  </nav>

  <!-- Hero Section -->
  <section class="main-header" id="home">
    <div class="container">
      <h1 id="heading1">Discover Your Perfect Journey With Us</h1>
      <img src="https://images.unsplash.com/photo-1506929562872-bb421503ef21?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2580&q=80" 
           alt="Travel destinations around the world" 
           class="hero-img">
    </div>
  </section>

  <!-- Places Section -->
  <section class="container py-5" id="places">
    <h2 class="section-title">Popular Destinations</h2>
    <div class="row">
      <div class="col-md-6 col-lg-3">
        <div class="card h-100">
          <img src="https://images.unsplash.com/photo-1431274172761-fca41d930114?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" 
               class="card-img" 
               alt="Paris, France">
          <div class="card-body">
            <h5 class="card-title">Paris, France</h5>
            <p class="card-text text-center">From $899</p>
          </div>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="card h-100">
          <img src="https://images.unsplash.com/photo-1496442226666-8d4d0e62e6e9?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" 
               class="card-img" 
               alt="New York, USA">
          <div class="card-body">
            <h5 class="card-title">New York, USA</h5>
            <p class="card-text text-center">From $799</p>
          </div>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="card h-100">
          <img src="https://images.unsplash.com/photo-1542051841857-5f90071e7989?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" 
               class="card-img" 
               alt="Tokyo, Japan">
          <div class="card-body">
            <h5 class="card-title">Tokyo, Japan</h5>
            <p class="card-text text-center">From $1099</p>
          </div>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="card h-100">
          <img src="https://images.unsplash.com/photo-1518684079-3c830dcef090?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" 
               class="card-img" 
               alt="Dubai, UAE">
          <div class="card-body">
            <h5 class="card-title">Dubai, UAE</h5>
            <p class="card-text text-center">From $1299</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Stay Section -->
  <section class="container py-5" id="stay">
    <h2 class="section-title">Luxury Stays</h2>
    <div class="row">
      <div class="col-md-6 col-lg-3">
        <div class="card h-100">
          <img src="https://images.unsplash.com/photo-1566073771259-6a8506099945?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" 
               class="card-img" 
               alt="Luxury Hotel A">
          <div class="card-body">
            <h5 class="card-title">The Grand Plaza</h5>
            <p class="card-text text-center">5-star | From $299/night</p>
          </div>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="card h-100">
          <img src="https://images.unsplash.com/photo-1582719478250-c89cae4dc85b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" 
               class="card-img" 
               alt="Luxury Hotel B">
          <div class="card-body">
            <h5 class="card-title">Ocean View Resort</h5>
            <p class="card-text text-center">5-star | From $349/night</p>
          </div>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="card h-100">
          <img src="https://images.unsplash.com/photo-1564501049412-61c2a3083791?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" 
               class="card-img" 
               alt="Luxury Hotel C">
          <div class="card-body">
            <h5 class="card-title">Mountain Retreat</h5>
            <p class="card-text text-center">5-star | From $279/night</p>
          </div>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="card h-100">
          <img src="https://images.unsplash.com/photo-1551882547-ff40c63fe5fa?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" 
               class="card-img" 
               alt="Luxury Hotel D">
          <div class="card-body">
            <h5 class="card-title">Desert Oasis</h5>
            <p class="card-text text-center">5-star | From $319/night</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Adventure Section -->
  <section class="container py-5" id="adventure">
    <h2 class="section-title">Adventure Awaits</h2>
    <div class="row">
      <div class="col-md-6 col-lg-3">
        <div class="card h-100">
          <img src="https://images.unsplash.com/photo-1551632811-561732d1e306?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" 
               class="card-img" 
               alt="Paragliding Adventure">
          <div class="card-body">
            <h5 class="card-title">Paragliding</h5>
            <p class="card-text text-center">From $149/experience</p>
          </div>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="card h-100">
          <img src="https://images.unsplash.com/photo-1544551763-46a013bb70d5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" 
               class="card-img" 
               alt="Scuba Diving">
          <div class="card-body">
            <h5 class="card-title">Scuba Diving</h5>
            <p class="card-text text-center">From $199/dive</p>
          </div>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="card h-100">
          <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" 
               class="card-img" 
               alt="Mountaineering">
          <div class="card-body">
            <h5 class="card-title">Mountaineering</h5>
            <p class="card-text text-center">From $249/trip</p>
          </div>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="card h-100">
          <img src="https://images.unsplash.com/photo-1509316785289-025f5b846b35?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80" 
               class="card-img" 
               alt="Desert Safari">
          <div class="card-body">
            <h5 class="card-title">Desert Safari</h5>
            <p class="card-text text-center">From $129/tour</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section class="container py-5" id="contact">
    <h2 class="section-title">Get In Touch</h2>
    <div class="row">
      <div class="col-lg-6 mb-4 mb-lg-0">
        <div class="contact-form">
          <form id="contactForm">
            <div class="mb-3">
              <label for="name" class="form-label">Full Name</label>
              <input type="text" class="form-control" id="name" required>
            </div>
            <div class="mb-3">
              <label for="email" class="form-label">Email Address</label>
              <input type="email" class="form-control" id="email" required>
            </div>
            <div class="mb-3">
              <label for="phone" class="form-label">Phone Number</label>
              <input type="tel" class="form-control" id="phone">
            </div>
            <div class="mb-3">
              <label for="message" class="form-label">Your Message</label>
              <textarea class="form-control" id="message" rows="4" required></textarea>
            </div>
            <button type="submit" class="btn btn-primary">Send Message</button>
          </form>
        </div>
      </div>
      <div class="col-lg-6">
        <div class="contact-info">
          <h3 class="mb-4">Contact Information</h3>
          <div class="contact-item">
            <div class="contact-icon">
              <i class="fas fa-map-marker-alt"></i>
            </div>
            <div>
              <h5>Address</h5>
              <p>Dy Patil Kasaba Bawada</p>
            </div>
          </div>
          <div class="contact-item">
            <div class="contact-icon">
              <i class="fas fa-phone-alt"></i>
            </div>
            <div>
              <h5>Phone</h5>
              <p>+91 9764482435</p>
            </div>
          </div>
          <div class="contact-item">
            <div class="contact-icon">
              <i class="fas fa-envelope"></i>
            </div>
            <div>
              <h5>Email</h5>
              <p>info@dyptours.com</p>
            </div>
          </div>
          <div class="contact-item">
            <div class="contact-icon">
              <i class="fas fa-clock"></i>
            </div>
            <div>
              <h5>Working Hours</h5>
              <p>Monday - Saturday: 9:00 AM - 6:00 PM</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="container">
      <div class="social-icons">
        <a href="#" class="social-icon" aria-label="Facebook">
          <i class="fab fa-facebook-f"></i>
        </a>
        <a href="#" class="social-icon" aria-label="Twitter">
          <i class="fab fa-twitter"></i>
        </a>
        <a href="#" class="social-icon" aria-label="Instagram">
          <i class="fab fa-instagram"></i>
        </a>
        <a href="#" class="social-icon" aria-label="LinkedIn">
          <i class="fab fa-linkedin-in"></i>
        </a>
        <a href="https://wa.me/919158630136" class="social-icon" aria-label="WhatsApp">
          <i class="fab fa-whatsapp"></i>
        </a>
      </div>
      <p class="copyright">© 2025 DYP Tours & Travels. All Rights Reserved.</p>
    </div>
  </footer>

  <!-- Bootstrap JS Bundle with Popper -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  
  <script>
    document.addEventListener('DOMContentLoaded', function() {
      // Form submission
      const contactForm = document.getElementById('contactForm');
      if (contactForm) {
        contactForm.addEventListener('submit', function(e) {
          e.preventDefault();
          alert('Thank you for your message! We will contact you soon.');
          contactForm.reset();
        });
      }
      
      // Smooth scrolling for anchor links
      document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
          e.preventDefault();
          
          const targetId = this.getAttribute('href');
          const targetElement = document.querySelector(targetId);
          
          if (targetElement) {
            window.scrollTo({
              top: targetElement.offsetTop - 80,
              behavior: 'smooth'
            });
            
            // Close mobile menu if open
            const navbarCollapse = document.querySelector('.navbar-collapse');
            if (navbarCollapse.classList.contains('show')) {
              new bootstrap.Collapse(navbarCollapse).hide();
            }
          }
        });
      });
      
      // Search functionality
      const searchForm = document.querySelector('.navbar form.d-flex');
      if (searchForm) {
        searchForm.addEventListener('submit', function(e) {
          e.preventDefault();
          const searchInput = this.querySelector('input[type="search"]');
          const searchTerm = searchInput.value.toLowerCase();
          
          let targetSection = null;
          
          if (searchTerm.includes('place') || searchTerm.includes('destination')) {
            targetSection = document.getElementById('places');
          } else if (searchTerm.includes('stay') || searchTerm.includes('hotel')) {
            targetSection = document.getElementById('stay');
          } else if (searchTerm.includes('adventure') || searchTerm.includes('activity')) {
            targetSection = document.getElementById('adventure');
          } else if (searchTerm.includes('contact') || searchTerm.includes('help')) {
            targetSection = document.getElementById('contact');
          } else if (searchTerm.includes('home') || searchTerm.includes('main')) {
            targetSection = document.getElementById('home');
          }
          
          if (targetSection) {
            window.scrollTo({
              top: targetSection.offsetTop - 80,
              behavior: 'smooth'
            });
          } else {
            alert('No results found for "' + searchTerm + '". Try searching for "Places", "Stay", "Adventure" or "Contact".');
          }
          
          searchInput.value = '';
        });
      }
    });
  </script>
</body>
</html>
