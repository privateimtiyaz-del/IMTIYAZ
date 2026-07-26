<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>IMTIYAZ - Bimbel Quran & Akademik</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }

        :root {
            --primary: #0f5c5c;
            --primary-dark: #0a4545;
            --accent: #e6b422;
            --accent-dark: #c49a1a;
            --bg-light: #fef9f0;
            --text: #1e2a3a;
            --text-light: #5a6e7c;
            --white: #ffffff;
            --shadow: 0 8px 24px rgba(0, 0, 0, 0.08);
            --shadow-sm: 0 4px 12px rgba(0, 0, 0, 0.06);
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Inter', sans-serif;
            color: var(--text);
            background: var(--bg-light);
            line-height: 1.5;
            max-width: 480px;
            margin: 0 auto;
            overflow-x: hidden;
            padding-bottom: 72px; /* space for bottom nav */
        }

        h1, h2, h3, h4 {
            font-family: 'Plus Jakarta Sans', sans-serif;
            font-weight: 700;
        }

        /* ===== TOP NAV ===== */
        nav {
            position: fixed;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100%;
            max-width: 480px;
            background: rgba(255, 255, 255, 0.97);
            backdrop-filter: blur(12px);
            z-index: 100;
            padding: 0.9rem 1.2rem;
            border-bottom: 1px solid rgba(0, 0, 0, 0.07);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--primary);
            text-decoration: none;
            font-family: 'Plus Jakarta Sans', sans-serif;
        }

        .logo span {
            color: var(--accent);
        }

        .nav-daftar {
            background: var(--primary);
            color: white !important;
            padding: 0.45rem 1rem;
            border-radius: 100px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.85rem;
        }

        /* ===== BOTTOM NAV ===== */
        .bottom-nav {
            position: fixed;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100%;
            max-width: 480px;
            background: white;
            border-top: 1px solid rgba(0,0,0,0.08);
            display: flex;
            justify-content: space-around;
            align-items: center;
            padding: 0.6rem 0 0.8rem;
            z-index: 100;
            box-shadow: 0 -4px 16px rgba(0,0,0,0.06);
        }

        .bottom-nav a {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 0.25rem;
            text-decoration: none;
            color: var(--text-light);
            font-size: 0.6rem;
            font-weight: 500;
            transition: color 0.2s;
            flex: 1;
        }

        .bottom-nav a i {
            font-size: 1.1rem;
        }

        .bottom-nav a.active,
        .bottom-nav a:hover {
            color: var(--primary);
        }

        /* ===== SECTIONS ===== */
        section {
            padding: 1.5rem 1.2rem;
        }

        .section-top-space {
            padding-top: 5rem; /* offset fixed nav */
        }

        .container {
            width: 100%;
        }

        .section-title {
            text-align: center;
            font-size: 1.4rem;
            margin-bottom: 1.5rem;
            color: var(--text);
        }

        .section-title span {
            color: var(--accent);
        }

        /* ===== HERO ===== */
        .hero {
            padding-top: 5rem;
            padding-bottom: 2rem;
            background: linear-gradient(160deg, #f8f3e8 0%, #fff 100%);
            padding-left: 1.2rem;
            padding-right: 1.2rem;
        }

        .hero-badge {
            display: inline-block;
            background: rgba(230, 180, 34, 0.15);
            color: var(--accent-dark);
            padding: 0.3rem 0.8rem;
            border-radius: 100px;
            font-size: 0.75rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .hero h1 {
            font-size: 1.85rem;
            line-height: 1.25;
            margin-bottom: 0.8rem;
            color: var(--text);
        }

        .hero h1 span {
            color: var(--accent);
        }

        .hero p {
            font-size: 0.95rem;
            color: var(--text-light);
            margin-bottom: 1.5rem;
            line-height: 1.6;
        }

        .hero-buttons {
            display: flex;
            gap: 0.75rem;
            flex-wrap: wrap;
        }

        .btn {
            padding: 0.8rem 1.5rem;
            border-radius: 100px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.2s;
            display: inline-block;
            font-size: 0.9rem;
        }

        .btn-primary {
            background: var(--primary);
            color: white;
        }

        .btn-primary:hover {
            background: var(--primary-dark);
        }

        .btn-outline {
            border: 2px solid var(--primary);
            color: var(--primary);
            background: transparent;
        }

        .hero-stats {
            display: flex;
            gap: 0;
            margin-top: 2rem;
            background: white;
            border-radius: 20px;
            box-shadow: var(--shadow-sm);
            overflow: hidden;
        }

        .stat {
            flex: 1;
            text-align: center;
            padding: 1rem 0.5rem;
            border-right: 1px solid rgba(0,0,0,0.06);
        }

        .stat:last-child {
            border-right: none;
        }

        .stat-number {
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--primary);
            font-family: 'Plus Jakarta Sans', sans-serif;
        }

        .stat-label {
            font-size: 0.7rem;
            color: var(--text-light);
            margin-top: 0.15rem;
        }

        /* ===== PROGRAM PRICE ACCORDION ===== */
        #program {
            background: white;
        }

        .programs-grid {
            display: flex;
            flex-direction: column;
            gap: 0.9rem;
        }

        .price-item {
            background: var(--bg-light);
            border-radius: 18px;
            border: 1px solid rgba(0,0,0,0.06);
            overflow: hidden;
        }

        .price-header {
            display: flex;
            align-items: center;
            gap: 0.85rem;
            padding: 1rem 1.1rem;
            cursor: pointer;
            background: none;
            border: none;
            width: 100%;
            text-align: left;
            font-family: inherit;
        }

        .program-icon {
            font-size: 1.6rem;
            flex-shrink: 0;
            width: 44px;
            height: 44px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: white;
            border-radius: 12px;
            box-shadow: var(--shadow-sm);
        }

        .price-header-info {
            flex: 1;
        }

        .price-header-info h3 {
            font-size: 0.95rem;
            margin-bottom: 0.1rem;
        }

        .price-header-info p {
            color: var(--text-light);
            font-size: 0.75rem;
        }

        .price-arrow {
            color: var(--primary);
            font-size: 1rem;
            flex-shrink: 0;
            transition: transform 0.25s ease;
        }

        .price-item.open .price-arrow {
            transform: rotate(180deg);
        }

        .price-body {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease;
        }

        .price-item.open .price-body {
            max-height: 1000px;
        }

        .price-body-inner {
            padding: 0 1.1rem 1.1rem;
        }

        .price-table-scroll {
            overflow-x: auto;
            border-radius: 12px;
            border: 1px solid rgba(0,0,0,0.08);
        }

        .price-table {
            width: 100%;
            min-width: 340px;
            border-collapse: collapse;
            background: white;
            font-size: 0.78rem;
        }

        .price-table th,
        .price-table td {
            padding: 0.55rem 0.5rem;
            text-align: center;
            border-bottom: 1px solid rgba(0,0,0,0.06);
            white-space: nowrap;
        }

        .price-table thead th {
            background: var(--primary);
            color: white;
            font-weight: 700;
            font-size: 0.72rem;
        }

        .price-table tbody th {
            background: var(--bg-light);
            font-weight: 700;
            color: var(--text);
            white-space: normal;
        }

        .price-table tbody tr:last-child td,
        .price-table tbody tr:last-child th {
            border-bottom: none;
        }

        .price-note {
            font-size: 0.72rem;
            color: var(--text-light);
            margin-top: 0.5rem;
            line-height: 1.5;
        }

        /* ===== KEUNGGULAN ===== */
        #keunggulan {
            background: var(--bg-light);
        }

        .feature-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 0.9rem;
        }

        .feature-card {
            background: white;
            border-radius: 18px;
            padding: 1.1rem 0.9rem;
            border: 1px solid rgba(0,0,0,0.06);
            box-shadow: var(--shadow-sm);
        }

        .feature-icon {
            width: 42px;
            height: 42px;
            border-radius: 12px;
            background: rgba(15, 92, 92, 0.08);
            color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            margin-bottom: 0.7rem;
        }

        .feature-card h3 {
            font-size: 0.88rem;
            margin-bottom: 0.3rem;
        }

        .feature-card p {
            font-size: 0.75rem;
            color: var(--text-light);
            line-height: 1.45;
        }

        /* ===== STATISTIK LEMBAGA ===== */
        #statistik {
            background: var(--primary);
            color: white;
        }

        #statistik .section-title {
            color: white;
        }

        #statistik .section-title span {
            color: var(--accent);
        }

        .stats-grid-full {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 0.9rem;
        }

        .stat-card-full {
            background: rgba(255,255,255,0.08);
            border-radius: 18px;
            padding: 1.2rem 0.8rem;
            text-align: center;
        }

        .stat-card-full .stat-icon {
            font-size: 1.3rem;
            color: var(--accent);
            margin-bottom: 0.4rem;
        }

        .stat-card-full .stat-number {
            color: white;
            font-size: 1.6rem;
        }

        .stat-card-full .stat-label {
            color: rgba(255,255,255,0.7);
            font-size: 0.75rem;
        }

        /* ===== PROFIL PENGAJAR ===== */
        #pengajar {
            background: white;
        }

        .teacher-scroll {
            display: flex;
            gap: 1rem;
            overflow-x: auto;
            padding-bottom: 0.5rem;
            scrollbar-width: none;
        }

        .teacher-scroll::-webkit-scrollbar {
            display: none;
        }

        .teacher-card {
            background: var(--bg-light);
            border-radius: 18px;
            padding: 1.2rem 1rem;
            min-width: 155px;
            flex-shrink: 0;
            text-align: center;
            border: 1px solid rgba(0,0,0,0.06);
        }

        .teacher-avatar {
            width: 64px;
            height: 64px;
            border-radius: 50%;
            background: var(--primary);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.4rem;
            font-weight: 700;
            margin: 0 auto 0.7rem;
        }

        .teacher-card h3 {
            font-size: 0.85rem;
            margin-bottom: 0.2rem;
        }

        .teacher-card p {
            font-size: 0.72rem;
            color: var(--text-light);
        }

        /* ===== ALUR PENDAFTARAN ===== */
        #alur {
            background: var(--bg-light);
        }

        .steps-list {
            display: flex;
            flex-direction: column;
            gap: 0;
        }

        .step-item {
            display: flex;
            gap: 1rem;
        }

        .step-marker {
            display: flex;
            flex-direction: column;
            align-items: center;
            flex-shrink: 0;
        }

        .step-number {
            width: 36px;
            height: 36px;
            border-radius: 50%;
            background: var(--primary);
            color: white;
            font-weight: 700;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
        }

        .step-line {
            width: 2px;
            flex: 1;
            background: rgba(15, 92, 92, 0.2);
            margin: 0.25rem 0;
        }

        .step-item:last-child .step-line {
            display: none;
        }

        .step-content {
            padding-bottom: 1.5rem;
        }

        .step-content h3 {
            font-size: 0.92rem;
            margin-bottom: 0.25rem;
        }

        .step-content p {
            font-size: 0.8rem;
            color: var(--text-light);
            line-height: 1.5;
        }

        /* ===== FAQ ===== */
        #faq {
            background: white;
        }

        .faq-item {
            background: var(--bg-light);
            border-radius: 16px;
            border: 1px solid rgba(0,0,0,0.06);
            overflow: hidden;
            margin-bottom: 0.8rem;
        }

        .faq-question {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 0.75rem;
            padding: 1rem 1.1rem;
            cursor: pointer;
            background: none;
            border: none;
            width: 100%;
            text-align: left;
            font-family: inherit;
            font-size: 0.88rem;
            font-weight: 600;
            color: var(--text);
        }

        .faq-question i {
            color: var(--primary);
            flex-shrink: 0;
            transition: transform 0.25s ease;
        }

        .faq-item.open .faq-question i {
            transform: rotate(180deg);
        }

        .faq-answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease;
        }

        .faq-item.open .faq-answer {
            max-height: 400px;
        }

        .faq-answer p {
            padding: 0 1.1rem 1.1rem;
            font-size: 0.8rem;
            color: var(--text-light);
            line-height: 1.55;
        }

        /* ===== KONTAK & LOKASI ===== */
        #kontak {
            background: var(--bg-light);
        }

        .kontak-card {
            background: white;
            border-radius: 18px;
            border: 1px solid rgba(0,0,0,0.06);
            overflow: hidden;
            box-shadow: var(--shadow-sm);
        }

        .kontak-map {
            width: 100%;
            height: 180px;
            border: none;
            display: block;
        }

        .kontak-info {
            padding: 1.1rem;
            display: flex;
            flex-direction: column;
            gap: 0.8rem;
        }

        .kontak-row {
            display: flex;
            align-items: flex-start;
            gap: 0.8rem;
            text-decoration: none;
            color: var(--text);
        }

        .kontak-row .kontak-icon {
            width: 36px;
            height: 36px;
            border-radius: 10px;
            background: rgba(15, 92, 92, 0.08);
            color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
            font-size: 0.9rem;
        }

        .kontak-row .kontak-label {
            font-size: 0.7rem;
            color: var(--text-light);
            text-transform: uppercase;
            letter-spacing: 0.03em;
        }

        .kontak-row .kontak-value {
            font-size: 0.86rem;
            font-weight: 600;
        }

        /* ===== TESTIMONI ===== */
        #testimoni {
            background: var(--bg-light);
        }

        .testimonials-scroll {
            display: flex;
            gap: 1rem;
            overflow-x: auto;
            padding-bottom: 0.5rem;
            scrollbar-width: none;
            -ms-overflow-style: none;
        }

        .testimonials-scroll::-webkit-scrollbar {
            display: none;
        }

        .testimonial-card {
            background: white;
            padding: 1.3rem;
            border-radius: 20px;
            box-shadow: var(--shadow-sm);
            min-width: 270px;
            flex-shrink: 0;
        }

        .stars {
            color: var(--accent);
            font-size: 0.85rem;
            margin-bottom: 0.6rem;
        }

        .testimonial-text {
            font-style: italic;
            color: var(--text-light);
            margin-bottom: 1rem;
            font-size: 0.88rem;
            line-height: 1.5;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 0.75rem;
        }

        .author-avatar {
            width: 40px;
            height: 40px;
            background: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            font-size: 0.85rem;
            flex-shrink: 0;
        }

        .author-name {
            font-size: 0.88rem;
            font-weight: 600;
        }

        .author-role {
            font-size: 0.75rem;
            color: var(--text-light);
        }

        /* ===== CTA BANNER ===== */
        .cta-section {
            background: var(--primary);
            border-radius: 24px;
            padding: 2rem 1.5rem;
            text-align: center;
            color: white;
            margin: 0 1.2rem 1.5rem;
        }

        .cta-section h2 {
            font-size: 1.4rem;
            margin-bottom: 0.6rem;
        }

        .cta-section p {
            font-size: 0.88rem;
            opacity: 0.8;
            margin-bottom: 1.2rem;
        }

        .btn-white {
            background: white;
            color: var(--primary);
            font-weight: 700;
        }

        /* ===== FORM ===== */
        #daftar {
            background: white;
        }

        .form-card {
            background: var(--bg-light);
            padding: 1.5rem;
            border-radius: 24px;
            border: 1px solid rgba(0,0,0,0.06);
        }

        .form-card h2 {
            text-align: center;
            font-size: 1.3rem;
            margin-bottom: 1.2rem;
        }

        .form-group {
            margin-bottom: 1rem;
        }

        .form-label {
            display: block;
            font-size: 0.8rem;
            font-weight: 600;
            color: var(--text-light);
            margin-bottom: 0.35rem;
            text-transform: uppercase;
            letter-spacing: 0.04em;
        }

        .form-group input,
        .form-group select {
            width: 100%;
            padding: 0.85rem 1rem;
            border: 1.5px solid #e2e8f0;
            border-radius: 14px;
            font-family: inherit;
            font-size: 0.95rem;
            transition: all 0.2s;
            background: white;
            color: var(--text);
            -webkit-appearance: none;
        }

        .form-group input:focus,
        .form-group select:focus {
            outline: none;
            border-color: var(--accent);
            box-shadow: 0 0 0 3px rgba(230, 180, 34, 0.15);
        }

        .btn-wa {
            width: 100%;
            padding: 1rem;
            background: #25D366;
            color: white;
            border: none;
            border-radius: 14px;
            font-family: inherit;
            font-size: 1rem;
            font-weight: 700;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            margin-top: 0.5rem;
            transition: background 0.2s;
        }

        .btn-wa:hover {
            background: #1ebe5a;
        }

        /* ===== FOOTER ===== */
        footer {
            background: #1a2a2a;
            color: white;
            padding: 2rem 1.2rem 1.5rem;
            text-align: center;
        }

        .footer-logo {
            font-size: 1.4rem;
            font-weight: 800;
            margin-bottom: 0.3rem;
            font-family: 'Plus Jakarta Sans', sans-serif;
        }

        .footer-tagline {
            color: rgba(255,255,255,0.5);
            font-size: 0.8rem;
            margin-bottom: 1.2rem;
        }

        .footer-contact {
            display: flex;
            flex-direction: column;
            gap: 0.5rem;
            margin-bottom: 1.5rem;
        }

        .footer-contact a {
            color: rgba(255,255,255,0.7);
            text-decoration: none;
            font-size: 0.85rem;
        }

        .footer-links-row {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            flex-wrap: wrap;
            margin-bottom: 1.5rem;
        }

        .footer-links-row a {
            color: rgba(255,255,255,0.6);
            text-decoration: none;
            font-size: 0.82rem;
        }

        .footer-copy {
            font-size: 0.75rem;
            color: rgba(255,255,255,0.35);
            padding-top: 1.2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
        }

        /* ===== WHATSAPP FLOAT ===== */
        .whatsapp-float {
            position: fixed;
            bottom: 84px;
            right: 16px;
            background: #25D366;
            width: 52px;
            height: 52px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.6rem;
            box-shadow: 0 4px 16px rgba(37, 211, 102, 0.4);
            text-decoration: none;
            z-index: 99;
        }

        /* ===== DIVIDER ===== */
        .section-divider {
            height: 1px;
            background: rgba(0,0,0,0.06);
            margin: 0 1.2rem;
        }
    </style>
