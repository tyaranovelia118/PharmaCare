<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>PharmaCare | Medicine & Health Consultation</title>

<style>
:root{
    --pink:#e8a9bd;
    --pink-soft:#fdf1f5;
    --pink-light:#fff8fa;
    --pink-dark:#b85c7b;
    --pink-deep:#963f60;
    --white:#ffffff;
    --text:#4a3940;
    --muted:#806d74;
    --border:#f0dce3;
    --shadow:0 8px 25px rgba(150,63,96,.10);
}

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:Arial, Helvetica, sans-serif;
    background:linear-gradient(135deg,#fff8fa,#fdf1f5,#fff);
    color:var(--text);
    line-height:1.6;
}

/* HEADER */
header{
    background:linear-gradient(135deg,#e8a9bd,#d98ca7);
    color:white;
    padding:25px 18px 28px;
    text-align:center;
    border-radius:0 0 30px 30px;
    box-shadow:var(--shadow);
}

.logo{
    font-size:35px;
    margin-bottom:5px;
}

header h1{
    font-size:28px;
    letter-spacing:.5px;
}

.tagline{
    font-size:13px;
    opacity:.95;
    margin-top:3px;
}

/* NAV */
nav{
    position:sticky;
    top:0;
    z-index:999;
    background:rgba(255,255,255,.96);
    backdrop-filter:blur(10px);
    border-bottom:1px solid var(--border);
    box-shadow:0 3px 15px rgba(0,0,0,.06);
}

.nav-inner{
    max-width:1100px;
    margin:auto;
    display:flex;
    justify-content:center;
    gap:5px;
    overflow-x:auto;
    white-space:nowrap;
    padding:9px 8px;
}

nav button{
    border:none;
    background:transparent;
    color:var(--pink-deep);
    font-weight:bold;
    font-size:13px;
    padding:8px 11px;
    border-radius:20px;
    cursor:pointer;
}

nav button:hover{
    background:var(--pink-soft);
}

/* CONTAINER */
.container{
    width:92%;
    max-width:1100px;
    margin:auto;
}

.page{
    display:none;
    padding:30px 0 45px;
    animation:fade .25s ease;
}

.page.active{
    display:block;
}

@keyframes fade{
    from{opacity:0;transform:translateY(5px)}
    to{opacity:1;transform:translateY(0)}
}

/* HERO */
.hero{
    text-align:center;
    padding:30px 18px;
    background:white;
    border:1px solid var(--border);
    border-radius:28px;
    box-shadow:var(--shadow);
}

.hero-icon{
    font-size:60px;
}

.hero h2{
    color:var(--pink-deep);
    font-size:30px;
    margin:8px 0;
}

.hero p{
    max-width:700px;
    margin:auto;
    color:var(--muted);
}

/* SEARCH */
.search-box{
    margin:22px auto 0;
    max-width:700px;
    display:flex;
    background:white;
    border:2px solid #f1ccd8;
    border-radius:18px;
    overflow:hidden;
}

.search-box input{
    flex:1;
    border:none;
    outline:none;
    padding:14px;
    font-size:14px;
}

.search-box button{
    border:none;
    background:var(--pink-dark);
    color:white;
    padding:0 18px;
    cursor:pointer;
}

/* SECTION TITLE */
.section-title{
    text-align:center;
    color:var(--pink-deep);
    font-size:24px;
    margin-bottom:20px;
}

/* CARDS */
.grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:16px;
}

.card{
    background:white;
    border:1px solid var(--border);
    border-radius:20px;
    padding:18px;
    box-shadow:var(--shadow);
    transition:.25s;
}

.card:hover{
    transform:translateY(-4px);
    box-shadow:0 12px 30px rgba(150,63,96,.16);
}

.clickable{
    cursor:pointer;
}

.card-icon{
    font-size:35px;
    margin-bottom:8px;
}

.card h3{
    color:var(--pink-deep);
    font-size:17px;
    margin-bottom:6px;
}

.card p{
    font-size:13px;
    color:var(--muted);
}

/* BUTTON */
.btn{
    display:inline-block;
    border:none;
    background:var(--pink-dark);
    color:white;
    padding:11px 18px;
    border-radius:12px;
    font-weight:bold;
    cursor:pointer;
    text-decoration:none;
    transition:.2s;
}

.btn:hover{
    background:var(--pink-deep);
    transform:translateY(-2px);
}

.btn-light{
    background:var(--pink-soft);
    color:var(--pink-deep);
}

/* HOME FEATURES */
.feature-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:16px;
    margin-top:25px;
}

/* CATEGORY */
.category-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:15px;
}

.category{
    text-align:center;
    padding:22px 12px;
    background:white;
    border:1px solid var(--border);
    border-radius:20px;
    box-shadow:var(--shadow);
    cursor:pointer;
    transition:.25s;
}

.category:hover{
    transform:translateY(-4px);
    background:var(--pink-soft);
}

.category-icon{
    font-size:38px;
}

.category h3{
    color:var(--pink-deep);
    margin-top:6px;
    font-size:15px;
}

/* MEDICINE */
.medicine-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:18px;
}

.medicine-card{
    background:white;
    border:1px solid var(--border);
    border-radius:20px;
    overflow:hidden;
    box-shadow:var(--shadow);
    cursor:pointer;
    transition:.25s;
}

.medicine-card:hover{
    transform:translateY(-5px);
    box-shadow:0 13px 30px rgba(150,63,96,.17);
}

.medicine-image{
    height:190px;
    background:var(--pink-soft);
    display:flex;
    align-items:center;
    justify-content:center;
    overflow:hidden;
}

.medicine-image img{
    width:100%;
    height:100%;
    object-fit:contain;
}

.image-placeholder{
    text-align:center;
    color:var(--pink-dark);
}

.image-placeholder span{
    display:block;
    font-size:55px;
}

.medicine-content{
    padding:16px;
}

.medicine-content h3{
    color:var(--pink-deep);
    margin-bottom:5px;
}

.medicine-content p{
    font-size:13px;
    color:var(--muted);
}

.status{
    display:inline-block;
    background:#fcecf2;
    color:var(--pink-deep);
    border-radius:20px;
    padding:4px 9px;
    font-size:11px;
    font-weight:bold;
    margin-top:8px;
}

/* DETAIL */
.detail-card{
    background:white;
    border:1px solid var(--border);
    border-radius:25px;
    box-shadow:var(--shadow);
    padding:22px;
}

.detail-top{
    display:grid;
    grid-template-columns:320px 1fr;
    gap:25px;
    align-items:start;
}

.detail-image{
    height:300px;
    background:var(--pink-soft);
    border-radius:20px;
    overflow:hidden;
    display:flex;
    justify-content:center;
    align-items:center;
}

