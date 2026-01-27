---
title: "Muhammad Elsadany | Portfolio"
layout: default
---

<style>
  /* Import and define BrauerNeue font - Headings only */
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
  
  /* CSS Variables - Simplified Color Palette */
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
    /* Simplified Core Colors */
    --primary: #4782b4;
    --accent: #ff4600;
    --accent-light: #88ADE1;
    --accent-dark: #3C4856;
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
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
    line-height: 1.6;
    color: var(--text-primary);
    background: var(--bg-gradient);
    background-attachment: fixed;
    min-height: 100vh;
    transition: all 0.3s ease;
  }
  
  /* Use BrauerNeue only for headings */
  h1, h2, h3, h4, h5, h6 {
    font-family: 'BrauerNeue', sans-serif;
  }
  
  /* Hide the download buttons */
  .btn, .header-btn {
    display: none !important;
  }
  
  /* Page Header - Hidden */
  .page-header {
    display: none !important;
  }
  
  /* Main Layout */
  .layout-container {
    display: block;
    min-height: 100vh;
    width: 100%;
    background: var(--bg-primary);
  }
  
  /* Sidebar */
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
    text-align: center;
  }
  
  .profile-title {
    color: var(--accent);
    font-size: 1em;
    margin-bottom: 5px;
    text-align: center;
    font-weight: 600;
  }
  
  .profile-role {
    color: var(--text-secondary);
    font-size: 0.95em;
    margin-bottom: 20px;
    text-align: center;
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
    font-size: 0.95em;
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
    font-size: 0.85em;
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
    font-size: 0.95em;
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
    flex-shrink: 0;
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
    background-color: #ccc;
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
  
  /* Main Content */
  .main-content {
    padding: 0;
    width: calc(100% - 280px);
    margin-left: 280px;
    min-height: 100vh;
    overflow-x: hidden;
  }
  
  .content-container {
    max-width: 1200px; /* Adjust this value as needed */
    margin: 0 auto; /* Centers the content */
    padding: 50px 30px; /* This controls the text area padding */
    width: 100%;
  }
  
  /* Hero Statement - NEW */
  .hero-statement {
      background: transparent;
      color: var(--text-primary);
      padding: 40px;
      border-radius: 12px;
      margin-bottom: 50px;
      box-shadow: none;
  }
    
  .hero-statement h2 {
    font-size: 2em;
    margin-bottom: 15px;
    color: var(--accent);
  }
    
  .hero-statement p {
    font-size: 1.1em;
    line-height: 1.7;
    margin: 0;
    color: var(--text-secondary);
  }
  
  /* Text alignment and readability */
  .main-content p,
  .main-content li,
  .talk p,
  .project p,
  .gallery-count,
  .link-card p {
    text-align: left;
    line-height: 1.7;
  }
  
  .main-content blockquote {
    text-align: left;
  }
  
  .main-content p em {
    font-size: inherit;
    font-style: italic;
    color: inherit;
  }
  
  /* Sections */
  .section {
    margin: 80px 0;
    scroll-margin-top: 40px;
    width: 100%;
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
    flex-shrink: 0;
  }
  
  .section h2 {
    font-size: 2.2em;
    color: var(--text-primary);
    margin: 0;
  }
  
  /* Hamburger Menu */
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
  
  .project + .project {
    margin-top: 50px;
  }
  
  .talk p strong,
  .project p strong {
    font-size: 0.95em;
    color: var(--text-secondary);
  }
  
  /* Callout boxes */
  .callout-box {
    background: linear-gradient(135deg, var(--accent-light) 0%, var(--primary) 100%);
    color: white;
    padding: 20px 25px;
    border-radius: 8px;
    margin: 25px 0;
    font-style: italic;
    border-left: 4px solid var(--accent);
  }
  
  .callout-box ul {
    margin: 10px 0 0 20px;
    padding: 0;
  }
  
  .callout-box li {
    margin-bottom: 8px;
  }
  
  /* Lighter callout variant */
  .callout-box.light {
    background: var(--card-bg);
    color: var(--text-primary);
    border: 1px solid var(--border-color);
  }
  
  .callout-box.light ul {
    color: var(--text-primary);
  }
  
  /* Gallery */
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
  
  /* Gallery caption overlay - NEW */
  .gallery-caption {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background: rgba(0,0,0,0.8);
    color: white;
    padding: 10px 15px;
    font-size: 0.85em;
    opacity: 0;
    transition: opacity 0.3s ease;
  }
  
  .gallery-item:hover .gallery-caption {
    opacity: 1;
  }
  
  .gallery-controls {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-top: 40px;
  }
  
  .gallery-btn {
    background: linear-gradient(135deg, var(--accent) 0%, var(--accent-dark) 100%);
    color: white;
    border: none;
    padding: 14px 32px;
    border-radius: 25px;
    font-size: 1em;
    cursor: pointer;
    transition: all 0.3s ease;
    font-weight: 600;
  }
  
  .gallery-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 20px rgba(255, 70, 0, 0.3);
  }
  
  .gallery-count {
    text-align: center;
    color: var(--text-secondary);
    margin: 20px 0;
    font-style: italic;
    font-size: 1em;
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
    background: linear-gradient(135deg, var(--primary) 0%, var(--accent-light) 100%);
    color: white;
    text-decoration: none;
    padding: 12px 24px;
    border-radius: 25px;
    font-weight: 600;
    transition: all 0.3s ease;
  }
  
  .link-button:hover {
    background: linear-gradient(135deg, var(--accent) 0%, var(--accent-dark) 100%);
    transform: translateY(-2px);
    box-shadow: 0 8px 20px rgba(255, 70, 0, 0.3);
  }
  
  /* Inline slide links in talks */
  .talk-slides {
    display: inline-block;
    margin-left: 10px;
  }
  
  .talk-slides a {
    color: var(--accent);
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s ease;
  }
  
  .talk-slides a:hover {
    color: var(--accent-dark);
    text-decoration: underline;
  }
  
  /* Lightbox */
  .lightbox {
    display: none;
    position: fixed;
    z-index: 10000;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0,0,0,0.95);
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
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .lightbox-nav button:hover {
    background: var(--accent-dark);
    transform: scale(1.1);
    opacity: 1;
  }
  
  /* Footer - NEW */
  footer {
    background: var(--bg-secondary);
    border-top: 1px solid var(--border-color);
    padding: 30px;
    text-align: center;
    color: var(--text-secondary);
    font-size: 0.9em;
    margin-top: 80px;
  }
  
  footer p {
    margin: 0;
  }
  
  /* Mobile Responsive Design */
  @media (max-width: 1200px) {
    .main-content {
      width: calc(100% - 280px);
      margin-left: 280px;
    }
    .gallery-grid,
    .links-grid {
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    }
  }
  
  @media (max-width: 992px) {
    .hamburger-menu {
      display: flex;
      align-items: center;
      justify-content: center;
    }
    
    .mobile-overlay.active {
      display: block;
    }
    
    .sidebar {
      position: fixed;
      width: 100%;
      height: auto;
      max-height: 100vh;
      overflow-y: auto;
      transform: translateY(0);
      z-index: 1001;
      padding: 80px 25px 25px;
      transition: transform 0.3s ease;
    }
    
    .sidebar.hidden {
      transform: translateY(-100%);
    }
    
    .main-content {
      width: 100%;
      margin-left: 0;
      padding: 80px 20px;
    }
    
    .content-container {
      padding: 0 20px;
    }
    
    .profile-img {
      width: 140px;
      height: 140px;
      margin-bottom: 25px;
    }
    
    .section {
      margin: 60px 0;
    }
    
    .gallery-grid,
    .links-grid {
      grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    }
    
    
    .hero-statement {
      padding: 30px;
      margin-bottom: 40px;
    }
    
    .hero-statement h2 {
      font-size: 1.6em;
    }
  }
  
  @media (max-width: 768px) {
    .main-content {
      padding: 80px 15px;
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
    
    .profile-img {
      width: 100px;
      height: 100px;
    }
    
    .sidebar {
      padding: 60px 20px 20px;
    }
    
    .lightbox-nav button {
      width: 40px;
      height: 40px;
      font-size: 20px;
    }
    
    .lightbox-content {
      max-width: 95%;
      max-height: 75%;
    }
  }
  
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
    
    .gallery-item {
      height: 220px;
    }
    
    .profile-img {
      width: 80px;
      height: 80px;
    }
    
    .sidebar {
      padding: 50px 15px 15px;
    }
    
    .profile-name {
      font-size: 1.5em;
    }
    
    .profile-title {
      font-size: 0.9em;
    }
    
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
    
    .hero-statement h2 {
      font-size: 1.4em;
    }
    
    .hero-statement p {
      font-size: 1em;
    }
  }
  
  @media (hover: none) and (pointer: coarse) {
    .lightbox-nav {
      display: none;
    }
  }
