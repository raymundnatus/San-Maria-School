# San-Maria-School

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>San Maria School of Music</title>
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@600&family=Poppins:wght@400;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #3c096c, #ff01fb, #ffbd00,  #006fc4);
      color: white;
      transition: background 0.4s, color 0.4s;
    }

    h1, h2, h3 {
      font-family: 'Cinzel', serif;
    }

    body.dark-mode {
      background: #1e1e2f;
      color: #f0f0f0;
    }

    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: linear-gradient(135deg, #1900ff, #ffe600);
      padding: 30px 50px;
      flex-wrap: wrap;
    }

    header h1 {
      font-size: 3rem;
    }

    nav {
      background: #ebf376;
      padding: 12px;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 999;
    }

    nav a {
      color: rgb(255, 0, 0);
      margin: 0 15px;
      font-weight: bold;
      text-decoration: none;
      transition: color 0.3s;
    }

    nav a:hover {
      color: #000;
    }

    .toggle-mode {
      position: fixed;
      top: 20px;
      right: 20px;
      background: #ffffff;
      border: none;
      border-radius: 30px;
      padding: 10px 20px;
      font-weight: bold;
      cursor: pointer;
      z-index: 1000;
      box-shadow: 0 4px 10px rgba(255, 254, 254, 0.2);
    }

    body.dark-mode .toggle-mode {
      background: #444;
      color: #fff;
    }

    section {
      padding: 60px 20px;
      max-width: 1100px;
      margin: auto;
      transition: all 0.3s;
    }

    h2 {
      color: #00ffd5;
      margin-bottom: 25px;
    }

    body.dark-mode h2 {
      color: #e1ff00;
    }

    .courses ul {
      list-style: none;
    }

    .courses li::before {
      content: "🎵";
      margin-right: 10px;
    }

    .courses, .contact, .video {
      background: rgba(255, 255, 255, 0.05);
      margin: 30px 0;
      border-radius: 15px;
      padding: 30px;
      box-shadow: 0 4px 16px rgba(255, 255, 255, 0.05);
    }

    body.dark-mode .courses,
    body.dark-mode .contact,
    body.dark-mode .video {
      background: rgba(50, 50, 60, 0.7);
      color: white;
    }

    form input, form textarea {
      width: 100%;
      padding: 12px;
      margin-top: 10px;
      border-radius: 8px;
      border: 1px solid #ccc;
      font-size: 1rem;
    }

    form button {
      background: #00b894;
      color: white;
      padding: 12px 24px;
      border: none;
      margin-top: 15px;
      cursor: pointer;
      font-weight: bold;
      border-radius: 8px;
      transition: background 0.3s;
    }

    form button:hover {
      background: #009879;
    }

    iframe {
      width: 100%;
      height: 350px;
      border-radius: 12px;
      border: none;
    }

    footer {
      background: #2c3e50;
      color: white;
      text-align: center;
      padding: 20px;
    }

    .logo {
      height: 350px;
      width: auto;
      max-width: 100%;
      object-fit: contain;
    }

    /* Teacher Cards */
    .teacher-card-container {
      display: flex;
      flex-wrap: wrap;
      gap: 30px;
      justify-content: center;
    }

    .teacher-card {
      background: rgba(255, 215, 0, 0.75);
      border-radius: 20px;
      backdrop-filter: blur(8px);
      box-shadow: 0 8px 32px rgba(210, 237, 5, 0.15);
      width: 220px;
      text-align: center;
      padding: 25px;
      transition: transform 0.3s, background 0.3s;
      color: black;
    }

    .teacher-card:hover {
      transform: translateY(-8px);
    }

    .teacher-card img {
      width: 140px;
      height: 140px;
      object-fit: cover;
      border-radius: 50%;
      margin-bottom: 15px;
      border: 4px solid #5a44ff;
    }

    /* Floating Notes */
    .note {
      position: absolute;
      color: #fff;
      font-size: 24px;
      opacity: 0.4;
      animation: floatNotes 8s linear infinite;
    }

    @keyframes floatNotes {
      0% { transform: translateY(0) translateX(0); opacity: 0.3;}
      100% { transform: translateY(-100vh) translateX(50px); opacity: 0;}
    }

    /* Animated Instruments */
    .bg-instruments {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      z-index: 0;
      overflow: hidden;
      pointer-events: none;
    }

    .instrument {
      position: absolute;
      opacity: 0.1;
      filter: grayscale(80%);
      animation: floatInstruments 10s ease-in-out infinite alternate;
    }

    @keyframes floatInstruments {
      from { transform: translateY(0) rotate(0deg); }
      to { transform: translateY(-30px) rotate(5deg); }
    }

    main, section, header, footer, nav {
      position: relative;
      z-index: 1;
    }

    @media screen and (max-width: 768px) {
      header h1 {
        font-size: 2rem;
      }
      .teacher-card {
        width: 100%;
      }
    }

    /* Fix color for About & Choir */
    .About p, 
    #choir p,
    .courses p, .courses li, .video p {
      color: white;
    }

  </style>
