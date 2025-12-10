---
title: "Muhammad Elsadany | Portfolio"
layout: default
---

<style>
  /* Import and define BrauerNeue font */
  @font-face {
    font-family: 'BrauerNeue';
    src: url('assets/fonts/BrauerNeue-Regular.ttf') format('truetype');
    font-weight: normal;
    font-style: normal;
    font-display: swap;
  }
  
  @font-face {
    font-family: 'BrauerNeue';
    src: url('assets/fonts/BrauerNeue-Bold.ttf') format('truetype');
    font-weight: bold;
    font-style: normal;
    font-display: swap;
  }
  
  @font-face {
    font-family: 'BrauerNeue';
    src: url('assets/fonts/BrauerNeue-Italic.ttf') format('truetype');
    font-weight: normal;
    font-style: italic;
    font-display: swap;
  }
  
  /* CSS Variables for Dark/Light Themes */
  :root {
    /* Light Theme (Default) */
    --bg-primary: #ffffff;
    --bg-secondary: #f8f9fa;
    --bg-gradient: linear-gradient(135deg, #4782b4 0%, #3C4856 100%);
    --text-primary: #2c3e50;
    --text-secondary: #627899;
    --card-bg: #ffffff;
    --border-color: #e9ecef;
    --shadow-color: rgba(0,0,0,0.08);
    /* My Color Palette */
    --primary: #4782b4;
    --primary-dark: #3C4856;
    --accent: #ff4600;
    --secondary: #39C08F;
    --tertiary: #00C0C5;
    --warm: #C1624A;
    --light: #88ADE1;
    --neutral: #627899;
    --purple: #AE6885;
    --deep-purple: #783753;
  }
  
  [data-theme="dark"] {
    /* Dark Theme */
    --bg-primary: #1a1a2e;
    --bg-secondary: #16213e;
    --bg-gradient: linear-gradient(135deg, #0f3460 0%, #1a1a2e 100%);
    --text-primary: #e2e2e2;
    --text-secondary: #a0aec0;
    --card-bg: #2d3748;
    --border-color: #4a5568;
    --shadow-color: rgba(0,0,0,0.3);
  }
  
  /* Reset and base styles */
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  
  body {
    font-family: 'BrauerNeue', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: var(--text-primary);
    background: var(--bg-gradient);
    background-attachment: fixed;
    min-height: 100vh;
    transition: all 0.3s ease;
  }
  
  /* Hide the download buttons */
  .btn, .header-btn {
    display: none !important;
  }
  
  /* Page Header - Hidden */
  .page-header {
    display: none !important;
  }
  
  /* Main Layout - Fixed sidebar with main content offset */
  .layout-container {
    display: block;
    min-height: 100vh;
    width: 100%;
    background: var(--bg-primary);
  }
  
  /* Sidebar - FIXED POSITION (properly implemented) */
  .sidebar {
    background: var(--bg-secondary);
    padding: 40px 25px;
    border-right: 1px solid var(--border-color);
    position: fixed;
    top: 0;
    left: 0;
    height: 100vh;
    width: 280px;
    overflow-y: auto;
    display: flex;
    flex-direction: column;
    z-index: 1000;
    box-shadow: 5px 0 15px rgba(0,0,0,0.1);
    transition: transform 0.3s ease;
  }
  
  .profile-container {
    text-align: center;
    margin-bottom: 40px;
  }
  
  .profile-img {
    width: 180px;
    height: 180px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 20px;
    border: 4px solid var(--accent);
    box-shadow: 0 10px 30px var(--shadow-color);
  }
  
  .profile-name {
    font-size: 1.8em;
    color: var(--text-primary);
    margin-bottom: 5px;
  }
  
  .profile-title {
    color: var(--accent);
    font-size: 1.1em;
    margin-bottom: 20px;
  }
  
  .contact-links {
    display: flex;
    flex-direction: column;
    gap: 10px;
    margin-bottom: 40px;
  }
  
  .contact-link {
    display: flex;
    align-items: center;
    gap: 10px;
    color: var(--text-secondary);
    text-decoration: none;
    padding: 8px 12px;
    border-radius: 8px;
    transition: all 0.3s ease;
  }
  
  .contact-link:hover {
    background: var(--card-bg);
    color: var(--accent);
    transform: translateX(5px);
  }
  
  /* Navigation Menu */
  .nav-menu {
    flex-grow: 1;
  }
  
  .nav-title {
    font-size: 0.9em;
    text-transform: uppercase;
    color: var(--text-secondary);
    margin-bottom: 15px;
    letter-spacing: 1px;
  }
  
  .nav-list {
    list-style: none;
  }
  
  .nav-item {
    margin-bottom: 8px;
  }
  
  .nav-link {
    display: flex;
    align-items: center;
    gap: 10px;
    color: var(--text-primary);
    text-decoration: none;
    padding: 10px 15px;
    border-radius: 8px;
    transition: all 0.3s ease;
    font-weight: 500;
  }
  
  .nav-link:hover {
    background: var(--card-bg);
    color: var(--accent);
  }
  
  .nav-link.active {
    background: var(--primary);
    color: white;
  }
  
  .nav-number {
    background: var(--accent);
    color: white;
    width: 24px;
    height: 24px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.8em;
  }
  
  /* Theme Toggle */
  .theme-toggle-container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 15px;
    background: var(--card-bg);
    border-radius: 10px;
    margin-top: 20px;
  }
  
  .theme-label {
    font-size: 0.9em;
    color: var(--text-secondary);
  }
  
  .theme-toggle {
    position: relative;
    width: 50px;
    height: 26px;
  }
  
  .theme-checkbox {
    opacity: 0;
    width: 0;
    height: 0;
  }
  
  .theme-slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: var(--neutral);
    transition: .4s;
    border-radius: 34px;
  }
  
  .theme-slider:before {
    position: absolute;
    content: "";
    height: 18px;
    width: 18px;
    left: 4px;
    bottom: 4px;
    background-color: white;
    transition: .4s;
    border-radius: 50%;
  }
  
  .theme-checkbox:checked + .theme-slider {
    background-color: var(--accent);
  }
  
  .theme-checkbox:checked + .theme-slider:before {
    transform: translateX(24px);
  }
  
  /* Main Content - Properly offset for fixed sidebar */
  .main-content {
    padding: 0;
    width: 100%;
    margin-left: 280px;
    min-height: 100vh;
    overflow-x: hidden;
  }
  
  /* Add this new container for content */
  .content-container {
    max-width: 1200px; /* Adjust this value as needed */
    margin: 0 auto; /* Centers the content */
    padding: 50px 30px; /* This controls the text area padding */
    width: 100%;
  }

  /* Justified text */
  .main-content p,
  .main-content li,
  .talk p,
  .project p,
  .gallery-count,
  .link-card p {
    text-align: justify;
    text-justify: inter-word;
    hyphens: auto;
  }
  
  /* Blockquotes should be centered/left, not justified */
  .main-content blockquote {
    text-align: left;
  }
  
  /* Keep headings left-aligned, but exclude sidebar profile headings */
  .main-content h2, 
  .main-content h3,
  .main-content h4,
  .main-content h5,
  .main-content h6,
  .talk h3,
  .project h3,
  .link-card h3 {
    text-align: left;
  }
  
  /* Profile name and title in sidebar should be centered */
  .sidebar h1,
  .sidebar .profile-name,
  .sidebar .profile-title {
    text-align: center;
  }  
  .section {
    margin: 80px 0;
    scroll-margin-top: 40px;
    width: 100%;
    max_width: none;
  }
  
  /* Center profile name and title in sidebar */
  .profile-name,
  .profile-title {
    text-align: center;
    width: 100%;
    display: block;
  }
  
  .section:first-of-type {
    margin-top: 0;
  }
  
  .section-title {
    display: flex;
    align-items: center;
    gap: 15px;
    margin-bottom: 40px;
    padding-bottom: 15px;
    border-bottom: 3px solid var(--accent);
  }
  
  .section-number {
    background: var(--accent);
    color: white;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.2em;
    font-weight: bold;
  }
  
  .section h2 {
    font-size: 2.2em;
    color: var(--text-primary);
    margin: 0;
  }
  
  /* Hamburger Menu (Mobile Only) */
  .hamburger-menu {
    display: none;
    position: fixed;
    top: 20px;
    right: 20px;
    background: var(--accent);
    color: white;
    border: none;
    border-radius: 50%;
    width: 50px;
    height: 50px;
    font-size: 1.5em;
    cursor: pointer;
    z-index: 1001;
    box-shadow: 0 4px 15px rgba(0,0,0,0.2);
  }
  
  .mobile-overlay {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,0.7);
    z-index: 999;
  }
  
  /* Content Cards */
  .talk, .project {
    background: var(--card-bg);
    padding: 35px;
    border-radius: 12px;
    margin: 40px 0;
    border-left: 4px solid var(--accent);
    box-shadow: 0 5px 20px var(--shadow-color);
    transition: all 0.3s ease;
    width: 100%;
  }
  
  .talk:hover, .project:hover {
    transform: translateY(-5px);
    box-shadow: 0 15px 35px var(--shadow-color);
  }
  
  .talk h3, .project h3 {
    font-size: 1.6em;
    color: var(--text-primary);
    margin-bottom: 15px;
  }
  
  .talk img, .project img {
    max-width: 100%;
    border-radius: 8px;
    margin: 20px 0;
    border: 2px solid var(--border-color);
  }
  
  .tools {
    background: linear-gradient(135deg, var(--light) 0%, var(--tertiary) 100%);
    color: white;
    padding: 15px 20px;
    border-radius: 8px;
    margin: 20px 0;
    font-style: italic;
    font-size: 1.05em;
  }
  
  /* Gallery - Improved Layout */
  .gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
    gap: 25px;
    margin: 40px 0;
  }
  
  .gallery-item {
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 8px 25px var(--shadow-color);
    transition: all 0.3s ease;
    cursor: pointer;
    background: var(--card-bg);
    height: 320px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
  }
  
  .gallery-item:hover {
    transform: translateY(-8px) scale(1.02);
    box-shadow: 0 20px 40px var(--shadow-color);
  }
  
  .gallery-item img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    padding: 15px;
    background: var(--bg-primary);
    transition: transform 0.3s ease;
  }
  
  .gallery-item:hover img {
    transform: scale(1.05);
  }
  
  /* Gallery Controls */
  .gallery-controls {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-top: 40px;
  }
  
  .gallery-btn {
    background: linear-gradient(135deg, var(--accent) 0%, var(--warm) 100%);
    color: white;
    border: none;
    padding: 14px 32px;
    border-radius: 25px;
    font-size: 1.1em;
    cursor: pointer;
    transition: all 0.3s ease;
    font-family: 'BrauerNeue', sans-serif;
    font-weight: 500;
  }
  
  .gallery-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 20px rgba(255, 70, 0, 0.3);
    background: linear-gradient(135deg, var(--warm) 0%, var(--accent) 100%);
  }
  
  .gallery-count {
    text-align: center;
    color: var(--text-secondary);
    margin: 20px 0;
    font-style: italic;
    font-size: 1.1em;
  }
  
  /* Links Grid */
  .links-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 30px;
    margin: 40px 0;
  }
  
  .link-card {
    background: var(--card-bg);
    border-radius: 12px;
    padding: 30px;
    text-align: center;
    box-shadow: 0 5px 20px var(--shadow-color);
    transition: all 0.3s ease;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  
  .link-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 15px 35px var(--shadow-color);
  }
  
  .link-card h3 {
    color: var(--text-primary);
    margin-bottom: 15px;
    font-size: 1.4em;
  }
  
  .link-card p {
    color: var(--text-secondary);
    margin-bottom: 25px;
    line-height: 1.6;
    flex-grow: 1;
  }
  
  .link-button {
    display: inline-block;
    background: linear-gradient(135deg, var(--primary) 0%, var(--tertiary) 100%);
    color: white;
    text-decoration: none;
    padding: 12px 24px;
    border-radius: 25px;
    font-weight: 500;
    transition: all 0.3s ease;
    font-family: 'BrauerNeue', sans-serif;
  }
  
  .link-button:hover {
    background: linear-gradient(135deg, var(--accent) 0%, var(--warm) 100%);
    transform: translateY(-2px);
    box-shadow: 0 8px 20px rgba(255, 70, 0, 0.3);
  }
  
  /* Lightbox styles with improved mobile support */
  .lightbox {
    display: none;
    position: fixed;
    z-index: 10000;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0,0,0,0.95);
    -webkit-tap-highlight-color: transparent;
    user-select: none;
    touch-action: pan-y;
  }
  
  .lightbox-content {
    max-width: 90%;
    max-height: 80%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    border-radius: 8px;
    border: 2px solid var(--accent);
    background: black;
    pointer-events: none; /* Prevent image from interfering with swipe */
  }
  
  .close-lightbox {
    position: absolute;
    top: 25px;
    right: 35px;
    color: white;
    font-size: 45px;
    cursor: pointer;
    z-index: 10001;
    background: var(--accent);
    width: 50px;
    height: 50px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 4px 15px rgba(0,0,0,0.3);
  }
  
  .lightbox-nav {
    position: absolute;
    top: 50%;
    width: 100%;
    display: flex;
    justify-content: space-between;
    padding: 0 15px;
    transform: translateY(-50%);
    z-index: 10001;
    opacity: 0.8;
  }
  
  .lightbox-nav button {
    background: rgba(255, 70, 0, 0.8);
    border: none;
    color: white;
    font-size: 24px;
    width: 44px;
    height: 44px;
    border-radius: 50%;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 4px 15px rgba(0,0,0,0.3);
    -webkit-tap-highlight-color: transparent;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .lightbox-nav button:hover {
    background: var(--warm);
    transform: scale(1.1);
    opacity: 1;
  }
  
  /* Mobile Responsive Design - MUST BE IN CORRECT ORDER (large to small) */

  /* Tablet and up (1200px and below) */
  @media (max-width: 1200px) {
    .main-content {
      padding: 40px 50px;
      width: calc(100% - 280px);
      margin-left: 280px;
    }
    .gallery-grid,
    .links-grid {
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    }
  }
  
  /* Tablet and Mobile - Sidebar becomes hamburger menu (992px and below) */
  @media (max-width: 992px) {
    .hamburger-menu {
      display: flex;
      align-items: center;
      justify-content: center;
      opacity: 0;
      transform: translateY(-20px);
      transition: opacity 0.3s ease, transform 0.3s ease;
    }
    /* Show hamburger when scrolled down */
    .hamburger-menu.visible {
      opacity: 1;
      transform: translateY(0);
    }
    .mobile-overlay.active {
      display: block;
    }
    /* Sidebar visible by default on mobile */
    .sidebar {
      position: fixed;
      width: 100%;
      height: auto;
      max-height: 100vh;
      overflow-y: auto;
      transform: translateY(0);
      z-index: 1001;
      padding-top: 80px; /* Make room for hamburger when it appears */
      transition: transform 0.3s ease, padding-top 0.3s ease;
    }
    /* Hide sidebar when hamburger is clicked */
    .sidebar.hidden {
      transform: translateY(-100%);
    }
    /* Main content takes full width */
    .main-content {
      width: 100%;
      margin-left: 0;
      padding: 20px 20px 80px;
      margin-top: 0; /* Start at top */
    }
    /* Profile image smaller on mobile */
    .profile-img {
      width: 120px;
      height: 120px;
    }
    /* Navigation visible by default */
    .nav-menu {
      display: block;
    }
    /* Section adjustments */
    .section {
      margin: 60px 0;
    }
    .gallery-grid,
    .links-grid {
      grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    }
  }
  
  /* Mobile landscape and smaller tablets (768px and below) */
  @media (max-width: 768px) {
    .main-content {
      padding: 20px 15px 80px;
    }
    .section h2 {
      font-size: 1.8em;
    }
    .gallery-grid,
    .links-grid {
      grid-template-columns: 1fr;
      gap: 20px;
    }
    .gallery-item {
      height: 250px;
    }
    .talk, .project {
      padding: 25px;
    }
    .talk h3, .project h3 {
      font-size: 1.4em;
    }
    /* Smaller profile image on very small screens */
    .profile-img {
      width: 100px;
      height: 100px;
    }
    /* Adjust sidebar padding */
    .sidebar {
      padding: 60px 20px 20px;
    }
    /* Lightbox adjustments for tablets */
    .lightbox-nav button {
      width: 40px;
      height: 40px;
      font-size: 20px;
      padding: 0;
    }
    .lightbox-content {
      max-width: 95%;
      max-height: 75%;
    }
  }
  
  /* Small phones (480px and below) */
  @media (max-width: 480px) {
    .section-title {
      flex-direction: column;
      align-items: flex-start;
      gap: 10px;
    }
    .section-number {
      width: 35px;
      height: 35px;
      font-size: 1em;
    }
    .gallery-controls {
      flex-direction: column;
      align-items: center;
    }
    .gallery-btn {
      width: 100%;
      max-width: 300px;
    }
    .contact-links {
      flex-direction: column;
    }
    /* Even smaller profile image */
    .profile-img {
      width: 80px;
      height: 80px;
    }
    /* Condense sidebar content */
    .sidebar {
      padding: 50px 15px 15px;
    }
    .profile-name {
      font-size: 1.5em;
    }
    .profile-title {
      font-size: 0.9em;
    }
    /* Lightbox adjustments for small phones */
    .lightbox-nav {
      display: none;
    }
    .lightbox-content {
      max-width: 98%;
      max-height: 70%;
    }
    .close-lightbox {
      top: 15px;
      right: 20px;
      font-size: 35px;
      width: 40px;
      height: 40px;
    }
  }
  
  /* Hide arrows on touch devices (this should be last) */
  @media (hover: none) and (pointer: coarse) {
    .lightbox-nav {
      display: none; /* Completely hide arrows on all touch devices */
    }
  }
</style>

<!-- Hamburger Menu for Mobile -->
<button class="hamburger-menu" id="hamburgerBtn">
  <span>☰</span>
</button>
<div class="mobile-overlay" id="mobileOverlay"></div>

// Show/hide hamburger based on scroll
let lastScrollTop = 0;
const hamburgerBtn = document.getElementById('hamburgerBtn');
const sidebar = document.getElementById('sidebar');
const mobileOverlay = document.getElementById('mobileOverlay');

// Mobile scrolling behavior
function handleMobileScroll() {
  if (window.innerWidth <= 992) {
    const scrollTop = window.pageYOffset || document.documentElement.scrollTop;
    // Show hamburger when scrolled down more than 100px
    if (scrollTop > 100) {
      hamburgerBtn.classList.add('visible');
      // Auto-hide sidebar when scrolling down
      if (scrollTop > lastScrollTop && scrollTop > 200) {
        sidebar.classList.add('hidden');
        mobileOverlay.classList.remove('active');
      }
    } else {
      hamburgerBtn.classList.remove('visible');
      sidebar.classList.remove('hidden');
    }
    lastScrollTop = scrollTop;
  } else {
    // Reset on desktop
    hamburgerBtn.classList.remove('visible');
    sidebar.classList.remove('hidden');
  }
}

// Update hamburger menu toggle for new behavior
if (hamburgerBtn && sidebar) {
  hamburgerBtn.addEventListener('click', function(e) {
    e.stopPropagation();
    sidebar.classList.toggle('hidden');
    mobileOverlay.classList.toggle('active');
    // Scroll to top when opening sidebar
    if (!sidebar.classList.contains('hidden')) {
      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      });
    }
  });
  
  mobileOverlay.addEventListener('click', function() {
    sidebar.classList.add('hidden');
    mobileOverlay.classList.remove('active');
  });
  
  // Close sidebar when clicking on a nav link on mobile
  document.querySelectorAll('.nav-link').forEach(link => {
    link.addEventListener('click', function() {
      if (window.innerWidth <= 992) {
        sidebar.classList.add('hidden');
        mobileOverlay.classList.remove('active');
      }
    });
  });
}