</style>

<!-- Hamburger Menu -->
<button class="hamburger-menu" id="hamburgerBtn">
  <span>☰</span>
</button>
<div class="mobile-overlay" id="mobileOverlay"></div>

<div class="layout-container">
  <!-- Sidebar -->
  <aside class="sidebar" id="sidebar">
    <div class="profile-container">
      <img src="assets/images/profile/headshot.jpg" alt="Muhammad Elsadany" class="profile-img">
      <h1 class="profile-name">Muhammad Elsadany</h1>
      <p class="profile-title">PhD Candidate, Computational Genetics</p>
      <p class="profile-role">University of Iowa | Psychiatry Department</p>
    </div>
    
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
      <a href="assets/docs/profile/Elsadany-resume_122825.pdf" class="contact-link">
        <span>Resume (PDF)</span>
      </a>
      <a href="https://orcid.org/0000-0002-1019-3905" class="contact-link" target="_blank">
        <span>ORCiD</span>
      </a>
    </div>
    
    <nav class="nav-menu">
      <h3 class="nav-title">Navigation</h3>
      <ul class="nav-list">
        <li class="nav-item">
          <a href="#about" class="nav-link">
            <span class="nav-number">01</span>
            <span>About</span>
          </a>
        </li>
        <li class="nav-item">
          <a href="#expertise" class="nav-link">
            <span class="nav-number">02</span>
            <span>Expertise</span>
          </a>
        </li>
        <li class="nav-item">
          <a href="#projects" class="nav-link">
            <span class="nav-number">03</span>
            <span>Projects</span>
          </a>
        </li>
        <li class="nav-item">
          <a href="#talks" class="nav-link">
            <span class="nav-number">04</span>
            <span>Talks</span>
          </a>
        </li>
        <li class="nav-item">
          <a href="#gallery" class="nav-link">
            <span class="nav-number">05</span>
            <span>Gallery</span>
          </a>
        </li>
        <li class="nav-item">
          <a href="#links" class="nav-link">
            <span class="nav-number">06</span>
            <span>Links</span>
          </a>
        </li>
      </ul>
    </nav>
    
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
      
      <!-- Hero Statement - NEW -->
      <div class="hero-statement">
        <h2>Multimodal Mental Health Data Scientist</h2>
        <p>I build computational tools that bridge genetics, neuroimaging, and behavior to unlock insights for neurodiversity and psychiatric research. Currently finishing my PhD at University of Iowa.</p>
      </div>
      
      <div style="margin-bottom: 30px; text-align: right;">
        <a href="assets/docs/profile/Elsadany-resume_122825.pdf" class="link-button" target="_blank">
          ↓ Download Resume (PDF)
        </a>
      </div>
      
      <!-- About Me Section - UPDATED -->
      <section id="about" class="section">
        <div class="section-title">
          <div class="section-number">01</div>
          <h2>About Me</h2>
        </div>
        
        <p><strong>My passion:</strong> I combine genetics, neuroimaging, and language analysis to understand mental health at the intersection of biology and behavior. As an autistic researcher, I bring lived experience to understanding neurodiversity—and I'm building tools that actually serve this community.</p>
        
        <p>My research integrates diverse data modalities—genetic, clinical, neuroimaging, audio, interview transcripts, and facial imagery to uncover patterns that bridge laboratory discovery with real clinical interventions.</p>
        
        <div class="callout-box">
          <strong>What I'm looking for:</strong>
          <ul>
            <li>Clinical informatics / health data science roles in psychiatry, neurology, or genomics</li>
            <li>Computational genetics / statistical genetics positions with large-scale cohorts</li>
            <li>Data science roles in biotech, health tech, or research institutes</li>
            <li>Positions that value reproducible science and open-source tools</li>
          </ul>
        </div>
        
        <p><em>I'm wrapping up my PhD in April 2026 and actively networking. Let's chat about opportunities!</em></p>
      </section>
      
      <!-- Expertise Section - NEW (replaces Code & Tools + condenses Projects) -->
      <section id="expertise" class="section">
        <div class="section-title">
          <div class="section-number">02</div>
          <h2>Expertise & Tools</h2>
        </div>
        
        <p>My work spans multimodal data analysis, reproducible pipeline development, and computational tool building for psychiatric research.</p>
        
        <div class="links-grid">
          <div class="link-card">
            <h3>Neuroimaging</h3>
            <p>7T structural MRI processing, fMRI analysis, DTI, cortical reconstruction, surface-based morphometry</p>
            <p style="font-size: 0.9em; color: var(--text-secondary);">freesurfer · ANTs · FSL · AFNI · nilearn</p>
          </div>
          <div class="link-card">
            <h3>Genomics</h3>
            <p>GWAS, eQTL analysis, transcriptomics, single-nuclei multi-omics, expression-QTL integration</p>
            <p style="font-size: 0.9em; color: var(--text-secondary);">R · Python · TWAS · Seurat · edgeR</p>
          </div>
          <div class="link-card">
            <h3>NLP & Behavior</h3>
            <p>Acoustic feature extraction, interview transcription, sentiment analysis, linguistic biomarkers, emotion detection</p>
            <p style="font-size: 0.9em; color: var(--text-secondary);">WhisperAI · GPT · lingmatch · topic modeling</p>
          </div>
          <div class="link-card">
            <h3>Reproducible Science</h3>
            <p>End-to-end computational pipelines, QC workflows, interactive visualizations, open-source development</p>
            <p style="font-size: 0.9em; color: var(--text-secondary);">Git · Bash · R Shiny · Docker</p>
          </div>
          <div class="link-card">
            <h3>Statistical Analysis</h3>
            <p>Mixed-effects modeling, machine learning, deep learning for phenotype prediction, cross-species validation</p>
            <p style="font-size: 0.9em; color: var(--text-secondary);">lmmSeq · scikit-learn · TensorFlow</p>
          </div>
          <div class="link-card">
            <h3>Computer Vision</h3>
            <p>Facial landmark detection, morphometric analysis, automated QC on images</p>
            <p style="font-size: 0.9em; color: var(--text-secondary);">OpenCV · facial recognition · morphometry</p>
          </div>
        </div>
      </section>
      
      <!-- Projects Section - UPDATED with outcomes -->
      <section id="projects" class="section">
        <div class="section-title">
          <div class="section-number">03</div>
          <h2>Featured Research Projects</h2>
        </div>
        
        <div class="project">
          <h3>Gene Expression Signature of Human Brain Stimulation</h3>
          <img src="assets/images/brain-stim/overview.jpg" alt="Brain Stimulation Analysis">
          <p><strong>Key Findings:</strong> Identified cell-type-specific genes upregulated in response to electrical stimulation.</p>
          <ul>
            <li>Engineered end-to-end pipeline for single-nuclei multi-omics (RNA+ATAC) data with bootstrapped pseudo-bulk strategy</li>
            <li>Applied mixed-effects models for robust cell-type-specific detection</li>
            <li>Cross-species validation using RRHO identified conserved gene sets</li>
          </ul>
          <div class="callout-box light">
            <strong>Tools:</strong> R · Seurat · lmmSeq · RRHO2 · CellChat · edgeR · DCA
          </div>
        </div>
        
        <div class="project">
          <h3>Exceptional Ability: Multimodal Cognitive Study</h3>
          <img src="assets/images/te/overview-data.png" alt="Exceptional Ability Overview">
          <p><strong>Key Insight:</strong> Used a 10-minute language task that effectively captures cognitive performance as a digital biomarker, demonstrating potential for scalable assessment.</p>
          <ul>
            <li>Integrated NIH-Toolbox scores, custom language task, acoustic features, interview transcription, facial landmarks, and multi-modal MRI</li>
            <li>Applied WhisperAI for automated transcription and GPT embeddings for linguistic analysis</li>
            <li>Built reproducible QC and visualization pipelines</li>
          </ul>
          <div class="callout-box light">
            <strong>Tools:</strong> WhisperAI · GPT · lingmatch · ANTs · AFNI · FSL · computer vision
          </div>
        </div>
        
        <div class="project">
          <h3>Polygenic Drug Response Signatures</h3>
          <img src="assets/images/drug-response/overview.jpg" alt="Drug Response Analysis">
          <p><strong>Impact:</strong> Scaled analysis to 88,000+ participants (SPARK, ABCD) with validated predictions against behavioral phenotypes and neuroimaging biomarkers.</p>
          <ul>
            <li>Integrated GWAS, eQTL, and RNA-Seq to generate personalized treatment recommendations for psychiatric disorders (ADHD focus)</li>
            <li>Cross-validated polygenic scores against CBCL, BPM behavioral scales and fMRI data</li>
          </ul>
          <div class="callout-box light">
            <strong>Tools:</strong> GWAS · eQTL · TWAS · R
          </div>
        </div>
        
        <div class="project">
          <h3>Brain-Wide Drug Effects: Deep Learning Prediction</h3>
          <img src="assets/images/drug-maps/app-view.png" alt="Drug Effects Brain Map">
          <p><strong>Deliverable:</strong> Interactive R Shiny application mapping 838 compounds to predicted functional brain changes for phenotype discovery.</p>
          <ul>
            <li>Integrated brain-wide gene expression (Allen Institute), fMRI trait maps, and drug perturbation signatures (CMAP, LINCS)</li>
            <li>Built deep learning model for cross-dataset drug effect prediction</li>
            <li>Deployed interactive 3D brain visualizations linked to Neurosynth and Neuromaps phenotypes</li>
          </ul>
          <div class="callout-box light">
            <strong>Tools:</strong> Deep learning · R Shiny · 3D visualization
          </div>
        </div>
        
        <div class="project">
          <h3>Linguistic & Behavioral Patterns in Bipolar Disorder (Social Media)</h3>
          <img src="assets/images/bp-reddit/overview.jpg" alt="Bipolar Reddit Analysis">
          <p><strong>Discovery:</strong> Identified distinct behavioral signatures including disrupted sleep patterns, content topic shifts, and cyclical emotional patterns aligned with mood episodes.</p>
          <ul>
            <li>Analyzed 20 years of Reddit data identifying 2,847 self-disclosed bipolar users</li>
            <li>Extracted temporal posting patterns, sentiment, topic shifts, and GPT-4 embeddings for emotional volatility tracking</li>
            <li>Validated linguistic markers against reported mood episode timelines</li>
          </ul>
          <div class="callout-box light">
            <strong>Tools:</strong> Python · NLP · GPT-4 · time-series analysis · sentiment analysis · topic modeling
          </div>
        </div>
      </section>
      
      <!-- Talks Section - UPDATED with inline slide links -->
      <section id="talks" class="section">
        <div class="section-title">
          <div class="section-number">04</div>
          <h2>Selected Talks & Presentations</h2>
        </div>
        
        <div class="talk">
          <h3>Beyond Yes/No: Multimodal Autism Propensity Score from Genes to Brain
            <span class="talk-slides"><a href="assets/docs/talks/INSAR.ppsx">[View Slides →]</a></span>
          </h3>
          <p><strong>INSAR Conference 2025</strong> | Oral Presentation</p>
          <img src="assets/images/INSAR/overview.jpg" alt="INSAR Presentation Preview">
          <p>Presented novel deep learning framework integrating multi-modal neuroimaging (fALFF, structural morphometry, DTI) to generate continuous autism likelihood scores. Demonstrates potential of combining MRI modalities for improved autism neurophenotyping.</p>
          <div class="callout-box light">
            <strong>Topics:</strong> Deep Learning · Multi-modal MRI · fALFF · Structural MRI · DTI · Autism Biomarkers
          </div>
        </div>
        
        <div class="talk">
          <h3>Optimizing Structural MRI Processing Pipelines for 7T Data
            <span class="talk-slides"><a href="assets/docs/talks/INC.ppsx">[View Slides →]</a></span>
          </h3>
          <p><strong>Iowa Neuroimaging Consortium, University of Iowa</strong> | Invited Talk</p>
          <img src="assets/images/MRI-pipeline/overview.jpg" alt="MRI Pipeline Preview">
          <p>Comprehensive overview of 7T structural MRI processing pipelines, comparing tools for cortical reconstruction, subcortical segmentation, and surface-based analysis. Provided practical guidance on pipeline selection based on research objectives.</p>
          <div class="callout-box light">
            <strong>Topics:</strong> 7T MRI · Processing Pipelines · freesurfer · ANTs · FSL · Quality Control
          </div>
        </div>
      </section>
      
      <!-- Gallery Section - UPDATED with captions -->
      <section id="gallery" class="section">
        <div class="section-title">
          <div class="section-number">05</div>
          <h2>Visualization Gallery</h2>
        </div>
        
        <p>Click any visualization to view in full size. Gallery organized by research domain.</p>
        
        <div id="gallery-container" class="gallery-grid">
          <!-- Gallery populated by JavaScript -->
        </div>
        
        <div class="gallery-count" id="gallery-count">Loading...</div>
        
        <div class="gallery-controls">
          <button id="show-more-btn" class="gallery-btn">Show More</button>
          <button id="show-less-btn" class="gallery-btn" style="display: none;">Show Less</button>
        </div>
      </section>
      
      <!-- Media & Links Section - UPDATED and condensed -->
      <section id="links" class="section">
        <div class="section-title">
          <div class="section-number">06</div>
          <h2>Media, Publications & Links</h2>
        </div>
        
        <p>Learn more about my research, background, and lab environment:</p>
        
        <div class="links-grid">
          <div class="link-card">
            <h3>Personal Journey</h3>
            <p>My path into computational psychiatry and neurodiversity research</p>
            <a href="https://michaelson.lab.uiowa.edu/news/2025/02/ui-psychiatry-graduate-student-muhammad-elsadany-decodes-mental-health-data-and-his" class="link-button" target="_blank">Read Story</a>
          </div>
          <div class="link-card">
            <h3>Michaelson Lab</h3>
            <p>Research environment and team behind my PhD work</p>
            <a href="https://michaelson.lab.uiowa.edu/people" class="link-button" target="_blank">Visit Lab</a>
          </div>
          <div class="link-card">
            <h3>IGP in Genetics</h3>
            <p>Interdisciplinary genetics program at University of Iowa</p>
            <a href="https://genetics.grad.uiowa.edu" class="link-button" target="_blank">Program Info</a>
          </div>
          <div class="link-card">
            <h3>Research Features</h3>
            <p>News coverage of recent research</p>
            <a href="https://medicineiowa.org/fall-2024/closer-exceptional-processing" class="link-button" target="_blank">View Articles</a>
          </div>
          <div class="link-card">
            <h3>GitHub Repos</h3>
            <p>Open-source pipelines and analysis code</p>
            <a href="https://github.com/melsadany" class="link-button" target="_blank">View Code</a>
          </div>
          <div class="link-card">
            <h3>Connect on LinkedIn</h3>
            <p>Professional updates and networking</p>
            <a href="https://www.linkedin.com/in/melsadany/" class="link-button" target="_blank">Connect</a>
          </div>
        </div>
      </section>
      
    </div>
  </main>