.detail-image img{
    width:100%;
    height:100%;
    object-fit:contain;
}

.detail-title{
    color:var(--pink-deep);
    font-size:28px;
}

.info-list{
    margin-top:15px;
}

.info-row{
    padding:10px 0;
    border-bottom:1px solid #f2e3e8;
    font-size:14px;
}

.info-row strong{
    color:var(--pink-deep);
}

.warning{
    background:#fff6df;
    border-left:5px solid #e4ad46;
    padding:15px;
    border-radius:12px;
    margin-top:18px;
    font-size:13px;
}

/* HEALTH DETAIL */
.article{
    background:white;
    border-radius:22px;
    padding:23px;
    border:1px solid var(--border);
    box-shadow:var(--shadow);
}

.article h3{
    color:var(--pink-deep);
    margin:18px 0 7px;
}

.article p,
.article li{
    font-size:14px;
    color:var(--text);
}

.article ul{
    padding-left:22px;
}

/* COUNSELOR */
.profile-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:18px;
}

.profile{
    background:white;
    border:1px solid var(--border);
    border-radius:22px;
    padding:22px;
    text-align:center;
    box-shadow:var(--shadow);
    cursor:pointer;
    transition:.25s;
}

.profile:hover{
    transform:translateY(-4px);
}

.avatar{
    width:75px;
    height:75px;
    border-radius:50%;
    margin:auto;
    display:flex;
    align-items:center;
    justify-content:center;
    background:var(--pink-soft);
    font-size:35px;
}

.online{
    display:inline-block;
    color:#27815a;
    background:#e9f8f0;
    padding:4px 10px;
    border-radius:20px;
    font-size:11px;
    font-weight:bold;
    margin-top:8px;
}

/* FORM */
.form-card{
    max-width:650px;
    margin:auto;
    background:white;
    padding:23px;
    border-radius:22px;
    border:1px solid var(--border);
    box-shadow:var(--shadow);
}

.form-group{
    margin-bottom:15px;
}

.form-group label{
    display:block;
    font-size:13px;
    font-weight:bold;
    margin-bottom:6px;
    color:var(--pink-deep);
}

.form-group input,
.form-group textarea{
    width:100%;
    border:1px solid #e8d2da;
    border-radius:12px;
    padding:12px;
    outline:none;
    font-family:inherit;
}

.form-group textarea{
    min-height:130px;
    resize:vertical;
}

.form-group input:focus,
.form-group textarea:focus{
    border-color:var(--pink);
}

/* LOGIN */
.login-card{
    max-width:450px;
    margin:auto;
    background:white;
    padding:25px;
    border-radius:24px;
    box-shadow:var(--shadow);
    border:1px solid var(--border);
}

/* BACK */
.back{
    margin-bottom:18px;
}

/* ANTIBIOTIC */
.antibiotic-note{
    background:#fff0f4;
    border:1px solid #e8bdcc;
    border-radius:18px;
    padding:18px;
    margin-bottom:22px;
}

.antibiotic-note h3{
    color:var(--pink-deep);
    margin-bottom:8px;
}

.antibiotic-card{
    background:white;
    border:1px solid var(--border);
    border-radius:20px;
    padding:18px;
    box-shadow:var(--shadow);
}

.antibiotic-grid{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:18px;
}

/* FOOTER */
footer{
    background:#9e526e;
    color:white;
    text-align:center;
    padding:28px 18px;
    margin-top:30px;
}

footer h3{
    font-size:20px;
}

footer p{
    font-size:12px;
    margin-top:5px;
    opacity:.95;
}

/* RESPONSIVE */
@media(max-width:900px){
    .grid,
    .category-grid{
        grid-template-columns:repeat(2,1fr);
    }

    .medicine-grid{
        grid-template-columns:repeat(2,1fr);
    }

    .profile-grid{
        grid-template-columns:1fr;
    }

    .feature-grid{
        grid-template-columns:1fr;
    }

    .detail-top{
        grid-template-columns:1fr;
    }
}

@media(max-width:600px){

    header h1{
        font-size:25px;
    }

    .hero h2{
        font-size:23px;
    }

    .grid,
    .category-grid,
    .medicine-grid,
    .antibiotic-grid{
        grid-template-columns:1fr;
    }

    .container{
        width:93%;
    }

    .page{
        padding-top:23px;
    }

    .section-title{
        font-size:21px;
    }

    nav button{
        font-size:11px;
        padding:7px 9px;
    }

    .detail-title{
        font-size:23px;
    }

    .detail-image{
        height:240px;
    }
}
</style>
</head>

<body>

<!-- HEADER -->
<header>
    <div class="logo">🌸💊</div>
    <h1>PharmaCare</h1>
    <div class="tagline">
        Your Guide to Medicine & Health Consultation
    </div>
</header>

<!-- NAVIGATION -->
<nav>
<div class="nav-inner">
    <button onclick="showPage('home')">Home</button>
    <button onclick="showPage('obat')">Obat</button>
    <button onclick="showPage('kesehatan')">Informasi Kesehatan</button>
    <button onclick="showPage('konseling')">Konseling Apoteker</button>
    <button onclick="showPage('penting')">Informasi Penting</button>
    <button onclick="showPage('login')">Login</button>
</div>
</nav>


<main class="container">

