
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Telephone Pole</title>
  <link rel="icon" href="https://f4.bcbits.com/img/0040578065_25.jpg" type="image/x-icon">

  <!-- Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Patrick+Hand&family=American+Typewriter&display=swap" rel="stylesheet" />
  <style>
    body {
      margin: 0;
      background-color: #fffaea;
      color: #000;
      font-family: "american-typewriter", serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
    }

    /* Sticky nav bar */
    header {
      position: sticky;
      top: 0;
      background-color: #fffaea;
      padding: 1em 0;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.25);
      z-index: 1000;
    }

    nav {
      max-width: 980px;
      margin: 0 auto;
      padding: 0 1em;
      display: flex;
      gap: 2rem;
      font-family: "patrick hand", cursive;
      font-size: 1.3rem;
    }

    /* ... nav button styles same as before ... */
    nav a.home {
      color: #0a74f2;
    }

    nav a.home:hover,
    nav a.home:focus {
      background-color: rgba(0, 87, 225, 0.36);
      border: 1px dashed #0057e1;
      color: #fffaea;
      outline: none;
    }

    nav a.find {
      color: #13dc69;
    }

    nav a.find:hover,
    nav a.find:focus {
      background-color: rgba(19, 220, 105, 0.36);
      border: 1px dashed #0057e1;
      color: #fff;
      outline: none;
    }

    nav a.records {
      color: #dc132a;
    }

    nav a.records:hover,
    nav a.records:focus {
      background-color: rgba(220, 19, 42, 0.36);
      border: 1px dashed #0057e1;
      color: #fff;
      outline: none;
    }

    nav a.shows {
      color: #dc9113;
    }

    nav a.shows:hover,
    nav a.shows:focus {
      background-color: rgba(220, 145, 19, 0.36);
      border: 1px dashed #0057e1;
      color: #fff;
      outline: none;
    }

    main {
      max-width: 980px;
      margin: 3rem auto 5rem;
      padding: 0 1em;
    }

    @font-face {
      font-family: 'rosewood-w01-regular';
      src: url('https://static.parastorage.com/fonts/v2/f731409f-b163-424d-a1ab-3d3cd7ef1d26/v1/rosewood-w08-regular.woff2') format('woff2');
      font-weight: normal;
      font-style: normal;
      font-display: swap;
    }

    h1.band-name {
      font-family: "rosewood-w01-regular", cursive, serif;
      font-weight: normal;
      font-size: 7rem;
      text-align: center;
      margin: 0 0 2rem 0;
      user-select: none;
      text-shadow:
        1px 1px 0 #bfbfbf,
        2px 2px 0 #dfdfdf;
      padding-top: 60px;
      padding-bottom: 60px;
    }

    .section {
      position: relative;
      padding: 80px 1em 100px;
      margin: 0 auto;
      max-width: 980px;
      box-sizing: border-box;
    }

    /* Add checkered border: use linear-gradient repeating pattern */
    .section + .divider {
      width: 100%;
      height: 16px;
      background:
        repeating-linear-gradient(
          45deg,
          #000 0,
          #000 4px,
          #fff 4px,
          #fff 8px,
          #000 8px,
          #000 12px,
          #fff 12px,
          #fff 16px
        );
      margin: 0 auto;
      max-width: 980px;
    }
    
    .divider {
  width: 100%;
  height: 16px;
  background:
    repeating-linear-gradient(
      45deg,
      #000 0,
      #000 4px,
      #fff 4px,
      #fff 8px,
      #000 8px,
      #000 12px,
      #fff 12px,
      #fff 16px
    );
  margin: 0 auto 2rem auto;
  max-width: 980px;
}

    section.about {
      font-size: 1.2rem;
      font-family: "americantypwrteritcw01--731025", serif, Georgia, serif;
      line-height: 1.6;
      letter-spacing: 0.02em;
      color: #000;
      text-align: center;
    }

    section.about a {
      color: #000;
      text-decoration: underline;
    }

    /* Social Links Section with retro colors */
    section.social-links {
      display: flex;
      justify-content: center;
      gap: 1rem;
      flex-wrap: wrap;
    }

    section.social-links a {
      font-family: "patrick hand", cursive;
      font-size: 1.25rem;
      text-decoration: underline;
      cursor: pointer;
      user-select: none;
      padding: 8px 18px;
      border-radius: 5px;
      border: 1px dashed transparent;
      transition: background-color 0.3s ease, border-color 0.3s ease, color 0.3s ease;
      min-width: 80px;
      text-align: center;
      font-weight: 400;
    }

    /* Retro button colors */
    a.bandcamp {
      color: #f22fd9;
    }

    a.bandcamp:hover,
    a.bandcamp:focus {
      background-color: rgba(0, 87, 225, 0.36);
      border-color: #0057e1;
      color: #f22fd9;
      outline: none;
      letter-spacing: 0.1em;
    }

    a.instagram {
      color: #ff7100;
    }

    a.instagram:hover,
    a.instagram:focus {
      background-color: rgba(19, 220, 105, 0.36);
      border-color: #0057e1;
      color: #ff7100;
      outline: none;
      letter-spacing: 0.1em;
    }

    a.email {
      color: #00ffef;
    }

    a.email:hover,
    a.email:focus {
      background-color: rgba(220, 19, 42, 0.36);
      border-color: #0057e1;
      color: #00ffef;
      outline: none;
      letter-spacing: 0.1em;
    }

    a.youtube {
      color: #460089;
    }

    a.youtube:hover,
    a.youtube:focus {
      background-color: rgba(220, 145, 19, 0.36);
      border-color: #0057e1;
      color: #460089;
      outline: none;
      letter-spacing: 0.1em;
    }

    /* Records section with hover zoom and border */
    section.records {
      display: flex;
      justify-content: center;
      gap: 3rem;
      max-width: 980px;
      margin: 0 auto;
    }

    a.record-link {
      width: 250;
      height: 250;
      display: block;
      overflow: hidden;
      border: 5px solid transparent;
      border-radius: 6px;
      box-shadow: 0 3px 7px rgba(0, 0, 0, 0.15);
      cursor: pointer;
      transition: border-color 0.3s ease, transform 0.3s ease;
      position: relative;
    }

    a.record-link img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.3s ease;
      user-select: none;
      pointer-events: none;
    }

    a.record-link:hover,
    a.record-link:focus {
      border-color: #0057e1;
      outline: none;
      transform: scale(1.1);
      z-index: 10;
    }

    a.record-link:hover img,
    a.record-link:focus img {
      transform: scale(1.15);
    }

    /* Shows heading */
    #shows h2.shows-header {
      font-family: "ccprimalscream", fantasy, cursive, serif;
      font-size: 6rem;
      font-weight: normal;
      letter-spacing: 0.01em;
      margin-bottom: 1rem;
      text-shadow:
        1px 1px 0 #c8c8c8,
        0 2px 0 #b4b4b4,
        0 3px 0 #a0a0a0,
        0 4px 0 rgba(140, 140, 140, 0.5),
        0 5px 10px rgba(0, 0, 0, 0.5);
      user-select: none;
      text-align: center;
    margin-top: -25px;
      padding-bottom: 60px;
    }

    footer {
      text-align: center;
      font-family: "americantypwrteritcw01--731025", serif;
      font-weight: normal;
      font-size: 1rem;
      color: #595959;
      margin: 4rem 0 2rem;
    }

    /* Smooth scroll anchor */
    html {
      scroll-behavior: smooth;
    }

    @media (max-width: 600px) {
      h1.band-name {
        font-size: 3.5rem;
      }

      #shows h2.shows-header {
        font-size: 3.5rem;
      }

      nav {
        font-size: 1rem;
        justify-content: space-around;
      }

      section.records {
        gap: 1rem;
        flex-wrap: wrap;
      }

      a.record-link {
        width: 120px;
        height: 120px;
      }

      a.record-link img {
        height: 120px;
      }

      section.about,
      section.social-links a {
        font-size: 1rem;
      }
    }
  </style>