</head>
<body>



  <!-- 🎸 Animated Instrument Background -->
  <div class="bg-instruments">
    <img src="C:\Users\hp\Downloads\piano-keyboard.gif" class="instrument" style="top: 10%; left: 5%; width: 100px;">
    <img src="C:\Users\hp\Downloads\violin-joypixels.webp" class="instrument" style="bottom: 15%; right: 8%; width: 100px;">
    <img src="C:\Users\hp\Downloads\red-and-white-fender-guitar.webp" class="instrument" style="top: 40%; right: 10%; width: 120px;">
    <img src="C:\Users\hp\Downloads\playing-drums-danny-rico.gif" class="instrument" style="bottom: 10%; left: 65%; width: 110px;">
    <img src="C:\Users\hp\Downloads\cantando-singing.gif" class="instrument" style="top: 60%; left: 50%; width: 100px;">
    <img src="C:\Users\hp\Downloads\tom-and-jerry-tom-the-cat.gif" class="instrument" style="top: 45%; left: 20%; width: 100px;">
    <img src="C:\Users\hp\Downloads\playing-guitar-cole-rolland.gif" class="instrument" style="top: 9%; left: 80%; width: 100px;">
    <img src="C:\Users\hp\Downloads\playing-piano-kyle-landry.gif" class="instrument" style="top: 74%; left: 12%; width: 100px;">
    <img src="C:\Users\hp\Downloads\playing-electric-guitar-tim-henson.gif" class="instrument" style="top: 33%; left: 60%; width: 100px;">
  </div>

  <button class="toggle-mode" onclick="toggleDarkMode()">Toggle Dark Mode</button>

  <script>
    // Floating musical notes animation
    for (let i = 0; i < 30; i++) {
      const note = document.createElement('div');
      note.classList.add('note');
      note.style.left = Math.random() * 100 + 'vw';
      note.style.top = Math.random() * 100 + 'vh';
      note.style.animationDuration = (5 + Math.random() * 5) + 's';
      note.textContent = ['🎶', '🎵', '🎼'][Math.floor(Math.random() * 3)];
      document.body.appendChild(note);
    }
  </script>

<header>
    <div class="center-content">
      <h1>San Maria School of Music</h1>
      <p>Celebrate Life with Music</p>
    </div>
    <img src="C:\Users\hp\Downloads\school_logo-removebg-preview.png" alt="School Logo" class="logo">
  </header>
  
  <nav>
    <a href="#About">About Us</a>
    <a href="#courses">Courses</a>
    <a href="#choir">SMCC</a>
    <a href="#Faculty">Faculty</a>
    <a href="#buying and selling">Buy & Sell</a>
    <a href="#video">Demo</a>
    <a href="#testimonials">Testimonials</a>
    <a href="#gallery">Gallery</a>
    <a href="#branches">Branches</a>
    <a href="#form">Registration</a>
    <a href="#contact">Contact</a>
  </nav>


</style>

<section id="About" class="About Us">
  <h2>About Us</h2>
  <p>
    Established in 2017, Our San Maria School of Music is a vibrant community of musicians, educators, and learners passionate about music, dedicated to fostering a love of music and providing high-quality music education to students of all ages above 7 and backgrounds.
    We offer a supportive and stimulating environment where students develop their musical skill levels and explore their musical interests, develop their playing skills, and achieve their goals.
  </p>
  <p>
    We train our students to confidently take up exams conducted by Trinity College London also.
  </p>
