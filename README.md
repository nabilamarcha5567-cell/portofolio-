<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Portofolio Marcha Nabila Alfatuz Zahra</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        :root {
            --bg: #eef8ff;
            --card: #ffffff;
            --text: #263746;
            --primary: #7dbde8;
            --primary-dark: #4e9ed2;
            --secondary: #dff2ff;
            --danger: #ef7d8a;
            --shadow: 0 8px 25px rgba(80, 150, 200, 0.15);
        }

        body.dark {
            --bg: #17212b;
            --card: #22303c;
            --text: #f1f8ff;
            --primary: #70b8e8;
            --primary-dark: #9bd5f5;
            --secondary: #2b4050;
            --shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
        }

        body {
            font-family: Arial, sans-serif;
            background: var(--bg);
            color: var(--text);
            line-height: 1.6;
            transition: 0.3s;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        /* ================= HEADER ================= */

        header {
            position: sticky;
            top: 0;
            z-index: 1000;
            background: var(--card);
            box-shadow: var(--shadow);
        }

        .navbar {
            max-width: 1100px;
            margin: auto;
            padding: 15px 25px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
            color: var(--primary-dark);
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 25px;
            align-items: center;
        }

        .nav-menu a {
            font-weight: bold;
        }

        .nav-menu a:hover {
            color: var(--primary-dark);
        }

        .theme-button,
        .menu-button {
            border: none;
            background: var(--secondary);
            color: var(--text);
            padding: 9px 12px;
            border-radius: 12px;
            cursor: pointer;
            font-size: 18px;
        }

        .menu-button {
            display: none;
        }

        /* ================= GENERAL ================= */

        section {
            max-width: 1100px;
            margin: auto;
            padding: 80px 25px;
        }

        .section-title {
            text-align: center;
            font-size: 32px;
            margin-bottom: 40px;
            color: var(--primary-dark);
        }

        /* ================= HERO ================= */

        .hero {
            min-height: 90vh;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 50px;
        }

        .hero-text {
            flex: 1;
        }

        .small-title {
            color: var(--primary-dark);
            font-weight: bold;
            font-size: 18px;
        }

        .hero h1 {
            font-size: 48px;
            margin: 10px 0;
        }

        .hero h2 {
            font-size: 28px;
            color: var(--primary-dark);
            margin-bottom: 15px;
        }

        .hero p {
            max-width: 600px;
            margin-bottom: 25px;
        }

        .main-button {
            display: inline-block;
            background: var(--primary);
            color: white;
            padding: 12px 22px;
            border-radius: 15px;
            font-weight: bold;
        }

        .main-button:hover {
            background: var(--primary-dark);
        }

        /* ================= FOTO ================= */

        .hero-photo {
            flex: 1;
            text-align: center;
        }

        .photo-frame {
            width: 300px;
            height: 350px;
            margin: auto;
            border-radius: 30px;
            background: var(--secondary);
            padding: 12px;
            box-shadow: var(--shadow);
        }

        .photo-frame img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 23px;
        }

        /* ================= ABOUT ================= */

        .about-card,
        .biodata,
        .education,
        .contact-box {
            background: var(--card);
            padding: 30px;
            border-radius: 25px;
            box-shadow: var(--shadow);
            margin-bottom: 30px;
        }

        .about-card h3,
        .biodata h3,
        .education h3 {
            color: var(--primary-dark);
            margin-bottom: 15px;
        }

        .biodata p {
            margin: 8px 0;
        }

        .biodata strong {
            display: inline-block;
            width: 130px;
        }

        /* ================= PENDIDIKAN ================= */

        .education-item {
            padding: 15px;
            margin: 10px 0;
            background: var(--secondary);
            border-radius: 15px;
        }

        .education-item strong {
            color: var(--primary-dark);
        }

        /* ================= PROJECT ================= */

        .project-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .project-card {
            background: var(--card);
            border-radius: 25px;
            overflow: hidden;
            box-shadow: var(--shadow);
        }

        .project-image {
            height: 180px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 70px;
            background: var(--secondary);
        }

        .project-content {
            padding: 25px;
        }

        .project-number {
            color: var(--primary-dark);
            font-weight: bold;
        }

        .project-content h3 {
            margin: 8px 0;
        }

        .project-content p {
            margin-bottom: 20px;
        }

        .demo-button {
            border: none;
            background: var(--primary);
            color: white;
            padding: 10px 16px;
            border-radius: 12px;
            cursor: pointer;
            font-weight: bold;
        }

        .demo-button:hover {
            background: var(--primary-dark);
        }

        /* ================= DEMO ================= */

        .demo-area {
            display: none;
            margin-top: 20px;
            padding: 20px;
            background: var(--secondary);
            border-radius: 18px;
        }

        .demo-area.active {
            display: block;
        }

        .demo-area h4 {
            margin-bottom: 15px;
            color: var(--primary-dark);
        }

        /* ================= TODO LIST ================= */

        .todo-input {
            display: flex;
            gap: 8px;
            margin-bottom: 15px;
        }

        .todo-input input {
            min-width: 0;
            flex: 1;
            padding: 10px;
            border: 2px solid var(--primary);
            border-radius: 10px;
            outline: none;
        }

        .todo-input button,
        .schedule-form button {
            border: none;
            background: var(--primary);
            color: white;
            padding: 10px 14px;
            border-radius: 10px;
            cursor: pointer;
        }

        #todo-list {
            list-style: none;
        }

        #todo-list li {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 8px;
            background: var(--card);
            padding: 10px;
            border-radius: 10px;
            margin-top: 8px;
        }

        #todo-list li span {
            cursor: pointer;
            flex: 1;
        }

        #todo-list li.done span {
            text-decoration: line-through;
            opacity: 0.6;
        }

        .delete-button {
            border: none;
            background: var(--danger);
            color: white;
            padding: 6px 9px;
            border-radius: 8px;
            cursor: pointer;
        }

        /* ================= CALCULATOR ================= */

        .calculator {
            max-width: 280px;
            margin: auto;
        }

        #calc-display {
            width: 100%;
            height: 55px;
            margin-bottom: 10px;
            border: none;
            border-radius: 10px;
            padding: 10px;
            font-size: 22px;
            text-align: right;
            background: var(--card);
            color: var(--text);
        }

        .calc-buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 7px;
        }

        .calc-buttons button {
            border: none;
            padding: 14px 5px;
            border-radius: 10px;
            background: var(--card);
            color: var(--text);
            font-size: 17px;
            cursor: pointer;
        }

        .calc-buttons button:hover {
            background: var(--primary);
            color: white;
        }

        .calc-equal {
            background: var(--primary) !important;
            color: white !important;
        }

        /* ================= JADWAL ================= */

        .schedule-form {
            display: grid;
            gap: 8px;
            margin-bottom: 15px;
        }

        .schedule-form input,
        .schedule-form select {
            padding: 10px;
            border: 2px solid var(--primary);
            border-radius: 10px;
            outline: none;
            background: var(--card);
            color: var(--text);
        }

        .schedule-item {
            background: var(--card);
            padding: 12px;
            border-radius: 10px;
            margin-top: 8px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 10px;
        }

        .schedule-info strong {
            color: var(--primary-dark);
        }

        /* ================= CONTACT ================= */

        .contact-box {
            text-align: center;
        }

        .contact-box p {
            margin: 12px;
        }

        .contact-box a {
            color: var(--primary-dark);
            font-weight: bold;
        }

        /* ================= FOOTER ================= */

        footer {
            text-align: center;
            background: var(--card);
            padding: 25px;
            box-shadow: var(--shadow);
        }

        /* ================= SCROLL TOP ================= */

        #scroll-top {
            position: fixed;
            right: 20px;
            bottom: 20px;
            border: none;
            background: var(--primary);
            color: white;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            cursor: pointer;
            display: none;
            font-size: 20px;
        }

        /* ================= RESPONSIVE ================= */

        @media (max-width: 800px) {
            .project-grid {
                grid-template-columns: 1fr;
            }

            .hero {
                flex-direction: column;
                text-align: center;
            }
        }

        @media (max-width: 600px) {

            .navbar {
                padding: 15px 20px;
            }

            .menu-button {
                display: inline-block;
            }

            .nav-menu {
                display: none;
                position: absolute;
                top: 65px;
                left: 0;
                width: 100%;
                background: var(--card);
                flex-direction: column;
                padding: 20px;
                box-shadow: var(--shadow);
            }

            .nav-menu.active {
                display: flex;
            }

            .hero {
                padding-top: 50px;
            }

            .hero h1 {
                font-size: 36px;
            }

            .hero h2 {
                font-size: 22px;
            }

            .photo-frame {
                width: 250px;
                height: 300px;
            }

            .section-title {
                font-size: 27px;
            }

            .biodata strong {
                width: 110px;
            }

            .todo-input {
                flex-direction: column;
            }

            .schedule-item {
                align-items: flex-start;
                flex-direction: column;
            }
        }
    </style>
