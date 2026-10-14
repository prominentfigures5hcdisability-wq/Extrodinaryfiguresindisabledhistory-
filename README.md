<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Your Company Name</title>

  <style>
    :root {
      /* MAIN COLORS – CHANGE THESE */
      --primary: #1e88e5;
      --primary-dark: #1565c0;
      --accent: #ffb300;
      --bg: #f5f5f5;
      --text: #222;
      --text-light: #666;
      --white: #ffffff;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    /* HEADER / NAVBAR */
    header {
      background: var(--white);
      border-bottom: 1px solid #ddd;
      position: sticky;
      top: 0;
      z-index: 10;
    }

    .nav {
      max-width: 1100px;
      margin: 0 auto;
      padding: 1rem 1.5rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-weight: 700;
      font-size: 1.2rem;
      color: var(--primary-dark);
    }

    .nav-links {
      display: flex;
      gap: 1.5rem;
      font-size: 0.95rem;
    }

    .nav-links a:hover {
      color: var(--primary);
    }

    /* HERO SECTION */
    .hero {
      background: linear-gradient(135deg, var(--primary), var(--primary-dark));
      color: var(--white);
      padding: 4rem 1.5rem;
    }

    .hero-inner {
      max-width: 1100px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: minmax(0, 2fr) minmax(0, 1.5fr);
      gap: 2.5rem;
      align-items: center;
    }

    .hero h1 {
      font-size: clamp(2.2rem, 4vw, 3rem);
      margin-bottom: 1rem;
    }

    .hero p {
      font-size: 1.05rem;
      margin-bottom: 1.5rem;
      color: #e3f2fd;
    }

    .hero-buttons {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .btn-primary {
      background: var(--accent);
      color: #000;
      padding: 0.8rem 1.4rem;
      border-radius: 999px;
      font-weight: 600;
      font-size: 0.95rem;
    }

    .btn-outline {
      border: 1px solid #fff;
      color: #fff;
      padding: 0.8rem 1.4rem;
      border-radius: 999px;
      font-weight: 500;
      font-size: 0.95rem;
    }

    .hero-card {
      background: rgba(255, 255, 255, 0.08);
      border-radius: 1rem;
      padding: 1.5rem;
      border: 1px solid rgba(255, 255, 255, 0.25);
      backdrop-filter: blur(6px);
    }

    .hero-card h3 {
      margin-bottom: 0.75rem;
      font-size: 1.1rem;
    }

    .hero-card ul {
      list-style: none;
      font-size: 0.95rem;
    }

    .hero-card li {
      margin-bottom: 0.4rem;
    }

    /* MAIN CONTENT SECTIONS */
    main {
      max-width: 1100px;
      margin: 0 auto;
      padding: 3rem 1.5rem 4rem;
    }

    .section {
      margin-bottom: 3rem;
    }

    .section-header {
      margin-bottom: 1.5rem;
    }

    .section-header h2 {
      font-size: 1.6rem;
      margin-bottom: 0.4rem;
    }

    .section-header p {
      color: var(--text-light);
      font-size: 0.98rem;
    }

    /* SERVICES GRID */
    .grid-3 {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1.5rem;
    }

    .card {
      background: var(--white);
      border-radius: 0.75rem;
      padding: 1.5rem;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.04);
      border: 1px solid #eee;
    }

    .card h3 {
      font-size: 1.1rem;
      margin-bottom: 0.5rem;
    }

    .card p {
      font-size: 0.95rem;
      color: var(--text-light);
    }

    /* ABOUT SECTION */
    .two-column {
      display: grid;
      grid-template-columns: minmax(0, 1.4fr) minmax(0, 1fr);
      gap: 2rem;
      align-items: start;
    }

    .highlight-box {
      background: var(--white);
      border-radius: 0.75rem;
      padding: 1.25rem;
      border: 1px solid #eee;
    }

    .highlight-box h3 {
      font-size: 1.05rem;
      margin-bottom: 0.5rem;
    }

    .highlight-box ul {
      list-style: none;
      font-size: 0.95rem;
      color: var(--text-light);
    }

    .highlight-box li {
      margin-bottom: 0.4rem;
    }

    /* CONTACT SECTION */
    .contact-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.3fr) minmax(0, 1fr);
      gap: 2rem;
    }

    form {
      display: grid;
      gap: 1rem;
    }

    label {
      font-size: 0.9rem;
      font-weight: 600;
    }

    input,
    textarea {
      width: 100%;
      padding: 0.7rem 0.8rem;
      border-radius: 0.5rem;
      border: 1px solid #ccc;
      font-size: 0.95rem;
      font-family: inherit;
    }

    textarea {
      min-height: 120px;
      resize: vertical;
    }

    .contact-info p {
      font-size: 0.95rem;
      color: var(--text-light);
      margin-bottom: 0.4rem;
    }

    .contact-info strong {
      color: var(--text);
    }

    /* FOOTER */
    footer {
      background: #111;
      color: #bbb;
      padding: 1.5rem;
      font-size: 0.85rem;
    }

    .footer-inner {
      max-width: 1100px;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .footer-links {
      display: flex;
      gap: 1rem;
    }

    .footer-links a {
      color: #bbb;
    }

    .footer-links a:hover {
      color: var(--accent);
    }

    /* RESPONSIVE */
    @media (max-width: 900px) {
      .hero-inner,
      .grid-3,
      .two-column,
      .contact-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .hero {
        padding: 3rem 1.25rem;
      }

      .nav {
        flex-direction: column;
        align-items: flex-start;
        gap: 0.75rem;
      }
    }
  </style>
</head>
<body>
  <!-- HEADER / NAV -->
  <header>
    <nav class="nav">
      <div class="logo">Your Company</div>
      <div class="nav-links">
        <a href="#services">Services</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </div>
    </nav>
  </header>

  <!-- HERO -->
  <section class="hero">
    <div class="hero-inner">
      <div>
        <h1>Professional Solutions for Modern Businesses</h1>
        <p>
          Replace this text with your main value statement. Explain clearly what you do and
          who you serve.
        </p>
        <div class="hero-buttons">
          <a href="#contact" class="btn-primary">Request a Consultation</a>
          <a href="#services" class="btn-outline">View Our Services</a>
        </div>
      </div>

      <aside class="hero-card">
        <h3>Why Clients Choose Us</h3>
        <ul>
          <li>✔ Clear, measurable results</li>
          <li>✔ Dedicated, responsive support</li>
          <li>✔ Tailored strategies for your goals</li>
        </ul>
      </aside>
    </div>
  </section>

  <!-- MAIN CONTENT -->
  <main>
    <!-- SERVICES -->
    <section id="services" class="section">
      <div class="section-header">
        <h2>Our Services</h2>
        <p>Update these cards to match what your business offers.</p>
      </div>

      <div class="grid-3">
        <article class="card">
          <h3>Service One</h3>
          <p>
            Short description of your first key service. Focus on benefits and outcomes for the client.
          </p>
        </article>

        <article class="card">
          <h3>Service Two</h3>
          <p>
            Another core service. You can duplicate or remove cards depending on how many you need.
          </p>
        </article>

        <article class="card">
          <h3>Service Three</h3>
          <p>
            Use this space to highlight a premium or signature offering that sets you apart.
          </p>
        </article>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about" class="section">
      <div class="section-header">
        <h2>About Our Company</h2>
        <p>Tell your story, your mission, and what makes your team unique.</p>
      </div>

      <div class="two-column">
        <div>
          <p>
            Replace this paragraph with a concise overview of your company. Mention your experience,
            industries you serve, and the values that guide your work.
          </p>
          <p>
            You can add more paragraphs, bullet lists, or images here. Keep it clear and
            client-focused.
          </p>
        </div>

        <aside class="highlight-box">
          <h3>Key Highlights</h3>
          <ul>
            <li>• Years in business: 10+</li>
            <li>• Clients served: 200+ worldwide</li>
            <li>• Offices: New York, London, Remote</li>
          </ul>
        </aside>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="section">
      <div class="section-header">
        <h2>Contact Us</h2>
        <p>Invite visitors to reach out. You can connect this form to a backend later.</p>
      </div>

      <div class="contact-grid">
        <form>
          <div>
            <label for="name">Name</label>
            <input id="name" type="text" placeholder="Your full name" />
          </div>

          <div>
            <label for="email">Email</label>
            <input id="email" type="email" placeholder="you@example.com" />
          </div>

          <div>
            <label for="message">Message</label>
            <textarea id="message" placeholder="Tell us what you’re looking for"></textarea>
          </div>

          <button type="submit" class="btn-primary">Send Message</button>
        </form>

        <div class="contact-info">
          <p><strong>Email:</strong> contact@yourcompany.com</p>
          <p><strong>Phone:</strong> +1 (555) 123-4567</p>
          <p><strong>Address:</strong> 123 Business Street, City, Country</p>
          <p>
            You can replace this block with a map embed, social media links, or office hours.
          </p>
        </div>
      </div>
    </section>
  </main>

  <!-- FOOTER -->
  <footer>
    <div class="footer-inner">
      <div>© <span id="year"></span> Your Company. All rights reserved.</div>
      <div class="footer-links">
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
      </div>
    </div>
  </footer>

  <script>
    // Auto-update year in footer
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
