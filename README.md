# gercekler
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sanal Suç Gerçektir</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            background-color: #050505;
            color: white;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* Giriş Ekranı (Overlay) */
        #enter-screen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 1);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 999;
            cursor: pointer;
            transition: opacity 1s ease;
        }

        #enter-screen p {
            font-size: 1.2rem;
            letter-spacing: 5px;
            animation: blink 1.5s infinite;
        }

        /* Ana İçerik */
        #main-content {
            text-align: center;
            opacity: 0;
            transform: scale(0.8);
            transition: all 1.5s ease;
        }

        h1 {
            font-size: 5vw; /* Ekran boyutuna göre büyür */
            font-weight: 900;
            text-transform: uppercase;
            letter-spacing: 10px;
            margin: 0;
            background: linear-gradient(to right, #ff0000, #ffffff, #ff0000);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 30px rgba(255, 0, 0, 0.5);
        }

        @keyframes blink {
            0% { opacity: 0; }
            50% { opacity: 1; }
            100% { opacity: 0; }
        }

        /* Arkaplan Video/Efekt (Opsiyonel) */
        .particles {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: radial-gradient(circle, #1a1a1a 0%, #000000 100%);
        }
    </style>
</head>
<body>

    <div id="enter-screen" onclick="startPage()">
        <p>[ GİRİŞ YAP ]</p>
    </div>

    <audio id="bg-music" loop>
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    </audio>

    <div id="main-content">
        <div class="particles"></div>
        <h1>ORTAM SANALSA<br>İŞLENEN SUÇ GERÇEKTİR</h1>
    </div>

    <script>
        function startPage() {
            // Müziği çal
            var audio = document.getElementById("bg-music");
            audio.play();

            // Giriş ekranını kaldır
            var enter = document.getElementById("enter-screen");
            enter.style.opacity = "0";
            setTimeout(() => {
                enter.style.display = "none";
            }, 1000);

            // Ana içeriği göster
            var content = document.getElementById("main-content");
            content.style.opacity = "1";
            content.style.transform = "scale(1)";
        }
    </script>

</body>
</html>