<!-- ================= HOME ================= -->
<section id="home" class="page active">

    <div class="hero">

        <div class="hero-icon">💊</div>

        <h2>Selamat Datang di PharmaCare</h2>

        <p>
            PharmaCare adalah website informasi obat dan kesehatan
            yang dirancang untuk membantu masyarakat mendapatkan
            informasi edukatif mengenai obat, kesehatan, dan konsultasi
            kefarmasian dengan tampilan sederhana dan mudah digunakan.
        </p>

        <div class="search-box">
            <input
                type="text"
                id="searchInput"
                placeholder="Cari nama obat, zat aktif, atau kategori..."
                onkeydown="if(event.key==='Enter') searchMedicine()">

            <button onclick="searchMedicine()">🔍 Cari</button>
        </div>

        <div id="searchResult" style="margin-top:15px;"></div>

        <br>

        <button class="btn" onclick="showPage('login')">
            🔐 Login
        </button>

    </div>


    <h2 class="section-title" style="margin-top:35px;">
        💊 Kategori Obat
    </h2>

    <div class="category-grid">

        <div class="category" onclick="openCategory('Demam')">
            <div class="category-icon">🌡️</div>
            <h3>Demam</h3>
        </div>

        <div class="category" onclick="openCategory('Nyeri')">
            <div class="category-icon">🩹</div>
            <h3>Nyeri</h3>
        </div>

        <div class="category" onclick="openCategory('Maag')">
            <div class="category-icon">🫃</div>
            <h3>Maag</h3>
        </div>

        <div class="category" onclick="openCategory('Sembelit')">
            <div class="category-icon">🥗</div>
            <h3>Sembelit</h3>
        </div>

        <div class="category" onclick="openCategory('Diare')">
            <div class="category-icon">💧</div>
            <h3>Diare</h3>
        </div>

        <div class="category" onclick="openCategory('Alergi')">
            <div class="category-icon">🤧</div>
            <h3>Alergi</h3>
        </div>

        <div class="category" onclick="openCategory('Flu dan Batuk')">
            <div class="category-icon">😷</div>
            <h3>Flu dan Batuk</h3>
        </div>

        <div class="category" onclick="openCategory('Vitamin')">
            <div class="category-icon">🍊</div>
            <h3>Vitamin</h3>
        </div>

    </div>


    <h2 class="section-title" style="margin-top:35px;">
        ✨ Fitur PharmaCare
    </h2>

    <div class="feature-grid">

        <div class="card clickable" onclick="showPage('kesehatan')">
            <div class="card-icon">📚</div>
            <h3>Informasi Kesehatan</h3>
            <p>
                Pelajari berbagai informasi kesehatan yang
                mudah dipahami.
            </p>
        </div>

        <div class="card clickable" onclick="showPage('konseling')">
            <div class="card-icon">👩‍⚕️</div>
            <h3>Konseling Apoteker</h3>
            <p>
                Konsultasikan pertanyaan mengenai penggunaan obat
                kepada apoteker.
            </p>
        </div>

        <div class="card clickable" onclick="showPage('penting')">
            <div class="card-icon">⚠️</div>
            <h3>Informasi Penting</h3>
            <p>
                Pelajari penggunaan antibiotik secara tepat dan aman.
            </p>
        </div>

    </div>

</section>


<!-- ================= OBAT ================= -->
<section id="obat" class="page">

    <h2 class="section-title">💊 Informasi Obat</h2>

    <div id="categoryList">

        <p style="text-align:center;color:var(--muted);margin-bottom:18px;">
            Pilih kategori obat untuk melihat daftar obat.
        </p>

        <div class="category-grid">

            <div class="category" onclick="openCategory('Demam')">
                <div class="category-icon">🌡️</div>
                <h3>Demam</h3>
            </div>

            <div class="category" onclick="openCategory('Nyeri')">
                <div class="category-icon">🩹</div>
                <h3>Nyeri</h3>
            </div>

            <div class="category" onclick="openCategory('Maag')">
                <div class="category-icon">🫃</div>
                <h3>Maag</h3>
            </div>

            <div class="category" onclick="openCategory('Sembelit')">
                <div class="category-icon">🥗</div>
                <h3>Sembelit</h3>
            </div>

            <div class="category" onclick="openCategory('Diare')">
                <div class="category-icon">💧</div>
                <h3>Diare</h3>
            </div>

            <div class="category" onclick="openCategory('Alergi')">
                <div class="category-icon">🤧</div>
                <h3>Alergi</h3>
            </div>

            <div class="category" onclick="openCategory('Flu dan Batuk')">
                <div class="category-icon">😷</div>
                <h3>Flu dan Batuk</h3>
            </div>

            <div class="category" onclick="openCategory('Vitamin')">
                <div class="category-icon">🍊</div>
                <h3>Vitamin</h3>
            </div>

        </div>

    </div>

    <div id="medicineList" style="display:none;"></div>

    <div id="medicineDetail" style="display:none;"></div>

</section>


<!-- ================= KESEHATAN ================= -->
<section id="kesehatan" class="page">

    <h2 class="section-title">📚 Informasi Kesehatan</h2>

    <div id="healthList" class="grid">

        <div class="card clickable" onclick="openHealth('pola')">
            <div class="card-icon">🥗</div>
            <h3>Pola Hidup Sehat</h3>
            <p>Tips menjaga kesehatan melalui kebiasaan sehari-hari.</p>
        </div>

        <div class="card clickable" onclick="openHealth('konsumsi')">
            <div class="card-icon">💊</div>
            <h3>Cara Konsumsi Obat yang Benar</h3>
            <p>Hal penting yang perlu diperhatikan saat menggunakan obat.</p>
        </div>

        <div class="card clickable" onclick="openHealth('simpan')">
            <div class="card-icon">📦</div>
            <h3>Cara Menyimpan Obat</h3>
            <p>Ketahui cara penyimpanan obat agar kualitasnya tetap terjaga.</p>
        </div>

        <div class="card clickable" onclick="openHealth('etiket')">
            <div class="card-icon">🏷️</div>
            <h3>Cara Membaca Etiket Obat</h3>
            <p>Mengenal informasi penting yang terdapat pada etiket.</p>
        </div>

        <div class="card clickable" onclick="openHealth('rumah')">
            <div class="card-icon">🏠</div>
            <h3>Pengelolaan Obat di Rumah</h3>
            <p>Tips menyimpan dan memeriksa obat yang ada di rumah.</p>
        </div>

        <div class="card clickable" onclick="openHealth('golongan')">
            <div class="card-icon">📋</div>
            <h3>Mengenal Golongan Obat</h3>
            <p>Mengenal perbedaan status dan penggunaan obat.</p>
        </div>

        <div class="card clickable" onclick="openHealth('sediaan')">
            <div class="card-icon">💧</div>
            <h3>Bentuk Sediaan Obat</h3>
            <p>Mengenal tablet, kapsul, sirup, salep, dan lainnya.</p>
        </div>

    </div>

    <div id="healthDetail" style="display:none;"></div>

</section>


<!-- ================= KONSELING ================= -->
<section id="konseling" class="page">

    <h2 class="section-title">👩‍⚕️ Konseling Apoteker</h2>

    <p style="text-align:center;color:var(--muted);margin-bottom:22px;">
        Pilih profil apoteker untuk membuka halaman konsultasi.
    </p>

    <div class="profile-grid">

        <div class="profile" onclick="openCounselor(0)">
            <div class="avatar">👩‍⚕️</div>
            <h3 style="margin-top:10px;">
                apt. Arlamadha Tri Wangsa, M.Farm
            </h3>
            <p>Spesialis Farmasi Komunitas</p>
            <p>Pengalaman 7 tahun</p>
            <span class="online">● Online</span>
        </div>


        <div class="profile" onclick="openCounselor(1)">
            <div class="avatar">👨‍⚕️</div>
            <h3 style="margin-top:10px;">
                apt. Chandra Gardipta, M.Farm
            </h3>
            <p>Spesialis Farmasi Klinik</p>
            <p>Pengalaman 10 tahun</p>
            <span class="online">● Online</span>
        </div>


        <div class="profile" onclick="openCounselor(2)">
            <div class="avatar">👩‍⚕️</div>
            <h3 style="margin-top:10px;">
                apt. Nastikah Syafitri, S.Farm
            </h3>
            <p>Apoteker</p>
            <p>Pengalaman 4 tahun</p>
            <span class="online">● Online</span>
        </div>

    </div>

    <div id="counselorDetail" style="display:none;margin-top:25px;"></div>

