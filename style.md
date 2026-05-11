/* --- CSS Custom Properties --- */
:root {
  --sand-50: #FDF8F0;
  --sand-100: #F5E6D3;
  --sand-200: #E8D5B7;
  --sand-300: #D4C4A8;
  --sand-400: #C0A882;
  --ocean-100: #A8D8E8;
  --ocean-200: #4EACC5;
  --ocean-300: #1B6B93;
  --ocean-400: #145270;
  --ocean-500: #0D3A52;
  --coral-100: #FADCD2;
  --coral-200: #F09080;
  --coral-300: #E8735A;
  --coral-400: #D4533B;
  --white: #FFFFFF;
  --off-white: #F8F9FA;
  --gray-100: #F1F3F5;
  --gray-200: #E9ECEF;
  --gray-300: #DEE2E6;
  --gray-500: #ADB5BD;
  --gray-700: #495057;
  --gray-900: #212529;
  --text-primary: #2C3E50;
  --text-secondary: #5A6C7D;
  --text-light: #8A9BAC;
  --shadow-sm: 0 2px 8px rgba(0,0,0,0.08);
  --shadow-md: 0 4px 16px rgba(0,0,0,0.1);
  --shadow-lg: 0 8px 32px rgba(0,0,0,0.12);
  --radius-sm: 8px;
  --radius-md: 12px;
  --radius-lg: 20px;
  --radius-full: 50%;
  --transition: 0.3s ease;
  --max-width: 1200px;
  --nav-height: 72px;
}

/* --- Reset & Base --- */
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
  scroll-padding-top: var(--nav-height);
}

body {
  font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
  color: var(--text-primary);
  background-color: var(--off-white);
  line-height: 1.7;
  font-size: 16px;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

img {
  max-width: 100%;
  height: auto;
  display: block;
}

a {
  color: var(--ocean-300);
  text-decoration: none;
  transition: color var(--transition);
}

a:hover {
  color: var(--coral-300);
}

ul {
  list-style: none;
}

/* --- Sticky Navigation --- */
.navbar {
  position: sticky;
  top: 0;
  z-index: 1000;
  background: rgba(255,255,255,0.95);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--gray-200);
  height: var(--nav-height);
  display: flex;
  align-items: center;
  padding: 0 2rem;
}

.nav-container {
  max-width: var(--max-width);
  width: 100%;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-logo {
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--ocean-300);
  letter-spacing: -0.5px;
}

.nav-logo span {
  color: var(--coral-300);
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 0.25rem;
}

.nav-links > li {
  position: relative;
}

.nav-links > li > a {
  display: block;
  padding: 0.5rem 1rem;
  font-weight: 500;
  font-size: 0.95rem;
  color: var(--text-primary);
  border-radius: var(--radius-sm);
  transition: background var(--transition), color var(--transition);
}

.nav-links > li > a:hover,
.nav-links > li > a.active {
  background: var(--sand-100);
  color: var(--ocean-300);
}

/* Dropdown */
.dropdown-menu {
  display: none;
  position: absolute;
  top: 100%;
  left: 0;
  min-width: 220px;
  background: var(--white);
  border-radius: var(--radius-md);
  box-shadow: var(--shadow-lg);
  border: 1px solid var(--gray-200);
  padding: 0.5rem 0;
  z-index: 100;
}

.nav-links > li:hover > .dropdown-menu {
  display: block;
  animation: fadeDown 0.2s ease;
}

@keyframes fadeDown {
  from { opacity: 0; transform: translateY(-8px); }
  to { opacity: 1; transform: translateY(0); }
}

.dropdown-menu li a {
  display: block;
  padding: 0.6rem 1.25rem;
  font-size: 0.9rem;
  color: var(--text-secondary);
  transition: background var(--transition), color var(--transition);
}

.dropdown-menu li a:hover {
  background: var(--sand-50);
  color: var(--ocean-300);
}

/* Hamburger (CSS-only mobile toggle) */
.nav-toggle {
  display: none;
}

