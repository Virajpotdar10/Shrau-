

<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>DYP Tours & Travels</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet">
  <style>
    body {
      background-color: black;
      color: white;
    }

    .navbar {
      background-color: yellow;
    }

    .navbar a {
      color: black;
      font-weight: bold;
      margin: 0 10px;
      text-decoration: none;
    }

    #heading1 {
      animation: float 5s ease-in-out infinite;
    }

    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-20px); }
      100% { transform: translateY(0); }
    }

    footer .navbar {
      margin-top: 2rem;
      flex-wrap: wrap;
      justify-content: center;
    }

    .social-icons img {
      margin: 0 10px;
    }

    .form-control, .form-label {
      color: black;
    }

    .form-section input {
      margin-bottom: 1rem;
    }

    .fixed-img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      border-radius: 10px;
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg navbar-light px-4">
    <a class="navbar-brand" href="#"><b><i>DYP Tours & Travels</i></b></a>
    <div class="ms-auto d-flex align-items-center">
      <a href="#cont1">Home</a>
      <a href="#cont2">Places</a>
      <a href="#cont4">Stay</a>
      <a href="#cont5">Adventure</a>
      <a href="#cont3">Contact</a>
      <input class="form-control form-control-sm ms-3" id="search" placeholder="Search">
      <button class="btn btn-outline-primary btn-sm ms-2" id="searchBtn">Search</button>
    </div>
  </nav>

  <!-- Home Section -->
  <section class="container text-center my-5" id="cont1">
    <h1 id="heading1">Welcome to <b>DYP Tours & Travels</b></h1>
    <img src="https://media.cntraveler.com/photos/64879b50add73e0d14b17f9e/16:9/w_2580,c_limit/Most-Adventurous-things-to-do-in-your-lifetime-(update)_timur-garifov-sisZWCDkmwA-unsplash.jpg" class="img-fluid mt-4" alt="Travel Banner">
  </section>

  <!-- Places Section -->
  <section class="container my-5" id="cont2">
    <h2 class="text-center mb-4">Places</h2>
    <div class="row g-4">
      <div class="col-md-3"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQuIhmhSMBC44mycWicjO6jHLghQWEmzksW4Q&s" class="img-fluid fixed-img"><p class="text-center mt-2">Paris</p></div>
      <div class="col-md-3"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQigoJfWCGdP4fnwRnCXQ0rbBTcTGNwC33spA&s" class="img-fluid fixed-img"><p class="text-center mt-2">New York</p></div>
      <div class="col-md-3"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTOQmNpxrD9ccoxZ3Q23LOOE93wLr_tMR7LFQ&s" class="img-fluid fixed-img"><p class="text-center mt-2">Tokyo</p></div>
      <div class="col-md-3"><img src="https://cdn.britannica.com/43/134743-050-D0625A44/train-first-Dubai-emirate-rapid-transit-line-kind-Sept-10-2009.jpg" class="img-fluid fixed-img"><p class="text-center mt-2">Dubai</p></div>
    </div>
  </section>

  <!-- Stay Section -->
  <section class="container my-5" id="cont4">
    <h2 class="text-center mb-4">Stay</h2>
    <div class="row g-4">
      <div class="col-md-3"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ69nti-8_ijCzxKdRYCZfKH7wfL4DT7UFltA&s" class="img-fluid fixed-img"><p class="text-center mt-2">Hotel A</p></div>
      <div class="col-md-3"><img src="https://www.travelanddestinations.com/wp-content/uploads/2017/03/Beautiful-interiors-at-Hotel-Imperial-Vienna.jpg" class="img-fluid fixed-img"><p class="text-center mt-2">Hotel B</p></div>
      <div class="col-md-3"><img src="https://media.cntraveler.com/photos/53da60a46dec627b149e66f4/4:3/w_935,h_701,c_limit/hilton-moorea-lagoon-resort-spa-moorea-french-poly--110160-1.jpg" class="img-fluid fixed-img"><p class="text-center mt-2">Hotel C</p></div>
      <div class="col-md-3"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSdwSEUbQrpwY63uLruCuFzarnOW3Pa5NGNUw&s" class="img-fluid fixed-img"><p class="text-center mt-2">Hotel D</p></div>
    </div>
  </section>

  <!-- Adventure Section -->
  <section class="container my-5" id="cont5">
    <h2 class="text-center mb-4">Adventure</h2>
    <div class="row g-4">
      <div class="col-md-3"><img src="https://static.wixstatic.com/media/a56ba3_bfb12af785fd40ee9d8439bf00eeb49e~mv2.jpeg/v1/fill/w_1000,h_563,al_c,q_85,usm_0.66_1.00_0.01/a56ba3_bfb12af785fd40ee9d8439bf00eeb49e~mv2.jpeg" class="img-fluid fixed-img"><p class="text-center mt-2">Paragliding</p></div>
      <div class="col-md-3"><img src="https://res.cloudinary.com/manawa/image/upload/f_auto,c_limit,w_3840,q_auto/articles/most-beautiful-spots-for-your-first-scuba-dive/61396758347_kwukov" class="img-fluid fixed-img"><p class="text-center mt-2">Scuba Diving</p></div>
      <div class="col-md-3"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSFyBiVKTBXZWl4iy8zopeQM3XOyBBsQ2i1dg&s" class="img-fluid fixed-img"><p class="text-center mt-2">Mountaineering</p></div>
      <div class="col-md-3"><img src="https://media-cdn.tripadvisor.com/media/attractions-splice-spp-674x446/13/bb/6a/7b.jpg" class="img-fluid fixed-img"><p class="text-center mt-2">Desert Safari</p></div>
    </div>
  </section>

  <!-- Contact Section -->
  <section class="container my-5" id="cont3">
    <h2 class="text-center mb-4">Contact Our Office</h2>
    <div class="row">
      <div class="col-md-6 form-section">
        <label for="Name" class="form-label">Name</label>
        <input type="text" class="form-control" id="Name" placeholder="Full Name">

        <label for="MOB" class="form-label">Mobile No</label>
        <input type="number" class="form-control" id="MOB" placeholder="+91 00000 00000">

        <label for="email" class="form-label">Email ID</label>
        <input type="email" class="form-control" id="email" placeholder="abc@gmail.com">

        <label for="Addr" class="form-label">Address</label>
        <input type="text" class="form-control" id="Addr" placeholder="Your Address">

        <button class="btn btn-primary mt-3" id="submitBtn">Submit</button>
      </div>

      <div class="col-md-6">
        <p><strong>Email:</strong> dyptourstravels@gmail.com</p>
        <p><strong>Mobile:</strong> +91 9158630136</p>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <nav class="navbar">
      <div class="text-center w-100">
        <b>© All Rights Reserved | DYP Tours & Travels</b>
        <div class="social-icons mt-2">
          <img src="https://img.icons8.com/ios-filled/24/facebook--v1.png"/>
          <img src="https://img.icons8.com/ios-filled/24/instagram-new.png"/>
          <img src="https://img.icons8.com/ios-filled/24/linkedin.png"/>
          <img src="https://img.icons8.com/ios-filled/24/twitter.png"/>
          <img src="https://img.icons8.com/ios-filled/24/whatsapp.png"/>
        </div>
      </div>
    </nav>
  </footer>

  <!-- jQuery & Bootstrap JS -->
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js"></script>

  <script>
    $('#searchBtn').click(function () {
      let query = $('#search').val().toLowerCase();
      if (query.includes('place')) {
        $('html, body').animate({ scrollTop: $('#cont2').offset().top }, 800);
      } else if (query.includes('stay')) {
        $('html, body').animate({ scrollTop: $('#cont4').offset().top }, 800);
      } else if (query.includes('adventure')) {
        $('html, body').animate({ scrollTop: $('#cont5').offset().top }, 800);
      } else if (query.includes('contact')) {
        $('html, body').animate({ scrollTop: $('#cont3').offset().top }, 800);
      } else {
        alert('No results found!');
      }
    });

    $('#submitBtn').click(function () {
      alert("Thanks for contacting DYP Tours & Travels! We'll get back to you soon.");
      $('#Name, #MOB, #email, #Addr').val('');
    });
  </script>

</body>
</html>
