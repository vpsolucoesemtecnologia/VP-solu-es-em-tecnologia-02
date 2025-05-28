<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Catálogo Interativo de Funcionalidades</title>
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Ccircle cx='16' cy='16' r='16' fill='%232563eb'/%3E%3Cpath d='M16 6a7 7 0 0 0-3.5 13.1V22a1.5 1.5 0 0 0 3 0v-2.9A7 7 0 0 0 16 6zm0 12a5 5 0 1 1 0-10 5 5 0 0 1 0 10z' fill='%23fff'/%3E%3C/svg%3E">
  <style>
    :root {
      --primary-blue: #2563eb;
      --light-blue: #dbeafe;
      --dark-blue: #1e40af;
      --accent-blue: #60a5fa;
      --white: #ffffff;
      --gray-50: #f8fafc;
      --gray-100: #f1f5f9;
      --gray-200: #e2e8f0;
      --gray-300: #cbd5e1;
      --gray-600: #475569;
      --gray-700: #334155;
      --shadow-sm: 0 1px 2px 0 rgb(0 0 0 / 0.05);
      --shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
      --shadow-lg: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
      --shadow-xl: 0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(135deg, var(--light-blue) 0%, var(--gray-50) 100%);
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      line-height: 1.6;
      color: var(--gray-700);
      min-height: 100vh;
    }

    .header {
      background: linear-gradient(135deg, var(--primary-blue) 0%, var(--dark-blue) 100%);
      color: var(--white);
      padding: 2rem 0;
      box-shadow: var(--shadow-lg);
      position: relative;
      overflow: hidden;
    }

    .header::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: url('data:image/svg+xml,<svg width="60" height="60" viewBox="0 0 60 60" xmlns="http://www.w3.org/2000/svg"><g fill="none" fill-rule="evenodd"><g fill="rgba(255,255,255,0.03)" fill-opacity="0.4"><circle cx="36" cy="24" r="3"/><circle cx="12" cy="36" r="2"/><circle cx="48" cy="48" r="1.5"/></g></svg>') repeat;
    }

    .header-content {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 2rem;
      position: relative;
      z-index: 1;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 1rem;
    }

    .header-logo {
      font-size: 2.5rem;
      color: var(--white);
      animation: glow 2s ease-in-out infinite alternate;
    }

    .header h1 {
      font-size: 2.5rem;
      font-weight: 700;
      margin-bottom: 0.5rem;
      text-align: center;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .header p {
      font-size: 1.2rem;
      text-align: center;
      opacity: 0.9;
    }

    .nav-bar {
      background: var(--white);
      box-shadow: var(--shadow-md);
      padding: 1rem 0;
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .nav-content {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 2rem;
      display: flex;
      justify-content: center;
      gap: 2rem;
      flex-wrap: wrap;
    }

    .nav-link {
      color: var(--gray-700);
      text-decoration: none;
      font-weight: 600;
      padding: 0.5rem 1rem;
      border-radius: 8px;
      transition: all 0.3s ease;
      position: relative;
    }

    .nav-link:hover {
      color: var(--primary-blue);
      background: var(--light-blue);
    }

    .nav-link::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 50%;
      width: 0;
      height: 2px;
      background: var(--primary-blue);
      transition: all 0.3s ease;
      transform: translateX(-50%);
    }

    .nav-link:hover::after {
      width: 80%;
    }

    @media (max-width: 768px) {
      .nav-content {
        gap: 1rem;
        padding: 0 1rem;
      }

      .nav-link {
        font-size: 0.9rem;
        padding: 0.4rem 0.8rem;
      }
    }

    .container {
      display: grid;
      grid-template-columns: 1fr 350px;
      gap: 2rem;
      max-width: 1200px;
      margin: 2rem auto;
      padding: 0 1rem;
    }

    .features {
      background: var(--white);
      padding: 2rem;
      border-radius: 16px;
      box-shadow: var(--shadow-lg);
      border: 1px solid var(--gray-200);
    }

    .features-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 1.5rem;
      position: relative;
    }

    .feature-column {
      background: var(--gray-50);
      padding: 1.5rem;
      border-radius: 12px;
      border: 1px solid var(--gray-200);
    }

    .sidebar {
      background: var(--white);
      padding: 2rem;
      border-radius: 16px;
      box-shadow: var(--shadow-lg);
      border: 1px solid var(--gray-200);
      position: sticky;
      top: 2rem;
      height: fit-content;
      align-self: start;
    }

    .features-header {
      background: var(--white);
      padding: 2rem;
      border-radius: 16px;
      box-shadow: var(--shadow-lg);
      border: 1px solid var(--gray-200);
      margin-bottom: 2rem;
    }

    .features-content {
      display: flex;
      gap: 2rem;
    }

    .user-selection {
      background: var(--gray-50);
      padding: 1.5rem;
      border-radius: 12px;
      border: 2px solid var(--light-blue);
      margin-bottom: 2rem;
    }

    .user-selection label {
      display: block;
      font-weight: 600;
      color: var(--dark-blue);
      margin-bottom: 0.5rem;
      font-size: 1.1rem;
    }

    .user-selection select {
      width: 100%;
      padding: 0.75rem;
      border: 2px solid var(--gray-200);
      border-radius: 8px;
      font-size: 1rem;
      background: var(--white);
      transition: all 0.3s ease;
    }

    .user-selection select:focus {
      outline: none;
      border-color: var(--primary-blue);
      box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.1);
    }

    .feature-item {
      display: flex;
      align-items: center;
      margin-bottom: 1rem;
      padding: 0.75rem;
      border-radius: 8px;
      transition: all 0.3s ease;
      cursor: pointer;
      position: relative;
    }

    .feature-item:hover {
      background: var(--white);
      transform: translateY(-2px);
      box-shadow: var(--shadow-md);
    }

    .feature-item input[type="checkbox"] {
      appearance: none;
      width: 20px;
      height: 20px;
      border: 2px solid var(--gray-300);
      border-radius: 4px;
      margin-right: 1rem;
      position: relative;
      transition: all 0.3s ease;
      cursor: pointer;
    }

    .feature-item input[type="checkbox"]:checked {
      background: var(--primary-blue);
      border-color: var(--primary-blue);
    }

    .feature-item input[type="checkbox"]:checked::after {
      content: '✓';
      position: absolute;
      color: var(--white);
      font-size: 14px;
      font-weight: bold;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }

    .feature-item label {
      flex: 1;
      font-weight: 500;
      color: var(--gray-700);
      cursor: pointer;
      user-select: none;
    }

    .feature-item:hover label {
      color: var(--dark-blue);
    }

    .plan-card {
      background: linear-gradient(135deg, var(--primary-blue) 0%, var(--dark-blue) 100%);
      color: var(--white);
      padding: 1.5rem;
      border-radius: 12px;
      text-align: center;
      margin-bottom: 1.5rem;
      box-shadow: var(--shadow-md);
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
    }

    .plan-card h3 {
      font-size: 1.5rem;
      margin-bottom: 0.25rem;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.5rem;
    }

    .plan-card h3 i {
      font-size: 1.8rem;
      transition: all 0.3s ease;
    }

    .plan-card .price {
      font-size: 2.5rem;
      font-weight: 700;
      margin: 0.5rem 0;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.25rem;
    }

    .plan-card .price::before {
      content: 'R$';
      font-size: 1.5rem;
      font-weight: 600;
      opacity: 0.9;
    }

    .plan-card .price-label {
      opacity: 0.9;
      font-size: 0.9rem;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.25rem;
    }

    .plan-card .price-label i {
      font-size: 0.8rem;
    }

    .selected-list {
      margin-top: 1.5rem;
      background: var(--white);
      border-radius: 12px;
      padding: 1rem;
      border: 1px solid var(--gray-200);
    }

    .selected-list h3 {
      color: var(--dark-blue);
      margin-bottom: 1rem;
      font-size: 1.2rem;
      font-weight: 600;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .selected-list ul {
      list-style: none;
      max-height: 300px;
      overflow-y: auto;
      padding: 0.5rem;
    }

    .selected-list li {
      background: var(--light-blue);
      margin-bottom: 0.5rem;
      padding: 0.75rem;
      border-radius: 8px;
      font-size: 0.9rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-left: 4px solid var(--primary-blue);
    }

    .selected-list li .feature-price {
      background: var(--primary-blue);
      color: var(--white);
      padding: 0.25rem 0.5rem;
      border-radius: 4px;
      font-size: 0.85rem;
      font-weight: 600;
    }

    .selected-list li .plan-base {
      font-weight: 600;
      color: var(--primary-blue);
      border-bottom: 2px solid var(--light-blue);
      padding-bottom: 0.5rem;
      margin-bottom: 0.5rem;
      display: block;
      width: 100%;
    }

    .empty-state {
      text-align: center;
      padding: 2rem;
      color: var(--gray-600);
    }

    .empty-state i {
      font-size: 2.5rem;
      color: var(--gray-300);
      margin-bottom: 1rem;
    }

    .feature-counter {
      background: var(--primary-blue);
      color: var(--white);
      padding: 0.5rem 1rem;
      border-radius: 20px;
      font-size: 0.9rem;
      font-weight: 600;
      display: inline-block;
      margin-bottom: 1rem;
    }

    .footer {
      background: linear-gradient(135deg, var(--primary-blue) 0%, var(--dark-blue) 100%);
      color: var(--white);
      padding: 2rem 0;
      box-shadow: var(--shadow-lg);
      position: relative;
      overflow: hidden;
      margin-top: 2rem;
    }

    .footer::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: url('data:image/svg+xml,<svg width="60" height="60" viewBox="0 0 60 60" xmlns="http://www.w3.org/2000/svg"><g fill="none" fill-rule="evenodd"><g fill="rgba(255,255,255,0.03)" fill-opacity="0.4"><circle cx="36" cy="24" r="3"/><circle cx="12" cy="36" r="2"/><circle cx="48" cy="48" r="1.5"/></g></svg>') repeat;
    }

    .footer-content {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 2rem;
      position: relative;
      z-index: 1;
      text-align: center;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
    }

    .footer-section {
      text-align: left;
    }

    .footer-section h3 {
      font-size: 1.2rem;
      margin-bottom: 1rem;
      color: var(--white);
    }

    .footer-section p, .footer-section a {
      color: var(--white);
      opacity: 0.9;
      text-decoration: none;
      display: block;
      margin-bottom: 0.5rem;
      transition: opacity 0.3s ease;
    }

    .footer-section a:hover {
      opacity: 1;
    }

    .copyright-bar {
      background: var(--dark-blue);
      color: var(--white);
      padding: 1rem 0;
      text-align: center;
      font-size: 0.95rem;
      border-top: 1px solid rgba(255, 255, 255, 0.1);
    }

    .copyright-bar p {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 2rem;
    }

    .copyright-bar i {
      margin-right: 0.5rem;
      font-size: 0.9rem;
    }

    .social-links {
      display: flex;
      gap: 1rem;
      margin-top: 1rem;
    }

    .social-links a {
      font-size: 1.5rem;
    }

    @media (max-width: 1200px) {
      .container {
        grid-template-columns: 1fr;
      }

      .sidebar {
        position: static;
        margin-top: 2rem;
      }
    }

    @media (max-width: 768px) {
      .container {
        padding: 0 1rem;
      }

      .features, .sidebar {
        padding: 1.5rem;
      }

      .features {
        flex: 1 1 100%;
      }

      .sidebar {
        flex: 1 1 100%;
        position: static;
      }

      .features-grid {
        grid-template-columns: 1fr;
      }

      .header h1 {
        font-size: 2rem;
      }
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .features, .sidebar {
      animation: fadeInUp 0.6s ease-out;
    }

    .feature-item {
      animation: fadeInUp 0.4s ease-out;
      animation-fill-mode: both;
    }

    .feature-item:nth-child(1) { animation-delay: 0.1s; }
    .feature-item:nth-child(2) { animation-delay: 0.15s; }
    .feature-item:nth-child(3) { animation-delay: 0.2s; }
    .feature-item:nth-child(4) { animation-delay: 0.25s; }
    .feature-item:nth-child(5) { animation-delay: 0.3s; }

    .sidebar h2 {
      text-align: center;
      color: var(--dark-blue);
      margin-bottom: 1.5rem;
      font-size: 1.8rem;
      font-weight: 700;
    }

    .newsletter-section {
      background: var(--white);
      padding: 1.5rem;
      border-radius: 12px;
      margin-top: 1.5rem;
      border: 1px solid var(--gray-200);
    }

    .newsletter-section h3 {
      color: var(--dark-blue);
      font-size: 1.2rem;
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .newsletter-section h3 i {
      color: var(--primary-blue);
    }

    .newsletter-section p {
      color: var(--gray-600);
      font-size: 0.9rem;
      margin-bottom: 1rem;
    }

    .newsletter-form {
      display: flex;
      gap: 0.5rem;
      flex-direction: column;
    }

    .newsletter-form input {
      width: 100%;
      padding: 0.75rem;
      border: 1px solid var(--gray-200);
      border-radius: 8px;
      font-size: 0.9rem;
      transition: all 0.3s ease;
    }

    .newsletter-form input:focus {
      outline: none;
      border-color: var(--primary-blue);
      box-shadow: 0 0 0 2px rgba(37, 99, 235, 0.1);
    }

    .newsletter-form button {
      width: 100%;
      padding: 0.75rem;
      background: var(--primary-blue);
      color: var(--white);
      border: none;
      border-radius: 8px;
      font-weight: 600;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.5rem;
      transition: all 0.3s ease;
      font-size: 0.95rem;
    }

    .newsletter-form button:hover {
      background: var(--dark-blue);
      transform: translateY(-1px);
    }

    .newsletter-form button i {
      font-size: 1rem;
    }

    @media (max-width: 768px) {
      .newsletter-form {
        flex-direction: column;
      }
    }

    .whatsapp-contact-btn {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.8rem;
      width: 100%;
      padding: 1rem;
      background: #25D366;
      color: var(--white);
      border: none;
      border-radius: 8px;
      font-size: 1rem;
      font-weight: 600;
      cursor: pointer;
      text-decoration: none;
      margin-top: 1.5rem;
    }

    .whatsapp-contact-btn:hover {
      background: #128C7E;
    }

    .whatsapp-contact-btn i {
      font-size: 1.4rem;
    }

    .whatsapp-contact-btn .btn-text {
      display: flex;
      flex-direction: column;
      align-items: center;
      line-height: 1.2;
    }

    .whatsapp-contact-btn .btn-text span {
      font-size: 1.1rem;
    }

    .whatsapp-contact-btn .btn-text small {
      font-size: 0.8rem;
      opacity: 0.9;
    }

    .whatsapp-btn {
      display: block;
      width: 100%;
      padding: 1rem;
      background: #25D366;
      color: var(--white);
      border: none;
      border-radius: 8px;
      font-size: 1rem;
      font-weight: 600;
      cursor: pointer;
      margin-top: 1.5rem;
    }

    .whatsapp-btn:hover {
      background: #128C7E;
    }

    .whatsapp-btn i {
      font-size: 1.2rem;
      margin-right: 0.5rem;
    }

    .selected-list ul {
      list-style: none;
      padding: 0;
      margin: 0;
    }

    .selected-list li {
      background: var(--light-blue);
      margin-bottom: 0.5rem;
      padding: 0.75rem;
      border-radius: 8px;
      font-size: 0.9rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-left: 4px solid var(--primary-blue);
      transition: all 0.3s ease;
    }

    .selected-list li:hover {
      transform: translateX(5px);
      background: var(--white);
    }

    .selected-list li.plan-base {
      background: var(--primary-blue);
      color: var(--white);
      font-weight: 600;
      border-left: 4px solid var(--dark-blue);
    }

    .selected-list li.feature-item-selected {
      background: var(--light-blue);
      animation: fadeIn 0.3s ease-in-out;
    }

    .selected-list li.total-price {
      background: var(--dark-blue);
      color: var(--white);
      font-weight: 600;
      margin-top: 1rem;
      border-left: 4px solid var(--primary-blue);
    }

    .selected-list .feature-price {
      background: var(--primary-blue);
      color: var(--white);
      padding: 0.25rem 0.5rem;
      border-radius: 4px;
      font-size: 0.85rem;
      font-weight: 600;
    }

    .selected-list li.total-price .feature-price {
      background: var(--white);
      color: var(--dark-blue);
    }

    .feature-counter {
      background: var(--primary-blue);
      color: var(--white);
      padding: 0.5rem 1rem;
      border-radius: 20px;
      font-size: 0.9rem;
      font-weight: 600;
      display: inline-block;
      margin-bottom: 1rem;
      animation: fadeIn 0.3s ease-in-out;
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: translateY(-10px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .selected-list {
      background: var(--white);
      border-radius: 12px;
      padding: 1rem;
      border: 1px solid var(--gray-200);
      min-height: 100px;
    }

    .selected-list ul {
      list-style: none;
      padding: 0;
      margin: 0;
    }

    .selected-list li {
      background: var(--light-blue);
      margin-bottom: 0.5rem;
      padding: 0.75rem;
      border-radius: 8px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-left: 4px solid var(--primary-blue);
    }

    .selected-list li.total-price {
      background: var(--dark-blue);
      color: var(--white);
      font-weight: 600;
      margin-top: 1rem;
    }

    .selected-list .feature-price {
      background: var(--primary-blue);
      color: var(--white);
      padding: 0.25rem 0.5rem;
      border-radius: 4px;
      font-weight: 600;
    }

    .selected-list li.total-price .feature-price {
      background: var(--white);
      color: var(--dark-blue);
    }

    .empty-state {
      text-align: center;
      padding: 1rem;
      color: var(--gray-600);
    }

    .empty-state i {
      font-size: 2rem;
      color: var(--gray-300);
      margin-bottom: 0.5rem;
    }

    .empty-state p {
      font-size: 0.9rem;
      color: var(--gray-600);
    }
  </style>
</head>
<body>
  <div class="header">
    <div class="header-content">
      <div>
        <h1><i class="fas fa-lightbulb header-logo"></i> VP Soluções em Tecnologia</h1>
        <p>Selecione as funcionalidades que sua empresa precisa e monte o plano perfeito</p>
      </div>
    </div>
  </div>

  <nav class="nav-bar">
    <div class="nav-content">
      <a href="sistema-gestao.html" class="nav-link">
        <i class="fas fa-chart-line"></i> Sistema de Gestão
      </a>
      <a href="pdv.html" class="nav-link">
        <i class="fas fa-cash-register"></i> PDV Completo
      </a>
      <a href="ecommerce.html" class="nav-link">
        <i class="fas fa-shopping-cart"></i> E-commerce
      </a>
      <a href="fiscal.html" class="nav-link">
        <i class="fas fa-file-invoice"></i> Gestão Fiscal
      </a>
      <a href="financeiro.html" class="nav-link">
        <i class="fas fa-money-bill-wave"></i> Financeiro
      </a>
      <a href="integracoes.html" class="nav-link">
        <i class="fas fa-plug"></i> Integrações
      </a>
    </div>
  </nav>

  <div class="container">
    <div class="features">
      <div class="user-selection">
        <label for="numUsers"><i class="fas fa-users"></i> Número de Usuários:</label>
        <select id="numUsers" onchange="atualizarPreco()">
          <option value="0">1 Usuário - Essencial (R$ 100)</option>
          <option value="1">3 Usuários - Standard (R$ 140)</option>
          <option value="2">Usuários Ilimitados - Premium (R$ 220)</option>
        </select>
      </div>

      <div class="features-grid">
        <div class="feature-column">
          <h3 style="color: var(--dark-blue); margin-bottom: 1rem; font-weight: 600;"><i class="fas fa-chart-line"></i> Gestão e Vendas</h3>
          <div class="feature-item">
            <input type="checkbox" value="Dashboard" id="dashboard">
            <label for="dashboard">Dashboard</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Boleto/Remessa" id="boleto">
            <label for="boleto">Boleto/Remessa</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Orçamento" id="orcamento">
            <label for="orcamento">Orçamento</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Pedido de Venda" id="pedido">
            <label for="pedido">Pedido de Venda</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="NFe, NFCe" id="nfe">
            <label for="nfe">NFe, NFCe</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="MFe" id="mfe">
            <label for="mfe">MFe</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Minhas Notas" id="notas">
            <label for="notas">Minhas Notas</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Portal do Contador" id="contador">
            <label for="contador">Portal do Contador</label>
          </div>
        </div>

        <div class="feature-column">
          <h3 style="color: var(--dark-blue); margin-bottom: 1rem; font-weight: 600;"><i class="fas fa-money-check-alt"></i> Financeiro</h3>
          <div class="feature-item">
            <input type="checkbox" value="Aplicativo para NFCe" id="app-nfce">
            <label for="app-nfce">Aplicativo para NFCe</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Fluxo de Caixa" id="fluxo">
            <label for="fluxo">Fluxo de Caixa</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Contas a Receber" id="receber">
            <label for="receber">Contas a Receber</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Contas a Pagar" id="pagar">
            <label for="pagar">Contas a Pagar</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Importação de XML" id="xml">
            <label for="xml">Importação de XML</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Fator de Conversão" id="conversao">
            <label for="conversao">Fator de Conversão</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Ordem de Compra" id="compra">
            <label for="compra">Ordem de Compra</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Preço Atacado e Varejo" id="preco">
            <label for="preco">Preço Atacado e Varejo</label>
          </div>
        </div>

        <div class="feature-column">
          <h3 style="color: var(--dark-blue); margin-bottom: 1rem; font-weight: 600;"><i class="fas fa-cogs"></i> Operacionais</h3>
          <div class="feature-item">
            <input type="checkbox" value="Conversão CFOP" id="cfop">
            <label for="cfop">Conversão CFOP</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Ordem de Serviço" id="servico">
            <label for="servico">Ordem de Serviço</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Integração Mercado Livre" id="mercadolivre">
            <label for="mercadolivre">Integração Mercado Livre</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="WhatsApp" id="whatsapp">
            <label for="whatsapp">WhatsApp</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Pré Venda Gerencial" id="prevenda">
            <label for="prevenda">Pré Venda Gerencial</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Tela PDV Frente de Caixa" id="pdv">
            <label for="pdv">Tela PDV Frente de Caixa</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Replicação de Dados" id="replicacao">
            <label for="replicacao">Replicação de Dados</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Parametrização de Tributos" id="tributos">
            <label for="tributos">Parametrização de Tributos</label>
          </div>
        </div>

        <div class="feature-column">
          <h3 style="color: var(--dark-blue); margin-bottom: 1rem; font-weight: 600;"><i class="fas fa-store"></i> E-commerce & Vendas</h3>
          <div class="feature-item">
            <input type="checkbox" value="Ecommerce" id="ecommerce">
            <label for="ecommerce">Ecommerce</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Tabelas de Preço" id="tabelas">
            <label for="tabelas">Tabelas de Preço</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="ZPOS" id="zpos">
            <label for="zpos">ZPOS</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Cadastros Gerais" id="cadastros">
            <label for="cadastros">Cadastros Gerais</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Cadastro de Kits" id="kits">
            <label for="kits">Cadastro de Kits</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Fiscal - Perfil de Tributação" id="fiscal">
            <label for="fiscal">Fiscal - Perfil de Tributação</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Suporte a Certificado A3" id="certificado">
            <label for="certificado">Suporte a Certificado A3</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Tabela de Preço por Cliente" id="preco-cliente">
            <label for="preco-cliente">Tabela de Preço por Cliente</label>
          </div>
        </div>

        <div class="feature-column">
          <h3 style="color: var(--dark-blue); margin-bottom: 1rem; font-weight: 600;"><i class="fas fa-tags"></i> Avançados</h3>
          <div class="feature-item">
            <input type="checkbox" value="Etiquetas Personalizadas" id="etiquetas">
            <label for="etiquetas">Etiquetas Personalizadas</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Tabelas de Preço por Produto" id="preco-produto">
            <label for="preco-produto">Tabelas de Preço por Produto</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Cadastro de Grades" id="grades">
            <label for="grades">Cadastro de Grades</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Retaguarda Offline" id="offline">
            <label for="offline">Retaguarda Offline</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Plano de Contas" id="plano-contas">
            <label for="plano-contas">Plano de Contas</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="DRE Simplificado" id="dre">
            <label for="dre">DRE Simplificado</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="PIX Dinâmico: Banco Sicoob" id="pix">
            <label for="pix">PIX Dinâmico: Banco Sicoob</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Envio Automático para Contador" id="envio-contador">
            <label for="envio-contador">Envio Automático para Contador</label>
          </div>
        </div>

        <div class="feature-column">
          <h3 style="color: var(--dark-blue); margin-bottom: 1rem; font-weight: 600;"><i class="fas fa-university"></i> Integração Bancária</h3>
          <div class="feature-item">
            <input type="checkbox" value="Boleto API: Banco Sicoob" id="boleto-sicoob">
            <label for="boleto-sicoob">Boleto API: Banco Sicoob</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Boleto API: Banco Inter" id="boleto-inter">
            <label for="boleto-inter">Boleto API: Banco Inter</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Boleto API: Banco Santander" id="boleto-santander">
            <label for="boleto-santander">Boleto API: Banco Santander</label>
          </div>
          <div class="feature-item">
            <input type="checkbox" value="Boleto API: Sicredi" id="boleto-sicredi">
            <label for="boleto-sicredi">Boleto API: Sicredi</label>
          </div>
        </div>
      </div>
    </div>

    <div class="sidebar">
      <h2><i class="fas fa-chart-pie"></i> Seu Plano</h2>
      <div class="plan-card">
        <h3>
          <i id="planIcon" class="fas fa-users"></i>
          <span id="planName">Selecione um Plano</span>
        </h3>
        <div class="plan-description" id="planDescription">Escolha o número de usuários acima</div>
        <div class="price">
          <span id="planPrice">0,00</span>
        </div>
        <div class="price-label">
          <i class="fas fa-calendar-alt"></i>
          por mês
        </div>
      </div>

      <div class="selected-list">
        <h3><i class="fas fa-check-circle"></i> Funcionalidades Selecionadas</h3>
        <div id="selectedList">
          <div class="empty-state">
            <i class="fas fa-shopping-cart"></i>
            <p>Selecione funcionalidades para ver aqui</p>
          </div>
        </div>
      </div>

      <div class="newsletter-section">
        <h3>
          <i class="fas fa-bell"></i>
          Receba Novidades
        </h3>
        <p>Cadastre-se para receber atualizações sobre novos recursos e promoções exclusivas.</p>
        <form class="newsletter-form" onsubmit="return false;">
          <input type="email" placeholder="Seu melhor e-mail" required>
          <button type="submit">
            <i class="fas fa-paper-plane"></i>
            Cadastrar
          </button>
        </form>
      </div>

      <a href="https://api.whatsapp.com/send?phone=8496115650" target="_blank" class="whatsapp-contact-btn">
        <i class="fab fa-whatsapp"></i>
        <div class="btn-text">
          <span>Fale Conosco</span>
          <small>Suporte via WhatsApp</small>
        </div>
      </a>

      <button id="whatsappBtn" class="whatsapp-btn" style="display:none;">
        <i class="fab fa-whatsapp"></i>
        Solicitar no WhatsApp
      </button>
    </div>
  </div>

  <footer class="footer">
    <div class="footer-content">
      <div class="footer-section">
        <h3>Contato</h3>
        <p><i class="fas fa-phone"></i> Suporte: (84) 9611-5650</p>
        <p><i class="fas fa-envelope"></i> contato@vpsolucoes.com.br</p>
        <p><i class="fas fa-map-marker-alt"></i> Natal, RN</p>
      </div>
      
      <div class="footer-section">
        <h3>Redes Sociais</h3>
        <div class="social-links">
          <a href="https://www.instagram.com/vpsolucoesemtecnologia/" target="_blank"><i class="fab fa-instagram"></i></a>
          <a href="https://www.tiktok.com/@vpsolucoesemtecno" target="_blank"><i class="fab fa-tiktok"></i></a>
          <a href="https://www.facebook.com/profile.php?id=61576840889104" target="_blank"><i class="fab fa-facebook"></i></a>
          <a href="https://www.youtube.com/@VP-Solu%C3%A7%C3%B5esemTecnologia" target="_blank"><i class="fab fa-youtube"></i></a>
        </div>
      </div>

      <div class="footer-section">
        <h3>Horário de Funcionamento</h3>
        <p>Segunda a Sexta: 8h às 22h</p>
        <p>Sábado: 9h às 18h</p>
      </div>
    </div>
  </footer>

  <div class="copyright-bar">
    <p>
      <i class="fas fa-copyright"></i> 2025 VP Soluções em Tecnologia. Todos os direitos reservados.
    </p>
  </div>

  <script>
    const planNames = ['Essencial', 'Standard', 'Premium'];
    const planPrices = [100, 140, 220];
    let selectedFeatures = new Set(); // Armazena as funcionalidades selecionadas

    const inputs = document.querySelectorAll('.features input[type=checkbox]');
    const numUsers = document.getElementById('numUsers');
    const planNameCell = document.getElementById('planName');
    const planPriceCell = document.getElementById('planPrice');
    const selectedList = document.getElementById('selectedList');
    const whatsappBtn = document.getElementById('whatsappBtn');
    const planIcon = document.getElementById('planIcon');

    // Variável global para armazenar os itens selecionados
    let selectedItems = new Set();
    let selectedItemsList = [];

    function atualizarPreco() {
      const select = document.getElementById('numUsers');
      const selectedValue = select.value;
      const planName = document.getElementById('planName');
      const planDescription = document.getElementById('planDescription');
      const planPrice = document.getElementById('planPrice');
      const planIcon = document.getElementById('planIcon');
      
      planName.textContent = planNames[selectedValue];
      planDescription.textContent = select.options[selectedValue].text;
      planPrice.textContent = planPrices[selectedValue].toFixed(2);
      
      if (selectedValue === '0') {
        planIcon.className = 'fas fa-user';
        planIcon.style.color = '#60a5fa';
      } else {
        planIcon.className = 'fas fa-users';
        planIcon.style.color = '#60a5fa';
      }
      
      update();
    }

    function update() {
      const checkboxes = document.querySelectorAll('.feature-item input[type="checkbox"]:checked');
      const selectedListDiv = document.querySelector('.sidebar .selected-list');
      const selectedListContent = selectedListDiv.querySelector('#selectedList');
      
      // Limpa as variáveis de armazenamento
      selectedItems.clear();
      selectedItemsList = [];

      // Se houver itens selecionados
      if (checkboxes.length > 0) {
        checkboxes.forEach(checkbox => {
          const featureItem = checkbox.closest('.feature-item');
          const label = featureItem.querySelector('label');
          const featureName = label ? label.textContent : checkbox.value;
          
          // Armazena o item selecionado
          selectedItems.add(featureName);
          selectedItemsList.push(featureName);
        });

        // Atualiza o conteúdo da div de Funcionalidades Selecionadas
        selectedListContent.innerHTML = `
          <ul>
            ${selectedItemsList.map(item => `
              <li>
                <div class="selected-feature">
                  <i class="fas fa-check-circle"></i>
                  <span>${item}</span>
                </div>
              </li>
            `).join('')}
          </ul>
        `;
        whatsappBtn.style.display = 'block';
      } else {
        selectedListContent.innerHTML = `
          <div class="empty-state">
            <i class="fas fa-shopping-cart"></i>
            <p>Selecione funcionalidades para ver aqui</p>
          </div>
        `;
        whatsappBtn.style.display = 'none';
      }
    }

    function enviarParaWhatsApp() {
      const selectedPlan = parseInt(numUsers.value);
      const planName = planNames[selectedPlan];
      const planPrice = planPrices[selectedPlan];
      
      // Monta a mensagem para o WhatsApp
      let mensagem = `Olá! Gostaria de solicitar um orçamento para o seguinte plano:\n\n`;
      mensagem += `*Plano:* ${planName}\n`;
      mensagem += `*Valor Base:* R$ ${planPrice.toFixed(2)}\n\n`;
      
      if (selectedItemsList.length > 0) {
        mensagem += `*Funcionalidades Selecionadas:*\n`;
        selectedItemsList.forEach(item => {
          mensagem += `- ${item}\n`;
        });
        mensagem += `\n*Total de Funcionalidades:* ${selectedItemsList.length}`;
      } else {
        mensagem += `*Nenhuma funcionalidade selecionada*`;
      }
      
      // Codifica a mensagem para URL
      const mensagemCodificada = encodeURIComponent(mensagem);
      
      // Abre o WhatsApp com a mensagem
      window.open(`https://api.whatsapp.com/send?phone=8496115650&text=${mensagemCodificada}`, '_blank');
    }

    // Adiciona os event listeners quando a página carregar
    document.addEventListener('DOMContentLoaded', () => {
      // Adiciona listener para cada checkbox
      document.querySelectorAll('.feature-item input[type="checkbox"]').forEach(checkbox => {
        checkbox.addEventListener('change', () => {
          update(); // Atualiza a lista e armazena os itens
        });
      });

      // Adiciona listener para mudança de plano
      document.getElementById('numUsers').addEventListener('change', () => {
        // Não limpa mais as seleções ao mudar o plano
        atualizarPreco();
      });

      // Adiciona listener para o botão do WhatsApp
      whatsappBtn.addEventListener('click', enviarParaWhatsApp);

      // Inicializa a lista
      update();
    });

    // Estilos para a lista de selecionados
    const style = document.createElement('style');
    style.textContent = `
      .sidebar .selected-list {
        background: var(--white);
        border-radius: 12px;
        padding: 1rem;
        border: 1px solid var(--gray-200);
        margin-top: 1.5rem;
      }

      .sidebar .selected-list h3 {
        color: var(--dark-blue);
        margin-bottom: 1rem;
        font-size: 1.2rem;
        font-weight: 600;
        display: flex;
        align-items: center;
        gap: 0.5rem;
      }

      .sidebar .selected-list ul {
        list-style: none;
        padding: 0;
        margin: 0;
      }

      .sidebar .selected-list li {
        background: var(--light-blue);
        margin-bottom: 0.5rem;
        padding: 0.75rem;
        border-radius: 8px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-left: 4px solid var(--primary-blue);
      }

      .sidebar .selected-feature {
        display: flex;
        align-items: center;
        gap: 0.5rem;
        width: 100%;
      }

      .sidebar .selected-feature i {
        color: var(--primary-blue);
        font-size: 1rem;
      }

      .sidebar .empty-state {
        text-align: center;
        padding: 1rem;
        color: var(--gray-600);
      }

      .sidebar .empty-state i {
        font-size: 2rem;
        color: var(--gray-300);
        margin-bottom: 0.5rem;
      }

      .sidebar .empty-state p {
        font-size: 0.9rem;
        color: var(--gray-600);
      }
    `;
    document.head.appendChild(style);
  </script>
</body>
</html>