.nav-toggle-label {
  display: none;
  cursor: pointer;
  flex-direction: column;
  gap: 5px;
  padding: 8px;
}

.nav-toggle-label span {
  display: block;
  width: 26px;
  height: 3px;
  background: var(--text-primary);
  border-radius: 2px;
  transition: var(--transition);
}

/* --- Hero Section --- */
.hero {
  position: relative;
  height: 100vh;
  min-height: 500px;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  overflow: hidden;
}

.hero-img {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.hero-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(
    180deg,
    rgba(13,58,82,0.35) 0%,
    rgba(13,58,82,0.55) 50%,
    rgba(13,58,82,0.7) 100%
  );
}

.hero-content {
  position: relative;
  z-index: 2;
  max-width: 700px;
  padding: 2rem;
}

.hero-content h1 {
  font-size: 3.5rem;
  font-weight: 700;
  color: var(--white);
  line-height: 1.15;
  margin-bottom: 1rem;
  text-shadow: 0 2px 20px rgba(0,0,0,0.2);
}

.hero-content p {
  font-size: 1.2rem;
  color: rgba(255,255,255,0.9);
  margin-bottom: 2rem;
  line-height: 1.6;
}

/* --- Buttons --- */
.btn {
  display: inline-block;
  padding: 0.85rem 2rem;
  border-radius: var(--radius-md);
  font-weight: 600;
  font-size: 1rem;
  text-align: center;
  cursor: pointer;
  border: none;
  transition: transform var(--transition), box-shadow var(--transition), background var(--transition);
}

.btn:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-md);
}

.btn-primary {
  background: var(--coral-300);
  color: var(--white);
}

.btn-primary:hover {
  background: var(--coral-400);
  color: var(--white);
}

.btn-secondary {
  background: var(--ocean-300);
  color: var(--white);
}

.btn-secondary:hover {
  background: var(--ocean-400);
  color: var(--white);
}

.btn-outline {
  background: transparent;
  color: var(--white);
  border: 2px solid var(--white);
}

.btn-outline:hover {
  background: var(--white);
  color: var(--ocean-300);
}

/* --- Section Layout --- */
.section {
  padding: 5rem 2rem;
}

.section-container {
  max-width: var(--max-width);
  margin: 0 auto;
}

.section-header {
  text-align: center;
  margin-bottom: 3.5rem;
}

.section-header h2 {
  font-size: 2.25rem;
  font-weight: 700;
  color: var(--ocean-500);
  margin-bottom: 0.75rem;
}

.section-header p {
  font-size: 1.1rem;
  color: var(--text-secondary);
  max-width: 600px;
  margin: 0 auto;
}

.section-alt {
  background: var(--sand-50);
}

/* --- Teaser Cards (Homepage) --- */
.teaser-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.teaser-card {
  background: var(--white);
  border-radius: var(--radius-lg);
  overflow: hidden;
  box-shadow: var(--shadow-sm);
  transition: transform var(--transition), box-shadow var(--transition);
}

.teaser-card:hover {
  transform: translateY(-6px);
  box-shadow: var(--shadow-lg);
}

.teaser-card img {
  width: 100%;
  height: 220px;
  object-fit: cover;
}

.teaser-card-body {
  padding: 1.75rem;
}

.teaser-card-body h3 {
  font-size: 1.3rem;
  font-weight: 600;
  color: var(--ocean-400);
  margin-bottom: 0.5rem;
}

.teaser-card-body p {
  color: var(--text-secondary);
  font-size: 0.95rem;
  margin-bottom: 1.25rem;
}

.teaser-card-body .btn {
  font-size: 0.9rem;
  padding: 0.65rem 1.5rem;
}

/* --- Intro Section (Homepage) --- */
.intro {
  background: var(--white);
}

.intro-text {
  max-width: 750px;
  margin: 0 auto;
  text-align: center;
  font-size: 1.15rem;
  color: var(--text-secondary);
  line-height: 1.8;
}

/* --- Place Cards (Orte) --- */
.place-list {
  display: flex;
  flex-direction: column;
  gap: 3rem;
}