</section>



  <section id="courses" class="courses">
    <h2>Courses Offered</h2>
   
    <!-- Tabs -->
    <div class="tabs">
      <button onclick="showCourse('piano')" class="active">🎹 Piano</button>
      <button onclick="showCourse('violin')">🎻 Violin</button>
      <button onclick="showCourse('guitar')">🎸 Guitar</button>
      <button onclick="showCourse('drums')">🥁 Drums</button>
      <button onclick="showCourse('vocal')">🎤 Vocal</button>
    </div>
  
    <div class="course-grid">
  
      <!-- Piano -->
      <div class="course-card course-tab" id="piano">
        <h3>🎹 Piano Course</h3>
        <ul>
          <li><strong>Benefits:</strong></li>
          <p>- Develops strong musical foundation and hand coordination.</p>
          <p>- Enhances concentration, memory, and finger independence</p>
          <p>- Gain confidence in playing solo and ensemble.</p>
          <li><strong>Features:</strong></li>
          <p>- Training in classical, film, and contemporary music</p>
          <p>- Hands-on practice with scales, chords, and sight-reading</p>
          <p>- Ideal for solo performance, accompaniment, and composition</p>
          <li><strong>Who Can Join?</strong></li>
          <p>- Suitable for ages 5 and above. Whether you're a beginner, a music exam candidate, or a hobbyist—piano offers something for everyone.</p>
        </ul>
      </div>
  
      <!-- Violin -->
      <div class="course-card course-tab" id="violin" style="display:none">
        <h3>🎻 Violin Course</h3>
        <ul>
          <li><strong>Benefits:</strong></li>
         <p>- Enhances fine motor skills and coordination</p>
         <p>- Develops pitch accuracy and listening ability</p>
         <p>- Builds patience, discipline, and emotional expression</p>
         <p>- Performance opportunities</p>
          <li><strong>Features:</strong></li>
          <p>- Training in bowing, fingering, and posture</p>
          <p>- Solo and ensemble performance opportunities</p>
          <p>- Lessons in classical, contemporary, and film music styles</p>
          <li><strong>Who Can Join?</strong></li>
         <p>- Anyone aged 6 and above—no prior experience needed. Ideal for students interested in classical foundations or orchestral music.</p>
        </ul>
      </div>
  
      <!-- Guitar -->
      <div class="course-card course-tab" id="guitar" style="display:none">
        <h3>🎸 Guitar Course</h3>
        <ul>
          <li><strong>Benefits:</strong></li>
          <p>- Improves hand-eye coordination and finger agility</p>
          <p>- Encourages creativity through improvisation and songwriting</p>
          <p>- Builds confidence in solo and group performance</p>
          <li><strong>Features:</strong></li>
          <p>- Acoustic, classical, and electric guitar options</p>
          <p>- Chord progressions, fingerstyle, and strumming techniques</p>
          <p>- Exposure to various genres: pop, rock, jazz, and more</p>
          <li><strong>Who Can Join?</strong></li>
          <p>- Open to ages 7 and up. Perfect for beginners, hobbyists, or aspiring performers.</p>
        </ul>
      </div>
  
      <!-- Drums -->
      <div class="course-card course-tab" id="drums" style="display:none">
        <h3>🥁 Drums Course</h3>
        <ul>
          <li><strong>Benefits:</strong></li>
          <p>- Boosts rhythm, focus, and physical coordination</p>
          <p>- Helps in stress release and energy management</p>
          <p>- Strengthens timing and group synchronization</p>
          <li><strong>Features:</strong></li>
          <p>- Full drum kit and percussion basics</p>
          <p>- Practice in various genres (rock, funk, jazz, gospel)</p>
          <p>- Training in tempo control, fills, and grooves</p>
          <li><strong>Who Can Join?</strong></li>
          <p>- Ages 8+, energetic learners</p>
        </ul>
      </div>
  
      <!-- Vocal -->
      <div class="course-card course-tab" id="vocal" style="display:none">
        <h3>🎤 Vocal Course</h3>
        <ul>
          <li><strong>Benefits:</strong></li>
          <p>- Builds confidence and stage presence</p>
          <p>- Improves breathing, diction, and vocal range</p>
          <p>- Strengthens emotional expression and musicality</p>
          <li><strong>Features:</strong></li>
          <p>- Classical, contemporary, and gospel vocal training</p>
          <p>- Ear training, harmony, and microphone techniques</p>
          <p>- Individual and group performance coaching</p>
          <li><strong>Who Can Join?</strong></li>
          <p>- Open to all ages (5+ to adults). Whether you're a beginner, a church singer, or an aspiring performer—this is for you.</p>
        </ul>
      </div>
  
    </div>
  </section>
  
  <!-- 🌟 Styling -->
  <style>
    .tabs {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 20px;
    }
  
    .tabs button {
      background: transparent;
      border: 2px solid #E5C100;
      color: #E5C100;
      padding: 8px 16px;
      font-weight: bold;
      cursor: pointer;
      border-radius: 30px;
      transition: all 0.3s ease;
    }
  
    .tabs button.active,
    .tabs button:hover {
      background: #E5C100;
      color: black;
    }
  
    .course-grid {
      display: grid;
      grid-template-columns: 1fr;
    }
  
    .course-card {
      background: rgba(253, 255, 124, 0.05);
      padding: 20px;
      border-radius: 10px;
      border: 1px solid #E5C100;
      box-shadow: 0 4px 12px rgba(229, 193, 0, 0.2);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
  
    .course-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 8px 16px rgba(229, 193, 0, 0.4);
    }
  
    .course-card h3 {
      color: #E5C100;
      margin-bottom: 10px;
    }
  
    .course-card ul {
      list-style: disc inside;
      color: #E5C100;
      line-height: 1.6;
    }
  
    @media (min-width: 768px) {
      .course-grid {
        grid-template-columns: repeat(1, 1fr);
      }
    }
  </style>
  
  <!-- 🔁 Script for Tab Switching -->
  <script>
    function showCourse(id) {
      const tabs = document.querySelectorAll('.course-tab');
      const buttons = document.querySelectorAll('.tabs button');
  
      tabs.forEach(tab => tab.style.display = 'none');
      buttons.forEach(btn => btn.classList.remove('active'));
  
      document.getElementById(id).style.display = 'block';
      event.target.classList.add('active');
    }
  </script>
  
  
  </style>

  <section id="choir" class="About">
    <h2>Choir & Concerts</h2>
    <p>✨ Choirs for Eucharistic Celebrations</p>
    <p>✨ Devotional & Cine Music Concerts</p>
    <p>✨ Beautiful Instrumental Performances</p>
    <p>Perfect for church events, special occasions, and spiritual gatherings.</p>
  
    <div style="text-align: center; margin-top: 20px;">
      <img src="C:\Users\hp\Downloads\Choir Poster.jpg" alt="Choir & Concert Poster" 
           style="width: 300px; height: auto; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.2);">
    </div>
  </section>
  
  <section id="Faculty" class="Faculty">
    <h2>Faculty</h2>
    <div class="teacher-card-container">
        <div class="teacher-card">
            <img src="C:\Users\hp\Downloads\Deepak HD (2).jpg" alt="Silvester Deepak" />
            <h3>Mr. Silvester Deepak I</h3>
            <p>Co-Director</p>
            <p>Piano, Guitar, Vocal</p>
          </div>
    
          <div class="teacher-card">
            <img src="C:\Users\hp\Downloads\daddy HD (2).jpg" alt="Mr. Albert Immanuel T" />
            <h3>Mr. Albert Immanuel T</h3>
            <p>Co-Director</p>
            <p>Vocal</p>
          </div>

          <div class="teacher-card">
            <img src="C:\Users\hp\Downloads\Passport photo (3).jpg" alt="Mr. Raymund Natus A" />
            <h3>Mr. Raymund Natus A</h3>
            <p>Violin & Piano</p>
          </div>
    
          <div class="teacher-card">
            <img src="C:\Users\hp\Downloads\WhatsApp Image 2025-07-14 at 11.05.04_ee68b0b0 (2).jpg" alt="Mr. Dannie" />
            <h3>Mr. Dannie Jerome E</h3>
            <p>Piano</p>
          </div>
    
          <div class="teacher-card">
            <img src="C:\Users\hp\Downloads\sindhu master.jpg" alt="Mr. Sindhuraj" />
            <h3>Mr. Sindhuraj</h3>
            <p>Vocal - Carnatic & Hindustani</p>
          </div>
    
          <div class="teacher-card">
            <img src="C:\Users\hp\Downloads\felix (2).jpg" alt="Mr. Felix" />
            <h3>Mr. Felix</h3>
            <p>Violin</p>
          </div>
    
          <div class="teacher-card">
            <img src="C:\Users\hp\Downloads\prem (2).jpg" alt="Mr. Prem" />
            <h3>Mr. Prem</h3>
            <p>Violin</p>
          </div>
    
          <div class="teacher-card">
            <img src="C:\Users\hp\Downloads\sam sambu ica (2).png" alt="Mr. Prabakaran Samuel B" />
            <h3>Mr. Prabakaran Samuel B</h3>
            <p>Drums</p>
          </div>
    
          <div class="teacher-card">
            <img src="C:\Users\hp\Downloads\edwin 1 (2).jpg" alt="Mr. John Edwin" />
            <h3>Mr. John Edwin</h3>
            <p>Advocate</p>
            <p>Legal Advisor</p>
    </div>
  </section>

  <section id="buying and selling" class ="courses">
    <h2>Buying and Selling Musical Instruments</h2>
    <p>- We offered you a wide range of Musical Instruments for Sale</p>
    <p>- We also provided Musical Instruments Services too</p>
    <p>- We buy used Keyboards / Pianos at best Prices</p>
    <p>- We exchange used keyboards and offer new Keyboards for best deals</p>
    <p>- We undertake repair services for Yamaha Keyboards at cost effective rates</p>

    <div style="text-align: center; margin-top: 20px;">
      <img src="C:\Users\hp\Downloads\buy and sell.png" alt="Buy & Sell Poster" 
           style="width: 300px; height: auto; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.2);">
    </div>

    <div class="form-container" style="max-width: 800px; margin: 40px auto; padding: 20px; background: #fff; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1);">
      <h2 style="text-align: center; color: #333;">📝Enquiry Form</h2>
      <iframe src="https://docs.google.com/forms/d/e/1FAIpQLScoH5JNpmfroK-dIgbr4_HafZnqh0xxTzq9fRSJGQ6Pb6LNkw/viewform?usp=dialog" 
              width="100%" 
              height="800" 
              frameborder="0" 
              marginheight="0" 
              marginwidth="0">
        Loading…
      </iframe>
    </div>

   </section> 

  <section id="video" class="video">
    <h2>📽️ Watch Our Demo</h2>
    <iframe src="https://www.youtube.com/embed/hryXR7Rl98Y?si=aO2Zfh4a6nOWb6Bb" allowfullscreen></iframe>
  </section>

  <section id="testimonials" class="video">
    <h2>🌟 Voices of San Maria</h2>
    <div class="testimonial-slider" style="overflow:hidden;">
      <div class="testimonial-track" style="display: flex; transition: transform 0.6s ease; width: 300%;">
        <div class="testimonial" style="min-width: 100%; padding: 20px;">
            <p>“An Excellant place for learning music. Every doubt is clarified with much care. Highly recommend learning here”</p>
            <h4>- Jemima Jason Vasanth Kumar, Piano Student</h4>
          </div>
          <div class="testimonial" style="min-width: 100%; padding: 20px;">
            <p>“It is an excellent place for studying music. I have enrolled my two kids there. Tutors are very dedicated and having very good knowledge in music.</p>
            <h4>-Bridget Cynthia, Parent</h4>
          </div>
          <div class="testimonial" style="min-width: 100%; padding: 20px;">
            <p>“I will give five why because apart from other music school this is the best music school which will improve our talent within us. ”</p>
            <h4>- Antony Gruz., Guitar Student</h4>
          </div>
      </div>
    </div>
  </section>
  <section id="gallery" class="courses">
    <h2>Gallery</h2>
  
    <!-- 🎓 School Gallery -->
    <h3 style="margin-top: 20px; color: white;">🏫 School</h3>
    <div class="gallery-grid" style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px;">
      <img src="C:\Users\hp\Pictures\Screenshots\Screenshot 2025-07-14 184040.png" alt="Classroom" style="width:100%; border-radius:10px;">
      <img src="C:\Users\hp\Pictures\Screenshots\Screenshot 2025-07-14 183952.png" alt="Class" style="width:100%; border-radius:10px;">
      <img src="C:\Users\hp\Pictures\Screenshots\Screenshot 2025-07-14 183916.png" alt="Joyful moment between teacher and students" style="width:100%; border-radius:10px;">
      <img src="C:\Users\hp\Pictures\Screenshots\Screenshot 2025-07-15 175402.png" alt="Joyful moment between teacher and students" style="width:100%; border-radius:10px;">
      <img src="C:\Users\hp\Pictures\Screenshots\Screenshot 2025-07-15 175514.png" alt="Joyful moment between teacher and students" style="width:100%; border-radius:10px;">
      <img src="C:\Users\hp\Pictures\Screenshots\Screenshot 2025-07-15 175534.png" alt="Joyful moment between teacher and students" style="width:100%; border-radius:10px;">
      <img src="C:\Users\hp\Pictures\Screenshots\Screenshot 2025-07-15 175121.png" alt="Joyful moment between teacher and students" style="width:100%; border-radius:10px;">    
    </div>
  
    <!-- 🎤 Choir Gallery -->
    <h3 style="margin-top: 40px; color: white;">🎤 Choir</h3>
    <div class="gallery-grid" style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px;">
      <img src="C:\Users\hp\Downloads\Choir pic.jpg" alt="Choir" style="width:100%; border-radius:10px;">
      <img src="C:\Users\hp\Pictures\Screenshots\Screenshot 2025-07-15 175345.png" alt="Choir" style="width:100%; border-radius:10px;">
      <img src="C:\Users\hp\Pictures\Screenshots\Screenshot 2025-07-15 175213.png" alt="Choir" style="width:100%; border-radius:10px;">
      <img src="C:\Users\hp\Pictures\Screenshots\Screenshot 2025-07-15 175234.png" alt="Choir" style="width:100%; border-radius:10px;">
      <img src="C:\Users\hp\Pictures\Screenshots\Screenshot 2025-07-15 175304.png" alt="Choir" style="width:100%; border-radius:10px;">
    </div>
  </section>
  
  <section id="branches" class="courses">
    <h2>🏫 Our Branches</h2>
    <p>Visit our nearby branches and explore the world of music education!</p>
  
    <div class="branch-grid">
  
      <!-- Branch 1 -->
      <div class="branch-card">
        <h3>🎼 San Maria School of Music - Tambaram Center</h3>
        <iframe 
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d589.3132768579687!2d80.12815602797052!3d12.919932566145077!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3a525f165428cebb%3A0x180e0f8a673cc2e3!2sSan%20Maria%20School%20of%20Music!5e0!3m2!1sen!2sin!4v1752569963913!5m2!1sen!2sin" 
          width="100%" height="300" style="border:0;" allowfullscreen="" loading="lazy"
          referrerpolicy="no-referrer-when-downgrade">
        </iframe>
      </div>
  
      <!-- Branch 2 -->
      <div class="branch-card">
        <h3>🎶 San Maria School of Music - Velachery Center</h3>
        <iframe 
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3887.830484762344!2d80.2243499748198!3d12.982691714635504!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3a525df58045fa3d%3A0x459ef8c8c5ee4dc2!2sSan%20Maria%20School%20of%20Music!5e0!3m2!1sen!2sin!4v1752586065382!5m2!1sen!2sin"
          width="100%" height="300" style="border:0;" allowfullscreen="" loading="lazy"
          referrerpolicy="no-referrer-when-downgrade">
        </iframe>
      </div>
      
      <!-- Branch 3-->
      <div class="branch-card">
        <h3>🎶 San Maria School of Music - Pallikaranai Center</h3>
        <iframe 
          src="https://www.google.com/maps/embed?pb=!1m17!1m12!1m3!1d343.71316812048667!2d80.2101556002812!3d12.928916926463748!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m2!1m1!2zMTLCsDU1JzQ0LjAiTiA4MMKwMTInMzcuNCJF!5e0!3m2!1sen!2sin!4v1752586242006!5m2!1sen!2sin" 
          width="100%" height="300" style="border:0;" allowfullscreen="" loading="lazy"
          referrerpolicy="no-referrer-when-downgrade">
        </iframe>
      </div>
    </div>
  </section>

  
  <style>
    .branch-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
      margin-top: 20px;
    }
  
    .branch-card {
      background: rgba(253, 255, 124, 0.05);
      border: 1px solid #E5C100;
      border-radius: 10px;
      padding: 20px;
      box-shadow: 0 4px 12px rgba(229, 193, 0, 0.2);
      transition: transform 0.3s ease;
    }
  
    .branch-card:hover {
      transform: translateY(-5px);
    }
  
    .branch-card h3 {
      color: #E5C100;
      margin-bottom: 15px;
    }
  </style>

