```html
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>PharmaCare | Your Guide to Medicine & Health Consultation</title>

<style>
:root {
    --pink: #d98fa5;
    --dusty: #c98a9d;
    --light-pink: #fdf0f4;
    --soft-pink: #f8dce5;
    --dark-pink: #a95f78;
    --white: #ffffff;
    --text: #4b3b40;
    --muted: #806d73;
    --border: #efd3dc;
    --shadow: 0 8px 25px rgba(170, 100, 125, 0.12);
}

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background: #fffafb;
    color: var(--text);
    line-height: 1.7;
}

/* ================= NAVBAR ================= */

.navbar {
    position: sticky;
    top: 0;
    z-index: 1000;
    background: rgba(255,255,255,0.96);
    border-bottom: 1px solid var(--border);
    box-shadow: 0 3px 15px rgba(0,0,0,0.04);
}

.nav-container {
    max-width: 1200px;
    margin: auto;
    padding: 15px 25px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.logo {
    font-size: 25px;
    font-weight: bold;
    color: var(--dark-pink);
    cursor: pointer;
}

.logo span {
    color: #6f5961;
}

.nav-links {
    display: flex;
    list-style: none;
    gap: 8px;
    align-items: center;
}

.nav-links button {
    border: none;
    background: transparent;
    padding: 9px 12px;
    border-radius: 10px;
    cursor: pointer;
    color: var(--text);
    font-size: 14px;
}

.nav-links button:hover {
    background: var(--soft-pink);
    color: var(--dark-pink);
}

.login-nav {
    background: var(--dark-pink) !important;
    color: white !important;
}

.menu-btn {
    display: none;
    border: none;
    background: var(--soft-pink);
    color: var(--dark-pink);
    padding: 8px 12px;
    border-radius: 8px;
    font-size: 20px;
    cursor: pointer;
}

/* ================= GENERAL ================= */

.container {
    max-width: 1150px;
    margin: auto;
    padding: 0 20px;
}

.page {
    display: none;
    min-height: 75vh;
    padding: 55px 0;
}

.page.active {
    display: block;
}

.section-title {
    text-align: center;
    margin-bottom: 35px;
}

.section-title h2 {
    font-size: 30px;
    color: var(--dark-pink);
    margin-bottom: 8px;
}

.section-title p {
    color: var(--muted);
}

/* ================= HOME ================= */

.hero {
    min-height: 550px;
    display: flex;
    align-items: center;
    background:
        radial-gradient(circle at 85% 20%, #f7dce5 0, transparent 28%),
        linear-gradient(135deg, #fff8fa, #fdf0f4);
}

.hero-content {
    max-width: 1150px;
    width: 100%;
    margin: auto;
    padding: 70px 25px;
    display: grid;
    grid-template-columns: 1.2fr 0.8fr;
    gap: 50px;
    align-items: center;
}

.hero h1 {
    font-size: 52px;
    color: var(--dark-pink);
    margin-bottom: 10px;
}

.tagline {
    font-size: 20px;
    font-weight: bold;
    color: #765b64;
    margin-bottom: 18px;
}

.hero p {
    color: var(--muted);
    margin-bottom: 25px;
    max-width: 650px;
}

.hero-illustration {
    background: white;
    border-radius: 35px;
    padding: 40px;
    text-align: center;
    box-shadow: var(--shadow);
    border: 1px solid var(--border);
}

.hero-icon {
    font-size: 110px;
    margin-bottom: 15px;
}

.search-box {
    display: flex;
    background: white;
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 6px;
    max-width: 650px;
    box-shadow: var(--shadow);
}

.search-box input {
    flex: 1;
    border: none;
    outline: none;
    padding: 13px;
    font-size: 15px;
}

.btn {
    background: var(--dark-pink);
    color: white;
    border: none;
    padding: 12px 20px;
    border-radius: 10px;
    cursor: pointer;
    font-weight: bold;
    transition: .2s;
}

.btn:hover {
    transform: translateY(-2px);
    background: #914f68;
}

.btn-light {
    background: var(--soft-pink);
    color: var(--dark-pink);
}

/* ================= CARDS ================= */

.grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 18px;
}

.card {
    background: white;
    border: 1px solid var(--border);
    border-radius: 17px;
    padding: 22px;
    box-shadow: var(--shadow);
    transition: .25s;
}

.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 12px 30px rgba(170, 100, 125, 0.18);
}

.clickable {
    cursor: pointer;
}

.card-icon {
    font-size: 38px;
    margin-bottom: 12px;
}

.card h3 {
    color: var(--dark-pink);
    margin-bottom: 7px;
}

.card p {
    font-size: 14px;
    color: var(--muted);
}

/* ================= CATEGORY ================= */

.category-grid {
    grid-template-columns: repeat(4, 1fr);
}

.category-card {
    text-align: center;
    cursor: pointer;
}

.category-card .card-icon {
    font-size: 42px;
}

/* ================= MEDICINE LIST ================= */

.back-btn {
    margin-bottom: 25px;
}

.medicine-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 22px;
}

.medicine-card {
    overflow: hidden;
    padding: 0;
}

.medicine-image {
    width: 100%;
    height: 190px;
    object-fit: contain;
    background: #fff6f8;
    padding: 20px;
}

.medicine-content {
    padding: 20px;
}

.badge {
    display: inline-block;
    background: var(--soft-pink);
    color: var(--dark-pink);
    padding: 4px 10px;
    border-radius: 20px;
    font-size: 12px;
    margin: 7px 0;
}

/* ================= DETAIL ================= */

.detail-box {
    background: white;
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 30px;
    box-shadow: var(--shadow);
}

.detail-header {
    display: grid;
    grid-template-columns: 300px 1fr;
    gap: 35px;
    align-items: center;
    margin-bottom: 30px;
}

.detail-image {
    width: 100%;
    height: 280px;
    object-fit: contain;
    background: #fff6f8;
    border-radius: 15px;
    padding: 20px;
}

.info-list {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 15px;
}

.info-item {
    background: #fff8fa;
    border-radius: 12px;
    padding: 15px;
}

.info-item strong {
    display: block;
    color: var(--dark-pink);
    margin-bottom: 4px;
}

/* ================= HEALTH ================= */

.health-grid {
    grid-template-columns: repeat(3, 1fr);
}

/* ================= PHARMACIST ================= */

.pharmacist-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

.profile {
    text-align: center;
}

.profile-photo {
    width: 100px;
    height: 100px;
    margin: 0 auto 15px;
    border-radius: 50%;
    background: var(--soft-pink);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 42px;
}

.online {
    color: #3b9b67;
    font-weight: bold;
    font-size: 13px;
}

/* ================= FORM ================= */

.form-box {
    max-width: 650px;
    margin: auto;
    background: white;
    padding: 30px;
    border-radius: 20px;
    border: 1px solid var(--border);
    box-shadow: var(--shadow);
}

.form-group {
    margin-bottom: 18px;
}

.form-group label {
    display: block;
    margin-bottom: 7px;
    font-weight: bold;
}

.form-group input,
.form-group textarea {
    width: 100%;
    padding: 13px;
    border: 1px solid var(--border);
    border-radius: 10px;
    outline: none;
    font-family: inherit;
}

.form-group textarea {
    min-height: 150px;
    resize: vertical;
}

.form-group input:focus,
.form-group textarea:focus {
    border-color: var(--pink);
}

/* ================= ANTIBIOTIC ================= */

.warning {
    background: #fff2f2;
    border-left: 5px solid #c56a6a;
    padding: 20px;
    border-radius: 10px;
    margin-bottom: 25px;
}

.warning strong {
    color: #a24e4e;
}

.antibiotic-list {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
}

/* ================= FOOTER ================= */

footer {
    background: #4f3c43;
    color: white;
    padding: 35px 20px;
    margin-top: 30px;
}

.footer-content {
    max-width: 1150px;
    margin: auto;
    text-align: center;
}

.footer-content h3 {
    color: #f5cbd7;
    margin-bottom: 7px;
}

.footer-content p {
    color: #e7dce0;
    font-size: 14px;
}

/* ================= NOTIFICATION ================= */

.toast {
    position: fixed;
    bottom: 25px;
    right: 25px;
    background: #4f3c43;
    color: white;
    padding: 15px 20px;
    border-radius: 10px;
    display: none;
    z-index: 2000;
}

/* ================= RESPONSIVE ================= */

@media (max-width: 900px) {

    .grid,
    .category-grid {
        grid-template-columns: repeat(2, 1fr);
    }

    .medicine-grid,
    .pharmacist-grid,
    .health-grid {
        grid-template-columns: repeat(2, 1fr);
    }

    .hero-content {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .search-box {
        margin: auto;
    }

    .detail-header {
        grid-template-columns: 1fr;
    }
}

@media (max-width: 700px) {

    .nav-container {
        padding: 13px 18px;
    }

    .menu-btn {
        display: block;
    }

    .nav-links {
        display: none;
        position: absolute;
        top: 65px;
        left: 0;
        width: 100%;
        background: white;
        padding: 15px;
        flex-direction: column;
        border-bottom: 1px solid var(--border);
    }

    .nav-links.show {
        display: flex;
    }

    .nav-links button {
        width: 100%;
        padding: 12px;
    }

    .hero h1 {
        font-size: 38px;
    }

    .tagline {
        font-size: 17px;
    }

    .grid,
    .category-grid,
    .medicine-grid,
    .pharmacist-grid,
    .health-grid,
    .antibiotic-list {
        grid-template-columns: 1fr;
    }

    .info-list {
        grid-template-columns: 1fr;
    }

    .page {
        padding: 35px 0;
    }

    .section-title h2 {
        font-size: 25px;
    }
}
</style>
</head>

<body>

<!-- ================= NAVIGATION ================= -->

<nav class="navbar">
    <div class="nav-container">

        <div class="logo" onclick="showPage('home')">
            💊 Pharma<span>Care</span>
        </div>

        <button class="menu-btn" onclick="toggleMenu()">☰</button>

        <ul class="nav-links" id="navLinks">
            <li><button onclick="showPage('home')">Home</button></li>
            <li><button onclick="showPage('obat')">Obat</button></li>
            <li><button onclick="showPage('kesehatan')">Informasi Kesehatan</button></li>
            <li><button onclick="showPage('konseling')">Konseling Apoteker</button></li>
            <li><button onclick="showPage('antibiotik')">Informasi Penting</button></li>
            <li><button class="login-nav" onclick="showPage('login')">Login</button></li>
        </ul>

    </div>
</nav>


<!-- ================= HOME ================= -->

<section id="home" class="page active">

    <div class="hero">

        <div class="hero-content">

            <div>

                <h1>PharmaCare</h1>

                <div class="tagline">
                    Your Guide to Medicine & Health Consultation
                </div>

                <p>
                    PharmaCare merupakan website informasi obat dan kesehatan
                    yang dirancang untuk membantu masyarakat memperoleh informasi
                    mengenai obat, penggunaan obat yang benar, kesehatan,
                    serta konsultasi dengan apoteker.
                </p>

                <div class="search-box">

                    <input
                        type="text"
                        id="homeSearch"
                        placeholder="Cari nama obat, zat aktif, atau kategori..."
                        onkeydown="if(event.key==='Enter') searchMedicine()">

                    <button class="btn" onclick="searchMedicine()">
                        🔍 Cari Obat
                    </button>

                </div>

                <br>

                <button class="btn" onclick="showPage('obat')">
                    💊 Lihat Kategori Obat
                </button>

                <button class="btn btn-light" onclick="showPage('konseling')">
                    👩‍⚕️ Konsultasi Apoteker
                </button>

            </div>

            <div class="hero-illustration">
                <div class="hero-icon">💊🩺</div>
                <h3>Informasi Obat & Kesehatan</h3>
                <p>
                    Temukan informasi obat dan panduan kesehatan
                    secara mudah dan informatif.
                </p>
            </div>

        </div>

    </div>


    <div class="container">

        <br><br>

        <div class="section-title">
            <h2>Kategori Obat</h2>
            <p>Pilih kategori untuk melihat daftar obat.</p>
        </div>

        <div class="grid category-grid">

            <div class="card category-card" onclick="showCategory('Demam')">
                <div class="card-icon">🌡️</div>
                <h3>Demam</h3>
                <p>Obat untuk membantu meredakan demam.</p>
            </div>

            <div class="card category-card" onclick="showCategory('Nyeri')">
                <div class="card-icon">🩹</div>
                <h3>Nyeri</h3>
                <p>Informasi obat untuk keluhan nyeri.</p>
            </div>

            <div class="card category-card" onclick="showCategory('Maag')">
                <div class="card-icon">🫃</div>
                <h3>Maag</h3>
                <p>Informasi obat untuk keluhan lambung.</p>
            </div>

            <div class="card category-card" onclick="showCategory('Sembelit')">
                <div class="card-icon">🌿</div>
                <h3>Sembelit</h3>
                <p>Informasi mengenai obat pencahar.</p>
            </div>

            <div class="card category-card" onclick="showCategory('Diare')">
                <div class="card-icon">💧</div>
                <h3>Diare</h3>
                <p>Informasi penanganan diare.</p>
            </div>

            <div class="card category-card" onclick="showCategory('Alergi')">
                <div class="card-icon">🤧</div>
                <h3>Alergi</h3>
                <p>Informasi obat untuk gejala alergi.</p>
            </div>

            <div class="card category-card" onclick="showCategory('Flu dan Batuk')">
                <div class="card-icon">😷</div>
                <h3>Flu dan Batuk</h3>
                <p>Informasi obat untuk flu dan batuk.</p>
            </div>

            <div class="card category-card" onclick="showCategory('Vitamin')">
                <div class="card-icon">🍊</div>
                <h3>Vitamin</h3>
                <p>Informasi mengenai berbagai vitamin.</p>
            </div>

        </div>

    </div>

</section>


<!-- ================= OBAT ================= -->

<section id="obat" class="page">

    <div class="container">

        <div class="section-title">
            <h2>💊 Informasi Obat</h2>
            <p>Pilih kategori obat yang ingin Anda ketahui.</p>
        </div>

        <div class="grid category-grid">

            <div class="card category-card" onclick="showCategory('Demam')">
                <div class="card-icon">🌡️</div>
                <h3>Demam</h3>
            </div>

            <div class="card category-card" onclick="showCategory('Nyeri')">
                <div class="card-icon">🩹</div>
                <h3>Nyeri</h3>
            </div>

            <div class="card category-card" onclick="showCategory('Maag')">
                <div class="card-icon">🫃</div>
                <h3>Maag</h3>
            </div>

            <div class="card category-card" onclick="showCategory('Sembelit')">
                <div class="card-icon">🌿</div>
                <h3>Sembelit</h3>
            </div>

            <div class="card category-card" onclick="showCategory('Diare')">
                <div class="card-icon">💧</div>
                <h3>Diare</h3>
            </div>

            <div class="card category-card" onclick="showCategory('Alergi')">
                <div class="card-icon">🤧</div>
                <h3>Alergi</h3>
            </div>

            <div class="card category-card" onclick="showCategory('Flu dan Batuk')">
                <div class="card-icon">😷</div>
                <h3>Flu dan Batuk</h3>
            </div>

            <div class="card category-card" onclick="showCategory('Vitamin')">
                <div class="card-icon">🍊</div>
                <h3>Vitamin</h3>
            </div>

        </div>

    </div>

</section>


<!-- ================= DAFTAR OBAT ================= -->

<section id="daftar-obat" class="page">

    <div class="container">

        <button class="btn back-btn" onclick="showPage('obat')">
            ← Kembali ke Kategori
        </button>

        <div class="section-title">
            <h2 id="categoryTitle">Daftar Obat</h2>
            <p id="categoryDescription"></p>
        </div>

        <div id="medicineList" class="medicine-grid"></div>

    </div>

</section>


<!-- ================= DETAIL OBAT ================= -->

<section id="detail-obat" class="page">

    <div class="container">

        <button class="btn back-btn" onclick="goBackToMedicineList()">
            ← Kembali ke Daftar Obat
        </button>

        <div id="medicineDetail"></div>

    </div>

</section>


<!-- ================= KESEHATAN ================= -->

<section id="kesehatan" class="page">

    <div class="container">

        <div class="section-title">
            <h2>🩺 Informasi Kesehatan</h2>
            <p>Pelajari berbagai informasi dasar mengenai kesehatan dan obat.</p>
        </div>

        <div class="grid health-grid">

            <div class="card clickable" onclick="showHealthDetail('Pola Hidup Sehat')">
                <div class="card-icon">🥗</div>
                <h3>Pola Hidup Sehat</h3>
                <p>Pedoman sederhana untuk menjaga kesehatan.</p>
            </div>

            <div class="card clickable" onclick="showHealthDetail('Cara Konsumsi Obat yang Benar')">
                <div class="card-icon">💊</div>
                <h3>Cara Konsumsi Obat yang Benar</h3>
                <p>Ketahui cara menggunakan obat secara tepat.</p>
            </div>

            <div class="card clickable" onclick="showHealthDetail('Cara Menyimpan Obat')">
                <div class="card-icon">📦</div>
                <h3>Cara Menyimpan Obat</h3>
                <p>Tips menyimpan obat agar kualitasnya tetap terjaga.</p>
            </div>

            <div class="card clickable" onclick="showHealthDetail('Cara Membaca Etiket Obat')">
                <div class="card-icon">🏷️</div>
                <h3>Cara Membaca Etiket Obat</h3>
                <p>Kenali informasi penting pada etiket obat.</p>
            </div>

            <div class="card clickable" onclick="showHealthDetail('Pengelolaan Obat di Rumah')">
                <div class="card-icon">🏠</div>
                <h3>Pengelolaan Obat di Rumah</h3>
                <p>Kelola persediaan obat dengan aman.</p>
            </div>

            <div class="card clickable" onclick="showHealthDetail('Mengenal Golongan Obat')">
                <div class="card-icon">📚</div>
                <h3>Mengenal Golongan Obat</h3>
                <p>Kenali perbedaan status dan penggunaan obat.</p>
            </div>

            <div class="card clickable" onclick="showHealthDetail('Bentuk Sediaan Obat')">
                <div class="card-icon">💧</div>
                <h3>Bentuk Sediaan Obat</h3>
                <p>Tablet, kapsul, sirup, salep, dan bentuk lainnya.</p>
            </div>

        </div>

    </div>

</section>


<!-- ================= DETAIL KESEHATAN ================= -->

<section id="detail-kesehatan" class="page">

    <div class="container">

        <button class="btn back-btn" onclick="showPage('kesehatan')">
            ← Kembali
        </button>

        <div class="detail-box">

            <div class="section-title">
                <h2 id="healthTitle"></h2>
            </div>

            <div id="healthContent"></div>

        </div>

    </div>

</section>


<!-- ================= KONSELING ================= -->

<section id="konseling" class="page">

    <div class="container">

        <div class="section-title">
            <h2>👩‍⚕️ Konseling Apoteker</h2>
            <p>Pilih apoteker untuk memulai konsultasi.</p>
        </div>

        <div class="pharmacist-grid">

            <div class="card profile clickable" onclick="openConsultation(0)">
                <div class="profile-photo">👩‍⚕️</div>
                <h3>apt. Arlamadha Tri Wangsa, M.Farm</h3>
                <p>Spesialis Farmasi Komunitas</p>
                <p>Pengalaman 7 tahun</p>
                <div class="online">● Online</div>
            </div>

            <div class="card profile clickable" onclick="openConsultation(1)">
                <div class="profile-photo">👨‍⚕️</div>
                <h3>apt. Chandra Gardipta, M.Farm</h3>
                <p>Spesialis Farmasi Klinik</p>
                <p>Pengalaman 10 tahun</p>
                <div class="online">● Online</div>
            </div>

            <div class="card profile clickable" onclick="openConsultation(2)">
                <div class="profile-photo">👩‍⚕️</div>
                <h3>apt. Nastikah Syafitri, S.Farm</h3>
                <p>Apoteker</p>
                <p>Pengalaman 4 tahun</p>
                <div class="online">● Online</div>
            </div>

        </div>

    </div>

</section>


<!-- ================= FORM KONSELING ================= -->

<section id="form-konseling" class="page">

    <div class="container">

        <button class="btn back-btn" onclick="showPage('konseling')">
            ← Kembali
        </button>

        <div class="form-box">

            <div class="section-title">
                <h2>💬 Konsultasi Apoteker</h2>
            </div>

            <div id="pharmacistInfo"></div>

            <br>

            <form onsubmit="sendQuestion(event)">

                <div class="form-group">
                    <label>Nama Pengguna</label>
                    <input type="text" id="consultName" required>
                </div>

                <div class="form-group">
                    <label>Pertanyaan</label>
                    <textarea id="consultQuestion" required
                    placeholder="Tuliskan pertanyaan mengenai obat atau kesehatan..."></textarea>
                </div>

                <button class="btn" type="submit">
                    Kirim Pertanyaan
                </button>

            </form>

        </div>

    </div>

</section>


<!-- ================= ANTIBIOTIK ================= -->

<section id="antibiotik" class="page">

    <div class="container">

        <div class="section-title">
            <h2>⚠️ Informasi Penting — Antibiotik</h2>
            <p>Gunakan antibiotik secara bijak dan sesuai resep dokter.</p>
        </div>

        <div class="warning">

            <strong>⚠️ Penting tentang antibiotik</strong>

            <p>
                Antibiotik merupakan obat keras yang penggunaannya harus
                berdasarkan resep dokter. Antibiotik digunakan untuk menangani
                infeksi bakteri tertentu dan bukan untuk mengobati flu atau
                penyakit yang disebabkan oleh virus.
            </p>

            <br>

            <p>
                Jangan menggunakan antibiotik secara sembarangan, jangan
                menggunakan sisa antibiotik sebelumnya, dan jangan memberikan
                antibiotik kepada orang lain.
            </p>

            <br>

            <p>
                Antibiotik harus digunakan sesuai dosis dan durasi yang
                diresepkan dokter. Jika dokter memberikan antibiotik untuk
                digunakan selama durasi tertentu, terapi perlu diselesaikan
                sesuai resep meskipun gejala sudah membaik.
            </p>

            <br>

            <p>
                Penggunaan antibiotik yang tidak tepat dapat berkontribusi
                terhadap resistensi antibiotik.
            </p>

            <br>

            <p>
                Jika lupa minum antibiotik, ikuti petunjuk pada etiket atau
                resep maupun konsultasikan dengan apoteker. Jangan menggandakan
                dosis secara sembarangan.
            </p>

        </div>

        <div class="antibiotic-list">

            <div class="card">

                <div class="card-icon">💊</div>

                <h3>Amoxsan</h3>

                <span class="badge">
                    Obat Keras — Antibiotik
                </span>

                <p><strong>Zat aktif:</strong> Amoksisilin</p>
                <p><strong>Golongan:</strong> Penisilin</p>
                <p><strong>Bentuk:</strong> Kapsul</p>
                <p><strong>Indikasi:</strong> Infeksi bakteri yang sensitif terhadap amoksisilin sesuai diagnosis dokter.</p>
                <p><strong>Efek samping:</strong> Mual, diare, ruam, reaksi alergi.</p>
                <p><strong>Peringatan:</strong> Perhatikan riwayat alergi terhadap penisilin atau antibiotik beta-laktam.</p>
                <p><strong>Penggunaan:</strong> Sesuai dosis dan durasi yang ditentukan dokter.</p>

                <br>

                <button class="btn" onclick="showAntibioticDetail('Amoxsan')">
                    Lihat Detail
                </button>

            </div>


            <div class="card">

                <div class="card-icon">💊</div>

                <h3>Zibramax</h3>

                <span class="badge">
                    Obat Keras — Antibiotik
                </span>

                <p><strong>Zat aktif:</strong> Azitromisin</p>
                <p><strong>Golongan:</strong> Makrolida</p>
                <p><strong>Bentuk:</strong> Tablet</p>
                <p><strong>Indikasi:</strong> Infeksi bakteri tertentu sesuai diagnosis dan resep dokter.</p>
                <p><strong>Efek samping:</strong> Mual, diare, nyeri perut.</p>
                <p><strong>Peringatan:</strong> Informasikan kepada dokter/apoteker mengenai obat lain yang sedang digunakan.</p>
                <p><strong>Penggunaan:</strong> Sesuai resep dokter dan petunjuk pada etiket.</p>

                <br>

                <button class="btn" onclick="showAntibioticDetail('Zibramax')">
                    Lihat Detail
                </button>

            </div>

        </div>

    </div>

</section>


<!-- ================= DETAIL ANTIBIOTIK ================= -->

<section id="detail-antibiotik" class="page">

    <div class="container">

        <button class="btn back-btn" onclick="showPage('antibiotik')">
            ← Kembali
        </button>

        <div id="antibioticDetail"></div>

    </div>

</section>


<!-- ================= LOGIN ================= -->

<section id="login" class="page">

    <div class="container">

        <div class="form-box">

            <div class="section-title">

                <h2>🔐 Login PharmaCare</h2>

                <p>
                    Masukkan nama lengkap untuk melanjutkan.
                </p>

            </div>

            <form onsubmit="loginUser(event)">

                <div class="form-group">

                    <label>Nama Lengkap</label>

                    <input
                        type="text"
                        id="loginName"
                        placeholder="Masukkan nama lengkap"
                        required>

                </div>

                <button class="btn" type="submit">
                    Masuk
                </button>

            </form>

        </div>

    </div>

</section>


<!-- ================= FOOTER ================= -->

<footer>

    <div class="footer-content">

        <h3>💊 PharmaCare</h3>

        <p>
            Your Guide to Medicine & Health Consultation
        </p>

        <br>

        <p>
            Konten website ini bersifat edukatif dan tidak menggantikan
            pemeriksaan atau diagnosis tenaga kesehatan.
        </p>

        <p>
            Untuk kondisi yang membutuhkan pemeriksaan langsung,
            konsultasikan dengan apoteker atau dokter.
        </p>

        <br>

        <p>
            © 2026 PharmaCare. All Rights Reserved.
        </p>

    </div>

</footer>


<div class="toast" id="toast"></div>


<script>

/* =====================================================
   DATABASE OBAT
===================================================== */

const medicines = [

    {
        id: "sanmol",
        name: "Sanmol",
        active: "Paracetamol",
        strength: "500 mg",
        form: "Tablet",
        status: "Obat Bebas",
        category: "Demam",
        indication: "Meredakan demam dan nyeri ringan sampai sedang.",
        contraindication: "Hipersensitivitas terhadap paracetamol. Penggunaan pada gangguan hati perlu perhatian tenaga kesehatan.",
        sideEffect: "Mual, reaksi kulit, dan pada penggunaan berlebihan dapat menyebabkan kerusakan hati.",
        dosage: "Ikuti dosis pada etiket atau anjuran tenaga kesehatan.",
        usage: "Diminum dengan air. Jangan menggunakan lebih dari dosis yang dianjurkan.",
        storage: "Simpan di tempat kering, terlindung dari cahaya langsung dan jauh dari jangkauan anak.",
        warning: "Jangan menggunakan beberapa produk yang sama-sama mengandung paracetamol secara bersamaan tanpa memperhatikan jumlah total dosis.",
        interaction: "Dapat berinteraksi dengan obat tertentu. Informasikan obat lain yang sedang digunakan kepada apoteker/dokter.",
        image: "assets/obat/sanmol.jpg"
    },

    {
        id: "panadol",
        name: "Panadol",
        active: "Paracetamol",
        strength: "500 mg",
        form: "Kaplet",
        status: "Obat Bebas",
        category: "Demam",
        indication: "Membantu meredakan demam dan nyeri ringan sampai sedang.",
        contraindication: "Hipersensitivitas terhadap kandungan obat.",
        sideEffect: "Reaksi alergi dan gangguan hati jika digunakan secara berlebihan.",
        dosage: "Sesuai petunjuk pada kemasan atau anjuran tenaga kesehatan.",
        usage: "Diminum dengan air sesuai aturan penggunaan.",
        storage: "Simpan pada suhu ruang dan terlindung dari kelembapan.",
        warning: "Jangan melebihi dosis yang dianjurkan.",
        interaction: "Beritahu apoteker/dokter mengenai obat lain yang sedang digunakan.",
        image: "assets/obat/panadol.jpg"
    },

    {
        id: "bodrex",
        name: "Bodrex",
        active: "Paracetamol",
        strength: "500 mg",
        form: "Kaplet",
        status: "Obat Bebas",
        category: "Demam",
        indication: "Meredakan sakit kepala, nyeri ringan dan demam.",
        contraindication: "Hipersensitivitas terhadap bahan obat.",
        sideEffect: "Mual dan reaksi alergi; risiko kerusakan hati pada overdosis.",
        dosage: "Gunakan sesuai etiket produk.",
        usage: "Diminum dengan air.",
        storage: "Simpan di tempat kering dan terlindung dari cahaya.",
        warning: "Hindari penggunaan berlebihan.",
        interaction: "Informasikan penggunaan obat lain kepada apoteker/dokter.",
        image: "assets/obat/bodrex.jpg"
    },

    {
        id: "proris",
        name: "Proris",
        active: "Ibuprofen",
        strength: "200 mg",
        form: "Tablet",
        status: "Obat Bebas Terbatas",
        category: "Nyeri",
        indication: "Meredakan nyeri ringan sampai sedang dan demam.",
        contraindication: "Hipersensitivitas terhadap ibuprofen atau NSAID tertentu; beberapa kondisi lambung, ginjal, dan jantung memerlukan perhatian medis.",
        sideEffect: "Mual, nyeri lambung, gangguan pencernaan.",
        dosage: "Ikuti petunjuk pada kemasan atau anjuran tenaga kesehatan.",
        usage: "Sebaiknya diminum setelah makan bila sesuai petunjuk.",
        storage: "Simpan pada tempat kering dan suhu ruang.",
        warning: "Perhatian pada pasien dengan riwayat tukak lambung atau gangguan ginjal.",
        interaction: "Dapat berinteraksi dengan antikoagulan, NSAID lain dan obat tertentu.",
        image: "assets/obat/proris.jpg"
    },

    {
        id: "promag",
        name: "Promag",
        active: "Hydrotalcite, Magnesium Hydroxide",
        strength: "Sesuai sediaan",
        form: "Tablet kunyah",
        status: "Obat Bebas",
        category: "Maag",
        indication: "Meredakan gejala yang berhubungan dengan kelebihan asam lambung.",
        contraindication: "Hipersensitivitas terhadap komponen produk.",
        sideEffect: "Gangguan saluran cerna seperti konstipasi atau diare dapat terjadi.",
        dosage: "Ikuti aturan pakai pada kemasan.",
        usage: "Dikunyah sesuai petunjuk produk.",
        storage: "Simpan di tempat kering dan tertutup.",
        warning: "Berikan jarak dengan obat tertentu karena antasida dapat memengaruhi penyerapan obat.",
        interaction: "Dapat memengaruhi penyerapan beberapa obat oral.",
        image: "assets/obat/promag.jpg"
    },

    {
        id: "entrostop",
        name: "Entrostop",
        active: "Attapulgite",
        strength: "Sesuai sediaan",
        form: "Tablet",
        status: "Obat Bebas",
        category: "Diare",
        indication: "Membantu meredakan gejala diare.",
        contraindication: "Hipersensitivitas terhadap kandungan produk.",
        sideEffect: "Konstipasi dapat terjadi.",
        dosage: "Ikuti aturan pakai pada kemasan.",
        usage: "Diminum sesuai petunjuk penggunaan.",
        storage: "Simpan di tempat kering dan tertutup.",
        warning: "Utamakan penggantian cairan dan elektrolit. Jika diare berat atau disertai tanda dehidrasi, segera mencari pertolongan medis.",
        interaction: "Dapat mengganggu penyerapan obat oral tertentu.",
        image: "assets/obat/entrostop.jpg"
    },

    {
        id: "dulcolax",
        name: "Dulcolax",
        active: "Bisacodyl",
        strength: "5 mg",
        form: "Tablet salut enterik",
        status: "Obat Bebas Terbatas",
        category: "Sembelit",
        indication: "Digunakan untuk membantu mengatasi konstipasi sesuai petunjuk.",
        contraindication: "Tidak digunakan pada kondisi tertentu seperti sumbatan usus tanpa arahan tenaga medis.",
        sideEffect: "Kram perut, diare, dan mual.",
        dosage: "Ikuti petunjuk pada kemasan.",
        usage: "Telan utuh sesuai aturan penggunaan. Jangan mengunyah tablet salut enterik.",
        storage: "Simpan pada suhu ruang dan tempat kering.",
        warning: "Tidak dianjurkan digunakan terus-menerus tanpa evaluasi tenaga kesehatan.",
        interaction: "Beritahu apoteker mengenai obat lain yang digunakan.",
        image: "assets/obat/dulcolax.jpg"
    },

    {
        id: "cetirizine",
        name: "Cetirizine",
        active: "Cetirizine",
        strength: "10 mg",
        form: "Tablet",
        status: "Obat Bebas Terbatas",
        category: "Alergi",
        indication: "Meredakan gejala alergi seperti bersin dan hidung berair.",
        contraindication: "Hipersensitivitas terhadap cetirizine atau komponennya.",
        sideEffect: "Mengantuk, lelah, mulut kering.",
        dosage: "Sesuai petunjuk pada kemasan atau anjuran tenaga kesehatan.",
        usage: "Diminum dengan air.",
        storage: "Simpan di tempat kering dan suhu ruang.",
        warning: "Dapat menyebabkan kantuk pada sebagian orang.",
        interaction: "Hindari kombinasi dengan zat yang meningkatkan kantuk tanpa konsultasi tenaga kesehatan.",
        image: "assets/obat/cetirizine.jpg"
    },

    {
        id: "obh",
        name: "OBH Combi",
        active: "Kombinasi zat aktif sesuai varian",
        strength: "Sesuai varian produk",
        form: "Sirup",
        status: "Periksa status pada kemasan",
        category: "Flu dan Batuk",
        indication: "Membantu meredakan gejala flu dan batuk sesuai varian produk.",
        contraindication: "Bergantung pada kandungan dan kondisi pengguna.",
        sideEffect: "Bergantung pada zat aktif yang terkandung.",
        dosage: "Ikuti aturan pakai pada kemasan.",
        usage: "Gunakan sendok takar yang sesuai.",
        storage: "Simpan sesuai petunjuk pada kemasan.",
        warning: "Periksa kandungan sebelum menggunakan bersama obat flu/batuk lainnya.",
        interaction: "Bergantung pada kandungan produk.",
        image: "assets/obat/obh-combi.jpg"
    },

    {
        id: "enervon-c",
        name: "Enervon-C",
        active: "Vitamin B kompleks dan Vitamin C",
        strength: "Sesuai komposisi produk",
        form: "Tablet",
        status: "Suplemen Kesehatan",
        category: "Vitamin",
        indication: "Membantu memenuhi kebutuhan vitamin sesuai penggunaan produk.",
        contraindication: "Hipersensitivitas terhadap komponen produk.",
        sideEffect: "Gangguan saluran cerna dapat terjadi pada sebagian orang.",
        dosage: "Ikuti petunjuk penggunaan pada kemasan.",
        usage: "Diminum dengan air.",
        storage: "Simpan di tempat kering dan terlindung dari cahaya.",
        warning: "Jangan melebihi anjuran konsumsi.",
        interaction: "Informasikan penggunaan suplemen kepada tenaga kesehatan bila menggunakan obat lain.",
        image: "assets/obat/enervon-c.jpg"
    }

];


/* =====================================================
   DATABASE KATEGORI
===================================================== */

const categoryDescription = {

    "Demam": "Obat yang digunakan untuk membantu meredakan demam dan nyeri.",
    "Nyeri": "Informasi obat yang digunakan untuk membantu meredakan nyeri.",
    "Maag": "Informasi mengenai obat untuk gejala yang berhubungan dengan asam lambung.",
    "Sembelit": "Informasi obat yang dapat digunakan untuk membantu mengatasi konstipasi.",
    "Diare": "Informasi mengenai penanganan gejala diare.",
    "Alergi": "Informasi obat untuk membantu meredakan gejala alergi.",
    "Flu dan Batuk": "Informasi mengenai obat untuk membantu meredakan gejala flu dan batuk.",
    "Vitamin": "Informasi mengenai vitamin dan suplemen kesehatan."

};


/* =====================================================
   DATABASE APOTEKER
===================================================== */

const pharmacists = [

    {
        name: "apt. Arlamadha Tri Wangsa, M.Farm",
        specialty: "Spesialis Farmasi Komunitas",
        experience: "7 tahun",
        status: "Online"
    },

    {
        name: "apt. Chandra Gardipta, M.Farm",
        specialty: "Spesialis Farmasi Klinik",
        experience: "10 tahun",
        status: "Online"
    },

    {
        name: "apt. Nastikah Syafitri, S.Farm",
        specialty: "Apoteker",
        experience: "4 tahun",
        status: "Online"
    }

];


/* =====================================================
   NAVIGATION
===================================================== */

function showPage(pageId) {

    document.querySelectorAll(".page").forEach(page => {
        page.classList.remove("active");
    });

    const page = document.getElementById(pageId);

    if (page) {
        page.classList.add("active");
        window.scrollTo({
            top: 0,
            behavior: "smooth"
        });
    }

    document.getElementById("navLinks").classList.remove("show");
}


/* =====================================================
   CATEGORY
===================================================== */

let currentCategory = "";

function showCategory(category) {

    currentCategory = category;

    const medicinesInCategory =
        medicines.filter(medicine =>
            medicine.category === category
        );

    document.getElementById("categoryTitle").textContent =
        "Obat Kategori " + category;

    document.getElementById("categoryDescription").textContent =
        categoryDescription[category] || "";

    const medicineList =
        document.getElementById("medicineList");

    medicineList.innerHTML = "";

    if (medicinesInCategory.length === 0) {

        medicineList.innerHTML = `
            <div class="card">
                <h3>Belum ada data obat</h3>
                <p>
                    Data obat untuk kategori ini sedang disiapkan.
                    Silakan konsultasikan dengan apoteker.
                </p>
            </div>
        `;

    } else {

        medicinesInCategory.forEach(medicine => {

            medicineList.innerHTML += `

                <div class="card medicine-card clickable"
                     onclick="showMedicineDetail('${medicine.id}')">

                    <img
                        src="${medicine.image}"
                        class="medicine-image"
                        alt="${medicine.name}"
                        onerror="this.onerror=null;this.src='https://placehold.co/600x400/fdf0f4/a95f78?text=${encodeURIComponent(medicine.name)}';">

                    <div class="medicine-content">

                        <h3>${medicine.name}</h3>

                        <span class="badge">
                            ${medicine.status}
                        </span>

                        <p>
                            <strong>Zat aktif:</strong>
                            ${medicine.active}
                        </p>

                        <p>
                            <strong>Kekuatan:</strong>
                            ${medicine.strength}
                        </p>

                        <p>
                            <strong>Bentuk:</strong>
                            ${medicine.form}
                        </p>

                        <br>

                        <button
                            class="btn"
                            onclick="event.stopPropagation();showMedicineDetail('${medicine.id}')">

                            Lihat Detail →

                        </button>

                    </div>

                </div>

            `;

        });

    }

    showPage("daftar-obat");
}


/* =====================================================
   DETAIL OBAT
===================================================== */

let previousMedicinePage = "daftar-obat";

function showMedicineDetail(id) {

    const medicine =
        medicines.find(item => item.id === id);

    if (!medicine) {
        showToast("Data obat tidak ditemukan.");
        return;
    }

    previousMedicinePage = "daftar-obat";

    document.getElementById("medicineDetail").innerHTML = `

        <div class="detail-box">

            <div class="detail-header">

                <img
                    src="${medicine.image}"
                    class="detail-image"
                    alt="${medicine.name}"
                    onerror="this.onerror=null;this.src='https://placehold.co/600x500/fdf0f4/a95f78?text=${encodeURIComponent(medicine.name)}';">

                <div>

                    <h1 style="color:var(--dark-pink);">
                        ${medicine.name}
                    </h1>

                    <span class="badge">
                        ${medicine.status}
                    </span>

                    <p>
                        <strong>Zat aktif:</strong>
                        ${medicine.active}
                    </p>

                    <p>
                        <strong>Kekuatan:</strong>
                        ${medicine.strength}
                    </p>

                    <p>
                        <strong>Bentuk sediaan:</strong>
                        ${medicine.form}
                    </p>

                    <p>
                        <strong>Kategori:</strong>
                        ${medicine.category}
                    </p>

                </div>

            </div>


            <div class="info-list">

                <div class="info-item">
                    <strong>Indikasi</strong>
                    ${medicine.indication}
                </div>

                <div class="info-item">
                    <strong>Kontraindikasi</strong>
                    ${medicine.contraindication}
                </div>

                <div class="info-item">
                    <strong>Efek Samping</strong>
                    ${medicine.sideEffect}
                </div>

                <div class="info-item">
                    <strong>Aturan Pakai</strong>
                    ${medicine.dosage}
                </div>

                <div class="info-item">
                    <strong>Cara Penggunaan</strong>
                    ${medicine.usage}
                </div>

                <div class="info-item">
                    <strong>Cara Penyimpanan</strong>
                    ${medicine.storage}
                </div>

                <div class="info-item">
                    <strong>Peringatan / Perhatian</strong>
                    ${medicine.warning}
                </div>

                <div class="info-item">
                    <strong>Interaksi Obat</strong>
                    ${medicine.interaction}
                </div>

            </div>

            <br>

            <button class="btn"
                    onclick="showPage('konseling')">

                👩‍⚕️ Konsultasikan dengan Apoteker

            </button>

        </div>

    `;

    showPage("detail-obat");
}


function goBackToMedicineList() {
    showCategory(currentCategory);
}


/* =====================================================
   SEARCH
===================================================== */

function searchMedicine() {

    const query =
        document.getElementById("homeSearch")
        .value
        .trim()
        .toLowerCase();

    if (!query) {
        showToast("Silakan masukkan nama obat atau kategori.");
        return;
    }

    const result = medicines.find(medicine =>

        medicine.name.toLowerCase().includes(query) ||

        medicine.active.toLowerCase().includes(query) ||

        medicine.category.toLowerCase().includes(query)

    );

    if (result) {

        currentCategory = result.category;

        showMedicineDetail(result.id);

    } else {

        showToast(
            "Obat belum ditemukan. Silakan periksa kembali nama obat atau konsultasikan dengan apoteker."
        );

    }

}


/* =====================================================
   INFORMASI KESEHATAN
===================================================== */

const healthInformation = {

    "Pola Hidup Sehat": `
        <p>
            Pola hidup sehat dapat dilakukan dengan mengonsumsi makanan
            bergizi seimbang, melakukan aktivitas fisik secara rutin,
            menjaga kebersihan diri dan lingkungan, tidur yang cukup,
            serta menghindari kebiasaan yang dapat meningkatkan risiko
            penyakit.
        </p>
        <br>
        <p>
            Menjaga pola hidup sehat juga perlu disesuaikan dengan kondisi
            masing-masing individu. Jika memiliki kondisi kesehatan tertentu,
            konsultasikan dengan tenaga kesehatan.
        </p>
    `,

    "Cara Konsumsi Obat yang Benar": `
        <p>
            Gunakan obat sesuai nama, dosis, aturan pakai dan durasi yang
            tercantum pada etiket atau sesuai resep dokter.
        </p>
        <br>
        <p>
            Jangan menggandakan dosis tanpa petunjuk tenaga kesehatan.
            Perhatikan apakah obat harus diminum sebelum atau sesudah makan,
            serta gunakan alat takar yang sesuai untuk obat cair.
        </p>
    `,

    "Cara Menyimpan Obat": `
        <p>
            Simpan obat sesuai petunjuk pada kemasan. Secara umum obat perlu
            disimpan di tempat kering, terlindung dari cahaya langsung,
            dan jauh dari jangkauan anak-anak.
        </p>
        <br>
        <p>
            Jangan menyimpan obat yang sudah berubah warna, bau, bentuk,
            atau kemasannya rusak tanpa berkonsultasi dengan apoteker.
        </p>
    `,

    "Cara Membaca Etiket Obat": `
        <p>
            Etiket obat dapat memuat nama obat, kandungan, kekuatan,
            aturan pakai, jumlah obat, tanggal kedaluwarsa dan informasi
            penyimpanan.
        </p>
        <br>
        <p>
            Bacalah etiket sebelum menggunakan obat. Jika terdapat informasi
            yang tidak dipahami, tanyakan kepada apoteker.
        </p>
    `,

    "Pengelolaan Obat di Rumah": `
        <p>
            Simpan obat dalam kemasan aslinya dan pisahkan obat berdasarkan
            kebutuhan. Periksa tanggal kedaluwarsa secara berkala.
        </p>
        <br>
        <p>
            Obat yang sudah tidak digunakan sebaiknya tidak diberikan kepada
            orang lain. Pengelolaan dan pembuangan obat sebaiknya mengikuti
            petunjuk tenaga kesehatan atau ketentuan setempat.
        </p>
    `,

    "Mengenal Golongan Obat": `
        <p>
            Obat memiliki status penggunaan yang berbeda. Contohnya obat
            bebas, obat bebas terbatas, obat keras dan kategori lainnya.
        </p>
        <br>
        <p>
            Status obat dapat dilihat pada kemasan dan informasi resmi produk.
            Obat keras umumnya memerlukan resep dokter dan penggunaannya
            perlu mengikuti arahan tenaga kesehatan.
        </p>
    `,

    "Bentuk Sediaan Obat": `
        <p>
            Obat tersedia dalam berbagai bentuk sediaan seperti tablet,
            kapsul, sirup, suspensi, salep, krim, gel, tetes mata,
            tetes telinga, inhalasi dan bentuk lainnya.
        </p>
        <br>
        <p>
            Setiap bentuk sediaan mempunyai cara penggunaan yang berbeda.
            Ikuti petunjuk pada kemasan atau arahan apoteker.
        </p>
    `

};


function showHealthDetail(title) {

    document.getElementById("healthTitle").textContent = title;

    document.getElementById("healthContent").innerHTML =
        healthInformation[title];

    showPage("detail-kesehatan");
}


/* =====================================================
   KONSELING
===================================================== */

let selectedPharmacist = null;

function openConsultation(index) {

    selectedPharmacist =
        pharmacists[index];

    document.getElementById("pharmacistInfo").innerHTML = `

        <div class="card">

            <h3>${selectedPharmacist.name}</h3>

            <p>
                <strong>Spesialisasi:</strong>
                ${selectedPharmacist.specialty}
            </p>

            <p>
                <strong>Pengalaman:</strong>
                ${selectedPharmacist.experience}
            </p>

            <p class="online">
                ● ${selectedPharmacist.status}
            </p>

        </div>

    `;

    showPage("form-konseling");
}


function sendQuestion(event) {

    event.preventDefault();

    const name =
        document.getElementById("consultName").value;

    const question =
        document.getElementById("consultQuestion").value;

    if (!name || !question) {
        showToast("Silakan lengkapi formulir.");
        return;
    }

    showToast(
        "Pertanyaan berhasil dikirim kepada " +
        selectedPharmacist.name
    );

    document.getElementById("consultName").value = "";
    document.getElementById("consultQuestion").value = "";

}


/* =====================================================
   ANTIBIOTIK
===================================================== */

const antibioticData = {

    "Amoxsan": {

        active: "Amoksisilin",

        class: "Penisilin",

        form: "Kapsul / sediaan sesuai produk",

        indication:
            "Digunakan untuk infeksi bakteri tertentu yang sensitif terhadap amoksisilin berdasarkan diagnosis dokter.",

        dosage:
            "Digunakan sesuai dosis dan durasi yang diresepkan dokter.",

        sideEffect:
            "Mual, diare, ruam, dan reaksi alergi dapat terjadi.",

        warning:
            "Informasikan riwayat alergi terhadap penisilin atau antibiotik beta-laktam kepada dokter.",

        correct:
            "Antibiotik harus digunakan berdasarkan resep dokter dan tidak boleh digunakan untuk flu atau infeksi virus."
    },

    "Zibramax": {

        active: "Azitromisin",

        class: "Makrolida",

        form: "Tablet / sediaan sesuai produk",

        indication:
            "Digunakan untuk infeksi bakteri tertentu berdasarkan diagnosis dan resep dokter.",

        dosage:
            "Gunakan sesuai dosis dan durasi yang diresepkan dokter.",

        sideEffect:
            "Mual, diare, nyeri perut, dan gangguan pencernaan dapat terjadi.",

        warning:
            "Informasikan kepada dokter/apoteker mengenai obat lain yang sedang digunakan.",

        correct:
            "Tidak digunakan untuk flu biasa atau infeksi virus dan tidak boleh digunakan tanpa resep dokter."
    }

};


function showAntibioticDetail(name) {

    const data =
        antibioticData[name];

    document.getElementById("antibioticDetail").innerHTML = `

        <div class="detail-box">

            <h1 style="color:var(--dark-pink);">
                ${name}
            </h1>

            <span class="badge">
                Obat Keras — Antibiotik
            </span>

            <br><br>

            <div class="info-list">

                <div class="info-item">
                    <strong>Zat Aktif</strong>
                    ${data.active}
                </div>

                <div class="info-item">
                    <strong>Golongan Antibiotik</strong>
                    ${data.class}
                </div>

                <div class="info-item">
                    <strong>Bentuk Sediaan</strong>
                    ${data.form}
                </div>

                <div class="info-item">
                    <strong>Indikasi</strong>
                    ${data.indication}
                </div>

                <div class="info-item">
                    <strong>Aturan Penggunaan</strong>
                    ${data.dosage}
                </div>

                <div class="info-item">
                    <strong>Efek Samping</strong>
                    ${data.sideEffect}
                </div>

                <div class="info-item">
                    <strong>Peringatan</strong>
                    ${data.warning}
                </div>

                <div class="info-item">
                    <strong>Penggunaan yang Benar</strong>
                    ${data.correct}
                </div>

            </div>

            <br>

            <div class="warning">

                <strong>⚠️ Ingat!</strong>

                <p>
                    Antibiotik merupakan obat keras dan penggunaannya
                    harus berdasarkan resep dokter.
                </p>

                <p>
                    Jangan menggunakan sisa antibiotik, jangan memberikan
                    antibiotik kepada orang lain, dan jangan menggandakan
                    dosis jika lupa minum tanpa mengikuti petunjuk resep
                    atau berkonsultasi dengan apoteker.
                </p>

            </div>

            <button class="btn"
                    onclick="showPage('konseling')">

                👩‍⚕️ Konsultasikan dengan Apoteker

            </button>

        </div>

    `;

    showPage("detail-antibiotik");
}


/* =====================================================
   LOGIN
===================================================== */

function loginUser(event) {

    event.preventDefault();

    const name =
        document.getElementById("loginName").value.trim();

    if (!name) {
        showToast("Masukkan nama lengkap terlebih dahulu.");
        return;
    }

    localStorage.setItem("pharmaCareUser", name);

    showToast(
        "Selamat datang di PharmaCare, " + name + "!"
    );

    setTimeout(() => {
        showPage("home");
    }, 1200);

}


/* =====================================================
   MOBILE MENU
===================================================== */

function toggleMenu() {

    document
        .getElementById("navLinks")
        .classList.toggle("show");

}


/* =====================================================
   TOAST
===================================================== */

function showToast(message) {

    const toast =
        document.getElementById("toast");

    toast.textContent = message;

    toast.style.display = "block";

    setTimeout(() => {
        toast.style.display = "none";
    }, 3500);

}

</script>

</body>
</html>
```