.place-card {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2.5rem;
  align-items: center;
  background: var(--white);
  border-radius: var(--radius-lg);
  overflow: hidden;
  box-shadow: var(--shadow-sm);
}

.place-card:nth-child(even) .place-card-img {
  order: 2;
}

.place-card:nth-child(even) .place-card-body {
  order: 1;
}

.place-card-img {
  width: 100%;
  height: 100%;
  min-height: 320px;
  object-fit: cover;
}

.place-card-body {
  padding: 2.5rem;
}

.place-card-body h3 {
  font-size: 1.6rem;
  font-weight: 700;
  color: var(--ocean-400);
  margin-bottom: 0.75rem;
}

.place-card-body p {
  color: var(--text-secondary);
  line-height: 1.8;
  margin-bottom: 1rem;
}

.place-highlight {
  display: inline-block;
  background: var(--coral-100);
  color: var(--coral-400);
  padding: 0.4rem 1rem;
  border-radius: var(--radius-sm);
  font-size: 0.85rem;
  font-weight: 600;
}

/* --- Info Sections (Infrastruktur, Wirtschaft, Geschichte) --- */
.info-block {
  background: var(--white);
  border-radius: var(--radius-lg);
  padding: 2.5rem;
  margin-bottom: 2rem;
  box-shadow: var(--shadow-sm);
}

.info-block h3 {
  font-size: 1.4rem;
  font-weight: 700;
  color: var(--ocean-400);
  margin-bottom: 1rem;
  padding-bottom: 0.75rem;
  border-bottom: 2px solid var(--sand-200);
}

.info-block p {
  color: var(--text-secondary);
  line-height: 1.8;
  margin-bottom: 1rem;
}

.info-block ul {
  list-style: disc;
  padding-left: 1.5rem;
  margin-bottom: 1rem;
}

.info-block ul li {
  color: var(--text-secondary);
  line-height: 1.8;
  margin-bottom: 0.35rem;
}

.info-block strong {
  color: var(--text-primary);
}

/* --- Timeline (Geschichte) --- */
.timeline {
  position: relative;
  padding-left: 2.5rem;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 0.75rem;
  top: 0;
  bottom: 0;
  width: 3px;
  background: linear-gradient(180deg, var(--ocean-200), var(--coral-200));
  border-radius: 2px;
}

.timeline-item {
  position: relative;
  margin-bottom: 2.5rem;
  background: var(--white);
  border-radius: var(--radius-md);
  padding: 2rem;
  box-shadow: var(--shadow-sm);
}

.timeline-item::before {
  content: '';
  position: absolute;
  left: -2.05rem;
  top: 1.75rem;
  width: 14px;
  height: 14px;
  background: var(--ocean-300);
  border: 3px solid var(--white);
  border-radius: var(--radius-full);
  box-shadow: 0 0 0 3px var(--ocean-200);
}

.timeline-item h3 {
  font-size: 1.2rem;
  font-weight: 700;
  color: var(--ocean-400);
  margin-bottom: 0.5rem;
}

.timeline-item .timeline-year {
  display: inline-block;
  background: var(--coral-300);
  color: var(--white);
  padding: 0.2rem 0.75rem;
  border-radius: var(--radius-sm);
  font-size: 0.8rem;
  font-weight: 600;
  margin-bottom: 0.75rem;
}

.timeline-item p {
  color: var(--text-secondary);
  line-height: 1.8;
}

/* --- Page Header (non-home pages) --- */
.page-header {
  background: linear-gradient(135deg, var(--ocean-500), var(--ocean-300));
  padding: 4rem 2rem;
  text-align: center;
}

.page-header h1 {
  font-size: 2.75rem;
  font-weight: 700;
  color: var(--white);
  margin-bottom: 0.5rem;
}

.page-header p {
  font-size: 1.15rem;
  color: rgba(255,255,255,0.85);
  max-width: 600px;
  margin: 0 auto;
}

