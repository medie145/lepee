# lepee
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>L'épée - A Christian Platform</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background: #f9f9f9;
      color: #333;
    }
    header {
      background: #0e1d34;
      color: #f1c40f;
      padding: 20px;
      text-align: center;
    }
    header img {
      max-width: 120px;
      display: block;
      margin: 0 auto 10px;
    }
    nav {
      background: #1b2a4e;
      padding: 10px;
      text-align: center;
    }
    nav a {
      color: white;
      margin: 0 15px;
      text-decoration: none;
      font-weight: bold;
    }
    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
    }
    .verse-box {
      background: #e0d4ed;
      border-left: 5px solid #6a3790;
      padding: 15px;
      margin-bottom: 30px;
      font-style: italic;
    }
    .form-container {
      background: #eee5f5;
      padding: 20px;
      border-radius: 8px;
      margin-top: 30px;
    }
    .form-container input,
    .form-container textarea {
      width: 100%;
      padding: 10px;
      margin: 8px 0;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    .form-container button {
      background-color: #6a3790;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    .form-container button:hover {
      background-color: #502b72;
    }
    .whatsapp-button {
      display: inline-block;
      margin-top: 15px;
      padding: 10px 20px;
      background-color: #25D366;
      color: white;
      border-radius: 5px;
      text-decoration: none;
      font-weight: bold;
    }
    footer {
      background: #0e1d34;
      color: #f1c40f;
      text-align: center;
      padding: 15px;
      margin-top: 30px;
    }
  </style>
  <script>
    document.addEventListener('DOMContentLoaded', async () => {
      const verseBox = document.querySelector('.verse-box');
      try {
        const response = await fetch('https://beta.ourmanna.com/api/v1/get/?format=text');
        const verseText = await response.text();
        verseBox.innerHTML = `<strong>Verse of the Day:</strong><br />${verseText}`;
      } catch {
        verseBox.innerHTML += '<br /><small>(Unable to fetch verse of the day right now.)</small>';
      }
    });
  </script>
</head>
<body>
  <header>
    <img src="/mnt/data/WhatsApp Image 2025-08-03 at 01.08.42.jpeg" alt="L'épée Logo">
    <h1>L'épée</h1>
    <p><em>"For the word of God is alive and active... sharper than any double-edged sword."</em> – Hebrews 4:12</p>
  </header>

  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#reflections">Bible Reflections</a>
    <a href="#prayers">Midweek Prayers</a>
    <a href="#involved">Get Involved</a>
    <a href="#contact">Contact</a>
  </nav>

  <section id="home">
    <h2>Welcome to L'épée</h2>
    <div class="verse-box">
      <strong>Verse of the Day:</strong><br />Loading daily scripture...
    </div>
    <p>L'épée is a Christian platform dedicated to strengthening believers through God's Word, prayer times, and Bible reflections. Join us as we explore, share, and grow together in faith.</p>
    <a href="https://chat.whatsapp.com/HiciZCvEhDjIufCKzu1Ijk" target="_blank" class="whatsapp-button">📱 Join our WhatsApp Group</a>
  </section>

  <section id="about">
    <h2>About</h2>
    <p><strong>Mission:</strong> Empowering believers through the living Word of God and creating a space for spiritual growth, prayer, and connection.</p>
  </section>

  <section id="reflections">
    <h2>Bible Reflections</h2>
    <p>Coming soon: weekly devotionals in English to uplift your walk with Christ.</p>
    <p><strong>📖 Bible Study & Reflection Nights:</strong> Fridays from 9 PM – 10 PM on WhatsApp</p>
  </section>

  <section id="prayers">
    <h2>Midweek Prayers</h2>
    <p>Join us every Wednesday from 9 PM – 9:30 PM on WhatsApp for a time of online prayer and reflection.</p>
  </section>

  <section id="involved">
    <h2>Get Involved</h2>
    <p>Want to join a small group, submit a prayer request, or help lead a session? We'd love to hear from you.</p>
  </section>

  <section id="contact">
    <h2>Contact</h2>
    <p>Email: <a href="mailto:contact@lepee.org">contact@lepee.org</a></p>
    <p>Instagram: <a href="https://instagram.com/the_sword" target="_blank">@the_sword</a></p>
    <p>TikTok: <a href="https://www.tiktok.com/@the_sword" target="_blank">@the_sword</a></p>
    <div class="form-container">
      <h3>Prayer Request Form</h3>
      <form action="https://formspree.io/f/mwkdvyzq" method="POST">
        <input type="text" name="name" placeholder="Your Name" required>
        <input type="email" name="email" placeholder="Your Email" required>
        <textarea name="message" rows="5" placeholder="Your Prayer Request" required></textarea>
        <button type="submit">Submit</button>
      </form>
    </div>
  </section>

  <footer>
    <p>&copy; 2025 L'épée. Inspired by Hebrews 4:12 and Ephesians 6:17.</p>
  </footer>
</body>
</html>