</div>

<!-- Lightbox -->
<div id="lightbox" class="lightbox">
  <span class="close-lightbox" onclick="closeLightbox()">&times;</span>
  <div class="lightbox-nav">
    <button onclick="changeImage(-1)">&#10094;</button>
    <button onclick="changeImage(1)">&#10095;</button>
  </div>
  <img class="lightbox-content" id="lightbox-img">
</div>

<!-- Footer - NEW -->
<footer>
  <p>&copy; 2026 Muhammad Elsadany. Last updated: January 2026.</p>
</footer>

<script>
// Theme Toggle
const themeToggle = document.getElementById('themeToggle');
const prefersDarkScheme = window.matchMedia('(prefers-color-scheme: dark)');

let currentTheme = localStorage.getItem('theme') || (prefersDarkScheme.matches ? 'dark' : 'light');
document.documentElement.setAttribute('data-theme', currentTheme);
themeToggle.checked = currentTheme === 'dark';

themeToggle.addEventListener('change', function() {
  const newTheme = this.checked ? 'dark' : 'light';
  document.documentElement.setAttribute('data-theme', newTheme);
  localStorage.setItem('theme', newTheme);
});

// Navigation active link highlight
document.querySelectorAll('.nav-link').forEach(link => {
  link.addEventListener('click', function() {
    document.querySelectorAll('.nav-link').forEach(l => l.classList.remove('active'));
    this.classList.add('active');
    
    // Close sidebar on mobile when clicking a link
    if (window.innerWidth <= 992) {
      document.getElementById('sidebar').classList.add('hidden');
      document.getElementById('mobileOverlay').classList.remove('active');
    }
  });
});

