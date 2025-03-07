<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tulipanes Mágicos</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f8ff;
            overflow: hidden;
            position: relative;
        }

        .tulipan {
            width: 50px;
            height: 75px;
            background-color: transparent;
            border-radius: 50% 50% 0 0;
            position: absolute;
            bottom: -75px;
            animation: aparecerDesaparecer 10s infinite;
        }

        .azul {
            background-color: blue;
        }

        .morado {
            background-color: purple;
        }

        @keyframes aparecerDesaparecer {
            0%, 100% {
                opacity: 0;
                transform: translateY(0);
            }
            50% {
                opacity: 1;
                transform: translateY(-200px);
            }
        }
    </style>
</head>
<body>
    <script>
        function crearTulipan(color, delay) {
            const tulipan = document.createElement('div');
            tulipan.classList.add('tulipan', color);
            tulipan.style.left = Math.random() * 100 + 'vw';
            tulipan.style.animationDelay = delay + 's';
            document.body.appendChild(tulipan);
        }

        for (let i = 0; i < 10; i++) {
            crearTulipan('azul', Math.random() * 10);
            crearTulipan('morado', Math.random() * 10);
        }
    </script>
</body>
</html>