</section>


<!-- ================= INFORMASI PENTING ================= -->
<section id="penting" class="page">

    <h2 class="section-title">
        ⚠️ Informasi Penting — Antibiotik
    </h2>

    <div class="antibiotic-note">

        <h3>💊 Gunakan Antibiotik dengan Tepat</h3>

        <p style="font-size:14px;">
            Antibiotik digunakan untuk menangani infeksi bakteri tertentu
            dan bukan untuk mengobati infeksi yang disebabkan oleh virus,
            seperti sebagian besar flu dan pilek.
        </p>

        <br>

        <p style="font-size:14px;">
            Antibiotik termasuk obat yang penggunaannya memerlukan
            resep dokter. Jangan menggunakan antibiotik sembarangan,
            menggunakan sisa antibiotik sebelumnya, atau memberikan
            antibiotik kepada orang lain.
        </p>

        <br>

        <ul style="font-size:14px;padding-left:20px;">
            <li>Gunakan sesuai resep dokter.</li>
            <li>Gunakan sesuai dosis dan durasi yang diresepkan.</li>
            <li>Jangan menggunakan sisa antibiotik sebelumnya.</li>
            <li>Jangan memberikan antibiotik kepada orang lain.</li>
            <li>Antibiotik tidak digunakan untuk penyakit akibat virus.</li>
            <li>Penggunaan yang tidak tepat dapat berkontribusi terhadap resistensi antibiotik.</li>
            <li>Jika lupa minum, ikuti petunjuk pada resep/etiket atau tanyakan kepada apoteker.</li>
            <li>Jangan menggandakan dosis secara sembarangan.</li>
        </ul>

    </div>


    <div class="antibiotic-grid">

        <div class="antibiotic-card clickable"
             onclick="openAntibiotic('amoxicillin')">

            <div class="card-icon">💊</div>

            <h3>Amoxicillin</h3>

            <p>
                Zat aktif: Amoxicillin
            </p>

            <span class="status">
                Obat Keras — Resep Dokter
            </span>

            <br><br>

            <button class="btn">
                Lihat Detail
            </button>

        </div>


        <div class="antibiotic-card clickable"
             onclick="openAntibiotic('azithromycin')">

            <div class="card-icon">💊</div>

            <h3>Azithromycin</h3>

            <p>
                Zat aktif: Azithromycin
            </p>

            <span class="status">
                Obat Keras — Resep Dokter
            </span>

            <br><br>

            <button class="btn">
                Lihat Detail
            </button>

        </div>

    </div>

    <div id="antibioticDetail" style="display:none;margin-top:22px;"></div>

</section>


<!-- ================= LOGIN ================= -->
<section id="login" class="page">

    <h2 class="section-title">🔐 Login PharmaCare</h2>

    <div class="login-card">

        <p style="text-align:center;color:var(--muted);margin-bottom:20px;">
            Silakan masukkan nama lengkap untuk masuk.
        </p>

        <div class="form-group">

            <label>Nama Lengkap</label>

            <input
                type="text"
                id="loginName"
                placeholder="Masukkan nama lengkap">

        </div>

        <button class="btn" style="width:100%;" onclick="loginUser()">
            Masuk
        </button>

        <div id="loginMessage" style="text-align:center;margin-top:15px;"></div>

    </div>

</section>

</main>


<!-- FOOTER -->
<footer>

    <h3>🌸 PharmaCare</h3>

    <p>
        Your Guide to Medicine & Health Consultation
    </p>

    <p>
        Konten website ini bersifat edukatif dan tidak menggantikan
        pemeriksaan atau diagnosis oleh tenaga kesehatan.
    </p>

    <p>
        Untuk kondisi yang membutuhkan pemeriksaan langsung,
        konsultasikan dengan apoteker atau dokter.
    </p>

    <p style="margin-top:15px;">
        © 2026 PharmaCare
    </p>

</footer>


<script>

/* =========================================================
   DATABASE OBAT
========================================================= */

