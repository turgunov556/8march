<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>С 8 марта!</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            overflow: hidden;
            background-color: #ffe6f2;
            font-family: 'Arial', sans-serif;
        }

        .hearts, .confetti {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }

        .hearts span {
            position: absolute;
            color: #ff4d6a;
            font-size: 24px; /* Уменьшен размер для мобильных */
            animation: animate 5s linear infinite;
        }

        .confetti span {
            position: absolute;
            color: #ff4d6a;
            font-size: 16px; /* Уменьшен размер для мобильных */
            animation: confetti 2s ease-out forwards;
        }

        @keyframes animate {
            0% {
                transform: translateY(-10%);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(110%);
                opacity: 0;
            }
        }

        @keyframes confetti {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(100vh) rotate(360deg);
                opacity: 0;
            }
        }

        .congrats {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
            background-color: #fff;
            padding: 15px; /* Уменьшен padding для мобильных */
            border: 2px solid #ff4d6a;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            opacity: 0;
            animation: fadeIn 2s forwards 7s; /* Появление через 7 секунд */
            width: 90%; /* Ширина рамки адаптирована под мобильные */
            max-width: 300px; /* Максимальная ширина для удобства чтения */
        }

        @keyframes fadeIn {
            to {
                opacity: 1;
            }
        }

        .congrats h1 {
            color: #ff4d6a;
            font-size: 1.8em; /* Уменьшен размер заголовка */
            margin-bottom: 10px;
        }

        .congrats p {
            color: #333;
            font-size: 1em; /* Уменьшен размер текста */
            white-space: pre-line; /* Сохраняем переносы строк */
        }
    </style>
</head>
<body>
    <div class="hearts">
        <!-- Генерация сердечек -->
        <script>
            for (let i = 0; i < 50; i++) { /* Уменьшено количество сердечек для мобильных */
                const heart = document.createElement('span');
                heart.innerHTML = '&#10084;'; /* HTML-код для сердечка */
                heart.style.left = Math.random() * 100 + 'vw';
                heart.style.animationDuration = Math.random() * 3 + 2 + 's';
                document.querySelector('.hearts').appendChild(heart);
            }
        </script>
    </div>

    <div class="confetti">
        <!-- Генерация конфетти -->
        <script>
            setTimeout(() => {
                for (let i = 0; i < 100; i++) { /* Уменьшено количество конфетти для мобильных */
                    const confettiPiece = document.createElement('span');
                    confettiPiece.innerHTML = '&#127881;'; /* HTML-код для конфетти */
                    confettiPiece.style.left = Math.random() * 100 + 'vw';
                    confettiPiece.style.animationDuration = Math.random() * 1 + 0.5 + 's';
                    document.querySelector('.confetti').appendChild(confettiPiece);
                }
            }, 5000); // Конфетти через 5 секунд
        </script>
    </div>

    <div class="congrats">
        <h1>С Восьмым марта вас, девчонки!</h1>
        <p>
            Будьте счастливы всегда,
            Веселитесь, смейтесь звонко,
            Не грустите никогда.

            Вам желаем приключений,
            Дружбы, радости в глазах,
            Жить без слёз и огорчений,
            Верить в сказку, чудеса!
        </p>
    </div>
</body>
</html>
