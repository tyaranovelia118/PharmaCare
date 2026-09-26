<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>PharmaCare | Your Guide to Medicine & Health Consultation</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: "Poppins", Arial, sans-serif;
    }

    body {
      background: #fff7fa;
      color: #4b3b42;
      line-height: 1.7;
    }

    /* ================= HEADER ================= */

    header {
      background: linear-gradient(135deg, #f6c6d8, #eeb3ca);
      padding: 18px 6%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 3px 15px rgba(120, 70, 90, 0.12);
    }

    .logo {
      font-size: 27px;
      font-weight: 700;
      color: #8f4566;
    }

    .tagline-small {
      font-size: 11px;
      color: #704657;
    }

    nav {
      display: flex;
      gap: 8px;
      flex-wrap: wrap;
      justify-content: center;
    }

    nav button {
      border: none;
      background: transparent;
      color: #633d4d;
      padding: 8px 12px;
      border-radius: 20px;
      cursor: pointer;
      font-weight: 600;
      transition: 0.3s;
    }

    nav button:hover {
      background: #fff;
      color: #a64f73;
    }

    /* ================= PAGE ================= */

    .page {
      display: none;
      animation: fadeIn 0.3s ease;
    }

    .page.active {
      display: block;
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: translateY(8px);
      }

      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .container {
      width: 90%;
      max-width: 1150px;
      margin: auto;
    }

    /* ================= HERO ================= */

    .hero {
      background: linear-gradient(135deg, #fde7ef, #fff);
      padding: 70px 20px;
      text-align: center;
    }

    .hero h1 {
      color: #914866;
      font-size: 42px;
      margin-bottom: 8px;
    }

    .hero h2 {
      color: #6f4757;
      font-size: 20px;
      font-weight: 500;
      margin-bottom: 20px;
    }

    .hero p {
      max-width: 750px;
      margin: auto;
      color: #67545c;
    }

    .search-box {
      max-width: 700px;
      margin: 30px auto 0;
      display: flex;
      background: white;
      padding: 7px;
      border-radius: 40px;
      box-shadow: 0 5px 20px rgba(150, 70, 100, 0.12);
    }

    .search-box input {
      flex: 1;
      border: none;
      outline: none;
      padding: 14px 18px;
      border-radius: 30px;
      font-size: 15px;
    }

    .btn {
      border: none;
      background: #b65d82;
      color: white;
      padding: 12px 22px;
      border-radius: 30px;
      cursor: pointer;
      font-weight: 600;
      transition: 0.3s;
    }

    .btn:hover {
      background: #934965;
      transform: translateY(-2px);
    }

    /* ================= SECTION ================= */

    section.content {
      padding: 55px 0;
    }

    .section-title {
      text-align: center;
      margin-bottom: 35px;
    }

    .section-title h2 {
      color: #914866;
      font-size: 30px;
      margin-bottom: 8px;
    }

    .section-title p {
      color: #77656c;
    }

    /* ================= CARD ================= */

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
    }

    .card {
      background: white;
      border-radius: 18px;
      padding: 24px;
      box-shadow: 0 5px 18px rgba(100, 60, 80, 0.08);
      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 25px rgba(100, 60, 80, 0.14);
    }

    .card h3 {
      color: #934b69;
      margin-bottom: 8px;
    }

    .card p {
      color: #6f6065;
      font-size: 14px;
    }

    .card-icon {
      font-size: 38px;
      margin-bottom: 12px;
    }

    /* ================= CATEGORY ================= */

    .category-card {
      text-align: center;
      cursor: pointer;
    }

    .category-card .card-icon {
      font-size: 42px;
    }

    /* ================= MEDICINE ================= */

    .medicine-card {
      overflow: hidden;
      padding: 0;
    }

    .medicine-img {
      width: 100%;
      height: 180px;
      object-fit: contain;
      background: #fff1f6;
      padding: 15px;
    }

    .medicine-content {
      padding: 20px;
    }

    .medicine-content h3 {
      margin-bottom: 5px;
    }

    .medicine-content .active {
      color: #8a6672;
      font-size: 14px;
      margin-bottom: 12px;
    }

    .medicine-detail {
      background: white;
      border-radius: 20px;
      padding: 30px;
      box-shadow: 0 5px 20px rgba(100, 60, 80, 0.08);
    }

    .detail-image {
      width: 250px;
      max-width: 100%;
      height: 220px;
      object-fit: contain;
      background: #fff1f6;
      border-radius: 15px;
      padding: 15px;
      display: block;
      margin: 0 auto 25px;
    }

    .detail-list {
      margin-top: 20px;
    }

    .detail-item {
      padding: 13px 0;
      border-bottom: 1px solid #f1dce5;
    }

    .detail-item strong {
      color: #914866;
    }

    /* ================= INFO BOX ================= */

    .info-box {
      background: #fde9f0;
      border-left: 5px solid #b65d82;
      padding: 20px;
      border-radius: 12px;
      margin: 20px 0;
    }

    .warning-box {
      background: #fff2e6;
      border-left: 5px solid #d58a4b;
      padding: 20px;
      border-radius: 12px;
      margin: 20px 0;
    }

    /* ================= PHARMACIST ================= */

    .pharmacist-card {
      text-align: center;
    }

    .avatar {
      width: 85px;
      height: 85px;
      margin: 0 auto 15px;
      border-radius: 50%;
      background: #f5c5d7;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 35px;
    }

    .status {
      display: inline-block;
      background: #e3f7e9;
      color: #31804b;
      padding: 5px 12px;
      border-radius: 20px;
      font-size: 12px;
      margin: 8px 0;
    }

    /* ================= FORM ================= */

    .form-card {
      max-width: 700px;
      margin: auto;
      background: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 5px 20px rgba(100, 60, 80, 0.08);
    }

    .form-group {
      margin-bottom: 18px;
    }

    .form-group label {
      display: block;
      margin-bottom: 6px;
      font-weight: 600;
      color: #704657;
    }

    .form-group input,
    .form-group textarea {
      width: 100%;
      border: 1px solid #e8cbd6;
      padding: 13px;
      border-radius: 12px;
      outline: none;
      resize: vertical;
    }

    .form-group input:focus,
    .form-group textarea:focus {
      border-color: #b65d82;
    }

    /* ================= BACK BUTTON ================= */

    .back-btn {
      margin-bottom: 20px;
      background: #f3d2df;
      color: #744558;
      border: none;
      padding: 9px 16px;
      border-radius: 20px;
      cursor: pointer;
      font-weight: 600;
    }

    /* ================= FOOTER ================= */

    footer {
      background: #8f4566;
      color: white;
      text-align: center;
      padding: 30px 20px;
      margin-top: 50px;
    }

    footer p {
      font-size: 14px;
      opacity: 0.9;
    }

    /* ================= MOBILE ================= */

    @media (max-width: 768px) {

      header {
        flex-direction: column;
        gap: 12px;
      }

      nav {
        gap: 3px;
      }

      nav button {
        font-size: 12px;
        padding: 7px 8px;
      }

      .hero {
        padding: 50px 15px;
      }

      .hero h1 {
        font-size: 32px;
      }

      .hero h2 {
        font-size: 17px;
      }

      .search-box {
        flex-direction: column;
        background: transparent;
        box-shadow: none;
        gap: 8px;
      }

      .search-box input {
        background: white;
        box-shadow: 0 3px 12px rgba(100, 60, 80, 0.08);
      }

      .search-box .btn {
        width: 100%;
      }

      .container {
        width: 92%;
      }

      .grid {
        grid-template-columns: 1fr 1fr;
        gap: 12px;
      }

      .card {
        padding: 18px;
      }

      .card-icon {
        font-size: 32px;
      }
    }

    @media (max-width: 480px) {
      .grid {
        grid-template-columns: 1fr;
      }

      .logo {
        font-size: 24px;
      }

      .hero h1 {
        font-size: 28px;
      }

      .section-title h2 {
        font-size: 25px;
      }
    }
  </style>
</head>

<body>

<!-- =====================================================
     HEADER
===================================================== -->

<header>

  <div>
    <div class="logo">🌸 PharmaCare</div>
    <div class="tagline-small">
      Your Guide to Medicine & Health Consultation
    </div>
  </div>

  <nav>
    <button onclick="showPage('home')">🏠 Home</button>
    <button onclick="showPage('obat')">💊 Obat</button>
    <button onclick="showPage('kesehatan')">📚 Informasi Kesehatan</button>
    <button onclick="showPage('konseling')">🩺 Konseling Apoteker</button>
    <button onclick="showPage('penting')">⚠️ Informasi Penting</button>
    <button onclick="showPage('kontak')">📞 Kontak</button>
  </nav>

</header>


<!-- =====================================================
     HOME
===================================================== -->

<main id="home" class="page active">

  <section class="hero">

    <div class="container">

      <h1>PharmaCare</h1>

      <h2>Your Guide to Medicine & Health Consultation</h2>

      <p>
        PharmaCare merupakan website informasi obat dan kesehatan
        yang membantu masyarakat memperoleh informasi mengenai obat,
        penggunaan obat yang tepat, edukasi kesehatan, serta konsultasi
        dengan apoteker.
      </p>

      <div class="search-box">

        <input
          type="text"
          id="searchInput"
          placeholder="Cari nama obat, zat aktif, atau kategori..."
          onkeydown="if(event.key==='Enter') searchMedicine()"
        >

        <button class="btn" onclick="searchMedicine()">
          🔍 Cari Obat
        </button>

      </div>

      <div id="searchResult"></div>

    </div>

  </section>


  <section class="content">

    <div class="container">

      <div class="section-title">

        <h2>Kategori Obat</h2>

        <p>
          Pilih kategori untuk melihat daftar obat yang tersedia.
        </p>

      </div>

      <div class="grid">

        <div class="card category-card" onclick="openCategory('Demam')">
          <div class="card-icon">🌡️</div>
          <h3>Demam</h3>
          <p>Informasi obat yang digunakan untuk membantu mengatasi demam.</p>
        </div>

        <div class="card category-card" onclick="openCategory('Nyeri')">
          <div class="card-icon">💊</div>
          <h3>Nyeri</h3>
          <p>Informasi mengenai obat untuk membantu meredakan nyeri.</p>
        </div>

        <div class="card category-card" onclick="openCategory('Maag')">
          <div class="card-icon">🫃</div>
          <h3>Maag</h3>
          <p>Informasi obat untuk keluhan lambung dan asam lambung.</p>
        </div>

        <div class="card category-card" onclick="openCategory('Sembelit')">
          <div class="card-icon">🌿</div>
          <h3>Sembelit</h3>
          <p>Informasi mengenai obat yang digunakan pada sembelit.</p>
        </div>

        <div class="card category-card" onclick="openCategory('Diare')">
          <div class="card-icon">💧</div>
          <h3>Diare</h3>
          <p>Informasi obat dan penanganan awal pada diare.</p>
        </div>

        <div class="card category-card" onclick="openCategory('Alergi')">
          <div class="card-icon">🤧</div>
          <h3>Alergi</h3>
          <p>Informasi obat yang digunakan untuk membantu mengatasi alergi.</p>
        </div>

        <div class="card category-card" onclick="openCategory('Flu dan Batuk')">
          <div class="card-icon">😷</div>
          <h3>Flu dan Batuk</h3>
          <p>Informasi mengenai obat untuk gejala flu dan batuk.</p>
        </div>

        <div class="card category-card" onclick="openCategory('Vitamin')">
          <div class="card-icon">🍊</div>
          <h3>Vitamin</h3>
          <p>Informasi vitamin dan penggunaannya secara tepat.</p>
        </div>

      </div>

    </div>

  </section>


  <section class="content">

    <div class="container">

      <div class="section-title">

        <h2>Layanan PharmaCare</h2>

        <p>
          Informasi dan layanan yang dapat membantu Anda memahami
          penggunaan obat dan kesehatan.
        </p>

      </div>

      <div class="grid">

        <div class="card">
          <div class="card-icon">💊</div>
          <h3>Informasi Obat</h3>
          <p>
            Temukan informasi mengenai nama dagang, zat aktif,
            kekuatan, indikasi, aturan penggunaan, efek samping,
            penyimpanan, dan peringatan obat.
          </p>
        </div>

        <div class="card">
          <div class="card-icon">📚</div>
          <h3>Informasi Kesehatan</h3>
          <p>
            Pelajari berbagai informasi mengenai penggunaan obat
            yang benar, penyimpanan obat, membaca label, dan
            pengelolaan obat di rumah.
          </p>
        </div>

        <div class="card">
          <div class="card-icon">🩺</div>
          <h3>Konseling Apoteker</h3>
          <p>
            Ajukan pertanyaan kepada apoteker mengenai penggunaan
            obat, aturan pakai, efek samping, dan hal lain yang
            berkaitan dengan penggunaan obat.
          </p>
        </div>

        <div class="card">
          <div class="card-icon">⚠️</div>
          <h3>Informasi Penting</h3>
          <p>
            Ketahui informasi penting mengenai penggunaan antibiotik
            yang tepat untuk mencegah penggunaan obat secara tidak
            bertanggung jawab.
          </p>
        </div>

      </div>

    </div>

  </section>

</main>


<!-- =====================================================
     OBAT
===================================================== -->

<section id="obat" class="page">

  <section class="content">

    <div class="container">

      <div class="section-title">

        <h2>💊 Informasi Obat</h2>

        <p>
          Pilih kategori obat untuk melihat informasi lebih lengkap.
        </p>

      </div>

      <div id="categoryContent">

        <div class="grid">

          <div class="card category-card" onclick="openCategory('Demam')">
            <div class="card-icon">🌡️</div>
            <h3>Demam</h3>
            <p>Daftar obat kategori demam.</p>
          </div>

          <div class="card category-card" onclick="openCategory('Nyeri')">
            <div class="card-icon">💊</div>
            <h3>Nyeri</h3>
            <p>Daftar obat kategori nyeri.</p>
          </div>

          <div class="card category-card" onclick="openCategory('Maag')">
            <div class="card-icon">🫃</div>
            <h3>Maag</h3>
            <p>Daftar obat kategori maag.</p>
          </div>

          <div class="card category-card" onclick="openCategory('Sembelit')">
            <div class="card-icon">🌿</div>
            <h3>Sembelit</h3>
            <p>Daftar obat kategori sembelit.</p>
          </div>

          <div class="card category-card" onclick="openCategory('Diare')">
            <div class="card-icon">💧</div>
            <h3>Diare</h3>
            <p>Daftar obat kategori diare.</p>
          </div>

          <div class="card category-card" onclick="openCategory('Alergi')">
            <div class="card-icon">🤧</div>
            <h3>Alergi</h3>
            <p>Daftar obat kategori alergi.</p>
          </div>

          <div class="card category-card" onclick="openCategory('Flu dan Batuk')">
            <div class="card-icon">😷</div>
            <h3>Flu dan Batuk</h3>
            <p>Daftar obat flu dan batuk.</p>
          </div>

          <div class="card category-card" onclick="openCategory('Vitamin')">
            <div class="card-icon">🍊</div>
            <h3>Vitamin</h3>
            <p>Daftar vitamin.</p>
          </div>

        </div>

      </div>

    </div>

  </section>

</section>


<!-- =====================================================
     KESEHATAN
===================================================== -->

<section id="kesehatan" class="page">

  <section class="content">

    <div class="container">

      <div class="section-title">

        <h2>📚 Informasi Kesehatan</h2>

        <p>
          Edukasi kesehatan sederhana untuk membantu penggunaan
          obat dan menjaga kesehatan.
        </p>

      </div>

      <div id="healthList" class="grid">

      </div>

    </div>

  </section>

</section>


<!-- =====================================================
     KONSELING
===================================================== -->

<section id="konseling" class="page">

  <section class="content">

    <div class="container">

      <div class="section-title">

        <h2>🩺 Konseling Apoteker</h2>

        <p>
          Pilih apoteker untuk mengajukan pertanyaan mengenai obat
          dan penggunaan obat.
        </p>

      </div>

      <div id="pharmacistList" class="grid">

      </div>

      <div id="consultationContent"></div>

    </div>

  </section>

</section>


<!-- =====================================================
     INFORMASI PENTING
===================================================== -->

<section id="penting" class="page">

  <section class="content">

    <div class="container">

      <div class="section-title">

        <h2>⚠️ Informasi Penting tentang Antibiotik</h2>

        <p>
          Gunakan antibiotik secara tepat dan bertanggung jawab.
        </p>

      </div>

      <div class="info-box">

        <h3>💊 Apa itu antibiotik?</h3>

        <p>
          Antibiotik merupakan obat yang digunakan untuk mengatasi
          infeksi tertentu yang disebabkan oleh bakteri. Antibiotik
          tidak digunakan untuk mengobati penyakit yang disebabkan
          oleh virus seperti sebagian besar flu dan pilek.
        </p>

      </div>

      <div class="grid">

        <div class="card">
          <div class="card-icon">🦠</div>
          <h3>Untuk Infeksi Bakteri</h3>
          <p>
            Antibiotik digunakan untuk infeksi bakteri tertentu
            sesuai dengan diagnosis dan pertimbangan tenaga kesehatan.
          </p>
        </div>

        <div class="card">
          <div class="card-icon">🚫</div>
          <h3>Bukan untuk Flu</h3>
          <p>
            Antibiotik tidak digunakan untuk mengobati infeksi
            virus seperti flu biasa.
          </p>
        </div>

        <div class="card">
          <div class="card-icon">👨‍⚕️</div>
          <h3>Sesuai Resep Dokter</h3>
          <p>
            Antibiotik harus digunakan berdasarkan resep dan
            petunjuk dokter.
          </p>
        </div>

        <div class="card">
          <div class="card-icon">⏱️</div>
          <h3>Ikuti Aturan Penggunaan</h3>
          <p>
            Gunakan sesuai dosis dan lama penggunaan yang telah
            diresepkan.
          </p>
        </div>

      </div>

      <div class="warning-box">

        <h3>⚠️ Hal yang harus diperhatikan</h3>

        <ul style="padding-left:20px; margin-top:10px;">

          <li>
            Jangan menggunakan antibiotik tanpa resep dokter.
          </li>

          <li>
            Jangan menggunakan antibiotik sisa pengobatan sebelumnya.
          </li>

          <li>
            Jangan memberikan antibiotik kepada orang lain.
          </li>

          <li>
            Gunakan antibiotik sesuai dosis dan durasi yang diresepkan.
          </li>

          <li>
            Jangan menggandakan dosis secara sembarangan apabila
            lupa minum obat. Periksa petunjuk pada resep/kemasan
            atau konsultasikan kepada apoteker.
          </li>

          <li>
            Penggunaan antibiotik yang tidak tepat dapat berkontribusi
            terhadap terjadinya resistensi antibiotik.
          </li>

        </ul>

      </div>

      <div class="section-title" style="margin-top:45px;">

        <h2>Contoh Antibiotik</h2>

        <p>
          Klik salah satu obat untuk melihat informasi lebih lanjut.
        </p>

      </div>

      <div id="antibioticList" class="grid">

      </div>

      <div id="antibioticDetail"></div>

    </div>

  </section>

</section>


<!-- =====================================================
     KONTAK
===================================================== -->

<section id="kontak" class="page">

  <section class="content">

    <div class="container">

      <div class="section-title">

        <h2>📞 Kontak PharmaCare</h2>

        <p>
          Hubungi PharmaCare untuk mendapatkan informasi lebih lanjut.
        </p>

      </div>

      <div class="grid">

        <div class="card">
          <div class="card-icon">📱</div>
          <h3>WhatsApp</h3>
          <p>
            Konsultasi dan informasi dapat dilakukan melalui
            layanan komunikasi yang tersedia.
          </p>
        </div>

        <div class="card">
          <div class="card-icon">📧</div>
          <h3>Email</h3>
          <p>
            Silakan gunakan email resmi PharmaCare untuk pertanyaan
            dan informasi umum.
          </p>
        </div>

        <div class="card">
          <div class="card-icon">🩺</div>
          <h3>Konsultasi Apoteker</h3>
          <p>
            Pertanyaan mengenai obat dapat disampaikan melalui
            halaman Konseling Apoteker.
          </p>
        </div>

      </div>

    </div>

  </section>

</section>


<!-- =====================================================
     FOOTER
===================================================== -->

<footer>

  <h3>🌸 PharmaCare</h3>

  <p>
    Your Guide to Medicine & Health Consultation
  </p>

  <p style="margin-top:10px;">
    © 2026 PharmaCare. Website informasi obat dan kesehatan.
  </p>

</footer>


<script>

/* =====================================================
   DATA OBAT
===================================================== */

const medicines = [

  {
    id: 1,
    brand: "Paracetamol",
    active: "Paracetamol",
    strength: "500 mg",
    form: "Tablet",
    category: "Demam",
    class: "Analgesik-antipiretik",
    status: "Obat Bebas",
    indication: "Membantu menurunkan demam dan meredakan nyeri ringan sampai sedang.",
    contraindication: "Hipersensitivitas terhadap paracetamol dan kondisi tertentu sesuai pertimbangan tenaga kesehatan.",
    sideEffects: "Mual, ruam, atau reaksi alergi. Penggunaan berlebihan dapat menyebabkan kerusakan hati.",
    dosing: "Gunakan sesuai aturan pada kemasan atau petunjuk tenaga kesehatan.",
    use: "Diminum dengan air dan digunakan sesuai dosis yang dianjurkan.",
    storage: "Simpan pada tempat kering, terlindung dari cahaya dan jauh dari jangkauan anak.",
    warnings: "Jangan menggunakan melebihi dosis yang dianjurkan."
  },

  {
    id: 2,
    brand: "Sanmol",
    active: "Paracetamol",
    strength: "500 mg",
    form: "Tablet",
    category: "Demam",
    class: "Analgesik-antipiretik",
    status: "Obat Bebas",
    indication: "Membantu menurunkan demam dan meredakan nyeri ringan sampai sedang.",
    contraindication: "Hipersensitivitas terhadap paracetamol.",
    sideEffects: "Mual, ruam, dan reaksi alergi. Dosis berlebihan dapat menyebabkan kerusakan hati.",
    dosing: "Ikuti aturan penggunaan pada kemasan atau petunjuk tenaga kesehatan.",
    use: "Diminum dengan air.",
    storage: "Simpan di tempat kering dan terlindung dari cahaya.",
    warnings: "Hindari penggunaan bersamaan dengan obat lain yang juga mengandung paracetamol tanpa memperhatikan total dosis."
  },

  {
    id: 3,
    brand: "Promag",
    active: "Antasida",
    strength: "Tablet kunyah",
    form: "Tablet kunyah",
    category: "Maag",
    class: "Antasida",
    status: "Obat Bebas",
    indication: "Membantu meredakan gejala akibat kelebihan asam lambung seperti nyeri ulu hati.",
    contraindication: "Hipersensitivitas terhadap komponen obat.",
    sideEffects: "Gangguan saluran pencernaan dapat terjadi.",
    dosing: "Gunakan sesuai aturan pada kemasan.",
    use: "Dikunyah sesuai petunjuk penggunaan.",
    storage: "Simpan pada tempat kering.",
    warnings: "Jika keluhan menetap atau memburuk, konsultasikan dengan tenaga kesehatan."
  },

  {
    id: 4,
    brand: "Diapet",
    active: "Ekstrak tanaman obat",
    strength: "Kapsul",
    form: "Kapsul",
    category: "Diare",
    class: "Antidiare",
    status: "Obat Tradisional",
    indication: "Membantu meredakan gejala diare.",
    contraindication: "Perhatikan komposisi dan kondisi pengguna sebelum digunakan.",
    sideEffects: "Dapat terjadi gangguan saluran pencernaan pada sebagian pengguna.",
    dosing: "Ikuti aturan penggunaan pada kemasan.",
    use: "Diminum dengan air.",
    storage: "Simpan pada tempat kering dan terlindung dari cahaya.",
    warnings: "Pada diare, perhatikan kecukupan cairan. Jika terdapat darah, demam tinggi, atau tanda dehidrasi, segera mencari pertolongan medis."
  },

  {
    id: 5,
    brand: "Cetirizine",
    active: "Cetirizine",
    strength: "10 mg",
    form: "Tablet",
    category: "Alergi",
    class: "Antihistamin",
    status: "Obat Bebas Terbatas",
    indication: "Membantu meredakan gejala alergi seperti bersin dan hidung berair.",
    contraindication: "Hipersensitivitas terhadap cetirizine atau komponen terkait.",
    sideEffects: "Mengantuk, sakit kepala, atau mulut kering.",
    dosing: "Gunakan sesuai aturan pada kemasan atau petunjuk tenaga kesehatan.",
    use: "Diminum dengan air.",
    storage: "Simpan pada tempat kering.",
    warnings: "Perhatikan kemungkinan kantuk setelah penggunaan."
  },

  {
    id: 6,
    brand: "OBH Combi",
    active: "Kombinasi bahan aktif sesuai varian",
    strength: "Sediaan sirup",
    form: "Sirup",
    category: "Flu dan Batuk",
    class: "Obat batuk dan flu",
    status: "Sesuai varian",
    indication: "Membantu meredakan gejala flu dan batuk sesuai jenis produknya.",
    contraindication: "Periksa komposisi dan kontraindikasi pada kemasan.",
    sideEffects: "Dapat terjadi kantuk atau gangguan pencernaan tergantung kandungan.",
    dosing: "Gunakan sesuai aturan pada kemasan.",
    use: "Gunakan sendok takar dan jangan melebihi dosis.",
    storage: "Simpan sesuai petunjuk pada kemasan.",
    warnings: "Periksa kandungan sebelum menggunakan bersama obat flu atau batuk lainnya."
  },

  {
    id: 7,
    brand: "Dulcolax",
    active: "Bisacodyl",
    strength: "5 mg",
    form: "Tablet salut enterik",
    category: "Sembelit",
    class: "Laksatif stimulan",
    status: "Obat Bebas Terbatas",
    indication: "Membantu mengatasi sembelit.",
    contraindication: "Tidak digunakan pada kondisi tertentu seperti sumbatan usus.",
    sideEffects: "Kram perut dan diare dapat terjadi.",
    dosing: "Gunakan sesuai aturan pada kemasan.",
    use: "Telan sesuai petunjuk dan jangan mengunyah tablet salut enterik.",
    storage: "Simpan pada tempat kering.",
    warnings: "Penggunaan jangka panjang tanpa pengawasan tidak dianjurkan."
  },

  {
    id: 8,
    brand: "Enervon-C",
    active: "Vitamin dan mineral",
    strength: "Sesuai komposisi produk",
    form: "Tablet",
    category: "Vitamin",
    class: "Multivitamin",
    status: "Suplemen",
    indication: "Membantu memenuhi kebutuhan vitamin dan mineral.",
    contraindication: "Perhatikan komposisi jika memiliki alergi terhadap bahan tertentu.",
    sideEffects: "Gangguan pencernaan dapat terjadi pada sebagian pengguna.",
    dosing: "Ikuti aturan penggunaan pada kemasan.",
    use: "Diminum dengan air.",
    storage: "Simpan pada tempat kering dan terlindung dari cahaya.",
    warnings: "Suplemen tidak menggantikan pola makan bergizi seimbang."
  }

];


/* =====================================================
   DATA INFORMASI KESEHATAN
===================================================== */

const healthArticles = [

  {
    id: 1,
    icon: "🥗",
    title: "Pola Hidup Sehat",
    text: "Pola hidup sehat dapat dilakukan melalui konsumsi makanan bergizi seimbang, aktivitas fisik, tidur cukup, menjaga kebersihan dan menghindari kebiasaan yang berisiko bagi kesehatan."
  },

  {
    id: 2,
    icon: "💊",
    title: "Penggunaan Obat yang Tepat",
    text: "Gunakan obat sesuai indikasi, dosis, aturan pakai dan lama penggunaan. Perhatikan informasi pada kemasan dan konsultasikan kepada apoteker jika terdapat hal yang belum dipahami."
  },

  {
    id: 3,
    icon: "📦",
    title: "Penyimpanan Obat",
    text: "Obat perlu disimpan sesuai petunjuk pada kemasan. Hindarkan obat dari panas, kelembapan dan cahaya berlebihan serta jauhkan dari jangkauan anak-anak."
  },

  {
    id: 4,
    icon: "🏷️",
    title: "Cara Membaca Label Obat",
    text: "Label obat dapat memberikan informasi mengenai nama obat, zat aktif, kekuatan, aturan penggunaan, peringatan, tanggal kedaluwarsa dan cara penyimpanan."
  },

  {
    id: 5,
    icon: "🏠",
    title: "Pengelolaan Obat di Rumah",
    text: "Simpan obat secara teratur dan periksa tanggal kedaluwarsa secara berkala. Pisahkan obat yang sudah rusak atau kedaluwarsa dan lakukan pembuangan sesuai ketentuan."
  },

  {
    id: 6,
    icon: "📚",
    title: "Golongan Obat",
    text: "Obat memiliki berbagai golongan berdasarkan ketentuan dan penggunaannya. Kenali informasi pada kemasan sebelum menggunakan obat."
  },

  {
    id: 7,
    icon: "💧",
    title: "Bentuk Sediaan Obat",
    text: "Obat tersedia dalam berbagai bentuk sediaan seperti tablet, kapsul, sirup, salep, krim, tetes dan bentuk lainnya. Setiap sediaan memiliki cara penggunaan yang berbeda."
  }

];


/* =====================================================
   DATA APOTEKER
===================================================== */

const pharmacists = [

  {
    name: "apt. Arlamadha Tri Wangsa, M.Farm",
    specialization: "Spesialis Farmasi Komunitas",
    experience: "7 tahun",
    status: "Online"
  },

  {
    name: "apt. Chandra Gardipta, M.Farm",
    specialization: "Spesialis Farmasi Klinik",
    experience: "10 tahun",
    status: "Online"
  },

  {
    name: "apt. Nastikah Syafitri, S.Farm",
    specialization: "Apoteker",
    experience: "4 tahun",
    status: "Online"
  }

];


/* =====================================================
   DATA ANTIBIOTIK
===================================================== */

const antibiotics = [

  {
    id: 1,
    brand: "Amoxicillin",
    active: "Amoxicillin",
    class: "Antibiotik penisilin",
    form: "Kapsul",
    indication: "Digunakan untuk infeksi bakteri tertentu berdasarkan diagnosis dan resep dokter.",
    use: "Gunakan sesuai dosis dan durasi yang diresepkan dokter.",
    sideEffects: "Mual, diare, ruam atau reaksi alergi.",
    warnings: "Tidak digunakan untuk flu atau infeksi virus. Jangan menggunakan sisa antibiotik."
  },

  {
    id: 2,
    brand: "Cefixime",
    active: "Cefixime",
    class: "Antibiotik sefalosporin",
    form: "Kapsul atau sirup",
    indication: "Digunakan untuk infeksi bakteri tertentu sesuai diagnosis dokter.",
    use: "Gunakan sesuai resep dan petunjuk tenaga kesehatan.",
    sideEffects: "Diare, mual, sakit perut atau reaksi alergi.",
    warnings: "Gunakan berdasarkan resep dokter dan jangan diberikan kepada orang lain."
  },

  {
    id: 3,
    brand: "Azithromycin",
    active: "Azithromycin",
    class: "Antibiotik makrolida",
    form: "Tablet atau kapsul",
    indication: "Digunakan untuk infeksi bakteri tertentu berdasarkan pertimbangan dokter.",
    use: "Gunakan sesuai resep dokter.",
    sideEffects: "Mual, diare, sakit perut dan reaksi alergi.",
    warnings: "Tidak digunakan untuk mengatasi flu biasa atau infeksi virus."
  }

];


/* =====================================================
   PINDAH HALAMAN
===================================================== */

function showPage(pageId) {

  document.querySelectorAll(".page").forEach(page => {
    page.classList.remove("active");
  });

  const page = document.getElementById(pageId);

  if (page) {
    page.classList.add("active");
  }

  window.scrollTo({
    top: 0,
    behavior: "smooth"
  });
}


/* =====================================================
   KATEGORI OBAT
===================================================== */

function openCategory(category) {

  showPage("obat");

  const result = medicines.filter(
    medicine => medicine.category === category
  );

  const container = document.getElementById("categoryContent");

  container.innerHTML = `

    <button class="back-btn" onclick="showPage('obat')">
      ← Kembali ke Kategori
    </button>

    <div class="section-title">

      <h2>${category}</h2>

      <p>
        Daftar obat dalam kategori ${category}.
      </p>

    </div>

    <div class="grid">

      ${result.map(createMedicineCard).join("")}

    </div>

  `;

}


/* =====================================================
   CARD OBAT
===================================================== */

function createMedicineCard(medicine) {

  return `

    <div class="card medicine-card">

      <img
        class="medicine-img"
        src="assets/obat/${medicine.brand.toLowerCase().replaceAll(" ", "-")}.jpg"
        alt="${medicine.brand}"
        onerror="this.style.display='none'"
      >

      <div class="medicine-content">

        <h3>${medicine.brand}</h3>

        <p class="active">
          ${medicine.active} - ${medicine.strength}
        </p>

        <p>
          <strong>Bentuk:</strong> ${medicine.form}
        </p>

        <p>
          <strong>Golongan:</strong> ${medicine.status}
        </p>

        <br>

        <button class="btn" onclick="openMedicine(${medicine.id})">
          Lihat Detail
        </button>

      </div>

    </div>

  `;

}


/* =====================================================
   DETAIL OBAT
===================================================== */

function openMedicine(id) {

  const medicine = medicines.find(item => item.id === id);

  if (!medicine) return;

  showPage("obat");

  const container = document.getElementById("categoryContent");

  container.innerHTML = `

    <button class="back-btn" onclick="openCategory('${medicine.category}')">
      ← Kembali ke ${medicine.category}
    </button>

    <div class="medicine-detail">

      <img
        class="detail-image"
        src="assets/obat/${medicine.brand.toLowerCase().replaceAll(" ", "-")}.jpg"
        alt="${medicine.brand}"
        onerror="this.style.display='none'"
      >

      <div class="section-title">

        <h2>${medicine.brand}</h2>

        <p>${medicine.active}</p>

      </div>

      <div class="detail-list">

        <div class="detail-item">
          <strong>Zat Aktif:</strong>
          ${medicine.active}
        </div>

        <div class="detail-item">
          <strong>Kekuatan:</strong>
          ${medicine.strength}
        </div>

        <div class="detail-item">
          <strong>Bentuk Sediaan:</strong>
          ${medicine.form}
        </div>

        <div class="detail-item">
          <strong>Golongan/Kelas:</strong>
          ${medicine.class}
        </div>

        <div class="detail-item">
          <strong>Status:</strong>
          ${medicine.status}
        </div>

        <div class="detail-item">
          <strong>Indikasi:</strong>
          ${medicine.indication}
        </div>

        <div class="detail-item">
          <strong>Kontraindikasi:</strong>
          ${medicine.contraindication}
        </div>

        <div class="detail-item">
          <strong>Efek Samping:</strong>
          ${medicine.sideEffects}
        </div>

        <div class="detail-item">
          <strong>Dosis:</strong>
          ${medicine.dosing}
        </div>

        <div class="detail-item">
          <strong>Cara Penggunaan:</strong>
          ${medicine.use}
        </div>

        <div class="detail-item">
          <strong>Penyimpanan:</strong>
          ${medicine.storage}
        </div>

        <div class="detail-item">
          <strong>Peringatan:</strong>
          ${medicine.warnings}
        </div>

      </div>

    </div>

  `;

}


/* =====================================================
   PENCARIAN OBAT
===================================================== */

function searchMedicine() {

  const keyword =
    document.getElementById("searchInput").value
    .trim()
    .toLowerCase();

  const resultBox =
    document.getElementById("searchResult");

  if (!keyword) {

    resultBox.innerHTML = `
      <div class="info-box">
        Silakan masukkan nama obat, zat aktif, atau kategori.
      </div>
    `;

    return;
  }

  const result = medicines.filter(medicine =>

    medicine.brand.toLowerCase().includes(keyword) ||

    medicine.active.toLowerCase().includes(keyword) ||

    medicine.category.toLowerCase().includes(keyword)

  );

  if (result.length === 0) {

    resultBox.innerHTML = `
      <div class="warning-box">
        Obat belum ditemukan. Silakan periksa kembali nama obat
        atau konsultasikan dengan apoteker.
      </div>
    `;

    return;
  }

  resultBox.innerHTML = `

    <div style="
      background:white;
      padding:20px;
      border-radius:18px;
      margin-top:20px;
      text-align:left;
    ">

      <h3 style="color:#914866;">
        Hasil pencarian
      </h3>

      <div style="margin-top:15px;">

        ${result.map(medicine => `

          <div style="
            padding:12px 0;
            border-bottom:1px solid #f1dce5;
          ">

            <strong>${medicine.brand}</strong>

            <br>

            <small>
              ${medicine.active} • ${medicine.category}
            </small>

            <br><br>

            <button
              class="btn"
              onclick="openMedicine(${medicine.id})"
            >
              Lihat Detail
            </button>

          </div>

        `).join("")}

      </div>

    </div>

  `;

}


/* =====================================================
   INFORMASI KESEHATAN
===================================================== */

function loadHealthArticles() {

  const container =
    document.getElementById("healthList");

  container.innerHTML = healthArticles.map(article => `

    <div class="card">

      <div class="card-icon">
        ${article.icon}
      </div>

      <h3>${article.title}</h3>

      <p>
        ${article.text}
      </p>

      <br>

      <button
        class="btn"
        onclick="openHealth(${article.id})"
      >
        Baca Selengkapnya
      </button>

    </div>

  `).join("");

}


function openHealth(id) {

  const article =
    healthArticles.find(item => item.id === id);

  if (!article) return;

  showPage("kesehatan");

  const container =
    document.getElementById("healthList");

  container.innerHTML = `

    <button
      class="back-btn"
      onclick="loadHealthArticles()"
    >
      ← Kembali
    </button>

    <div class="medicine-detail">

      <div class="section-title">

        <div style="font-size:50px;">
          ${article.icon}
        </div>

        <h2>${article.title}</h2>

      </div>

      <p>
        ${article.text}
      </p>

      <div class="info-box">

        <strong>Catatan:</strong>

        <p>
          Informasi pada halaman ini bersifat edukatif.
          Untuk kondisi kesehatan tertentu, konsultasikan
          dengan dokter atau apoteker.
        </p>

      </div>

    </div>

  `;

}


/* =====================================================
   APOTEKER
===================================================== */

function loadPharmacists() {

  const container =
    document.getElementById("pharmacistList");

  container.innerHTML = pharmacists.map((pharmacist, index) => `

    <div class="card pharmacist-card">

      <div class="avatar">
        🧑‍⚕️
      </div>

      <h3>
        ${pharmacist.name}
      </h3>

      <p>
        ${pharmacist.specialization}
      </p>

      <p>
        Pengalaman: ${pharmacist.experience}
      </p>

      <span class="status">
        ● ${pharmacist.status}
      </span>

      <br><br>

      <button
        class="btn"
        onclick="openCounselor(${index})"
      >
        Konsultasi
      </button>

    </div>

  `).join("");

}


function openCounselor(index) {

  const pharmacist = pharmacists[index];

  const container =
    document.getElementById("consultationContent");

  container.innerHTML = `

    <div class="form-card" style="margin-top:35px;">

      <button
        class="back-btn"
        onclick="document.getElementById('consultationContent').innerHTML=''"
      >
        ← Tutup
      </button>

      <div class="section-title">

        <h2>Konsultasi dengan Apoteker</h2>

        <p>
          ${pharmacist.name}
        </p>

      </div>

      <div class="info-box">

        <strong>Spesialisasi:</strong>
        ${pharmacist.specialization}

        <br>

        <strong>Pengalaman:</strong>
        ${pharmacist.experience}

        <br>

        <strong>Status:</strong>
        ${pharmacist.status}

      </div>

      <div class="form-group">

        <label>
          Nama Anda
        </label>

        <input
          type="text"
          id="consultName"
          placeholder="Masukkan nama"
        >

      </div>

      <div class="form-group">

        <label>
          Pertanyaan
        </label>

        <textarea
          id="consultQuestion"
          rows="6"
          placeholder="Tuliskan pertanyaan mengenai obat atau kesehatan..."
        ></textarea>

      </div>

      <button
        class="btn"
        onclick="sendQuestion('${pharmacist.name}')"
      >
        💬 Kirim Pertanyaan
      </button>

      <div id="consultMessage"></div>

    </div>

  `;

  setTimeout(() => {

    document.getElementById("consultationContent")
      .scrollIntoView({
        behavior: "smooth"
      });

  }, 100);

}


function sendQuestion(apoteker) {

  const name =
    document.getElementById("consultName").value.trim();

  const question =
    document.getElementById("consultQuestion").value.trim();

  const message =
    document.getElementById("consultMessage");

  if (!name || !question) {

    message.innerHTML = `
      <div class="warning-box">
        Nama dan pertanyaan harus diisi.
      </div>
    `;

    return;
  }

  message.innerHTML = `

    <div class="info-box">

      <strong>Pertanyaan berhasil dicatat.</strong>

      <p>
        Terima kasih ${name}. Pertanyaan Anda telah
        disiapkan untuk konsultasi dengan ${apoteker}.
      </p>

    </div>

  `;

}


/* =====================================================
   ANTIBIOTIK
===================================================== */

function loadAntibiotics() {

  const container =
    document.getElementById("antibioticList");

  container.innerHTML = antibiotics.map(item => `

    <div class="card">

      <div class="card-icon">
        💊
      </div>

      <h3>${item.brand}</h3>

      <p>
        <strong>Zat aktif:</strong>
        ${item.active}
      </p>

      <p>
        <strong>Kelas:</strong>
        ${item.class}
      </p>

      <br>

      <button
        class="btn"
        onclick="openAntibiotic(${item.id})"
      >
        Lihat Informasi
      </button>

    </div>

  `).join("");

}


function openAntibiotic(id) {

  const item =
    antibiotics.find(item => item.id === id);

  if (!item) return;

  const container =
    document.getElementById("antibioticDetail");

  container.innerHTML = `

    <div class="medicine-detail" style="margin-top:30px;">

      <button
        class="back-btn"
        onclick="document.getElementById('antibioticDetail').innerHTML=''"
      >
        ← Tutup
      </button>

      <div class="section-title">

        <h2>${item.brand}</h2>

        <p>${item.active}</p>

      </div>

      <div class="detail-list">

        <div class="detail-item">
          <strong>Kelas Antibiotik:</strong>
          ${item.class}
        </div>

        <div class="detail-item">
          <strong>Bentuk Sediaan:</strong>
          ${item.form}
        </div>

        <div class="detail-item">
          <strong>Indikasi:</strong>
          ${item.indication}
        </div>

        <div class="detail-item">
          <strong>Cara Penggunaan:</strong>
          ${item.use}
        </div>

        <div class="detail-item">
          <strong>Efek Samping:</strong>
          ${item.sideEffects}
        </div>

        <div class="detail-item">
          <strong>Peringatan:</strong>
          ${item.warnings}
        </div>

      </div>

      <div class="warning-box">

        <h3>⚠️ Perhatikan</h3>

        <p>
          Antibiotik harus digunakan berdasarkan resep dan
          petunjuk dokter. Jangan menggunakan antibiotik
          secara sembarangan, menggunakan sisa obat, atau
          memberikannya kepada orang lain.
        </p>

      </div>

      <button
        class="btn"
        onclick="showPage('konseling')"
      >
        🩺 Konsultasikan dengan Apoteker
      </button>

    </div>

  `;

  setTimeout(() => {

    container.scrollIntoView({
      behavior: "smooth"
    });

  }, 100);

}


/* =====================================================
   LOAD AWAL
===================================================== */

window.onload = function() {

  loadHealthArticles();

  loadPharmacists();

  loadAntibiotics();

};

</script>

</body>
</html>
