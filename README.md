<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>IonAfrica Foundation – Discover Africa’s Flags</title>
<style>
  body {
    font-family: 'Poppins', sans-serif;
    margin: 0;
    background: #fdf6ec;
    color: #222;
    line-height: 1.6;
  }
  header {
    background: linear-gradient(90deg, #00853f, #fcd116, #e8112d);
    color: white;
    text-align: center;
    padding: 2rem 1rem;
  }
  header h1 { margin: 0; font-size: 2rem; }
  nav {
    background: #333;
    display: flex;
    justify-content: center;
    gap: 1.5rem;
    padding: 0.8rem;
  }
  nav a {
    color: white;
    text-decoration: none;
    font-weight: bold;
  }
  section { padding: 40px 20px; text-align: center; }
  img.qr {
    max-width: 250px;
    border-radius: 10px;
    box-shadow: 0 5px 10px rgba(0,0,0,0.2);
  }
  footer {
    background: #333;
    color: white;
    padding: 20px;
    font-size: 0.9rem;
  }
  button.lang {
    background: white;
    color: #333;
    border: none;
    margin: 0 5px;
    padding: 5px 10px;
    border-radius: 5px;
    cursor: pointer;
  }
</style>
</head>
<body>
  <header>
    <h1>IonAfrica Foundation</h1>
    <p id="subtitle">Celebrating Africa’s flags, cultures, and stories.</p>
    <div>
      <button class="lang" onclick="setLang('en')">EN</button>
      <button class="lang" onclick="setLang('fr')">FR</button>
    </div>
  </header>

  <section>
    <h2 id="mission-title">Our Mission</h2>
    <p id="mission-text">
      We showcase every African country’s flag. Each flag links to a page with fun facts and cultural insights.
    </p>
  </section>

  <section id="donate">
    <h2 id="donate-title">Support IonAfrica Foundation</h2>
    <p id="donate-text">
      Your donation helps us celebrate Africa’s cultures and stories. Every contribution counts!
    </p>
    <img class="qr" src="2435c8ad-29eb-40f1-ad9f-b8d79a6c4d2c.JPG" alt="PayPal Donate QR - IonAfrica">
    <p><strong id="scan-text">Scan. Pay. Go.</strong></p>
    <p><a href="https://www.paypal.com/donate" target="_blank">Donate via PayPal</a></p>
  </section>

  <footer>
    <p>&copy; 2025 IonAfrica Foundation</p>
  </footer>

<script>
function setLang(lang){
  const en = {
    subtitle: "Celebrating Africa’s flags, cultures, and stories.",
    mission_title: "Our Mission",
    mission_text: "We showcase every African country’s flag. Each flag links to a page with fun facts and cultural insights.",
    donate_title: "Support IonAfrica Foundation",
    donate_text: "Your donation helps us celebrate Africa’s cultures and stories. Every contribution counts!",
    scan_text: "Scan. Pay. Go."
  };
  const fr = {
    subtitle: "Célébrer les drapeaux, les cultures et les histoires de l’Afrique.",
    mission_title: "Notre Mission",
    mission_text: "Nous présentons le drapeau de chaque pays africain, avec des faits amusants et des aperçus culturels.",
    donate_title: "Soutenez la Fondation IonAfrica",
    donate_text: "Votre don nous aide à célébrer les cultures et les histoires de l’Afrique. Chaque contribution compte !",
    scan_text: "Scannez. Payez. C’est tout."
  };
  const dict = lang === 'fr' ? fr : en;
  for(const id in dict){ document.getElementById(id.replace('_','-')).textContent = dict[id]; }
}
</script>
</body>
</html>