</head>

<body>

  <header>
    <nav aria-label="Primary navigation">
      <a href="#home" class="home" tabindex="0">home</a>
      <a href="#find-us" class="find" tabindex="0">find us</a>
      <a href="#records" class="records" tabindex="0">records</a>
      <a href="#shows" class="shows" tabindex="0">shows</a>
    </nav>
  </header>


  <main> 
  
    <div class="divider"></div>
  
    <section id="home" class="section">
      <h1 class="band-name">Telephone Pole</h1>
    </section>

    <div class="divider"></div>

    <section id="find-us" class="section about" tabindex="-1" aria-label="About Telephone Pole">
      <p>telephone pole is a band from athens, ga. thanks for checking us out and supporting!</p>
      <p>also, <a href="mailto:telephonepole25@gmail.com" aria-label="Email Telephone Pole">reach out</a> so we can come to your town.</p>
    </section>

    <div class="divider"></div>

    <section class="section social-links" aria-label="Online Platforms">
      <a href="https://telephonepole.bandcamp.com/" target="_blank" rel="noopener" aria-label="Bandcamp" class="bandcamp">bandcamp</a>
      <a href="https://www.instagram.com/telephonepoleband/" target="_blank" rel="noopener" aria-label="Instagram" class="instagram">instagram</a>
      <a href="mailto:telephonepole25@gmail.com" aria-label="Email" class="email">email</a>
      <a href="https://www.youtube.com/@TelephonePoleAthens" target="_blank" rel="noopener" aria-label="YouTube" class="youtube">youtube</a>
    </section>

    <div class="divider"></div>

    <section id="records" class="section records" aria-label="Records">
      <a href="https://telephonepole.bandcamp.com/album/you-get-so-alone-at-times-that-it-just-makes-sense" target="_blank" rel="noopener noreferrer" class="record-link" aria-label="You Get So Alone At Times That It Just Makes Sense">
        <img src="https://static.wixstatic.com/media/3445dc_b303c262cf6a4633be5a8cbbcdc166e6~mv2.jpg" alt="You Get So Alone At Times That It Just Makes Sense album cover" />
      </a>
      <a href="https://telephonepole.bandcamp.com/track/bipolar" target="_blank" rel="noopener noreferrer" class="record-link" aria-label="Bipolar">
        <img src="https://static.wixstatic.com/media/3445dc_7910a68575ee4a73849d6008495fc8ed~mv2.jpg" alt="Bipolar album cover" />
      </a>
    </section>

    <div class="divider"></div>
    
    <section id="shows" tabindex="-1" aria-label="Shows and Events" class="section">
      <h2 class="shows-header">Shows</h2>
      <script src="https://widgetv3.bandsintown.com/main.min.js"></script>
      <div class="bit-widget-initializer" data-artist-name="Telephone Pole" data-display-limit="15" data-display-details="true" data-language="en" style="max-width: 980px; margin: auto;"></div>
    </section>
  </main>

  <footer>
    <p>Copyright Telephone Pole 2026</p>
  </footer>

</body>

</html>