/* --- Form (Buchen) --- */
.form-container {
  max-width: 720px;
  margin: 0 auto;
  background: var(--white);
  border-radius: var(--radius-lg);
  padding: 3rem;
  box-shadow: var(--shadow-md);
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-group label {
  display: block;
  font-weight: 600;
  font-size: 0.9rem;
  color: var(--text-primary);
  margin-bottom: 0.4rem;
}

.form-group label .optional {
  font-weight: 400;
  color: var(--text-light);
  font-size: 0.8rem;
}

.form-group input,
.form-group select,
.form-group textarea {
  width: 100%;
  padding: 0.75rem 1rem;
  border: 2px solid var(--gray-300);
  border-radius: var(--radius-sm);
  font-family: inherit;
  font-size: 0.95rem;
  color: var(--text-primary);
  background: var(--off-white);
  transition: border-color var(--transition), box-shadow var(--transition);
}

.form-group input:focus,
.form-group select:focus,
.form-group textarea:focus {
  outline: none;
  border-color: var(--ocean-200);
  box-shadow: 0 0 0 3px rgba(78,172,197,0.15);
}

.form-group textarea {
  resize: vertical;
  min-height: 120px;
}

.form-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.5rem;
}

.checkbox-group {
  display: flex;
  align-items: flex-start;
  gap: 0.75rem;
}

.checkbox-group input[type="checkbox"] {
  width: auto;
  margin-top: 0.25rem;
  accent-color: var(--ocean-300);
}

.checkbox-group label {
  font-weight: 400;
  font-size: 0.9rem;
  color: var(--text-secondary);
  line-height: 1.5;
}

.form-notice {
  margin-top: 1.5rem;
  padding: 1rem 1.25rem;
  background: var(--sand-50);
  border-left: 4px solid var(--ocean-200);
  border-radius: 0 var(--radius-sm) var(--radius-sm) 0;
  font-size: 0.85rem;
  color: var(--text-secondary);
}

/* --- Impressum --- */
.impressum-content {
  max-width: 800px;
  margin: 0 auto;
}

.impressum-content h3 {
  font-size: 1.3rem;
  font-weight: 700;
  color: var(--ocean-400);
  margin-top: 2rem;
  margin-bottom: 0.75rem;
}

.impressum-content p {
  color: var(--text-secondary);
  line-height: 1.8;
  margin-bottom: 0.75rem;
}

.impressum-content ul {
  list-style: disc;
  padding-left: 1.5rem;
  margin-bottom: 1rem;
}

.impressum-content ul li {
  color: var(--text-secondary);
  line-height: 1.8;
  margin-bottom: 0.25rem;
}

/* --- Footer --- */
.footer {
  background: var(--ocean-500);
  color: rgba(255,255,255,0.8);
  padding: 3rem 2rem 1.5rem;
  margin-top: auto;
}

.footer-grid {
  max-width: var(--max-width);
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 2rem;
  padding-bottom: 2rem;
  border-bottom: 1px solid rgba(255,255,255,0.15);
}

.footer-col h4 {
  font-size: 1rem;
  font-weight: 600;
  color: var(--white);
  margin-bottom: 1rem;
}

.footer-col ul li {
  margin-bottom: 0.5rem;
}

.footer-col ul li a {
  color: rgba(255,255,255,0.7);
  font-size: 0.9rem;
  transition: color var(--transition);
}

.footer-col ul li a:hover {
  color: var(--white);
}

.footer-brand {
  text-align: center;
}

.footer-brand .footer-logo {
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--white);
  margin-bottom: 0.5rem;
}

.footer-brand .footer-logo span {
  color: var(--coral-200);
}

.footer-brand p {
  font-size: 0.85rem;
  color: rgba(255,255,255,0.5);
}

.social-icons {
  display: flex;
  gap: 0.75rem;
  justify-content: center;
  margin-top: 1rem;
}

.social-icons a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: var(--radius-full);
  background: rgba(255,255,255,0.1);
  color: rgba(255,255,255,0.7);
  font-size: 1.1rem;
  transition: background var(--transition), color var(--transition);
}