// Hamburger menu toggle
const hamburgerBtn = document.getElementById('hamburgerBtn');
const sidebar = document.getElementById('sidebar');
const mobileOverlay = document.getElementById('mobileOverlay');

if (hamburgerBtn) {
  hamburgerBtn.addEventListener('click', function(e) {
    e.stopPropagation();
    sidebar.classList.toggle('hidden');
    mobileOverlay.classList.toggle('active');
  });
  
  mobileOverlay.addEventListener('click', function() {
    sidebar.classList.add('hidden');
    mobileOverlay.classList.remove('active');
  });
}

// Gallery functionality (keeping your existing gallery code)
// Gallery images array
const galleryImages = [
{ src: 'assets/gallery/arch-1.png', caption: 'Architecture Diagram' },
{ src: 'assets/gallery/dwi.jpg', caption: 'DTI Visualization' },
{ src: 'assets/gallery/nct-1.png', caption: 'Network Analysis' },
{ src: 'assets/gallery/rpoe-data.png', caption: 'RPOE Data' },
{ src: 'assets/gallery/iq-2.png', caption: 'IQ Distribution' },
{ src: 'assets/gallery/wc-1.png', caption: 'Word Cloud' },
{ src: 'assets/gallery/sche-1.png', caption: 'Schema Diagram' },
{ src: 'assets/gallery/thesis-overview-1.jpg', caption: 'Thesis Overview' },
{ src: 'assets/gallery/sche-2.png', caption: 'Processing Schema' },
{ src: 'assets/gallery/line-2.png', caption: 'Time Series' },
{ src: 'assets/gallery/resid-1.png', caption: 'Residual Analysis' },
{ src: 'assets/gallery/rad-1.svg', caption: 'Radial Plot' },
{ src: 'assets/gallery/ne-1.jpg', caption: 'Network Connectivity' },
{ src: 'assets/images/drug-maps/overview.jpg', caption: 'Drug Response Map' },
{ src: 'assets/images/te/overview-lang.jpg', caption: 'Language Analysis' },
{ src: 'assets/gallery/bar-1.png', caption: 'Bar Chart' },
{ src: 'assets/gallery/bm-v1.jpg', caption: 'Brain Map' },
{ src: 'assets/gallery/cyto-1.jpg', caption: 'Cell Type Analysis' },
{ src: 'assets/gallery/den-1.png', caption: 'Density Plot' },
{ src: 'assets/gallery/den-2.png', caption: 'Density Distribution' },
{ src: 'assets/gallery/den-3.jpg', caption: 'Density Heatmap' },
{ src: 'assets/gallery/euc-1.jpg', caption: 'Euclidean Distance' },
{ src: 'assets/gallery/fALFF-1.png', caption: 'fALFF Map' },
{ src: 'assets/gallery/forest-1.png', caption: 'Forest Plot' },
{ src: 'assets/gallery/dti-res-1.png', caption: 'DTI Results' },
{ src: 'assets/gallery/jeo-1.png', caption: 'Jeopardy Plot' },
{ src: 'assets/gallery/loli-1.png', caption: 'Lollipop Chart' },
{ src: 'assets/gallery/mo-1.png', caption: 'Morphometry' },
{ src: 'assets/gallery/mph-1.svg', caption: 'Morphological Analysis' },
{ src: 'assets/gallery/net-1.png', caption: 'Network 1' },
{ src: 'assets/gallery/net-2.png', caption: 'Network 2' },
{ src: 'assets/gallery/peaks-1.jpg', caption: 'Peak Detection' },
{ src: 'assets/gallery/scat-1.png', caption: 'Scatter Plot 1' },
{ src: 'assets/gallery/scat-2.png', caption: 'Scatter Plot 2' },
{ src: 'assets/gallery/scat-3.png', caption: 'Scatter Plot 3' },
{ src: 'assets/gallery/sel-1.jpg', caption: 'Selection Analysis' },
{ src: 'assets/gallery/sem-1.png', caption: 'SEM Path Diagram' },
{ src: 'assets/gallery/sem-2.jpg', caption: 'SEM Results' },
{ src: 'assets/gallery/st.png', caption: 'Statistical Summary' },
{ src: 'assets/gallery/time-1.gif', caption: 'Time Series Animation' },
{ src: 'assets/gallery/time-2.png', caption: 'Temporal Pattern' },
{ src: 'assets/gallery/umap-1.jpg', caption: 'UMAP Embedding' },
{ src: 'assets/gallery/upset-1.png', caption: 'UpSet Plot' },
{ src: 'assets/gallery/viol-1.png', caption: 'Violin Plot' }
];

