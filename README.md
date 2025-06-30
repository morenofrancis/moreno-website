<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Biografi Saya - [Nama Lengkap Anda]</title>

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

    <script src="https://kit.fontawesome.com/YOUR_FONT_AWESOME_KIT_ID.js" crossorigin="anonymous"></script>

    <style>
        /* Variabel Warna dan Font */
        :root {
            --light-primary: #F8F8F8; /* Latar belakang utama (putih pudar) */
            --light-secondary: #FFFFFF; /* Latar belakang bagian/kartu (putih bersih) */
            --pastel-blue: #A2D9CE;   /* Pastel biru/hijau laut */
            --pastel-pink: #F7CAC9;   /* Pastel pink */
            --pastel-yellow: #FBE69C; /* Pastel kuning */
            --text-dark: #333333; /* Teks gelap */
            --text-subtle: #777777; /* Teks abu-abu halus */
            --border-light: #E0E0E0; /* Border sangat terang */
            --shadow-light: rgba(0, 0, 0, 0.05); /* Bayangan sangat lembut */
            --border-radius-card: 10px;
            --border-radius-button: 30px; /* Lebih bulat untuk tombol */
            --transition-duration: 0.3s;

            --font-heading: 'Playfair Display', serif;
            --font-body: 'Poppins', sans-serif;
        }

        /* Reset CSS */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: var(--font-body);
            line-height: 1.7;
            color: var(--text-dark);
            background-color: var(--light-primary);
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        /* Utility Classes */
        .container {
            max-width: 1000px; /* Sedikit lebih sempit untuk kesan ramping */
            margin: 0 auto;
            padding: 0 25px;
        }

        /* Header / Hero Section */
        .hero-section {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: linear-gradient(135deg, var(--pastel-blue) 0%, var(--pastel-pink) 100%); /* Gradien pastel */
            position: relative;
            overflow: hidden;
            padding: 50px 0;
            color: var(--text-dark);
            position: relative;
        }

        .hero-content {
            z-index: 10;
            opacity: 0;
            transform: translateY(30px);
            animation: fadeInSlideUp 1.2s ease-out forwards;
            animation-delay: 0.8s;
            position: relative;
        }

        @keyframes fadeInSlideUp {
            to { opacity: 1; transform: translateY(0); }
        }

        .profile-pic-hero {
            width: 220px;
            height: 220px;
            border-radius: 50%;
            overflow: hidden;
            border: 6px solid var(--light-secondary); /* Border putih */
            box-shadow: 0 10px 30px var(--shadow-light); /* Bayangan lembut */
            margin: 0 auto 35px auto;
            transition: transform var(--transition-duration) ease-in-out, box-shadow var(--transition-duration) ease-in-out;
            cursor: pointer;
            position: relative; /* Untuk efek hover circle */
        }

        .profile-pic-hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.3); /* Overlay putih semi-transparan */
            transform: scale(0);
            opacity: 0;
            transition: transform 0.4s ease-out, opacity 0.4s ease-out;
            z-index: 1;
        }

        .profile-pic-hero:hover::before {
            transform: scale(1);
            opacity: 1;
        }

        .profile-pic-hero img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
            position: relative;
            z-index: 2;
        }

        .hero-content h1 {
            font-family: var(--font-heading);
            font-size: 4.8rem; /* Ukuran besar namun elegan */
            margin-bottom: 20px;
            color: var(--text-dark);
            line-height: 1.1;
            letter-spacing: -0.5px;
            position: relative;
        }

        .hero-content h1::after {
            content: '';
            position: absolute;
            left: 50%;
            bottom: -10px;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--pastel-yellow);
            border-radius: 2px;
        }

        .hero-content p {
            font-family: var(--font-body);
            font-size: 1.6rem;
            color: var(--text-dark);
            max-width: 700px;
            margin: 0 auto;
            font-weight: 300;
            opacity: 0.9;
        }

        /* Navigasi Utama */
        nav {
            background-color: var(--light-secondary);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 15px var(--shadow-light);
            border-bottom: 1px solid var(--border-light);
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
        }

        nav ul li a {
            color: var(--text-subtle);
            text-decoration: none;
            font-family: var(--font-body);
            font-weight: 500;
            font-size: 1.05rem;
            padding: 10px 20px;
            border-radius: var(--border-radius-button); /* Lebih bulat */
            transition: all var(--transition-duration) ease-in-out;
            position: relative;
        }

        nav ul li a::before {
            content: '';
            position: absolute;
            bottom: 8px;
            left: 50%;
            transform: translateX(-50%);
            width: 0;
            height: 3px;
            background-color: var(--pastel-blue);
            border-radius: 1.5px;
            transition: width var(--transition-duration) ease-in-out;
        }

        nav ul li a:hover::before,
        nav ul li a.active::before {
            width: 100%;
        }

        nav ul li a:hover,
        nav ul li a.active {
            color: var(--text-dark);
            background-color: rgba(0, 0, 0, 0.03); /* Sedikit bayangan saat hover */
        }

        /* Konten Utama */
        main {
            padding: 80px 0 60px 0;
        }

        /* Gaya Umum untuk Setiap Bagian (Section) */
        section {
            background-color: var(--light-secondary);
            margin-bottom: 50px;
            padding: 60px;
            border-radius: var(--border-radius-card);
            box-shadow: 0 8px 25px var(--shadow-light);
            border: 1px solid var(--border-light);
            opacity: 0;
            transform: translateY(40px);
            transition: opacity 0.8s ease-out, transform 0.8s ease-out;
        }

        section.fade-in {
            opacity: 1;
            transform: translateY(0);
        }

        /* Judul H2 di Setiap Bagian */
        section h2 {
            font-family: var(--font-heading);
            color: var(--text-dark);
            font-size: 3.5rem; /* Ukuran yang elegan */
            margin-bottom: 40px;
            text-align: center;
            position: relative;
            padding-bottom: 15px;
            letter-spacing: -0.5px;
        }

        section h2::after {
            content: '';
            position: absolute;
            left: 50%;
            bottom: 0;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background-color: var(--pastel-pink); /* Warna underline berbeda */
            border-radius: 2px;
        }

        section p {
            font-family: var(--font-body);
            font-size: 1.15rem;
            color: var(--text-dark);
            margin-bottom: 25px;
            line-height: 1.8;
            opacity: 0.9;
        }

        /* Detail Data Diri */
        .personal-details-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .detail-item {
            background-color: var(--light-primary);
            padding: 30px;
            border-radius: var(--border-radius-card);
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.03);
            display: flex;
            align-items: center;
            gap: 20px;
            border: 1px solid var(--border-light);
            transition: transform var(--transition-duration) ease-out, box-shadow var(--transition-duration) ease-out;
        }

        .detail-item:hover {
            transform: translateY(-8px);
            box-shadow: 0 8px 25px var(--shadow-light);
        }

        .detail-item i {
            font-size: 2.8rem;
            color: var(--pastel-blue); /* Ikon warna pastel */
            flex-shrink: 0;
        }

        .detail-item div {
            text-align: left;
        }

        .detail-item h3 {
            font-family: var(--font-body);
            font-weight: 600;
            font-size: 1.5rem;
            color: var(--text-dark);
            margin-bottom: 5px;
        }

        .detail-item p {
            font-family: var(--font-body);
            font-size: 1.05rem;
            color: var(--text-subtle);
            margin-bottom: 0;
        }

        /* Hobi (Hobbies Grid) */
        .hobbies-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .hobby-card {
            background-color: var(--light-primary);
            padding: 35px;
            border-radius: var(--border-radius-card);
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.04);
            text-align: center;
            border: 1px solid var(--border-light);
            transition: all var(--transition-duration) ease-out;
        }

        .hobby-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 10px 30px var(--shadow-light);
            background-color: var(--light-secondary);
        }

        .hobby-card i {
            font-size: 4rem;
            color: var(--pastel-pink); /* Ikon warna pastel pink */
            margin-bottom: 20px;
            transition: transform var(--transition-duration) ease-out;
        }
        .hobby-card:hover i {
            transform: scale(1.1) rotate(2deg);
            color: var(--pastel-blue); /* Berubah warna saat hover */
        }

        .hobby-card h3 {
            font-family: var(--font-body);
            font-weight: 600;
            font-size: 1.7rem;
            color: var(--text-dark);
            margin-bottom: 12px;
        }

        .hobby-card p {
            font-family: var(--font-body);
            font-size: 1rem;
            color: var(--text-subtle);
            margin-bottom: 0;
        }

        /* Riwayat Pendidikan (Gaya Kartu Grid BARU) */
        .education-cards-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(380px, 1fr)); /* Minimal 380px per kartu */
            gap: 35px; /* Jarak antar kartu lebih besar */
            margin-top: 40px;
            justify-content: center; /* Pusatkan kartu jika tidak memenuhi grid penuh */
        }

        .education-card {
            background-color: var(--light-primary); /* Latar belakang kartu sama dengan primary */
            padding: 35px; /* Padding lebih luas */
            border-radius: var(--border-radius-card);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.05); /* Bayangan lembut */
            border: 1px solid var(--border-light);
            display: flex;
            align-items: flex-start; /* Konten dimulai dari atas */
            gap: 25px; /* Jarak antara ikon dan konten */
            transition: transform var(--transition-duration) ease-out, box-shadow var(--transition-duration) ease-out, background-color var(--transition-duration) ease-out;
            position: relative;
            overflow: hidden; /* Untuk efek border overlay */
        }

        .education-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px; /* Garis aksen di atas kartu */
            background-color: var(--pastel-blue); /* Warna aksen */
            transform: translateY(-100%);
            transition: transform 0.4s ease-out;
        }

        .education-card:hover::before {
            transform: translateY(0);
        }

        .education-card:hover {
            transform: translateY(-12px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.08); /* Bayangan lebih jelas saat hover */
            background-color: var(--light-secondary); /* Sedikit lebih terang saat hover */
        }

        .education-card .card-icon {
            flex-shrink: 0; /* Pastikan ikon tidak mengecil */
            width: 70px; /* Ukuran area ikon */
            height: 70px;
            background-color: var(--pastel-yellow); /* Latar belakang ikon */
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.08);
            transition: background-color var(--transition-duration) ease-out;
        }

        .education-card:hover .card-icon {
            background-color: var(--pastel-pink); /* Warna ikon berubah saat hover */
        }

        .education-card .card-icon i {
            font-size: 2.5rem; /* Ukuran ikon */
            color: var(--text-dark); /* Warna ikon di dalam lingkaran */
            transition: transform var(--transition-duration) ease-out;
        }

        .education-card:hover .card-icon i {
            transform: scale(1.1); /* Ikon sedikit membesar */
        }

        .education-card .card-content {
            flex-grow: 1;
        }

        .education-card .card-content h3 {
            font-family: var(--font-body);
            font-weight: 700;
            color: var(--text-dark);
            font-size: 1.8rem; /* Ukuran judul institusi */
            margin-bottom: 8px;
            line-height: 1.2;
        }

        .education-card .card-content .degree {
            font-family: var(--font-body);
            font-weight: 500;
            color: var(--pastel-blue);
            font-size: 1.15rem;
            margin-bottom: 6px;
            display: block;
        }

        .education-card .card-content .period {
            font-family: var(--font-body);
            font-size: 0.95rem;
            color: var(--text-subtle);
            margin-bottom: 15px;
            display: block;
        }

        .education-card .card-content ul {
            list-style: none;
            padding-left: 0;
            margin-bottom: 0;
            border-top: 1px dashed var(--border-light); /* Garis pemisah tipis */
            padding-top: 15px;
            margin-top: 15px;
        }

        .education-card .card-content ul li {
            position: relative;
            padding-left: 20px;
            margin-bottom: 8px;
            font-size: 0.98rem;
            color: var(--text-dark);
            opacity: 0.9;
        }

        .education-card .card-content ul li::before {
            content: '\2022';
            color: var(--pastel-pink);
            font-weight: bold;
            display: inline-block;
            width: 1em;
            margin-left: -1em;
            position: absolute;
            left: 0;
            font-size: 1.2em;
            line-height: 1;
        }

        /* Kontak */
        .contact-links {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 25px;
            margin-top: 40px;
        }

        .contact-button {
            background-color: var(--pastel-blue);
            color: var(--text-dark); /* Teks gelap di tombol terang */
            padding: 15px 30px;
            border-radius: var(--border-radius-button); /* Bulat */
            text-decoration: none;
            font-family: var(--font-body);
            font-weight: 600;
            font-size: 1.15rem;
            transition: all var(--transition-duration) ease-in-out;
            display: inline-flex;
            align-items: center;
            gap: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            border: none;
        }

        .contact-button:hover {
            background-color: var(--pastel-pink); /* Berubah warna saat hover */
            transform: translateY(-6px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
        }

        .contact-button i {
            font-size: 1.6rem;
            color: var(--text-dark);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 40px;
            margin-top: 60px;
            background-color: var(--light-secondary);
            color: var(--text-subtle);
            font-family: var(--font-body);
            font-size: 0.95rem;
            box-shadow: inset 0 1px 8px rgba(0, 0, 0, 0.03);
            border-top: 1px solid var(--border-light);
        }

        /* --- LIGHTBOX (GALERI FOTO POP-UP) --- */
        .lightbox-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 9999;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.4s ease;
            cursor: pointer;
        }

        .lightbox-overlay.active {
            display: flex;
            opacity: 1;
        }

        .lightbox-content {
            background-color: var(--light-secondary);
            padding: 30px;
            border-radius: var(--border-radius-card);
            box-shadow: 0 15px 50px rgba(0, 0, 0, 0.4);
            max-width: 85%;
            max-height: 85%;
            overflow-y: auto;
            position: relative;
            transform: scale(0.8);
            opacity: 0;
            transition: transform 0.4s ease-out, opacity 0.4s ease-out;
        }

        .lightbox-overlay.active .lightbox-content {
            transform: scale(1);
            opacity: 1;
        }

        .lightbox-close {
            position: absolute;
            top: 15px;
            right: 25px;
            font-size: 3rem;
            color: var(--text-subtle);
            cursor: pointer;
            z-index: 10000;
            transition: color 0.3s ease, transform 0.3s ease;
        }

        .lightbox-close:hover {
            color: var(--pastel-pink);
            transform: rotate(90deg);
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 20px;
            padding: 20px;
            justify-content: center;
        }

        .gallery-item {
            width: 100%;
            height: 180px;
            overflow: hidden;
            border-radius: var(--border-radius-card);
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
            border: 2px solid var(--border-light);
        }

        .gallery-item:hover {
            transform: scale(1.05);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.15);
            border-color: var(--pastel-blue);
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
        }

        /* Responsivitas */
        @media (max-width: 992px) {
            .hero-content h1 {
                font-size: 4rem;
            }
            .hero-content p {
                font-size: 1.4rem;
            }
            section {
                padding: 45px;
                margin-bottom: 40px;
            }
            section h2 {
                font-size: 3rem;
            }
            /* Responsivitas untuk Education Cards */
            .education-cards-grid {
                grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
                gap: 30px;
            }
            .education-card {
                padding: 30px;
                gap: 20px;
            }
            .education-card .card-icon {
                width: 60px;
                height: 60px;
            }
            .education-card .card-icon i {
                font-size: 2.2rem;
            }
            .education-card .card-content h3 {
                font-size: 1.6rem;
            }
            .education-card .card-content .degree {
                font-size: 1.1rem;
            }
        }

        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 3.2rem;
            }
            .hero-content p {
                font-size: 1.2rem;
            }
            .profile-pic-hero {
                width: 180px;
                height: 180px;
            }
            nav ul {
                gap: 15px;
                padding: 8px;
            }
            nav ul li a {
                font-size: 0.95rem;
                padding: 8px 15px;
            }
            section {
                padding: 30px;
                margin-bottom: 30px;
            }
            section h2 {
                font-size: 2.5rem;
                margin-bottom: 30px;
            }
            .personal-details-grid, .hobbies-grid {
                grid-template-columns: 1fr;
            }
            .detail-item {
                flex-direction: column;
                align-items: center;
                text-align: center;
                gap: 12px;
                padding: 25px;
            }
            .detail-item i {
                margin-bottom: 0;
            }
            /* Responsivitas untuk Education Cards */
            .education-cards-grid {
                grid-template-columns: 1fr; /* Satu kolom di layar kecil */
                gap: 25px;
            }
            .education-card {
                flex-direction: column; /* Ikon di atas konten */
                align-items: center;
                text-align: center;
                padding: 25px;
                gap: 15px;
            }
            .education-card .card-icon {
                margin-bottom: 10px;
            }
            .education-card .card-content h3 {
                font-size: 1.5rem;
            }
            .education-card .card-content ul {
                text-align: left; /* Biarkan bullet points tetap rata kiri */
            }
            .education-card .card-content ul li {
                padding-left: 25px; /* Sesuaikan padding agar bullet masuk */
            }
            .contact-links {
                flex-direction: column;
                align-items: center;
            }
            .lightbox-content {
                max-width: 90%;
                padding: 20px;
            }
            .gallery-grid {
                grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
                gap: 15px;
            }
            .gallery-item {
                height: 120px;
            }
        }

        @media (max-width: 480px) {
            .hero-content h1 {
                font-size: 2.5rem;
                letter-spacing: normal;
            }
            .hero-content p {
                font-size: 1rem;
            }
            .profile-pic-hero {
                width: 150px;
                height: 150px;
            }
            section h2 {
                font-size: 2rem;
            }
            .detail-item h3 {
                font-size: 1.3rem;
            }
            .detail-item p {
                font-size: 0.9rem;
            }
            .hobby-card h3 {
                font-size: 1.4rem;
            }
            /* Responsivitas untuk Education Cards */
            .education-card {
                padding: 20px;
            }
            .education-card .card-icon {
                width: 50px;
                height: 50px;
            }
            .education-card .card-icon i {
                font-size: 1.8rem;
            }
            .education-card .card-content h3 {
                font-size: 1.3rem;
            }
            .education-card .card-content .degree {
                font-size: 1rem;
            }
            .education-card .card-content .period {
                font-size: 0.85rem;
            }
            .education-card .card-content ul li {
                font-size: 0.9rem;
            }
            .contact-button {
                font-size: 1rem;
                padding: 12px 25px;
            }
            .lightbox-close {
                font-size: 2.2rem;
                top: 10px;
                right: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="hero-section">
        <div class="hero-content">
            <div class="profile-pic-hero" id="profilePicHero">
                <img src="C:\Users\ZYREX\Pictures\43ba23a0-c370-4027-a655-7a810e1b0b73.jfif" alt="Foto Profil Anda">
            </div>
            <h1>Moreno Francis</h1>
            <p>Selamat Datang di Profil Saya!</p>
        </div>
    </div>

    <nav>
        <ul>
            <li><a href="#about" class="active">Tentang Saya</a></li>
            <li><a href="#personal-data">Data Diri</a></li>
            <li><a href="#hobbies">Hobi</a></li>
            <li><a href="#education">Pendidikan</a></li>
            <li><a href="#contact">Kontak</a></li>
        </ul>
    </nav>

    <main class="container">
        <section id="about">
            <h2>Tentang Saya</h2>
            <p>Saya Moreno Francis, seorang mahasiswa semester 4 yang berkuliah di Universitas Kristen Indonesia Maluku.</p>
            <p>Mata kuliah pemrograman web memberikan keterampilan yang sangat relevan dengan dunia kerja. Di era digital ini, hampir semua perusahaan, organisasi, dan bahkan individu memiliki kehadiran online melalui website. Dengan mempelajari pengembangan web, mahasiswa mempersiapkan diri untuk memasuki dunia industri teknologi yang terus berkembang. Keterampilan ini sangat dicari oleh perusahaan, terutama dalam bidang pengembangan web..</p>
        </section>

        <section id="personal-data">
            <h2>Data Diri</h2>
            <div class="personal-details-grid">
                <div class="detail-item">
                    <i class="fas fa-user-alt"></i>
                    <div>
                        <h3>NAMA</h3>
                        <p>Moreno Francis</p>
                    </div>
                </div>
                <div class="detail-item">
                    <i class="fas fa-calendar-day"></i>
                    <div>
                        <h3>TEMPAT TANGGAL LAHIR</h3>
                        <p>Ambon, 24 November 2004</p>
                    </div>
                </div>
                <div class="detail-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <div>
                        <h3>DOMISILI</h3>
                        <p>Waipia, Maluku Tengah, Indonesia</p>
                    </div>
                </div>
                <div class="detail-item">
                    <i class="fas fa-restroom"></i>
                    <div>
                        <h3>JENIS KELAMIN</h3>
                        <p>Pria</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="hobbies">
            <h2>Hobi</h2>
            <p style="text-align: center; margin-bottom: 35px; font-size: 1.1rem; color: var(--text-subtle);">Aktivitas yang saya nikmati di waktu luang untuk relaksasi dan inspirasi.</p>
                <div class="hobby-card">
                    <i class="fas fa-spa"></i>
                    <h3>BEROLAHRAGA</h3>
                    <p>Menjaga keseimbangan pikiran dan tubuh melalui praktik ketenangan.</p>
                </div>
                <div class="hobby-card">
                    <i class="fas fa-mountain"></i>
                    <h3>HIKING/ALAM</h3>
                    <p>Menjelajahi keindahan alam dan menikmati udara segar jalan atau pantai.</p>
                </div>
                <div class="hobby-card">
                    <i class="fas fa-seedling"></i>
                    <h3>BERKEBUN</h3>
                    <p>Merawat tanaman dan menikmati hasil panen dari kebun sendiri.</p>
                </div>
                <div class="hobby-card">
                    <i class="fas fa-puzzle-piece"></i>
                    <h3>DRIVE</h3>
                    <p>Mengemudi memberikan kenyamanan, kebebasan, dan kemudahan dalam melakukan berbagai aktivitas sehari-hari, baik untuk pekerjaan, keluarga, atau sekadar sebagai hobi. Tentu, tujuan seseorang mengemudi sangat tergantung pada konteks hidup dan kebutuhannya.</p>
                </div>
                </div>
        </section>

        <section id="education">
            <h2>Riwayat Pendidikan</h2>
            <p style="text-align: center; margin-bottom: 45px; font-size: 1.1rem; color: var(--text-subtle);">Setiap langkah dalam perjalanan akademik saya, diwakili oleh dedikasi dan pertumbuhan.</p>

            <div class="education-cards-grid">
                <div class="education-card">
                    <div class="card-icon">
                        <i class="fas fa-graduation-cap"></i>
                    </div>
                    <div class="card-content">
                        <h3>UKIM</h3>
                        <span class="degree">S1 Ilmu Komputer</span>
                    </div>
                </div>

                <div class="education-card">
                    <div class="card-icon">
                        <i class="fas fa-school"></i>
                    </div>
                    <div class="card-content">
                        <h3>SMK</h3>
                        <span class="degree">Jurusan TKJ</span>
                    </div>
                </div>

                <div class="education-card">
                    <div class="card-icon">
                        <i class="fas fa-book-open"></i>
                    </div>
                    <div class="card-content">
                        <h3>SMP</h3>
                    </div>
                </div>

                <div class="education-card">
                    <div class="card-icon">
                        <i class="fas fa-child"></i>
                    </div>
                    <div class="card-content">
                        <h3>SD</h3>
                    </div>
                </div>
                </div>
        </section>

        <section id="contact">
            <h2>Hubungi Saya</h2>
            <div class="contact-links">
                <a href="https://www.instagram.com/renox_fs?igsh=ZXUzMm90a3YzbWJi" class="contact-button" target="_blank">
                    <i class="fab fa-instagram"></i> Instagram
                </a>
                </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 God Bless u</p>
    </footer>
	
	<div class="hero-section">
        <div class="hero-content">
            <h1>Moreno Francis</h1>
            <p>Terima Kasih sudah Mengunjungi Profil saya!</p>
        </div>
    </div>

    <div class="lightbox-overlay" id="lightboxOverlay">
        <span class="lightbox-close">&times;</span>
        <div class="lightbox-content">
            <h2>Galeri Momen Saya</h2>
            <div class="gallery-grid" id="profileGalleryGrid">
                </div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Data foto profil untuk galeri lightbox
            const profilePhotos = [
                { src: 'https://via.placeholder.com/600/F7CAC9/333333?text=Karya+1', alt: 'Foto Karya 1' },
                { src: 'https://via.placeholder.com/600/A2D9CE/333333?text=Aktivitas+Santai', alt: 'Foto Aktivitas Santai' },
                { src: 'https://via.placeholder.com/600/FBE69C/333333?text=Inspirasi+Desain', alt: 'Foto Inspirasi Desain' },
                { src: 'https://via.placeholder.com/600/FFFFFF/F7CAC9?text=Momen+Personal', alt: 'Foto Momen Personal' },
                { src: 'https://via.placeholder.com/600/E0E0E0/A2D9CE?text=Proyek+Kreatif', alt: 'Foto Proyek Kreatif' },
                { src: 'https://via.placeholder.com/600/F8F8F8/FBE69C?text=Liburan', alt: 'Foto Liburan' }
            ];

            const profilePicHero = document.getElementById('profilePicHero');
            const lightboxOverlay = document.getElementById('lightboxOverlay');
            const lightboxClose = document.querySelector('.lightbox-close');
            const profileGalleryGrid = document.getElementById('profileGalleryGrid');

            // Fungsi untuk memuat gambar ke galeri lightbox
            function loadGalleryPhotos() {
                profileGalleryGrid.innerHTML = ''; // Kosongkan galeri sebelumnya
                profilePhotos.forEach(photo => {
                    const galleryItem = document.createElement('div');
                    galleryItem.classList.add('gallery-item');
                    const img = document.createElement('img');
                    img.src = photo.src;
                    img.alt = photo.alt;
                    galleryItem.appendChild(img);
                    profileGalleryGrid.appendChild(galleryItem);
                });
            }

            // Buka lightbox saat foto profil utama diklik
            profilePicHero.addEventListener('click', function() {
                loadGalleryPhotos(); // Muat ulang gambar setiap kali dibuka
                lightboxOverlay.classList.add('active');
                document.body.style.overflow = 'hidden'; // Nonaktifkan scroll body
            });

            // Tutup lightbox saat tombol close diklik atau area overlay diklik
            lightboxClose.addEventListener('click', function() {
                lightboxOverlay.classList.remove('active');
                document.body.style.overflow = ''; // Aktifkan kembali scroll body
            });

            lightboxOverlay.addEventListener('click', function(e) {
                // Tutup hanya jika klik dilakukan di overlay itu sendiri, bukan di dalam konten lightbox
                if (e.target === lightboxOverlay) {
                    lightboxOverlay.classList.remove('active');
                    document.body.style.overflow = '';
                }
            });

            // --- Fungsionalitas Navigasi & Animasi Scroll ---

            // Smooth scrolling untuk link navigasi
            document.querySelectorAll('nav a').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href').substring(1);
                    const targetElement = document.getElementById(targetId);
                    if (targetElement) {
                        const navHeight = document.querySelector('nav').offsetHeight;
                        window.scrollTo({
                            top: targetElement.offsetTop - navHeight, // Sesuaikan dengan tinggi nav
                            behavior: 'smooth'
                        });
                    }
                });
            });

            // Animasi fade-in untuk setiap section saat di-scroll
            const sections = document.querySelectorAll('main section');
            const observerOptions = {
                root: null,
                rootMargin: '0px',
                threshold: 0.1 // Animasi mulai saat 10% dari section terlihat
            };

            const observer = new IntersectionObserver((entries, observer) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('fade-in');
                        // observer.unobserve(entry.target); // Opsional: Hentikan observasi setelah animasi pertama kali
                    }
                });
            }, observerOptions);

            sections.forEach(section => {
                observer.observe(section);
            });

            // Menentukan link navigasi yang aktif berdasarkan posisi scroll
            function setActiveNavLinkOnScroll() {
                const navHeight = document.querySelector('nav').offsetHeight;
                const scrollPosition = window.scrollY + navHeight + 20; // Offset sedikit ke bawah

                document.querySelectorAll('nav a').forEach(anchor => {
                    const targetId = anchor.getAttribute('href').substring(1);
                    const targetElement = document.getElementById(targetId);

                    if (targetElement) {
                        if (scrollPosition >= targetElement.offsetTop && scrollPosition < targetElement.offsetTop + targetElement.offsetHeight) {
                            document.querySelectorAll('nav a').forEach(navLink => navLink.classList.remove('active'));
                            anchor.classList.add('active');
                        }
                    }
                });

                // Pastikan link 'Tentang' aktif jika di paling atas
                if (window.scrollY < document.getElementById('about').offsetTop - navHeight) {
                    document.querySelectorAll('nav a').forEach(navLink => navLink.classList.remove('active'));
                    document.querySelector('nav a[href="#about"]').classList.add('active');
                }
            }

            // Panggil saat halaman dimuat dan saat di-scroll
            window.addEventListener('load', setActiveNavLinkOnScroll);
            window.addEventListener('scroll', setActiveNavLinkOnScroll);
            setActiveNavLinkOnScroll(); // Panggilan awal
        });
    </script>
</body>
</html>