</head>

<body>

    <!-- ================= HEADER ================= -->

    <header>
        <nav class="navbar">

            <div class="logo">
                Marcha♡
            </div>

            <ul class="nav-menu" id="nav-menu">
                <li>
                    <a href="#beranda">Beranda</a>
                </li>

                <li>
                    <a href="#tentang">Tentang</a>
                </li>

                <li>
                    <a href="#proyek">Proyek</a>
                </li>

                <li>
                    <a href="#kontak">Kontak</a>
                </li>
            </ul>

            <div>
                <button
                    class="theme-button"
                    id="theme-button">
                    🌙
                </button>

                <button
                    class="menu-button"
                    id="menu-button">
                    ☰
                </button>
            </div>

        </nav>
    </header>


    <!-- ================= BERANDA ================= -->

    <section class="hero" id="beranda">

        <div class="hero-text">

            <p class="small-title">
                ✨ Halo, semuanya!
            </p>

            <h1>
                Marcha Nabila
            </h1>

            <h2>
                Welcome to my portfolio ♡
            </h2>

            <p>
                Saya adalah siswi kelas X RPL 3 yang tertarik
                dengan dunia pemrograman, desain UI/UX,
                dan pembuatan website.
            </p>

            <a
                href="#proyek"
                class="main-button">
                Lihat Proyek
            </a>

        </div>


        <div class="hero-photo">

            <div class="photo-frame">

                <img
                    src="https://uploads.onecompiler.io/45447qjvv/1790334519966/WhatsApp%20Image%202026-09-25%20at%2003.59.33.jpeg"
                    alt="Foto Marcha Nabila">

            </div>

        </div>

    </section>


    <!-- ================= TENTANG ================= -->

    <section id="tentang">

        <h2 class="section-title">
            Tentang Saya ♡
        </h2>


        <div class="about-card">

            <h3>
                Hai, aku Marcha! 🌷
            </h3>

            <p>
                Saya adalah siswi SMK Krian 1 Sidoarjo
                jurusan Rekayasa Perangkat Lunak.
                Saya senang mempelajari coding,
                membuat website, dan mencoba desain
                yang menarik serta mudah digunakan.
            </p>

        </div>


        <!-- BIODATA -->

        <div class="biodata">

            <h3>
                Biodata
            </h3>

            <p>
                <strong>Nama</strong> :
                Marcha Nabila Alfatuz Zahra
            </p>

            <p>
                <strong>Kelas</strong> :
                X RPL 3
            </p>

            <p>
                <strong>Absen</strong> :
                41
            </p>

        </div>


        <!-- PENDIDIKAN -->

        <div class="education">

            <h3>
                Pendidikan 🎓
            </h3>

            <div class="education-item">
                <strong>SD</strong>
                <p>SDN Kepunten</p>
            </div>

            <div class="education-item">
                <strong>SMP</strong>
                <p>MTs 4 Sidoarjo</p>
            </div>

            <div class="education-item">
                <strong>SMK</strong>
                <p>SMK Krian 1 Sidoarjo</p>
            </div>

        </div>

    </section>


    <!-- ================= PROYEK ================= -->

    <section id="proyek">

        <h2 class="section-title">
            My Projects 💻
        </h2>

        <div class="project-grid">


            <!-- PROJECT 1 -->

            <article class="project-card">

                <div class="project-image">
                    🌸
                </div>

                <div class="project-content">

                    <span class="project-number">
                        01
                    </span>

                    <h3>
                        Website To-Do List
                    </h3>

                    <p>
                        Aplikasi sederhana untuk mencatat
                        tugas dan kegiatan.
                    </p>

                    <button
                        class="demo-button"
                        onclick="openDemo('todo-demo')">
                        Gunakan Proyek →
                    </button>


                    <div
                        class="demo-area"
                        id="todo-demo">

                        <h4>
                            🌸 To-Do List
                        </h4>

                        <div class="todo-input">

                            <input
                                type="text"
                                id="todo-input"
                                placeholder="Tulis tugas...">

                            <button onclick="addTodo()">
                                Tambah
                            </button>

                        </div>

                        <ul id="todo-list"></ul>

                    </div>

                </div>

            </article>


            <!-- PROJECT 2 -->

            <article class="project-card">

                <div class="project-image">
                    🎨
                </div>

                <div class="project-content">

                    <span class="project-number">
                        02
                    </span>

                    <h3>
                        Mini Calculator
                    </h3>

                    <p>
                        Kalkulator sederhana yang dapat
                        melakukan operasi matematika.
                    </p>

                    <button
                        class="demo-button"
                        onclick="openDemo('calculator-demo')">
                        Gunakan Proyek →
                    </button>


                    <div
                        class="demo-area"
                        id="calculator-demo">

                        <h4>
                            🎨 Mini Calculator
                        </h4>

                        <div class="calculator">

                            <input
                                type="text"
                                id="calc-display"
                                readonly>


                            <div class="calc-buttons">

                                <button
                                    onclick="clearCalc()">
                                    C
                                </button>

                                <button
                                    onclick="deleteCalc()">
                                    ⌫
                                </button>

                                <button
                                    onclick="appendCalc('%')">
                                    %
                                </button>

                                <button
                                    onclick="appendCalc('/')">
                                    ÷
                                </button>


                                <button
                                    onclick="appendCalc('7')">
                                    7
                                </button>

                                <button
                                    onclick="appendCalc('8')">
                                    8
                                </button>

                                <button
                                    onclick="appendCalc('9')">
                                    9
                                </button>

                                <button
                                    onclick="appendCalc('*')">
                                    ×
                                </button>


                                <button
                                    onclick="appendCalc('4')">
                                    4
                                </button>

                                <button
                                    onclick="appendCalc('5')">
                                    5
                                </button>

                                <button
                                    onclick="appendCalc('6')">
                                    6
                                </button>

                                <button
                                    onclick="appendCalc('-')">
                                    −
                                </button>


                                <button
                                    onclick="appendCalc('1')">
                                    1
                                </button>

                                <button
                                    onclick="appendCalc('2')">
                                    2
                                </button>

                                <button
                                    onclick="appendCalc('3')">
                                    3
                                </button>

                                <button
                                    onclick="appendCalc('+')">
                                    +
                                </button>


                                <button
                                    onclick="appendCalc('0')">
                                    0
                                </button>

                                <button
                                    onclick="appendCalc('.')">
                                    .
                                </button>

                                <button
                                    class="calc-equal"
                                    onclick="calculate()">
                                    =
                                </button>

                            </div>

                        </div>

                    </div>

                </div>

            </article>


            <!-- PROJECT 3 -->

            <article class="project-card">

                <div class="project-image">
                    📚
                </div>

                <div class="project-content">

                    <span class="project-number">
                        03
                    </span>

                    <h3>
                        Aplikasi Jadwal Pelajaran
                    </h3>

                    <p>
                        Aplikasi untuk mencatat jadwal
                        pelajaran sekolah.
                    </p>

                    <button
                        class="demo-button"
                        onclick="openDemo('schedule-demo')">
                        Gunakan Proyek →
                    </button>


                    <div
                        class="demo-area"
                        id="schedule-demo">

                        <h4>
                            📚 Jadwal Pelajaran
                        </h4>

                        <div class="schedule-form">

                            <select id="schedule-day">

                                <option value="Senin">
                                    Senin
                                </option>

                                <option value="Selasa">
                                    Selasa
                                </option>

                                <option value="Rabu">
                                    Rabu
                                </option>

                                <option value="Kamis">
                                    Kamis
                                </option>

                                <option value="Jumat">
                                    Jumat
                                </option>

                            </select>


                            <input
                                type="text"
                                id="schedule-subject"
                                placeholder="Nama pelajaran">


                            <input
                                type="text"
                                id="schedule-time"
                                placeholder="Jam, contoh: 07.00 - 08.30">


                            <button onclick="addSchedule()">
                                Tambah Jadwal
                            </button>

                        </div>

                        <div id="schedule-list"></div>

                    </div>

                </div>

            </article>

        </div>

    </section>


    <!-- ================= KONTAK ================= -->

    <section id="kontak">

        <h2 class="section-title">
            Kontak Saya 💌
        </h2>

        <div class="contact-box">

            <p>
                📧 Email:
                <a
                    href="mailto:nabilamarcha008@gmail.com">
                    nabilamarcha008@gmail.com
                </a>
            </p>

            <p>
                📷 Instagram:
                <a
                    href="https://instagram.com/mrcha.aja"
                    target="_blank">
                    @mrcha.aja
                </a>
            </p>

        </div>

    </section>


    <!-- ================= FOOTER ================= -->

    <footer>

        <p>
            © 2026 Marcha Nabila Alfatuz Zahra
        </p>

        <p>
            Made with ♡ using HTML, CSS & JavaScript
        </p>

    </footer>


    <!-- TOMBOL KE ATAS -->

    <button id="scroll-top">
        ↑
    </button>


    <!-- ================= JAVASCRIPT ================= -->

    <script>

        /* HAMBURGER MENU */

        const menuButton =
            document.getElementById("menu-button");

        const navMenu =
            document.getElementById("nav-menu");


        menuButton.addEventListener(
            "click",
            function () {

                navMenu.classList.toggle("active");

            }
        );


        document
            .querySelectorAll(".nav-menu a")
            .forEach(function (link) {

                link.addEventListener(
                    "click",
                    function () {

                        navMenu.classList.remove("active");

                    }
                );

            });


        /* DARK MODE */

        const themeButton =
            document.getElementById("theme-button");


        themeButton.addEventListener(
            "click",
            function () {

                document.body.classList.toggle("dark");

                if (
                    document.body.classList.contains("dark")
                ) {

                    themeButton.textContent = "☀️";

                } else {

                    themeButton.textContent = "🌙";

                }

            }
        );


        /* BUKA DEMO */

        function openDemo(id) {

            const demo =
                document.getElementById(id);

            demo.classList.toggle("active");

        }


        /* TO-DO LIST */

        function addTodo() {

            const input =
                document.getElementById("todo-input");

            const list =
                document.getElementById("todo-list");

            const text =
                input.value.trim();


            if (text === "") {

                alert(
                    "Tulis tugas terlebih dahulu!"
                );

                return;

            }


            const li =
                document.createElement("li");


            const span =
                document.createElement("span");

            span.textContent = text;


            span.onclick = function () {

                li.classList.toggle("done");

            };


            const deleteButton =
                document.createElement("button");

            deleteButton.textContent = "Hapus";

            deleteButton.className =
                "delete-button";


            deleteButton.onclick = function () {

                li.remove();

            };


            li.appendChild(span);

            li.appendChild(deleteButton);

            list.appendChild(li);


            input.value = "";

        }


        /* ENTER UNTUK TODO */

        document
            .getElementById("todo-input")
            .addEventListener(
                "keydown",
                function (event) {

                    if (event.key === "Enter") {

                        addTodo();

                    }

                }
            );


        /* CALCULATOR */

        const calcDisplay =
            document.getElementById(
                "calc-display"
            );


        function appendCalc(value) {

            calcDisplay.value += value;

        }


        function clearCalc() {

            calcDisplay.value = "";

        }


        function deleteCalc() {

            calcDisplay.value =
                calcDisplay.value.slice(
                    0,
                    -1
                );

        }


        function calculate() {

            try {

                let expression =
                    calcDisplay.value;

                expression =
                    expression.replace(
                        /%/g,
                        "/100"
                    );

                calcDisplay.value =
                    Function(
                        '"use strict"; return (' +
                        expression +
                        ')'
                    )();

            } catch {

                calcDisplay.value =
                    "Error";

            }

        }


        /* JADWAL PELAJARAN */

        function addSchedule() {

            const day =
                document.getElementById(
                    "schedule-day"
                ).value;


            const subject =
                document.getElementById(
                    "schedule-subject"
                ).value.trim();


            const time =
                document.getElementById(
                    "schedule-time"
                ).value.trim();


            const list =
                document.getElementById(
                    "schedule-list"
                );


            if (
                subject === "" ||
                time === ""
            ) {

                alert(
                    "Isi pelajaran dan jam terlebih dahulu!"
                );

                return;

            }


            const item =
                document.createElement("div");

            item.className =
                "schedule-item";


            const info =
                document.createElement("div");

            info.className =
                "schedule-info";


            info.innerHTML =
                "<strong>" +
                day +
                "</strong><br>" +
                subject +
                "<br>" +
                time;


            const deleteButton =
                document.createElement("button");

            deleteButton.textContent =
                "Hapus";

            deleteButton.className =
                "delete-button";


            deleteButton.onclick =
                function () {

                    item.remove();

                };


            item.appendChild(info);

            item.appendChild(deleteButton);

            list.appendChild(item);


            document.getElementById(
                "schedule-subject"
            ).value = "";


            document.getElementById(
                "schedule-time"
            ).value = "";

        }


        /* SCROLL TOP */

        const scrollTop =
            document.getElementById(
                "scroll-top"
            );


        window.addEventListener(
            "scroll",
            function () {

                if (window.scrollY > 300) {

                    scrollTop.style.display =
                        "block";

                } else {

                    scrollTop.style.display =
                        "none";

                }

            }
        );


        scrollTop.addEventListener(
            "click",
            function () {

                window.scrollTo({
                    top: 0,
                    behavior: "smooth"
                });

            }
        );

    </script>

</body>
</html>