let currentGalleryIndex = 0;
const itemsPerPage = 12;
let maxItemsShown = itemsPerPage;

// Populate gallery on page load
function populateGallery() {
const container = document.getElementById('gallery-container');
const itemsToShow = galleryImages.slice(0, maxItemsShown);

container.innerHTML = itemsToShow.map((img, index) => <div class="gallery-item" onclick="openLightbox(${index})"> <img src="${img.src}" alt="${img.caption}" onerror="this.style.display='none'"> <div class="gallery-caption">${img.caption}</div> </div> ).join('');

updateGalleryCount();
}

function updateGalleryCount() {
const count = document.getElementById('gallery-count');
count.textContent = Showing ${Math.min(maxItemsShown, galleryImages.length)} of ${galleryImages.length} visualizations;
}

// Lightbox functions
function openLightbox(index) {
currentGalleryIndex = index;
const lightbox = document.getElementById('lightbox');
const img = document.getElementById('lightbox-img');
const caption = document.getElementById('lightbox-caption');

img.src = galleryImages[index].src;
if (!caption) {
const captionDiv = document.createElement('div');
captionDiv.id = 'lightbox-caption';
captionDiv.style.cssText = 'color: white; text-align: center; margin-top: 10px; font-size: 0.9em;';
lightbox.appendChild(captionDiv);
}
document.getElementById('lightbox-caption').textContent = galleryImages[index].caption;

lightbox.style.display = 'block';
}

