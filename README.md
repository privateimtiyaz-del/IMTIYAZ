<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>IMTIYAZ PRIVATE - Bimbel Quran & Akademik ke Rumah</title>
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

        html { scroll-behavior: smooth; }

        body {
            font-family: 'Inter', sans-serif;
            color: var(--text);
            background: var(--bg-light);
            line-height: 1.5;
            max-width: 480px;
            margin: 0 auto;
            overflow-x: hidden;
            padding-bottom: 72px;
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
            padding: 0.9rem 1.2rem 1.6rem;
            border-bottom: 1px solid rgba(0, 0, 0, 0.07);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-nav {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            text-decoration: none;
        }

        .logo-nav img {
            height: 32px;
            width: 32px;
            object-fit: contain;
            mix-blend-mode: multiply;
        }

        .logo-nav span {
            font-size: 1.15rem;
            font-weight: 800;
            color: var(--primary);
            font-family: 'Plus Jakarta Sans', sans-serif;
        }

        .logo-nav span em {
            font-style: normal;
            color: var(--accent);
        }

        .nav-daftar {
            background: var(--primary);
            color: white !important;
            padding: 0.45rem 1rem;
            border-radius: 100px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.82rem;
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

        .bottom-nav a i { font-size: 1.1rem; }
        .bottom-nav a.active, .bottom-nav a:hover { color: var(--primary); }

        /* ===== SECTIONS ===== */
        section { padding: 1.5rem 1.2rem; }
        .container { width: 100%; }

        .section-title {
            text-align: center;
            font-size: 1.4rem;
            margin-bottom: 0.4rem;
            color: var(--text);
        }

        .section-title span { color: var(--accent); }

        .section-subtitle {
            text-align: center;
            color: var(--text-light);
            font-size: 0.82rem;
            margin-bottom: 1.5rem;
        }

        .section-divider {
            height: 1px;
            background: rgba(0,0,0,0.06);
            margin: 0 1.2rem;
        }

        /* ===== HERO ===== */
        .hero {
            padding-top: 5.3rem;
            padding-bottom: 2rem;
            background: linear-gradient(160deg, #f8f3e8 0%, #fff 100%);
            padding-left: 1.2rem;
            padding-right: 1.2rem;
            text-align: center;
        }

        .hero-logo {
            display: block;
            max-width: 84px;
            margin: 0 auto 1rem;
            mix-blend-mode: multiply;
        }

        .hero-badge {
            display: block;
            width: fit-content;
            margin: 0 auto 1rem;
            background: rgba(230, 180, 34, 0.15);
            color: var(--accent-dark);
            padding: 0.3rem 0.8rem;
            border-radius: 100px;
            font-size: 0.75rem;
            font-weight: 600;
            text-align: center;
        }

        .hero h1 {
            font-size: 1.7rem;
            line-height: 1.3;
            margin-bottom: 1rem;
            color: var(--text);
            text-align: center;
        }

        .hero h1 span { color: var(--accent); }

        .hero-points {
            list-style: none;
            text-align: left;
            display: inline-flex;
            flex-direction: column;
            gap: 0.6rem;
            margin: 0 auto 1.5rem;
        }

        .hero-points li {
            display: flex;
            align-items: flex-start;
            gap: 0.6rem;
            font-size: 0.88rem;
            color: var(--text-light);
        }

        .hero-points li i {
            color: var(--primary);
            margin-top: 0.2rem;
            flex-shrink: 0;
        }

        .hero-buttons {
            display: flex;
            gap: 0.75rem;
            flex-wrap: wrap;
            justify-content: center;
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

        .btn-primary { background: var(--primary); color: white; }
        .btn-primary:hover { background: var(--primary-dark); }
        .btn-outline { border: 2px solid var(--primary); color: var(--primary); background: transparent; }
        .btn-white { background: white; color: var(--primary); font-weight: 700; }

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
        .stat:last-child { border-right: none; }
        .stat-number { font-size: 1.4rem; font-weight: 800; color: var(--primary); font-family: 'Plus Jakarta Sans', sans-serif; }
        .stat-label { font-size: 0.68rem; color: var(--text-light); margin-top: 0.15rem; }

        /* ===== KEUNGGULAN ===== */
        #keunggulan { background: white; }

        .feature-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 0.9rem;
        }

        .feature-card {
            background: var(--bg-light);
            border-radius: 18px;
            padding: 1.1rem 0.9rem;
            border: 1px solid rgba(0,0,0,0.06);
            text-align: center;
        }

        .feature-icon {
            width: 46px;
            height: 46px;
            border-radius: 14px;
            background: rgba(15, 92, 92, 0.08);
            color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.3rem;
            margin: 0 auto 0.6rem;
        }

        .feature-card h3 { font-size: 0.85rem; margin-bottom: 0.25rem; }
        .feature-card p { font-size: 0.72rem; color: var(--text-light); line-height: 1.4; }

        /* ===== ACCORDION GENERIC (Program List, FAQ) ===== */
        #program-list { background: var(--bg-light); }

        .acc-list { display: flex; flex-direction: column; gap: 0.7rem; }

        .acc-item {
            background: white;
            border-radius: 16px;
            border: 1px solid rgba(0,0,0,0.06);
            overflow: hidden;
        }

        .acc-header {
            display: flex;
            align-items: center;
            gap: 0.8rem;
            padding: 0.9rem 1rem;
            cursor: pointer;
            background: none;
            border: none;
            width: 100%;
            text-align: left;
            font-family: inherit;
        }

        .acc-icon {
            width: 38px;
            height: 38px;
            border-radius: 10px;
            background: rgba(15, 92, 92, 0.08);
            color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1rem;
            flex-shrink: 0;
        }

        .acc-header span.acc-title {
            flex: 1;
            font-size: 0.88rem;
            font-weight: 600;
            color: var(--text);
        }

        .acc-header i.acc-arrow {
            color: var(--primary);
            transition: transform 0.25s ease;
            flex-shrink: 0;
        }

        .acc-item.open .acc-arrow { transform: rotate(180deg); }

        .acc-body { max-height: 0; overflow: hidden; transition: max-height 0.3s ease; }
        .acc-item.open .acc-body { max-height: 400px; }

        .acc-body p {
            padding: 0 1rem 1rem 3.6rem;
            font-size: 0.78rem;
            color: var(--text-light);
            line-height: 1.5;
        }

        /* ===== PAKET & HARGA ===== */
        #harga { background: white; }

        .price-item {
            background: var(--bg-light);
            border-radius: 18px;
            border: 1px solid rgba(0,0,0,0.06);
            overflow: hidden;
            margin-bottom: 0.9rem;
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

        .price-header-info { flex: 1; }
        .price-header-info h3 { font-size: 0.95rem; margin-bottom: 0.1rem; }
        .price-header-info p { color: var(--text-light); font-size: 0.75rem; }

        .price-arrow { color: var(--primary); font-size: 1rem; flex-shrink: 0; transition: transform 0.25s ease; }
        .price-item.open .price-arrow { transform: rotate(180deg); }

        .price-body { max-height: 0; overflow: hidden; transition: max-height 0.3s ease; }
        .price-item.open .price-body { max-height: 1000px; }
        .price-body-inner { padding: 0 1.1rem 1.1rem; }

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

        .price-table th, .price-table td {
            padding: 0.55rem 0.5rem;
            text-align: center;
            border-bottom: 1px solid rgba(0,0,0,0.06);
            white-space: nowrap;
        }

        .price-table thead th { background: var(--primary); color: white; font-weight: 700; font-size: 0.72rem; }
        .price-table tbody th { background: var(--bg-light); font-weight: 700; color: var(--text); white-space: normal; }
        .price-table tbody tr:last-child td, .price-table tbody tr:last-child th { border-bottom: none; }

        .harga-notes {
            background: var(--bg-light);
            border-radius: 16px;
            border: 1px solid rgba(0,0,0,0.06);
            padding: 1.1rem;
            margin-top: 0.3rem;
        }

        .harga-notes h3 { font-size: 0.88rem; margin-bottom: 0.7rem; }

        .harga-notes ul { list-style: none; display: flex; flex-direction: column; gap: 0.5rem; }

        .harga-notes li {
            display: flex;
            align-items: flex-start;
            gap: 0.5rem;
            font-size: 0.8rem;
            color: var(--text-light);
        }

        .harga-notes li i { color: var(--primary); margin-top: 0.2rem; flex-shrink: 0; }

        .harga-notes .harga-transport {
            margin-top: 0.7rem;
            padding-top: 0.7rem;
            border-top: 1px dashed rgba(0,0,0,0.1);
            font-size: 0.76rem;
            color: var(--text-light);
            font-style: italic;
        }

        /* ===== ALUR PENDAFTARAN ===== */
        #alur { background: var(--bg-light); }

        .steps-list { display: flex; flex-direction: column; }
        .step-item { display: flex; gap: 1rem; }

        .step-marker { display: flex; flex-direction: column; align-items: center; flex-shrink: 0; }

        .step-number {
            width: 36px; height: 36px; border-radius: 50%;
            background: var(--primary); color: white; font-weight: 700; font-size: 0.9rem;
            display: flex; align-items: center; justify-content: center; flex-shrink: 0;
        }

        .step-line { width: 2px; flex: 1; background: rgba(15, 92, 92, 0.2); margin: 0.25rem 0; }
        .step-item:last-child .step-line { display: none; }
        .step-content { padding-bottom: 1.5rem; }
        .step-content h3 { font-size: 0.92rem; margin-bottom: 0.25rem; }
        .step-content p { font-size: 0.8rem; color: var(--text-light); line-height: 1.5; }

        /* ===== FAQ ===== */
        #faq { background: white; }

        /* ===== TESTIMONI ===== */
        #testimoni { background: var(--bg-light); }

        .testimonials-scroll {
            display: flex; gap: 1rem; overflow-x: auto; padding-bottom: 0.5rem;
            scrollbar-width: none; -ms-overflow-style: none;
        }
        .testimonials-scroll::-webkit-scrollbar { display: none; }

        .testimonial-card {
            background: white; padding: 1.3rem; border-radius: 20px;
            box-shadow: var(--shadow-sm); min-width: 270px; flex-shrink: 0;
        }

        .stars { color: var(--accent); font-size: 0.85rem; margin-bottom: 0.6rem; }

        .testimonial-text {
            font-style: italic; color: var(--text-light); margin-bottom: 1rem;
            font-size: 0.88rem; line-height: 1.5;
        }

        .testimonial-author { display: flex; align-items: center; gap: 0.75rem; }

        .author-avatar {
            width: 40px; height: 40px; background: var(--primary); border-radius: 50%;
            display: flex; align-items: center; justify-content: center; color: white;
            font-weight: bold; font-size: 0.85rem; flex-shrink: 0;
        }

        .author-name { font-size: 0.88rem; font-weight: 600; }
        .author-role { font-size: 0.75rem; color: var(--text-light); }

        /* ===== DOKUMENTASI ===== */
        #dokumentasi { background: white; }

        .doc-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 0.8rem;
        }

        .doc-placeholder {
            aspect-ratio: 1;
            background: linear-gradient(135deg, rgba(15,92,92,0.08), rgba(230,180,34,0.1));
            border-radius: 16px;
            border: 1px dashed rgba(15,92,92,0.25);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 0.4rem;
            color: var(--primary);
        }

        .doc-placeholder i { font-size: 1.4rem; }
        .doc-placeholder span { font-size: 0.68rem; color: var(--text-light); text-align: center; padding: 0 0.5rem; }

        /* ===== TENTANG IMTIYAZ ===== */
        #tentang { background: var(--bg-light); }

        .tentang-card {
            background: white;
            border-radius: 18px;
            border: 1px solid rgba(0,0,0,0.06);
            padding: 1.2rem;
            margin-bottom: 0.9rem;
        }

        .tentang-card h3 {
            font-size: 0.9rem;
            color: var(--primary);
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .tentang-card p, .tentang-card li {
            font-size: 0.8rem;
            color: var(--text-light);
            line-height: 1.55;
        }

        .tentang-card ul { padding-left: 1.1rem; }

        /* ===== FORM PENDAFTARAN ===== */
        #daftar { background: white; }

        .form-card {
            background: var(--bg-light);
            padding: 1.4rem 1.2rem;
            border-radius: 24px;
            border: 1px solid rgba(0,0,0,0.06);
        }

        .form-section-label {
            font-size: 0.78rem;
            font-weight: 700;
            color: var(--primary);
            text-transform: uppercase;
            letter-spacing: 0.04em;
            margin: 1.2rem 0 0.7rem;
            display: flex;
            align-items: center;
            gap: 0.4rem;
        }

        .form-section-label:first-child { margin-top: 0; }

        .form-group { margin-bottom: 0.9rem; }

        .form-label {
            display: block;
            font-size: 0.76rem;
            font-weight: 600;
            color: var(--text-light);
            margin-bottom: 0.3rem;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem 0.9rem;
            border: 1.5px solid #e2e8f0;
            border-radius: 14px;
            font-family: inherit;
            font-size: 0.92rem;
            transition: all 0.2s;
            background: white;
            color: var(--text);
            -webkit-appearance: none;
        }

        .form-group textarea { resize: vertical; min-height: 70px; }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--accent);
            box-shadow: 0 0 0 3px rgba(230, 180, 34, 0.15);
        }

        .check-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 0.5rem;
        }

        .check-option {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            background: white;
            border: 1.5px solid #e2e8f0;
            border-radius: 12px;
            padding: 0.6rem 0.7rem;
            font-size: 0.78rem;
            cursor: pointer;
        }

        .check-option input { width: auto; flex-shrink: 0; accent-color: var(--primary); }

        .radio-row {
            display: flex;
            gap: 0.5rem;
            flex-wrap: wrap;
        }

        .radio-option {
            display: flex;
            align-items: center;
            gap: 0.4rem;
            background: white;
            border: 1.5px solid #e2e8f0;
            border-radius: 100px;
            padding: 0.5rem 0.9rem;
            font-size: 0.78rem;
            cursor: pointer;
        }

        .radio-option input { accent-color: var(--primary); }

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
            margin-top: 0.9rem;
            transition: background 0.2s;
        }

        .btn-wa:hover { background: #1ebe5a; }

        /* ===== SUCCESS OVERLAY ===== */
        .success-overlay {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(15, 92, 92, 0.55);
            z-index: 200;
            align-items: center;
            justify-content: center;
            padding: 1.5rem;
        }

        .success-overlay.show { display: flex; }

        .success-card {
            background: white;
            border-radius: 24px;
            padding: 2rem 1.5rem;
            text-align: center;
            max-width: 380px;
            width: 100%;
        }

        .success-icon {
            font-size: 3rem;
            margin-bottom: 0.8rem;
        }

        .success-card h2 { font-size: 1.2rem; margin-bottom: 0.5rem; }
        .success-card p { font-size: 0.85rem; color: var(--text-light); margin-bottom: 1rem; line-height: 1.5; }

        .success-regno {
            background: var(--bg-light);
            border-radius: 12px;
            padding: 0.8rem;
            font-weight: 700;
            color: var(--primary);
            font-size: 0.95rem;
            margin-bottom: 1.2rem;
            letter-spacing: 0.02em;
        }

        /* ===== KONTAK & LOKASI ===== */
        #kontak { background: var(--bg-light); }

        .kontak-card {
            background: white;
            border-radius: 18px;
            border: 1px solid rgba(0,0,0,0.06);
            overflow: hidden;
            box-shadow: var(--shadow-sm);
        }

        .kontak-map { width: 100%; height: 180px; border: none; display: block; }

        .kontak-info { padding: 1.1rem; display: flex; flex-direction: column; gap: 0.8rem; }

        .kontak-row {
            display: flex;
            align-items: flex-start;
            gap: 0.8rem;
            text-decoration: none;
            color: var(--text);
        }

        .kontak-row .kontak-icon {
            width: 36px; height: 36px; border-radius: 10px;
            background: rgba(15, 92, 92, 0.08); color: var(--primary);
            display: flex; align-items: center; justify-content: center;
            flex-shrink: 0; font-size: 0.9rem;
        }

        .kontak-row .kontak-label { font-size: 0.7rem; color: var(--text-light); text-transform: uppercase; letter-spacing: 0.03em; }
        .kontak-row .kontak-value { font-size: 0.86rem; font-weight: 600; }

        /* ===== FOOTER ===== */
        footer {
            background: #1a2a2a;
            color: white;
            padding: 2rem 1.2rem 1.5rem;
            text-align: center;
        }

        .footer-logo-wrap {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            margin-bottom: 0.3rem;
        }

        .footer-logo-wrap img {
            height: 30px;
            width: 30px;
            object-fit: contain;
            border-radius: 8px;
            background: white;
            padding: 3px;
        }

        .footer-logo {
            font-size: 1.4rem;
            font-weight: 800;
            font-family: 'Plus Jakarta Sans', sans-serif;
        }

        .footer-tagline { color: rgba(255,255,255,0.5); font-size: 0.8rem; margin-bottom: 1.2rem; }

        .footer-links-row {
            display: flex; justify-content: center; gap: 1.2rem; flex-wrap: wrap; margin-bottom: 1.5rem;
        }
        .footer-links-row a { color: rgba(255,255,255,0.6); text-decoration: none; font-size: 0.8rem; }

        .footer-copy {
            font-size: 0.75rem; color: rgba(255,255,255,0.35);
            padding-top: 1.2rem; border-top: 1px solid rgba(255,255,255,0.1);
        }

        /* ===== WHATSAPP FLOAT ===== */
        .whatsapp-float {
            position: fixed; bottom: 84px; right: 16px; background: #25D366;
            width: 52px; height: 52px; border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            color: white; font-size: 1.6rem;
            box-shadow: 0 4px 16px rgba(37, 211, 102, 0.4);
            text-decoration: none; z-index: 99;
        }
    </style>
</head>
<body>

    <!-- TOP NAV -->
    <nav>
        <a href="#home" class="logo-nav">
            <img src="logo-imtiyaz.png" alt="Logo IMTIYAZ">
            <span>IMTI<em>YAZ</em></span>
        </a>
        <a href="#daftar" class="nav-daftar">Daftar</a>
    </nav>

    <!-- 1. HERO SECTION -->
    <section class="hero" id="home">
        <img src="logo-imtiyaz.png" alt="Logo IMTIYAZ" class="hero-logo">
        <div class="hero-badge">✨ Privat Quran & Akademik ke Rumah</div>
        <h1>Belajar Privat di Rumah Lebih Nyaman Bersama <span>IMTIYAZ PRIVATE</span></h1>
        <ul class="hero-points">
            <li><i class="fas fa-check-circle"></i> Guru datang ke rumah</li>
            <li><i class="fas fa-check-circle"></i> Bisa request ustadz/ustadzah</li>
            <li><i class="fas fa-check-circle"></i> Jadwal fleksibel</li>
            <li><i class="fas fa-check-circle"></i> Laporan perkembangan setiap bulan</li>
        </ul>
        <div class="hero-buttons">
            <a href="#daftar" class="btn btn-primary">✅ Daftar Sekarang</a>
            <a href="#harga" class="btn btn-outline">✅ Lihat Paket</a>
        </div>
        <div class="hero-stats">
            <div class="stat"><div class="stat-number">500+</div><div class="stat-label">Siswa</div></div>
            <div class="stat"><div class="stat-number">20+</div><div class="stat-label">Pengajar</div></div>
            <div class="stat"><div class="stat-number">98%</div><div class="stat-label">Puas</div></div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- 2. KENAPA MEMILIH IMTIYAZ -->
    <section id="keunggulan">
        <div class="container">
            <h2 class="section-title">Kenapa Memilih <span>IMTIYAZ?</span></h2>
            <p class="section-subtitle">Alasan orang tua percaya IMTIYAZ untuk anaknya</p>
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-house"></i></div>
                    <h3>Guru Datang ke Rumah</h3>
                    <p>Belajar lebih nyaman tanpa perlu keluar rumah.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-chalkboard-teacher"></i></div>
                    <h3>Pengajar Diseleksi</h3>
                    <p>Melalui proses seleksi ketat sebelum mengajar.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-book"></i></div>
                    <h3>Kurikulum Menyesuaikan</h3>
                    <p>Materi disesuaikan kebutuhan & kemampuan anak.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-chart-line"></i></div>
                    <h3>Laporan Perkembangan</h3>
                    <p>Orang tua dapat update perkembangan anak rutin.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-clock"></i></div>
                    <h3>Jadwal Fleksibel</h3>
                    <p>Bisa disesuaikan dengan waktu luang keluarga.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon"><i class="fas fa-people-arrows"></i></div>
                    <h3>Admin Siap Membantu</h3>
                    <p>Respon cepat untuk semua pertanyaan orang tua.</p>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- 3. PROGRAM YANG TERSEDIA -->
    <section id="program-list">
        <div class="container">
            <h2 class="section-title">Program yang <span>Tersedia</span></h2>
            <p class="section-subtitle">Ketuk salah satu program untuk lihat penjelasan</p>
            <div class="acc-list">
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-book-quran"></i></div>
                        <span class="acc-title">Privat Mengaji</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body">
                        <p>Belajar membaca Al-Qur'an dari dasar (Iqra) hingga Al-Qur'an, dibimbing langsung oleh pengajar berpengalaman.</p>
                    </div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-microphone-lines"></i></div>
                        <span class="acc-title">Tahsin</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body">
                        <p>Memperbaiki bacaan Al-Qur'an sesuai kaidah tajwid dan makhraj huruf yang benar.</p>
                    </div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-brain"></i></div>
                        <span class="acc-title">Tahfidz</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body">
                        <p>Program menghafal Al-Qur'an dengan metode muraja'ah dan bimbingan hafalan bertahap.</p>
                    </div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-pen"></i></div>
                        <span class="acc-title">Calistung</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body">
                        <p>Belajar membaca, menulis, dan berhitung untuk anak usia dini.</p>
                    </div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-mosque"></i></div>
                        <span class="acc-title">Bahasa Arab</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body">
                        <p>Belajar nahwu, sharaf, dan percakapan bahasa Arab sehari-hari.</p>
                    </div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-calculator"></i></div>
                        <span class="acc-title">Matematika</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body">
                        <p>Bimbingan matematika sesuai kurikulum sekolah, dari dasar hingga lanjutan.</p>
                    </div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-globe"></i></div>
                        <span class="acc-title">Bahasa Inggris</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body">
                        <p>Belajar speaking, grammar, dan persiapan ujian bahasa Inggris.</p>
                    </div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-graduation-cap"></i></div>
                        <span class="acc-title">Semua Mata Pelajaran Sekolah</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body">
                        <p>Bimbingan untuk semua mata pelajaran SD, SMP, dan SMA sesuai kebutuhan siswa.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- 4. PAKET & HARGA -->
    <section id="harga">
        <div class="container">
            <h2 class="section-title">Paket <span>& Harga</span></h2>
            <p class="section-subtitle">Ketuk tiap kategori untuk lihat rincian paket & harga</p>
            <div class="programs-grid">

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
                                    <thead><tr><th>Paket</th><th>Calistung & Iqra<br>1 jam</th><th>Calistung & Iqra<br>1&frac12; jam</th></tr></thead>
                                    <tbody>
                                        <tr><th>Durasi sesi</th><td>1&ndash;2 Murid<br>(kakak beradik)</td><td>3&ndash;5 Murid<br>(kelompok)</td></tr>
                                        <tr><th>8 Pertemuan</th><td>Rp 280.000 &ndash; 300.000</td><td>Rp 350.000</td></tr>
                                        <tr><th>12 Pertemuan</th><td>Rp 420.000 &ndash; 440.000</td><td>Rp 510.000</td></tr>
                                        <tr><th>16 Pertemuan</th><td>Rp 560.000 &ndash; 580.000</td><td>Rp 700.000</td></tr>
                                    </tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                </div>

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
                                    <thead><tr><th>Paket</th><th>Tahfiz & Tahsin<br>1 jam</th><th>Tahfiz & Tahsin<br>1&frac12; jam</th></tr></thead>
                                    <tbody>
                                        <tr><th>Durasi sesi</th><td>1&ndash;2 Murid<br>(kakak beradik)</td><td>3&ndash;5 Murid<br>(kelompok)</td></tr>
                                        <tr><th>8 Pertemuan</th><td>Rp 280.000 &ndash; 300.000</td><td>Rp 350.000</td></tr>
                                        <tr><th>12 Pertemuan</th><td>Rp 420.000 &ndash; 440.000</td><td>Rp 510.000</td></tr>
                                        <tr><th>16 Pertemuan</th><td>Rp 560.000 &ndash; 580.000</td><td>Rp 700.000</td></tr>
                                    </tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                </div>

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
                                    <thead><tr><th>Paket</th><th>TK/SD</th><th>SMP</th><th>SMA</th></tr></thead>
                                    <tbody>
                                        <tr><th>4 pertemuan</th><td>Rp 180.000</td><td>Rp 220.000</td><td>Rp 260.000</td></tr>
                                        <tr><th>6 pertemuan</th><td>Rp 270.000</td><td>Rp 330.000</td><td>Rp 390.000</td></tr>
                                        <tr><th>8 pertemuan</th><td>Rp 360.000</td><td>Rp 440.000</td><td>Rp 520.000</td></tr>
                                        <tr><th>12 pertemuan</th><td>Rp 540.000</td><td>Rp 660.000</td><td>Rp 700.000</td></tr>
                                        <tr><th>16 pertemuan</th><td>Rp 720.000</td><td>Rp 880.000</td><td>Rp 1.000.000</td></tr>
                                    </tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="price-item">
                    <button class="price-header" onclick="togglePrice(this)">
                        <div class="program-icon">📖</div>
                        <div class="price-header-info">
                            <h3>Mapel Umum</h3>
                            <p>SD, SMP, SMA &mdash; semua mata pelajaran</p>
                        </div>
                        <i class="fas fa-chevron-down price-arrow"></i>
                    </button>
                    <div class="price-body">
                        <div class="price-body-inner">
                            <div class="price-table-scroll">
                                <table class="price-table">
                                    <thead><tr><th>Paket</th><th>SD<br>(Kelas 1-3)</th><th>SD<br>(Kelas 4-6)</th><th>SMP</th><th>SMA</th></tr></thead>
                                    <tbody>
                                        <tr><th>4 Pertemuan</th><td>&ndash;</td><td>Rp 160.000</td><td>Rp 180.000</td><td>Rp 200.000</td></tr>
                                        <tr><th>6 Pertemuan</th><td>&ndash;</td><td>Rp 240.000</td><td>Rp 270.000</td><td>Rp 300.000</td></tr>
                                        <tr><th>8 Pertemuan</th><td>Rp 280.000</td><td>Rp 320.000</td><td>Rp 360.000</td><td>Rp 400.000</td></tr>
                                        <tr><th>12 Pertemuan</th><td>Rp 420.000</td><td>Rp 480.000</td><td>Rp 540.000</td><td>Rp 600.000</td></tr>
                                        <tr><th>16 Pertemuan</th><td>Rp 560.000</td><td>Rp 640.000</td><td>Rp 720.000</td><td>Rp 800.000</td></tr>
                                    </tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                </div>

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
                                    <thead><tr><th>Paket</th><th>Tilawah (3&ndash;5 Murid)</th></tr></thead>
                                    <tbody>
                                        <tr><th>8 Pertemuan</th><td>Rp 400.000</td></tr>
                                        <tr><th>12 Pertemuan</th><td>Rp 600.000</td></tr>
                                        <tr><th>16 Pertemuan</th><td>Rp 800.000</td></tr>
                                    </tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                </div>

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
                                    <thead><tr><th>Spesial</th><th>Detail</th></tr></thead>
                                    <tbody>
                                        <tr><th>ABK Shadow Teacher</th><td>Rp 900.000 / bulan</td></tr>
                                        <tr><th>Privat Khusus ABK</th><td>Diskusi dulu nanti</td></tr>
                                    </tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                </div>

            </div>

            <div class="harga-notes">
                <h3>Yang Perlu Diketahui</h3>
                <ul>
                    <li><i class="fas fa-check"></i> Harga sudah termasuk guru datang ke rumah.</li>
                    <li><i class="fas fa-check"></i> Bisa memilih ustadz atau ustadzah.</li>
                    <li><i class="fas fa-check"></i> Jadwal fleksibel.</li>
                    <li><i class="fas fa-check"></i> Bisa ganti jadwal sesuai ketentuan yang berlaku.</li>
                </ul>
                <p class="harga-transport">*Untuk area tertentu di luar jangkauan standar, mungkin ada biaya transport tambahan &mdash; akan diinfokan admin saat konfirmasi pendaftaran.</p>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- 5. ALUR PENDAFTARAN -->
    <section id="alur">
        <div class="container">
            <h2 class="section-title">Alur <span>Pendaftaran</span></h2>
            <div class="steps-list">
                <div class="step-item">
                    <div class="step-marker"><div class="step-number">1</div><div class="step-line"></div></div>
                    <div class="step-content"><h3>Isi Formulir</h3><p>Lengkapi data orang tua, anak, dan kebutuhan belajar.</p></div>
                </div>
                <div class="step-item">
                    <div class="step-marker"><div class="step-number">2</div><div class="step-line"></div></div>
                    <div class="step-content"><h3>Admin Verifikasi</h3><p>Tim admin memeriksa dan mengonfirmasi data pendaftaran.</p></div>
                </div>
                <div class="step-item">
                    <div class="step-marker"><div class="step-number">3</div><div class="step-line"></div></div>
                    <div class="step-content"><h3>Pilih Paket</h3><p>Menentukan paket pertemuan sesuai kebutuhan & budget.</p></div>
                </div>
                <div class="step-item">
                    <div class="step-marker"><div class="step-number">4</div><div class="step-line"></div></div>
                    <div class="step-content"><h3>Penentuan Pengajar</h3><p>Admin mencocokkan pengajar sesuai preferensi & lokasi.</p></div>
                </div>
                <div class="step-item">
                    <div class="step-marker"><div class="step-number">5</div></div>
                    <div class="step-content"><h3>Mulai Belajar</h3><p>Siswa mulai sesi belajar privat sesuai jadwal yang disepakati.</p></div>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- 6. FAQ -->
    <section id="faq">
        <div class="container">
            <h2 class="section-title">Pertanyaan <span>Umum</span></h2>
            <p class="section-subtitle">Semoga bisa jawab pertanyaanmu sebelum chat admin</p>
            <div class="acc-list">
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-house"></i></div>
                        <span class="acc-title">Apakah guru datang ke rumah?</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body"><p>Ya, pengajar IMTIYAZ datang langsung ke rumah siswa.</p></div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-user-check"></i></div>
                        <span class="acc-title">Bisa request ustadz atau ustadzah?</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body"><p>Bisa, tinggal pilih preferensi pengajar saat mengisi formulir pendaftaran.</p></div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-moon"></i></div>
                        <span class="acc-title">Jadwal bisa malam?</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body"><p>Bisa, selama jadwal pengajar masih tersedia di jam tersebut.</p></div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-rotate"></i></div>
                        <span class="acc-title">Kalau pengajar tidak cocok?</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body"><p>Bisa konsultasi dengan admin untuk penggantian pengajar.</p></div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-money-bill-wave"></i></div>
                        <span class="acc-title">Pembayaran bagaimana?</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body"><p>Transfer ke rekening resmi IMTIYAZ. Detail rekening akan diinfokan admin saat konfirmasi.</p></div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-file-invoice"></i></div>
                        <span class="acc-title">Apakah ada biaya pendaftaran?</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body"><p>Biaya pendaftaran hanya dikenakan satu kali dengan nominal yang sangat terjangkau untuk proses administrasi dan penempatan pengajar.</p></div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-user-group"></i></div>
                        <span class="acc-title">Apakah bisa belajar 2 bersaudara?</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body"><p>Bisa, tersedia paket khusus kakak beradik (1&ndash;2 murid) dengan harga lebih hemat.</p></div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-hourglass-half"></i></div>
                        <span class="acc-title">Berapa lama satu pertemuan?</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body"><p>Umumnya 60&ndash;90 menit per pertemuan, tergantung program dan paket yang dipilih.</p></div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-laptop"></i></div>
                        <span class="acc-title">Bisa belajar online?</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body"><p>Fokus utama IMTIYAZ adalah privat ke rumah, namun sesi online bisa didiskusikan dengan admin sesuai kondisi.</p></div>
                </div>
                <div class="acc-item">
                    <button class="acc-header" onclick="toggleAcc(this)">
                        <div class="acc-icon"><i class="fas fa-map-location-dot"></i></div>
                        <span class="acc-title">Wilayah layanan?</span>
                        <i class="fas fa-chevron-down acc-arrow"></i>
                    </button>
                    <div class="acc-body"><p>Saat ini IMTIYAZ melayani area Banda Aceh dan sekitarnya. Konfirmasikan alamat lengkap ke admin untuk memastikan jangkauan.</p></div>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- 7. TESTIMONI -->
    <section id="testimoni">
        <div class="container">
            <h2 class="section-title">Apa Kata <span>Mereka?</span></h2>
            <div class="testimonials-scroll">
                <div class="testimonial-card">
                    <div class="stars">★★★★★</div>
                    <p class="testimonial-text">"Alhamdulillah anak saya sekarang semangat mengaji. Pengajarnya sabar dan ramah."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">SR</div>
                        <div><div class="author-name">Siti Rahmawati</div><div class="author-role">Orang Tua Siswa</div></div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="stars">★★★★★</div>
                    <p class="testimonial-text">"Program tahfidz sangat membantu. Anak saya jadi lebih lancar membaca Al-Qur'an dengan tajwid yang benar."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">AH</div>
                        <div><div class="author-name">Ahmad Hidayat</div><div class="author-role">Orang Tua Siswa</div></div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="stars">★★★★★</div>
                    <p class="testimonial-text">"Belajar Bahasa Inggris di sini seru! Sekarang saya lebih percaya diri speaking di sekolah."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">FZ</div>
                        <div><div class="author-name">Fatimah Az-Zahra</div><div class="author-role">Siswa SMA</div></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- 8. DOKUMENTASI -->
    <section id="dokumentasi">
        <div class="container">
            <h2 class="section-title">Dokumentasi <span>Kegiatan</span></h2>
            <p class="section-subtitle">Foto kegiatan belajar bersama IMTIYAZ</p>
            <div class="doc-grid">
                <div class="doc-placeholder"><i class="fas fa-camera"></i><span>Foto kegiatan mengaji</span></div>
                <div class="doc-placeholder"><i class="fas fa-camera"></i><span>Foto sesi belajar akademik</span></div>
                <div class="doc-placeholder"><i class="fas fa-camera"></i><span>Foto kegiatan tahfidz</span></div>
                <div class="doc-placeholder"><i class="fas fa-camera"></i><span>Foto bersama siswa</span></div>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- 9. TENTANG IMTIYAZ -->
    <section id="tentang">
        <div class="container">
            <h2 class="section-title">Tentang <span>IMTIYAZ</span></h2>
            <div class="tentang-card">
                <h3><i class="fas fa-eye"></i> Visi</h3>
                <p>Menjadi lembaga bimbingan belajar privat Quran dan akademik terpercaya di Banda Aceh yang mengantarkan setiap anak meraih prestasi dengan akhlak mulia.</p>
            </div>
            <div class="tentang-card">
                <h3><i class="fas fa-bullseye"></i> Misi</h3>
                <ul>
                    <li>Menyediakan pengajar yang kompeten dan berakhlak baik.</li>
                    <li>Memberikan metode belajar personal sesuai kebutuhan anak.</li>
                    <li>Membangun kedekatan antara siswa, orang tua, dan pengajar.</li>
                </ul>
            </div>
            <div class="tentang-card">
                <h3><i class="fas fa-file-shield"></i> Legalitas</h3>
                <p>Informasi legalitas / izin usaha IMTIYAZ akan dicantumkan di sini.</p>
            </div>
        </div>
    </section>

    <div class="section-divider"></div>

    <!-- 10. FORMULIR PENDAFTARAN -->
    <section id="daftar">
        <div class="container">
            <div class="form-card">
                <h2 class="section-title" style="margin-bottom:1.2rem;">Formulir <span>Pendaftaran</span></h2>
                <form id="registerForm">

                    <div class="form-section-label"><i class="fas fa-user"></i> Data Orang Tua</div>
                    <div class="form-group">
                        <label class="form-label" for="ortuNama">Nama Orang Tua</label>
                        <input type="text" id="ortuNama" placeholder="Masukkan nama lengkap" required>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="ortuWa">Nomor WhatsApp</label>
                        <input type="tel" id="ortuWa" placeholder="Contoh: 08123456789" required>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="ortuEmail">Email (opsional)</label>
                        <input type="email" id="ortuEmail" placeholder="nama@email.com">
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="ortuAlamat">Alamat Lengkap</label>
                        <textarea id="ortuAlamat" placeholder="Nama jalan, desa/kelurahan, kecamatan" required></textarea>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="ortuMaps">Link Google Maps Lokasi (opsional)</label>
                        <input type="url" id="ortuMaps" placeholder="Tempel link Google Maps di sini">
                    </div>

                    <div class="form-section-label"><i class="fas fa-child"></i> Data Anak</div>
                    <div class="form-group">
                        <label class="form-label" for="anakNama">Nama Anak</label>
                        <input type="text" id="anakNama" placeholder="Masukkan nama lengkap anak" required>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="anakGender">Jenis Kelamin</label>
                        <select id="anakGender" required>
                            <option value="">Pilih jenis kelamin</option>
                            <option value="Laki-laki">Laki-laki</option>
                            <option value="Perempuan">Perempuan</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="anakUsia">Usia</label>
                        <input type="number" id="anakUsia" min="1" max="25" placeholder="Contoh: 8" required>
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="anakSekolah">Sekolah</label>
                        <input type="text" id="anakSekolah" placeholder="Nama sekolah">
                    </div>
                    <div class="form-group">
                        <label class="form-label" for="anakKelas">Kelas</label>
                        <input type="text" id="anakKelas" placeholder="Contoh: Kelas 3 SD">
                    </div>

                    <div class="form-section-label"><i class="fas fa-list-check"></i> Kebutuhan Belajar</div>
                    <div class="form-group">
                        <div class="check-grid">
                            <label class="check-option"><input type="checkbox" name="kebutuhan" value="Mengaji"> Mengaji</label>
                            <label class="check-option"><input type="checkbox" name="kebutuhan" value="Tahsin"> Tahsin</label>
                            <label class="check-option"><input type="checkbox" name="kebutuhan" value="Tahfidz"> Tahfidz</label>
                            <label class="check-option"><input type="checkbox" name="kebutuhan" value="Calistung"> Calistung</label>
                            <label class="check-option"><input type="checkbox" name="kebutuhan" value="Matematika"> Matematika</label>
                            <label class="check-option"><input type="checkbox" name="kebutuhan" value="Bahasa Inggris"> B. Inggris</label>
                            <label class="check-option"><input type="checkbox" name="kebutuhan" value="Bahasa Arab"> B. Arab</label>
                            <label class="check-option"><input type="checkbox" name="kebutuhan" value="Semua Mapel"> Semua Mapel</label>
                        </div>
                    </div>

                    <div class="form-section-label"><i class="fas fa-user-tie"></i> Preferensi Pengajar</div>
                    <div class="form-group">
                        <div class="radio-row">
                            <label class="radio-option"><input type="radio" name="preferensi" value="Ustadz" required> Ustadz</label>
                            <label class="radio-option"><input type="radio" name="preferensi" value="Ustadzah"> Ustadzah</label>
                            <label class="radio-option"><input type="radio" name="preferensi" value="Tidak masalah"> Tidak masalah</label>
                        </div>
                    </div>

                    <div class="form-section-label"><i class="fas fa-calendar-days"></i> Hari yang Diinginkan</div>
                    <div class="form-group">
                        <label class="form-label" for="hariDiinginkan">Tulis hari yang diinginkan</label>
                        <input type="text" id="hariDiinginkan" placeholder="Contoh: Senin, Rabu, Jumat / Fleksibel kapan saja" required>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="jamDiinginkan">Jam yang Diinginkan</label>
                        <input type="text" id="jamDiinginkan" placeholder="Contoh: 16.00 - 17.30 atau malam sekitar jam 8" required>
                    </div>

                    <div class="form-section-label"><i class="fas fa-box"></i> Paket yang Dipilih</div>
                    <div class="form-group">
                        <select id="paketDipilih" required>
                            <option value="">Pilih paket</option>
                            <option value="Paket 8x Pertemuan">Paket 8x Pertemuan</option>
                            <option value="Paket 12x Pertemuan">Paket 12x Pertemuan</option>
                            <option value="Paket 16x Pertemuan">Paket 16x Pertemuan</option>
                            <option value="Belum yakin, konsultasi dulu">Belum yakin, konsultasi dulu</option>
                        </select>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="catatan">Catatan Tambahan</label>
                        <textarea id="catatan" placeholder="Tulis catatan tambahan jika ada"></textarea>
                    </div>

                    <button type="submit" class="btn-wa">
                        <i class="fab fa-whatsapp"></i> Daftar Sekarang
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
                <div class="kontak-info">
                    <a href="tel:+6285373842629" class="kontak-row">
                        <div class="kontak-icon"><i class="fas fa-phone"></i></div>
                        <div><div class="kontak-label">Telepon</div><div class="kontak-value">+62 853-7384-2629</div></div>
                    </a>
                    <a href="https://wa.me/6285373842629" target="_blank" class="kontak-row">
                        <div class="kontak-icon"><i class="fab fa-whatsapp"></i></div>
                        <div><div class="kontak-label">WhatsApp</div><div class="kontak-value">Chat Sekarang</div></div>
                    </a>
                    <a href="mailto:privateimtiyaz@gmail.com" class="kontak-row">
                        <div class="kontak-icon"><i class="fas fa-envelope"></i></div>
                        <div><div class="kontak-label">Email</div><div class="kontak-value">privateimtiyaz@gmail.com</div></div>
                    </a>
                    <a href="https://instagram.com/imtiyaz.private" target="_blank" class="kontak-row">
                        <div class="kontak-icon"><i class="fab fa-instagram"></i></div>
                        <div><div class="kontak-label">Instagram</div><div class="kontak-value">@imtiyaz.private</div></div>
                    </a>
                    <div class="kontak-row">
                        <div class="kontak-icon"><i class="fas fa-map-marker-alt"></i></div>
                        <div><div class="kontak-label">Alamat Kantor</div><div class="kontak-value">Jl. Prada Utama, Lamgugob, Kec. Syiah Kuala, Banda Aceh 24415</div></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="footer-logo-wrap">
            <img src="logo-imtiyaz.png" alt="Logo IMTIYAZ">
            <div class="footer-logo">IMTI<span style="color: var(--accent);">YAZ</span></div>
        </div>
        <p class="footer-tagline">Quranic & Academic Tutoring · Banda Aceh</p>
        <div class="footer-links-row">
            <a href="#program-list">Program</a>
            <a href="#harga">Harga</a>
            <a href="#faq">FAQ</a>
            <a href="#kontak">Kontak</a>
        </div>
        <div class="footer-copy">© 2026 IMTIYAZ. All rights reserved.</div>
    </footer>

    <!-- WHATSAPP FLOAT -->
    <a href="https://wa.me/6285373842629" class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <!-- BOTTOM NAV -->
    <div class="bottom-nav">
        <a href="#home" class="active"><i class="fas fa-home"></i><span>Beranda</span></a>
        <a href="#program-list"><i class="fas fa-book-open"></i><span>Program</span></a>
        <a href="#harga"><i class="fas fa-tags"></i><span>Harga</span></a>
        <a href="#daftar"><i class="fas fa-user-plus"></i><span>Daftar</span></a>
        <a href="#kontak"><i class="fas fa-map-marker-alt"></i><span>Kontak</span></a>
    </div>

    <!-- SUCCESS OVERLAY -->
    <div class="success-overlay" id="successOverlay">
        <div class="success-card">
            <div class="success-icon">🎉</div>
            <h2>Alhamdulillah!</h2>
            <p>Pendaftaran Anda berhasil dikirim. Silakan tunggu konfirmasi admin maksimal 1&times;24 jam.</p>
            <div class="success-regno" id="regNoDisplay">Nomor pendaftaran: IP-00000000-000</div>
            <button class="btn btn-primary" style="width:100%; border:none;" onclick="document.getElementById('successOverlay').classList.remove('show')">Tutup</button>
        </div>
    </div>

    <script>
        // Toggle accordion generik (Program List & FAQ)
        function toggleAcc(headerEl) {
            const item = headerEl.closest('.acc-item');
            const wasOpen = item.classList.contains('open');
            document.querySelectorAll('.acc-item.open').forEach(el => el.classList.remove('open'));
            if (!wasOpen) item.classList.add('open');
        }

        // Toggle accordion daftar harga
        function togglePrice(headerEl) {
            const item = headerEl.closest('.price-item');
            const wasOpen = item.classList.contains('open');
            document.querySelectorAll('.price-item.open').forEach(el => el.classList.remove('open'));
            if (!wasOpen) item.classList.add('open');
        }

        // Generate nomor pendaftaran: IP-YYYYMMDD-XXX
        function generateRegNo() {
            const now = new Date();
            const y = now.getFullYear();
            const m = String(now.getMonth() + 1).padStart(2, '0');
            const d = String(now.getDate()).padStart(2, '0');
            const rand = String(Math.floor(Math.random() * 900) + 100);
            return `IP-${y}${m}${d}-${rand}`;
        }

        // Form submission → WhatsApp + Success overlay
        const form = document.getElementById('registerForm');
        form.addEventListener('submit', (e) => {
            e.preventDefault();

            const ortuNama = document.getElementById('ortuNama').value.trim();
            const ortuWa = document.getElementById('ortuWa').value.trim();
            const ortuEmail = document.getElementById('ortuEmail').value.trim();
            const ortuAlamat = document.getElementById('ortuAlamat').value.trim();
            const ortuMaps = document.getElementById('ortuMaps').value.trim();

            const anakNama = document.getElementById('anakNama').value.trim();
            const anakGender = document.getElementById('anakGender').value;
            const anakUsia = document.getElementById('anakUsia').value.trim();
            const anakSekolah = document.getElementById('anakSekolah').value.trim();
            const anakKelas = document.getElementById('anakKelas').value.trim();

            const kebutuhan = Array.from(document.querySelectorAll('input[name="kebutuhan"]:checked')).map(el => el.value);
            const preferensiEl = document.querySelector('input[name="preferensi"]:checked');
            const hariDiinginkan = document.getElementById('hariDiinginkan').value.trim();
            const jamDiinginkan = document.getElementById('jamDiinginkan').value;
            const paketDipilih = document.getElementById('paketDipilih').value;
            const catatan = document.getElementById('catatan').value.trim();

            if (!ortuNama || !ortuWa || !ortuAlamat || !anakNama || !anakGender || !anakUsia || !preferensiEl || !hariDiinginkan || !jamDiinginkan || !paketDipilih) {
                alert('Mohon lengkapi semua data yang wajib diisi!');
                return;
            }

            const regNo = generateRegNo();

            let message = `Halo IMTIYAZ, saya ingin mendaftar:%0A%0A`;
            message += `*Nomor Pendaftaran:* ${regNo}%0A%0A`;
            message += `*--- Data Orang Tua ---*%0A`;
            message += `Nama: ${encodeURIComponent(ortuNama)}%0A`;
            message += `WhatsApp: ${encodeURIComponent(ortuWa)}%0A`;
            if (ortuEmail) message += `Email: ${encodeURIComponent(ortuEmail)}%0A`;
            message += `Alamat: ${encodeURIComponent(ortuAlamat)}%0A`;
            if (ortuMaps) message += `Lokasi Maps: ${encodeURIComponent(ortuMaps)}%0A`;
            message += `%0A*--- Data Anak ---*%0A`;
            message += `Nama: ${encodeURIComponent(anakNama)}%0A`;
            message += `Jenis Kelamin: ${encodeURIComponent(anakGender)}%0A`;
            message += `Usia: ${encodeURIComponent(anakUsia)}%0A`;
            if (anakSekolah) message += `Sekolah: ${encodeURIComponent(anakSekolah)}%0A`;
            if (anakKelas) message += `Kelas: ${encodeURIComponent(anakKelas)}%0A`;
            message += `%0A*--- Kebutuhan Belajar ---*%0A`;
            message += `${kebutuhan.length ? encodeURIComponent(kebutuhan.join(', ')) : '-'}%0A`;
            message += `%0A*Preferensi Pengajar:* ${encodeURIComponent(preferensiEl.value)}%0A`;
            message += `*Hari Diinginkan:* ${hariDiinginkan ? encodeURIComponent(hariDiinginkan) : '-'}%0A`;
            message += `*Jam Diinginkan:* ${encodeURIComponent(jamDiinginkan)}%0A`;
            message += `*Paket Dipilih:* ${encodeURIComponent(paketDipilih)}%0A`;
            if (catatan) message += `*Catatan:* ${encodeURIComponent(catatan)}%0A`;
            message += `%0AMohon info lebih lanjut. Terima kasih.`;

            window.open(`https://wa.me/6285373842629?text=${message}`, '_blank');

            document.getElementById('regNoDisplay').textContent = `Nomor pendaftaran: ${regNo}`;
            document.getElementById('successOverlay').classList.add('show');

            form.reset();
        });

        // Active bottom nav on scroll
        const sections = document.querySelectorAll('section[id]');
        const navLinks = document.querySelectorAll('.bottom-nav a');

        window.addEventListener('scroll', () => {
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop - 100;
                if (pageYOffset >= sectionTop) current = section.getAttribute('id');
            });
            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === '#' + current) link.classList.add('active');
            });
        });
    </script>
</body>
</html>