const medicines = [

    {
        id:"sanmol",
        category:"Demam",
        brand:"Sanmol",
        active:"Paracetamol",
        strength:"500 mg",
        form:"Tablet",
        status:"Obat Bebas",
        indication:"Membantu meredakan demam dan nyeri ringan sampai sedang.",
        contraindication:"Hipersensitivitas terhadap paracetamol. Perhatian khusus diperlukan pada gangguan hati.",
        sideEffect:"Mual, ruam, atau reaksi alergi dapat terjadi. Penggunaan berlebihan dapat menyebabkan kerusakan hati.",
        dose:"Ikuti aturan pada kemasan atau petunjuk tenaga kesehatan.",
        usage:"Ditelan dengan air. Jangan melebihi dosis yang dianjurkan.",
        storage:"Simpan pada suhu ruang, terlindung dari kelembapan dan panas berlebih.",
        warning:"Hindari penggunaan bersamaan dengan produk lain yang juga mengandung paracetamol tanpa memperhitungkan total dosis.",
        interaction:"Perlu perhatian terhadap obat tertentu yang memengaruhi fungsi hati atau metabolisme obat.",
        image:"assets/obat/sanmol.jpg"
    },

    {
        id:"panadol",
        category:"Demam",
        brand:"Panadol",
        active:"Paracetamol",
        strength:"500 mg",
        form:"Kaplet",
        status:"Obat Bebas",
        indication:"Meredakan demam serta nyeri ringan sampai sedang.",
        contraindication:"Hipersensitivitas terhadap kandungan produk.",
        sideEffect:"Dapat terjadi mual, ruam, atau reaksi hipersensitivitas.",
        dose:"Gunakan sesuai petunjuk pada kemasan.",
        usage:"Diminum dengan air dan tidak melebihi dosis yang dianjurkan.",
        storage:"Simpan di tempat kering pada suhu ruang.",
        warning:"Perhatikan kandungan paracetamol dari obat lain yang digunakan bersamaan.",
        interaction:"Dapat berinteraksi dengan beberapa obat tertentu; konsultasikan bila menggunakan obat lain secara rutin.",
        image:"assets/obat/panadol.jpg"
    },

    {
        id:"bodrex",
        category:"Demam",
        brand:"Bodrex",
        active:"Paracetamol",
        strength:"500 mg",
        form:"Kaplet",
        status:"Obat Bebas",
        indication:"Membantu meredakan sakit kepala dan demam.",
        contraindication:"Hipersensitivitas terhadap kandungan obat.",
        sideEffect:"Gangguan saluran cerna atau reaksi alergi dapat terjadi.",
        dose:"Sesuai petunjuk pada kemasan.",
        usage:"Diminum dengan air.",
        storage:"Simpan pada suhu ruang dan tempat kering.",
        warning:"Jangan menggunakan lebih dari dosis yang dianjurkan.",
        interaction:"Perhatikan penggunaan bersama obat lain yang mengandung paracetamol.",
        image:"assets/obat/bodrex.jpg"
    },

    {
        id:"proris",
        category:"Nyeri",
        brand:"Proris",
        active:"Ibuprofen",
        strength:"200 mg",
        form:"Kaplet",
        status:"Obat Bebas Terbatas*",
        indication:"Meredakan nyeri ringan sampai sedang dan demam sesuai indikasi.",
        contraindication:"Riwayat alergi terhadap NSAID, ulkus aktif, dan kondisi tertentu sesuai petunjuk produk.",
        sideEffect:"Mual, nyeri lambung, gangguan pencernaan, dan reaksi alergi.",
        dose:"Ikuti petunjuk pada kemasan atau tenaga kesehatan.",
        usage:"Diminum dengan air; sebaiknya setelah makan bila sesuai petunjuk produk.",
        storage:"Simpan di tempat kering dan terlindung dari panas.",
        warning:"Berhati-hati pada pasien dengan riwayat penyakit lambung, ginjal, atau penggunaan NSAID lain.",
        interaction:"Dapat berinteraksi dengan antikoagulan, NSAID lain, dan beberapa obat antihipertensi.",
        image:"assets/obat/proris.jpg"
    },

    {
        id:"promag",
        category:"Maag",
        brand:"Promag",
        active:"Antasida kombinasi",
        strength:"Sesuai sediaan",
        form:"Tablet kunyah",
        status:"Obat Bebas",
        indication:"Membantu meredakan gejala yang berkaitan dengan kelebihan asam lambung seperti nyeri ulu hati.",
        contraindication:"Hipersensitivitas terhadap kandungan produk.",
        sideEffect:"Gangguan saluran cerna dapat terjadi.",
        dose:"Sesuai petunjuk pada kemasan.",
        usage:"Tablet dikunyah sesuai petunjuk sebelum ditelan.",
        storage:"Simpan pada suhu ruang dan tempat kering.",
        warning:"Berikan jarak dengan obat tertentu karena antasida dapat memengaruhi penyerapan beberapa obat.",
        interaction:"Dapat mengurangi penyerapan obat tertentu bila diminum bersamaan.",
        image:"assets/obat/promag.jpg"
    },

    {
        id:"dulcolax",
        category:"Sembelit",
        brand:"Dulcolax",
        active:"Bisacodyl",
        strength:"5 mg",
        form:"Tablet salut enterik",
        status:"Obat Bebas Terbatas*",
        indication:"Digunakan sebagai laksatif untuk membantu mengatasi konstipasi.",
        contraindication:"Tidak digunakan pada kondisi tertentu seperti obstruksi usus atau nyeri perut akut yang belum diketahui penyebabnya.",
        sideEffect:"Kram perut, diare, dan rasa tidak nyaman pada perut.",
        dose:"Ikuti petunjuk pada kemasan atau tenaga kesehatan.",
        usage:"Telan utuh; jangan dikunyah atau dihancurkan jika sesuai bentuk sediaannya.",
        storage:"Simpan pada suhu ruang dan tempat kering.",
        warning:"Tidak dianjurkan digunakan terus-menerus tanpa evaluasi penyebab konstipasi.",
        interaction:"Penggunaan bersama obat tertentu perlu diperhatikan; konsultasikan kepada apoteker.",
        image:"assets/obat/dulcolax.jpg"
    },

    {
        id:"diapet",
        category:"Diare",
        brand:"Diapet",
        active:"Ekstrak bahan herbal sesuai formulasi produk",
        strength:"Sesuai sediaan",
        form:"Kapsul",
        status:"Obat Bebas",
        indication:"Digunakan sesuai informasi produk untuk membantu meredakan gejala diare.",
        contraindication:"Hipersensitivitas terhadap kandungan produk.",
        sideEffect:"Keluhan saluran cerna atau reaksi alergi dapat terjadi.",
        dose:"Sesuai aturan pada kemasan.",
        usage:"Diminum dengan air sesuai aturan penggunaan.",
        storage:"Simpan pada tempat kering dan terlindung dari panas.",
        warning:"Diare dengan darah, demam tinggi, dehidrasi berat, atau berlangsung lama memerlukan pemeriksaan tenaga kesehatan.",
        interaction:"Periksa penggunaan obat lain kepada apoteker.",
        image:"assets/obat/diapet.jpg"
    },

    {
        id:"cetirizine",
        category:"Alergi",
        brand:"Cetirizine",
        active:"Cetirizine",
        strength:"10 mg",
        form:"Tablet",
        status:"Obat Keras",
        indication:"Meredakan gejala alergi seperti bersin, hidung berair, dan gatal sesuai indikasi.",
        contraindication:"Hipersensitivitas terhadap cetirizine atau komponen terkait.",
        sideEffect:"Mengantuk, lelah, sakit kepala, atau mulut kering dapat terjadi.",
        dose:"Sesuai petunjuk dokter atau apoteker.",
        usage:"Diminum dengan air.",
        storage:"Simpan pada suhu ruang dan tempat kering.",
        warning:"Dapat menyebabkan kantuk pada sebagian orang; berhati-hati saat mengemudi.",
        interaction:"Informasikan kepada tenaga kesehatan jika menggunakan obat yang menyebabkan kantuk.",
        image:"assets/obat/cetirizine.jpg"
    },

    {
        id:"woods",
        category:"Flu dan Batuk",
        brand:"Woods",
        active:"Kandungan sesuai varian produk",
        strength:"Sesuai varian",
        form:"Sirup",
        status:"Periksa status pada kemasan",
        indication:"Membantu meredakan gejala batuk sesuai jenis dan formulasi produk.",
        contraindication:"Tergantung kandungan dan kondisi pasien.",
        sideEffect:"Dapat menyebabkan mual, kantuk, atau keluhan lain tergantung kandungan.",
        dose:"Gunakan sesuai etiket dan varian produk.",
        usage:"Gunakan sendok takar sesuai dosis.",
        storage:"Simpan sesuai petunjuk pada kemasan.",
        warning:"Jangan memilih obat batuk hanya berdasarkan merek; periksa kandungan dan jenis batuk.",
        interaction:"Periksa obat lain yang sedang digunakan untuk menghindari kandungan yang tumpang tindih.",
        image:"assets/obat/woods.jpg"
    },

    {
        id:"enervon-c",
        category:"Vitamin",
        brand:"Enervon-C",
        active:"Vitamin dan mineral sesuai formulasi produk",
        strength:"Sesuai formulasi",
        form:"Tablet",
        status:"Periksa status pada kemasan",
        indication:"Membantu memenuhi kebutuhan vitamin dan mineral sesuai kondisi.",
        contraindication:"Hipersensitivitas terhadap kandungan produk.",
        sideEffect:"Keluhan saluran cerna dapat terjadi pada sebagian pengguna.",
        dose:"Sesuai petunjuk pada kemasan.",
        usage:"Diminum sesuai petunjuk penggunaan.",
        storage:"Simpan pada tempat kering dan terlindung dari panas.",
        warning:"Suplemen tidak menggantikan pola makan seimbang.",
        interaction:"Informasikan penggunaan suplemen kepada tenaga kesehatan bila mengonsumsi obat rutin.",
        image:"assets/obat/enervon-c.jpg"
    }

];


