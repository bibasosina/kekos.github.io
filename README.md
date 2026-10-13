<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Пpoгoлoсyйтe за меня, пoжалyйста</title>

    <!-- Мета-теги для превью -->
    <meta property="og:title" content="Пpoгoлoсyйтe за меня, пoжалyйста">
    <meta property="og:description" content="Выберите участника, который достоин получить эксклюзивный набор для жарки мяса">
    <meta property="og:image" content="https://avatars.mds.yandex.net/get-mpic/6364476/2a0000019686bace4e20330cff709efb1613/optimize">
    <meta property="og:url" content="#">
    <meta property="og:type" content="website">

    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800&display=swap">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #FF6B35;
            --secondary-color: #E63946;
            --accent-color: #FFB703;
            --bg-color: #FFF8F0;
            --card-bg: #FFFFFF;
            --text-color: #2B2D42;
            --text-secondary: #6C757D;
            --border-color: #F0E6DA;
            --gradient: linear-gradient(135deg, #FF6B35, #E63946);
            --shadow: 0 10px 30px rgba(230, 57, 70, 0.12);
            --shadow-hover: 0 20px 40px rgba(230, 57, 70, 0.22);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 2rem;
            background-image:
                radial-gradient(circle at 10% 10%, rgba(255, 107, 53, 0.10) 0%, transparent 30%),
                radial-gradient(circle at 90% 20%, rgba(255, 183, 3, 0.12) 0%, transparent 30%),
                radial-gradient(circle at 50% 90%, rgba(230, 57, 70, 0.08) 0%, transparent 35%);
        }

        .container {
            max-width: 1100px;
            width: 100%;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 2.5rem;
        }

        .logo {
            font-size: 1.4rem;
            font-weight: 800;
            margin-bottom: 1.2rem;
            color: var(--primary-color);
            display: inline-flex;
            align-items: center;
            gap: 0.6rem;
            letter-spacing: 2px;
        }

        h1 {
            font-size: 2.8rem;
            margin-bottom: 1rem;
            background: var(--gradient);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 800;
            line-height: 1.2;
        }

        .subtitle {
            color: var(--text-secondary);
            font-size: 1.15rem;
            max-width: 650px;
            margin: 0 auto;
            line-height: 1.6;
        }

        .timer-wrapper {
            background: var(--card-bg);
            border-radius: 20px;
            padding: 1.5rem 2rem;
            margin: 2rem auto 3rem;
            max-width: 600px;
            border: 1px solid var(--border-color);
            text-align: center;
            box-shadow: var(--shadow);
        }
        .timer-wrapper .label {
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: var(--text-secondary);
            margin-bottom: 0.8rem;
            font-weight: 600;
        }
        .timer-wrapper .time-blocks {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            font-weight: 700;
        }
        .timer-wrapper .time-block {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .timer-wrapper .time-block .number {
            font-size: 2.6rem;
            line-height: 1;
            background: var(--gradient);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 800;
            min-width: 3.2rem;
        }
        .timer-wrapper .time-block .unit {
            font-size: 0.7rem;
            color: var(--text-secondary);
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-top: 0.3rem;
        }
        .timer-wrapper .separator {
            font-size: 2rem;
            color: var(--primary-color);
            align-self: center;
            font-weight: 400;
        }
        @media (max-width: 480px) {
            .timer-wrapper .time-blocks { gap: 0.6rem; }
            .timer-wrapper .time-block .number { font-size: 2rem; min-width: 2.2rem; }
            .timer-wrapper .separator { font-size: 1.6rem; }
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2.5rem;
            margin-bottom: 4rem;
            max-width: 850px;
            margin-left: auto;
            margin-right: auto;
        }

        .photo-card {
            background-color: var(--card-bg);
            border-radius: 22px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: all 0.4s ease;
            border: 1px solid var(--border-color);
            display: flex;
            flex-direction: column;
        }

        .photo-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-hover);
        }

        .photo-image {
            width: 100%;
            height: 320px;
            overflow: hidden;
            position: relative;
            background: linear-gradient(135deg, #FFE8D6, #FFD6BA);
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .photo-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.7s ease;
        }

        .photo-card:hover .photo-image img {
            transform: scale(1.08);
        }

        .photo-info {
            padding: 1.8rem 1.6rem 2rem;
            flex: 1;
            display: flex;
            flex-direction: column;
            text-align: center;
        }

        .photo-info h3 {
            color: var(--text-color);
            margin-bottom: 0.4rem;
            font-size: 1.4rem;
            font-weight: 700;
        }

        .photo-info .participant-label {
            color: var(--primary-color);
            font-size: 0.85rem;
            font-weight: 600;
            margin-bottom: 1.5rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .select-btn {
            background: var(--gradient);
            color: #fff;
            border: none;
            padding: 1rem 1.5rem;
            font-size: 0.95rem;
            font-weight: 700;
            border-radius: 14px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 8px 20px rgba(230, 57, 70, 0.3);
            text-transform: uppercase;
            letter-spacing: 1px;
            width: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            text-decoration: none;
        }

        .select-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 25px rgba(230, 57, 70, 0.45);
        }

        .select-btn:active {
            transform: translateY(1px);
        }

        .prize-section {
            background-color: var(--card-bg);
            padding: 3rem;
            border-radius: 22px;
            margin: 2rem auto 4rem;
            max-width: 900px;
            width: 100%;
            box-shadow: var(--shadow);
            text-align: center;
            border: 1px solid var(--border-color);
            position: relative;
            overflow: hidden;
        }

        .prize-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--gradient);
        }

        .prize-section h2 {
            color: var(--secondary-color);
            margin-bottom: 1.5rem;
            font-size: 2.1rem;
            font-weight: 800;
        }

        .prize-container {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: center;
            gap: 3rem;
            margin-top: 1.5rem;
        }

        .prize-image {
            width: 300px;
            height: 220px;
            border-radius: 16px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease;
            background: #FFF8F0;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 1px solid var(--border-color);
        }

        .prize-image:hover {
            transform: scale(1.04);
        }

        .prize-image img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }

        .prize-description {
            text-align: left;
            max-width: 450px;
        }

        .prize-description h3 {
            color: var(--primary-color);
            font-size: 1.5rem;
            margin-bottom: 1rem;
            font-weight: 700;
        }

        .prize-description p {
            color: var(--text-secondary);
            line-height: 1.7;
            margin-bottom: 0.8rem;
        }

        .highlight {
            color: var(--secondary-color);
            font-weight: 700;
        }

        .features {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            margin: 1.2rem 0;
        }

        .feature {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            background: rgba(255, 107, 53, 0.10);
            color: var(--text-color);
            padding: 0.45rem 1rem;
            border-radius: 50px;
            font-size: 0.85rem;
            font-weight: 500;
            border: 1px solid rgba(255, 107, 53, 0.2);
        }

        .feature i {
            color: var(--primary-color);
        }

        footer {
            margin-top: 4rem;
            text-align: center;
            color: var(--text-secondary);
            font-size: 0.9rem;
            padding-top: 2rem;
            border-top: 1px solid var(--border-color);
            width: 100%;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 1rem;
        }

        .social-links a {
            color: var(--text-secondary);
            font-size: 1.3rem;
            transition: color 0.3s ease;
        }

        .social-links a:hover {
            color: var(--primary-color);
        }

        @media (max-width: 768px) {
            body { padding: 1rem; }
            h1 { font-size: 2rem; }
            .gallery { grid-template-columns: 1fr; gap: 1.8rem; }
            .photo-image { height: 280px; }
            .prize-container { flex-direction: column; gap: 2rem; }
            .prize-description { text-align: center; }
            .prize-section { padding: 1.8rem; }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="logo">
                <i class="fas fa-fire"></i>
                <span>ГОЛОСОВАНИЕ</span>
            </div>
            <h1>Выбери своего фаворита</h1>
            <p class="subtitle">Поддержите своего участника — победитель получит эксклюзивный набор для приготовления мяса</p>
        </header>

        <!-- ⏳ Таймер обратного отсчёта до 27 октября 2026 -->
        <div class="timer-wrapper">
            <div class="label">🔥 Голосование завершится через</div>
            <div class="time-blocks" id="countdown">
                <div class="time-block">
                    <span class="number" id="days">00</span>
                    <span class="unit">дней</span>
                </div>
                <span class="separator">:</span>
                <div class="time-block">
                    <span class="number" id="hours">00</span>
                    <span class="unit">часов</span>
                </div>
                <span class="separator">:</span>
                <div class="time-block">
                    <span class="number" id="minutes">00</span>
                    <span class="unit">минут</span>
                </div>
                <span class="separator">:</span>
                <div class="time-block">
                    <span class="number" id="seconds">00</span>
                    <span class="unit">секунд</span>
                </div>
            </div>
        </div>

        <!-- ============================================================
             УЧАСТНИКИ (2 человека)
             ↓↓↓ ЗДЕСЬ МЕНЯЙТЕ ФОТО, ИМЯ И ССЫЛКУ КНОПКИ ↓↓↓
        ============================================================ -->
        <div class="gallery">

            <!-- ========== УЧАСТНИК №1 ========== -->
            <div class="photo-card">
                <div class="photo-image">
                    <!-- 👇 ЗАМЕНИТЕ ССЫЛКУ НА ФОТО УЧАСТНИКА №1 -->
                    <img src="https://sun9-65.vkuserphoto.ru/s/v1/ig2/byuKMwYaP0p8LPzpKxgPLyi2AloHgH9VmH9YJIwY0pikgaovFraonoMSPQNzLDAZOWaD2HpzlRPDGvxIv904Rta0.jpg?quality=95&crop=576,272,1536,1536&as=32x32,48x48,72x72,108x108,160x160,240x240,360x360,480x480,540x540,640x640,720x720,1080x1080,1280x1280,1440x1440&ava=1&u=8J4GLFNWVAcPbq7Pk99ygBvSLilY3pkRtDIaAM7PgmQ&cs=200x200"
                         alt="Участник №1"
                         onerror="this.src='https://via.placeholder.com/400x400/FFE8D6/FF6B35?text=Фото'">
                </div>
                <div class="photo-info">
                    <!-- 👇 ЗАМЕНИТЕ ИМЯ УЧАСТНИКА №1 -->
                    <h3>Елизавета Плеханова</h3>
                    <div class="participant-label"><i class="fas fa-user-circle"></i> Участник №1</div>
                    <!-- 👇 ЗАМЕНИТЕ ССЫЛКУ КНОПКИ УЧАСТНИКА №1 -->
                    <a href="https://askrodan.com/k6321dknf9vajg6svpi2" target="_blank" class="select-btn">
                        <i class="fas fa-check-circle"></i> Проголосовать
                    </a>
                </div>
            </div>

            <!-- ========== УЧАСТНИК №2 ========== -->
            <div class="photo-card">
                <div class="photo-image">
                    <!-- 👇 ЗАМЕНИТЕ ССЫЛКУ НА ФОТО УЧАСТНИКА №2 -->
                    <img src="https://sun9-57.userapi.com/s/v1/ig2/756XJ8jSdxNHMooalYDMPGJ0Ub8XzCYdC-E_6bjRc_EDlyZXWyzVYy4jk8p4wKPGwd8Hg1fDq7CBjMdX0b4jlPQI.jpg?quality=95&as=32x42,48x62,72x94,108x140,160x208,240x312,360x468,480x624,540x702,640x832,720x936,1080x1405,1121x1458&from=bu&cs=1121x0"
                         alt="Участник №2"
                         onerror="this.src='https://via.placeholder.com/400x400/FFE8D6/FF6B35?text=Фото'">
                </div>
                <div class="photo-info">
                    <!-- 👇 ЗАМЕНИТЕ ИМЯ УЧАСТНИКА №2 -->
                    <h3>Алексей Ковальчук</h3>
                    <div class="participant-label"><i class="fas fa-user-circle"></i> Участник №2</div>
                    <!-- 👇 ЗАМЕНИТЕ ССЫЛКУ КНОПКИ УЧАСТНИКА №2 -->
                    <a href="https://askrodan.com/k6321dknf9vajg6svpi2" target="_blank" class="select-btn">
                        <i class="fas fa-check-circle"></i> Проголосовать
                    </a>
                </div>
            </div>

        </div>
        <!-- ============================================================
             КОНЕЦ БЛОКА УЧАСТНИКОВ
        ============================================================ -->

        <!-- Описание приза -->
        <div class="prize-section">
            <h2>🏆 Подарок победителю</h2>
            <div class="prize-container">
                <div class="prize-image">
                    <!-- 👇 ЗАМЕНИТЕ ССЫЛКУ НА ФОТО ПРИЗА -->
                    <img src="https://avatars.mds.yandex.net/get-mpic/6364476/2a0000019686bace4e20330cff709efb1613/optimize"
                         alt="Набор для жарки мяса"
                         onerror="this.src='https://via.placeholder.com/300x220/FFE8D6/FF6B35?text=Приз'">
                </div>
                <div class="prize-description">
                    <h3>🔥 ПРЕМИУМ НАБОР ДЛЯ ЖАРКИ МЯСА</h3>
                    <p>Эксклюзивный подарочный кейс <span class="highlight">«Скиф»</span> с полным комплектом аксессуаров от <span class="highlight">GRILLS FACTORY</span></p>

                    <div class="features">
                        <div class="feature"><i class="fas fa-check"></i> 8 шампуров из нержавейки</div>
                        <div class="feature"><i class="fas fa-check"></i> Подарочный деревянный кейс</div>
                        <div class="feature"><i class="fas fa-check"></i> Длина 50 см</div>
                        <div class="feature"><i class="fas fa-check"></i> Идеальный баланс</div>
                    </div>

                    <p>Помогите выбрать достойного обладателя этого набора — проголосуйте за одного из участников!</p>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <p>&copy; 2026 Голосование. Все права защищены.</p>
        <div class="social-links">
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-telegram"></i></a>
            <a href="#"><i class="fab fa-vk"></i></a>
        </div>
    </footer>

    <script>
        // Таймер до 27 октября 2026 23:59:59
        const endDate = new Date('October 27, 2026 23:59:59').getTime();

        function updateTimer() {
            const now = new Date().getTime();
            const distance = endDate - now;

            if (distance < 0) {
                document.getElementById('countdown').innerHTML =
                    '<div style="color: var(--secondary-color); font-size:1.4rem; font-weight:700;">ГОЛОСОВАНИЕ ЗАВЕРШЕНО</div>';
                return;
            }

            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);

            document.getElementById('days').textContent = String(days).padStart(2, '0');
            document.getElementById('hours').textContent = String(hours).padStart(2, '0');
            document.getElementById('minutes').textContent = String(minutes).padStart(2, '0');
            document.getElementById('seconds').textContent = String(seconds).padStart(2, '0');
        }

        updateTimer();
        setInterval(updateTimer, 1000);
    </script>
</body>
</html>
