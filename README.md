<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>DYP TOURS & TRAVELLERS</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <meta name="theme-color" content="#000000">

  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
  <style>
    body {
      background-color: #afa9a9;
      color: #f3e9e9;
      font-family: 'Roboto', sans-serif;
      font-size: 16px;
      -webkit-text-size-adjust: 100%;
    }

    .navbar {
      background-color: #69cef0;
      padding: 10px 0;
    }

    .navbar-brand {
      font-size: 1.2rem;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      max-width: 60%;
    }

    .navbar a {
      color: #f40404;
      font-weight: bold;
      text-decoration: none;
      font-size: 0.9rem;
      padding: 5px 8px;
    }

    #heading1 {
      animation: float 5s ease-in-out infinite;
      font-size: 1.8rem;
      margin-top: 15px;
    }

    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0); }
    }

    footer .navbar {
      margin-top: 1rem;
      padding: 10px 0;
    }

    .social-icons img {
      width: 20px;
      height: 20px;
      margin: 0 5px;
    }

    .form-control, .form-label {
      color: #222222;
      font-size: 0.9rem;
    }

    .form-section input {
      margin-bottom: 0.8rem;
    }

    .fixed-img {
      width: 100%;
      height: 150px;
      object-fit: cover;
      border-radius: 8px;
    }

    section {
      padding: 15px 0;
    }

    h2 {
      font-size: 1.5rem;
      margin-bottom: 15px !important;
    }

    /* Mobile-specific optimizations */
    @media (max-width: 768px) {
      .navbar-collapse {
        background-color: #69cef0;
        padding: 10px;
        margin-top: 10px;
        border-radius: 5px;
      }
      
      .navbar-toggler {
        border: none;
        padding: 5px 10px;
      }
      
      .navbar-toggler-icon {
        width: 1.2em;
        height: 1.2em;
      }
      
      #search {
        margin-top: 10px;
        width: 100%;
      }
      
      #searchBtn {
        width: 100%;
        margin-left: 0 !important;
        margin-top: 5px;
      }
      
      .fixed-img {
        height: 120px;
      }
      
      .col-md-3 {
        margin-bottom: 15px;
      }
      
      #heading1 {
        font-size: 1.5rem;
      }
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg navbar-light px-3">
    <div class="container-fluid">
      <a class="navbar-brand" href="#"><b><i>DYP Tours & Travels</i></b></a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <div class="ms-auto d-flex flex-column flex-lg-row align-items-lg-center">
          <a href="#cont1">Home</a>
          <a href="#cont2">Places</a>
          <a href="#cont4">Stay</a>
          <a href="#cont5">Adventure</a>
          <a href="#cont3">Contact</a>
          <input class="form-control form-control-sm mt-2 mt-lg-0 ms-lg-3" id="search" placeholder="Search">
          <button class="btn btn-outline-primary btn-sm mt-2 mt-lg-0 ms-lg-2" id="searchBtn">Search</button>
        </div>
      </div>
    </div>
  </nav>

  <!-- Home Section -->
  <section class="container text-center my-3" id="cont1">
    <h1 id="heading1">Welcome to <b>DYP Tours & Travels</b></h1>
    <img src="https://media.cntraveler.com/photos/64879b50add73e0d14b17f9e/16:9/w_2580,c_limit/Most-Adventurous-things-to-do-in-your-lifetime-(update)_timur-garifov-sisZWCDkmwA-unsplash.jpg" 
         class="img-fluid mt-3" 
         alt="Travel Banner"
         style="max-height: 200px; width: 100%; object-fit: cover;">
  </section>

  <!-- Places Section -->
  <section class="container my-3" id="cont2">
    <h2 class="text-center mb-3">Places</h2>
    <div class="row g-3">
      <div class="col-6 col-md-3"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQuIhmhSMBC44mycWicjO6jHLghQWEmzksW4Q&s" class="img-fluid fixed-img"><p class="text-center mt-2">Paris</p></div>
      <div class="col-6 col-md-3"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQigoJfWCGdP4fnwRnCXQ0rbBTcTGNwC33spA&s" class="img-fluid fixed-img"><p class="text-center mt-2">New York</p></div>
      <div class="col-6 col-md-3"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTOQmNpxrD9ccoxZ3Q23LOOE93wLr_tMR7LFQ&s" class="img-fluid fixed-img"><p class="text-center mt-2">Tokyo</p></div>
      <div class="col-6 col-md-3"><img src="https://cdn.britannica.com/43/134743-050-D0625A44/train-first-Dubai-emirate-rapid-transit-line-kind-Sept-10-2009.jpg" class="img-fluid fixed-img"><p class="text-center mt-2">Dubai</p></div>
    </div>
  </section>

  <!-- Stay Section -->
  <section class="container my-3" id="cont4">
    <h2 class="text-center mb-3">Stay</h2>
    <div class="row g-3">
      <div class="col-6 col-md-3"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ69nti-8_ijCzxKdRYCZfKH7wfL4DT7UFltA&s" class="img-fluid fixed-img"><p class="text-center mt-2">Hotel A</p></div>
      <div class="col-6 col-md-3"><img src="https://www.travelanddestinations.com/wp-content/uploads/2017/03/Beautiful-interiors-at-Hotel-Imperial-Vienna.jpg" class="img-fluid fixed-img"><p class="text-center mt-2">Hotel B</p></div>
      <div class="col-6 col-md-3"><img src="https://media.cntraveler.com/photos/53da60a46dec627b149e66f4/4:3/w_935,h_701,c_limit/hilton-moorea-lagoon-resort-spa-moorea-french-poly--110160-1.jpg" class="img-fluid fixed-img"><p class="text-center mt-2">Hotel C</p></div>
      <div class="col-6 col-md-3"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSdwSEUbQrpwY63uLruCuFzarnOW3Pa5NGNUw&s" class="img-fluid fixed-img"><p class="text-center mt-2">Hotel D</p></div>
    </div>
  </section>

  <!-- Adventure Section -->
  <section class="container my-3" id="cont5">
    <h2 class="text-center mb-3">Adventure</h2>
    <div class="row g-3">
      <div class="col-6 col-md-3"><img src="https://static.wixstatic.com/media/a56ba3_bfb12af785fd40ee9d8439bf00eeb49e~mv2.jpeg/v1/fill/w_1000,h_563,al_c,q_85,usm_0.66_1.00_0.01/a56ba3_bfb12af785fd40ee9d8439bf00eeb49e~mv2.jpeg" class="img-fluid fixed-img"><p class="text-center mt-2">Paragliding</p></div>
      <div class="col-6 col-md-3"><img src="https://res.cloudinary.com/manawa/image/upload/f_auto,c_limit,w_3840,q_auto/articles/most-beautiful-spots-for-your-first-scuba-dive/61396758347_kwukov" class="img-fluid fixed-img"><p class="text-center mt-2">Scuba Diving</p></div>
      <div class="col-6 col-md-3"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSFyBiVKTBXZWl4iy8zopeQM3XOyBBsQ2i1dg&s" class="img-fluid fixed-img"><p class="text-center mt-2">Mountaineering</p></div>
      <div class="col-6 col-md-3"><img src="https://media-cdn.tripadvisor.com/media/attractions-splice-spp-674x446/13/bb/6a/7b.jpg" class="img-fluid fixed-img"><p class="text-center mt-2">Desert Safari</p></div>
    </div>
  </section>

  <!-- Contact Section -->
  <section class="container my-3" id="cont3">
    <h2 class="text-center mb-3">Contact Our Office</h2>
    <div class="row">
      <div class="col-md-6 form-section">
        <label for="Name" class="form-label">Name</label>
        <input type="text" class="form-control" id="Name" placeholder="Full Name">

        <label for="MOB" class="form-label">Mobile No</label>
        <input type="tel" class="form-control" id="MOB" placeholder="+91 00000 00000" pattern="[0-9]{10}">

        <label for="email" class="form-label">Email ID</label>
        <input type="email" class="form-control" id="email" placeholder="abc@gmail.com">

        <label for="Addr" class="form-label">Address</label>
        <input type="text" class="form-control" id="Addr" placeholder="Your Address">

        <button class="btn btn-primary mt-2 w-100" id="submitBtn">Submit</button>
      </div>

      <div class="col-md-6 mt-3 mt-md-0">
        <p><i class="fas fa-envelope"></i> <strong>Email:</strong> dyptourstravels@gmail.com</p>
        <p><i class="fas fa-phone"></i> <strong>Mobile:</strong> +91 9158630136</p>
        <p><i class="fas fa-clock"></i> <strong>Hours:</strong> 9:00 AM - 6:00 PM (Mon-Sat)</p>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <nav class="navbar">
      <div class="text-center w-100">
        <b>© All Rights Reserved | DYP Tours & Travels</b>
        <div class="social-icons mt-2">
          <a href="#"><img src="https://img.icons8.com/ios-filled/24/ffffff/facebook--v1.png" alt="Facebook"/></a>
          <a href="#"><img src="https://img.icons8.com/ios-filled/24/ffffff/instagram-new.png" alt="Instagram"/></a>
          <a href="#"><img src="https://img.icons8.com/ios-filled/24/ffffff/linkedin.png" alt="LinkedIn"/></a>
          <a href="#"><img src="https://img.icons8.com/ios-filled/24/ffffff/twitter.png" alt="Twitter"/></a>
          <a href="https://wa.me/919158630136"><img src="https://img.icons8.com/ios-filled/24/ffffff/whatsapp.png" alt="WhatsApp"/></a>
        </div>
      </div>
    </nav>
  </footer>

  <!-- jQuery & Bootstrap JS -->
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js"></script>

  <script>
    $(document).ready(function() {
      // Search functionality
      $('#searchBtn').click(function () {
        let query = $('#search').val().toLowerCase();
        if (query.includes('place')) {
          $('html, body').animate({ scrollTop: $('#cont2').offset().top - 70 }, 800);
        } else if (query.includes('stay')) {
          $('html, body').animate({ scrollTop: $('#cont4').offset().top - 70 }, 800);
        } else if (query.includes('adventure')) {
          $('html, body').animate({ scrollTop: $('#cont5').offset().top - 70 }, 800);
        } else if (query.includes('contact') || query.includes('help')) {
          $('html, body').animate({ scrollTop: $('#cont3').offset().top - 70 }, 800);
        } else if (query.includes('home')) {
          $('html, body').animate({ scrollTop: $('#cont1').offset().top - 70 }, 800);
        } else {
          alert('No results found for "' + query + '". Try searching for "Places", "Stay", "Adventure" or "Contact".');
        }
      });

      // Form submission
      $('#submitBtn').click(function () {
        if ($('#Name').val() && $('#MOB').val() && $('#email').val()) {
          alert("Thanks for contacting DYP Tours & Travels! We'll get back to you soon.");
          $('#Name, #MOB, #email, #Addr').val('');
        } else {
          alert("Please fill in all required fields (Name, Mobile, Email).");
        }
      });
      
      // Make social icons clickable
      $('.social-icons a').click(function(e) {
        e.preventDefault();
        // In a real implementation, these would link to your social media pages
        alert('This would link to our social media page in the live version.');
      });
      
      // Better mobile menu handling
      $('.navbar a').click(function() {
        if ($(window).width() < 768) {
          $('.navbar-collapse').collapse('hide');
        }
      });
    });
    
    // Prevent zooming on mobile
    document.addEventListener('gesturestart', function (e) {
      e.preventDefault();
    });
  </script>

</body>
</html>
