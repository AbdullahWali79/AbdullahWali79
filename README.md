<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Muhammad Abdullah - Professional Software Solutions" />
  <title>Muhammad Abdullah | Software House</title>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet" />

  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" />

  <!-- Font Awesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />

  <!-- AOS Animation Library -->
  <link href="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.css" rel="stylesheet" />

  <!-- Animate CSS -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css" />

  <style>
    :root {
      /* Updated Color Scheme */
      --primary: #2C3E50;
      --secondary: #3498DB;
      --accent: #E74C3C;
      --background: #FFFFFF;
      --text: #2C3E50;
      --card-bg: #FFFFFF;
      --header-bg: #2C3E50;
      --gradient-primary: linear-gradient(135deg, #2C3E50, #3498DB);
      --gradient-accent: linear-gradient(135deg, #E74C3C, #F39C12);
      --footer-bg: #2C3E50;
      --footer-text: #ECF0F1;
      --card-text: #2C3E50;
      --menu-text: #FFFFFF;
    }

    [data-theme="dark"] {
      --primary: #3498DB;
      --secondary: #2C3E50;
      --accent: #E74C3C;
      --background: #1A1A1A;
      --text: #ECF0F1;
      --card-bg: #2D2D2D;
      --header-bg: #1A1A1A;
      --gradient-primary: linear-gradient(135deg, #3498DB, #2C3E50);
      --gradient-accent: linear-gradient(135deg, #E74C3C, #F39C12);
      --footer-bg: #1A1A1A;
      --footer-text: #ECF0F1;
      --card-text: #ECF0F1;
      --menu-text: #FFFFFF;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background-color: var(--background);
      color: var(--text);
      scroll-behavior: smooth;
      transition: all 0.3s ease;
    }

    /* Glassmorphism Effect */
    .glass-effect {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.2);
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    /* Modern Card Design */
    .card {
      background: var(--card-bg);
      border: none;
      border-radius: 15px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      transition: all 0.3s ease;
      color: var(--card-text);
    }

    .card:hover {
      transform: translateY(-10px);
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
    }

    /* Gradient Text */
    .gradient-text {
      background: var(--gradient-primary);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    /* Modern Button Styles */
    .btn-modern {
      background: var(--gradient-primary);
      border: none;
      color: white;
      padding: 12px 24px;
      border-radius: 50px;
      transition: all 0.3s ease;
    }

    .btn-modern:hover {
      transform: translateY(-2px);
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }

    /* Header Styles */
    header {
      background: var(--header-bg);
      backdrop-filter: blur(10px);
      transition: all 0.3s ease;
    }

    .navbar-brand {
      font-weight: 700;
      font-size: 1.5rem;
    }

    .navbar-nav .nav-link {
      position: relative;
      padding: 0.5rem 1rem;
      font-weight: 500;
    }

    .navbar-nav .nav-link::after {
      content: '';
      position: absolute;
      width: 0;
      height: 2px;
      bottom: 0;
      left: 50%;
      background: var(--gradient-primary);
      transition: all 0.3s ease;
    }

    .navbar-nav .nav-link:hover::after {
      width: 100%;
      left: 0;
    }

    /* Hero Section */
    .hero-section {
      min-height: 60vh;
      padding: 2rem 0;
      background: var(--gradient-primary);
      position: relative;
      overflow: hidden;
    }

    .hero-section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><rect width="100" height="100" fill="none"/><circle cx="50" cy="50" r="40" fill="rgba(255,255,255,0.1)"/></svg>') center/cover;
      opacity: 0.1;
    }

    /* Progress Bar */
    .progress-container {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 4px;
      background: transparent;
      z-index: 1000;
    }

    .progress-bar {
      height: 4px;
      background: var(--gradient-primary);
      width: 0%;
      transition: width 0.1s ease;
    }

    /* Dark Mode Toggle */
    .theme-toggle {
      position: fixed;
      top: 20px;
      right: 20px;
      z-index: 1000;
      background: var(--gradient-primary);
      border: none;
      cursor: pointer;
      padding: 12px;
      border-radius: 50%;
      transition: all 0.3s ease;
    }

    .theme-toggle:hover {
      transform: scale(1.1);
    }

    .theme-toggle i {
      font-size: 20px;
      color: white;
    }

    /* Back to Top Button */
    .back-to-top {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: var(--gradient-primary);
      color: white;
      width: 50px;
      height: 50px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      opacity: 0;
      transition: all 0.3s ease;
      z-index: 1000;
    }

    .back-to-top.visible {
      opacity: 1;
    }

    .back-to-top:hover {
      transform: scale(1.1);
    }

    /* Responsive Design */
    @media (max-width: 768px) {
      .hero-section {
        min-height: 60vh;
      }
      
      .navbar-brand {
        font-size: 1.2rem;
      }
    }

    /* Accessibility */
    .focus-visible {
      outline: 2px solid var(--accent);
      outline-offset: 2px;
    }

    /* Loading Animation */
    .loading {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: var(--gradient-primary);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      z-index: 9999;
    }

    .loading-spinner {
      width: 50px;
      height: 50px;
      border: 3px solid rgba(255, 255, 255, 0.3);
      border-top: 3px solid white;
      border-radius: 50%;
      animation: spin 1s linear infinite;
      margin-bottom: 20px;
    }

    .welcome-text {
      font-size: 2.5rem;
      font-weight: 700;
      color: white;
      text-align: center;
      opacity: 0;
      animation: fadeInUp 1s ease forwards;
      text-shadow: 0 2px 10px rgba(255, 255, 255, 0.3);
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 2px;
    }

    .welcome-text span {
      display: inline-block;
      opacity: 0;
      transform: translateY(20px);
      animation: fadeInUp 0.5s ease forwards;
    }

    .ai-icon {
      font-size: 2rem;
      color: var(--accent);
      margin-left: 10px;
      opacity: 0;
      animation: pulse 2s infinite;
    }

    .ai-icon i {
      animation: float 3s ease-in-out infinite;
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.1); }
      100% { transform: scale(1); }
    }

    @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0px); }
    }

    /* Animation delays for each character - increased timing */
    .welcome-text span:nth-child(1) { animation-delay: 0.2s; }
    .welcome-text span:nth-child(2) { animation-delay: 0.4s; }
    .welcome-text span:nth-child(3) { animation-delay: 0.6s; }
    .welcome-text span:nth-child(4) { animation-delay: 0.8s; }
    .welcome-text span:nth-child(5) { animation-delay: 1.0s; }
    .welcome-text span:nth-child(6) { animation-delay: 1.2s; }
    .welcome-text span:nth-child(7) { animation-delay: 1.4s; }
    .welcome-text span:nth-child(8) { animation-delay: 1.6s; }
    .welcome-text span:nth-child(9) { animation-delay: 1.8s; }
    .welcome-text span:nth-child(10) { animation-delay: 2.0s; }
    .welcome-text span:nth-child(11) { animation-delay: 2.2s; }
    .welcome-text span:nth-child(12) { animation-delay: 2.4s; }
    .welcome-text span:nth-child(13) { animation-delay: 2.6s; }
    .welcome-text span:nth-child(14) { animation-delay: 2.8s; }
    .welcome-text span:nth-child(15) { animation-delay: 3.0s; }
    .welcome-text span:nth-child(16) { animation-delay: 3.2s; }
    .welcome-text span:nth-child(17) { animation-delay: 3.4s; }
    .welcome-text span:nth-child(18) { animation-delay: 3.6s; }
    .welcome-text span:nth-child(19) { animation-delay: 3.8s; }
    .welcome-text span:nth-child(20) { animation-delay: 4.0s; }
    .welcome-text span:nth-child(21) { animation-delay: 4.2s; }
    .welcome-text span:nth-child(22) { animation-delay: 4.4s; }
    .welcome-text span:nth-child(23) { animation-delay: 4.6s; }
    .welcome-text span:nth-child(24) { animation-delay: 4.8s; }
    .welcome-text span:nth-child(25) { animation-delay: 5.0s; }
    .welcome-text span:nth-child(26) { animation-delay: 5.2s; }
    .welcome-text span:nth-child(27) { animation-delay: 5.4s; }
    .welcome-text span:nth-child(28) { animation-delay: 5.6s; }
    .welcome-text span:nth-child(29) { animation-delay: 5.8s; }
    .welcome-text span:nth-child(30) { animation-delay: 6.0s; }
    .welcome-text span:nth-child(31) { animation-delay: 6.2s; }
    .welcome-text span:nth-child(32) { animation-delay: 6.4s; }
    .welcome-text span:nth-child(33) { animation-delay: 6.6s; }
    .welcome-text span:nth-child(34) { animation-delay: 6.8s; }
    .welcome-text span:nth-child(35) { animation-delay: 7.0s; }
    .welcome-text span:nth-child(36) { animation-delay: 7.2s; }
    .welcome-text span:nth-child(37) { animation-delay: 7.4s; }
    .welcome-text span:nth-child(38) { animation-delay: 7.6s; }
    .welcome-text span:nth-child(39) { animation-delay: 7.8s; }
    .welcome-text span:nth-child(40) { animation-delay: 8.0s; }

    @keyframes fadeInUp {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }

    /* Register Now Button */
    .register-now {
      position: fixed;
      right: 20px;
      bottom: 20px;
      background: var(--gradient-accent);
      color: white;
      padding: 12px 24px;
      border-radius: 50px;
      text-decoration: none;
      z-index: 1000;
      box-shadow: 0 4px 15px rgba(231, 76, 60, 0.3);
      transition: all 0.3s ease;
      font-weight: 600;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .register-now:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 20px rgba(231, 76, 60, 0.4);
      color: white;
    }

    .register-now i {
      font-size: 1.2rem;
    }

    /* Header Spacing */
    .hero-section {
      min-height: 60vh;
      padding: 2rem 0;
    }

    .navbar {
      padding: 0.5rem 0;
    }

    /* Footer Spacing */
    footer {
      padding: 2rem 0 1rem;
    }

    footer .container {
      padding: 0 1rem;
    }

    /* Text Colors */
    .text-white {
      color: var(--footer-text) !important;
    }

    .text-muted {
      color: rgba(236, 240, 241, 0.7) !important;
    }

    .navbar-dark .navbar-nav .nav-link {
      color: var(--footer-text);
    }

    .navbar-dark .navbar-nav .nav-link:hover {
      color: var(--accent);
    }

    /* Footer Background */
    footer {
      background-color: var(--header-bg);
    }

    /* Quick Links Hover */
    footer .list-unstyled a {
      transition: color 0.3s ease;
    }

    footer .list-unstyled a:hover {
      color: var(--accent) !important;
    }

    /* Card Text Colors */
    .card-title {
      color: var(--card-text);
    }

    .card p {
      color: var(--card-text);
    }

    /* Flip Card Colors */
    .flip-card-front {
      background-color: var(--card-bg);
      color: var(--card-text);
    }

    .flip-card-back {
      background-color: var(--accent);
      color: white;
    }

    /* Section Headings */
    .section-heading {
      color: var(--text);
    }

    /* Table Colors */
    .table {
      color: var(--text);
    }

    .table-striped > tbody > tr:nth-of-type(odd) {
      background-color: var(--card-bg);
    }

    .table-striped > tbody > tr:nth-of-type(even) {
      background-color: var(--background);
    }

    /* Navigation Styles */
    .navbar {
      background: var(--header-bg);
      padding: 0.5rem 0;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }

    .navbar-brand {
      color: var(--menu-text) !important;
      font-weight: 600;
      display: flex;
      align-items: center;
      transition: all 0.3s ease;
    }

    .navbar-brand:hover {
      transform: scale(1.05);
    }

    .navbar-brand img {
      transition: all 0.3s ease;
      border: 2px solid transparent;
    }

    .navbar-brand:hover img {
      transform: rotate(360deg);
      border-color: var(--accent);
      box-shadow: 0 0 15px rgba(231, 76, 60, 0.3);
    }

    .navbar-brand span {
      transition: all 0.3s ease;
      position: relative;
    }

    .navbar-brand:hover span {
      color: var(--accent) !important;
    }

    .navbar-brand span::after {
      content: '';
      position: absolute;
      width: 0;
      height: 2px;
      bottom: -2px;
      left: 0;
      background: var(--accent);
      transition: width 0.3s ease;
    }

    .navbar-brand:hover span::after {
      width: 100%;
    }

    .navbar-nav .nav-link {
      color: var(--menu-text) !important;
      position: relative;
      padding: 0.5rem 1rem;
      font-weight: 500;
      opacity: 0.9;
    }

    .navbar-nav .nav-link:hover {
      color: var(--accent) !important;
      opacity: 1;
    }

    .navbar-nav .nav-link::after {
      content: '';
      position: absolute;
      width: 0;
      height: 2px;
      bottom: 0;
      left: 50%;
      background: var(--accent);
      transition: all 0.3s ease;
    }

    .navbar-nav .nav-link:hover::after {
      width: 100%;
      left: 0;
    }

    .dropdown-menu {
      background: var(--card-bg);
      border: none;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    .dropdown-item {
      color: var(--text);
      font-weight: 500;
    }

    .dropdown-item:hover {
      background: var(--accent);
      color: white;
    }

    /* Toggler Icon Color */
    .navbar-toggler {
      border-color: var(--menu-text);
    }

    .navbar-toggler-icon {
      background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 30 30'%3e%3cpath stroke='rgba(255, 255, 255, 0.9)' stroke-linecap='round' stroke-miterlimit='10' stroke-width='2' d='M4 7h22M4 15h22M4 23h22'/%3e%3c/svg%3e");
    }

    /* Animated Wave Divider */
    .wave-divider {
      position: relative;
      height: 120px;
      overflow: hidden;
    }

    .wave-divider::before {
      content: '';
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      height: 120px;
      background: linear-gradient(135deg, var(--primary), var(--secondary));
      clip-path: polygon(
        0% 0%,
        100% 0%,
        100% 100%,
        0% 100%,
        0% 0%,
        0% 50%,
        10% 45%,
        20% 50%,
        30% 45%,
        40% 50%,
        50% 45%,
        60% 50%,
        70% 45%,
        80% 50%,
        90% 45%,
        100% 50%,
        100% 0%
      );
      animation: waveFloat 3s ease-in-out infinite;
    }

    .wave-divider.reverse::before {
      clip-path: polygon(
        0% 0%,
        100% 0%,
        100% 100%,
        0% 100%,
        0% 0%,
        0% 45%,
        10% 50%,
        20% 45%,
        30% 50%,
        40% 45%,
        50% 50%,
        60% 45%,
        70% 50%,
        80% 45%,
        90% 50%,
        100% 45%,
        100% 0%
      );
      animation: waveFloat 3s ease-in-out infinite reverse;
    }

    @keyframes waveFloat {
      0% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-10px);
      }
      100% {
        transform: translateY(0);
      }
    }

    /* Add subtle wave movement */
    .wave-divider::after {
      content: '';
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      height: 120px;
      background: linear-gradient(135deg, var(--primary), var(--secondary));
      opacity: 0.5;
      clip-path: polygon(
        0% 0%,
        100% 0%,
        100% 100%,
        0% 100%,
        0% 0%,
        0% 55%,
        10% 50%,
        20% 55%,
        30% 50%,
        40% 55%,
        50% 50%,
        60% 55%,
        70% 50%,
        80% 55%,
        90% 50%,
        100% 55%,
        100% 0%
      );
      animation: waveFloat 4s ease-in-out infinite;
    }

    .wave-divider.reverse::after {
      clip-path: polygon(
        0% 0%,
        100% 0%,
        100% 100%,
        0% 100%,
        0% 0%,
        0% 50%,
        10% 55%,
        20% 50%,
        30% 55%,
        40% 50%,
        50% 55%,
        60% 50%,
        70% 55%,
        80% 50%,
        90% 55%,
        100% 50%,
        100% 0%
      );
      animation: waveFloat 4s ease-in-out infinite reverse;
    }

    /* Training Courses Section */
    .course-card {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.2);
      border-radius: 20px;
      padding: 2.5rem;
      height: 100%;
      transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
      position: relative;
      overflow: hidden;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    }

    .course-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(
        135deg,
        rgba(255, 255, 255, 0.1) 0%,
        rgba(255, 255, 255, 0) 50%,
        rgba(255, 255, 255, 0.1) 100%
      );
      background-size: 200% 100%;
      opacity: 0;
      transition: opacity 0.4s ease;
    }

    .course-card:hover {
      transform: translateY(-15px) scale(1.02);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
    }

    .course-card:hover::before {
      opacity: 1;
      animation: shine 2s infinite;
    }

    .course-icon {
      font-size: 3rem;
      margin-bottom: 1.5rem;
      color: var(--accent);
      animation: float 3s ease-in-out infinite;
    }

    .course-title {
      font-size: 1.8rem;
      font-weight: 700;
      margin-bottom: 1.2rem;
      color: white;
      position: relative;
      display: inline-block;
    }

    .course-title::after {
      content: '';
      position: absolute;
      bottom: -5px;
      left: 0;
      width: 0;
      height: 2px;
      background: var(--accent);
      transition: width 0.3s ease;
    }

    .course-card:hover .course-title::after {
      width: 100%;
    }

    .course-description {
      color: rgba(255, 255, 255, 0.9);
      margin-bottom: 2rem;
      line-height: 1.6;
    }

    .course-features {
      list-style: none;
      padding: 0;
      margin: 0;
    }

    .course-features li {
      color: rgba(255, 255, 255, 0.8);
      margin-bottom: 0.8rem;
      display: flex;
      align-items: center;
      transition: transform 0.3s ease;
    }

    .course-features li:hover {
      transform: translateX(10px);
    }

    .course-features li i {
      color: var(--accent);
      margin-right: 0.8rem;
      font-size: 1.2rem;
      animation: pulse 2s infinite;
    }

    /* Section Background Colors */
    #about {
      background: linear-gradient(135deg, #2C3E50, #3498DB);
    }

    #services {
      background: linear-gradient(135deg, #3498DB, #2C3E50);
    }

    #projects {
      background: linear-gradient(135deg, #2C3E50, #E74C3C);
    }

    #students {
      background: linear-gradient(135deg, #E74C3C, #2C3E50);
    }

    #internships {
      background: linear-gradient(135deg, #2C3E50, #3498DB);
    }

    #contact {
      background: linear-gradient(135deg, #3498DB, #2C3E50);
    }

    /* Section Text Colors */
    section {
      color: white;
    }

    .section-heading {
      font-size: 2.5rem;
      font-weight: 700;
      margin-bottom: 3rem;
      text-align: center;
      color: white;
      position: relative;
      padding-bottom: 1rem;
    }

    .section-heading::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translateX(-50%);
      width: 100px;
      height: 3px;
      background: var(--accent);
      border-radius: 2px;
    }

    .card {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.2);
    }

    .card-title, .card p {
      color: white;
    }

    /* Enhanced Animations */
    @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0px); }
    }

    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.05); }
      100% { transform: scale(1); }
    }

    @keyframes shine {
      0% { background-position: -100% 0; }
      100% { background-position: 200% 0; }
    }

    /* Enhanced YouTube Videos Section */
    .videos-section {
      background: linear-gradient(135deg, var(--primary), var(--secondary));
      padding: 5rem 0;
      position: relative;
      overflow: hidden;
    }

    .videos-section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><rect width="100" height="100" fill="none"/><circle cx="50" cy="50" r="40" fill="rgba(255,255,255,0.1)"/></svg>') center/cover;
      opacity: 0.1;
    }

    .video-card {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      overflow: hidden;
      transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
      position: relative;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
      height: 100%;
    }

    .video-card:hover {
      transform: translateY(-15px) scale(1.02);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
    }

    .video-thumbnail {
      position: relative;
      overflow: hidden;
      padding-top: 56.25%; /* 16:9 Aspect Ratio */
    }

    .video-thumbnail img {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
    }

    .video-card:hover .video-thumbnail img {
      transform: scale(1.15);
    }

    .play-button {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%) scale(0.8);
      width: 70px;
      height: 70px;
      background: rgba(255, 0, 0, 0.9);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 28px;
      opacity: 0;
      transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
      box-shadow: 0 5px 15px rgba(255, 0, 0, 0.3);
    }

    .video-card:hover .play-button {
      opacity: 1;
      transform: translate(-50%, -50%) scale(1);
    }

    .video-info {
      padding: 1.8rem;
      color: white;
      position: relative;
      z-index: 1;
    }

    .video-title {
      font-size: 1.4rem;
      font-weight: 700;
      margin-bottom: 0.8rem;
      color: white;
      line-height: 1.4;
    }

    .video-description {
      font-size: 1rem;
      color: rgba(255, 255, 255, 0.9);
      margin-bottom: 1.2rem;
      line-height: 1.6;
    }

    .video-meta {
      display: flex;
      align-items: center;
      gap: 1.5rem;
      color: rgba(255, 255, 255, 0.7);
      font-size: 0.95rem;
    }

    .video-meta i {
      color: var(--accent);
      font-size: 1.1rem;
    }

    .subscribe-button {
      display: inline-flex;
      align-items: center;
      gap: 0.8rem;
      background: #FF0000;
      color: white;
      padding: 1rem 2rem;
      border-radius: 50px;
      text-decoration: none;
      font-weight: 600;
      font-size: 1.1rem;
      transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
      margin-top: 3rem;
      box-shadow: 0 5px 15px rgba(255, 0, 0, 0.2);
    }

    .subscribe-button:hover {
      transform: translateY(-5px);
      box-shadow: 0 8px 25px rgba(255, 0, 0, 0.3);
      color: white;
    }

    .subscribe-button i {
      font-size: 1.4rem;
    }

    .video-duration {
      position: absolute;
      bottom: 1rem;
      right: 1rem;
      background: rgba(0, 0, 0, 0.8);
      color: white;
      padding: 0.3rem 0.6rem;
      border-radius: 4px;
      font-size: 0.9rem;
    }

    /* Registration Form Styles */
    .registration-section {
      background: linear-gradient(135deg, var(--primary), var(--secondary));
      padding: 5rem 0;
      position: relative;
      overflow: hidden;
    }

    .registration-form {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      padding: 3rem;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    }

    .form-control {
      background: rgba(255, 255, 255, 0.1);
      border: 1px solid rgba(255, 255, 255, 0.2);
      color: white;
      padding: 1rem;
      border-radius: 10px;
      transition: all 0.3s ease;
    }

    .form-control:focus {
      background: rgba(255, 255, 255, 0.15);
      border-color: var(--accent);
      box-shadow: 0 0 0 0.2rem rgba(231, 76, 60, 0.25);
      color: white;
    }

    .form-control::placeholder {
      color: rgba(255, 255, 255, 0.6);
    }

    .form-label {
      color: white;
      font-weight: 500;
      margin-bottom: 0.5rem;
    }

    .submit-btn {
      background: var(--accent);
      color: white;
      padding: 1rem 2rem;
      border: none;
      border-radius: 50px;
      font-weight: 600;
      transition: all 0.3s ease;
      width: 100%;
      margin-top: 1rem;
    }

    .submit-btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 5px 15px rgba(231, 76, 60, 0.3);
    }

    .form-select {
      background: rgba(255, 255, 255, 0.1);
      border: 1px solid rgba(255, 255, 255, 0.2);
      color: white;
      padding: 1rem;
      border-radius: 10px;
      transition: all 0.3s ease;
    }

    .form-select:focus {
      background: rgba(255, 255, 255, 0.15);
      border-color: var(--accent);
      box-shadow: 0 0 0 0.2rem rgba(231, 76, 60, 0.25);
      color: white;
    }

    .form-select option {
      background: var(--primary);
      color: white;
    }

    /* Success Message Styles */
    .success-message {
      position: fixed;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      background: rgba(40, 167, 69, 0.9);
      color: white;
      padding: 1rem 2rem;
      border-radius: 50px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
      display: none;
      z-index: 9999;
      animation: slideUp 0.5s ease-out;
    }

    @keyframes slideUp {
      from {
        transform: translate(-50%, 100%);
        opacity: 0;
      }
      to {
        transform: translate(-50%, 0);
        opacity: 1;
      }
    }

    .error-message {
      background: rgba(220, 53, 69, 0.9);
    }

    /* YouTube Playlists Section Styles */
    .playlists-section {
      background: linear-gradient(135deg, var(--primary), var(--secondary));
      padding: 5rem 0;
      position: relative;
      overflow: hidden;
    }

    .playlist-card {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      overflow: hidden;
      transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
      position: relative;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
      height: 100%;
    }

    .playlist-card:hover {
      transform: translateY(-15px) scale(1.02);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
    }

    .playlist-thumbnail {
      position: relative;
      overflow: hidden;
      padding-top: 56.25%; /* 16:9 Aspect Ratio */
    }

    .playlist-thumbnail img {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
    }

    .playlist-card:hover .playlist-thumbnail img {
      transform: scale(1.15);
    }

    .playlist-overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.5);
      display: flex;
      align-items: center;
      justify-content: center;
      opacity: 0;
      transition: all 0.4s ease;
    }

    .playlist-card:hover .playlist-overlay {
      opacity: 1;
    }

    .playlist-overlay i {
      color: white;
      font-size: 3rem;
      transform: scale(0.8);
      transition: all 0.4s ease;
    }

    .playlist-card:hover .playlist-overlay i {
      transform: scale(1);
    }

    .playlist-info {
      padding: 1.8rem;
      color: white;
      position: relative;
      z-index: 1;
    }

    .playlist-title {
      font-size: 1.4rem;
      font-weight: 700;
      margin-bottom: 0.8rem;
      color: white;
      line-height: 1.4;
    }

    .playlist-description {
      font-size: 1rem;
      color: rgba(255, 255, 255, 0.9);
      margin-bottom: 1.2rem;
      line-height: 1.6;
    }

    .playlist-meta {
      display: flex;
      align-items: center;
      gap: 1.5rem;
      color: rgba(255, 255, 255, 0.7);
      font-size: 0.95rem;
    }

    .playlist-meta i {
      color: var(--accent);
      font-size: 1.1rem;
    }

    /* Profile Image Animation */
    .profile-image-container {
      position: relative;
      animation: float 6s ease-in-out infinite;
    }

    .profile-image-container::before {
      content: '';
      position: absolute;
      top: -10px;
      left: -10px;
      right: -10px;
      bottom: -10px;
      border: 2px solid rgba(255, 255, 255, 0.2);
      border-radius: 50%;
      animation: pulse 2s ease-in-out infinite;
    }

    .profile-image-container::after {
      content: '';
      position: absolute;
      top: -5px;
      left: -5px;
      right: -5px;
      bottom: -5px;
      border: 2px solid rgba(255, 255, 255, 0.1);
      border-radius: 50%;
      animation: pulse 2s ease-in-out infinite 0.5s;
    }

    .profile-image {
      width: 100%;
      height: auto;
      border-radius: 50%;
      border: 5px solid rgba(255, 255, 255, 0.2);
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
      transition: all 0.3s ease;
    }

    .profile-image:hover {
      transform: scale(1.05) rotate(5deg);
      border-color: rgba(255, 255, 255, 0.4);
    }

    @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-20px); }
      100% { transform: translateY(0px); }
    }

    @keyframes pulse {
      0% { transform: scale(1); opacity: 0.5; }
      50% { transform: scale(1.1); opacity: 0.2; }
      100% { transform: scale(1); opacity: 0.5; }
    }
  </style>
