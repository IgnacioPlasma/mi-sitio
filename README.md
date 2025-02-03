<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>San Valentín</title>
    <style>
        body {
            background: url('/assets/index-zKhTG_2O.css');
            background-size: cover;
            text-align: center;
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .slide {
            display: none;
            background: rgba(255, 240, 245, 0.9);
            padding: 20px;
            border-radius: 10px;
            max-width: 600px;
        }
        .active {
            display: block;
        }
        .buttons {
            margin-top: 20px;
        }
        button {
            padding: 10px 20px;
            margin: 5px;
            border: none;
            cursor: pointer;
            font-size: 16px;
            border-radius: 5px;
        }
        .yes {
            background-color: #ff6699;
            color: white;
        }
        .no {
            background-color: #ffcccb;
            color: black;
        }
        .text-container {
            text-align: justify;
            font-size: 18px;
            line-height: 1.6;
            padding: 20px;
            color: #ff66b2;
            font-weight: bold;
        }
        .sparkle {
            color: #ff66b2;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div id="slide1" class="slide active">
        <div class="text-container">
            <p class="sparkle">✨Hola morocha, soy consciente de que tenemos asuntos pendientes y otras cosas sobre las cuales pensar y ocuparnos en este momento...</p>
            <p class="sparkle">Pero me encantaría pasar un día muy especial con mi personita especial.</p>
            <p class="sparkle">Por lo tanto, me gustaría hacerte la siguiente pregunta:✨</p>
        </div>
        <button onclick="nextSlide()">Siguiente</button>
    </div>
    <div id="slide2" class="slide">
        <h2 class="sparkle">✨¿Querés ser mi San Valentín?💕</h2>
        <div class="buttons">
            <button class="yes" onclick="sayYes()">Sí</button>
            <button class="no" onclick="sayNo()">No</button>
        </div>
    </div>

    <script>
        let noClickCount = 0;

        function nextSlide() {
            document.getElementById('slide1').classList.remove('active');
            document.getElementById('slide2').classList.add('active');
        }

        function sayYes() {
            alert("iiiiiiiiiiiiiiiiiiiiiiiiiiEJEM digo Genial, hasta pronto entonces ❤️✨");
        }

        function sayNo() {
            const responses = ["Mentirosa", "Poquee 🥺", "OHHH"];
            alert(responses[noClickCount % responses.length]);
            noClickCount++;
        }
    </script>
</body>
</html>
