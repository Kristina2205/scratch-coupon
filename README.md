<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Стираемый купон</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
    <script src="https://cdn.jsdelivr.net/gh/websanova/wScratchPad@master/dist/wScratchPad.min.js"></script>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: #f8f8f8;
        }
        #scratchpad {
            width: 300px;
            height: 150px;
            position: relative;
            margin: 20px auto;
            background: gray; /* Цвет скрытого слоя */
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 24px;
            font-weight: bold;
        }
        #hiddenText {
            display: none; /* Скрытый текст, пока не сотрётся */
        }
    </style>
</head>
<body>
    <h2>Сотри и узнай свою скидку!</h2>
    <div id="scratchpad">
        <span id="hiddenText"></span>
    </div>

    <script>
        // Генерация случайной скидки
        let discounts = [
            "5% скидка", 
            "10% скидка", 
            "15% скидка", 
            "20% скидка", 
            "25% скидка", 
            "10% скидка на чистку лица", 
            "10% скидка на массаж", 
            "10% скидка на маникюр", 
            "10% скидка на педикюр"
        ];
        let randomDiscount = discounts[Math.floor(Math.random() * discounts.length)];

        // Вставляем её в скрытый текст
        document.getElementById("hiddenText").innerText = randomDiscount;

        // Настройка стираемого слоя
        $(document).ready(function() {
            $('#scratchpad').wScratchPad({
                size: 30, // Размер ластика
                bg: '#ffffff', // Что будет под слоем (можно сделать картинку)
                fg: 'gray', // Цвет стираемого слоя
                cursor: 'pointer',
                scratchMove: function() {
                    $("#hiddenText").show(); // Показываем текст при стирании
                }
            });
        });
    </script>
</body>
</html>
