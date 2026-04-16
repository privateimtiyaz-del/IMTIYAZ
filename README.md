<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IMTIYAZ - Bimbel Quran & Akademik</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
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
            --shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.08);
            --shadow-sm: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        body {
            font-family: 'Inter', sans-serif;
            color: var(--text);
            background: var(--bg-light);
            line-height: 1.5;
        }

        h1, h2, h3, h4 {
            font-family: 'Plus Jakarta Sans', sans-serif;
            font-weight: 700;
            letter-spacing: -0.02em;
        }

        /* Navigation - Simple */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(12px);
            z-index: 100;
            padding: 1rem 0;
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.6rem;
            font-weight: 800;
            color: var(--primary);
            text-decoration: none;
        }

        .logo span {
            color: var(--accent);
        }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text);
            font-weight: 500;
            font-size: 0.9rem;
            transition: color 0.2s;
        }

        .nav-links a:hover {
            color: var(--accent);
        }

        .btn-nav {
            background: var(--primary);
            color: white !important;
            padding: 0.5rem 1.2rem;
            border-radius: 100px;
        }

        .btn-nav:hover {
            background: var(--primary-dark);
        }

        /* Mobile Menu */
        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section - Clean */
        .hero {
            min-height: 85vh;
            display: flex;
            align-items: center;
            padding: 7rem 2rem 4rem;
            background: linear-gradient(135deg, #f8f3e8 0%, #fff 100%);
        }

        .hero-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            align-items: center;
        }

        .hero-content h1 {
            font-size: 3rem;
            line-height: 1.2;
            margin-bottom: 1.2rem;
        }

        .hero-content h1 span {
            color: var(--accent);
        }

        .hero-content p {
            font-size: 1.1rem;
            color: var(--text-light);
            margin-bottom: 2rem;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .btn {
            padding: 0.9rem 2rem;
            border-radius: 100px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.2s;
            display: inline-block;
            font-size: 0.95rem;
        }

        .btn-primary {
            background: var(--primary);
            color: white;
        }

        .btn-primary:hover {
            background: var(--primary-dark);
            transform: translateY(-2px);
        }

        .btn-outline {
            border: 2px solid var(--primary);
            color: var(--primary);
        }

        .btn-outline:hover {
            background: var(--primary);
            color: white;
        }

        .hero-stats {
            display: flex;
            gap: 2rem;
            margin-top: 2.5rem;
        }

        .stat {
            text-align: left;
        }

        .stat-number {
            font-size: 1.8rem;
            font-weight: 800;
            color: var(--primary);
        }

        .hero-image img {
            width: 100%;
            max-width: 450px;
            border-radius: 32px;
        }

        /* Section Umum */
        section {
            padding: 5rem 2rem;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2rem;
            margin-bottom: 3rem;
        }

        .section-title span {
            color: var(--accent);
        }

        /* Program Cards - Simple */
        .programs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 1.8rem;
        }

        .program-card {
            background: var(--white);
            padding: 2rem;
            border-radius: 24px;
            box-shadow: var(--shadow-sm);
            transition: all 0.3s;
            text-align: center;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .program-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow);
        }

        .program-icon {
            font-size: 2.8rem;
            margin-bottom: 1rem;
        }

        .program-card h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
        }

        .program-card p {
            color: var(--text-light);
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        .program-price {
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--primary);
            margin: 1rem 0;
        }

        /* Testimoni - Minimal */
        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .testimonial-card {
            background: var(--white);
            padding: 2rem;
            border-radius: 24px;
            box-shadow: var(--shadow-sm);
        }

        .testimonial-text {
            font-style: italic;
            color: var(--text-light);
            margin-bottom: 1.5rem;
            font-size: 0.95rem;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .author-avatar {
            width: 48px;
            height: 48px;
            background: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }

        /* Form - Simple */
        .form-card {
            background: var(--white);
            padding: 2.5rem;
            border-radius: 32px;
            box-shadow: var(--shadow);
            max-width: 600px;
            margin: 0 auto;
        }

        .form-group {
            margin-bottom: 1.2rem;
        }

        .form-group input,
        .form-group select {
            width: 100%;
            padding: 1rem;
            border: 1px solid #e2e8f0;
            border-radius: 16px;
            font-family: inherit;
            font-size: 0.95rem;
            transition: all 0.2s;
        }

        .form-group input:focus,
        .form-group select:focus {
            outline: none;
            border-color: var(--accent);
            box-shadow: 0 0 0 3px rgba(230, 180, 34, 0.1);
        }

        /* CTA Section */
        .cta-section {
            background: var(--primary);
            border-radius: 32px;
            padding: 4rem;
            text-align: center;
            color: white;
        }

        .cta-section h2 {
            font-size: 2rem;
            margin-bottom: 1rem;
        }

        .cta-section .btn-white {
            background: white;
            color: var(--primary);
            margin-top: 1.5rem;
        }

        /* Footer */
        footer {
            background: #1a2a2a;
            color: white;
            padding: 3rem 2rem 2rem;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 2rem;
        }

        .footer-logo {
            font-size: 1.5rem;
            font-weight: 800;
            margin-bottom: 1rem;
        }

        .footer-links {
            display: flex;
            gap: 3rem;
            flex-wrap: wrap;
        }

        .footer-links a {
            color: rgba(255, 255, 255, 0.7);
            text-decoration: none;
            display: block;
            margin-bottom: 0.5rem;
        }

        .whatsapp-float {
            position: fixed;
            bottom: 24px;
            right: 24px;
            background: #25D366;
            width: 56px;
            height: 56px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.8rem;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
            transition: transform 0.2s;
            text-decoration: none;
        }

        /* Responsive */
        @media (max-width: 768px) {

    .hero {
        padding: 5rem 1.2rem 2rem;
    }

    .hero-content h1 {
        font-size: 1.8rem;
        line-height: 1.3;
    }

    .hero-content p {
        font-size: 0.9rem;
    }

    .hero-buttons {
        flex-direction: column;
        gap: 0.6rem;
    }

    .btn {
        width: 100%;
        font-size: 0.9rem;
        padding: 0.8rem;
    }

    .hero-stats {
        flex-direction: column;
        align-items: center;
        gap: 0.8rem;
        margin-top: 1.5rem;
    }

    .stat-number {
        font-size: 1.5rem;
    }

    .hero-image img {
        max-width: 220px;
    }

    section {
        padding: 2.5rem 1.2rem;
    }

    .program-card {
        padding: 1.5rem;
    }

}
}
    </style>
