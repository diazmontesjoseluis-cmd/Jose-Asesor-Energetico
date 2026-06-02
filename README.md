[index_mejorado.html](https://github.com/user-attachments/files/28500882/index_mejorado.html)
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Jose Asesor Energético | Ahorro Premium en Luz y Gas</title>
  <meta name="description" content="Asesor energético profesional. Ahorra hasta un 40% en tu factura de luz y gas con un estudio gratuito y sin compromiso.">

  <!-- Google Fonts: Outfit (headings) & Inter (body) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Outfit:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
  
  <!-- Font Awesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css">

  <style>
    /* ══════════════════════════════════════════════
       DESIGN SYSTEM (HSL TOKENS)
       ══════════════════════════════════════════════ */
    :root {
      /* Color Palette: Emerald + Cool Blue */
      --primary-hsl: 150, 84%, 37%;
      --primary: hsl(var(--primary-hsl));
      --primary-hover: hsl(150, 84%, 30%);
      --primary-light: hsl(150, 80%, 95%);
      --primary-glow: rgba(16, 185, 129, 0.35);

      --blue: hsl(217, 91%, 60%);
      --blue-light: hsl(217, 91%, 95%);
      --amber: hsl(40, 95%, 50%);
      --orange: hsl(24, 95%, 50%);
      --purple: hsl(270, 85%, 60%);
      --red: hsl(350, 80%, 55%);

      /* Light Theme Variables */
      --bg: hsl(150, 15%, 98%);
      --bg-alt: hsl(0, 0%, 100%);
      --surface: hsl(0, 0%, 100%);
      --surface-hover: hsl(150, 60%, 97%);
      --text: hsl(217, 33%, 17%);
      --text-muted: hsl(215, 16%, 47%);
      --text-light: hsl(215, 16%, 65%);
      --border: hsl(220, 13%, 91%);
      --border-focus: var(--primary);
      --glass: rgba(255, 255, 255, 0.75);
      --glass-border: rgba(255, 255, 255, 0.4);

      /* Shadows & Radii */
      --shadow-xs: 0 1px 3px rgba(0,0,0,0.02);
      --shadow-sm: 0 4px 20px rgba(15, 23, 42, 0.03);
      --shadow-md: 0 12px 36px rgba(15, 23, 42, 0.06);
      --shadow-lg: 0 24px 64px rgba(15, 23, 42, 0.09);
      --shadow-primary: 0 8px 30px var(--primary-glow);

      --r-sm: 12px;
      --r-md: 18px;
      --r-lg: 26px;
      --r-xl: 36px;
      --r-2xl: 48px;

      --ease: cubic-bezier(0.16, 1, 0.3, 1);
      --spring: cubic-bezier(0.34, 1.56, 0.64, 1);
    }

    /* Dark Theme Override */
    body.dark {
      --bg: hsl(222, 47%, 7%);
      --bg-alt: hsl(223, 47%, 4%);
      --surface: hsl(223, 47%, 11%);
      --surface-hover: hsl(223, 47%, 14%);
      --text: hsl(210, 40%, 98%);
      --text-muted: hsl(215, 20%, 75%);
      --text-light: hsl(215, 15%, 55%);
      --border: hsl(222, 22%, 18%);
      --primary-light: hsl(150, 50%, 15%);
      --blue-light: hsl(217, 50%, 15%);
      --glass: rgba(15, 23, 42, 0.7);
      --glass-border: rgba(255, 255, 255, 0.06);
      --shadow-sm: 0 4px 20px rgba(0, 0, 0, 0.2);
      --shadow-md: 0 12px 36px rgba(0, 0, 0, 0.35);
      --shadow-lg: 0 24px 64px rgba(0, 0, 0, 0.5);
    }

    /* Custom Scrollbar */
    ::-webkit-scrollbar {
      width: 10px;
    }
    ::-webkit-scrollbar-track {
      background: var(--bg);
    }
    ::-webkit-scrollbar-thumb {
      background: var(--border);
      border-radius: 10px;
      border: 2px solid var(--bg);
    }
    ::-webkit-scrollbar-thumb:hover {
      background: var(--text-light);
    }

    /* Reset */
    *, *::before, *::after {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    html {
      scroll-behavior: smooth;
    }
    body {
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
      background: var(--bg);
      color: var(--text);
      overflow-x: hidden;
      transition: background 0.6s var(--ease), color 0.6s var(--ease);
      line-height: 1.7;
      -webkit-font-smoothing: antialiased;
    }

    h1, h2, h3, h4, .logo-title, .btn, .sec-badge {
      font-family: 'Outfit', sans-serif;
    }

    /* Noise Background */
    .noise-bg {
      position: fixed;
      inset: 0;
      z-index: 9999;
      pointer-events: none;
      background: url('data:image/svg+xml;utf8,%3Csvg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg"%3E%3Cfilter id="noiseFilter"%3E%3CfeTurbulence type="fractalNoise" baseFrequency="0.8" numOctaves="3" stitchTiles="stitch"/%3E%3C/filter%3E%3Crect width="100%25" height="100%25" filter="url(%23noiseFilter)" opacity="0.04"/%3E%3C/svg%3E');
      opacity: 0.55;
      mix-blend-mode: overlay;
    }

    a {
      text-decoration: none;
      color: inherit;
    }
    button, input, select, textarea {
      font-family: inherit;
      border: none;
      outline: none;
    }
    img {
      max-width: 100%;
      display: block;
    }

    /* Loader */
    .loader {
      position: fixed;
      inset: 0;
      z-index: 99999;
      background: linear-gradient(135deg, hsl(223, 47%, 7%), hsl(150, 84%, 15%));
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      transition: opacity 0.5s var(--ease), visibility 0.5s var(--ease);
    }
    .loader.done {
      opacity: 0;
      visibility: hidden;
      pointer-events: none;
    }
    .loader-ring {
      width: 50px;
      height: 50px;
      border: 3px solid rgba(255, 255, 255, 0.1);
      border-top-color: var(--primary);
      border-radius: 50%;
      animation: spin 0.8s linear infinite;
    }
    .loader-label {
      color: #fff;
      font-weight: 700;
      margin-top: 20px;
      font-size: 1.1rem;
      letter-spacing: 2px;
      text-transform: uppercase;
      opacity: 0.9;
    }
    @keyframes spin { to { transform: rotate(360deg); } }

    /* Layout & Utilities */
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 24px;
    }
    .text-center { text-align: center; }
    .gradient-text {
      background: linear-gradient(135deg, hsl(150, 84%, 45%), var(--primary-hover));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    /* Buttons */
    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      padding: 16px 36px;
      border-radius: 60px;
      font-weight: 700;
      font-size: 0.95rem;
      transition: background 0.3s, color 0.3s, box-shadow 0.3s, transform 0.3s;
      position: relative;
      overflow: hidden;
      cursor: pointer;
    }
    .btn::before {
      content: '';
      position: absolute;
      inset: 0;
      border-radius: inherit;
      background: linear-gradient(135deg, rgba(255,255,255,0.25), transparent);
      opacity: 0;
      transition: opacity 0.3s;
    }
    .btn:hover::before { opacity: 1; }
    
    .btn-primary {
      background: linear-gradient(135deg, var(--primary), var(--primary-hover));
      color: #fff;
      box-shadow: var(--shadow-primary);
    }
    .btn-primary:hover {
      box-shadow: 0 16px 48px rgba(16, 185, 129, 0.45);
      transform: translateY(-3px) scale(1.02);
    }
    
    .btn-ghost {
      background: rgba(255, 255, 255, 0.08);
      color: #fff;
      border: 1.5px solid rgba(255, 255, 255, 0.18);
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);
    }
    .btn-ghost:hover {
      background: rgba(255, 255, 255, 0.16);
      border-color: rgba(255, 255, 255, 0.35);
      transform: translateY(-3px);
    }
    
    .btn-white {
      background: #fff;
      color: hsl(150, 84%, 25%);
      font-weight: 800;
      box-shadow: var(--shadow-sm);
    }
    .btn-white:hover {
      box-shadow: var(--shadow-lg);
      transform: translateY(-3px);
    }
    .btn-lg {
      padding: 18px 44px;
      font-size: 1.05rem;
    }

    /* Scroll Reveal Classes */
    .rv { opacity: 0; transform: translateY(40px); transition: opacity 0.85s var(--ease), transform 0.85s var(--ease); }
    .rv.on { opacity: 1; transform: translateY(0); }
    .rv-l { opacity: 0; transform: translateX(-40px); transition: all 0.85s var(--ease); }
    .rv-l.on { opacity: 1; transform: translateX(0); }
    .rv-r { opacity: 0; transform: translateX(40px); transition: all 0.85s var(--ease); }
    .rv-r.on { opacity: 1; transform: translateX(0); }
    .rv-s { opacity: 0; transform: scale(0.94); transition: all 0.85s var(--ease); }
    .rv-s.on { opacity: 1; transform: scale(1); }

    /* Header */
    header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      padding: 18px 0;
      transition: all 0.4s var(--ease);
    }
    header.stuck {
      padding: 10px 0;
      background: var(--glass) !important;
      backdrop-filter: blur(15px);
      -webkit-backdrop-filter: blur(15px);
      border-bottom: 1px solid var(--glass-border);
      box-shadow: var(--shadow-sm);
    }
    .nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .logo {
      display: flex;
      align-items: center;
      gap: 14px;
    }
    .logo-box {
      width: 48px;
      height: 48px;
      border-radius: 14px;
      background: linear-gradient(135deg, var(--primary), var(--primary-hover));
      display: flex;
      align-items: center;
      justify-content: center;
      color: #fff;
      font-size: 1.25rem;
      box-shadow: var(--shadow-primary);
      transition: transform 0.4s var(--spring);
    }
    .logo-box img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      border-radius: 14px;
    }
    .logo:hover .logo-box {
      transform: rotate(-6deg) scale(1.1);
    }
    
    /* Logo Title styling */
    .logo-title {
      font-size: 1.2rem;
      font-weight: 900;
      letter-spacing: -0.5px;
      line-height: 1.1;
      color: var(--text);
    }
    .logo-sub {
      font-size: 0.78rem;
      color: var(--primary);
      font-weight: 700;
      letter-spacing: 0.5px;
      text-transform: uppercase;
    }

    .nav-pills {
      display: flex;
      align-items: center;
      gap: 4px;
      background: var(--glass);
      border: 1px solid var(--glass-border);
      border-radius: 60px;
      padding: 6px;
      box-shadow: var(--shadow-xs);
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);
    }
    .nav-pills a {
      padding: 10px 22px;
      border-radius: 50px;
      font-weight: 600;
      font-size: 0.88rem;
      color: var(--text-muted);
      transition: all 0.3s var(--ease);
      white-space: nowrap;
    }
    .nav-pills a:hover {
      color: var(--primary);
      background: var(--primary-light);
    }
    .nav-pills a.active {
      background: var(--primary);
      color: #fff;
      box-shadow: var(--shadow-primary);
    }

    .nav-right {
      display: flex;
      align-items: center;
      gap: 12px;
    }
    
    /* Theme Toggle Switch */
    .theme-btn {
      width: 44px;
      height: 44px;
      border-radius: 12px;
      background: var(--surface);
      border: 1px solid var(--border);
      display: flex;
      align-items: center;
      justify-content: center;
      transition: all 0.3s var(--spring);
      color: var(--text);
      font-size: 1.1rem;
      cursor: pointer;
      box-shadow: var(--shadow-xs);
    }
    .theme-btn:hover {
      transform: rotate(15deg) scale(1.08);
      border-color: var(--primary);
      color: var(--primary);
    }
    
    .th-icon-wrap {
      position: relative;
      width: 18px;
      height: 18px;
    }
    .th-icon-wrap i {
      position: absolute;
      top: 0;
      left: 0;
      transition: all 0.5s var(--spring);
    }
    
    /* Sun/Moon visibility in Light/Dark themes */
    body:not(.dark) .fa-sun {
      opacity: 0;
      transform: rotate(-90deg) scale(0.5);
    }
    body:not(.dark) .fa-moon {
      opacity: 1;
      transform: rotate(0) scale(1);
    }
    body.dark .fa-sun {
      opacity: 1;
      transform: rotate(0) scale(1);
    }
    body.dark .fa-moon {
      opacity: 0;
      transform: rotate(90deg) scale(0.5);
    }

    .burger {
      display: none;
      width: 44px;
      height: 44px;
      border-radius: 12px;
      background: var(--surface);
      border: 1px solid var(--border);
      align-items: center;
      justify-content: center;
      flex-direction: column;
      gap: 5px;
      padding: 12px;
      transition: all 0.3s;
      cursor: pointer;
    }
    .burger span {
      display: block;
      width: 100%;
      height: 2.5px;
      background: var(--text);
      border-radius: 2px;
      transition: all 0.35s var(--ease);
    }
    .burger.on span:nth-child(1) { transform: rotate(45deg) translate(5px, 5px); }
    .burger.on span:nth-child(2) { opacity: 0; }
    .burger.on span:nth-child(3) { transform: rotate(-45deg) translate(5px, -5px); }

    .mob-menu {
      position: fixed;
      inset: 0;
      z-index: 999;
      background: var(--bg);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 12px;
      opacity: 0;
      visibility: hidden;
      transition: all 0.45s var(--ease);
    }
    .mob-menu.show {
      opacity: 1;
      visibility: visible;
    }
    .mob-menu a {
      font-size: 1.8rem;
      font-weight: 800;
      padding: 12px 40px;
      border-radius: 18px;
      transition: all 0.3s;
      color: var(--text);
    }
    .mob-menu a:hover {
      background: var(--primary-light);
      color: var(--primary);
    }

    /* Hero Section */
    .hero {
      position: relative;
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 130px 0 100px;
      overflow: hidden;
    }
    .hero-bg {
      position: absolute;
      inset: 0;
      z-index: 0;
      background: url('paginaweb/background-hero.jpg') center/cover no-repeat;
    }
    /* Dynamic overlay depending on light/dark mode */
    .hero-ov {
      position: absolute;
      inset: 0;
      z-index: 1;
      background: linear-gradient(160deg, rgba(4, 10, 4, 0.95) 0%, rgba(10, 15, 28, 0.6) 55%, rgba(4, 10, 4, 0.93) 100%);
      transition: background 0.5s ease;
    }
    body.dark .hero-ov {
      background: linear-gradient(160deg, rgba(3, 6, 12, 0.98) 0%, rgba(10, 15, 28, 0.8) 55%, rgba(2, 4, 8, 0.98) 100%);
    }

    .hero-orb {
      position: absolute;
      border-radius: 50%;
      filter: blur(120px);
      z-index: 2;
      animation: orb-float 14s ease-in-out infinite alternate;
      pointer-events: none;
    }
    .hero-orb-1 { width: 550px; height: 550px; background: rgba(16, 185, 129, 0.14); top: -10%; right: 5%; }
    .hero-orb-2 { width: 450px; height: 450px; background: rgba(59, 130, 246, 0.09); bottom: -5%; left: -5%; animation-delay: 3s; }
    .hero-orb-3 { width: 350px; height: 350px; background: rgba(168, 85, 247, 0.08); top: 35%; right: -5%; animation-delay: 6s; }
    
    @keyframes orb-float {
      0% { transform: translate(0, 0) scale(1); }
      50% { transform: translate(40px, -50px) scale(1.1); }
      100% { transform: translate(-30px, 40px) scale(0.92); }
    }

    canvas#pCanvas {
      position: absolute;
      inset: 0;
      z-index: 3;
      pointer-events: none;
    }

    .hero-grid {
      position: relative;
      z-index: 4;
      display: grid;
      grid-template-columns: 1.15fr 1fr;
      gap: 80px;
      align-items: center;
    }
    .hero-left { color: #fff; }
    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      background: rgba(16, 185, 129, 0.15);
      border: 1px solid rgba(16, 185, 129, 0.35);
      padding: 9px 24px;
      border-radius: 60px;
      font-size: 0.85rem;
      font-weight: 700;
      margin-bottom: 32px;
      backdrop-filter: blur(8px);
      -webkit-backdrop-filter: blur(8px);
      animation: badge-pulse 3s ease-in-out infinite;
    }
    .hero-badge i { color: var(--amber); font-size: 0.95rem; }
    
    @keyframes badge-pulse {
      0%, 100% { box-shadow: 0 0 0 0 rgba(16, 185, 129, 0.2); }
      50% { box-shadow: 0 0 24px 8px rgba(16, 185, 129, 0.15); }
    }
    
    .hero-title {
      font-size: clamp(2.8rem, 5.5vw, 4.8rem);
      font-weight: 900;
      line-height: 1.08;
      margin-bottom: 28px;
      letter-spacing: -2px;
    }
    .hero-desc {
      font-size: 1.2rem;
      color: rgba(255, 255, 255, 0.75);
      max-width: 520px;
      margin-bottom: 44px;
      line-height: 1.8;
    }
    .hero-btns {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
    }

    .hero-stats {
      display: flex;
      gap: 52px;
      margin-top: 60px;
      padding-top: 40px;
      border-top: 1px solid rgba(255, 255, 255, 0.1);
    }
    .h-stat-val {
      font-size: 2.8rem;
      font-weight: 900;
      color: var(--primary);
      line-height: 1;
      margin-bottom: 4px;
      letter-spacing: -1px;
    }
    .h-stat-lbl {
      font-size: 0.88rem;
      color: rgba(255, 255, 255, 0.6);
      font-weight: 600;
    }

    /* 3D Glass Card */
    .hero-right {
      perspective: 1500px;
    }
    .hero-glass {
      background: rgba(255, 255, 255, 0.05);
      backdrop-filter: blur(25px);
      -webkit-backdrop-filter: blur(25px);
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: var(--r-2xl);
      padding: 24px;
      transform-style: preserve-3d;
      transform: rotateY(-8deg) rotateX(4deg);
      transition: transform 0.15s ease-out, box-shadow 0.3s;
      box-shadow: 0 50px 100px rgba(0, 0, 0, 0.4);
      position: relative;
    }
    .hero-glass:hover {
      box-shadow: 0 70px 120px rgba(0, 0, 0, 0.55);
    }
    
    .glare-effect {
      position: absolute;
      inset: 0;
      border-radius: var(--r-2xl);
      background: radial-gradient(circle at 50% 50%, rgba(255,255,255,0.15) 0%, transparent 60%);
      pointer-events: none;
      z-index: 5;
      opacity: 0;
      transition: opacity 0.3s;
    }
    
    .hero-card {
      background: var(--surface);
      border-radius: var(--r-xl);
      padding: 36px;
      box-shadow: var(--shadow-md);
      color: var(--text);
      position: relative;
      overflow: hidden;
      transform: translateZ(30px); /* 3D Pop Effect */
      transition: background 0.5s var(--ease);
    }
    
    .hero-card::before {
      content: '';
      position: absolute;
      inset: 0;
      border-radius: var(--r-xl);
      padding: 2px;
      background: linear-gradient(135deg, var(--primary), transparent, transparent);
      -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
      -webkit-mask-composite: xor;
      mask-composite: exclude;
      pointer-events: none;
    }
    
    .hc-top {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 32px;
    }
    .hc-top small {
      display: block;
      color: var(--text-light);
      font-weight: 700;
      font-size: 0.85rem;
      margin-bottom: 6px;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }
    .hc-amount {
      font-size: 3.2rem;
      font-weight: 900;
      color: var(--primary);
      line-height: 1;
      letter-spacing: -1px;
    }
    .hc-icon {
      width: 58px;
      height: 58px;
      border-radius: 18px;
      background: var(--primary-light);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.6rem;
      color: var(--primary);
      transition: transform 0.4s var(--ease);
    }
    .hero-glass:hover .hc-icon {
      transform: scale(1.1) rotate(12deg);
    }
    
    .prog { margin-bottom: 22px; }
    .prog:last-child { margin-bottom: 0; }
    .prog-head {
      display: flex;
      justify-content: space-between;
      margin-bottom: 8px;
      font-weight: 700;
      font-size: 0.92rem;
    }
    .prog-bar {
      width: 100%;
      height: 12px;
      background: var(--bg);
      border-radius: 20px;
      overflow: hidden;
      border: 1px solid var(--border);
    }
    
    .prog-fill {
      height: 100%;
      border-radius: 20px;
      width: 0;
      transition: width 1.6s var(--ease);
    }
    .fill-r { background: linear-gradient(90deg, var(--red), hsl(350, 80%, 70%)); }
    .fill-g { background: linear-gradient(90deg, var(--primary), hsl(150, 80%, 60%)); }

    /* Wave transition */
    .wave-div {
      position: relative;
      overflow: hidden;
      line-height: 0;
      margin-top: -2px;
      z-index: 10;
    }
    .wave-div svg {
      display: block;
      width: 100%;
      height: 70px;
    }
    .wave-div svg path {
      fill: var(--bg-alt);
      transition: fill 0.6s var(--ease);
    }

    /* Common Section Styles */
    section {
      padding: 110px 0;
      position: relative;
      z-index: 10;
      transition: background 0.6s var(--ease);
    }
    .sec-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: var(--primary-light);
      color: var(--primary);
      padding: 8px 22px;
      border-radius: 50px;
      font-size: 0.8rem;
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: 2px;
      margin-bottom: 18px;
    }
    
    .sec-title {
      font-size: clamp(2.1rem, 3.8vw, 3.2rem);
      font-weight: 900;
      letter-spacing: -1.5px;
      line-height: 1.15;
      margin-bottom: 18px;
    }
    .sec-desc {
      font-size: 1.15rem;
      color: var(--text-muted);
      max-width: 600px;
      margin: 0 auto;
      line-height: 1.8;
    }

    /* Trust Strip */
    .trust {
      padding: 56px 0;
      border-bottom: 1px solid var(--border);
      background: var(--bg-alt);
      position: relative;
      z-index: 10;
      transition: background 0.6s var(--ease), border-color 0.6s var(--ease);
    }
    .trust-lbl {
      text-align: center;
      font-size: 0.8rem;
      font-weight: 800;
      color: var(--text-light);
      text-transform: uppercase;
      letter-spacing: 3px;
      margin-bottom: 28px;
    }
    .trust-row {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 56px;
      flex-wrap: wrap;
    }
    .trust-row img {
      height: 38px;
      object-fit: contain;
      opacity: 0.38;
      transition: all 0.4s var(--ease);
      filter: grayscale(1);
    }
    body.dark .trust-row img {
      filter: grayscale(1) invert(1);
      opacity: 0.45;
    }
    .trust-row img:hover {
      opacity: 1;
      transform: scale(1.1);
      filter: none;
    }

    /* Companies Dashboard */
    .comp-sec {
      background: var(--bg-alt);
    }
    .comp-wrap {
      background: var(--surface);
      border-radius: var(--r-2xl);
      box-shadow: var(--shadow-lg);
      border: 1px solid var(--border);
      overflow: hidden;
      max-width: 960px;
      margin: 56px auto 0;
      position: relative;
      transition: all 0.5s var(--ease);
    }
    
    .comp-head {
      display: grid;
      grid-template-columns: 2.2fr 1fr 1fr;
      background: linear-gradient(135deg, hsl(150, 84%, 25%), var(--primary-hover));
      color: #fff;
      font-weight: 700;
      font-size: 0.85rem;
      text-transform: uppercase;
      letter-spacing: 1.5px;
    }
    .comp-head > div {
      padding: 20px 28px;
    }
    .comp-head > div:not(:first-child) {
      text-align: center;
      border-left: 1px solid rgba(255, 255, 255, 0.1);
    }
    
    .comp-r {
      display: grid;
      grid-template-columns: 2.2fr 1fr 1fr;
      align-items: center;
      border-bottom: 1px solid var(--border);
      transition: all 0.3s var(--ease);
      cursor: default;
      position: relative;
    }
    .comp-r:last-child { border-bottom: none; }
    .comp-r:hover {
      background: var(--surface-hover);
    }
    .comp-r > div {
      padding: 20px 28px;
    }
    .comp-r > div:not(:first-child) {
      text-align: center;
    }
    
    .comp-id {
      display: flex;
      align-items: center;
      gap: 18px;
    }
    .comp-logo {
      width: 52px;
      height: 52px;
      border-radius: 14px;
      object-fit: contain;
      background: #fff;
      padding: 6px;
      box-shadow: var(--shadow-xs);
      border: 1px solid var(--border);
      transition: all 0.4s var(--ease);
    }
    .comp-r:hover .comp-logo {
      transform: scale(1.1) rotate(-4deg);
      box-shadow: var(--shadow-sm);
    }
    .comp-nm {
      font-weight: 800;
      font-size: 1.05rem;
      letter-spacing: -0.4px;
      color: var(--text);
    }
    .comp-pl {
      font-size: 0.8rem;
      color: var(--text-light);
      margin-top: 2px;
      font-weight: 600;
    }
    .comp-pr {
      font-weight: 800;
      font-size: 1.15rem;
      color: var(--text);
    }
    
    /* Verified Tag & Badges */
    .tag {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 6px 16px;
      border-radius: 50px;
      font-size: 0.78rem;
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }
    .tg-g { background: var(--primary-light); color: var(--primary); }
    .tg-b { background: var(--blue-light); color: var(--blue); }
    .tg-a { background: hsl(40, 100%, 93%); color: var(--amber); }
    .tg-o { background: hsl(24, 100%, 93%); color: var(--orange); }
    .tg-p { background: hsl(270, 100%, 95%); color: var(--purple); }
    
    body.dark .tg-g { background: rgba(16, 185, 129, 0.15); }
    body.dark .tg-b { background: rgba(59, 130, 246, 0.15); }
    body.dark .tg-a { background: rgba(245, 158, 11, 0.15); }
    body.dark .tg-o { background: rgba(249, 115, 22, 0.15); }
    body.dark .tg-p { background: rgba(168, 85, 247, 0.15); }

    /* Mobile Companies */
    .comp-mob {
      display: none;
      margin-top: 40px;
    }
    .comp-mc {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--r-md);
      padding: 22px;
      margin-bottom: 14px;
      display: flex;
      align-items: center;
      gap: 16px;
      transition: all 0.3s var(--ease);
    }
    .comp-mc:hover {
      transform: translateY(-4px);
      box-shadow: var(--shadow-md);
      border-color: var(--primary);
    }
    .comp-mc img {
      width: 48px;
      height: 48px;
      border-radius: 12px;
      object-fit: contain;
      background: #fff;
      padding: 5px;
      box-shadow: var(--shadow-xs);
      border: 1px solid var(--border);
    }
    .comp-mc-info {
      flex: 1;
    }
    .comp-mc-info h4 {
      font-weight: 800;
      font-size: 1rem;
      color: var(--text);
    }
    .comp-mc-info p {
      color: var(--text-light);
      font-size: 0.8rem;
      font-weight: 600;
      margin-top: 2px;
    }
    .comp-mc-pr {
      font-weight: 800;
      font-size: 1.15rem;
      color: var(--primary);
    }

    /* Dual Calculator Premium */
    .calc-sec {
      background: var(--bg);
    }
    .calc-tabs {
      display: flex;
      background: var(--border);
      border-radius: 60px;
      padding: 6px;
      margin: 0 auto 44px;
      max-width: 440px;
      box-shadow: var(--shadow-xs);
    }
    .calc-tab {
      flex: 1;
      text-align: center;
      padding: 14px 24px;
      border-radius: 50px;
      font-weight: 700;
      font-size: 0.95rem;
      color: var(--text-muted);
      cursor: pointer;
      transition: all 0.3s var(--ease);
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
    }
    .calc-tab.active {
      background: var(--surface);
      color: var(--primary);
      box-shadow: var(--shadow-sm);
    }
    
    .calc-wrap {
      background: var(--surface);
      border-radius: var(--r-2xl);
      box-shadow: var(--shadow-lg);
      border: 1px solid var(--border);
      padding: 56px;
      position: relative;
      overflow: hidden;
      transition: background 0.5s var(--ease);
    }
    .calc-wrap::before {
      content: '';
      position: absolute;
      inset: 0;
      border-radius: var(--r-2xl);
      padding: 1px;
      background: linear-gradient(135deg, var(--primary), transparent, transparent);
      -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
      -webkit-mask-composite: xor;
      mask-composite: exclude;
      pointer-events: none;
    }

    .calc-grid {
      display: grid;
      grid-template-columns: 1.1fr 1fr;
      gap: 60px;
      align-items: center;
    }
    .calc-pane {
      display: none;
      animation: calcFade 0.4s var(--ease);
    }
    .calc-pane.active {
      display: block;
    }
    @keyframes calcFade {
      from { opacity: 0; transform: translateY(12px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .calc-form label {
      display: block;
      font-weight: 700;
      margin-bottom: 14px;
      font-size: 0.95rem;
      color: var(--text);
    }
    
    .calc-rng-wrap {
      margin-bottom: 40px;
      position: relative;
    }
    
    .rng-val {
      font-size: 3rem;
      font-weight: 900;
      color: var(--primary);
      line-height: 1;
      margin: 8px 0 16px;
      letter-spacing: -1px;
    }
    
    .rng {
      width: 100%;
      -webkit-appearance: none;
      appearance: none;
      height: 8px;
      border-radius: 20px;
      outline: none;
      background: linear-gradient(90deg, var(--primary) 0%, var(--border) 0%);
      cursor: pointer;
    }
    .rng::-webkit-slider-thumb {
      -webkit-appearance: none;
      width: 28px;
      height: 28px;
      border-radius: 50%;
      background: #fff;
      border: 4px solid var(--primary);
      box-shadow: 0 4px 12px rgba(16, 185, 129, 0.4);
      cursor: pointer;
      transition: transform 0.2s var(--spring);
    }
    .rng::-webkit-slider-thumb:hover {
      transform: scale(1.22);
    }
    .rng::-moz-range-thumb {
      width: 28px;
      height: 28px;
      border-radius: 50%;
      background: #fff;
      border: 4px solid var(--primary);
      box-shadow: 0 4px 12px rgba(16, 185, 129, 0.4);
      cursor: pointer;
      transition: transform 0.2s var(--spring);
    }
    .rng::-moz-range-thumb:hover {
      transform: scale(1.22);
    }

    .rng-lim {
      display: flex;
      justify-content: space-between;
      color: var(--text-light);
      font-size: 0.82rem;
      font-weight: 600;
      margin-top: 8px;
    }

    .calc-sel {
      width: 100%;
      padding: 16px 22px;
      border-radius: 16px;
      border: 2px solid var(--border);
      background: var(--surface);
      color: var(--text);
      font-size: 0.95rem;
      font-weight: 700;
      cursor: pointer;
      transition: all 0.3s;
      -webkit-appearance: none;
      appearance: none;
      background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='20' height='20' viewBox='0 0 24 24' fill='none' stroke='%2394a3b8' stroke-width='2.5'%3E%3Cpolyline points='6 9 12 15 18 9'/%3E%3C/svg%3E");
      background-repeat: no-repeat;
      background-position: right 18px center;
    }
    .calc-sel:focus {
      border-color: var(--primary);
      box-shadow: 0 0 0 4px var(--primary-glow);
    }

    /* Result pane with real-time Graph */
    .calc-res {
      background: linear-gradient(135deg, hsl(150, 84%, 22%), var(--primary-hover));
      color: #fff;
      border-radius: var(--r-2xl);
      padding: 44px 36px;
      text-align: center;
      position: relative;
      overflow: hidden;
      box-shadow: var(--shadow-primary);
    }
    .calc-res::before {
      content: '';
      position: absolute;
      width: 320px;
      height: 320px;
      background: rgba(255, 255, 255, 0.04);
      border-radius: 50%;
      top: -100px;
      right: -80px;
    }
    
    .calc-res-lbl {
      font-size: 1.1rem;
      font-weight: 700;
      opacity: 0.9;
      margin-bottom: 6px;
      position: relative;
      z-index: 2;
    }
    .calc-res-val {
      font-size: 4.4rem;
      font-weight: 950;
      line-height: 1;
      margin-bottom: 8px;
      position: relative;
      z-index: 2;
      letter-spacing: -2px;
    }
    .calc-res-sub {
      font-size: 1.25rem;
      font-weight: 800;
      color: var(--amber);
      margin-bottom: 12px;
      position: relative;
      z-index: 2;
    }
    .calc-res-note {
      font-size: 0.88rem;
      opacity: 0.8;
      margin-bottom: 32px;
      position: relative;
      z-index: 2;
      font-weight: 500;
    }
    .calc-res .btn {
      position: relative;
      z-index: 2;
    }

    /* Live comparison columns graphic */
    .calc-graphic {
      display: flex;
      justify-content: center;
      align-items: flex-end;
      gap: 32px;
      height: 130px;
      margin-bottom: 32px;
      position: relative;
      z-index: 2;
    }
    .cg-col {
      display: flex;
      flex-direction: column;
      align-items: center;
      width: 70px;
      height: 100%;
      justify-content: flex-end;
    }
    .cg-bar {
      width: 100%;
      border-radius: 12px 12px 0 0;
      transition: height 0.6s var(--ease);
      position: relative;
    }
    .cg-bar-old {
      background: rgba(255, 255, 255, 0.15);
      border: 1.5px dashed rgba(255, 255, 255, 0.4);
      height: 85%;
    }
    .cg-bar-new {
      background: linear-gradient(to top, var(--primary), #5cfba5);
      box-shadow: 0 4px 20px rgba(92, 251, 165, 0.3);
      height: 55%;
    }
    .cg-val-label {
      font-size: 0.8rem;
      font-weight: 700;
      margin-bottom: 6px;
      white-space: nowrap;
    }
    .cg-col-lbl {
      font-size: 0.78rem;
      font-weight: 700;
      opacity: 0.75;
      margin-top: 8px;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }

    /* How It Works with animated connector lines */
    .how-sec {
      background: var(--bg-alt);
    }
    .steps-container {
      position: relative;
      margin-top: 60px;
    }
    /* Connector line between steps */
    .steps-connector-line {
      position: absolute;
      top: 62px;
      left: 10%;
      right: 10%;
      height: 3px;
      background: var(--border);
      z-index: 1;
      display: block;
    }
    .steps-connector-progress {
      width: 0;
      height: 100%;
      background: linear-gradient(90deg, var(--primary), var(--blue));
      transition: width 1.5s var(--ease);
    }
    
    .steps {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 24px;
      position: relative;
      z-index: 2;
    }
    .step {
      background: var(--surface);
      border-radius: var(--r-lg);
      padding: 38px 26px;
      text-align: center;
      border: 1px solid var(--border);
      transition: all 0.4s var(--ease), background 0.5s var(--ease);
    }
    .step:hover {
      transform: translateY(-10px);
      box-shadow: var(--shadow-lg);
      border-color: var(--primary);
    }
    .step-n {
      width: 52px;
      height: 52px;
      border-radius: 16px;
      background: linear-gradient(135deg, var(--primary), var(--primary-hover));
      color: #fff;
      font-weight: 900;
      font-size: 1.3rem;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 22px;
      box-shadow: var(--shadow-primary);
      transition: transform 0.4s var(--spring);
    }
    .step:hover .step-n {
      transform: scale(1.1) rotate(6deg);
    }
    .step h3 {
      font-size: 1.15rem;
      font-weight: 800;
      margin-bottom: 10px;
      color: var(--text);
    }
    .step p {
      font-size: 0.9rem;
      color: var(--text-muted);
      line-height: 1.7;
    }

    /* Services cards */
    .svc-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 28px;
      margin-top: 60px;
    }
    .svc {
      background: var(--surface);
      border-radius: var(--r-lg);
      padding: 44px 34px;
      border: 1px solid var(--border);
      transition: all 0.45s var(--ease), background 0.5s var(--ease);
      position: relative;
      overflow: hidden;
    }
    .svc::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 4px;
      background: linear-gradient(90deg, var(--primary), #5cfba5);
      transform: scaleX(0);
      transform-origin: left;
      transition: transform 0.4s var(--ease);
    }
    .svc:hover::before {
      transform: scaleX(1);
    }
    .svc:hover {
      transform: translateY(-10px);
      box-shadow: var(--shadow-lg);
      border-color: var(--primary);
    }
    .svc-ico {
      width: 72px;
      height: 72px;
      border-radius: 22px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 2rem;
      margin-bottom: 26px;
      transition: transform 0.4s var(--spring);
    }
    .svc:hover .svc-ico {
      transform: scale(1.12) rotate(-6deg);
    }
    .ico-g { background: var(--primary-light); color: var(--primary); }
    .ico-b { background: var(--blue-light); color: var(--blue); }
    .ico-a { background: hsl(40, 100%, 93%); color: var(--amber); }
    
    body.dark .ico-g { background: rgba(16, 185, 129, 0.15); }
    body.dark .ico-b { background: rgba(59, 130, 246, 0.15); }
    body.dark .ico-a { background: rgba(245, 158, 11, 0.15); }

    .svc h3 {
      font-size: 1.3rem;
      font-weight: 800;
      margin-bottom: 12px;
      color: var(--text);
    }
    .svc p {
      color: var(--text-muted);
      font-size: 0.95rem;
      line-height: 1.7;
    }

    /* Testimonials Autoplay Slider */
    .testi-sec {
      background: var(--bg);
    }
    .slider-container {
      position: relative;
      max-width: 1000px;
      margin: 60px auto 0;
    }
    .testi-slider-wrap {
      overflow: hidden;
      cursor: grab;
      border-radius: var(--r-lg);
      padding: 10px;
    }
    .testi-slider-wrap:active {
      cursor: grabbing;
    }
    .testi-slider {
      display: flex;
      gap: 28px;
      transition: transform 0.5s var(--ease);
      user-select: none;
    }
    .tc {
      background: var(--surface);
      border-radius: var(--r-lg);
      padding: 44px;
      border: 1px solid var(--border);
      transition: all 0.4s var(--ease), background 0.5s var(--ease);
      flex: 0 0 calc(50% - 14px); /* 2 items visible on large screens */
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }
    .tc:hover {
      transform: translateY(-6px);
      box-shadow: var(--shadow-lg);
      border-color: var(--primary);
    }
    .tc-stars {
      color: var(--amber);
      font-size: 1rem;
      margin-bottom: 20px;
      display: flex;
      gap: 4px;
    }
    .tc-q {
      font-size: 1.05rem;
      color: var(--text);
      font-style: italic;
      margin-bottom: 32px;
      line-height: 1.8;
      font-weight: 500;
    }
    .tc-author {
      display: flex;
      align-items: center;
      gap: 16px;
    }
    .tc-av {
      width: 50px;
      height: 50px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #fff;
      font-weight: 900;
      font-size: 1.2rem;
      box-shadow: var(--shadow-sm);
    }
    .av-1 { background: linear-gradient(135deg, var(--primary), #5cfba5); }
    .av-2 { background: linear-gradient(135deg, var(--blue), #64b5f6); }
    .av-3 { background: linear-gradient(135deg, var(--amber), #ffd54f); }
    
    .tc-nm {
      font-weight: 800;
      font-size: 0.95rem;
      color: var(--text);
    }
    .tc-loc {
      color: var(--text-light);
      font-size: 0.82rem;
      font-weight: 600;
      margin-top: 1px;
    }
    
    /* Navigation chevrons for testimonials */
    .slider-btn {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      width: 50px;
      height: 50px;
      border-radius: 50%;
      background: var(--surface);
      border: 1px solid var(--border);
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--text);
      cursor: pointer;
      z-index: 5;
      transition: all 0.3s;
      box-shadow: var(--shadow-sm);
    }
    .slider-btn:hover {
      background: var(--primary);
      color: #fff;
      border-color: var(--primary);
      box-shadow: var(--shadow-primary);
    }
    .slider-btn-prev { left: -64px; }
    .slider-btn-next { right: -64px; }
    
    .slider-dots {
      display: flex;
      justify-content: center;
      gap: 8px;
      margin-top: 36px;
    }
    .slider-dot {
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: var(--border);
      cursor: pointer;
      transition: all 0.3s;
    }
    .slider-dot.active {
      width: 24px;
      border-radius: 10px;
      background: var(--primary);
    }

    /* FAQ accordion transitions */
    .faq-sec {
      background: var(--bg-alt);
    }
    .faq-list {
      max-width: 760px;
      margin: 56px auto 0;
    }
    .faq-it {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--r-md);
      margin-bottom: 14px;
      overflow: hidden;
      transition: all 0.4s var(--ease), background 0.5s var(--ease);
    }
    .faq-it:hover {
      box-shadow: var(--shadow-md);
      border-color: var(--primary);
    }
    .faq-q {
      width: 100%;
      padding: 22px 28px;
      background: none;
      display: flex;
      justify-content: space-between;
      align-items: center;
      cursor: pointer;
      font-weight: 750;
      font-size: 1.05rem;
      text-align: left;
      color: var(--text);
    }
    .faq-q i {
      font-size: 0.9rem;
      color: var(--text-light);
      transition: transform 0.4s var(--spring);
    }
    .faq-it.open .faq-q i {
      transform: rotate(180deg);
      color: var(--primary);
    }
    .faq-a {
      max-height: 0;
      overflow: hidden;
      padding: 0 28px;
      transition: max-height 0.45s var(--ease), padding 0.3s var(--ease);
      color: var(--text-muted);
      font-size: 0.95rem;
      line-height: 1.8;
    }
    .faq-it.open .faq-a {
      max-height: 280px;
      padding: 0 28px 22px;
    }

    /* Contact Section styling */
    .contact-sec {
      background: linear-gradient(135deg, hsl(150, 84%, 18%), hsl(223, 47%, 9%));
      color: #fff;
      overflow: hidden;
      position: relative;
    }
    .contact-sec::before {
      content: '';
      position: absolute;
      width: 600px;
      height: 600px;
      background: rgba(255, 255, 255, 0.03);
      border-radius: 50%;
      top: -200px;
      right: -100px;
    }
    .contact-sec::after {
      content: '';
      position: absolute;
      width: 400px;
      height: 400px;
      background: rgba(16, 185, 129, 0.05);
      border-radius: 50%;
      bottom: -100px;
      left: -80px;
    }
    
    .ct-grid {
      display: grid;
      grid-template-columns: 1fr 1.05fr;
      gap: 80px;
      align-items: center;
      position: relative;
      z-index: 2;
    }
    .ct-left h2 {
      font-size: clamp(2.2rem, 4vw, 3.4rem);
      font-weight: 900;
      line-height: 1.1;
      margin-bottom: 22px;
      letter-spacing: -1.5px;
    }
    .ct-left > p {
      font-size: 1.15rem;
      opacity: 0.85;
      margin-bottom: 40px;
      line-height: 1.8;
    }
    .ct-links {
      display: flex;
      flex-direction: column;
      gap: 16px;
    }
    .ct-card {
      display: flex;
      align-items: center;
      gap: 20px;
      padding: 20px 24px;
      background: rgba(255, 255, 255, 0.06);
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: var(--r-md);
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);
      transition: all 0.35s var(--ease);
    }
    .ct-card:hover {
      background: rgba(255, 255, 255, 0.12);
      transform: translateX(8px);
      border-color: var(--primary);
    }
    .ct-card i {
      font-size: 2rem;
      color: var(--primary);
    }
    .ct-card-t {
      font-weight: 800;
      font-size: 1.05rem;
    }
    .ct-card-s {
      font-size: 0.88rem;
      opacity: 0.75;
      margin-top: 2px;
      font-weight: 600;
    }

    /* Form Fields with Floating Labels */
    .ct-form {
      background: var(--surface);
      color: var(--text);
      border-radius: var(--r-2xl);
      padding: 50px;
      box-shadow: var(--shadow-lg);
      position: relative;
      transition: background 0.5s var(--ease);
    }
    .ct-form::before {
      content: '';
      position: absolute;
      inset: 0;
      border-radius: var(--r-2xl);
      padding: 1px;
      background: linear-gradient(135deg, var(--primary), transparent);
      -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
      -webkit-mask-composite: xor;
      mask-composite: exclude;
      pointer-events: none;
    }
    .ct-form h3 {
      font-size: 1.85rem;
      font-weight: 900;
      margin-bottom: 8px;
      letter-spacing: -0.5px;
    }
    .ct-form > p {
      color: var(--text-light);
      margin-bottom: 36px;
      font-size: 0.92rem;
      font-weight: 600;
    }
    
    .fg-floating {
      position: relative;
      margin-bottom: 24px;
    }
    .fi {
      width: 100%;
      padding: 16px 20px;
      border-radius: 14px;
      border: 2px solid var(--border);
      background: var(--bg);
      color: var(--text);
      font-size: 0.95rem;
      font-weight: 600;
      transition: all 0.3s;
    }
    .fi:focus {
      border-color: var(--primary);
      background: var(--surface);
      box-shadow: 0 0 0 4px var(--primary-glow);
    }
    
    /* Floating label animation */
    .fg-floating label {
      position: absolute;
      left: 20px;
      top: 50%;
      transform: translateY(-50%);
      color: var(--text-light);
      transition: all 0.3s var(--ease);
      pointer-events: none;
      font-weight: 600;
    }
    textarea.fi {
      resize: vertical;
      min-height: 120px;
    }
    .fg-floating textarea ~ label {
      top: 26px;
      transform: none;
    }
    
    /* Label shifts up on focus or if input has text */
    .fi:focus ~ label,
    .fi:not(:placeholder-shown) ~ label {
      top: 0;
      left: 14px;
      transform: translateY(-50%);
      font-size: 0.78rem;
      background: var(--surface);
      padding: 0 8px;
      color: var(--primary);
      font-weight: 700;
    }

    /* Footer */
    footer {
      background: #05080e;
      color: #fff;
      padding: 80px 0 40px;
      text-align: center;
      position: relative;
      z-index: 10;
    }
    .ft-ico {
      width: 58px;
      height: 58px;
      border-radius: 16px;
      background: linear-gradient(135deg, var(--primary), var(--primary-hover));
      display: inline-flex;
      align-items: center;
      justify-content: center;
      font-size: 1.5rem;
      color: #fff;
      margin-bottom: 22px;
      box-shadow: var(--shadow-primary);
    }
    footer h2 {
      font-size: 1.75rem;
      font-weight: 900;
      margin-bottom: 12px;
      letter-spacing: -0.5px;
    }
    .ft-desc {
      color: #94a3b8;
      max-width: 500px;
      margin: 0 auto;
      font-size: 0.95rem;
      line-height: 1.7;
    }
    .ft-soc {
      display: flex;
      justify-content: center;
      gap: 16px;
      margin: 32px 0;
      font-size: 1.3rem;
    }
    .ft-soc a {
      width: 48px;
      height: 48px;
      border-radius: 14px;
      background: rgba(255, 255, 255, 0.05);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #94a3b8;
      transition: all 0.3s var(--ease);
    }
    .ft-soc a:hover {
      background: var(--primary);
      color: #fff;
      transform: translateY(-4px) rotate(8deg);
      box-shadow: var(--shadow-primary);
    }
    .ft-copy {
      color: #475569;
      font-size: 0.85rem;
      margin-top: 10px;
      font-weight: 500;
    }

    /* Floating WhatsApp Button */
    .fwa {
      position: fixed;
      bottom: 26px;
      right: 26px;
      z-index: 999;
      width: 62px;
      height: 62px;
      border-radius: 50%;
      background: #25D366;
      color: #fff;
      font-size: 2rem;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 10px 30px rgba(37, 211, 102, 0.45);
      transition: all 0.3s var(--spring);
      animation: wa-bob 3s ease-in-out infinite;
    }
    .fwa:hover {
      transform: scale(1.15) rotate(10deg);
      box-shadow: 0 14px 40px rgba(37, 211, 102, 0.65);
      animation: none;
    }
    @keyframes wa-bob {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-6px); }
    }

    /* ══════════════════════════════════════════════
       RESPONSIVE ADAPTABILITY
       ══════════════════════════════════════════════ */
    @media (max-width: 1140px) {
      .slider-btn-prev { left: -15px; }
      .slider-btn-next { right: -15px; }
    }

    @media (max-width: 1024px) {
      .hero-grid, .calc-grid, .ct-grid {
        grid-template-columns: 1fr;
      }
      .hero-left {
        text-align: center;
      }
      .hero-desc {
        margin: 0 auto 40px;
      }
      .hero-btns {
        justify-content: center;
      }
      .hero-stats {
        justify-content: center;
      }
      .hero-right {
        margin-top: 48px;
        max-width: 500px;
        margin-left: auto;
        margin-right: auto;
      }
      .hero-glass {
        transform: none;
      }
      .hero-glass:hover {
        transform: none;
      }
      .steps-connector-line {
        display: none;
      }
      .steps {
        grid-template-columns: repeat(2, 1fr);
      }
      .tc {
        flex: 0 0 100%; /* Single card visible at a time */
      }
      .slider-btn-prev { left: 0px; }
      .slider-btn-next { right: 0px; }
    }

    @media (max-width: 768px) {
      .nav-pills { display: none; }
      .burger { display: flex; }
      .hero-stats {
        flex-direction: column;
        gap: 20px;
        align-items: center;
      }
      .comp-wrap, .comp-head { display: none; }
      .comp-mob { display: block !important; }
      .svc-grid { grid-template-columns: 1fr; }
      .steps { grid-template-columns: 1fr; }
      .sec-title { font-size: 1.95rem !important; }
      .calc-wrap { padding: 36px 20px; }
      .ct-form { padding: 36px 20px; }
      section { padding: 80px 0; }
      .calc-tabs {
        flex-direction: column;
        border-radius: 20px;
      }
      .calc-tab {
        border-radius: 14px;
        padding: 12px 20px;
      }
    }

    @media (max-width: 480px) {
      .hero-title { letter-spacing: -1px; }
      .hero-btns .btn { width: 100%; }
    }
  </style>
</head>
<body>

<!-- Noise Overlay -->
<div class="noise-bg"></div>

<!-- Loader -->
<div class="loader" id="ld">
  <div class="loader-ring"></div>
  <div class="loader-label">Jose Asesor Energético</div>
</div>

<!-- Floating WA -->
<a href="https://wa.me/34675205144" target="_blank" class="fwa" aria-label="WhatsApp"><i class="fab fa-whatsapp"></i></a>

<!-- Mobile Menu -->
<div class="mob-menu" id="mobMenu">
  <a href="#companias" onclick="closeMob()">Compañías</a>
  <a href="#calculadora" onclick="closeMob()">Calculadora</a>
  <a href="#como" onclick="closeMob()">Proceso</a>
  <a href="#servicios" onclick="closeMob()">Servicios</a>
  <a href="#opiniones" onclick="closeMob()">Opiniones</a>
  <a href="#faq" onclick="closeMob()">FAQ</a>
  <a href="#contacto" onclick="closeMob()" class="btn btn-primary" style="margin-top:14px">Contacto</a>
</div>

<!-- HEADER -->
<header id="hdr">
  <div class="container nav">
    <a href="#" class="logo">
      <div class="logo-box">
        <!-- Path pointing to subfolder for local assets -->
        <img src="paginaweb/logos/logo.png" alt="Logo" onerror="this.parentElement.innerHTML='<i class=\'fas fa-bolt\'></i>'">
      </div>
      <div>
        <!-- Inline SVG logo text for absolute perfection in outlines -->
        <svg viewBox="0 0 130 22" width="130" height="22" style="display: block; margin-bottom: 2px;" aria-label="Jose Asesor">
          <text x="0" y="17" font-family="'Outfit', sans-serif" font-size="18" font-weight="900" fill="#ffffff" stroke="#000000" stroke-width="3" paint-order="stroke fill" stroke-linejoin="round" letter-spacing="-0.5">Jose Asesor</text>
        </svg>
        <div class="logo-sub">Energético</div>
      </div>
    </a>

    <nav class="nav-pills" id="navPills">
      <a href="#companias">Compañías</a>
      <a href="#calculadora">Calculadora</a>
      <a href="#como">Proceso</a>
      <a href="#servicios">Servicios</a>
      <a href="#opiniones">Opiniones</a>
      <a href="#faq">FAQ</a>
    </nav>

    <div class="nav-right">
      <button class="theme-btn" id="thBtn" aria-label="Cambiar Tema">
        <div class="th-icon-wrap">
          <i class="fas fa-sun"></i>
          <i class="fas fa-moon"></i>
        </div>
      </button>
      
      <a href="#contacto" class="btn btn-primary" style="padding:10px 24px; font-size:0.85rem">Contacto</a>
      <button class="burger" id="burg" aria-label="Menú">
        <span></span>
        <span></span>
        <span></span>
      </button>
    </div>
  </div>
</header>

<!-- HERO SECTION -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-ov"></div>
  <div class="hero-orb hero-orb-1"></div>
  <div class="hero-orb hero-orb-2"></div>
  <div class="hero-orb hero-orb-3"></div>
  <canvas id="pCanvas"></canvas>

  <div class="container hero-grid">
    <div class="hero-left rv">
      <div class="hero-badge"><i class="fas fa-bolt"></i> Estudio gratuito sin compromiso</div>
      <!-- Single H1 for proper semantic SEO hierarchy -->
      <h1 class="hero-title">Reduce tu<br><span class="gradient-text">factura</span> de luz y gas</h1>
      <p class="hero-desc">Encuentro las mejores tarifas energéticas para hogares y empresas. Sin coste, sin complicaciones y con resultados 100% garantizados.</p>
      <div class="hero-btns">
        <a href="https://wa.me/34675205144" target="_blank" class="btn btn-primary btn-lg"><i class="fab fa-whatsapp"></i> Hablar por WhatsApp</a>
        <a href="#contacto" class="btn btn-ghost btn-lg">Solicitar estudio</a>
      </div>
      <div class="hero-stats">
        <div><div class="h-stat-val" data-c="450">+450</div><div class="h-stat-lbl">Clientes activos</div></div>
        <div><div class="h-stat-val" data-c="32" data-s="%">32%</div><div class="h-stat-lbl">Ahorro medio</div></div>
        <div><div class="h-stat-val" data-c="8" data-s=" años">8 años</div><div class="h-stat-lbl">De experiencia</div></div>
      </div>
    </div>

    <!-- 3D Parallax Interactive Glass Card -->
    <div class="hero-right rv" style="transition-delay:0.15s">
      <div class="hero-glass" id="parallaxCard">
        <div class="glare-effect" id="cardGlare"></div>
        <div class="hero-card">
          <div class="hc-top">
            <div>
              <small>Ahorro estimado anual</small>
              <div class="hc-amount">682€</div>
            </div>
            <div class="hc-icon"><i class="fas fa-leaf"></i></div>
          </div>
          <div class="prog">
            <div class="prog-head"><span>Factura anterior</span><span style="color:var(--red)">189€/mes</span></div>
            <div class="prog-bar"><div class="prog-fill fill-r" data-w="85"></div></div>
          </div>
          <div class="prog">
            <div class="prog-head"><span>Nueva tarifa optimizada</span><span style="color:var(--primary)">119€/mes</span></div>
            <div class="prog-bar"><div class="prog-fill fill-g" data-w="55"></div></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Wave Section Divider -->
<div class="wave-div"><svg viewBox="0 0 1440 80" preserveAspectRatio="none"><path d="M0,40 C360,100 1080,0 1440,40 L1440,80 L0,80Z"></path></svg></div>

<!-- TRUST STRIP -->
<div class="trust">
  <div class="container">
    <p class="trust-lbl">Trabajamos con las principales comercializadoras</p>
    <div class="trust-row">
      <!-- References look inside subdirectorypaginaweb -->
      <img src="paginaweb/logos/endesa.png" alt="Endesa" onerror="this.src='https://placehold.co/100x40/10b981/fff?text=ENDESA'">
      <img src="paginaweb/logos/iberdrola.png" alt="Iberdrola" onerror="this.src='https://placehold.co/100x40/3b82f6/fff?text=IBERDROLA'">
      <img src="paginaweb/logos/naturgy.png" alt="Naturgy" onerror="this.src='https://placehold.co/100x40/f59e0b/fff?text=NATURGY'">
      <img src="paginaweb/logos/repsol.png" alt="Repsol" onerror="this.src='https://placehold.co/100x40/f97316/fff?text=REPSOL'">
      <img src="paginaweb/logos/octopus.png" alt="Octopus" onerror="this.src='https://placehold.co/100x40/a855f7/fff?text=OCTOPUS'">
    </div>
  </div>
</div>

<!-- COMPANIES -->
<section id="companias" class="comp-sec">
  <div class="container">
    <div class="text-center rv">
      <div class="sec-badge"><i class="fas fa-building"></i> Comparador</div>
      <h2 class="sec-title">Comparamos por ti las mejores ofertas</h2>
      <p class="sec-desc">Analizamos diariamente las tarifas reales del mercado energético para garantizarte el mayor ahorro.</p>
    </div>
    
    <div class="comp-wrap rv-s">
      <div class="comp-head">
        <div>Compañía y Plan</div>
        <div>Precio de Referencia</div>
        <div>Público Ideal</div>
      </div>
      <div class="comp-r">
        <div class="comp-id">
          <img src="paginaweb/logos/endesa.png" alt="Endesa" class="comp-logo" onerror="this.src='https://placehold.co/50x50/10b981/fff?text=E'">
          <div><div class="comp-nm">ENDESA</div><div class="comp-pl">Tarifa One Luz</div></div>
        </div>
        <div class="comp-pr">0,118€ / kWh</div>
        <div><span class="tag tg-g"><i class="fas fa-check-circle"></i> Hogar Estándar</span></div>
      </div>
      <div class="comp-r">
        <div class="comp-id">
          <img src="paginaweb/logos/iberdrola.png" alt="Iberdrola" class="comp-logo" onerror="this.src='https://placehold.co/50x50/3b82f6/fff?text=I'">
          <div><div class="comp-nm">IBERDROLA</div><div class="comp-pl">Plan Estable</div></div>
        </div>
        <div class="comp-pr">0,109€ / kWh</div>
        <div><span class="tag tg-b"><i class="fas fa-star"></i> Familias</span></div>
      </div>
      <div class="comp-r">
        <div class="comp-id">
          <img src="paginaweb/logos/naturgy.png" alt="Naturgy" class="comp-logo" onerror="this.src='https://placehold.co/50x50/f59e0b/fff?text=N'">
          <div><div class="comp-nm">NATURGY</div><div class="comp-pl">Tarifa Flexible</div></div>
        </div>
        <div class="comp-pr">0,113€ / kWh</div>
        <div><span class="tag tg-a"><i class="fas fa-briefcase"></i> Negocios / Pymes</span></div>
      </div>
      <div class="comp-r">
        <div class="comp-id">
          <img src="paginaweb/logos/repsol.png" alt="Repsol" class="comp-logo" onerror="this.src='https://placehold.co/50x50/f97316/fff?text=R'">
          <div><div class="comp-nm">REPSOL</div><div class="comp-pl">Ahorro Plus</div></div>
        </div>
        <div class="comp-pr">0,116€ / kWh</div>
        <div><span class="tag tg-o"><i class="fas fa-fire"></i> Luz + Gas</span></div>
      </div>
      <div class="comp-r">
        <div class="comp-id">
          <img src="paginaweb/logos/octopus.png" alt="Octopus" class="comp-logo" onerror="this.src='https://placehold.co/50x50/a855f7/fff?text=O'">
          <div><div class="comp-nm">OCTOPUS ENERGY</div><div class="comp-pl">Octopus Relax</div></div>
        </div>
        <div class="comp-pr">0,105€ / kWh</div>
        <div><span class="tag tg-p"><i class="fas fa-seedling"></i> Hogar Ecológico</span></div>
      </div>
    </div>

    <!-- Mobile View for Companies -->
    <div class="comp-mob">
      <div class="comp-mc">
        <img src="paginaweb/logos/endesa.png" alt="Endesa" onerror="this.src='https://placehold.co/44x44/10b981/fff?text=E'">
        <div class="comp-mc-info"><h4>ENDESA</h4><p>Tarifa One Luz · Hogar</p></div>
        <div class="comp-mc-pr">0,118€</div>
      </div>
      <div class="comp-mc">
        <img src="paginaweb/logos/iberdrola.png" alt="Iberdrola" onerror="this.src='https://placehold.co/44x44/3b82f6/fff?text=I'">
        <div class="comp-mc-info"><h4>IBERDROLA</h4><p>Plan Estable · Familias</p></div>
        <div class="comp-mc-pr">0,109€</div>
      </div>
      <div class="comp-mc">
        <img src="paginaweb/logos/naturgy.png" alt="Naturgy" onerror="this.src='https://placehold.co/44x44/f59e0b/fff?text=N'">
        <div class="comp-mc-info"><h4>NATURGY</h4><p>Tarifa Flexible · Pymes</p></div>
        <div class="comp-mc-pr">0,113€</div>
      </div>
      <div class="comp-mc">
        <img src="paginaweb/logos/repsol.png" alt="Repsol" onerror="this.src='https://placehold.co/44x44/f97316/fff?text=R'">
        <div class="comp-mc-info"><h4>REPSOL</h4><p>Ahorro Plus · Gas</p></div>
        <div class="comp-mc-pr">0,116€</div>
      </div>
      <div class="comp-mc">
        <img src="paginaweb/logos/octopus.png" alt="Octopus" onerror="this.src='https://placehold.co/44x44/a855f7/fff?text=O'">
        <div class="comp-mc-info"><h4>OCTOPUS ENERGY</h4><p>Octopus Relax · Eco</p></div>
        <div class="comp-mc-pr">0,105€</div>
      </div>
    </div>
  </div>
</section>

<!-- DUAL INTERACTIVE CALCULATOR -->
<section id="calculadora" class="calc-sec">
  <div class="container">
    <div class="text-center rv">
      <div class="sec-badge"><i class="fas fa-calculator"></i> Ahorro en tiempo real</div>
      <h2 class="sec-title">Calculadora de Optimización</h2>
      <p class="sec-desc">Calcula de forma interactiva cuánto pagarías de menos con un estudio energético a medida.</p>
    </div>
    
    <div class="calc-tabs rv">
      <div class="calc-tab active" data-target="calc-luz"><i class="fas fa-bolt"></i> Luz y Gas</div>
      <div class="calc-tab" data-target="calc-solar"><i class="fas fa-solar-panel"></i> Energía Solar</div>
    </div>

    <div class="calc-wrap rv-s">
      <!-- LUZ PANE -->
      <div class="calc-pane active" id="calc-luz">
        <div class="calc-grid">
          <div class="calc-form">
            <div class="calc-rng-wrap">
              <label for="bSlider">Tu factura mensual actual</label>
              <div class="rng-val"><span id="bDisp">120</span>€/mes</div>
              <input type="range" id="bSlider" class="rng" min="40" max="400" value="120">
              <div class="rng-lim"><span>40€</span><span>400€</span></div>
            </div>
            <div>
              <label for="tSel">Tipo de vivienda / local</label>
              <select id="tSel" class="calc-sel">
                <option value="1">🏠 Piso o apartamento estándar</option>
                <option value="1.25">🏡 Chalet o casa unifamiliar</option>
                <option value="1.6">🏢 Local comercial u Oficina</option>
              </select>
            </div>
          </div>
          
          <div class="calc-res">
            <div class="calc-graphic">
              <div class="cg-col">
                <div class="cg-val-label"><span id="cgOldVal">120</span>€</div>
                <div class="cg-bar cg-bar-old"></div>
                <div class="cg-col-lbl">Actual</div>
              </div>
              <div class="cg-col">
                <div class="cg-val-label" style="color:#5cfba5"><span id="cgNewVal">84</span>€</div>
                <div class="cg-bar cg-bar-new" id="cgNewBar"></div>
                <div class="cg-col-lbl" style="color:#5cfba5">Con Jose</div>
              </div>
            </div>
            <div class="calc-res-lbl">Ahorro anual aproximado</div>
            <div class="calc-res-val" id="sDisp">432€</div>
            <div class="calc-res-note">Optimización media del 30% en potencia y tarifa</div>
            <a href="#contacto" class="btn btn-white">Obtener estudio exacto</a>
          </div>
        </div>
      </div>

      <!-- SOLAR PANE -->
      <div class="calc-pane" id="calc-solar">
        <div class="calc-grid">
          <div class="calc-form">
            <div class="calc-rng-wrap">
              <label for="solSlider">Gasto actual en electricidad</label>
              <div class="rng-val"><span id="solDisp">150</span>€/mes</div>
              <input type="range" id="solSlider" class="rng" min="60" max="500" value="150">
              <div class="rng-lim"><span>60€</span><span>500€</span></div>
            </div>
            <div>
              <label for="solSel">Exposición solar / Orientación</label>
              <select id="solSel" class="calc-sel">
                <option value="1">☀️ Orientación Sur (Óptima - 100% eficiencia)</option>
                <option value="0.85">🌤️ Orientación Este/Oeste (Muy Buena - 85% ef.)</option>
                <option value="0.7">⛅ Orientación Norte (Favorable - 70% ef.)</option>
              </select>
            </div>
          </div>
          
          <div class="calc-res">
            <div class="calc-graphic">
              <div class="cg-col">
                <div class="cg-val-label"><span id="cgOldSol">150</span>€</div>
                <div class="cg-bar cg-bar-old"></div>
                <div class="cg-col-lbl">Actual</div>
              </div>
              <div class="cg-col">
                <div class="cg-val-label" style="color:#ffd54f"><span id="cgNewSol">45</span>€</div>
                <div class="cg-bar cg-bar-new" id="cgNewSolBar" style="background: linear-gradient(to top, var(--amber), #ffe082); box-shadow: 0 4px 20px rgba(255, 213, 79, 0.3);"></div>
                <div class="cg-col-lbl" style="color:#ffd54f">Solar</div>
              </div>
            </div>
            <div class="calc-res-lbl">Ahorro total a 10 años</div>
            <div class="calc-res-val" id="solSave" style="color:#ffd54f">12.600€</div>
            <div class="calc-res-sub" id="solAmort">Amortización en 4.5 años</div>
            <div class="calc-res-note">Ahorro medio superior al 70% de consumo directo</div>
            <a href="#contacto" class="btn btn-white">Calcular viabilidad técnica</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- HOW IT WORKS WITH PROGRESS CONNECTORS -->
<section id="como" class="how-sec">
  <div class="container">
    <div class="text-center rv">
      <div class="sec-badge"><i class="fas fa-route"></i> Metodología</div>
      <h2 class="sec-title">¿Cómo conseguimos tu ahorro?</h2>
      <p class="sec-desc">Un proceso transparente en 4 sencillos pasos. Sin papeleos ni dolores de cabeza.</p>
    </div>
    
    <div class="steps-container">
      <div class="steps-connector-line">
        <div class="steps-connector-progress" id="scrollProgressLine"></div>
      </div>
      <div class="steps">
        <div class="step rv" style="transition-delay:0.05s">
          <div class="step-n">1</div>
          <h3>Envías tu factura</h3>
          <p>Por WhatsApp o email. Solo necesito una foto o PDF de tu última factura de luz o gas.</p>
        </div>
        <div class="step rv" style="transition-delay:0.12s">
          <div class="step-n">2</div>
          <h3>Análisis Gratuito</h3>
          <p>Comparo minuciosamente las potencias contratadas y tarifas con las ofertas del mercado libre.</p>
        </div>
        <div class="step rv" style="transition-delay:0.19s">
          <div class="step-n">3</div>
          <h3>Te presento opciones</h3>
          <p>Te explico de forma clara y sin tecnicismos la propuesta que más te beneficia para que tú elijas.</p>
        </div>
        <div class="step rv" style="transition-delay:0.26s">
          <div class="step-n">4</div>
          <h3>Gestión Llave en Mano</h3>
          <p>Yo me encargo de todo el trámite con la distribuidora. Tú solo ves descender tu factura.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="servicios">
  <div class="container">
    <div class="text-center rv">
      <div class="sec-badge"><i class="fas fa-star"></i> Servicios</div>
      <h2 class="sec-title">Soluciones de Ahorro Integral</h2>
      <p class="sec-desc">Servicios avanzados enfocados en exprimir al máximo el rendimiento de cada euro gastado.</p>
    </div>
    <div class="svc-grid">
      <div class="svc rv" style="transition-delay:0.05s">
        <div class="svc-ico ico-g"><i class="fas fa-lightbulb"></i></div>
        <h3>Optimización Tarifaria</h3>
        <p>Ajustamos tus potencias de forma exacta a tu perfil de consumo y te posicionamos en la mejor comercializadora activa en España.</p>
      </div>
      <div class="svc rv" style="transition-delay:0.12s">
        <div class="svc-ico ico-b"><i class="fas fa-solar-panel"></i></div>
        <h3>Estudios Solares</h3>
        <p>Te asesoramos en la compra, dimensionado de paneles solares, gestión de subvenciones públicas y optimización de excedentes vertidos.</p>
      </div>
      <div class="svc rv" style="transition-delay:0.19s">
        <div class="svc-ico ico-a"><i class="fas fa-file-signature"></i></div>
        <h3>Certificados Energéticos</h3>
        <p>Tramitamos de forma ágil y económica el certificado oficial de eficiencia, obligatorio por ley para procesos de venta o alquiler.</p>
      </div>
    </div>
  </div>
</section>

<!-- TESTIMONIALS DRAGGABLE CAROUSEL -->
<section id="opiniones" class="testi-sec">
  <div class="container">
    <div class="text-center rv">
      <div class="sec-badge"><i class="fas fa-heart"></i> Testimonios</div>
      <h2 class="sec-title">Lo que dicen mis clientes</h2>
      <p class="sec-desc">La mejor garantía es el ahorro recurrente reflejado en las facturas de quienes ya confían en mí.</p>
    </div>
    
    <div class="slider-container rv-s">
      <!-- Chevrons for manual control -->
      <button class="slider-btn slider-btn-prev" id="sliderPrev" aria-label="Anterior"><i class="fas fa-chevron-left"></i></button>
      <button class="slider-btn slider-btn-next" id="sliderNext" aria-label="Siguiente"><i class="fas fa-chevron-right"></i></button>
      
      <div class="testi-slider-wrap" id="tSliderWrap">
        <div class="testi-slider" id="tSlider">
          <div class="tc">
            <div>
              <div class="tc-stars">
                <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
              </div>
              <p class="tc-q">"Jose es un profesional de diez. Consiguió rebajar mi factura mensual a casi la mitad sin cambiar mis hábitos."</p>
            </div>
            <div class="tc-author">
              <div class="tc-av av-1">L</div>
              <div>
                <div class="tc-nm">Laura Martínez</div>
                <div class="tc-loc">Madrid</div>
              </div>
            </div>
          </div>
          <div class="tc">
            <div>
              <div class="tc-stars">
                <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
              </div>
              <p class="tc-q">"Me daba mucha pereza ponerme a buscar compañías, pero Jose se ocupó de toda la burocracia. Transparente y rapidísimo."</p>
            </div>
            <div class="tc-author">
              <div class="tc-av av-2">M</div>
              <div>
                <div class="tc-nm">Miguel Torres</div>
                <div class="tc-loc">Valencia</div>
              </div>
            </div>
          </div>
          <div class="tc">
            <div>
              <div class="tc-stars">
                <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
              </div>
              <p class="tc-q">"Sin duda el mejor servicio. Ahora entiendo perfectamente lo que pago de luz y mi ahorro es del 40% mensual."</p>
            </div>
            <div class="tc-author">
              <div class="tc-av av-3">C</div>
              <div>
                <div class="tc-nm">Carmen Ruiz</div>
                <div class="tc-loc">Barcelona</div>
              </div>
            </div>
          </div>
          <div class="tc">
            <div>
              <div class="tc-stars">
                <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star-half-alt"></i>
              </div>
              <p class="tc-q">"Instalamos los paneles solares siguiendo sus consejos. La amortización está yendo tal y como nos prometió. Un gran acierto."</p>
            </div>
            <div class="tc-author">
              <div class="tc-av av-1">R</div>
              <div>
                <div class="tc-nm">Roberto Díaz</div>
                <div class="tc-loc">Sevilla</div>
              </div>
            </div>
          </div>
        </div>
      </div>
      
      <div class="slider-dots" id="sliderDots"></div>
    </div>
  </div>
</section>

<!-- FAQ ACCORDION -->
<section id="faq" class="faq-sec">
  <div class="container">
    <div class="text-center rv">
      <div class="sec-badge"><i class="fas fa-question-circle"></i> Preguntas</div>
      <h2 class="sec-title">Dudas frecuentes</h2>
      <p class="sec-desc">Respondo a las principales inquietudes para que te sientas 100% seguro del cambio.</p>
    </div>
    
    <div class="faq-list rv">
      <div class="faq-it">
        <button class="faq-q">¿El estudio y análisis tiene algún coste para mí? <i class="fas fa-chevron-down"></i></button>
        <div class="faq-a">Ninguno. El estudio y toda mi asesoría personalizada son 100% gratuitos. Mis honorarios son abonados directamente por la comercializadora correspondiente, por lo que tú solo te beneficias del ahorro.</div>
      </div>
      <div class="faq-it">
        <button class="faq-q">¿Cuánto tarda en completarse la optimización? <i class="fas fa-chevron-down"></i></button>
        <div class="faq-a">El proceso de portabilidad o alta suele tardar entre 7 y 20 días hábiles. En ningún momento te quedarás sin suministro y todo el papeleo corre por mi cuenta.</div>
      </div>
      <div class="faq-it">
        <button class="faq-q">¿Existe riesgo de quedarme sin luz o gas en el proceso? <i class="fas fa-chevron-down"></i></button>
        <div class="faq-a">Rotundamente no. La continuidad del suministro eléctrico y de gas está totalmente garantizada por la ley de competencia en España durante cualquier cambio de comercializadora.</div>
      </div>
      <div class="faq-it">
        <button class="faq-q">¿Asesoras también sobre autoconsumo solar? <i class="fas fa-chevron-down"></i></button>
        <div class="faq-a">Sí. Realizo estudios completos de viabilidad solar fotovoltaica para tejados residenciales y naves industriales, analizando consumos, orientación, costes de instalación, subvenciones y retornos de inversión.</div>
      </div>
      <div class="faq-it">
        <button class="faq-q">¿Qué datos o documentos necesitas de mi factura? <i class="fas fa-chevron-down"></i></button>
        <div class="faq-a">Simplemente necesito una captura de pantalla legible o el PDF de tu última factura completa. Con el código CUPS y tu gráfico histórico de consumo en mano puedo realizar el estudio comparativo.</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT FORM WITH FLOATING LABELS -->
<section id="contacto" class="contact-sec">
  <div class="container ct-grid">
    <div class="ct-left rv-l">
      <h2>Empieza a pagar<br>menos desde hoy</h2>
      <p>Envía tu última factura y te preparo una comparativa detallada y sin ningún tipo de compromiso.</p>
      <div class="ct-links">
        <a href="https://wa.me/34675205144" target="_blank" class="ct-card">
          <i class="fab fa-whatsapp"></i>
          <div>
            <div class="ct-card-t">WhatsApp Directo</div>
            <div class="ct-card-s">675 205 144</div>
          </div>
        </a>
        <a href="mailto:joseasesorenergetico@gmail.com" class="ct-card">
          <i class="far fa-envelope"></i>
          <div>
            <div class="ct-card-t">Correo Electrónico</div>
            <div class="ct-card-s">joseasesorenergetico@gmail.com</div>
          </div>
        </a>
      </div>
    </div>
    
    <div class="ct-form rv-r">
      <h3>Solicitar Estudio Gratuito</h3>
      <p>Te responderé con tu informe de ahorro en menos de 24 horas.</p>
      <form action="https://formsubmit.co/joseasesorenergetico@gmail.com" method="POST" id="contactForm">
        <input type="hidden" name="_captcha" value="false">
        <input type="hidden" name="_next" value="https://wa.me/34675205144">
        
        <div class="fg-floating">
          <input type="text" name="nombre" id="formName" class="fi" placeholder=" " required>
          <label for="formName">Tu Nombre Completo</label>
        </div>
        
        <div class="fg-floating">
          <input type="tel" name="telefono" id="formTel" class="fi" placeholder=" " required>
          <label for="formTel">Número de Teléfono</label>
        </div>
        
        <div class="fg-floating">
          <textarea name="mensaje" id="formMsg" class="fi" placeholder=" " rows="4"></textarea>
          <label for="formMsg">¿Quieres comentar algo sobre tus facturas?</label>
        </div>
        
        <button type="submit" class="btn btn-primary btn-lg" style="width:100%"><i class="fas fa-paper-plane"></i> Solicitar Comparativa Gratuita</button>
      </form>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="container">
    <div class="ft-ico"><i class="fas fa-bolt"></i></div>
    <h2>Jose Asesor Energético</h2>
    <p class="ft-desc">Especialistas con dilatada experiencia en consultoría y optimización de tarifas eléctricas, autoconsumo fotovoltaico y certificados oficiales.</p>
    <div class="ft-soc">
      <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
      <a href="#" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
      <a href="https://wa.me/34675205144" aria-label="WhatsApp"><i class="fab fa-whatsapp"></i></a>
    </div>
    <p class="ft-copy">&copy; 2026 Jose Asesor Energético · Todos los derechos reservados · Diseñado con Excelencia</p>
  </div>
</footer>

<script>
(function(){
  'use strict';

  // ──── LOADER ────
  const ld = document.getElementById('ld');
  function hideLd(){
    if(ld) ld.classList.add('done');
  }
  window.addEventListener('load', () => setTimeout(hideLd, 400));
  setTimeout(hideLd, 1800); // Fail-safe

  // ──── THEME SWITCHER LOGIC ────
  const thBtn = document.getElementById('thBtn');
  if(localStorage.getItem('theme') === 'dark'){
    document.body.classList.add('dark');
  }
  if(thBtn) {
    thBtn.onclick = () => {
      document.body.classList.toggle('dark');
      localStorage.setItem('theme', document.body.classList.contains('dark') ? 'dark' : 'light');
    };
  }

  // ──── HEADER SCROLL & ACTIVE DOTS ────
  const hdr = document.getElementById('hdr');
  const sections = document.querySelectorAll('section[id]');
  const navLinks = document.querySelectorAll('.nav-pills a');
  
  const onScroll = () => {
    if(hdr) hdr.classList.toggle('stuck', window.scrollY > 60);
    
    let cur = '';
    sections.forEach(s => {
      if(s.getBoundingClientRect().top < 220) {
        cur = s.id;
      }
    });
    navLinks.forEach(a => {
      a.classList.toggle('active', a.getAttribute('href') === '#' + cur);
    });

    // Connector Line in Steps Section
    const comoSec = document.getElementById('como');
    const progressLine = document.getElementById('scrollProgressLine');
    if(comoSec && progressLine) {
      const box = comoSec.getBoundingClientRect();
      const pct = Math.min(Math.max((window.innerHeight - box.top) / (box.height + 100), 0), 1);
      progressLine.style.width = (pct * 100) + '%';
    }
  };
  window.addEventListener('scroll', onScroll, {passive: true});
  onScroll();

  // ──── MOBILE NAVIGATION ────
  const burg = document.getElementById('burg');
  const mobMenu = document.getElementById('mobMenu');
  if(burg && mobMenu) {
    burg.onclick = () => {
      burg.classList.toggle('on');
      mobMenu.classList.toggle('show');
      document.body.style.overflow = mobMenu.classList.contains('show') ? 'hidden' : '';
    };
  }
  window.closeMob = () => {
    if(burg && mobMenu) {
      burg.classList.remove('on');
      mobMenu.classList.remove('show');
      document.body.style.overflow = '';
    }
  };

  // ──── SCROLL REVEAL OBSERVER ────
  const obs = new IntersectionObserver(es => es.forEach(e => {
    if(e.isIntersecting) {
      e.target.classList.add('on');
    }
  }), {threshold: 0.08, rootMargin: '0px 0px -40px 0px'});
  document.querySelectorAll('.rv, .rv-l, .rv-r, .rv-s').forEach(e => obs.observe(e));

  // ──── COUNTERS ────
  let cDone = false;
  const counters = document.querySelectorAll('[data-c]');
  const cObs = new IntersectionObserver(es => es.forEach(e => {
    if(e.isIntersecting && !cDone) {
      cDone = true;
      counters.forEach(c => {
        const end = +c.dataset.c;
        const suf = c.dataset.s || '';
        const pre = end > 100 ? '+' : '';
        const dur = 2000;
        const t0 = performance.now();
        const go = now => {
          const p = Math.min((now - t0) / dur, 1);
          const ez = 1 - Math.pow(1 - p, 3); // easeOutCubic
          c.textContent = pre + Math.floor(ez * end) + suf;
          if(p < 1) requestAnimationFrame(go);
        };
        requestAnimationFrame(go);
      });
    }
  }), {threshold: 0.5});
  counters.forEach(c => cObs.observe(c));

  // ──── PROGRESS BARS FILLS ────
  const pObs = new IntersectionObserver(es => es.forEach(e => {
    if(e.isIntersecting) {
      e.target.style.width = e.target.dataset.w + '%';
    }
  }), {threshold: 0.2});
  document.querySelectorAll('.prog-fill[data-w]').forEach(b => pObs.observe(b));

  // ──── 3D CARD PARALLAX EFFECT ────
  const card = document.getElementById('parallaxCard');
  const glare = document.getElementById('cardGlare');
  if(card) {
    card.addEventListener('mousemove', (e) => {
      const rect = card.getBoundingClientRect();
      const x = e.clientX - rect.left;
      const y = e.clientY - rect.top;
      
      const px = (x / rect.width) * 100;
      const py = (y / rect.height) * 100;
      
      // Calculate rotation angles (-10 to 10 degrees)
      const ry = ((x / rect.width) - 0.5) * 18;
      const rx = (0.5 - (y / rect.height)) * 18;
      
      card.style.transform = `rotateY(${ry}deg) rotateX(${rx}deg) translateZ(15px)`;
      
      if(glare) {
        glare.style.opacity = '1';
        glare.style.background = `radial-gradient(circle at ${px}% ${py}%, rgba(255, 255, 255, 0.16) 0%, transparent 65%)`;
      }
    });
    
    card.addEventListener('mouseleave', () => {
      card.style.transform = `rotateY(-8deg) rotateX(4deg)`;
      if(glare) glare.style.opacity = '0';
    });
  }

  // ──── DUAL CALCULATOR LOGIC ────
  // Tabs Switcher
  const tabs = document.querySelectorAll('.calc-tab');
  const panes = document.querySelectorAll('.calc-pane');
  tabs.forEach(tab => {
    tab.onclick = () => {
      tabs.forEach(t => t.classList.remove('active'));
      panes.forEach(p => p.classList.remove('active'));
      tab.classList.add('active');
      document.getElementById(tab.dataset.target).classList.add('active');
    };
  });

  // Range Slider Visual Fill Utility
  function updRng(el, val) {
    const p = ((val - el.min) / (el.max - el.min)) * 100;
    el.style.background = `linear-gradient(90deg, var(--primary) ${p}%, var(--border) ${p}%)`;
  }

  // 1. Luz/Gas Calc
  const bS = document.getElementById('bSlider'), bD = document.getElementById('bDisp');
  const tS = document.getElementById('tSel'), sD = document.getElementById('sDisp');
  const cgOldVal = document.getElementById('cgOldVal'), cgNewVal = document.getElementById('cgNewVal');
  const cgNewBar = document.getElementById('cgNewBar');
  
  let af = null;
  function calcLuz() {
    const b = +bS.value;
    const mult = +tS.value;
    bD.textContent = b;
    updRng(bS, b);
    
    cgOldVal.textContent = b;
    const optVal = Math.round(b * 0.7);
    cgNewVal.textContent = optVal;
    
    // Animate graphics bar height
    const barPct = (optVal / b) * 85;
    if(cgNewBar) cgNewBar.style.height = barPct + '%';
    
    const targetSavings = Math.round(b * 12 * 0.3 * mult);
    const currentDisp = parseInt(sD.textContent) || 0;
    
    if(af) cancelAnimationFrame(af);
    const t0 = performance.now(), dur = 400;
    const go = now => {
      const p = Math.min((now - t0) / dur, 1);
      const ez = 1 - Math.pow(1 - p, 3);
      sD.textContent = Math.floor(currentDisp + (targetSavings - currentDisp) * ez) + '€';
      if(p < 1) af = requestAnimationFrame(go);
    };
    af = requestAnimationFrame(go);
  }
  if(bS) {
    bS.oninput = calcLuz;
    tS.onchange = calcLuz;
    calcLuz();
  }

  // 2. Solar Calc
  const solS = document.getElementById('solSlider'), solD = document.getElementById('solDisp');
  const solSel = document.getElementById('solSel'), solSave = document.getElementById('solSave'), solAmort = document.getElementById('solAmort');
  const cgOldSol = document.getElementById('cgOldSol'), cgNewSol = document.getElementById('cgNewSol');
  const cgNewSolBar = document.getElementById('cgNewSolBar');
  
  let saf = null;
  function calcSolar() {
    const b = +solS.value;
    const eff = +solSel.value;
    solD.textContent = b;
    updRng(solS, b);
    
    cgOldSol.textContent = b;
    const solarVal = Math.round(b * 0.3); // 70% savings
    cgNewSol.textContent = solarVal;
    
    if(cgNewSolBar) cgNewSolBar.style.height = ((solarVal / b) * 85) + '%';
    
    const annualBill = b * 12;
    const annualSave = annualBill * 0.7 * eff;
    const tenYearSave = Math.round(annualSave * 10);
    const installCost = Math.max(3600, b * 32);
    const amort = (installCost / annualSave).toFixed(1);
    
    solAmort.textContent = `Amortización estimada en ${amort} años`;
    const curVal = parseInt(solSave.textContent.replace(/\./g, '')) || 0;
    
    if(saf) cancelAnimationFrame(saf);
    const t0 = performance.now(), dur = 400;
    const go = now => {
      const p = Math.min((now - t0) / dur, 1);
      const ez = 1 - Math.pow(1 - p, 3);
      const val = Math.floor(curVal + (tenYearSave - curVal) * ez);
      solSave.textContent = val.toLocaleString('es-ES') + '€';
      if(p < 1) saf = requestAnimationFrame(go);
    };
    saf = requestAnimationFrame(go);
  }
  if(solS) {
    solS.oninput = calcSolar;
    solSel.onchange = calcSolar;
    calcSolar();
  }

  // ──── TESTIMONIALS AUTOPLAY CAROUSEL ────
  const slider = document.getElementById('tSlider');
  const sliderWrap = document.getElementById('tSliderWrap');
  const prevBtn = document.getElementById('sliderPrev');
  const nextBtn = document.getElementById('sliderNext');
  const dotsContainer = document.getElementById('sliderDots');
  
  if(slider && sliderWrap) {
    const cards = document.querySelectorAll('.tc');
    const count = cards.length;
    let index = 0;
    let autoInterval = null;
    
    // Create navigation dots
    // On large screens, we slide 2 by 2, so count/2 is the steps
    // To make it simple, we dots for each step
    const getVisibleCards = () => window.innerWidth > 1024 ? 2 : 1;
    
    const createDots = () => {
      if(!dotsContainer) return;
      dotsContainer.innerHTML = '';
      const visible = getVisibleCards();
      const dotsCount = Math.ceil(count / visible);
      for(let i = 0; i < dotsCount; i++) {
        const dot = document.createElement('div');
        dot.className = `slider-dot ${i === 0 ? 'active' : ''}`;
        dot.onclick = () => goToIndex(i * visible);
        dotsContainer.appendChild(dot);
      }
    };
    
    const updateDots = () => {
      if(!dotsContainer) return;
      const visible = getVisibleCards();
      const activeDotIdx = Math.floor(index / visible);
      const dots = document.querySelectorAll('.slider-dot');
      dots.forEach((dot, idx) => {
        dot.classList.toggle('active', idx === activeDotIdx);
      });
    };
    
    const goToIndex = (targetIdx) => {
      const visible = getVisibleCards();
      const maxIdx = count - visible;
      index = Math.max(0, Math.min(targetIdx, maxIdx));
      
      const cardWidth = cards[0].offsetWidth;
      const gap = 28;
      slider.style.transform = `translateX(-${index * (cardWidth + gap)}px)`;
      updateDots();
    };
    
    const slideNext = () => {
      const visible = getVisibleCards();
      if(index + visible >= count) {
        goToIndex(0); // Loop back
      } else {
        goToIndex(index + 1);
      }
    };
    
    const slidePrev = () => {
      const visible = getVisibleCards();
      if(index === 0) {
        goToIndex(count - visible); // Loop to end
      } else {
        goToIndex(index - 1);
      }
    };
    
    if(nextBtn) nextBtn.onclick = () => { slideNext(); resetAuto(); };
    if(prevBtn) prevBtn.onclick = () => { slidePrev(); resetAuto(); };
    
    // Drag/Swipe Gesture
    let isDragging = false, startX, scrollLeft, cardWidth, gap = 28;
    
    sliderWrap.addEventListener('mousedown', (e) => {
      isDragging = true;
      startX = e.pageX;
      slider.style.transition = 'none';
      stopAuto();
    });
    
    window.addEventListener('mouseup', (e) => {
      if(!isDragging) return;
      isDragging = false;
      slider.style.transition = 'transform 0.5s var(--ease)';
      const deltaX = e.pageX - startX;
      
      if(Math.abs(deltaX) > 100) {
        if(deltaX < 0) slideNext();
        else slidePrev();
      } else {
        goToIndex(index); // Revert
      }
      startAuto();
    });
    
    sliderWrap.addEventListener('mousemove', (e) => {
      if(!isDragging) return;
      const deltaX = e.pageX - startX;
      const visible = getVisibleCards();
      const currentTranslate = -index * (cards[0].offsetWidth + gap);
      slider.style.transform = `translateX(${currentTranslate + deltaX}px)`;
    });
    
    // Auto Play Interval
    const startAuto = () => {
      autoInterval = setInterval(slideNext, 5000);
    };
    const stopAuto = () => {
      if(autoInterval) clearInterval(autoInterval);
    };
    const resetAuto = () => {
      stopAuto();
      startAuto();
    };
    
    sliderWrap.addEventListener('mouseenter', stopAuto);
    sliderWrap.addEventListener('mouseleave', startAuto);
    
    // Init carousels
    createDots();
    startAuto();
    
    window.addEventListener('resize', () => {
      createDots();
      goToIndex(index);
    });
  }

  // ──── FAQ ACCORDION LOGIC ────
  document.querySelectorAll('.faq-q').forEach(btn => {
    btn.onclick = () => {
      const it = btn.parentElement;
      const isOpen = it.classList.contains('open');
      
      // Close all accordions
      document.querySelectorAll('.faq-it').forEach(item => item.classList.remove('open'));
      
      // Toggle current accordion
      if(!isOpen) {
        it.classList.add('open');
      }
    };
  });

  // ──── INTERACTIVE BACKGROUND CANVAS PARTICLES ────
  const cv = document.getElementById('pCanvas');
  if(cv) {
    const ctx = cv.getContext('2d');
    let pts = [], w, h;
    let mouse = { x: null, y: null, radius: 140 };
    
    function rsz() {
      const hr = document.querySelector('.hero');
      if(hr) {
        w = cv.width = hr.offsetWidth;
        h = cv.height = hr.offsetHeight;
      }
    }
    rsz();
    window.addEventListener('resize', rsz);
    
    // Tracks mouse movement on Hero section
    const heroSec = document.querySelector('.hero');
    if(heroSec) {
      heroSec.addEventListener('mousemove', (e) => {
        const bounds = heroSec.getBoundingClientRect();
        mouse.x = e.clientX - bounds.left;
        mouse.y = e.clientY - bounds.top;
      });
      heroSec.addEventListener('mouseleave', () => {
        mouse.x = null;
        mouse.y = null;
      });
    }

    // Populate particles
    const particleCount = 48;
    for(let i = 0; i < particleCount; i++) {
      pts.push({
        x: Math.random() * w,
        y: Math.random() * h,
        baseX: null,
        baseY: null,
        vx: (Math.random() - 0.5) * 0.35,
        vy: (Math.random() - 0.5) * 0.35,
        r: Math.random() * 2 + 0.4,
        a: Math.random() * 0.25 + 0.08
      });
    }

    function draw() {
      ctx.clearRect(0, 0, w, h);
      
      pts.forEach(p => {
        // Move particle randomly
        p.x += p.vx;
        p.y += p.vy;
        
        // Wrap screen borders
        if(p.x < 0) p.x = w;
        if(p.x > w) p.x = 0;
        if(p.y < 0) p.y = h;
        if(p.y > h) p.y = 0;
        
        // Mouse Repulse Effect
        if(mouse.x !== null && mouse.y !== null) {
          const dx = p.x - mouse.x;
          const dy = p.y - mouse.y;
          const dist = Math.sqrt(dx * dx + dy * dy);
          
          if(dist < mouse.radius) {
            const force = (mouse.radius - dist) / mouse.radius;
            // Push particles slightly away
            p.x += (dx / dist) * force * 1.5;
            p.y += (dy / dist) * force * 1.5;
          }
        }
        
        ctx.beginPath();
        ctx.arc(p.x, p.y, p.r, 0, Math.PI * 2);
        ctx.fillStyle = `rgba(16, 185, 129, ${p.a})`;
        ctx.fill();
      });
      
      // Draw lines between nearby particles
      for(let i = 0; i < pts.length; i++) {
        for(let j = i + 1; j < pts.length; j++) {
          const dx = pts[i].x - pts[j].x;
          const dy = pts[i].y - pts[j].y;
          const d = Math.sqrt(dx * dx + dy * dy);
          
          if(d < 140) {
            ctx.beginPath();
            ctx.moveTo(pts[i].x, pts[i].y);
            ctx.lineTo(pts[j].x, pts[j].y);
            // Dynamic line opacity based on distance
            ctx.strokeStyle = `rgba(16, 185, 129, ${0.06 * (1 - d / 140)})`;
            ctx.lineWidth = 1;
            ctx.stroke();
          }
        }
      }
      requestAnimationFrame(draw);
    }
    draw();
  }

  // ──── SMOOTH ANCHOR LINK CLICK SCROLL ────
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.onclick = e => {
      const targetId = anchor.getAttribute('href');
      if(targetId === '#') return;
      const targetElement = document.querySelector(targetId);
      if(targetElement) {
        e.preventDefault();
        const headerOffset = (hdr ? hdr.offsetHeight : 80) + 12;
        const elementPosition = targetElement.getBoundingClientRect().top + window.scrollY;
        const offsetPosition = elementPosition - headerOffset;
        
        window.scrollTo({
          top: offsetPosition,
          behavior: 'smooth'
        });
      }
    };
  });
})();
</script>
</body>
</html>