.social-icons a:hover {
  background: rgba(255,255,255,0.2);
  color: var(--white);
}

.footer-bottom {
  max-width: var(--max-width);
  margin: 0 auto;
  text-align: center;
  padding-top: 1.5rem;
  font-size: 0.8rem;
  color: rgba(255,255,255,0.4);
}

/* --- Back to Top Button --- */
.back-to-top {
  position: fixed;
  bottom: 2rem;
  right: 2rem;
  width: 48px;
  height: 48px;
  background: var(--coral-300);
  color: var(--white);
  border-radius: var(--radius-full);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.3rem;
  font-weight: 700;
  box-shadow: var(--shadow-md);
  transition: background var(--transition), transform var(--transition);
  z-index: 900;
}

.back-to-top:hover {
  background: var(--coral-400);
  transform: translateY(-3px);
  color: var(--white);
}

/* --- Stat Cards (Wirtschaft) --- */
.stat-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1.5rem;
  margin-bottom: 2rem;
}

.stat-card {
  background: var(--white);
  border-radius: var(--radius-md);
  padding: 1.75rem;
  text-align: center;
  box-shadow: var(--shadow-sm);
  border-top: 4px solid var(--ocean-200);
}

.stat-card .stat-number {
  font-size: 2rem;
  font-weight: 700;
  color: var(--ocean-300);
  line-height: 1.2;
}

.stat-card .stat-label {
  font-size: 0.85rem;
  color: var(--text-secondary);
  margin-top: 0.25rem;
}

/* --- Transport Grid (Infrastruktur) --- */
.transport-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
  margin-bottom: 2rem;
}

.transport-card {
  background: var(--white);
  border-radius: var(--radius-md);
  padding: 1.75rem;
  box-shadow: var(--shadow-sm);
  border-left: 4px solid var(--ocean-200);
}

.transport-card h4 {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--ocean-400);
  margin-bottom: 0.5rem;
}

.transport-card p {
  font-size: 0.9rem;
  color: var(--text-secondary);
  line-height: 1.7;
}

/* --- Responsive --- */
@media (max-width: 900px) {
  .place-card {
    grid-template-columns: 1fr;
  }

  .place-card:nth-child(even) .place-card-img {
    order: 0;
  }

  .place-card:nth-child(even) .place-card-body {
    order: 0;
  }

  .place-card-img {
    min-height: 240px;
  }

  .footer-grid {
    grid-template-columns: 1fr;
    text-align: center;
  }

  .social-icons {
    justify-content: center;
  }

  .form-row {
    grid-template-columns: 1fr;
  }

  .hero-content h1 {
    font-size: 2.5rem;
  }

  .page-header h1 {
    font-size: 2rem;
  }
}

@media (max-width: 768px) {
  .nav-toggle-label {
    display: flex;
  }

  .nav-links {
    position: absolute;
    top: var(--nav-height);
    left: 0;
    right: 0;
    background: var(--white);
    flex-direction: column;
    padding: 1rem;
    box-shadow: var(--shadow-lg);
    border-top: 1px solid var(--gray-200);
    display: none;
  }

  .nav-toggle:checked ~ .nav-links {
    display: flex;
  }

  .nav-links > li > a {
    padding: 0.75rem 1rem;
  }

  .dropdown-menu {
    position: static;
    box-shadow: none;
    border: none;
    padding-left: 1rem;
    display: none;
  }

  .nav-links > li:hover > .dropdown-menu {
    display: block;
  }

  .section {
    padding: 3rem 1.25rem;
  }

  .hero-content h1 {
    font-size: 2rem;
  }

  .hero-content p {
    font-size: 1rem;
  }

  .form-container {
    padding: 2rem 1.5rem;
  }
}

@media (max-width: 480px) {
  .navbar {
    padding: 0 1rem;
  }

  .hero-content h1 {
    font-size: 1.75rem;
  }

  .section-header h2 {
    font-size: 1.75rem;
  }

  .stat-grid {
    grid-template-columns: 1fr 1fr;
  }
}