</head>
<body>
  <!-- Loading Screen -->
  <div class="loading" style="background: var(--gradient-primary);">
    <div class="loading-spinner"></div>
    <div class="text-center mb-4">
      <img src="https://i.postimg.cc/0jxPH0hq/logo.png" alt="Profile" class="img-fluid rounded-circle shadow-lg" style="max-width: 150px; border: 5px solid rgba(255,255,255,0.2);">
    </div>
    <div class="welcome-text">
      <span>W</span>
      <span>e</span>
      <span>l</span>
      <span>c</span>
      <span>o</span>
      <span>m</span>
      <span>e</span>
      <span> </span>
      <span>T</span>
      <span>o</span>
      <span> </span>
      <span>V</span>
      <span>i</span>
      <span>e</span>
      <span>w</span>
      <span> </span>
      <span>M</span>
      <span>y</span>
      <span> </span>
      <span>P</span>
      <span>o</span>
      <span>r</span>
      <span>t</span>
      <span>f</span>
      <span>o</span>
      <span>l</span>
      <span>i</span>
      <span>o</span>
    </div>
  </div>

  <!-- Progress Bar -->
  <div class="progress-container">
    <div class="progress-bar" id="progressBar"></div>
  </div>

  <!-- Dark Mode Toggle -->
  <button class="theme-toggle" id="themeToggle" aria-label="Toggle Dark Mode">
    <i class="fas fa-moon"></i>
  </button>

  <!-- Back to Top Button -->
  <div class="back-to-top" id="backToTop" aria-label="Back to Top">
    <i class="fas fa-arrow-up"></i>
  </div>

  <!-- Navigation -->
  <nav class="navbar navbar-expand-lg sticky-top">
    <div class="container">
      <a class="navbar-brand" href="#">
        <img src="https://i.postimg.cc/0jxPH0hq/logo.png" alt="logo" class="logo" width="50" height="50" style="border-radius: 50%;">
        <span class="ms-2">Muhammad Abdullah</span>
      </a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item">
            <a class="nav-link" href="#intro">Intro</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#projects">My Portfolio</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#contact">Contact Me</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Intro Section -->
  <section id="intro" class="py-5" style="background: var(--gradient-primary);">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6" data-aos="fade-right">
          <h1 class="display-4 text-white mb-4">I am Muhammad Abdullah</h1>
          <p class="lead text-white mb-4">A Lecturer at COMSATS University Vehari Campus with 12+ years of experience in AI-Driven SEO, No-Code App Development, and Automation.</p>
          <p class="text-white mb-4">I create and teach innovative solutions, such as:</p>
          <ul class="list-unstyled text-white">
            <li class="mb-3" data-aos="fade-up" data-aos-delay="100">
              <i class="fas fa-check-circle me-2"></i>AI-Enhanced SEO & GMB Management
            </li>
            <li class="mb-3" data-aos="fade-up" data-aos-delay="200">
              <i class="fas fa-check-circle me-2"></i>No-Code Flutter App Development (Windsurf, Cursor.ai)
            </li>
            <li class="mb-3" data-aos="fade-up" data-aos-delay="300">
              <i class="fas fa-check-circle me-2"></i>Google AppScripts & Knowledge Panel Creation
            </li>
            <li class="mb-3" data-aos="fade-up" data-aos-delay="400">
              <i class="fas fa-check-circle me-2"></i>AI Bots & Integrations (Botpress, Make.com, n8n)
            </li>
            <li class="mb-3" data-aos="fade-up" data-aos-delay="500">
              <i class="fas fa-check-circle me-2"></i>TradingView Pine Script Indicators
            </li>
            <li class="mb-3" data-aos="fade-up" data-aos-delay="600">
              <i class="fas fa-check-circle me-2"></i>YouTube Automation (AI-based content, thumbnails, etc.)
            </li>
          </ul>
          <p class="text-white mt-4" data-aos="fade-up" data-aos-delay="700">
            I combine practical experience with academic teaching to deliver top-tier results and empower businesses with AI Agents, AI-driven tools and strategies. Let's collaborate to take your project to the next level!
          </p>
        </div>
        <div class="col-lg-6" data-aos="fade-left">
          <div class="text-center">
            <div class="profile-image-container">
              <img src="https://i.postimg.cc/0jxPH0hq/logo.png" alt="Profile" class="profile-image">
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Projects Section -->
  <section id="projects" class="py-5">
    <div class="container">
      <h2 class="section-heading">My Portfolio List</h2>
      <div class="row g-4" data-aos="fade-up">
        <div class="col-md-4">
          <div class="card p-4 shadow">
            <i class="fas fa-laptop-code fa-2x mb-3 text-center text-info"></i>
            <h5 class="card-title text-center">Flutter Android App</h5>
            <p class="text-center">Built multiple mobile apps using Flutter for performance & UX.</p>
            <div class="text-center mt-3">
              <a href="https://github.com/AbdullahWali79" target="_blank" class="btn btn-sm btn-outline-primary">
                <i class="fab fa-github me-2"></i>View Projects
              </a>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card p-4 shadow">
            <i class="fas fa-cloud fa-2x mb-3 text-center text-warning"></i>
            <h5 class="card-title text-center">Google SEO</h5>
            <p class="text-center">Ranked websites using modern SEO strategies & backlinking.</p>
            <div class="text-center mt-3">
              <a href="http://appletaxisgatwick.co.uk/" target="_blank" class="btn btn-sm btn-outline-primary">
                <i class="fas fa-external-link-alt me-2"></i>View Website
              </a>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card p-4 shadow">
            <i class="fas fa-python fa-2x mb-3 text-center text-secondary"></i>
            <h5 class="card-title text-center">Python Flask Backend</h5>
            <p class="text-center">Built RESTful APIs for scalable and secure backend systems.</p>
            <div class="text-center mt-3">
              <a href="https://github.com/AbdullahWali79/100DaysofPython" target="_blank" class="btn btn-sm btn-outline-primary">
                <i class="fab fa-github me-2"></i>View Projects
              </a>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card p-4 shadow">
            <i class="fab fa-google fa-2x mb-3 text-center text-danger"></i>
            <h5 class="card-title text-center">Google My Business</h5>
            <p class="text-center">Optimized GMB profile for better local visibility and customer engagement.</p>
            <div class="text-center mt-3">
              <a href="https://g.co/kgs/uqhArQb" target="_blank" class="btn btn-sm btn-outline-primary">
                <i class="fas fa-external-link-alt me-2"></i>View Profile
              </a>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card p-4 shadow">
            <i class="fas fa-car fa-2x mb-3 text-center text-success"></i>
            <h5 class="card-title text-center">SpeeedyCars Website</h5>
            <p class="text-center">Developed a modern taxi booking website with AI integration for better user experience.</p>
            <div class="text-center mt-3">
              <a href="https://speeedycars.com/" target="_blank" class="btn btn-sm btn-outline-primary">
                <i class="fas fa-external-link-alt me-2"></i>Visit Website
              </a>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card p-4 shadow">
            <i class="fab fa-blogger-b fa-2x mb-3 text-center text-warning"></i>
            <h5 class="card-title text-center">We Connect Blog</h5>
            <p class="text-center">Created a professional training institute website using Blogger platform with modern design.</p>
            <div class="text-center mt-3">
              <a href="https://weconnectvehari.blogspot.com/" target="_blank" class="btn btn-sm btn-outline-primary">
                <i class="fas fa-external-link-alt me-2"></i>Visit Blog
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="py-5" id="contact">
    <div class="container">
      <div class="row g-4">
        <div class="col-lg-4">
          <h5 class="mb-4">Muhammad Abdullah</h5>
          <p class="text-muted">Professional Software Solutions & Training Institute</p>
          <div class="social-media-icons mt-4">
            <a href="https://www.youtube.com/@TechByAbdullah79" target="_blank" class="me-3">
              <i class="fab fa-youtube fa-lg text-danger"></i>
            </a>
            <a href="#" class="me-3">
              <i class="fab fa-facebook fa-lg text-primary"></i>
            </a>
            <a href="#" class="me-3">
              <i class="fab fa-twitter fa-lg text-info"></i>
            </a>
            <a href="#" class="me-3">
              <i class="fab fa-linkedin fa-lg text-primary"></i>
            </a>
          </div>
        </div>
        
        <div class="col-lg-4">
          <h5 class="mb-4">Quick Links</h5>
          <ul class="list-unstyled">
            <li class="mb-2">
              <a href="#intro" class="text-muted text-decoration-none">Intro</a>
            </li>
            <li class="mb-2">
              <a href="#projects" class="text-muted text-decoration-none">Portfolio</a>
            </li>
            <li class="mb-2">
              <a href="#contact" class="text-muted text-decoration-none">Contact Me</a>
            </li>
            <li class="mb-2">
              <a href="https://weconnectvehari.blogspot.com" target="_blank" class="text-muted text-decoration-none">
                <i class="fas fa-globe me-2"></i>We Connect Blog
              </a>
            </li>
          </ul>
        </div>
        
        <div class="col-lg-4">
          <h5 class="mb-4">Contact Info</h5>
          <p class="mb-2">
            <i class="fas fa-map-marker-alt me-2"></i>
            Sharki Colony East Main Road, Near Cookooz Cafe, Vehari
          </p>
          <p class="mb-2">
            <i class="fas fa-phone me-2"></i>
            <a href="https://wa.me/923046983794" class="text-muted text-decoration-none">+92 304 6983794</a>
          </p>
          <p class="mb-0">
            <i class="fas fa-envelope me-2"></i>
            <a href="mailto:abdullahwale@gmail.com" class="text-muted text-decoration-none">abdullahwale@gmail.com</a>
          </p>
        </div>
      </div>
      
      <hr class="my-4 border-secondary">
      
      <div class="row">
        <div class="col-md-6 text-center text-md-start">
          <p class="mb-0">&copy; 2024 Muhammad Abdullah. All Rights Reserved.</p>
        </div>
        <div class="col-md-6 text-center text-md-end">
          <p class="mb-0">
            <a href="https://www.youtube.com/@TechByAbdullah79" target="_blank" class="text-decoration-none">
              <i class="fab fa-youtube text-danger me-2"></i>
              Subscribe to TechbyAbdullah
            </a>
          </p>
        </div>
      </div>
    </div>
  </footer>

  <!-- Scripts -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.js"></script>
  <script>
    AOS.init();
  </script>

  <script>
    // Loading Screen with delayed hide
    window.addEventListener('load', () => {
      // Calculate total animation time (last character delay + animation duration + 2 seconds)
      const totalAnimationTime = 8.0 + 0.5 + 2.0;
      
      setTimeout(() => {
        document.querySelector('.loading').style.display = 'none';
      }, totalAnimationTime * 1000);
    });

    // Dark Mode Toggle
    const themeToggle = document.getElementById('themeToggle');
    const icon = themeToggle.querySelector('i');
    
    themeToggle.addEventListener('click', () => {
      document.body.setAttribute('data-theme', 
        document.body.getAttribute('data-theme') === 'dark' ? 'light' : 'dark'
      );
      icon.classList.toggle('fa-moon');
      icon.classList.toggle('fa-sun');
    });

    // Progress Bar
    window.addEventListener('scroll', () => {
      const winScroll = document.body.scrollTop || document.documentElement.scrollTop;
      const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
      const scrolled = (winScroll / height) * 100;
      document.getElementById('progressBar').style.width = scrolled + '%';
    });

    // Back to Top Button
    const backToTop = document.getElementById('backToTop');
    
    window.addEventListener('scroll', () => {
      if (window.pageYOffset > 300) {
        backToTop.classList.add('visible');
      } else {
        backToTop.classList.remove('visible');
      }
    });

    backToTop.addEventListener('click', () => {
      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      });
    });

    // Initialize AOS
    AOS.init({
      duration: 1000,
      once: true,
      offset: 100
    });

    // Accessibility
    document.addEventListener('keydown', (e) => {
      if (e.key === 'Tab') {
        document.body.classList.add('focus-visible');
      }
    });

    document.addEventListener('mousedown', () => {
      document.body.classList.remove('focus-visible');
    });

    // Smooth Scroll for Navigation Links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          target.scrollIntoView({
            behavior: 'smooth',
            block: 'start'
          });
        }
      });
    });
  </script>
</body>
</html>

