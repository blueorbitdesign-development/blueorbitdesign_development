<!mitul_h_Patel>
<!Contect_Us_:- +91-7383530020>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Machinery Drawings & Pattern Design</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #0a0f1c;
      color: #f4f4f4;
      line-height: 1.6;
      overflow-x: hidden;
    }

    header {
      background: linear-gradient(135deg, #1f2937, #111827);
      padding: 60px 20px;
      text-align: center;
      animation: fadeIn 2s ease-in-out;
    }

    header h1 {
      font-size: 2.8rem;
      margin-bottom: 10px;
    }

    header p {
      font-size: 1.2rem;
      color: #a0aec0;
    }

    nav {
      display: flex;
      justify-content: center;
      background: #1f2937;
      padding: 10px 0;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    nav a {
      color: #ffffff;
      margin: 0 20px;
      text-decoration: none;
      transition: color 0.3s;
    }

    nav a:hover {
      color: #00bcd4;
    }

    section {
      padding: 60px 20px;
      max-width: 1000px;
      margin: auto;
      opacity: 0;
      transform: translateY(40px);
      animation: fadeUp 1s ease forwards;
    }

    section.animate {
      opacity: 1;
      transform: translateY(0);
    }

    section:nth-child(odd) {
      background: #111827;
    }

    section:nth-child(even) {
      background: #1f2937;
    }

    h2 {
      font-size: 2rem;
      margin-bottom: 20px;
      color: #00bcd4;
    }

    ul {
      list-style: none;
      margin-bottom: 20px;
    }

    ul li::before {
      content: "✔";
      margin-right: 10px;
      color: #00bcd4;
    }

    .section-image {
      width: 100%;
      height: auto;
      border-radius: 8px;
      margin-top: 20px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.4);
    }

    footer {
      text-align: center;
      padding: 20px;
      background: #0a0f1c;
      font-size: 0.9rem;
      color: #718096;
    }

    /* Animations */
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeUp {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>Machinery Drawings & Pattern Design</h1>
    <p>Precision Engineering for Efficient Manufacturing</p>
  </header>

  <nav>
    <a href="#services">Services</a>
    <a href="#industries">Industries</a>
    <a href="#why-us">Why Us</a>
  </nav>

  <section id="services">
    <h2>Our Services</h2>
    <ul>
      <li>2D & 3D CAD Drawings</li>
      <li>Mechanical Component Design</li>
      <li>Reverse Engineering</li>
      <li>Pattern Design for Casting & Molding</li>
      <li>Geometric Dimensioning & Tolerancing (GD&T)</li>
      <li>Prototyping Support & Design Optimization</li>

  <section id="industries">
    <h2>Industries We Serve</h2>
    <ul>
      <li>Manufacturing & Fabrication</li>
      <li>Automotive & Heavy Machinery</li>
      <li>Foundry & Metal Casting</li>
      <li>Agricultural Equipment</li>
      <li>Oil & Gas Equipment</li>
    </ul>

  <section id="why-us">
    <h2>Why Choose Us?</h2>
    <ul>
      <li>High-precision, production-ready drawings</li>
      <li>Industry-standard software (AutoCAD, SolidWorks, CATIA, etc.)</li>
      <li>Fast turnaround with revision support</li>
      <li>Strict quality control and confidentiality</li>
    </ul>

  <footer>
    &copy; 2025 Machinery Drawings & Pattern Design Services. - Mitul_H_patel___________Contect_Us:- +91-7383530020
  </footer>

  <script>
    // Scroll-triggered animation
    const sections = document.querySelectorAll("section");

    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add("animate");
        }
      });
    }, {
      threshold: 0.2
    });

    sections.forEach(section => {
      observer.observe(section);
    });
  </script>

</body>
</html>