function closeLightbox() {
document.getElementById('lightbox').style.display = 'none';
}

function changeImage(direction) {
currentGalleryIndex = (currentGalleryIndex + direction + galleryImages.length) % galleryImages.length;
openLightbox(currentGalleryIndex);
}

// Show/Hide more images
document.addEventListener('DOMContentLoaded', function() {
const showMoreBtn = document.getElementById('show-more-btn');
const showLessBtn = document.getElementById('show-less-btn');

if (showMoreBtn) {
showMoreBtn.addEventListener('click', function() {
maxItemsShown += itemsPerPage;
if (maxItemsShown >= galleryImages.length) {
maxItemsShown = galleryImages.length;
showMoreBtn.style.display = 'none';
}
showLessBtn.style.display = 'inline-block';
populateGallery();
});
}

if (showLessBtn) {
showLessBtn.addEventListener('click', function() {
maxItemsShown = itemsPerPage;
showMoreBtn.style.display = 'inline-block';
showLessBtn.style.display = 'none';
populateGallery();
// Scroll to gallery section
document.getElementById('gallery').scrollIntoView({ behavior: 'smooth' });
});
}

// Populate gallery on load
populateGallery();
});

// Close lightbox when clicking outside the image
document.addEventListener('click', function(event) {
const lightbox = document.getElementById('lightbox');
if (event.target === lightbox) {
closeLightbox();
}
});

// Keyboard navigation for lightbox
document.addEventListener('keydown', function(event) {
const lightbox = document.getElementById('lightbox');
if (lightbox.style.display === 'block') {
if (event.key === 'ArrowLeft') changeImage(-1);
if (event.key === 'ArrowRight') changeImage(1);
if (event.key === 'Escape') closeLightbox();
}
});