/* =========================================================
   DATA APOTEKER
========================================================= */

const counselors = [

    {
        name:"apt. Arlamadha Tri Wangsa, M.Farm",
        specialty:"Spesialis Farmasi Komunitas",
        experience:"7 tahun",
        status:"Online"
    },

    {
        name:"apt. Chandra Gardipta, M.Farm",
        specialty:"Spesialis Farmasi Klinik",
        experience:"10 tahun",
        status:"Online"
    },

    {
        name:"apt. Nastikah Syafitri, S.Farm",
        specialty:"Apoteker",
        experience:"4 tahun",
        status:"Online"
    }

];


/* =========================================================
   NAVIGATION
========================================================= */

function showPage(page){

    document.querySelectorAll(".page").forEach(function(p){
        p.classList.remove("active");
    });

    document.getElementById(page).classList.add("active");

    window.scrollTo({
        top:0,
        behavior:"smooth"
    });
}


/* =========================================================
   KATEGORI OBAT
========================================================= */

function openCategory(category){

    showPage("obat");

    const list = medicines.filter(function(medicine){
        return medicine.category === category;
    });

    const categoryList = document.getElementById("categoryList");
    const medicineList = document.getElementById("medicineList");
    const detail = document.getElementById("medicineDetail");

    categoryList.style.display="none";
    detail.style.display="none";

    medicineList.style.display="block";

    let html=`

        <button class="btn btn-light back"
                onclick="backToCategories()">
            ← Kembali ke Kategori
        </button>

        <h2 class="section-title">
            ${category}
        </h2>

        <div class="medicine-grid">
    `;

    if(list.length===0){

        html += `
            <div class="card">
                <h3>Belum ada data</h3>
                <p>
                    Data obat pada kategori ini sedang disiapkan.
                </p>
            </div>
        `;

    }else{

        list.forEach(function(medicine){

            html += createMedicineCard(medicine);

        });

    }

    html += `</div>`;

    medicineList.innerHTML=html;
}


function createMedicineCard(medicine){

    return `

        <div class="medicine-card"
             onclick="openMedicine('${medicine.id}')">

            <div class="medicine-image">

                <img
                    src="${medicine.image}"
                    alt="${medicine.brand}"
                    onerror="this.style.display='none';
                    this.parentElement.innerHTML=
                    '<div class=\\'image-placeholder\\'>
                    <span>💊</span>Foto ${medicine.brand}</div>'">

            </div>

            <div class="medicine-content">

                <h3>${medicine.brand}</h3>

                <p>
                    <strong>Zat aktif:</strong>
                    ${medicine.active}
                </p>

                <p>
                    <strong>Kekuatan:</strong>
                    ${medicine.strength}
                </p>

                <span class="status">
                    ${medicine.status}
                </span>

            </div>

        </div>

    `;
}


function backToCategories(){

    document.getElementById("categoryList").style.display="block";
    document.getElementById("medicineList").style.display="none";
    document.getElementById("medicineDetail").style.display="none";

}


/* =========================================================
   DETAIL OBAT
========================================================= */

function openMedicine(id){

    const medicine=medicines.find(function(m){
        return m.id===id;
    });

    if(!medicine)return;

    const list=document.getElementById("medicineList");
    const detail=document.getElementById("medicineDetail");

    list.style.display="none";
    document.getElementById("categoryList").style.display="none";

    detail.style.display="block";

    detail.innerHTML=`

        <button class="btn btn-light back"
                onclick="openCategory('${medicine.category}')">
            ← Kembali ke ${medicine.category}
        </button>

        <div class="detail-card">

            <div class="detail-top">

                <div class="detail-image">

                    <img
                        src="${medicine.image}"
                        alt="${medicine.brand}"
                        onerror="this.style.display='none';
                        this.parentElement.innerHTML=
                        '<div class=\\'image-placeholder\\'>
                        <span>💊</span>
                        Foto ${medicine.brand}
                        </div>'">

                </div>


                <div>

                    <h2 class="detail-title">
                        ${medicine.brand}
                    </h2>

                    <p style="color:var(--muted);">
                        ${medicine.active}
                    </p>

                    <span class="status">
                        ${medicine.status}
                    </span>

                    <div class="info-list">

                        <div class="info-row">
                            <strong>Zat Aktif:</strong>
                            ${medicine.active}
                        </div>

                        <div class="info-row">
                            <strong>Kekuatan:</strong>
                            ${medicine.strength}
                        </div>

                        <div class="info-row">
                            <strong>Bentuk Sediaan:</strong>
                            ${medicine.form}
                        </div>

                        <div class="info-row">
                            <strong>Golongan/Status:</strong>
                            ${medicine.status}
                        </div>

                        <div class="info-row">
                            <strong>Indikasi:</strong>
                            ${medicine.indication}
                        </div>

                        <div class="info-row">
                            <strong>Kontraindikasi:</strong>
                            ${medicine.contraindication}
                        </div>

                        <div class="info-row">
                            <strong>Efek Samping:</strong>
                            ${medicine.sideEffect}
                        </div>

                        <div class="info-row">
                            <strong>Aturan Pakai:</strong>
                            ${medicine.dose}
                        </div>

                        <div class="info-row">
                            <strong>Cara Penggunaan:</strong>
                            ${medicine.usage}
                        </div>

                        <div class="info-row">
                            <strong>Cara Penyimpanan:</strong>
                            ${medicine.storage}
                        </div>

                        <div class="info-row">
                            <strong>Peringatan/Perhatian:</strong>
                            ${medicine.warning}
                        </div>

                        <div class="info-row">
                            <strong>Interaksi Obat:</strong>
                            ${medicine.interaction}
                        </div>

                    </div>

                </div>

            </div>

            <div class="warning">
                ⚠️ Informasi pada halaman ini bersifat edukatif.
                Selalu periksa kemasan/etiket dan konsultasikan dengan
                apoteker atau dokter apabila memiliki kondisi khusus
                atau menggunakan obat lain.
            </div>

            <br>

            <button class="btn"
                    onclick="showPage('konseling')">
                👩‍⚕️ Konsultasikan dengan Apoteker
            </button>

        </div>

    `;

    window.scrollTo({
        top:0,
        behavior:"smooth"
    });
}