<section id="form" class="courses">
  <div class="form-container" style="max-width: 800px; margin: 40px auto; padding: 20px; background: #fff; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.1);">
    <h2 style="text-align: center; color: #333;">📝 Student Registration Form</h2>
    <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSfLXU35XWO1dDyfifz0Y0Nn00MF0QGLtBNMXD0e6Gk9iMKdkQ/viewform?embedded=true" 
            width="100%" 
            height="800" 
            frameborder="0" 
            marginheight="0" 
            marginwidth="0">
      Loading…
    </iframe>
  </div>
  
</section>


  <section id="contact" class="contact">
    <h2>📩 Contact Us</h2>
  
    <div style="font-size: 1.2rem; line-height: 2;">
  
      <p><strong>📞 Contact Number:</strong>  +91 98413 33888, +91 9940182239, +91 9840393346</p>
  
    </div>
  </section>
  
      <p><strong><i class="fas fa-envelope"></i> Email:</strong>
        <a href="mailto:sanmaria.schoolofmusic@gmail.com" style="color: #00ffcc;">sanmaria.schoolofmusic@gmail.com</a>
      </p>
  
      <p><strong><i class="fas fa-map-marker-alt"></i> Address:</strong>  
        San Maria School of Music, No. 3A, Senbagapoo Street, Bhagavathy Nagar, East Tambaram, Chennai, Tamil Nadu - 600 059
      </p>
  
      <p><strong><i class="fas fa-clock"></i> Hours:</strong>  
        Monday - Saturday: 5 PM – 8 PM
      </p>
    </div>
    </div>
  </section>

  <div style="text-align: center; margin-top: 20px;">
    <h3 style="color: #60fffc;">Follow Us On</h3>
    <div style="margin-top: 10px;">
      <a href="https://www.facebook.com/sanmariamusic.sanmariamusic.5" target="_blank" style="margin: 0 10px; color: #3b5998;">
        <i class="fab fa-facebook fa-2x"></i>
      </a>
      <a href="https://www.instagram.com/sanmariaschoolofmusic2017/" target="_blank" style="margin: 0 10px; color: #E1306C;">
        <i class="fab fa-instagram fa-2x"></i>
      </a>
      <a href="https://www.youtube.com/@sanmariaschoolofmusic9892" target="_blank" style="margin: 0 10px; color: #FF0000;">
        <i class="fab fa-youtube fa-2x"></i>
      </a>
    </div>
  </div>
  

  <!-- Font Awesome for WhatsApp icon -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"/>

