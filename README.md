html_content = '''<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Мебель Комплект — Комплектующие для мягкой мебели | Хасавюрт</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2c5530;
            --primary-light: #4a7c59;
            --accent: #c9a227;
            --accent-hover: #b8941f;
            --bg-cream: #faf8f3;
            --bg-light: #f5f0e8;
            --text-dark: #2d2d2d;
            --text-muted: #6b6b6b;
            --white: #ffffff;
            --shadow: 0 4px 20px rgba(0,0,0,0.08);
            --shadow-hover: 0 8px 30px rgba(0,0,0,0.12);
            --radius: 16px;
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
       
        * { margin: 0; padding: 0; box-sizing: border-box; }
       
        body {
            font-family: 'Montserrat', sans-serif;
            background: var(--bg-cream);
            color: var(--text-dark);
            line-height: 1.6;
        }
       
        /* Header */
        .header {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-light) 100%);
            color: var(--white);
            padding: 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: var(--shadow);
        }
       
        .header-top {
            background: rgba(0,0,0,0.15);
            padding: 8px 0;
            font-size: 13px;
        }
       
        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 24px;
        }
       
        .header-flex {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
       
        .header-contact {
            display: flex;
            gap: 24px;
            align-items: center;
        }
       
        .header-contact a {
            color: var(--white);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 6px;
            transition: var(--transition);
        }
       
        .header-contact a:hover {
            color: var(--accent);
        }
       
        .header-main {
            padding: 16px 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
       
        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
        }
       
        .logo-icon {
            width: 48px;
            height: 48px;
            background: var(--accent);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            color: var(--primary);
        }
       
        .logo-text h1 {
            font-size: 24px;
            font-weight: 700;
            letter-spacing: -0.5px;
        }
       
        .logo-text span {
            font-size: 12px;
            opacity: 0.9;
            font-weight: 300;
        }
       
        .nav {
            display: flex;
            gap: 32px;
        }
       
        .nav a {
            color: var(--white);
            text-decoration: none;
            font-weight: 500;
            font-size: 15px;
            position: relative;
            padding: 4px 0;
        }
       
        .nav a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: var(--transition);
        }
       
        .nav a:hover::after {
            width: 100%;
        }
       
        .cart-btn {
            background: var(--accent);
            color: var(--primary);
            border: none;
            padding: 12px 24px;
            border-radius: 50px;
            font-weight: 600;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: var(--transition);
            position: relative;
        }
       
        .cart-btn:hover {
            background: var(--accent-hover);
            transform: translateY(-2px);
        }
       
        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background: #e74c3c;
            color: white;
            width: 22px;
            height: 22px;
            border-radius: 50%;
            font-size: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
        }
       
        /* Hero */
        .hero {
            background: linear-gradient(135deg, var(--bg-light) 0%, #e8e0d0 100%);
            padding: 80px 0;
            position: relative;
            overflow: hidden;
        }
       
        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -10%;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(201,162,39,0.15) 0%, transparent 70%);
            border-radius: 50%;
        }
       
        .hero-content {
            max-width: 600px;
            position: relative;
            z-index: 1;
        }
       
        .hero h2 {
            font-size: 48px;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 20px;
            color: var(--primary);
        }
       
        .hero h2 span {
            color: var(--accent);
        }
       
        .hero p {
            font-size: 18px;
            color: var(--text-muted);
            margin-bottom: 32px;
            line-height: 1.7;
        }
       
        .hero-btns {
            display: flex;
            gap: 16px;
        }
       
        .btn-primary {
            background: var(--primary);
            color: var(--white);
            padding: 16px 32px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 16px;
        }
       
        .btn-primary:hover {
            background: var(--primary-light);
            transform: translateY(-2px);
            box-shadow: var(--shadow-hover);
        }
       
        .btn-secondary {
            background: transparent;
            color: var(--primary);
            padding: 16px 32px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: var(--transition);
            border: 2px solid var(--primary);
            cursor: pointer;
            font-size: 16px;
        }
       
        .btn-secondary:hover {
            background: var(--primary);
            color: var(--white);
        }
       
        /* Products */
        .products {
            padding: 80px 0;
        }
       
        .section-header {
            text-align: center;
            margin-bottom: 48px;
        }
       
        .section-header h2 {
            font-size: 36px;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 12px;
        }
       
        .section-header p {
            color: var(--text-muted);
            font-size: 16px;
        }
       
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 24px;
        }
       
        .product-card {
            background: var(--white);
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
        }
       
        .product-card:hover {
            transform: translateY(-8px);
            box-shadow: var(--shadow-hover);
        }
       
        .product-image {
            width: 100%;
            height: 240px;
            background: var(--bg-light);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }
       
        .product-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }
       
        .product-card:hover .product-image img {
            transform: scale(1.05);
        }
       
        .product-placeholder {
            color: var(--text-muted);
            font-size: 14px;
            text-align: center;
            padding: 20px;
        }
       
        .product-placeholder i {
            font-size: 48px;
            margin-bottom: 12px;
            display: block;
            color: var(--primary-light);
            opacity: 0.5;
        }
       
        .product-badge {
            position: absolute;
            top: 12px;
            left: 12px;
            background: var(--accent);
            color: var(--primary);
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
        }
       
        .product-info {
            padding: 20px;
        }
       
        .product-info h3 {
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 8px;
            color: var(--text-dark);
        }
       
        .product-info p {
            font-size: 14px;
            color: var(--text-muted);
            margin-bottom: 16px;
            line-height: 1.5;
        }
       
        .product-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
       
        .product-price {
            font-size: 22px;
            font-weight: 700;
            color: var(--primary);
        }
       
        .product-price .old-price {
            font-size: 14px;
            color: var(--text-muted);
            text-decoration: line-through;
            margin-left: 8px;
            font-weight: 400;
        }
       
        .add-to-cart {
            background: var(--primary);
            color: var(--white);
            border: none;
            width: 44px;
            height: 44px;
            border-radius: 12px;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
            font-size: 18px;
        }
       
        .add-to-cart:hover {
            background: var(--accent);
            color: var(--primary);
            transform: scale(1.1);
        }
       
        /* Features */
        .features {
            background: var(--white);
            padding: 60px 0;
        }
       
        .features-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 32px;
        }
       
        .feature {
            text-align: center;
            padding: 24px;
        }
       
        .feature-icon {
            width: 64px;
            height: 64px;
            background: var(--bg-light);
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 16px;
            font-size: 28px;
            color: var(--primary);
        }
       
        .feature h3 {
            font-size: 16px;
            font-weight: 600;
            margin-bottom: 8px;
        }
       
        .feature p {
            font-size: 14px;
            color: var(--text-muted);
        }
       
        /* Contact Section */
        .contact {
            padding: 80px 0;
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-light) 100%);
            color: var(--white);
        }
       
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 48px;
            align-items: center;
        }
       
        .contact-info h2 {
            font-size: 36px;
            margin-bottom: 24px;
        }
       
        .contact-info p {
            opacity: 0.9;
            margin-bottom: 32px;
            line-height: 1.7;
        }
       
        .contact-details {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
       
        .contact-item {
            display: flex;
            align-items: center;
            gap: 16px;
            background: rgba(255,255,255,0.1);
            padding: 16px 20px;
            border-radius: 12px;
            transition: var(--transition);
        }
       
        .contact-item:hover {
            background: rgba(255,255,255,0.15);
            transform: translateX(4px);
        }
       
        .contact-item i {
            width: 40px;
            height: 40px;
            background: var(--accent);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-size: 18px;
        }
       
        .contact-item div {
            flex: 1;
        }
       
        .contact-item .label {
            font-size: 12px;
            opacity: 0.7;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
       
        .contact-item .value {
            font-size: 16px;
            font-weight: 600;
        }
       
        .contact-item a {
            color: var(--white);
            text-decoration: none;
        }
       
        .contact-form {
            background: var(--white);
            padding: 40px;
            border-radius: var(--radius);
            color: var(--text-dark);
        }
       
        .contact-form h3 {
            font-size: 24px;
            margin-bottom: 24px;
            color: var(--primary);
        }
       
        .form-group {
            margin-bottom: 20px;
        }
       
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            font-size: 14px;
        }
       
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 14px 16px;
            border: 2px solid var(--bg-light);
            border-radius: 12px;
            font-family: inherit;
            font-size: 15px;
            transition: var(--transition);
        }
       
        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
        }
       
        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }
       
        /* Cart Modal */
        .modal-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
            z-index: 2000;
            backdrop-filter: blur(4px);
        }
       
        .modal-overlay.active {
            display: flex;
            align-items: center;
            justify-content: center;
        }
       
        .modal {
            background: var(--white);
            border-radius: var(--radius);
            width: 90%;
            max-width: 600px;
            max-height: 80vh;
            overflow-y: auto;
            padding: 32px;
            position: relative;
            animation: modalSlide 0.3s ease;
        }
       
        @keyframes modalSlide {
            from { transform: translateY(-20px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
       
        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 24px;
        }
       
        .modal-header h2 {
            font-size: 24px;
            color: var(--primary);
        }
       
        .modal-close {
            background: none;
            border: none;
            font-size: 24px;
            cursor: pointer;
            color: var(--text-muted);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }
       
        .modal-close:hover {
            background: var(--bg-light);
            color: var(--text-dark);
        }
       
        .cart-items {
            display: flex;
            flex-direction: column;
            gap: 16px;
        }
       
        .cart-item {
            display: flex;
            gap: 16px;
            padding: 16px;
            background: var(--bg-cream);
            border-radius: 12px;
            align-items: center;
        }
       
        .cart-item img {
            width: 80px;
            height: 80px;
            object-fit: cover;
            border-radius: 8px;
        }
       
        .cart-item-info {
            flex: 1;
        }
       
        .cart-item-info h4 {
            font-size: 16px;
            margin-bottom: 4px;
        }
       
        .cart-item-info .price {
            color: var(--primary);
            font-weight: 600;
        }
       
        .cart-item-remove {
            background: none;
            border: none;
            color: #e74c3c;
            cursor: pointer;
            font-size: 18px;
            width: 36px;
            height: 36px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }
       
        .cart-item-remove:hover {
            background: rgba(231, 76, 60, 0.1);
        }
       
        .cart-total {
            margin-top: 24px;
            padding-top: 24px;
            border-top: 2px solid var(--bg-light);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
       
        .cart-total span {
            font-size: 14px;
            color: var(--text-muted);
        }
       
        .cart-total .total-price {
            font-size: 24px;
            font-weight: 700;
            color: var(--primary);
        }
       
        .cart-empty {
            text-align: center;
            padding: 40px;
            color: var(--text-muted);
        }
       
        .cart-empty i {
            font-size: 64px;
            margin-bottom: 16px;
            display: block;
            color: var(--bg-light);
        }
       
        /* Footer */
        .footer {
            background: var(--text-dark);
            color: var(--white);
            padding: 48px 0 24px;
        }
       
        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 32px;
            margin-bottom: 32px;
        }
       
        .footer-brand h3 {
            font-size: 24px;
            margin-bottom: 16px;
        }
       
        .footer-brand p {
            opacity: 0.7;
            font-size: 14px;
            line-height: 1.7;
        }
       
        .footer-links h4 {
            font-size: 16px;
            margin-bottom: 16px;
            color: var(--accent);
        }
       
        .footer-links a {
            display: block;
            color: rgba(255,255,255,0.7);
            text-decoration: none;
            padding: 6px 0;
            font-size: 14px;
            transition: var(--transition);
        }
       
        .footer-links a:hover {
            color: var(--accent);
            padding-left: 4px;
        }
       
        .footer-bottom {
            border-top: 1px solid rgba(255,255,255,0.1);
            padding-top: 24px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 14px;
            opacity: 0.6;
        }
       
        /* Toast */
        .toast {
            position: fixed;
            bottom: 24px;
            right: 24px;
            background: var(--primary);
            color: var(--white);
            padding: 16px 24px;
            border-radius: 12px;
            box-shadow: var(--shadow-hover);
            display: flex;
            align-items: center;
            gap: 12px;
            transform: translateY(100px);
            opacity: 0;
            transition: var(--transition);
            z-index: 3000;
        }
       
        .toast.show {
            transform: translateY(0);
            opacity: 1;
        }
       
        /* Responsive */
        @media (max-width: 1024px) {
            .features-grid { grid-template-columns: repeat(2, 1fr); }
            .footer-grid { grid-template-columns: 1fr 1fr; }
        }
       
        @media (max-width: 768px) {
            .header-main { flex-wrap: wrap; gap: 16px; }
            .nav { display: none; }
            .hero h2 { font-size: 32px; }
            .hero-btns { flex-direction: column; }
            .contact-grid { grid-template-columns: 1fr; }
            .features-grid { grid-template-columns: 1fr; }
            .footer-grid { grid-template-columns: 1fr; }
            .products-grid { grid-template-columns: 1fr; }
        }
       
        /* Image upload hint */
        .upload-hint {
            position: absolute;
            bottom: 8px;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(0,0,0,0.7);
            color: white;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 11px;
            opacity: 0;
            transition: var(--transition);
        }
       
        .product-card:hover .upload-hint {
            opacity: 1;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="header-top">
            <div class="container header-flex">
                <div class="header-contact">
                    <a href="mailto:ваш-email@mail.ru"><i class="fas fa-envelope"></i> ваш-email@mail.ru</a>
                    <a href="tel:+79991234567"><i class="fas fa-phone"></i> +7 (999) 123-45-67</a>
                </div>
                <span><i class="fas fa-map-marker-alt"></i> г. Хасавюрт, Республика Дагестан</span>
            </div>
        </div>
        <div class="container header-main">
            <div class="logo">
                <div class="logo-icon"><i class="fas fa-couch"></i></div>
                <div class="logo-text">
                    <h1>Мебель Комплект</h1>
                    <span>Комплектующие для мягкой мебели</span>
                </div>
            </div>
            <nav class="nav">
                <a href="#products">Каталог</a>
                <a href="#features">Преимущества</a>
                <a href="#contact">Контакты</a>
            </nav>
            <button class="cart-btn" onclick="toggleCart()">
                <i class="fas fa-shopping-cart"></i>
                Корзина
                <span class="cart-count" id="cartCount">0</span>
            </button>
        </div>
    </header>

    <!-- Hero -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h2>Всё для мягкой мебели<br>в одном месте</h2>
                <p>Качественные комплектующие для производства и ремонта мягкой мебели. Пружинные блоки, поролоны, ткани, фурнитура и многое другое. Доставка по Хасавюрту и всему Дагестану.</p>
                <div class="hero-btns">
                    <a href="#products" class="btn-primary"><i class="fas fa-th-large"></i> Смотреть каталог</a>
                    <a href="#contact" class="btn-secondary"><i class="fas fa-phone"></i> Связаться</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Features -->
    <section class="features" id="features">
        <div class="container">
            <div class="features-grid">
                <div class="feature">
                    <div class="feature-icon"><i class="fas fa-check-circle"></i></div>
                    <h3>Качество гарантировано</h3>
                    <p>Только проверенные поставщики и сертифицированная продукция</p>
                </div>
                <div class="feature">
                    <div class="feature-icon"><i class="fas fa-truck"></i></div>
                    <h3>Быстрая доставка</h3>
                    <p>Доставка по Хасавюрту в день заказа, по регионам — от 1 дня</p>
                </div>
                <div class="feature">
                    <div class="feature-icon"><i class="fas fa-tags"></i></div>
                    <h3>Оптовые цены</h3>
                    <p>Специальные условия для мебельных производств и мастерских</p>
                </div>
                <div class="feature">
                    <div class="feature-icon"><i class="fas fa-headset"></i></div>
                    <h3>Персональный подход</h3>
                    <p>Поможем подобрать комплектующие под ваши задачи</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Products -->
    <section class="products" id="products">
        <div class="container">
            <div class="section-header">
                <h2>Каталог товаров</h2>
                <p>Замените фото и описание на свои — просто отредактируйте код или используйте CMS</p>
            </div>
            <div class="products-grid" id="productsGrid">
                <!-- Products will be inserted by JS -->
            </div>
        </div>
    </section>

    <!-- Contact -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="contact-grid">
                <div class="contact-info">
                    <h2>Свяжитесь с нами</h2>
                    <p>Остались вопросы? Напишите или позвоните — мы поможем подобрать нужные комплектующие, рассчитать количество материалов и оформить заказ.</p>
                    <div class="contact-details">
                        <div class="contact-item">
                            <i class="fas fa-envelope"></i>
                            <div>
                                <div class="label">Email</div>
                                <div class="value"><a href="mailto:ваш-email@mail.ru">ваш-email@mail.ru</a></div>
                            </div>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-phone"></i>
                            <div>
                                <div class="label">Телефон</div>
                                <div class="value"><a href="tel:+79991234567">+7 (999) 123-45-67</a></div>
                            </div>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-map-marker-alt"></i>
                            <div>
                                <div class="label">Адрес</div>
                                <div class="value">г. Хасавюрт, Республика Дагестан</div>
                            </div>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-clock"></i>
                            <div>
                                <div class="label">Режим работы</div>
                                <div class="value">Пн-Пт: 9:00 — 18:00, Сб: 10:00 — 15:00</div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <h3><i class="fas fa-paper-plane"></i> Отправить заявку</h3>
                    <form onsubmit="handleSubmit(event)">
                        <div class="form-group">
                            <label>Ваше имя</label>
                            <input type="text" placeholder="Иван Иванов" required>
                        </div>
                        <div class="form-group">
                            <label>Телефон</label>
                            <input type="tel" placeholder="+7 (999) 123-45-67" required>
                        </div>
                        <div class="form-group">
                            <label>Email</label>
                            <input type="email" placeholder="email@example.com">
                        </div>
                        <div class="form-group">
                            <label>Сообщение</label>
                            <textarea placeholder="Какие комплектующие вас интересуют?"></textarea>
                        </div>
                        <button type="submit" class="btn-primary" style="width: 100%;">
                            <i class="fas fa-send"></i> Отправить заявку
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-brand">
                    <h3><i class="fas fa-couch"></i> Мебель Комплект</h3>
                    <p>Комплектующие для мягкой мебели в Хасавюрте. Пружинные блоки, поролоны, ткани, фурнитура и многое другое для производства и ремонта мебели.</p>
                </div>
                <div class="footer-links">
                    <h4>Каталог</h4>
                    <a href="#">Пружинные блоки</a>
                    <a href="#">Поролоны</a>
                    <a href="#">Мебельные ткани</a>
                    <a href="#">Фурнитура</a>
                </div>
                <div class="footer-links">
                    <h4>Информация</h4>
                    <a href="#">О компании</a>
                    <a href="#">Доставка</a>
                    <a href="#">Оплата</a>
                    <a href="#">Возврат</a>
                </div>
                <div class="footer-links">
                    <h4>Контакты</h4>
                    <a href="tel:+79991234567">+7 (999) 123-45-67</a>
                    <a href="mailto:ваш-email@mail.ru">ваш-email@mail.ru</a>
                    <a href="#">г. Хасавюрт</a>
                </div>
            </div>
            <div class="footer-bottom">
                <span>© 2024 Мебель Комплект. Все права защищены.</span>
                <span>Работаем с любовью к мебели ❤️</span>
            </div>
        </div>
    </footer>

    <!-- Cart Modal -->
    <div class="modal-overlay" id="cartModal">
        <div class="modal">
            <div class="modal-header">
                <h2><i class="fas fa-shopping-cart"></i> Корзина</h2>
                <button class="modal-close" onclick="toggleCart()"><i class="fas fa-times"></i></button>
            </div>
            <div id="cartContent">
                <div class="cart-empty">
                    <i class="fas fa-shopping-basket"></i>
                    <p>Корзина пуста</p>
                    <p style="font-size: 14px; margin-top: 8px;">Добавьте товары из каталога</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Toast -->
    <div class="toast" id="toast">
        <i class="fas fa-check-circle"></i>
        <span id="toastMessage">Товар добавлен в корзину</span>
    </div>

    <script>
        // Product data - EDIT THESE
        const products = [
            {
                id: 1,
                name: "Клипсы мебельные обивочные",
                description: "Металлические клипсы для крепления обивочного материала к каркасу мягкой мебели. Упаковка 100 шт.",
                price: 350,
                oldPrice: 420,
                badge: "Хит",
                image: "1000105474.jpg"
            },
            {
                id: 2,
                name: "Пружинный блок Bonnel",
                description: "Классический пружинный блок для диванов и кресел. Размер 120×200 см, 120 пружин/м².",
                price: 2800,
                oldPrice: null,
                badge: "Новинка",
                image: null
            },
            {
                id: 3,
                name: "Поролон листовой ST 2540",
                description: "Поролон средней жесткости для сидений и спинок. Размер 100×200 см, толщина 40 мм.",
                price: 1200,
                oldPrice: 1450,
                badge: null,
                image: null
            },
            {
                id: 4,
                name: "Мебельная ткань Велюр",
                description: "Обивочная ткань велюр, ширина 140 см. Прочная, износостойкая, приятная на ощупь.",
                price: 890,
                oldPrice: null,
                badge: "Акция",
                image: null
            },
            {
                id: 5,
                name: "Ножки мебельные металлические",
                description: "Хромированные ножки для диванов и кресел. Высота 15 см, комплект 4 шт.",
                price: 650,
                oldPrice: 800,
                badge: null,
                image: null
            },
            {
                id: 6,
                name: "Клей мебельный ПВА-Д3",
                description: "Влагостойкий клей для склеивания поролона, дерева и ДВП. Объем 1 кг.",
                price: 450,
                oldPrice: null,
                badge: null,
                image: null
            },
            {
                id: 7,
                name: "Лента мебельная эластичная",
                description: "Резиновая лента для крепления пружинных блоков. Ширина 50 мм, рулон 50 м.",
                price: 380,
                oldPrice: null,
                badge: null,
                image: null
            },
            {
                id: 8,
                name: "ДВП мебельная 3 мм",
                description: "Древесно-волокнистая плита для обивки мягкой мебели. Размер 1220×2440 мм.",
                price: 550,
                oldPrice: null,
                badge: null,
                image: null
            },
            {
                id: 9,
                name: "Скобы мебельные 80/10",
                description: "Гальванизированные скобы для степлера. Подходят для крепления ткани и поролона.",
                price: 280,
                oldPrice: 350,
                badge: null,
                image: null
            },
            {
                id: 10,
                name: "Молния мебельная 60 см",
                description: "Разъемная молния для съемных чехлов диванов. Цвет ассорти.",
                price: 120,
                oldPrice: null,
                badge: null,
                image: null
            }
        ];

        let cart = [];

        // Render products
        function renderProducts() {
            const grid = document.getElementById('productsGrid');
            grid.innerHTML = products.map(product => `
                <div class="product-card">
                    <div class="product-image">
                        ${product.image ?
                            `<img src="${product.image}" alt="${product.name}">` :
                            `<div class="product-placeholder">
                                <i class="fas fa-image"></i>
                                <p>Добавьте фото товара<br><small>Замените в коде</small></p>
                            </div>`
                        }
                        ${product.badge ? `<span class="product-badge">${product.badge}</span>` : ''}
                        <span class="upload-hint">Замените фото в коде</span>
                    </div>
                    <div class="product-info">
                        <h3>${product.name}</h3>
                        <p>${product.description}</p>
                        <div class="product-footer">
                            <div class="product-price">
                                ${product.price} ₽
                                ${product.oldPrice ? `<span class="old-price">${product.oldPrice} ₽</span>` : ''}
                            </div>
                            <button class="add-to-cart" onclick="addToCart(${product.id})" title="В корзину">
                                <i class="fas fa-plus"></i>
                            </button>
                        </div>
                    </div>
                </div>
            `).join('');
        }

        // Cart functions
        function addToCart(productId) {
            const product = products.find(p => p.id === productId);
            const existing = cart.find(item => item.id === productId);
           
            if (existing) {
                existing.quantity++;
            } else {
                cart.push({ ...product, quantity: 1 });
            }
           
            updateCart();
            showToast(`${product.name} добавлен в корзину`);
        }

        function removeFromCart(productId) {
            cart = cart.filter(item => item.id !== productId);
            updateCart();
        }

        function updateCart() {
            const count = cart.reduce((sum, item) => sum + item.quantity, 0);
            document.getElementById('cartCount').textContent = count;
           
            const content = document.getElementById('cartContent');
            if (cart.length === 0) {
                content.innerHTML = `
                    <div class="cart-empty">
                        <i class="fas fa-shopping-basket"></i>
                        <p>Корзина пуста</p>
                        <p style="font-size: 14px; margin-top: 8px;">Добавьте товары из каталога</p>
                    </div>
                `;
            } else {
                const total = cart.reduce((sum, item) => sum + item.price * item.quantity, 0);
                content.innerHTML = `
                    <div class="cart-items">
                        ${cart.map(item => `
                            <div class="cart-item">
                                <div style="width:80px;height:80px;background:var(--bg-light);border-radius:8px;display:flex;align-items:center;justify-content:center;">
                                    <i class="fas fa-box" style="font-size:24px;color:var(--primary-light);opacity:0.5;"></i>
                                </div>
                                <div class="cart-item-info">
                                    <h4>${item.name}</h4>
                                    <p class="price">${item.price} ₽ × ${item.quantity} = ${item.price * item.quantity} ₽</p>
                                </div>
                                <button class="cart-item-remove" onclick="removeFromCart(${item.id})">
                                    <i class="fas fa-trash"></i>
                                </button>
                            </div>
                        `).join('')}
                    </div>
                    <div class="cart-total">
                        <span>Итого (${cart.reduce((s,i) => s+i.quantity, 0)} товаров)</span>
                        <span class="total-price">${total} ₽</span>
                    </div>
                    <button class="btn-primary" style="width:100%;margin-top:16px;" onclick="showToast('Функция оформления в разработке')">
                        <i class="fas fa-check"></i> Оформить заказ
                    </button>
                `;
            }
        }

        function toggleCart() {
            document.getElementById('cartModal').classList.toggle('active');
        }

        function showToast(message) {
            const toast = document.getElementById('toast');
            document.getElementById('toastMessage').textContent = message;
            toast.classList.add('show');
            setTimeout(() => toast.classList.remove('show'), 3000);
        }

        function handleSubmit(e) {
            e.preventDefault();
            showToast('Заявка отправлена! Мы свяжемся с вами.');
            e.target.reset();
        }

        // Close modal on overlay click
        document.getElementById('cartModal').addEventListener('click', function(e) {
            if (e.target === this) toggleCart();
        });

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Initialize
        renderProducts();
    </script>
</body>
</html>'''

# Save the file
with open('/mnt/agents/output/index.html', 'w', encoding='utf-8') as f:
    f.write(html_content)

print("✅ Сайт создан и сохранен!")
print(f"Размер файла: {len(html_content)} символов")

