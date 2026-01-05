<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <meta name="description" content="Her Handy Pro — professional home repairs, maintenance, and upgrades. Woman-owned. Reliable. Skilled. Licensed & insured." />
  <title>Her Handy Pro | Professional Home Services</title>

  <!-- Open Graph -->
  <meta property="og:title" content="Her Handy Pro | Professional Home Services" />
  <meta property="og:description" content="Professional home repairs, maintenance, and upgrades. Woman-owned. Reliable. Skilled. Licensed & insured." />
  <meta property="og:type" content="website" />
  <meta property="og:image" content="assets/og-image.jpg" />

  <!-- Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@500;600;700&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">

  <style>
    :root{
      /* Brand-ish palette (adjust to match your exact logo) */
      --charcoal:#2f3238;
      --ink:#1f232a;
      --rose:#c98f94;
      --rose-dark:#b77a80;
      --gray:#6b7280;
      --bg:#fbfbfc;
      --card:#ffffff;
      --line:rgba(31,35,42,.10);
      --shadow:0 12px 28px rgba(17,24,39,.10);
      --radius:18px;
      --max:1100px;
    }

    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0;
      font-family:Inter, system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
      color:var(--ink);
      background:linear-gradient(180deg, #fff 0%, var(--bg) 100%);
      line-height:1.55;
    }
    a{color:inherit; text-decoration:none}
    img{max-width:100%; display:block}

    /* Layout helpers */
    .wrap{max-width:var(--max); margin:0 auto; padding:0 20px;}
    .section{padding:72px 0}
    .grid{display:grid; gap:18px}
    .two{grid-template-columns:repeat(2, minmax(0,1fr))}
    .three{grid-template-columns:repeat(3, minmax(0,1fr))}
    @media (max-width:900px){ .two,.three{grid-template-columns:1fr} }

    /* Top bar */
    .topbar{
      position:sticky; top:0; z-index:50;
      background:rgba(255,255,255,.85);
      backdrop-filter:saturate(180%) blur(12px);
      border-bottom:1px solid var(--line);
    }
    .nav{
      display:flex; align-items:center; justify-content:space-between;
      padding:14px 0;
      gap:16px;
    }
    .brand{
      display:flex; align-items:center; gap:12px;
      font-family:Montserrat, sans-serif;
      font-weight:700; letter-spacing:.2px;
    }
    .brand small{display:block; font-weight:600; color:var(--gray); letter-spacing:.1px}
    .logo{
      width:44px; height:44px; border-radius:12px;
      background:#fff;
      border:1px solid var(--line);
      box-shadow:0 6px 18px rgba(17,24,39,.08);
      overflow:hidden;
    }
    .logo img{width:100%; height:100%; object-fit:contain; padding:6px;}
    .links{display:flex; gap:18px; align-items:center}
    .links a{font-weight:600; color:rgba(31,35,42,.85)}
    .links a:hover{color:var(--ink)}
    @media (max-width:900px){
      .links{display:none}
    }

    /* Buttons */
    .btn{
      display:inline-flex; align-items:center; justify-content:center;
      padding:12px 16px;
      border-radius:14px;
      border:1px solid var(--line);
      background:#fff;
      font-weight:700;
      box-shadow:0 10px 22px rgba(17,24,39,.08);
      transition:transform .12s ease, box-shadow .12s ease, border-color .12s ease;
      cursor:pointer;
    }
    .btn:hover{transform:translateY(-1px); box-shadow:0 14px 28px rgba(17,24,39,.12); border-color:rgba(31,35,42,.18)}
    .btn.primary{
      background:linear-gradient(180deg, var(--rose) 0%, var(--rose-dark) 100%);
      color:#fff; border-color:rgba(0,0,0,.08);
    }
    .btn.primary:hover{border-color:rgba(255,255,255,.25)}
    .btn.ghost{background:transparent}
    .btn-row{display:flex; gap:12px; flex-wrap:wrap}

    /* Hero */
    .hero{
      padding:64px 0 26px;
      position:relative;
    }
    .hero-card{
      border:1px solid var(--line);
      background:radial-gradient(1200px 500px at 20% 0%, rgba(201,143,148,.18), transparent 55%),
                 radial-gradient(900px 460px at 90% 10%, rgba(47,50,56,.08), transparent 55%),
                 #fff;
      border-radius:28px;
      box-shadow:var(--shadow);
      overflow:hidden;
    }
    .hero-inner{
      display:grid;
      grid-template-columns:1.2fr .8fr;
      gap:18px;
      padding:34px;
      align-items:center;
    }
    @media (max-width:900px){
      .hero-inner{grid-template-columns:1fr; padding:24px}
    }
    h1{
      font-family:Montserrat, sans-serif;
      font-size:clamp(34px, 3.6vw, 52px);
      line-height:1.08;
      margin:0 0 10px;
      letter-spacing:-.6px;
    }
    .sub{
      font-size:18px;
      color:rgba(31,35,42,.78);
      margin:0 0 18px;
      max-width:54ch;
    }
    .pillbar{
      display:flex; flex-wrap:wrap; gap:10px;
      margin-top:18px;
    }
    .pill{
      padding:8px 10px;
      border-radius:999px;
      border:1px solid var(--line);
      background:rgba(255,255,255,.9);
      font-weight:700;
      color:rgba(31,35,42,.78);
      font-size:13px;
    }
    .hero-aside{
      border-left:1px solid var(--line);
      padding-left:22px;
    }
    @media (max-width:900px){
      .hero-aside{border-left:none; padding-left:0; border-top:1px solid var(--line); padding-top:18px}
    }
    .aside-card{
      background:rgba(255,255,255,.7);
      border:1px solid var(--line);
      border-radius:20px;
      padding:18px;
    }
    .aside-title{
      font-family:Montserrat, sans-serif;
      font-weight:800;
      margin:0 0 6px;
      letter-spacing:-.2px;
    }
    .aside-text{margin:0 0 14px; color:rgba(31,35,42,.72)}
    .mini{
      display:grid; gap:10px; margin-top:12px;
    }
    .mini div{
      display:flex; justify-content:space-between; align-items:center;
      padding:10px 12px;
      background:#fff;
      border:1px solid var(--line);
      border-radius:14px;
      font-weight:700;
    }
    .mini span{color:rgba(31,35,42,.72); font-weight:700}

    /* Section headers */
    .kicker{
      color:var(--rose-dark);
      font-weight:800;
      letter-spacing:.12em;
      text-transform:uppercase;
      font-size:12px;
      margin:0 0 10px;
    }
    h2{
      font-family:Montserrat, sans-serif;
      font-size:28px;
      margin:0 0 10px;
      letter-spacing:-.3px;
    }
    .lead{color:rgba(31,35,42,.72); margin:0; max-width:75ch}

    /* Cards */
    .card{
      background:var(--card);
      border:1px solid var(--line);
      border-radius:var(--radius);
      padding:18px;
      box-shadow:0 10px 20px rgba(17,24,39,.06);
    }
    .card h3{
      font-family:Montserrat, sans-serif;
      margin:0 0 6px;
      font-size:18px;
      letter-spacing:-.2px;
    }
    .card p{margin:0; color:rgba(31,35,42,.72)}
    .card ul{margin:12px 0 0; padding-left:18px; color:rgba(31,35,42,.72)}
    .card li{margin:6px 0}

    /* Testimonials */
    .quote{
      font-size:16px;
      margin:0 0 10px;
      color:rgba(31,35,42,.80);
    }
    .who{font-weight:800; color:rgba(31,35,42,.75)}
    .stars{color:var(--rose-dark); letter-spacing:.18em; font-weight:900}

    /* Contact */
    .contact{
      background:linear-gradient(180deg, rgba(201,143,148,.10) 0%, rgba(255,255,255,1) 70%);
      border-top:1px solid var(--line);
    }
    form{
      display:grid; gap:12px;
    }
    label{font-weight:800; font-size:13px; color:rgba(31,35,42,.78)}
    input, textarea, select{
      width:100%;
      padding:12px 12px;
      border-radius:14px;
      border:1px solid rgba(31,35,42,.18);
      background:#fff;
      font:inherit;
      outline:none;
    }
    input:focus, textarea:focus, select:focus{
      border-color:rgba(183,122,128,.75);
      box-shadow:0 0 0 4px rgba(201,143,148,.18);
    }
    textarea{min-height:120px; resize:vertical}
    .fine{font-size:13px; color:rgba(31,35,42,.65); margin:0}
    .footer{
      padding:28px 0;
      border-top:1px solid var(--line);
      color:rgba(31,35,42,.68);
      font-size:13px;
    }
    .footer-row{
      display:flex; justify-content:space-between; gap:12px; flex-wrap:wrap
    }

    /* Mobile menu (simple) */
    .menu-btn{display:none}
    @media (max-width:900px){
      .menu-btn{display:inline-flex}
      .mobile-links{
        display:none;
        border-top:1px solid var(--line);
        padding:10px 0 14px;
      }
      .mobile-links a{
        display:block;
        padding:10px 0;
        font-weight:800;
        color:rgba(31,35,42,.85);
      }
      .mobile-links.show{display:block}
    }
  </style>