<!-- WhatsApp Floating Button -->
<a href="https://api.whatsapp.com/send?phone=919841333888" class="float" target="_blank" title="Chat with us on WhatsApp">
  <i class="fa fa-whatsapp my-float"></i>
</a>

<!-- Style for WhatsApp Button -->
<style>
  .float {
    position: fixed;
    width: 60px;
    height: 60px;
    bottom: 20px;
    right: 20px;
    background-color: #25d366;
    color: white;
    border-radius: 50%;
    text-align: center;
    font-size: 30px;
    box-shadow: 2px 2px 5px rgba(0,0,0,0.3);
    z-index: 999;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: background-color 0.3s ease;
  }

  .float:hover {
    background-color: #20ba5a;
  }

  .my-float {
    margin: 0;
  }
</style>


  <footer>
    <p>&copy; 2025 San Maria School of Music. All rights reserved.</p>
  </footer>

  <script>
    function toggleDarkMode() {
      document.body.classList.toggle('dark-mode');
    }

    let slideIndex = 0;
    const track = document.querySelector('.testimonial-track');
    const totalSlides = document.querySelectorAll('.testimonial').length;

    setInterval(() => {
      slideIndex = (slideIndex + 1) % totalSlides;
      track.style.transform = `translateX(-${slideIndex * 100}%)`;
    }, 4000);
  </script>
</body>
</html>
