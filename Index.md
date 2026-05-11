<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sydney – Willkommen in Sydney</title>
  <link rel="stylesheet" href="style.css">
</head>
<body id="top">

  <!-- Navigation -->
  <nav class="navbar">
    <div class="nav-container">
      <a href="index.html" class="nav-logo">Sydney <span>&#9728;</span></a>
      <input type="checkbox" id="nav-toggle" class="nav-toggle">
      <label for="nav-toggle" class="nav-toggle-label">
        <span></span><span></span><span></span>
      </label>
      <ul class="nav-links">
        <li><a href="index.html" class="active">Start</a></li>
        <li>
          <a href="orte.html">Entdecken &#9662;</a>
          <ul class="dropdown-menu">
            <li><a href="orte.html">Sch&ouml;ne Orte</a></li>
            <li><a href="geschichte.html">Geschichte</a></li>
          </ul>
        </li>
        <li>
          <a href="infrastruktur.html">Praktisches &#9662;</a>
          <ul class="dropdown-menu">
            <li><a href="infrastruktur.html">Infrastruktur &amp; Anreise</a></li>
            <li><a href="wirtschaft.html">Wirtschaft</a></li>
          </ul>
        </li>
        <li><a href="buchen.html">Buchen</a></li>
        <li><a href="impressum.html">Impressum</a></li>
      </ul>
    </div>
  </nav>

  <!-- Hero -->
  <section class="hero">
    <img src="https://www.merian.de/uploads/media/jalag-content-image/04/14324-dan-freeman-unsplash-sydney-opera-house.jpg?v=1-0" alt="Sydney Opera House und Hafen" class="hero-img">
    <div class="hero-overlay"></div>
    <div class="hero-content">
      <h1>Willkommen in Sydney</h1>
      <p>Strahlender Himmel, endlose Str&auml;nde und eine Stadt, die Lebensgef&uuml;hl atmet. Entdecke eine der sch&ouml;nsten Metropolen der Welt.</p>
      <a href="orte.html" class="btn btn-primary">Jetzt entdecken</a>
    </div>
  </section>

  <!-- Intro -->
  <section class="section intro">
    <div class="section-container">
      <div class="intro-text">
        <p>Sydney, die gr&ouml;&szlig;te Stadt Australiens, verbindet auf einzigartige Weise pulsierendes Stadtleben mit entspannter Natur. Ob das ikonische Opernhaus, der ber&uuml;hmte Bondi Beach oder die historischen Gassen von The Rocks &ndash; Sydney bietet f&uuml;r jeden Reisenden unvergessliche Erlebnisse. Tauche ein in eine Stadt, die niemals schlaft und doch immer entspannt bleibt.</p>
      </div>
    </div>
  </section>

  <!-- Teaser Cards -->
  <section class="section section-alt">
    <div class="section-container">
      <div class="section-header">
        <h2>Dein Sydney-Abenteuer</h2>
        <p>Entdecke die Vielfalt dieser faszinierenden Stadt</p>
      </div>
      <div class="teaser-grid">
        <div class="teaser-card">
          <img src="https://media.architecturaldigest.com/photos/63d82d299dd44a3242d15ade/3:2/w_3000,h_2000,c_limit/GettyImages-982774858.jpg" alt="Sydney Opera House">
          <div class="teaser-card-body">
            <h3>Sch&ouml;ne Orte</h3>
            <p>Vom Opernhaus bis zu den Blue Mountains &ndash; die sch&ouml;nsten Sehensw&uuml;rdigkeiten Sydneys.</p>
            <a href="orte.html" class="btn btn-secondary">Orte entdecken</a>
          </div>
        </div>
        <div class="teaser-card">
          <img src="https://travel.usnews.com/images/Sydney_Harbour_Bridge_sunrise_seng_chye_teo_Getty.jpg" alt="Sydney Harbour Bridge">
          <div class="teaser-card-body">
            <h3>Geschichte</h3>
            <p>Von den Aborigines bis zur modernen Metropole &ndash; die faszinierende Geschichte Australiens.</p>
            <a href="geschichte.html" class="btn btn-secondary">Geschichte lesen</a>
          </div>
        </div>
        <div class="teaser-card">
          <img src="https://images.unsplash.com/photo-1546412414-e1885259563a?w=800&q=80" alt="Bondi Beach">
          <div class="teaser-card-body">
            <h3>Jetzt buchen</h3>
            <p>Plane deine Reise nach Sydney &ndash; unverbindlich anfragen und Traumurlaub starten.</p>
            <a href="buchen.html" class="btn btn-primary">Anfrage senden</a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="footer">
    <div class="footer-grid">
      <div class="footer-col">
        <h4>Seiten</h4>
        <ul>
          <li><a href="index.html">Start</a></li>
          <li><a href="orte.html">Sch&ouml;ne Orte</a></li>
          <li><a href="geschichte.html">Geschichte</a></li>
          <li><a href="infrastruktur.html">Infrastruktur</a></li>
          <li><a href="wirtschaft.html">Wirtschaft</a></li>
        </ul>
      </div>
      <div class="footer-brand">
        <div class="footer-logo">Sydney <span>&#9728;</span></div>
        <p>Dein Reisef&uuml;hrer f&uuml;r Sydney</p>
        <div class="social-icons">
          <a href="#" aria-label="Instagram">&#9741;</a>
          <a href="#" aria-label="Facebook">&#9733;</a>
          <a href="#" aria-label="YouTube">&#9654;</a>
        </div>
      </div>
      <div class="footer-col">
        <h4>Rechtliches</h4>
        <ul>
          <li><a href="buchen.html">Buchung</a></li>
          <li><a href="impressum.html">Impressum</a></li>
          <li><a href="impressum.html">Datenschutz</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">
      Diese Website wurde zu schulischen Zwecken erstellt. Alle Inhalte dienen ausschlie&szlig;lich der Bildung. &copy; 2024 &ndash; Schulprojekt
    </div>
  </footer>

  <!-- Back to Top -->
  <a href="#top" class="back-to-top" aria-label="Nach oben">&#8593;</a>

</body>
</html>