/* =========================================================
   SEARCH OBAT
========================================================= */

function searchMedicine(){

    const query=document
        .getElementById("searchInput")
        .value
        .trim()
        .toLowerCase();

    const result=document.getElementById("searchResult");

    if(!query){

        result.innerHTML=`
            <p style="color:#b85c7b;">
                Silakan masukkan nama obat, zat aktif, atau kategori.
            </p>
        `;

        return;
    }

    const medicine=medicines.find(function(m){

        return (
            m.brand.toLowerCase().includes(query) ||
            m.active.toLowerCase().includes(query) ||
            m.category.toLowerCase().includes(query)
        );

    });

    if(medicine){

        result.innerHTML=`
            <button class="btn"
                    onclick="openMedicine('${medicine.id}')">
                💊 ${medicine.brand} — Lihat Detail
            </button>
        `;

        showPage("obat");

        setTimeout(function(){
            openMedicine(medicine.id);
        },100);

    }else{

        showPage("home");

        result.innerHTML=`
            <div style="
                background:#fff0f4;
                padding:13px;
                border-radius:12px;
                color:#963f60;">
                Obat belum ditemukan. Silakan periksa kembali
                nama obat atau konsultasikan dengan apoteker.
            </div>
        `;

    }

}


/* =========================================================
   INFORMASI KESEHATAN
========================================================= */

const healthArticles={

    pola:{
        title:"Pola Hidup Sehat",
        content:`
            <p>
                Pola hidup sehat merupakan kebiasaan yang dilakukan
                secara konsisten untuk membantu menjaga kesehatan tubuh.
            </p>

            <h3>Hal yang dapat dilakukan</h3>

            <ul>
                <li>Mengonsumsi makanan dengan gizi seimbang.</li>
                <li>Melakukan aktivitas fisik secara rutin.</li>
                <li>Mencukupi kebutuhan tidur.</li>
                <li>Menjaga kebersihan diri dan lingkungan.</li>
                <li>Menghindari kebiasaan yang berisiko bagi kesehatan.</li>
            </ul>
        `
    },

    konsumsi:{
        title:"Cara Konsumsi Obat yang Benar",
        content:`
            <p>
                Gunakan obat sesuai etiket, resep, atau petunjuk tenaga
                kesehatan.
            </p>

            <ul>
                <li>Perhatikan nama dan dosis obat.</li>
                <li>Perhatikan waktu penggunaan.</li>
                <li>Gunakan alat ukur yang sesuai untuk obat cair.</li>
                <li>Jangan menggandakan dosis tanpa petunjuk.</li>
                <li>Tanyakan kepada apoteker jika terdapat keraguan.</li>
            </ul>
        `
    },

    simpan:{
        title:"Cara Menyimpan Obat",
        content:`
            <p>
                Penyimpanan obat yang tepat membantu menjaga mutu obat.
            </p>

            <ul>
                <li>Simpan sesuai petunjuk pada kemasan.</li>
                <li>Hindari tempat yang panas dan lembap jika tidak sesuai.</li>
                <li>Simpan obat jauh dari jangkauan anak-anak.</li>
                <li>Perhatikan tanggal kedaluwarsa.</li>
                <li>Jangan menggunakan obat yang berubah warna, bau, atau bentuk secara tidak wajar.</li>
            </ul>
        `
    },

    etiket:{
        title:"Cara Membaca Etiket Obat",
        content:`
            <p>
                Etiket memberikan informasi penting mengenai obat yang
                akan digunakan.
            </p>

            <ul>
                <li>Nama pasien bila tercantum.</li>
                <li>Nama obat.</li>
                <li>Jumlah atau kekuatan obat.</li>
                <li>Aturan pakai.</li>
                <li>Waktu penggunaan.</li>
                <li>Petunjuk khusus penyimpanan atau penggunaan.</li>
            </ul>
        `
    },

    rumah:{
        title:"Pengelolaan Obat di Rumah",
        content:`
            <p>
                Obat di rumah perlu diperiksa secara berkala agar obat
                yang tersedia tetap aman digunakan.
            </p>

            <ul>
                <li>Periksa tanggal kedaluwarsa.</li>
                <li>Pisahkan obat yang sudah tidak layak digunakan.</li>
                <li>Simpan dalam kemasan aslinya jika memungkinkan.</li>
                <li>Jangan mencampurkan obat tanpa identitas.</li>
                <li>Jauhkan dari anak-anak.</li>
            </ul>
        `
    },

    golongan:{
        title:"Mengenal Golongan Obat",
        content:`
            <p>
                Obat memiliki status atau golongan tertentu yang berkaitan
                dengan cara memperoleh dan penggunaannya.
            </p>

            <h3>Contoh</h3>

            <ul>
                <li>Obat bebas.</li>
                <li>Obat bebas terbatas.</li>
                <li>Obat keras.</li>
                <li>Obat narkotika dan psikotropika sesuai ketentuan.</li>
            </ul>

            <p>
                Status obat harus dilihat berdasarkan ketentuan dan
                informasi resmi produk, bukan hanya berdasarkan nama merek.
            </p>
        `
    },

    sediaan:{
        title:"Bentuk Sediaan Obat",
        content:`
            <p>
                Obat tersedia dalam berbagai bentuk sediaan untuk
                menyesuaikan kebutuhan terapi dan cara penggunaan.
            </p>

            <ul>
                <li>Tablet</li>
                <li>Kapsul</li>
                <li>Sirup</li>
                <li>Suspensi</li>
                <li>Salep</li>
                <li>Krim</li>
                <li>Tetes mata</li>
                <li>Tetes telinga</li>
                <li>Injeksi</li>
            </ul>
        `
    }

};


function openHealth(id){

    const article=healthArticles[id];

    document.getElementById("healthList").style.display="none";

    const detail=document.getElementById("healthDetail");

    detail.style.display="block";

    detail.innerHTML=`

        <button class="btn btn-light back"
                onclick="backHealth()">
            ← Kembali
        </button>

        <div class="article">

            <h2 style="color:var(--pink-deep);">
                ${article.title}
            </h2>

            <br>

            ${article.content}

        </div>

    `;

}


function backHealth(){

    document.getElementById("healthList").style.display="grid";
    document.getElementById("healthDetail").style.display="none";

}


/* =========================================================
   KONSELING APOTEKER
========================================================= */