// Add scroll event listener
window.addEventListener('scroll', handleMobileScroll);
window.addEventListener('resize', handleMobileScroll);

// Initial check
handleMobileScroll();


<div class="layout-container">
  <!-- Sidebar -->
  <aside class="sidebar" id="sidebar">
    <!-- Profile Section -->
    <div class="profile-container">
      <img src="assets/images/profile/headshot.jpg" alt="Muhammad Elsadany" class="profile-img">
      <h1 class="profile-name">Muhammad Elsadany</h1>
      <p class="profile-title">Computational Biologist | Psychiatry Researcher</p>
    </div>
    <!-- Contact Links -->
    <div class="contact-links">
      <a href="mailto:melsadany24@gmail.com" class="contact-link">
        <span>melsadany24@gmail.com</span>
      </a>
      <a href="https://www.linkedin.com/in/melsadany/" class="contact-link" target="_blank">
        <span>LinkedIn Profile</span>
      </a>
      <a href="https://github.com/melsadany" class="contact-link" target="_blank">
        <span>GitHub</span>
      </a>
      <a href="assets/docs/profile/Elsadany-resume_111625.pdf" class="contact-link">
        <span>Resume</span>
      </a>
      <a href="https://orcid.org/0000-0002-1019-3905" class="contact-link" target="_blank">
        <span>ORCiD</span>
      </a>
    </div>
    <!-- Navigation Menu -->
    <nav class="nav-menu">
      <h3 class="nav-title">Portfolio Sections</h3>
      <ul class="nav-list">
        <li class="nav-item">
          <a href="#about" class="nav-link">
            <span class="nav-number">01</span>
            <span>About Me</span>
          </a>
        </li>
        <li class="nav-item">
          <a href="#video-summary" class="nav-link">
            <span class="nav-number">02</span>
            <span>Video Summary</span>
          </a>
        </li>
        <li class="nav-item">
          <a href="#talks" class="nav-link">
            <span class="nav-number">03</span>
            <span>Talks & Presentations</span>
          </a>
        </li>
        <li class="nav-item">
          <a href="#projects" class="nav-link">
            <span class="nav-number">04</span>
            <span>Research Projects</span>
          </a>
        </li>
        <li class="nav-item">
          <a href="#gallery" class="nav-link">
            <span class="nav-number">05</span>
            <span>Visualization Gallery</span>
          </a>
        </li>
        <li class="nav-item">
          <a href="#media-links" class="nav-link">
            <span class="nav-number">06</span>
            <span>Media & Links</span>
          </a>
        </li>
      </ul>
    </nav>
    <!-- Theme Toggle -->
    <div class="theme-toggle-container">
      <span class="theme-label">Theme</span>
      <label class="theme-toggle">
        <input type="checkbox" class="theme-checkbox" id="themeToggle">
        <span class="theme-slider"></span>
      </label>
    </div>
  </aside>
  
  <!-- Main Content -->
  <main class="main-content">
    <div class="content-container">
    <!-- About Me Section -->
    <section id="about" class="section">
      <div class="section-title">
        <div class="section-number">01</div>
        <h2>About Me</h2>
      </div>
      <p>My passion for genetics and mental health research stems from both personal experience and a deep curiosity about human behavior. As an autistic researcher, I bring a unique perspective to understanding neurodiversity—not just as a subject of study, but as a lived reality.</p>
      <p>My research focuses on decoding the complex relationships between genetics, cognition, and mental health through computational approaches. I integrate diverse data modalities—genetic, clinical, neuroimaging, audio, interview, and facial imagery—to uncover patterns that bridge scientific discovery with practical interventions.</p>
      <p>A central theme of my research is leveraging language as a powerful metric for understanding cognitive functions and mental health challenges. I'm particularly interested in developing accessible tools that can capture the nuances of human experience often missed by traditional assessments.</p>
      <p>My journey in the lab revealed how much I 'fit in' with the populations we study, leading to being professionally diagnosed with autism at 25. This personal insight fuels my commitment to creating a more inclusive world where neurodiverse individuals are not just understood, but valued for their unique strengths.</p>
      <blockquote style="font-style: italic; border-left: 3px solid var(--accent); padding-left: 20px; margin: 30px 0; color: var(--text-secondary);">
        "I learn by going where I have to go." – Theodore Roethke
      </blockquote>
      <p><em>Currently pursuing my PhD in Computational Genetics at the University of Iowa, where I'm expanding my expertise in linguistics, computer vision, neuroimaging, and data science to better serve the neurodiversity community.</em></p>
    </section>
    <!-- Video Summary Section -->
    <section id="video-summary" class="section">
      <div class="section-title">
        <div class="section-number">02</div>
        <h2>Video Summary</h2>
      </div>
      <p>For a quick overview of my research and background, watch this video summary created by NotebookLM:</p>
      <div style="max-width: 800px; margin: 30px auto;">
        <video 
          id="summaryVideo"
          controls
          controlsList="nodownload" 
          poster="assets/video/overview.png"
          style="width: 100%; border-radius: 10px;"
        >
        
          <source src="assets/video/vid-2.mp4" type="video/mp4">
          Your browser doesn't support the video tag.
        </video>
      </div>
    </section>
    <!-- Talks Section -->
    <section id="talks" class="section">
      <div class="section-title">
        <div class="section-number">03</div>
        <h2>Selected Talks & Presentations</h2>
      </div>
      <div class="talk">
        <h3>Beyond Yes/No: A Multimodal Autism Propensity Score from Genes to Brain</h3>
        <p><strong>INSAR Conference 2025</strong> | <em>Oral Presentation</em></p>
        <img src="assets/images/INSAR/overview.jpg" alt="INSAR Presentation Preview">
        <p>Presented a novel deep learning framework that integrates multi-modal neuroimaging features—including fractional amplitude of low-frequency fluctuations (fALFF), structural morphometry, and diffusion tensor imaging (DTI) metrics—to generate a continuous autism likelihood score (0-1). This approach demonstrates the potential of combining multiple MRI modalities for improved neurophenotyping in autism spectrum disorder.</p>
        <div class="tools">
          <strong>Key Topics:</strong> Deep Learning, Multi-modal MRI Integration, fALFF, Structural MRI, DTI, Autism Biomarkers
        </div>
      </div>
      <div class="talk">
        <h3>Optimizing Structural MRI Processing Pipelines for 7T Data</h3>
        <p><strong>Iowa Neuroimaging Consortium, University of Iowa</strong> | <em>Invited Talk</em></p>
        <img src="assets/images/MRI-pipeline/overview.jpg" alt="MRI Pipeline Preview">
        <p>Comprehensive overview of structural MRI processing pipelines optimized for 7T scanner data, comparing various tools and approaches for cortical reconstruction, subcortical segmentation, and surface-based analysis. Provided practical guidance on pipeline selection based on specific research objectives and data characteristics.</p>
        <div class="tools">
          <strong>Key Topics:</strong> 7T MRI, Structural Processing Pipelines, Freesurfer, ANTs, FSL, Cortical Reconstruction, Quality Control
        </div>
      </div>
    </section>
    <!-- Projects Section -->
    <section id="projects" class="section">
      <div class="section-title">
        <div class="section-number">04</div>
        <h2>Featured Projects</h2>
      </div>
      <div class="project">
        <h3>Gene Expression Signature of Human Brain Stimulation</h3>
        <img src="assets/images/brain-stim/overview.jpg" alt="Brain Stimulation Analysis">
        <ul>
          <li>Engineered an end-to-end computational pipeline for single-nuclei multi-omics (RNA+ATAC) data, implementing a bootstrapped pseudo-bulk strategy and mixed-effects models (lmmSeq) to identify cell-type-specific responses to electrical stimulation.</li>
          <li>Validated translational relevance through cross-species comparison (RRHO) with mouse models, identifying conserved gene sets.</li>
        </ul>
        <div class="tools">
          <strong>Tools:</strong> R, Seurat, lmmSeq, RRHO2, CellChat, scSeqComm, edgeR, DCA
        </div>
      </div>
      <div class="project">
        <h3>Exceptional Ability: A Multimodal Cognitive Study</h3>
        <img src="assets/images/te/overview-PS.jpg" alt="Exceptional Ability Overview">
        <ul>
          <li>Designed and implemented a multimodal analysis pipeline integrating NIH-Toolbox/IQ scores, a custom language task, acoustic feature extraction (audio), interview transcription (Whisper AI), facial landmarking (computer vision), and structural/functional/diffusion MRI.</li>
          <li>Developed a 10-minute language task that effectively captures cognitive performance, demonstrating potential as an efficient digital biomarker.</li>
        </ul>
        <div class="tools">
          <strong>Tools:</strong> WhisperAI, PWEsuite, GPT, Archetypes, lingmatch, ANTs, AFNI, FSL, freesurfer, DSI-studio
        </div>
      </div>
      <div class="project">
        <h3>Polygenic Drug Response Signatures</h3>
        <img src="assets/images/drug-response/overview.jpg" alt="Drug Response Analysis">
        <ul>
          <li>Developed a computational tool integrating genetic data (GWAS, eQTL, RNA-Seq) to generate personalized treatment recommendations for psychiatric disorders, with a focus on ADHD.</li>
          <li>Scaled the application to cohorts with 88,000+ participants (SPARK, ABCD) and validated predictions against behavioral scales (CBCL, BPM) and neuroimaging (fMRI) data.</li>
        </ul>
        <div class="tools">
          <strong>Tools:</strong> GWAS, eQTL, TWAS
        </div>
      </div>
      <div class="project">
        <h3>Mapping Brain-Wide Drug Effects using Deep Learning</h3>
        <img src="assets/images/drug-maps/overview2.jpg" alt="Drug Effects Brain Map">
        <ul>
          <li>Built a deep learning model that integrates brain-wide gene expression (Allen Institute) and fMRI trait maps with drug perturbation signatures (CMAP, LINCS) to predict functional brain activity changes for 838 compounds.</li>
          <li>Delivered insights through an interactive R Shiny application featuring 3D brain visualizations, linking compounds to phenotypic effects via Neurosynth and Neuromaps.</li>
        </ul>
        <div class="tools">
          <strong>Tools:</strong> DL, eQTL, TWAS, R Shiny
        </div>
      </div>
      <div class="project">
        <h3>Linguistic and Behavioral Patterns in Bipolar Disorder from Social Media</h3>
        <img src="assets/images/bp-reddit/overview.jpg" alt="Bipolar Reddit Analysis">
        <ul>
          <li>Analyzed 20 years of Reddit data to identify users self-identifying with bipolar disorder, extracting temporal patterns in activity, sleep cycles, emotional expression, and content preferences.</li>
          <li>Applied natural language processing to track linguistic markers of mood episodes, including sentiment analysis, topic modeling, and GPT-4 embeddings to quantify emotional volatility over time.</li>
          <li>Identified distinct behavioral signatures including disrupted sleep patterns (via posting times), content topic shifts, and cyclical emotional patterns corresponding to reported mood episodes.</li>
        </ul>
        <div class="tools">
          <strong>Tools:</strong> Python, NLP, GPT-4 Embeddings, Time-series Analysis, Sentiment Analysis, Topic Modeling
        </div>
      </div>
    </section>
    <!-- Gallery Section -->
    <section id="gallery" class="section">
      <div class="section-title">
        <div class="section-number">05</div>
        <h2>Data Visualization Gallery</h2>
      </div>
      <p>Explore my favorite data visualizations across all research projects. Click on any visualization to view it in full size. Swipe left/right on mobile to navigate.</p>
      <div id="gallery-container" class="gallery-grid">
        <!-- Gallery will be populated by JavaScript -->
      </div>
      <div class="gallery-count" id="gallery-count">
        Loading gallery...
      </div>
      <div class="gallery-controls">
        <button id="show-more-btn" class="gallery-btn">Show More Visualizations</button>
        <button id="show-less-btn" class="gallery-btn" style="display: none;">Show Less</button>
      </div>
    </section>
    <!-- Media & Links Section -->
    <section id="media-links" class="section">
      <div class="section-title">
        <div class="section-number">06</div>
        <h2>Media & Additional Links</h2>
      </div>
      <p>Explore more about my background, research environment, and contributions:</p>
      <div class="links-grid">
        <div class="link-card">
          <h3>My Personal Journey</h3>
          <p>Read about my path into computational psychiatry and neurodiversity research</p>
          <a href="https://michaelson.lab.uiowa.edu/news/2025/02/ui-psychiatry-graduate-student-muhammad-elsadany-decodes-mental-health-data-and-his" class="link-button" target="_blank">Read Story</a>
        </div>
        <div class="link-card">
          <h3>Michaelson Lab</h3>
          <p>Learn about the research environment and team behind my PhD work</p>
          <a href="https://michaelson.lab.uiowa.edu/people/muhammad-elsadany" class="link-button" target="_blank">Visit Lab</a>
        </div>
        <div class="link-card">
          <h3>IGP in Genetics</h3>
          <p>Explore the interdisciplinary genetics program at University of Iowa</p>
          <a href="https://genetics.grad.uiowa.edu/people/muhammad-elsadany" class="link-button" target="_blank">Program Info</a>
        </div>
        <div class="link-card">
          <h3>Research Features</h3>
          <p>News article about our research</p>
          <a href="https://medicineiowa.org/fall-2024/closer-exceptional-processing" class="link-button" target="_blank">View Articles</a>
        </div>
        <div class="link-card">
          <h3>INSAR Talk</h3>
          <p>Slides from my presentation at INSAR</p>
          <a href="assets/docs/talks/INSAR.ppsx" class="link-button">Access Materials</a>
        </div>
        <div class="link-card">
          <h3>INC Talk</h3>
          <p>Slides from my presentation at INC</p>
          <a href="assets/docs/talks/INC.ppsx" class="link-button">Access Materials</a>
        </div>
        <div class="link-card">
          <h3>Seminar Talk</h3>
          <p>Slides from my last presentation at the IGPG seminar series</p>
          <a href="assets/docs/talks/te-PS.ppsx" class="link-button">Access Materials</a>
        </div>
      </div>
    </section>
    </div>
  </main>

  <!-- Lightbox Modal -->
  <div id="lightbox" class="lightbox">
    <span class="close-lightbox" onclick="closeLightbox()">&times;</span>
    <div class="lightbox-nav">
      <button onclick="changeImage(-1)">&#10094;</button>
      <button onclick="changeImage(1)">&#10095;</button>
    </div>
    <img class="lightbox-content" id="lightbox-img">
  </div>