</head>
<body>

    <!-- TOP NAV -->
    <nav>
        <a href="#home" class="logo">IMTI<span>YAZ</span></a>
        <a href="#daftar" class="nav-daftar">Daftar Sekarang</a>
    </nav>

    <!-- HERO -->
    <section class="hero" id="home">
        <img src="logo-imtiyaz.png" alt="logo">
        
        <h1>Belajar Lebih Dekat, <span>Hasil Lebih Hebat</span></h1>
        <p>Bimbingan privat Quran & Akademik di Banda Aceh. Metode personal, fleksibel, dan terjangkau.</p>
        <div class="hero-buttons">
            <a href="#daftar" class="btn btn-primary">Daftar Sekarang →</a>
            <a href="#program" class="btn btn-outline">Lihat Program</a>
        </div>
        <div class="hero-stats">
            <div class="stat">
                <div class="stat-number">500+</div>
                <div class="stat-label">Siswa</div>
            </div>
            <div class="stat">
                <div class="stat-number">20+</div>
                <div class="stat-label">Pengajar</div>
            </div>
            <div class="stat">
                <div class="stat-number">98%</div>
                <div class="stat-label">Puas</div>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- KEUNGGULAN -->
    <section id="keunggulan">
        <div class="container">
            <h2 class="section-title">Kenapa Pilih <span>IMTIYAZ?</span></h2>
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-user-graduate"></i></div>
                    <h3>Pengajar Berpengalaman</h3>
                    <p>Tenaga pengajar terseleksi, ahli di bidang Quran & akademik.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-house-user"></i></div>
                    <h3>Belajar Fleksibel</h3>
                    <p>Jadwal privat menyesuaikan waktu siswa & orang tua.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-tags"></i></div>
                    <h3>Harga Terjangkau</h3>
                    <p>Paket bervariasi, bisa dipilih sesuai kebutuhan & budget.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-heart"></i></div>
                    <h3>Metode Personal</h3>
                    <p>Pendekatan sabar & disesuaikan karakter tiap anak.</p>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- PROGRAM -->
    <section id="program">
        <div class="container">
            <h2 class="section-title">Daftar Harga <span>& Paket</span></h2>
            <p style="text-align:center; color:var(--text-light); font-size:0.8rem; margin-top:-1rem; margin-bottom:1.2rem;">Ketuk tiap kategori untuk lihat rincian paket & harga</p>
            <div class="programs-grid">

                <!-- 1. CALISTUNG & IQRA -->
                <div class="price-item">
                    <button class="price-header" onclick="togglePrice(this)">
                        <div class="program-icon">📚</div>
                        <div class="price-header-info">
                            <h3>Calistung & Iqra</h3>
                            <p>Baca, tulis, hitung & mengaji Iqra</p>
                        </div>
                        <i class="fas fa-chevron-down price-arrow"></i>
                    </button>
                    <div class="price-body">
                        <div class="price-body-inner">
                            <div class="price-table-scroll">
                                <table class="price-table">
                                    <thead>
                                        <tr>
                                            <th>Paket</th>
                                            <th>Calistung & Iqra<br>1 jam</th>
                                            <th>Calistung & Iqra<br>1½ jam</th>
                                        </tr>
                                    </thead>
                                    <tbody>
                                        <tr>
                                            <th>Durasi sesi</th>
                                            <td>1–2 Murid<br>(kakak beradik)</td>
                                            <td>3–5 Murid<br>(kelompok)</td>
                                        </tr>
                                        <tr>
                                            <th>8 Pertemuan</th>
                                            <td>Rp 280.000 – 300.000</td>
                                            <td>Rp 350.000</td>
                                        </tr>
                                        <tr>
                                            <th>12 Pertemuan</th>
                                            <td>Rp 420.000 – 440.000</td>
                                            <td>Rp 510.000</td>
                                        </tr>
                                        <tr>
                                            <th>16 Pertemuan</th>
                                            <td>Rp 560.000 – 580.000</td>
                                            <td>Rp 700.000</td>
                                        </tr>
                                    </tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 2. TAHFIZ & TAHSIN -->
                <div class="price-item">
                    <button class="price-header" onclick="togglePrice(this)">
                        <div class="program-icon">📿</div>
                        <div class="price-header-info">
                            <h3>Tahfiz & Tahsin</h3>
                            <p>Tajwid, makhraj, dan hafalan Al-Qur'an</p>
                        </div>
                        <i class="fas fa-chevron-down price-arrow"></i>
                    </button>
                    <div class="price-body">
                        <div class="price-body-inner">
                            <div class="price-table-scroll">
                                <table class="price-table">
                                    <thead>
                                        <tr>
                                            <th>Paket</th>
                                            <th>Tahfiz & Tahsin<br>1 jam</th>
                                            <th>Tahfiz & Tahsin<br>1½ jam</th>
                                        </tr>
                                    </thead>
                                    <tbody>
                                        <tr>
                                            <th>Durasi sesi</th>
                                            <td>1–2 Murid<br>(kakak beradik)</td>
                                            <td>3–5 Murid<br>(kelompok)</td>
                                        </tr>
                                        <tr>
                                            <th>8 Pertemuan</th>
                                            <td>Rp 280.000 – 300.000</td>
                                            <td>Rp 350.000</td>
                                        </tr>
                                        <tr>
                                            <th>12 Pertemuan</th>
                                            <td>Rp 420.000 – 440.000</td>
                                            <td>Rp 510.000</td>
                                        </tr>
                                        <tr>
                                            <th>16 Pertemuan</th>
                                            <td>Rp 560.000 – 580.000</td>
                                            <td>Rp 700.000</td>
                                        </tr>
                                    </tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 3. BAHASA ARAB / INGGRIS -->
                <div class="price-item">
                    <button class="price-header" onclick="togglePrice(this)">
                        <div class="program-icon">🌍</div>
                        <div class="price-header-info">
                            <h3>Bahasa Arab / Inggris</h3>
                            <p>Nahwu, sharaf, speaking & grammar</p>
                        </div>
                        <i class="fas fa-chevron-down price-arrow"></i>
                    </button>
                    <div class="price-body">
                        <div class="price-body-inner">
                            <div class="price-table-scroll">
                                <table class="price-table">
                                    <thead>
                                        <tr>
                                            <th>Paket</th>
                                            <th>TK/SD</th>
                                            <th>SMP</th>
                                            <th>SMA</th>
                                        </tr>
                                    </thead>
                                    <tbody>
                                        <tr>
                                            <th>4 pertemuan</th>
                                            <td>Rp 180.000</td>
                                            <td>Rp 220.000</td>
                                            <td>Rp 260.000</td>
                                        </tr>
                                        <tr>
                                            <th>6 pertemuan</th>
                                            <td>Rp 270.000</td>
                                            <td>Rp 330.000</td>
                                            <td>Rp 390.000</td>
                                        </tr>
                                        <tr>
                                            <th>8 pertemuan</th>
                                            <td>Rp 360.000</td>
                                            <td>Rp 440.000</td>
                                            <td>Rp 520.000</td>
                                        </tr>
                                        <tr>
                                            <th>12 pertemuan</th>
                                            <td>Rp 540.000</td>
                                            <td>Rp 660.000</td>
                                            <td>Rp 700.000</td>
                                        </tr>
                                        <tr>
                                            <th>16 pertemuan</th>
                                            <td>Rp 720.000</td>
                                            <td>Rp 880.000</td>
                                            <td>Rp 1.000.000</td>
                                        </tr>
                                    </tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 4. MAPEL UMUM -->
                <div class="price-item">
                    <button class="price-header" onclick="togglePrice(this)">
                        <div class="program-icon">📖</div>
                        <div class="price-header-info">
                            <h3>Mapel Umum</h3>
                            <p>SD, SMP, SMA — semua mata pelajaran</p>
                        </div>
                        <i class="fas fa-chevron-down price-arrow"></i>
                    </button>
                    <div class="price-body">
                        <div class="price-body-inner">
                            <div class="price-table-scroll">
                                <table class="price-table">
                                    <thead>
                                        <tr>
                                            <th>Paket</th>
                                            <th>SD<br>(Kelas 1-3)</th>
                                            <th>SD<br>(Kelas 4-6)</th>
                                            <th>SMP</th>
                                            <th>SMA</th>
                                        </tr>
                                    </thead>
                                    <tbody>
                                        <tr>
                                            <th>4 Pertemuan</th>
                                            <td>–</td>
                                            <td>Rp 160.000</td>
                                            <td>Rp 180.000</td>
                                            <td>Rp 200.000</td>
                                        </tr>
                                        <tr>
                                            <th>6 Pertemuan</th>
                                            <td>–</td>
                                            <td>Rp 240.000</td>
                                            <td>Rp 270.000</td>
                                            <td>Rp 300.000</td>
                                        </tr>
                                        <tr>
                                            <th>8 Pertemuan</th>
                                            <td>Rp 280.000</td>
                                            <td>Rp 320.000</td>
                                            <td>Rp 360.000</td>
                                            <td>Rp 400.000</td>
                                        </tr>
                                        <tr>
                                            <th>12 Pertemuan</th>
                                            <td>Rp 420.000</td>
                                            <td>Rp 480.000</td>
                                            <td>Rp 540.000</td>
                                            <td>Rp 600.000</td>
                                        </tr>
                                        <tr>
                                            <th>16 Pertemuan</th>
                                            <td>Rp 560.000</td>
                                            <td>Rp 640.000</td>
                                            <td>Rp 720.000</td>
                                            <td>Rp 800.000</td>
                                        </tr>
                                    </tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 5. TILAWAH -->
                <div class="price-item">
                    <button class="price-header" onclick="togglePrice(this)">
                        <div class="program-icon">🕌</div>
                        <div class="price-header-info">
                            <h3>Tilawah</h3>
                            <p>Seni membaca Al-Qur'an berkelompok</p>
                        </div>
                        <i class="fas fa-chevron-down price-arrow"></i>
                    </button>
                    <div class="price-body">
                        <div class="price-body-inner">
                            <div class="price-table-scroll">
                                <table class="price-table">
                                    <thead>
                                        <tr>
                                            <th>Paket</th>
                                            <th>Tilawah (3–5 Murid)</th>
                                        </tr>
                                    </thead>
                                    <tbody>
                                        <tr>
                                            <th>8 Pertemuan</th>
                                            <td>Rp 400.000</td>
                                        </tr>
                                        <tr>
                                            <th>12 Pertemuan</th>
                                            <td>Rp 600.000</td>
                                        </tr>
                                        <tr>
                                            <th>16 Pertemuan</th>
                                            <td>Rp 800.000</td>
                                        </tr>
                                    </tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- 6. ANAK BERKEBUTUHAN KHUSUS -->
                <div class="price-item">
                    <button class="price-header" onclick="togglePrice(this)">
                        <div class="program-icon">💛</div>
                        <div class="price-header-info">
                            <h3>Anak Berkebutuhan Khusus</h3>
                            <p>Pendampingan & privat khusus ABK</p>
                        </div>
                        <i class="fas fa-chevron-down price-arrow"></i>
                    </button>
                    <div class="price-body">
                        <div class="price-body-inner">
                            <div class="price-table-scroll">
                                <table class="price-table">
                                    <thead>
                                        <tr>
                                            <th>Spesial</th>
                                            <th>Detail</th>
                                        </tr>
                                    </thead>
                                    <tbody>
                                        <tr>
                                            <th>ABK Shadow Teacher</th>
                                            <td>Rp 900.000 / bulan</td>
                                        </tr>
                                        <tr>
                                            <th>Privat Khusus ABK</th>
                                            <td>Diskusi dulu nanti</td>
                                        </tr>
                                    </tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- STATISTIK LEMBAGA -->
    <section id="statistik">
        <div class="container">
            <h2 class="section-title">Statistik <span>Lembaga</span></h2>
            <div class="stats-grid-full">
                <div class="stat-card-full">
                    <div class="stat-icon"><i class="fas fa-user-graduate"></i></div>
                    <div class="stat-number">500+</div>
                    <div class="stat-label">Siswa Aktif</div>
                </div>
                <div class="stat-card-full">
                    <div class="stat-icon"><i class="fas fa-chalkboard-teacher"></i></div>
                    <div class="stat-number">20+</div>
                    <div class="stat-label">Pengajar</div>
                </div>
                <div class="stat-card-full">
                    <div class="stat-icon"><i class="fas fa-smile"></i></div>
                    <div class="stat-number">98%</div>
                    <div class="stat-label">Orang Tua Puas</div>
                </div>
                <div class="stat-card-full">
                    <div class="stat-icon"><i class="fas fa-map-marker-alt"></i></div>
                    <div class="stat-number">Banda Aceh</div>
                    <div class="stat-label">Area Layanan</div>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- PROFIL PENGAJAR -->
    <section id="pengajar">
        <div class="container">
            <h2 class="section-title">Profil <span>Pengajar</span></h2>
            <div class="teacher-scroll">
                <div class="teacher-card">
                    <div class="teacher-avatar">UF</div>
                    <h3>Ustadzah Fitri</h3>
                    <p>Spesialis Tahfiz & Tahsin</p>
                </div>
                <div class="teacher-card">
                    <div class="teacher-avatar">UR</div>
                    <h3>Ustadz Rizal</h3>
                    <p>Spesialis Bahasa Arab</p>
                </div>
                <div class="teacher-card">
                    <div class="teacher-avatar">KD</div>
                    <h3>Kak Dinda</h3>
                    <p>Spesialis Calistung</p>
                </div>
                <div class="teacher-card">
                    <div class="teacher-avatar">KH</div>
                    <h3>Kak Hafiz</h3>
                    <p>Spesialis Mapel Umum</p>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- TESTIMONI -->
    <section id="testimoni">
        <div class="container">
            <h2 class="section-title">Apa Kata <span>Mereka?</span></h2>
            <div class="testimonials-scroll">
                <div class="testimonial-card">
                    <div class="stars">★★★★★</div>
                    <p class="testimonial-text">"Alhamdulillah, nilai anak saya meningkat drastis. Pengajarnya sabar dan metode belajarnya menyenangkan."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">SR</div>
                        <div>
                            <div class="author-name">Siti Rahmawati</div>
                            <div class="author-role">Orang Tua Siswa</div>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="stars">★★★★★</div>
                    <p class="testimonial-text">"Program tahfidz sangat membantu. Anak saya jadi lebih lancar membaca Al-Qur'an dengan tajwid yang benar."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">AH</div>
                        <div>
                            <div class="author-name">Ahmad Hidayat</div>
                            <div class="author-role">Orang Tua Siswa</div>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="stars">★★★★★</div>
                    <p class="testimonial-text">"Belajar Bahasa Inggris di sini seru! Sekarang saya lebih percaya diri speaking di sekolah."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">FZ</div>
                        <div>
                            <div class="author-name">Fatimah Az-Zahra</div>
                            <div class="author-role">Siswa SMA</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- ALUR PENDAFTARAN -->
    <section id="alur">
        <div class="container">
            <h2 class="section-title">Alur <span>Pendaftaran</span></h2>
            <div class="steps-list">
                <div class="step-item">
                    <div class="step-marker">
                        <div class="step-number">1</div>
                        <div class="step-line"></div>
                    </div>
                    <div class="step-content">
                        <h3>Isi Formulir</h3>
                        <p>Lengkapi data siswa & pilih program di form pendaftaran.</p>
                    </div>
                </div>
                <div class="step-item">
                    <div class="step-marker">
                        <div class="step-number">2</div>
                        <div class="step-line"></div>
                    </div>
                    <div class="step-content">
                        <h3>Konfirmasi via WhatsApp</h3>
                        <p>Tim IMTIYAZ menghubungi untuk konfirmasi jadwal & pengajar.</p>
                    </div>
                </div>
                <div class="step-item">
                    <div class="step-marker">
                        <div class="step-number">3</div>
                        <div class="step-line"></div>
                    </div>
                    <div class="step-content">
                        <h3>Sesi Trial</h3>
                        <p>Coba sesi konsultasi & trial gratis 30 menit sebelum mulai.</p>
                    </div>
                </div>
                <div class="step-item">
                    <div class="step-marker">
                        <div class="step-number">4</div>
                    </div>
                    <div class="step-content">
                        <h3>Mulai Belajar</h3>
                        <p>Siswa mulai sesi belajar privat sesuai jadwal yang disepakati.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- FAQ -->
    <section id="faq">
        <div class="container">
            <h2 class="section-title">Pertanyaan <span>Umum</span></h2>
            <div class="faq-list">
                <div class="faq-item">
                    <button class="faq-question" onclick="toggleFaq(this)">
                        Apakah ada sesi trial gratis?
                        <i class="fas fa-chevron-down"></i>
                    </button>
                    <div class="faq-answer">
                        <p>Ya, IMTIYAZ menyediakan sesi konsultasi dan trial gratis selama 30 menit sebelum siswa memutuskan untuk mendaftar.</p>
                    </div>
                </div>
                <div class="faq-item">
                    <button class="faq-question" onclick="toggleFaq(this)">
                        Bagaimana sistem pembayarannya?
                        <i class="fas fa-chevron-down"></i>
                    </button>
                    <div class="faq-answer">
                        <p>Pembayaran dilakukan per paket (8/12/16 pertemuan) dan bisa didiskusikan langsung dengan tim admin via WhatsApp.</p>
                    </div>
                </div>
                <div class="faq-item">
                    <button class="faq-question" onclick="toggleFaq(this)">
                        Apakah bisa belajar berkelompok dengan saudara?
                        <i class="fas fa-chevron-down"></i>
                    </button>
                    <div class="faq-answer">
                        <p>Bisa. Tersedia paket kakak beradik (1-2 murid) dan paket kelompok (3-5 murid) dengan harga yang lebih hemat per anak.</p>
                    </div>
                </div>
                <div class="faq-item">
                    <button class="faq-question" onclick="toggleFaq(this)">
                        Apakah tersedia program untuk Anak Berkebutuhan Khusus?
                        <i class="fas fa-chevron-down"></i>
                    </button>
                    <div class="faq-answer">
                        <p>Ya, IMTIYAZ menyediakan layanan ABK Shadow Teacher dan privat khusus ABK yang bisa didiskusikan sesuai kebutuhan anak.</p>
                    </div>
                </div>
                <div class="faq-item">
                    <button class="faq-question" onclick="toggleFaq(this)">
                        Di mana lokasi bimbingan belajar?
                        <i class="fas fa-chevron-down"></i>
                    </button>
                    <div class="faq-answer">
                        <p>IMTIYAZ berlokasi di Banda Aceh dan melayani privat datang ke rumah maupun sesi di tempat, sesuai kesepakatan.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- CTA BANNER -->
    <div class="cta-section">
        <h2>Mau coba gratis?</h2>
        <p>Dapatkan sesi konsultasi dan uji coba gratis 30 menit</p>
        <a href="#daftar" class="btn btn-white">Hubungi Kami →</a>
    </div>

    <!-- FORM DAFTAR -->
    <section id="daftar">
        <div class="container">
            <div class="form-card">
                <h2>Daftar Sekarang</h2>
                <form id="registerForm">
                    <div class="form-group">
                        <label class="form-label" for="nama">Nama Siswa</label>
                        <input type="text" placeholder="Masukkan nama lengkap" id="nama" required>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="programSelect">Program</label>
                        <select id="programSelect" required>
                            <option value="">Pilih Program</option>
                            <option value="Calistung">Calistung</option>
                            <option value="Mengaji & Tahfidz">Mengaji & Tahfidz</option>
                            <option value="Bahasa Arab">Bahasa Arab</option>
                            <option value="Bahasa Inggris">Bahasa Inggris</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="wa">No. WhatsApp</label>
                        <input type="tel" placeholder="Contoh: 08123456789" id="wa" required>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="alamat">Alamat</label>
                        <input type="text" placeholder="Kecamatan / Kelurahan" id="alamat" required>
                    </div>
                    <button type="submit" class="btn-wa">
                        <i class="fab fa-whatsapp"></i> Daftar via WhatsApp
                    </button>
                </form>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- KONTAK & LOKASI -->
    <section id="kontak">
        <div class="container">
            <h2 class="section-title">Kontak <span>& Lokasi</span></h2>
            <div class="kontak-card">
                <iframe class="kontak-map" src="https://maps.google.com/maps?q=Banda%20Aceh&t=&z=13&ie=UTF8&iwloc=&output=embed" loading="lazy"></iframe>
                <div class="kontak-info">
                    <a href="tel:082280101093" class="kontak-row">
                        <div class="kontak-icon"><i class="fas fa-phone"></i></div>
                        <div>
                            <div class="kontak-label">Telepon</div>
                            <div class="kontak-value">0822 8010 1093</div>
                        </div>
                    </a>
                    <a href="https://wa.me/6282280101093" target="_blank" class="kontak-row">
                        <div class="kontak-icon"><i class="fab fa-whatsapp"></i></div>
                        <div>
                            <div class="kontak-label">WhatsApp</div>
                            <div class="kontak-value">Chat Sekarang</div>
                        </div>
                    </a>
                    <a href="mailto:privateimtiyaz@gmail.com" class="kontak-row">
                        <div class="kontak-icon"><i class="fas fa-envelope"></i></div>
                        <div>
                            <div class="kontak-label">Email</div>
                            <div class="kontak-value">privateimtiyaz@gmail.com</div>
                        </div>
                    </a>
                    <div class="kontak-row">
                        <div class="kontak-icon"><i class="fas fa-map-marker-alt"></i></div>
                        <div>
                            <div class="kontak-label">Lokasi</div>
                            <div class="kontak-value">Banda Aceh, Aceh</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="footer-logo">IMTI<span style="color: var(--accent);">YAZ</span></div>
        <p class="footer-tagline">Quranic & Academic Tutoring · Banda Aceh</p>
        <div class="footer-links-row">
            <a href="#program">Program</a>
            <a href="#pengajar">Pengajar</a>
            <a href="#faq">FAQ</a>
            <a href="#kontak">Kontak</a>
        </div>
        <div class="footer-copy">© 2026 IMTIYAZ. All rights reserved.</div>
    </footer>


    <!-- WHATSAPP FLOAT -->
    <a href="https://wa.me/6282280101093" class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <!-- BOTTOM NAV -->
    <div class="bottom-nav">
        <a href="#home" class="active">
            <i class="fas fa-home"></i>
            <span>Beranda</span>
        </a>
        <a href="#program">
            <i class="fas fa-book-open"></i>
            <span>Program</span>
        </a>
        <a href="#testimoni">
            <i class="fas fa-star"></i>
            <span>Testimoni</span>
        </a>
        <a href="#daftar">
            <i class="fas fa-user-plus"></i>
            <span>Daftar</span>
        </a>
        <a href="#kontak">
            <i class="fas fa-map-marker-alt"></i>
            <span>Kontak</span>
        </a>
    </div>

    <script>
        // Toggle accordion daftar harga
        function togglePrice(headerEl) {
            const item = headerEl.closest('.price-item');
            const wasOpen = item.classList.contains('open');
            document.querySelectorAll('.price-item.open').forEach(el => el.classList.remove('open'));
            if (!wasOpen) {
                item.classList.add('open');
            }
        }

        // Toggle accordion FAQ
        function toggleFaq(questionEl) {
            const item = questionEl.closest('.faq-item');
            const wasOpen = item.classList.contains('open');
            document.querySelectorAll('.faq-item.open').forEach(el => el.classList.remove('open'));
            if (!wasOpen) {
                item.classList.add('open');
            }
        }

        // Form submission → WhatsApp
        const form = document.getElementById('registerForm');
        form.addEventListener('submit', (e) => {
            e.preventDefault();
            const nama = document.getElementById('nama').value.trim();
            const program = document.getElementById('programSelect').value;
            const wa = document.getElementById('wa').value.trim();
            const alamat = document.getElementById('alamat').value.trim();

            if (!nama || !program || !wa || !alamat) {
                alert('Mohon lengkapi semua data!');
                return;
            }

            const message = `Halo IMTIYAZ, saya ingin mendaftar:%0A%0A*Nama:* ${encodeURIComponent(nama)}%0A*Program:* ${encodeURIComponent(program)}%0A*WhatsApp:* ${encodeURIComponent(wa)}%0A*Alamat:* ${encodeURIComponent(alamat)}%0A%0AMohon info lebih lanjut. Terima kasih.`;
            window.open(`https://wa.me/6282280101093?text=${message}`, '_blank');
            form.reset();
        });

        // Active bottom nav on scroll
        const sections = document.querySelectorAll('section[id]');
        const navLinks = document.querySelectorAll('.bottom-nav a');

        window.addEventListener('scroll', () => {
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop - 100;
                if (pageYOffset >= sectionTop) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === '#' + current) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>
