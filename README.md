<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="utf-8">
    <title>Дискотека 90-х - Юбилей</title>
    <style>
        body {
            background: linear-gradient(45deg, #ff00ff, #00ffff);
            font-family: "Comic Sans MS", cursive;
            margin: 0;
            animation: backgroundShift 10s infinite;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .header {
            background: rgba(0,0,0,0.7);
            padding: 30px;
            border-radius: 20px;
            margin-bottom: 40px;
            box-shadow: 0 0 20px neon;
            animation: glow 2s infinite;
        }
        .header h1 {
            font-size: 4em;
            color: #fff;
            text-shadow: 0 0 10px #ff00ff,
                         0 0 20px #ff00ff,
                         0 0 30px #ff00ff;
            margin: 0;
        }
        .photo-frame {
            width: 600px;
            height: 600px;
            border: 20px solid #fff;
            box-shadow: 0 0 50px #ff00ff;
            transform: rotate(-5deg);
            transition: transform 0.3s;
            position: relative;
            display: inline-block;
        }
        .photo-frame:hover {
            transform: rotate(5deg) scale(1.1);
        }
        .photo-frame img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 10px;
        }
        .celebration-info {
            display: inline-block;
            vertical-align: top;
            margin-left: 40px;
            background: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 0 20px #ff00ff;
            width: 400px;
            text-align: center;
        }
        .celebration-info h2 {
            font-size: 2em;
            color: #ff00ff;
            text-shadow: 0 0 10px #ff00ff;
        }
        .celebration-info p {
            font-size: 1.2em;
            line-height: 1.5;
        }
        .location {
            background: #fff;
            padding: 50px;
            margin: 30px 0;
            border-radius: 20px;
            animation: bounce 2s infinite;
            width: 100%;
            max-width: 800px;
            box-shadow: 0 0 30px #ff00ff;
        }
        .location h2 {
            font-size: 2.5em;
            color: #ff00ff;
            text-shadow: 0 0 10px #ff00ff;
            margin-bottom: 20px;
        }
        .map-container {
            width: 100%;
            max-width: 800px;
            aspect-ratio: 16 / 9;
            margin: 40px 0;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 0 20px #ff00ff;
        }
        .map-container iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
        .event-roadmap {
            background: rgba(255, 255, 255, 0.8);
            padding: 40px;
            border-radius: 15px;
            margin-top: 40px;
            text-align: center;
            box-shadow: 0 0 20px #ff00ff;
        }
        .event-roadmap h2 {
            font-size: 2.5em;
            color: #ff00ff;
            text-shadow: 0 0 10px #ff00ff;
            margin-bottom: 30px;
        }
        .event-roadmap ul {
            list-style-type: none;
            padding: 0;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        .event-roadmap li {
            font-size: 1.5em;
            padding: 15px;
            background: rgba(255, 255, 255, 0.5);
            border-radius: 10px;
            box-shadow: 0 0 10px #ff00ff;
            transition: transform 0.3s;
        }
        .event-roadmap li:hover {
            transform: scale(1.05);
        }
        .dress-code {
            background: rgba(255, 255, 255, 0.8);
            padding: 30px;
            border-radius: 15px;
            margin-top: 40px;
            text-align: center;
            width: 100%;
            box-shadow: 0 0 30px #ff00ff;
        }
        .dress-code h2 {
            font-size: 2.5em;
            color: #ff00ff;
            text-shadow: 0 0 10px #ff00ff;
            margin-bottom: 20px;
        }
        .dress-code-images {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin: 20px 0;
        }
        .dress-code-images img {
            width: 100%;
            height: 400px;
            object-fit: cover;
            border-radius: 10px;
            box-shadow: 0 0 20px #ff00ff;
            transition: transform 0.3s;
        }
        .dress-code-images img:hover {
            transform: scale(1.1);
        }
        @keyframes glow {
            0% { box-shadow: 0 0 10px #ff00ff; }
            50% { box-shadow: 0 0 50px #00ffff; }
            100% { box-shadow: 0 0 10px #ff00ff; }
        }
        @keyframes bounce {
            0% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0); }
        }
        @keyframes backgroundShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
				.dress-code ul {
			text-align: left;
			padding: 20px 40px;
			font-size: 1.8em; /* Увеличенный размер шрифта */
			list-style-type: none;
		}

		.dress-code ul li {
			margin: 15px 0;
			padding: 10px;
			background: rgba(255, 255, 255, 0.5);
			border-radius: 8px;
			transition: transform 0.3s;
			box-shadow: 0 0 10px rgba(255, 0, 255, 0.3);
		}

		.dress-code ul li:hover {
			transform: scale(1.05);
			background: rgba(255, 255, 255, 0.7);
		}

		.dress-code p {
			font-size: 2em; /* Увеличенный размер для заголовка "Варианты нарядов" */
			color: #ff00ff;
			text-shadow: 0 0 5px #ff00ff;
			margin: 30px 0;
		}
    </style>
</head>
<body>
    <div class="container">
        <!-- Заголовок -->
        <div class="header">
            <h1>Юбилей в стиле 90-х!</h1>
        </div>

        <!-- Блок с фото именинника и информацией о празднике -->
        <div style="display: flex; justify-content: center; align-items: center;">
            <div class="photo-frame">
                <img src="https://sun9-22.userapi.com/impf/ufefVEx0jF3HlGCemMRYEvD8Qn2-zuRvS5V4wQ/XS2QDzeDcAY.jpg?size=1280x850&quality=96&sign=0551bfd319fe68ce638558cc2e64ee95&type=album" alt="Именинник">
            </div>
            <div class="celebration-info">
                <h2>О празднике</h2>
                <p>🎉 Мы отмечаем юбилей в стиле 90-х!</p>
                <p>🎶 Ретро музыка, танцы и веселье!</p>
                <p>📸 Фотозона с декорациями!</p>
                <p>🎁 Призы за лучший наряд!</p>
				<p>❗❗❗ Обязательно приходим в наряде 90-х</p>
            </div>
        </div>

        <!-- Блок с местом и временем -->
        <div class="location">
            <h2>Где и когда:</h2>
            <p>Адрес: Кафе Девон, Респ. Татарстан, пгт Джалиль</p>
            <p>Дата: 05.04.2025 </p>
            <p>Время: 16:30</p>
        </div>

        <!-- Карта -->
        <div class="map-container">
            <iframe
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2391.780166459723!2d52.7344748!3d55.0267598!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x41603f1c4fffffff%3A0x641ff0d1467eaf29!2z0JrQsNGE0LUg0JTQtdCy0L7QvQ!5e0!3m2!1sru!2sru!4v1696587186825!5m2!1sru!2sru"
                allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade">
            </iframe>
        </div>

        <!-- План мероприятия -->
        <div class="event-roadmap">
            <h2>Что будет на вечеринке:</h2>
            <ul>
                <li>16:30 - 🎉 Сбор гостей</li>
                <li>📸 Фотосессия в ретро-фотозоне</li>
                <li>17:00 - 🔥 Открытие вечеринки</li>
                <li>🎠 Конкурсы и развлечения</li>
                <li>🕺💃🏻 Танцевальная программа</li>
                <li>22:00 - 🌟 Подведение итогов и прощание</li>
            </ul>
        </div>

        <!-- Дресс-код -->
<div class="dress-code">
    <h2>Дресс-код: Стиль 90-х</h2>
    <div class="dress-code-images">
        <img src="https://my-karnaval.ru/files/90-e_godi/1.jpg?1562626159639" alt="Образ 1">
        <img src="https://ecofoto.ru/wp-content/uploads/2024/02/stil-90kh-88.webp" alt="Образ 2">
        <img src="https://alexgrim.ru/wp-content/cache/thumb/ed/6d2b2cf959f1fed_900x600.jpg" alt="Образ 3">
        <img src="https://organizator.ru/wp-content/uploads/2023/05/odezhda-i-pricheski-na-timbilding-v-stile-90h-foto-2-scaled.jpg" alt="Образ 4">
    </div>
    <p>✨ Варианты нарядов:</p>
    <ul>
        <li>🎨 Кислотные цвета</li>
        <li>👖 Джинсовые куртки</li>
        <li>✨ Лосины неоновых цветов</li>
        <li>👖 Широкие джинсы</li>
        <li>👟 Кроссовки спортивные</li>
        <li>🏃‍♂️ Яркие спортивные костюмы</li>
    </ul>
</div>

    </div>
</body>
</html>