<script>
  // Theme Toggle
  const themeToggle = document.getElementById('themeToggle');
  const prefersDarkScheme = window.matchMedia('(prefers-color-scheme: dark)');
  
  // Set initial theme
  let currentTheme = localStorage.getItem('theme') || (prefersDarkScheme.matches ? 'dark' : 'light');
  document.documentElement.setAttribute('data-theme', currentTheme);
  themeToggle.checked = currentTheme === 'dark';
  
  // Toggle theme
  themeToggle.addEventListener('change', function() {
    const newTheme = this.checked ? 'dark' : 'light';
    document.documentElement.setAttribute('data-theme', newTheme);
    localStorage.setItem('theme', newTheme);
  });
  
  // Hamburger Menu Toggle
  const hamburgerBtn = document.getElementById('hamburgerBtn');
  const sidebar = document.getElementById('sidebar');
  const mobileOverlay = document.getElementById('mobileOverlay');
  
  if (hamburgerBtn && sidebar) {
    hamburgerBtn.addEventListener('click', function() {
      sidebar.classList.toggle('active');
      mobileOverlay.classList.toggle('active');
    });
    mobileOverlay.addEventListener('click', function() {
      sidebar.classList.remove('active');
      mobileOverlay.classList.remove('active');
    });
    // Close sidebar when clicking on a nav link on mobile
    document.querySelectorAll('.nav-link').forEach(link => {
      link.addEventListener('click', function() {
        if (window.innerWidth <= 992) {
          sidebar.classList.remove('active');
          mobileOverlay.classList.remove('active');
        }
      });
    });
  }
  
  // Gallery functionality
  document.addEventListener('DOMContentLoaded', function() {
    const galleryImages = [
      'assets/gallery/arch-1.png',
      'assets/gallery/dwi.jpg',
      'assets/gallery/nct-1.png',
      'assets/gallery/rpoe-data.png',
      'assets/gallery/iq-2.png',
      'assets/gallery/wc-1.png',
      'assets/gallery/sche-1.png',
      'assets/gallery/sche-2.png',
      'assets/gallery/line-2.png',
      'assets/gallery/resid-1.png',
      'assets/gallery/rad-1.svg',
      'assets/gallery/ne-1.jpg',
      'assets/images/drug-maps/overview.jpg',
      'assets/images/te/overview-lang.jpg',
      'assets/gallery/bar-1.png',
      'assets/gallery/bm-v1.jpg',
      'assets/gallery/cyto-1.jpg',
      'assets/gallery/den-1.png',
      'assets/gallery/den-2.png',
      'assets/gallery/den-3.jpg',
      'assets/gallery/euc-1.jpg',
      'assets/gallery/fALFF-1.png',
      'assets/gallery/forest-1.png',
      'assets/gallery/dti-res-1.png',
      'assets/gallery/jeo-1.png',
      'assets/gallery/loli-1.png',
      'assets/gallery/mo-1.png',
      'assets/gallery/mph-1.svg',
      'assets/gallery/net-1.png',
      'assets/gallery/net-2.png',
      'assets/gallery/peaks-1.jpg',
      'assets/gallery/scat-1.png',
      'assets/gallery/scat-2.png',
      'assets/gallery/scat-3.png',
      'assets/gallery/sel-1.jpg',
      'assets/gallery/sem-1.png',
      'assets/gallery/sem-2.jpg',
      'assets/gallery/st.png',
      'assets/gallery/time-1.gif',
      'assets/gallery/time-2.png',
      'assets/gallery/umap-1.jpg',
      'assets/gallery/upset-1.png',
      'assets/gallery/viol-1.png'
    ];
  
  const galleryContainer = document.getElementById('gallery-container');
  const showMoreBtn = document.getElementById('show-more-btn');
  const showLessBtn = document.getElementById('show-less-btn');
  const galleryCount = document.getElementById('gallery-count');
  let currentImageIndex = 0;
  let imagesPerLoad = 6;
  let currentlyVisible = 0;
  let isLightboxOpen = false;
  
  // Initialize gallery
  if (galleryContainer && galleryImages.length > 0) {
    loadMoreImages();
    updateButtonVisibility();
  }
  
  function loadMoreImages() {
    const endIndex = Math.min(currentlyVisible + imagesPerLoad, galleryImages.length);
    for (let i = currentlyVisible; i < endIndex; i++) {
      const galleryItem = document.createElement('div');
      galleryItem.className = 'gallery-item';
      galleryItem.onclick = () => openLightbox(i);
      const img = document.createElement('img');
      img.src = galleryImages[i];
      img.alt = 'Research Visualization';
      img.loading = 'lazy';
      galleryItem.appendChild(img);
      galleryContainer.appendChild(galleryItem);
    }
    currentlyVisible = endIndex;
    updateButtonVisibility();
    updateGalleryCount();
  }
  
  function showLessImages() {
    galleryContainer.innerHTML = '';
    currentlyVisible = 0;
    loadMoreImages();
  }
  
  function updateButtonVisibility() {
    if (currentlyVisible >= galleryImages.length) {
      showMoreBtn.style.display = 'none';
      showLessBtn.style.display = 'block';
    } else {
      showMoreBtn.style.display = 'block';
      showLessBtn.style.display = 'none';
    }
  }
  
  function updateGalleryCount() {
    galleryCount.textContent = `Showing ${currentlyVisible} of ${galleryImages.length} visualizations`;
  }
  
  // Improved lightbox functions with better mobile handling
  window.openLightbox = function(index) {
    currentImageIndex = index;
    const lightbox = document.getElementById('lightbox');
    const lightboxImg = document.getElementById('lightbox-img');
    lightbox.style.display = 'block';
    lightbox.classList.add('active');
    lightboxImg.src = galleryImages[index];
    isLightboxOpen = true;
    document.body.style.overflow = 'hidden';
    // Auto-hide arrows on mobile after 2 seconds
    if ('ontouchstart' in window) {
      setTimeout(() => {
        lightbox.classList.remove('active');
      }, 2000);
    }
    // Force focus for accessibility
    lightbox.focus();
  }
  
  window.closeLightbox = function() {
    const lightbox = document.getElementById('lightbox');
    lightbox.style.display = 'none';
    lightbox.classList.remove('active');
    isLightboxOpen = false;
    document.body.style.overflow = 'auto';
  }
  
  window.changeImage = function(step) {
    currentImageIndex += step;
    if (currentImageIndex >= galleryImages.length) {
      currentImageIndex = 0;
    } else if (currentImageIndex < 0) {
      currentImageIndex = galleryImages.length - 1;
    }
    document.getElementById('lightbox-img').src = galleryImages[currentImageIndex];
    // Show arrows briefly when changing image on mobile
    if ('ontouchstart' in window) {
      const lightbox = document.getElementById('lightbox');
      lightbox.classList.add('active');
      setTimeout(() => {
        lightbox.classList.remove('active');
      }, 1500);
    }
  }
  
  // Enhanced touch handling for swiping
  let touchStartX = 0;
  let touchEndX = 0;
  
  document.getElementById('lightbox').addEventListener('touchstart', function(e) {
    touchStartX = e.changedTouches[0].screenX;
    // Show arrows when touching lightbox
    this.classList.add('active');
  }, {passive: true});
  
  document.getElementById('lightbox').addEventListener('touchend', function(e) {
    touchEndX = e.changedTouches[0].screenX;
    const diffX = touchStartX - touchEndX;
    const swipeThreshold = 50; // Minimum swipe distance
    if (Math.abs(diffX) > swipeThreshold) {
      if (diffX > 0) {
        // Swiped left - next image
        changeImage(1);
      } else {
        // Swiped right - previous image
        changeImage(-1);
      }
    }
    // Hide arrows after swipe
    setTimeout(() => {
      this.classList.remove('active');
    }, 1000);
  }, {passive: true});
  
  // Button event listeners
  showMoreBtn.addEventListener('click', loadMoreImages);
  showLessBtn.addEventListener('click', showLessImages);
  
  // Keyboard navigation
  document.addEventListener('keydown', function(e) {
    if (!isLightboxOpen) return;
    if (e.key === 'Escape') {
      closeLightbox();
    } else if (e.key === 'ArrowLeft') {
      changeImage(-1);
    } else if (e.key === 'ArrowRight') {
      changeImage(1);
    }
  });
  
  // Close lightbox when clicking outside the image
  document.getElementById('lightbox').addEventListener('click', function(e) {
    if (e.target === this) {
      closeLightbox();
    }
  });
  
  // Smooth scrolling for navigation links
  document.querySelectorAll('.nav-link').forEach(link => {
    link.addEventListener('click', function(e) {
      e.preventDefault();
      const targetId = this.getAttribute('href');
      const targetElement = document.querySelector(targetId);
      if (targetElement) {
        // Update active link
        document.querySelectorAll('.nav-link').forEach(l => l.classList.remove('active'));
        this.classList.add('active');
        // Scroll to section
        window.scrollTo({
          top: targetElement.offsetTop - 40,
          behavior: 'smooth'
        });
      }
    });
  });
  
  // Update active nav link on scroll
  window.addEventListener('scroll', function() {
    const sections = document.querySelectorAll('.section');
    const scrollPos = window.scrollY + 100;
    sections.forEach(section => {
      const sectionTop = section.offsetTop;
      const sectionBottom = sectionTop + section.offsetHeight;
      const sectionId = section.getAttribute('id');
      if (scrollPos >= sectionTop && scrollPos < sectionBottom) {
        document.querySelectorAll('.nav-link').forEach(link => {
          link.classList.remove('active');
          if (link.getAttribute('href') === `#${sectionId}`) {
            link.classList.add('active');
          }
        });
      }
    });
  });
  
  // Video protection
  const video = document.getElementById('summaryVideo');
  if (video) {
    video.addEventListener('contextmenu', function(e) {
      e.preventDefault();
    });
    document.addEventListener('keydown', function(e) {
      if (e.ctrlKey && (e.key === 's' || e.key === 'S')) {
        e.preventDefault();
      }
    });
  }
});
</script>