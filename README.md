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
            font-size: 0.65rem;
            font-weight: 500;
            transition: color 0.2s;
            flex: 1;
        }

        .bottom-nav a i {
            font-size: 1.2rem;
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

        /* ===== PROGRAM CARDS ===== */
        #program {
            background: white;
        }

        .programs-grid {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .program-card {
            background: var(--bg-light);
            padding: 1.2rem;
            border-radius: 20px;
            border: 1px solid rgba(0,0,0,0.06);
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .program-icon {
            font-size: 2.2rem;
            flex-shrink: 0;
            width: 52px;
            height: 52px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: white;
            border-radius: 14px;
            box-shadow: var(--shadow-sm);
        }

        .program-info {
            flex: 1;
        }

        .program-card h3 {
            font-size: 1rem;
            margin-bottom: 0.2rem;
        }

        .program-card p {
            color: var(--text-light);
            font-size: 0.8rem;
            margin-bottom: 0.4rem;
        }

        .program-price {
            font-size: 1rem;
            font-weight: 800;
            color: var(--primary);
        }

        .program-arrow {
            color: var(--primary);
            font-size: 1.2rem;
            flex-shrink: 0;
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
        <div class="hero-badge">✨ Privat Quran & Akademik</div>
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

    <!-- PROGRAM -->
    <section id="program">
        <div class="container">
            <h2 class="section-title">Program <span>Unggulan</span></h2>
            <div class="programs-grid">
                <a href="#daftar" class="program-card" style="text-decoration:none; color:inherit;">
                    <div class="program-icon">📚</div>
                    <div class="program-info">
                        <h3>Calistung</h3>
                        <p>Baca, tulis, hitung untuk anak usia dini</p>
                        <div class="program-price">Rp35K / sesi</div>
                    </div>
                    <i class="fas fa-chevron-right program-arrow"></i>
                </a>
                <a href="#daftar" class="program-card" style="text-decoration:none; color:inherit;">
                    <div class="program-icon">📿</div>
                    <div class="program-info">
                        <h3>Mengaji & Tahfidz</h3>
                        <p>Tajwid, makhraj, dan hafalan Al-Qur'an</p>
                        <div class="program-price">Rp35K – 50K / sesi</div>
                    </div>
                    <i class="fas fa-chevron-right program-arrow"></i>
                </a>
                <a href="#daftar" class="program-card" style="text-decoration:none; color:inherit;">
                    <div class="program-icon">🕌</div>
                    <div class="program-info">
                        <h3>Bahasa Arab</h3>
                        <p>Nahwu, sharaf, dan percakapan sehari-hari</p>
                        <div class="program-price">Rp55K – 70K / sesi</div>
                    </div>
                    <i class="fas fa-chevron-right program-arrow"></i>
                </a>
                <a href="#daftar" class="program-card" style="text-decoration:none; color:inherit;">
                    <div class="program-icon">🌍</div>
                    <div class="program-info">
                        <h3>Bahasa Inggris</h3>
                        <p>Speaking, grammar, persiapan TOEFL</p>
                        <div class="program-price">Rp55K – 70K / sesi</div>
                    </div>
                    <i class="fas fa-chevron-right program-arrow"></i>
                </a>
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

    <!-- FOOTER -->
    <footer>
        <div class="footer-logo">IMTI<span style="color: var(--accent);">YAZ</span></div>
        <p class="footer-tagline">Quranic & Academic Tutoring · Banda Aceh</p>
        <div class="footer-contact">
            <a href="tel:087754721634"><i class="fas fa-phone"></i> 0877 5472 1634</a>
            <a href="mailto:privateimtiyaz@gmail.com"><i class="fas fa-envelope"></i> privateimtiyaz@gmail.com</a>
            <a href="https://wa.me/6287754721634" target="_blank"><i class="fab fa-whatsapp"></i> Chat WhatsApp</a>
        </div>
        <div class="footer-links-row">
            <a href="#program">Calistung</a>
            <a href="#program">Mengaji</a>
            <a href="#program">Bahasa Arab</a>
            <a href="#program">Bahasa Inggris</a>
        </div>
        <div class="footer-copy">© 2026 IMTIYAZ. All rights reserved.</div>
    </footer>

    <!-- WHATSAPP FLOAT -->
    <a href="https://wa.me/6287754721634" class="whatsapp-float" target="_blank">
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
    </div>

    <script>
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
            window.open(`https://wa.me/6287754721634?text=${message}`, '_blank');
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
