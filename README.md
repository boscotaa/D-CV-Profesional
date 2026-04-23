# D-CV-Profesional
Donbosco Silvester Taa — CV Profesional
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Donbosco Silvester Taa — Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0d0d0d;
    --surface: #161616;
    --surface2: #1e1e1e;
    --border: #2a2a2a;
    --accent: #c9a84c;
    --accent2: #e8c97e;
    --text: #f0ede8;
    --text2: #a09890;
    --text3: #6a6360;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    font-weight: 300;
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* NAV */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    background: rgba(13,13,13,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    padding: 0 48px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 64px;
  }

  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem;
    color: var(--accent);
    letter-spacing: 0.04em;
    font-weight: 600;
  }

  .nav-links {
    display: flex;
    gap: 36px;
    list-style: none;
  }

  .nav-links a {
    color: var(--text2);
    text-decoration: none;
    font-size: 0.82rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    font-weight: 500;
    transition: color 0.2s;
  }

  .nav-links a:hover { color: var(--accent); }

  /* HERO */
  .hero {
    min-height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding-top: 64px;
  }

  .hero-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 80px 72px 80px 80px;
  }

  .hero-tag {
    display: inline-block;
    font-size: 0.72rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--accent);
    border: 1px solid var(--accent);
    padding: 5px 14px;
    border-radius: 2px;
    margin-bottom: 32px;
    width: fit-content;
  }

  .hero-name {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.8rem, 4vw, 4.2rem);
    font-weight: 700;
    line-height: 1.12;
    letter-spacing: -0.01em;
    margin-bottom: 24px;
    color: var(--text);
  }

  .hero-name span {
    color: var(--accent);
    display: block;
  }

  .hero-desc {
    color: var(--text2);
    font-size: 0.96rem;
    line-height: 1.8;
    max-width: 480px;
    margin-bottom: 40px;
  }

  .hero-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 48px;
  }

  .tag {
    background: var(--surface2);
    border: 1px solid var(--border);
    color: var(--text2);
    font-size: 0.75rem;
    padding: 6px 14px;
    border-radius: 2px;
    letter-spacing: 0.05em;
  }

  .hero-stats {
    display: flex;
    gap: 40px;
    padding-top: 40px;
    border-top: 1px solid var(--border);
  }

  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2rem;
    font-weight: 700;
    color: var(--accent);
    line-height: 1;
  }

  .stat-label {
    font-size: 0.72rem;
    color: var(--text3);
    letter-spacing: 0.06em;
    text-transform: uppercase;
    margin-top: 6px;
  }

  .hero-img-wrap {
    position: relative;
    overflow: hidden;
    background: var(--surface);
  }

  .hero-img-wrap::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, rgba(201,168,76,0.12) 0%, transparent 60%);
    z-index: 1;
    pointer-events: none;
  }

  .hero-img-wrap img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center top;
    display: block;
    filter: grayscale(20%) contrast(1.05);
    transform: scale(1.0);
  }

  .hero-scroll {
    position: absolute;
    bottom: 40px;
    left: 80px;
    display: flex;
    align-items: center;
    gap: 12px;
    color: var(--text3);
    font-size: 0.72rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
  }

  .hero-scroll::before {
    content: '';
    display: block;
    width: 32px;
    height: 1px;
    background: var(--text3);
  }

  /* SECTIONS */
  section {
    padding: 100px 80px;
    border-top: 1px solid var(--border);
  }

  .section-label {
    font-size: 0.68rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
    max-width: 60px;
  }

  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3vw, 2.8rem);
    font-weight: 600;
    margin-bottom: 56px;
    color: var(--text);
  }

  /* PROFIL */
  #about .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: start;
  }

  .about-text {
    color: var(--text2);
    font-size: 1rem;
    line-height: 1.85;
  }

  .about-right {
    display: grid;
    gap: 24px;
  }

  .info-row {
    display: flex;
    align-items: flex-start;
    gap: 20px;
    padding: 20px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 4px;
  }

  .info-icon {
    width: 36px;
    height: 36px;
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.9rem;
    flex-shrink: 0;
  }

  .info-label {
    font-size: 0.68rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--text3);
    margin-bottom: 4px;
  }

  .info-val {
    font-size: 0.9rem;
    color: var(--text);
    font-weight: 500;
  }

  /* EXPERIENCE */
  .exp-item {
    display: grid;
    grid-template-columns: 200px 1fr;
    gap: 48px;
    padding: 48px 0;
    border-bottom: 1px solid var(--border);
  }

  .exp-item:first-of-type { padding-top: 0; }

  .exp-meta {
    padding-top: 4px;
  }

  .exp-period {
    font-size: 0.75rem;
    color: var(--accent);
    letter-spacing: 0.06em;
    margin-bottom: 10px;
    font-weight: 500;
  }

  .exp-company {
    font-size: 0.82rem;
    color: var(--text2);
    line-height: 1.5;
  }

  .exp-type {
    display: inline-block;
    margin-top: 10px;
    font-size: 0.65rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--text3);
    border: 1px solid var(--border);
    padding: 3px 8px;
    border-radius: 2px;
  }

  .exp-role {
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem;
    font-weight: 600;
    color: var(--text);
    margin-bottom: 20px;
    line-height: 1.3;
  }

  .exp-list {
    list-style: none;
    display: grid;
    gap: 12px;
  }

  .exp-list li {
    color: var(--text2);
    font-size: 0.9rem;
    padding-left: 20px;
    position: relative;
    line-height: 1.6;
  }

  .exp-list li::before {
    content: '—';
    position: absolute;
    left: 0;
    color: var(--accent);
    font-weight: 600;
  }

  /* SKILLS */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2px;
  }

  .skill-cat {
    background: var(--surface);
    padding: 36px 32px;
    border: 1px solid var(--border);
    transition: border-color 0.2s, background 0.2s;
  }

  .skill-cat:hover {
    border-color: var(--accent);
    background: var(--surface2);
  }

  .skill-cat-title {
    font-size: 0.7rem;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 20px;
    font-weight: 600;
  }

  .skill-items {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .skill-item {
    font-size: 0.8rem;
    color: var(--text2);
    background: var(--surface2);
    padding: 5px 12px;
    border-radius: 2px;
    border: 1px solid var(--border);
  }

  /* EDUCATION */
  .edu-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
  }

  .edu-card {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 40px 36px;
    border-radius: 4px;
    position: relative;
    overflow: hidden;
  }

  .edu-card::after {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px;
    height: 100%;
    background: var(--accent);
  }

  .edu-year {
    font-size: 0.72rem;
    letter-spacing: 0.1em;
    color: var(--accent);
    text-transform: uppercase;
    margin-bottom: 12px;
    font-weight: 600;
  }

  .edu-degree {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem;
    font-weight: 600;
    color: var(--text);
    margin-bottom: 8px;
  }

  .edu-inst {
    font-size: 0.88rem;
    color: var(--text2);
    margin-bottom: 16px;
  }

  .edu-ipk {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: var(--surface2);
    border: 1px solid var(--border);
    padding: 8px 16px;
    border-radius: 2px;
    font-size: 0.8rem;
  }

  .edu-ipk strong {
    color: var(--accent);
    font-family: 'Playfair Display', serif;
    font-size: 1rem;
  }

  .edu-note {
    margin-top: 16px;
    font-size: 0.82rem;
    color: var(--text3);
    line-height: 1.6;
  }

  /* ACHIEVEMENT */
  .achievement-box {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 36px 40px;
    display: flex;
    align-items: center;
    gap: 24px;
    border-radius: 4px;
    max-width: 700px;
  }

  .ach-icon {
    font-size: 2rem;
    flex-shrink: 0;
  }

  .ach-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    font-weight: 600;
    color: var(--text);
    margin-bottom: 6px;
  }

  .ach-sub {
    font-size: 0.84rem;
    color: var(--text2);
  }

  /* CONTACT */
  #contact {
    background: var(--surface);
  }

  .contact-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: center;
  }

  .contact-tagline {
    font-family: 'Playfair Display', serif;
    font-size: 2rem;
    font-weight: 600;
    line-height: 1.3;
    color: var(--text);
    margin-bottom: 20px;
  }

  .contact-desc {
    color: var(--text2);
    font-size: 0.9rem;
    line-height: 1.8;
    margin-bottom: 40px;
  }

  .contact-links {
    display: grid;
    gap: 16px;
  }

  .contact-link {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 20px 24px;
    background: var(--surface2);
    border: 1px solid var(--border);
    border-radius: 4px;
    text-decoration: none;
    color: var(--text);
    transition: border-color 0.2s, background 0.2s;
  }

  .contact-link:hover {
    border-color: var(--accent);
    background: var(--bg);
  }

  .contact-link-icon {
    width: 40px;
    height: 40px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1rem;
    flex-shrink: 0;
  }

  .contact-link-label {
    font-size: 0.68rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--text3);
    margin-bottom: 3px;
  }

  .contact-link-val {
    font-size: 0.9rem;
    color: var(--text);
    font-weight: 500;
  }

  /* FOOTER */
  footer {
    padding: 32px 80px;
    border-top: 1px solid var(--border);
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .footer-name {
    font-family: 'Playfair Display', serif;
    color: var(--accent);
    font-size: 1rem;
    font-weight: 600;
  }

  .footer-copy {
    font-size: 0.75rem;
    color: var(--text3);
  }

  @media (max-width: 1024px) {
    .hero { grid-template-columns: 1fr; min-height: auto; }
    .hero-img-wrap { height: 60vw; max-height: 480px; }
    .hero-content { padding: 60px 40px; }
    section { padding: 80px 40px; }
    .exp-item { grid-template-columns: 1fr; gap: 16px; }
    .skills-grid { grid-template-columns: repeat(2, 1fr); }
    #about .about-grid { grid-template-columns: 1fr; gap: 40px; }
    .edu-grid { grid-template-columns: 1fr; }
    .contact-grid { grid-template-columns: 1fr; gap: 40px; }
    nav { padding: 0 32px; }
    footer { padding: 24px 40px; }
    .hero-scroll { left: 40px; }
  }

  @media (max-width: 640px) {
    .nav-links { display: none; }
    .hero-content { padding: 40px 24px; }
    section { padding: 60px 24px; }
    .skills-grid { grid-template-columns: 1fr; }
    .hero-stats { flex-wrap: wrap; gap: 24px; }
    footer { flex-direction: column; gap: 12px; text-align: center; }
    nav { padding: 0 24px; }
    .hero-scroll { left: 24px; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">D. S. Taa</div>
  <ul class="nav-links">
    <li><a href="#about">Profil</a></li>
    <li><a href="#experience">Pengalaman</a></li>
    <li><a href="#skills">Keahlian</a></li>
    <li><a href="#education">Pendidikan</a></li>
    <li><a href="#contact">Kontak</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero" style="padding: 0; border: none;">
  <div class="hero-content" style="position: relative;">
    <div class="hero-tag">Portfolio Profesional</div>
    <h1 class="hero-name">
      Donbosco
      <span>Silvester Taa</span>
    </h1>
    <p class="hero-desc">Lulusan D4 Bisnis Internasional Universitas Padjadjaran dengan pengalaman di bidang ekspor-impor, digital marketing, dan analisis bisnis. Siap membawa kontribusi nyata bagi perusahaan Anda.</p>
    <div class="hero-tags">
      <span class="tag">Ekspor-Impor</span>
      <span class="tag">Digital Marketing</span>
      <span class="tag">Analisis Bisnis</span>
      <span class="tag">SEO & Ads</span>
      <span class="tag">Bisnis Internasional</span>
    </div>
    <div class="hero-stats">
      <div>
        <div class="stat-num">3.51</div>
        <div class="stat-label">IPK UNPAD</div>
      </div>
      <div>
        <div class="stat-num">2</div>
        <div class="stat-label">Pengalaman Magang</div>
      </div>
      <div>
        <div class="stat-num">1K+</div>
        <div class="stat-label">Data Klien Dikelola</div>
      </div>
      <div>
        <div class="stat-num">45+</div>
        <div class="stat-label">Konten Dibuat</div>
      </div>
    </div>
    <div class="hero-scroll">Scroll</div>
  </div>
  <div class="hero-img-wrap">
    <img src="data:image/jpeg;base64,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" alt="Donbosco Silvester Taa" />
  </div>
</section>

<!-- PROFIL -->
<section id="about">
  <div class="section-label">01</div>
  <h2 class="section-title">Profil Saya</h2>
  <div class="about-grid">
    <div>
      <p class="about-text">
        Fresh graduate D4 Bisnis Internasional Universitas Padjadjaran (IPK 3,51/4,00) dengan pengalaman magang yang solid di bidang administrasi, pengelolaan data skala besar, dan dokumentasi logistik. Terbukti mampu mengelola lebih dari 1.000 entri data dengan akurasi tinggi, serta menyusun dokumen rantai pasok meliputi packing list, invoice, bill of lading, dan PEB/PIB. Terbiasa berkoordinasi lintas divisi dalam lingkungan kerja profesional dan serba cepat.
        <br><br>
        Kemampuan kepemimpinan dibuktikan melalui jabatan Wakil Ketua organisasi kampus serta posisi Kepala Divisi pada tiga kegiatan kampus berskala besar. Fasih berbahasa Inggris secara aktif, berdomisili di Bandung, Jawa Barat, dan siap bekerja dalam sistem 3 shift.
      </p>
    </div>
    <div class="about-right">
      <div class="info-row">
        <div class="info-icon">🎓</div>
        <div>
          <div class="info-label">Beasiswa</div>
          <div class="info-val">Beasiswa Afirmasi/ADik — Pemerintah Pusat & Kab. Nabire (2020–Sekarang)</div>
        </div>
      </div>
      <div class="info-row">
        <div class="info-icon">📍</div>
        <div>
          <div class="info-label">Domisili</div>
          <div class="info-val">Bandung, Jawa Barat</div>
        </div>
      </div>
      <div class="info-row">
        <div class="info-icon">🌐</div>
        <div>
          <div class="info-label">Bahasa</div>
          <div class="info-val">Bahasa Indonesia (Pembicara Asli) · Bahasa Inggris (Advanced)</div>
        </div>
      </div>
      <div class="info-row">
        <div class="info-icon">🕐</div>
        <div>
          <div class="info-label">Kesiapan Kerja</div>
          <div class="info-val">Siap sistem 3 shift · Full-time</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section-label">02</div>
  <h2 class="section-title">Pengalaman</h2>

  <div class="exp-item">
    <div class="exp-meta">
      <div class="exp-period">Okt 2024 – Jan 2025</div>
      <div class="exp-company">Satukelas.id</div>
      <div class="exp-type">Magang · Digital Marketing</div>
    </div>
    <div>
      <div class="exp-role">Staf Marketing</div>
      <ul class="exp-list">
        <li>Menjalankan kampanye iklan berbayar Meta Ads & Google Ads untuk promosi produk Satukelas</li>
        <li>Membuat 45+ konten media sosial (TikTok & Instagram) berupa reels, feeds, dan story dengan teknik copywriting IDCA, HSO, dan PAS</li>
        <li>Membangun dan mengoptimalkan website dengan SEO berdasarkan riset Google Trends & Keyword Planner</li>
        <li>Melakukan analisis bisnis: Business Model Canvas, SWOT, Customer Journey, dan analisis kompetitor</li>
        <li>Berhasil merealisasikan minimal satu penjualan produk secara mandiri</li>
      </ul>
    </div>
  </div>

  <div class="exp-item">
    <div class="exp-meta">
      <div class="exp-period">Agu – Des 2023</div>
      <div class="exp-company">FTA Center — Kementerian Perdagangan RI</div>
      <div class="exp-type">Magang · Ekspor-Impor</div>
    </div>
    <div>
      <div class="exp-role">Konsultan Junior</div>
      <ul class="exp-list">
        <li>Memberikan layanan konsultasi proses ekspor: business matching, sales contract, logistik, dan pembayaran internasional</li>
        <li>Mengelola dan merekap lebih dari 1.000 data konsultasi klien dari tahun 2019–2023</li>
        <li>Penentuan HS Code via insw.go.id dan analisis regulasi ekspor-impor via macmap.org</li>
        <li>Analisis pasar ekspor menggunakan trademap.org</li>
        <li>Registrasi dan pengisian e-SKA (Surat Keterangan Asal)</li>
        <li>Merekap dan mendokumentasikan kegiatan FTA: konsultasi, kunjungan perusahaan, dan seminar edukasi</li>
      </ul>
    </div>
  </div>

  <div class="exp-item">
    <div class="exp-meta">
      <div class="exp-period">Feb 2021 – Feb 2022</div>
      <div class="exp-company">Himpunan Mahasiswa Papua — Universitas Padjadjaran</div>
      <div class="exp-type">Organisasi · Kepemimpinan</div>
    </div>
    <div>
      <div class="exp-role">Wakil Ketua</div>
      <ul class="exp-list">
        <li>Mendampingi ketua dalam koordinasi kegiatan dan memastikan program kerja berjalan efektif</li>
        <li>Mengelola komunikasi dan koordinasi antar anggota mahasiswa Papua di UNPAD</li>
        <li>Berperan aktif dalam perencanaan kegiatan akademik, sosial, dan pengambilan keputusan strategis</li>
        <li>Mendukung dan memfasilitasi mahasiswa Papua dalam beradaptasi secara akademik dan sosial</li>
      </ul>
    </div>
  </div>

  <div class="exp-item">
    <div class="exp-meta">
      <div class="exp-period">Okt – Nov 2021</div>
      <div class="exp-company">Virtual Porseni Kabim — Universitas Padjadjaran</div>
      <div class="exp-type">Kepanitiaan · Event</div>
    </div>
    <div>
      <div class="exp-role">Kepala Divisi Dokumentasi & Dekorasi</div>
      <ul class="exp-list">
        <li>Memimpin divisi desain dan dokumentasi: konten sosmed, sertifikat, dan piagam acara</li>
        <li>Memantau dan mendokumentasikan teknis acara virtual melalui Zoom</li>
        <li>Memberikan rekomendasi strategis kepada ketua panitia terkait pelaksanaan acara</li>
      </ul>
    </div>
  </div>

  <div class="exp-item" style="border-bottom: none;">
    <div class="exp-meta">
      <div class="exp-period">Feb 2021 – Feb 2022</div>
      <div class="exp-company">Padjadjaran Festival Finansial</div>
      <div class="exp-type">Kepanitiaan · Operasional</div>
    </div>
    <div>
      <div class="exp-role">Anggota Operasional</div>
      <ul class="exp-list">
        <li>Mengelola dan menyiapkan kebutuhan acara serta memantau teknis pelaksanaan</li>
        <li>Membuat dan mendistribusikan sertifikat kepada 10+ pemateri & juri, 6 pemenang, dan 300+ peserta</li>
        <li>Mengarahkan peserta dan berkolaborasi lintas tim selama acara berlangsung</li>
      </ul>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-label">03</div>
  <h2 class="section-title">Keahlian</h2>
  <div class="skills-grid">
    <div class="skill-cat">
      <div class="skill-cat-title">Digital Marketing</div>
      <div class="skill-items">
        <span class="skill-item">Meta Ads</span>
        <span class="skill-item">Google Ads</span>
        <span class="skill-item">TikTok Ads</span>
        <span class="skill-item">SEO</span>
        <span class="skill-item">Copywriting</span>
        <span class="skill-item">Marketing Funnel</span>
        <span class="skill-item">SMO</span>
        <span class="skill-item">STP Strategy</span>
      </div>
    </div>
    <div class="skill-cat">
      <div class="skill-cat-title">Ekspor-Impor</div>
      <div class="skill-items">
        <span class="skill-item">LC & Bill of Lading</span>
        <span class="skill-item">Invoice</span>
        <span class="skill-item">Packing List</span>
        <span class="skill-item">HS Code</span>
        <span class="skill-item">e-SKA</span>
        <span class="skill-item">PEB & PIB</span>
        <span class="skill-item">Trademap</span>
        <span class="skill-item">Macmap</span>
      </div>
    </div>
    <div class="skill-cat">
      <div class="skill-cat-title">Konten & Desain</div>
      <div class="skill-items">
        <span class="skill-item">Canva</span>
        <span class="skill-item">CapCut</span>
        <span class="skill-item">Adobe Premiere</span>
        <span class="skill-item">TikTok Live Studio</span>
        <span class="skill-item">Color Grading</span>
        <span class="skill-item">Konten Kreator</span>
      </div>
    </div>
    <div class="skill-cat">
      <div class="skill-cat-title">Analisis Bisnis</div>
      <div class="skill-items">
        <span class="skill-item">SWOT</span>
        <span class="skill-item">BMC</span>
        <span class="skill-item">Design Thinking</span>
        <span class="skill-item">Google Analytics</span>
        <span class="skill-item">Tableau</span>
        <span class="skill-item">NVivo</span>
        <span class="skill-item">Customer Journey</span>
      </div>
    </div>
    <div class="skill-cat">
      <div class="skill-cat-title">Produktivitas & Teknis</div>
      <div class="skill-items">
        <span class="skill-item">Microsoft Excel</span>
        <span class="skill-item">Microsoft Word</span>
        <span class="skill-item">Google Suite</span>
        <span class="skill-item">Wix Builder</span>
        <span class="skill-item">AI Tools</span>
        <span class="skill-item">Notulen</span>
      </div>
    </div>
    <div class="skill-cat">
      <div class="skill-cat-title">Soft Skills</div>
      <div class="skill-items">
        <span class="skill-item">Presentasi Publik</span>
        <span class="skill-item">Komunikasi Bisnis</span>
        <span class="skill-item">Kepemimpinan</span>
        <span class="skill-item">Problem Solving</span>
        <span class="skill-item">Koordinasi Tim</span>
        <span class="skill-item">Public Speaking</span>
      </div>
    </div>
  </div>
</section>

<!-- EDUCATION -->
<section id="education">
  <div class="section-label">04</div>
  <h2 class="section-title">Pendidikan & Pencapaian</h2>
  <div class="edu-grid">
    <div class="edu-card">
      <div class="edu-year">2020 – 2025</div>
      <div class="edu-degree">D4 Bisnis Internasional</div>
      <div class="edu-inst">Universitas Padjadjaran · Fakultas Ekonomi dan Bisnis</div>
      <div class="edu-ipk">IPK <strong>3,51 / 4,00</strong></div>
      <p class="edu-note">Fokus pada perdagangan internasional, manajemen bisnis global, analisis pasar, dan kewirausahaan digital.</p>
    </div>
    <div class="edu-card">
      <div class="edu-year">2017 – 2020</div>
      <div class="edu-degree">Sekolah Menengah Atas</div>
      <div class="edu-inst">YPPK Adhi Luhur Kolese LE COCQ D'Armandville</div>
      <p class="edu-note">Lulusan dengan fondasi akademik kuat, berhasil meraih Beasiswa Afirmasi/ADik dari Pemerintah Pusat dan Kabupaten Nabire untuk melanjutkan studi ke Universitas Padjadjaran.</p>
    </div>
  </div>

  <div style="margin-top: 40px;">
    <div class="achievement-box">
      <div class="ach-icon">🏆</div>
      <div>
        <div class="ach-title">Beasiswa Afirmasi/ADik</div>
        <div class="ach-sub">Pemerintah Pusat & Kabupaten Nabire · 2020 – Sekarang</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="contact-grid">
    <div>
      <div class="section-label">05</div>
      <h2 class="section-title" style="margin-bottom: 20px;">Mari Terhubung</h2>
      <p class="contact-desc">Terbuka untuk peluang di bidang digital marketing, bisnis internasional, logistik & rantai pasok, analisis bisnis, maupun posisi entry-level lainnya.</p>
    </div>
    <div class="contact-links">
      <a class="contact-link" href="tel:081388334752">
        <div class="contact-link-icon">📞</div>
        <div>
          <div class="contact-link-label">Telepon</div>
          <div class="contact-link-val">081388334752</div>
        </div>
      </a>
      <a class="contact-link" href="mailto:donboscosilvestertaa@gmail.com">
        <div class="contact-link-icon">✉️</div>
        <div>
          <div class="contact-link-label">Email</div>
          <div class="contact-link-val">donboscosilvestertaa@gmail.com</div>
        </div>
      </a>
      <a class="contact-link" href="https://lynk.id/boscotaa" target="_blank">
        <div class="contact-link-icon">🔗</div>
        <div>
          <div class="contact-link-label">Profil Linktree</div>
          <div class="contact-link-val">lynk.id/boscotaa</div>
        </div>
      </a>
    </div>
  </div>
</section>

<footer>
  <div class="footer-name">D. S. Taa</div>
  <div class="footer-copy">© 2025 Donbosco Silvester Taa. All rights reserved.</div>
</footer>

</body>
</html>
