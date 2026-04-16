<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;}

body{
    font-family:'Inter',sans-serif;
    background:#fef9f0;
    color:#1e2a3a;
}

/* NAV */
nav{
    position:fixed;
    top:0;
    width:100%;
    background:#fff;
    padding:1rem;
    text-align:center;
    font-weight:700;
}

/* HERO */
.hero{
    padding:5.5rem 1.2rem 2rem;
    text-align:center;
}

.hero h1{
    font-size:1.6rem;
    margin-bottom:0.8rem;
}

.hero span{
    color:#e6b422;
}

.hero p{
    font-size:0.9rem;
    margin-bottom:1.2rem;
}

.btn{
    display:block;
    width:100%;
    padding:0.8rem;
    border-radius:100px;
    text-decoration:none;
    margin-bottom:0.5rem;
    font-size:0.9rem;
}

.btn-primary{
    background:#0f5c5c;
    color:#fff;
}

.btn-outline{
    border:2px solid #0f5c5c;
    color:#0f5c5c;
}

/* STATS */
.stats{
    margin-top:1.2rem;
}

.stats div{
    margin-bottom:0.5rem;
}

/* SECTION */
section{
    padding:2rem 1.2rem;
}

.section-title{
    text-align:center;
    margin-bottom:1.5rem;
}

/* CARD */
.card{
    background:#fff;
    padding:1.2rem;
    border-radius:20px;
    margin-bottom:1rem;
    text-align:center;
}

/* FORM */
input, select{
    width:100%;
    padding:0.8rem;
    margin-bottom:0.7rem;
    border-radius:12px;
    border:1px solid #ddd;
}

/* CTA */
.cta{
    background:#0f5c5c;
    color:#fff;
    padding:1.5rem;
    border-radius:20px;
    text-align:center;
}

</style>
</head>

<body>

<nav>IMTI<span style="color:#e6b422;">YAZ</span></nav>

<section class="hero">
<h1>Belajar Lebih Dekat,<br><span>Hasil Lebih Hebat</span></h1>
<p>Bimbel privat Quran & Akademik</p>

<a href="#daftar" class="btn btn-primary">Daftar Sekarang</a>
<a href="#program" class="btn btn-outline">Lihat Program</a>

<div class="stats">
<div><strong>500+</strong> Siswa</div>
<div><strong>20+</strong> Pengajar</div>
<div><strong>98%</strong> Puas</div>
</div>
</section>

<section id="program">
<h2 class="section-title">Program</h2>

<div class="card">
<h3>Calistung</h3>
<p>Belajar baca tulis hitung</p>
</div>

<div class="card">
<h3>Mengaji</h3>
<p>Tajwid & Tahfidz</p>
</div>

<div class="card">
<h3>Bahasa Arab</h3>
<p>Nahwu & Sharaf</p>
</div>

<div class="card">
<h3>Bahasa Inggris</h3>
<p>Grammar & Speaking</p>
</div>

</section>

<section id="daftar">
<h2 class="section-title">Daftar</h2>

<input type="text" placeholder="Nama">
<select>
<option>Pilih Program</option>
<option>Calistung</option>
<option>Mengaji</option>
</select>
<input type="text" placeholder="No WA">
<input type="text" placeholder="Alamat">

<a href="https://wa.me/6287754721634" class="btn btn-primary">
Daftar via WhatsApp
</a>

</section>

<section>
<div class="cta">
<h3>Hubungi Kami Sekarang</h3>
</div>
</section>

</body>
</html>