</head>

<body>
  <!-- Topbar -->
  <div class="topbar">
    <div class="wrap">
      <div class="nav">
        <a class="brand" href="#top">
          <div class="logo" aria-hidden="true">
            <!-- Replace with your logo file -->
            <img src="assets/logo.png" alt="Her Handy Pro logo" />
          </div>
          <div>
            Her Handy Pro
            <small>Professional Home Services</small>
          </div>
        </a>

        <div class="links" aria-label="Primary navigation">
          <a href="#services">Services</a>
          <a href="#why">Why Us</a>
          <a href="#about">About</a>
          <a href="#reviews">Reviews</a>
          <a href="#contact">Contact</a>
        </div>

        <div class="btn-row">
          <a class="btn ghost" href="tel:+1-000-000-0000">Call</a>
          <a class="btn primary" href="#contact">Request a Quote</a>
          <button class="btn menu-btn" id="menuBtn" type="button" aria-expanded="false" aria-controls="mobileLinks">
            Menu
          </button>
        </div>
      </div>

      <div class="mobile-links" id="mobileLinks">
        <a href="#services">Services</a>
        <a href="#why">Why Us</a>
        <a href="#about">About</a>
        <a href="#reviews">Reviews</a>
        <a href="#contact">Contact</a>
      </div>
    </div>
  </div>

  <!-- Hero -->
  <main id="top" class="hero">
    <div class="wrap">
      <div class="hero-card">
        <div class="hero-inner">
          <div>
            <p class="kicker">Woman-Owned • Residential Focused</p>
            <h1>Professional Home Repairs.<br>Done Right.</h1>
            <p class="sub">
              Reliable repairs, preventative maintenance, and practical home upgrades—delivered with skill,
              clear communication, and respect for your home.
            </p>

            <div class="btn-row">
              <a class="btn primary" href="#contact">Schedule Service</a>
              <a class="btn" href="#services">View Services</a>
            </div>

            <div class="pillbar" aria-label="Trust highlights">
              <span class="pill">Licensed &amp; Insured</span>
              <span class="pill">On-Time &amp; Detail-Driven</span>
              <span class="pill">Transparent Pricing</span>
              <span class="pill">Clean, Respectful Service</span>
            </div>
          </div>

          <aside class="hero-aside">
            <div class="aside-card">
              <p class="aside-title">Service Area</p>
              <p class="aside-text">
                Serving <strong>[Your City/County]</strong> and surrounding areas.
                Same-week appointments available based on scope.
              </p>

              <div class="mini">
                <div><span>Response Time</span> 24–48 hrs</div>
                <div><span>Hours</span> Mon–Sat</div>
                <div><span>Estimates</span> Clear + Written</div>
              </div>

              <div class="btn-row" style="margin-top:14px">
                <a class="btn" href="tel:+1-000-000-0000">Call: (000) 000-0000</a>
              </div>

              <p class="fine" style="margin-top:10px">
                Emergency service: <strong>[Yes/No]</strong> • Weekend availability: <strong>[Yes/No]</strong>
              </p>
            </div>
          </aside>
        </div>
      </div>
    </div>
  </main>

  <!-- Services -->
  <section id="services" class="section">
    <div class="wrap">
      <p class="kicker">Services</p>
      <h2>Home Services Built on Trust</h2>
      <p class="lead">
        From everyday repairs to home refresh projects, we bring professionalism, preparation, and quality workmanship to every job.
      </p>

      <div class="grid three" style="margin-top:18px">
        <div class="card">
          <h3>General Home Repairs</h3>
          <p>Everyday fixes handled correctly the first time.</p>
          <ul>
            <li>Drywall repair &amp; patching</li>
            <li>Door locks, hardware, hinges</li>
            <li>Mounting (TVs, art, shelves)</li>
            <li>Minor carpentry and adjustments</li>
          </ul>
        </div>

        <div class="card">
          <h3>Home Maintenance</h3>
          <p>Prevent problems, extend the life of your home.</p>
          <ul>
            <li>Caulking &amp; sealing</li>
            <li>Weatherproofing</li>
            <li>Fixture replacements</li>
            <li>Punch lists for homeowners &amp; landlords</li>
          </ul>
        </div>

        <div class="card">
          <h3>Upgrades &amp; Improvements</h3>
          <p>Practical upgrades that elevate comfort and function.</p>
          <ul>
            <li>Trim and molding</li>
            <li>Accent walls &amp; small refreshes</li>
            <li>Smart home installs</li>
            <li>Pre-sale refresh services</li>
          </ul>
        </div>
      </div>

      <div class="btn-row" style="margin-top:18px">
        <a class="btn primary" href="#contact">Request a Quote</a>
        <a class="btn" href="#about">Learn About Our Standards</a>
      </div>
    </div>
  </section>

  <!-- Why Us -->
  <section id="why" class="section" style="padding-top:0">
    <div class="wrap">
      <div class="grid two">
        <div class="card">
          <p class="kicker">Why Us</p>
          <h2 style="margin-top:0">A Better In-Home Service Experience</h2>
          <p class="lead" style="margin-top:10px">
            Her Handy Pro was built on a simple idea: homeowners deserve dependable workmanship and a respectful, professional experience.
          </p>
          <div class="grid" style="margin-top:14px">
            <div class="card" style="box-shadow:none">
              <h3>Professional &amp; Prepared</h3>
              <p>We arrive ready, communicate clearly, and complete work to a high standard—no guesswork.</p>
            </div>
            <div class="card" style="box-shadow:none">
              <h3>Transparent Pricing</h3>
              <p>Written estimates and clear scope. You’ll understand what’s being done and why.</p>
            </div>
            <div class="card" style="box-shadow:none">
              <h3>Respect &amp; Cleanliness</h3>
              <p>We protect your space, clean up thoroughly, and treat your home like it matters—because it does.</p>
            </div>
          </div>
        </div>

        <div class="card">
          <p class="kicker">How It Works</p>
          <h2 style="margin-top:0">Simple, Clear, Efficient</h2>
          <div class="grid" style="margin-top:14px">
            <div class="card" style="box-shadow:none">
              <h3>1) Request</h3>
              <p>Tell us what you need using the form below (photos help).</p>
            </div>
            <div class="card" style="box-shadow:none">
              <h3>2) Estimate</h3>
              <p>We confirm scope and provide a clear written estimate.</p>
            </div>
            <div class="card" style="box-shadow:none">
              <h3>3) Complete</h3>
              <p>We complete the work professionally—clean, on-time, and done right.</p>
            </div>
          </div>

          <div class="btn-row" style="margin-top:16px">
            <a class="btn primary" href="#contact">Schedule Now</a>
            <a class="btn" href="tel:+1-000-000-0000">Call</a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- About -->
  <section id="about" class="section">
    <div class="wrap">
      <p class="kicker">About</p>
      <h2>Her Handy Pro</h2>
      <p class="lead">
        Her Handy Pro was founded to bring professionalism, care, and confidence back into home services.
        We believe expertise has no gender—only standards. And ours are high.
      </p>

      <div class="grid two" style="margin-top:18px">
        <div class="card">
          <h3>Mission</h3>
          <p>
            To provide dependable, professional home services while creating a respectful and comfortable experience for every client we serve.
          </p>
        </div>
        <div class="card">
          <h3>Values</h3>
          <ul>
            <li><strong>Trust First:</strong> We treat every home like our own.</li>
            <li><strong>Professional Excellence:</strong> Skilled, prepared, accountable.</li>
            <li><strong>Respect &amp; Safety:</strong> Your comfort matters—always.</li>
            <li><strong>Clear Communication:</strong> No ambiguity, no surprises.</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- Reviews -->
  <section id="reviews" class="section" style="padding-top:0">
    <div class="wrap">
      <p class="kicker">Reviews</p>
      <h2>What Clients Say</h2>
      <p class="lead">Replace these placeholders with real Google/Yelp reviews as you receive them.</p>

      <div class="grid three" style="margin-top:18px">
        <div class="card">
          <div class="stars">★★★★★</div>
          <p class="quote">“Professional, reliable, and extremely thorough. Communication was clear and the work was done right.”</p>
          <div class="who">— Homeowner</div>
        </div>
        <div class="card">
          <div class="stars">★★★★★</div>
          <p class="quote">“On time, respectful, and left everything spotless. I finally found someone I can trust in my home.”</p>
          <div class="who">— Client</div>
        </div>
        <div class="card">
          <div class="stars">★★★★★</div>
          <p class="quote">“Great workmanship and transparent pricing. Exactly what home services should feel like.”</p>
          <div class="who">— Resident</div>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="section contact">
    <div class="wrap">
      <p class="kicker">Contact</p>
      <h2>Request a Quote</h2>
      <p class="lead">Share a few details and we’ll respond within 24–48 hours.</p>

      <div class="grid two" style="margin-top:18px">
        <div class="card">
          <form id="quoteForm">
            <div>
              <label for="name">Full Name</label>
              <input id="name" name="name" autocomplete="name" required />
            </div>

            <div class="grid two">
              <div>
                <label for="phone">Phone</label>
                <input id="phone" name="phone" autocomplete="tel" required />
              </div>
              <div>
                <label for="email">Email</label>
                <input id="email" name="email" type="email" autocomplete="email" required />
              </div>
            </div>

            <div class="grid two">
              <div>
                <label for="service">Service Type</label>
                <select id="service" name="service" required>
                  <option value="" selected disabled>Select one</option>
                  <option>General Home Repairs</option>
                  <option>Home Maintenance</option>
                  <option>Upgrades & Improvements</option>
                  <option>Property Manager / Punch List</option>
                  <option>Other</option>
                </select>
              </div>
              <div>
                <label for="timing">Desired Timing</label>
                <select id="timing" name="timing" required>
                  <option value="" selected disabled>Select one</option>
                  <option>ASAP</option>
                  <option>This week</option>
                  <option>Next 1–2 weeks</option>
                  <option>Flexible</option>
                </select>
              </div>
            </div>

            <div>
              <label for="details">Project Details</label>
              <textarea id="details" name="details" placeholder="Describe what you need. Include measurements, photos, or links if available."></textarea>
            </div>

            <div class="btn-row">
              <button class="btn primary" type="submit">Send Request</button>
              <a class="btn" href="tel:+1-000-000-0000">Call Instead</a>
            </div>

            <p class="fine">
              By submitting, you agree to be contacted by phone/email. We do not sell your information.
            </p>
          </form>
        </div>

        <div class="card">
          <h3>Business Info</h3>
          <p style="color:rgba(31,35,42,.72); margin:0 0 14px">
            Update the details below with your real contact information.
          </p>

          <div class="mini">
            <div><span>Phone</span> (000) 000-0000</div>
            <div><span>Email</span> hello@herhandypro.com</div>
            <div><span>Service Area</span> [City/County + nearby]</div>
            <div><span>Hours</span> Mon–Sat • 9am–6pm</div>
          </div>

          <div class="btn-row" style="margin-top:16px">
            <a class="btn" href="mailto:hello@herhandypro.com">Email Us</a>
            <a class="btn" href="#services">Services</a>
          </div>

          <p class="fine" style="margin-top:12px">
            Add your license number and insurance note here if applicable:
            <strong>[License # / Insured]</strong>
          </p>
        </div>
      </div>
    </div>
  </section>

  <footer class="footer">
    <div class="wrap">
      <div class="footer-row">
        <div>
          <strong>Her Handy Pro</strong><br>
          Professional Home Services • Woman-Owned
        </div>
        <div>
          <a href="#top">Back to top</a> •
          <a href="#contact">Contact</a>
        </div>
        <div>
          © <span id="year"></span> Her Handy Pro. All rights reserved.
        </div>
      </div>
    </div>
  </footer>

  <!-- Minimal JS: Mobile menu + form mailto -->
  <script>
    // Footer year
    document.getElementById("year").textContent = new Date().getFullYear();

    // Mobile menu toggle
    const menuBtn = document.getElementById("menuBtn");
    const mobileLinks = document.getElementById("mobileLinks");
    if (menuBtn) {
      menuBtn.addEventListener("click", () => {
        const isOpen = mobileLinks.classList.toggle("show");
        menuBtn.setAttribute("aria-expanded", String(isOpen));
      });
    }

    // Quote form: sends via mailto (simple). Replace with Formspree/Netlify forms when ready.
    const form = document.getElementById("quoteForm");
    form.addEventListener("submit", (e) => {
      e.preventDefault();
      const data = new FormData(form);

      const subject = encodeURIComponent("Quote Request — Her Handy Pro");
      const body = encodeURIComponent(
        "New quote request:\n\n" +
        "Name: " + (data.get("name") || "") + "\n" +
        "Phone: " + (data.get("phone") || "") + "\n" +
        "Email: " + (data.get("email") || "") + "\n" +
        "Service Type: " + (data.get("service") || "") + "\n" +
        "Timing: " + (data.get("timing") || "") + "\n\n" +
        "Details:\n" + (data.get("details") || "") + "\n"
      );

      // Update this email to your real inbox:
      window.location.href = "mailto:hello@herhandypro.com?subject=" + subject + "&body=" + body;
    });
  </script>
</body>
</html>

