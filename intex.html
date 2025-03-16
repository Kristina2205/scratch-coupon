<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Скретч Купон</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f0f0;
            padding: 20px;
        }
        .coupon {
            background-color: #fff;
            border: 2px solid #ddd;
            width: 80%;
            margin: 20px auto;
            padding: 20px;
            text-align: center;
            font-size: 20px;
            position: relative;
        }
        #scratchpad {
            width: 100%;
            height: 200px;
            background-color: #ff66b2; /* Розовый цвет */
            cursor: pointer;
            position: relative;
            z-index: 10;
        }
        .scratch-result {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 24px;
            color: white;
            z-index: 5;
            visibility: hidden; /* Скрываем до стирания */
        }
    </style>
</head>
<body>
    <h1>Ваш Скретч Купон</h1>
    <div class="coupon">
        <p>Потрите поле, чтобы узнать свою скидку!</p>
        <canvas id="scratchpad"></canvas>
        <div id="result" class="scratch-result">Стерите поле, чтобы узнать свою скидку!</div>
    </div>

    <script>
        const scratchpad = document.getElementById("scratchpad");
        const ctx = scratchpad.getContext("2d");
        scratchpad.width = 300;  // Ширина canvas
        scratchpad.height = 150;  // Высота canvas

        // Создаем розовое поле для стирания
        ctx.fillStyle = "#ff66b2";  // Розовый цвет
        ctx.fillRect(0, 0, scratchpad.width, scratchpad.height);

        let isDrawing = false;
        let discountShown = false; // Флаг, чтобы скидка показывалась только один раз

        // Массив с возможными скидками
        const discounts = [
            "Скидка 5%",
            "Скидка 10%",
            "Скидка 15%",
            "Скидка 20%",
            "Скидка 25%"
        ];

        // Обработчики событий для мобильных устройств и ПК
        scratchpad.addEventListener("mousedown", startScratch);
        scratchpad.addEventListener("mousemove", scratch);
        scratchpad.addEventListener("mouseup", stopScratch);
        scratchpad.addEventListener("touchstart", startScratch);
        scratchpad.addEventListener("touchmove", scratch);
        scratchpad.addEventListener("touchend", stopScratch);

        function startScratch(e) {
            isDrawing = true;
            e.preventDefault();  // Отключаем стандартное поведение (например, выделение текста)
            scratch(e);
        }

        function scratch(e) {
            if (!isDrawing) return;

            // Если это мобильное устройство
            const rect = scratchpad.getBoundingClientRect();
            const x = e.touches ? e.touches[0].clientX - rect.left : e.clientX - rect.left;
            const y = e.touches ? e.touches[0].clientY - rect.top : e.clientY - rect.top;

            // Чистим область
            ctx.clearRect(x - 15, y - 15, 30, 30);

            // Если скидка еще не показана, то показываем
            if (!discountShown) {
                showDiscount();
            }
        }

        function stopScratch() {
            isDrawing = false;
        }

        // Показываем скидку
        function showDiscount() {
            const randomDiscount = discounts[Math.floor(Math.random() * discounts.length)];
            const result = document.getElementById("result");
            result.textContent = randomDiscount;
            result.style.visibility = "visible"; // Показываем скидку
            discountShown = true; // Обновляем флаг, чтобы скидка не менялась
        }
    </script>
</body>
</html>