</head>
<body>
    <nav>
        <div class="nav-container">
            <a href="#" class="logo">IMTI<span>YAZ</span></a>
            <div class="menu-toggle" id="menuToggle">
                <i class="fas fa-bars"></i>
            </div>
            <div class="nav-links" id="navLinks">
                <a href="#home">Beranda</a>
                <a href="#program">Program</a>
                <a href="#testimoni">Testimoni</a>
                <a href="#daftar" class="btn-nav">Daftar</a>
            </div>
        </div>
    </nav>

    <section class="hero" id="home">
        <div class="hero-container">
            <div class="hero-content">
                <h1>Belajar Lebih Dekat, <br><span>Hasil Lebih Hebat</span></h1>
                <p>Bimbingan privat Quran & Akademik di Banda Aceh. Metode personal, fleksibel, dan terjangkau.</p>
                <div class="hero-buttons">
                    <a href="#daftar" class="btn btn-primary">Daftar Sekarang →</a>
                    <a href="#program" class="btn btn-outline">Lihat Program</a>
                </div>
                <div class="hero-stats">
                    <div class="stat">
                        <div class="stat-number">500+</div>
                        <div>Siswa</div>
                    </div>
                    <div class="stat">
                        <div class="stat-number">20+</div>
                        <div>Pengajar</div>
                    </div>
                    <div class="stat">
                        <div class="stat-number">98%</div>
                        <div>Puas</div>
                    </div>
                </div>
            </div>
            <div class="hero-image">
                <img src="logo imtiyaz.png" alt="Belajar">
            </div>
        </div>
    </section>

    <section id="program">
        <div class="container">
            <h2 class="section-title">Program <span>Unggulan</span></h2>
            <div class="programs-grid">
                <div class="program-card">
                    <div class="program-icon">📚</div>
                    <h3>Calistung</h3>
                    <p>Baca, tulis, hitung untuk anak usia dini</p>
                    <div class="program-price">Rp35K</div>
                    <a href="#daftar" class="btn btn-primary" style="padding: 0.6rem 1.5rem;">Daftar</a>
                </div>
                <div class="program-card">
                    <div class="program-icon">📿</div>
                    <h3>Mengaji & Tahfidz</h3>
                    <p>Tajwid, makhraj, dan hafalan Al-Qur'an</p>
                    <div class="program-price">Rp35K - 50K</div>
                    <a href="#daftar" class="btn btn-primary" style="padding: 0.6rem 1.5rem;">Daftar</a>
                </div>
                <div class="program-card">
                    <div class="program-icon">🕌</div>
                    <h3>Bahasa Arab</h3>
                    <p>Nahwu, sharaf, dan percakapan sehari-hari</p>
                    <div class="program-price">Rp55K - 70K</div>
                    <a href="#daftar" class="btn btn-primary" style="padding: 0.6rem 1.5rem;">Daftar</a>
                </div>
                <div class="program-card">
                    <div class="program-icon">🌍</div>
                    <h3>Bahasa Inggris</h3>
                    <p>Speaking, grammar, persiapan TOEFL</p>
                    <div class="program-price">Rp55K - 70K</div>
                    <a href="#daftar" class="btn btn-primary" style="padding: 0.6rem 1.5rem;">Daftar</a>
                </div>
            </div>
        </div>
    </section>

    <section id="testimoni" style="background: var(--white);">
        <div class="container">
            <h2 class="section-title">Apa Kata <span>Mereka?</span></h2>
            <div class="testimonials-grid">
                <div class="testimonial-card">
                    <p class="testimonial-text">"Alhamdulillah, nilai anak saya meningkat drastis. Pengajarnya sabar dan metode belajarnya menyenangkan."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">SR</div>
                        <div>
                            <strong>Siti Rahmawati</strong>
                            <p style="font-size: 0.8rem; color: var(--text-light);">Orang Tua Siswa</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">"Program tahfidz sangat membantu. Anak saya jadi lebih lancar membaca Al-Qur'an dengan tajwid yang benar."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">AH</div>
                        <div>
                            <strong>Ahmad Hidayat</strong>
                            <p style="font-size: 0.8rem; color: var(--text-light);">Orang Tua Siswa</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <p class="testimonial-text">"Belajar Bahasa Inggris di sini seru! Sekarang saya lebih percaya diri speaking di sekolah."</p>
                    <div class="testimonial-author">
                        <div class="author-avatar">FZ</div>
                        <div>
                            <strong>Fatimah Az-Zahra</strong>
                            <p style="font-size: 0.8rem; color: var(--text-light);">Siswa SMA</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="daftar">
        <div class="container">
            <div class="form-card">
                <h2 style="text-align: center; margin-bottom: 1.5rem;">Daftar Sekarang</h2>
                <form id="registerForm">
                    <div class="form-group">
                        <input type="text" placeholder="Nama Siswa" id="nama" required>
                    </div>
                    <div class="form-group">
                        <select id="programSelect" required>
                            <option value="">Pilih Program</option>
                            <option value="Calistung">Calistung</option>
                            <option value="Mengaji & Tahfidz">Mengaji & Tahfidz</option>
                            <option value="Bahasa Arab">Bahasa Arab</option>
                            <option value="Bahasa Inggris">Bahasa Inggris</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <input type="tel" placeholder="No. WhatsApp" id="wa" required>
                    </div>
                    <div class="form-group">
                        <input type="text" placeholder="Alamat" id="alamat" required>
                    </div>
                    <button type="submit" class="btn btn-primary" style="width: 100%;">
                        <i class="fab fa-whatsapp"></i> Daftar via WhatsApp
                    </button>
                </form>
            </div>
        </div>
    </section>

    <div class="container">
        <div class="cta-section">
            <h2>Untuk Informasi Lebih Lanjut</h2>
            <a href="#daftar" class="btn btn-white">Hubungi Kami! →</a>
        </div>
    </div>

    <footer>
        <div class="footer-content">
            <div>
                <div class="footer-logo">IMTI<span style="color: var(--accent);">YAZ</span></div>
                <p style="color: rgba(255,255,255,0.6);">Quranic & Academic Tutoring</p>
                <p style="margin-top: 1rem; font-size: 0.85rem;">📍 Banda Aceh & Sekitarnya </p>
            </div>
            <div class="footer-links">
                <div>
                    <strong>Program</strong>
                    <a href="#">Calistung</a>
                    <a href="#">Mengaji & Tahfidz</a>
                    <a href="#">Bahasa Arab</a>
                    <a href="#">Bahasa Inggris</a>
                </div>
                <div>
                    <strong>Kontak</strong>
                    <a href="tel:087754721634">0877 5472 1634</a>
                    <a href="mailto:privateimtiyaz@gmail.com">privateimtiyaz@gmail.com</a>
                </div>
            </div>
        </div>
        <div style="text-align: center; margin-top: 3rem; padding-top: 1.5rem; border-top: 1px solid rgba(255,255,255,0.1); font-size: 0.8rem; color: rgba(255,255,255,0.5);">
            © 2026 IMTIYAZ. All rights reserved.
        </div>
    </footer>

    <a href="https://wa.me/6287754721634" class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <script>
        // Mobile menu
        const menuToggle = document.getElementById('menuToggle');
        const navLinksMobile = document.getElementById('navLinks');
        
        menuToggle.addEventListener('click', () => {
            navLinksMobile.classList.toggle('show');
        });

        // Form submission
        const form = document.getElementById('registerForm');
        form.addEventListener('submit', (e) => {
            e.preventDefault();
            const nama = document.getElementById('nama').value;
            const program = document.getElementById('programSelect').value;
            const wa = document.getElementById('wa').value;
            const alamat = document.getElementById('alamat').value;

            if (!nama || !program || !wa || !alamat) {
                alert('Mohon lengkapi data!');
                return;
            }

            const message = `Halo IMTIYAZ, saya ingin mendaftar:%0A%0A*Nama:* ${nama}%0A*Program:* ${program}%0A*WhatsApp:* ${wa}%0A*Alamat:* ${alamat}%0A%0A Mohon info lebih lanjut. Terima kasih.`;
            window.open(`https://wa.me/6287754721634?text=${message}`, '_blank');
            form.reset();
        });

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                    navLinksMobile.classList.remove('show');
                }
            });
        });
    </script>
</body>
</html>