function openCounselor(index){

    const person=counselors[index];

    const detail=document.getElementById("counselorDetail");

    detail.style.display="block";

    detail.innerHTML=`

        <button class="btn btn-light back"
                onclick="document.getElementById('counselorDetail').style.display='none'">
            ← Kembali ke Profil
        </button>

        <div class="form-card">

            <div style="text-align:center;font-size:50px;">
                👩‍⚕️
            </div>

            <h2 style="text-align:center;color:var(--pink-deep);">
                ${person.name}
            </h2>

            <p style="text-align:center;">
                ${person.specialty}
            </p>

            <p style="text-align:center;">
                Pengalaman ${person.experience}
            </p>

            <p style="text-align:center;">
                <span class="online">
                    ● ${person.status}
                </span>
            </p>

            <br>

            <div class="form-group">

                <label>Nama Pengguna</label>

                <input
                    type="text"
                    id="questionName"
                    placeholder="Masukkan nama Anda">

            </div>

            <div class="form-group">

                <label>Pertanyaan</label>

                <textarea
                    id="questionText"
                    placeholder="Tuliskan pertanyaan Anda mengenai obat atau kesehatan..."></textarea>

            </div>

            <button
                class="btn"
                style="width:100%;"
                onclick="sendQuestion('${person.name}')">
                Kirim Pertanyaan
            </button>

            <div id="questionMessage"
                 style="text-align:center;margin-top:14px;">
            </div>

        </div>
    `;

    detail.scrollIntoView({
        behavior:"smooth"
    });

}


function sendQuestion(apoteker){

    const name=document.getElementById("questionName").value.trim();
    const question=document.getElementById("questionText").value.trim();
    const message=document.getElementById("questionMessage");

    if(!name || !question){

        message.innerHTML=`
            <span style="color:#b85c7b;">
                Nama dan pertanyaan harus diisi.
            </span>
        `;

        return;
    }

    message.innerHTML=`
        <div style="
            background:#eaf8f0;
            color:#277452;
            padding:12px;
            border-radius:12px;">

            Pertanyaan Anda telah disiapkan untuk
            <strong>${apoteker}</strong>.

            <br><br>

            Pada versi website statis ini, data belum dikirim
            ke server/database. Untuk konsultasi nyata,
            hubungkan formulir ini dengan sistem backend atau
            layanan formulir.
        </div>
    `;

}


/* =========================================================
   ANTIBIOTIK
========================================================= */

const antibiotics={

    amoxicillin:{
        brand:"Amoxicillin",
        active:"Amoxicillin",
        class:"Antibiotik beta-laktam — penisilin",
        form:"Kapsul / tablet / suspensi, tergantung produk",
        indication:"Digunakan untuk infeksi bakteri tertentu yang sensitif terhadap amoxicillin sesuai diagnosis dokter.",
        dose:"Mengikuti dosis dan durasi yang diresepkan dokter.",
        side:"Mual, diare, ruam, dan reaksi alergi dapat terjadi.",
        warning:"Hentikan penggunaan dan segera cari pertolongan medis bila muncul tanda reaksi alergi berat.",
        usage:"Gunakan tepat sesuai resep. Jangan membagikan obat kepada orang lain dan jangan menggunakan sisa antibiotik."
    },

    azithromycin:{
        brand:"Azithromycin",
        active:"Azithromycin",
        class:"Antibiotik makrolida",
        form:"Tablet / kapsul / suspensi, tergantung produk",
        indication:"Digunakan untuk infeksi bakteri tertentu sesuai diagnosis dan pertimbangan dokter.",
        dose:"Mengikuti dosis dan durasi yang diresepkan dokter.",
        side:"Mual, diare, nyeri perut, dan gangguan saluran cerna dapat terjadi.",
        warning:"Informasikan kepada dokter/apoteker mengenai obat lain dan riwayat penyakit yang dimiliki.",
        usage:"Gunakan sesuai resep. Jangan menggandakan dosis jika lupa tanpa mengikuti petunjuk tenaga kesehatan."
    }

};


function openAntibiotic(id){

    const a=antibiotics[id];

    const detail=document.getElementById("antibioticDetail");

    detail.style.display="block";

    detail.innerHTML=`

        <button class="btn btn-light back"
                onclick="document.getElementById('antibioticDetail').style.display='none'">
            ← Kembali
        </button>

        <div class="detail-card">

            <h2 class="detail-title">
                ${a.brand}
            </h2>

            <span class="status">
                Obat Keras — Penggunaan berdasarkan resep dokter
            </span>

            <div class="info-list">

                <div class="info-row">
                    <strong>Zat Aktif:</strong>
                    ${a.active}
                </div>

                <div class="info-row">
                    <strong>Golongan Antibiotik:</strong>
                    ${a.class}
                </div>

                <div class="info-row">
                    <strong>Bentuk Sediaan:</strong>
                    ${a.form}
                </div>

                <div class="info-row">
                    <strong>Indikasi:</strong>
                    ${a.indication}
                </div>

                <div class="info-row">
                    <strong>Aturan Penggunaan:</strong>
                    ${a.dose}
                </div>

                <div class="info-row">
                    <strong>Efek Samping:</strong>
                    ${a.side}
                </div>

                <div class="info-row">
                    <strong>Peringatan:</strong>
                    ${a.warning}
                </div>

                <div class="info-row">
                    <strong>Penggunaan yang Benar:</strong>
                    ${a.usage}
                </div>

            </div>

            <div class="warning">

                ⚠️ Antibiotik tidak digunakan untuk mengobati
                flu atau penyakit akibat virus.

                <br><br>

                Gunakan antibiotik sesuai resep dokter dan
                selesaikan terapi sesuai durasi yang diresepkan.
                Jangan menggunakan sisa antibiotik dan jangan
                memberikannya kepada orang lain.

            </div>

            <br>

            <button class="btn"
                    onclick="showPage('konseling')">
                👩‍⚕️ Konsultasikan dengan Apoteker
            </button>

        </div>
    `;

    detail.scrollIntoView({
        behavior:"smooth"
    });

}


/* =========================================================
   LOGIN
========================================================= */

function loginUser(){

    const name=document.getElementById("loginName").value.trim();
    const message=document.getElementById("loginMessage");

    if(!name){

        message.innerHTML=`
            <span style="color:#b85c7b;">
                Silakan masukkan nama lengkap.
            </span>
        `;

        return;
    }

    localStorage.setItem("pharmacareUser",name);

    message.innerHTML=`
        <div style="
            background:#eaf8f0;
            color:#277452;
            padding:12px;
            border-radius:12px;">

            Selamat datang,
            <strong>${name}</strong>! 🌸

        </div>
    `;

}


/* =========================================================
   INIT
========================================================= */

window.onload=function(){

    const savedName=localStorage.getItem("pharmacareUser");

    if(savedName){

        document.getElementById("loginName").value=savedName;

    }

};

</script>

</body>
</html>
