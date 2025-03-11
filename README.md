# navi-hbd1



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday My Love ❤️</title>
    <style>
        body {
            background-color: #ffccff; /* Light pink background */
            text-align: center;
            color: white;
            font-family: 'Arial', sans-serif;
            overflow: hidden;
        }
        .hidden {
            display: none;
        }
        .start-screen {
            width: 100%;
            height: 100vh;
            background-color: black;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            color: white;
        }
        .blast {
            width: 100%;
            height: 100vh;
            background: radial-gradient(circle, red, orange, yellow);
            display: none;
            animation: blastEffect 1s forwards;
        }
        @keyframes blastEffect {
            from { transform: scale(0); opacity: 0; }
            to { transform: scale(1); opacity: 1; }
        }
        h1 {
            font-size: 50px;
            margin-top: 5%;
            animation: glow 1.5s infinite alternate;
            color: #ff4081;
        }
        @keyframes glow {
            from { text-shadow: 0 0 10px #ff00ff, 0 0 20px #ff00ff; }
            to { text-shadow: 0 0 20px #ff00ff, 0 0 40px #ff00ff; }
        }
        p {
            font-size: 20px;
            color: black;
        }
        .button-container {
            margin-top: 20px;
        }
        button {
            display: block;
            margin: 10px auto;
            padding: 15px 30px;
            font-size: 18px;
            border: none;
            color: white;
            cursor: pointer;
            border-radius: 10px;
            transition: 0.3s;
            width: 200px;
        }
        .blue { background-color: blue; }
        .yellow { background-color: yellow; color: black; }
        .hug { background-color: purple; }
        .kiss { background-color: red; }
        .warning { background-color: orange; }
        .beating { background-color: brown; }
        .matter { background-color: green; }

        button:hover {
            opacity: 0.8;
        }
        img {
            width: 300px;
            height: 200px;
            margin-top: 10px;
            border-radius: 10px;
            display: none;
        }
        .image-container {
            margin-top: 20px;
        }
    </style>
</head>
<body>

    <!-- Start Screen -->
    <div class="start-screen" id="startScreen">
        <h1>Click to Enter 🎉</h1>
        <button onclick="startBirthday()">Enter</button>
    </div>

    <!-- Blast Effect -->
    <div class="blast" id="blastEffect"></div>

    <!-- Main Content -->
    <div id="mainContent" class="hidden">
        <h1>🎉 Happy Birthday, My Love! 🎂❤️</h1>
        <p>Wishing you a day filled with love, joy, and laughter. You are the most special person in my life, and I am so lucky to have you! 💖</p>

        <div class="button-container">
            <button class="blue" onclick="showImage('blueImg')">Blue and Blue</button>
            <button class="yellow" onclick="showImage('yellowImg')">Yellow and Yellow</button>
            <button class="hug" onclick="showImage('hugImg')">Hug</button>
            <button class="kiss" onclick="showImage('kissImg')">Kiss</button>
            <button class="warning" onclick="showImage('warningImg')">Warning</button>
            <button class="beating" onclick="showImage('beatingImg')">Beating</button>
            <button class="matter" onclick="showMessage()">Matter about Love</button>
        </div>

        <div class="image-container">
            <img id="blueImg" src="C:\Users\chand\OneDrive\Pictures\personal\blue and blue.jpg" alt="Blue and Blue">
            <img id="yellowImg" src="C:\Users\chand\OneDrive\Pictures\personal\side.jpg" alt="Yellow and Yellow">
            <img id="hugImg" src="C:\Users\chand\OneDrive\Pictures\personal\hug.jpg" alt="Hug">
            <img id="kissImg" src="C:\Users\chand\OneDrive\Pictures\personal\kiss.jpg" alt="Kiss">
            <img id="warningImg" src="C:\Users\chand\OneDrive\Pictures\personal\warning.jpg" alt="Warning">
            <img id="beatingImg" src="C:\Users\chand\OneDrive\Pictures\personal\beating.jpg" alt="Beating">
            <p id="loveMessage" style="display: none;">
                💖 **Love is divine and eternal.** In Hindu mythology, Radha-Krishna represent **selfless and spiritual love**.  
                Shiva and Parvati show **devotion, balance, and companionship**.  
                True love is about **trust, respect, and unwavering support**. Like these divine couples, may our love always remain strong and beautiful. 💑✨  
            </p>
        </div>

        <audio id="backgroundMusic" src="/happy-birthday-254480.mp3" loop></audio>
    </div>

    <script>
        function startBirthday() {
            document.getElementById("startScreen").style.display = "none";
            document.getElementById("blastEffect").style.display = "block";

            setTimeout(() => {
                document.getElementById("blastEffect").style.display = "none";
                document.getElementById("mainContent").classList.remove("hidden");
                playBackgroundMusic();
            }, 1000);
        }

        function playBackgroundMusic() {
            let music = document.getElementById("backgroundMusic");
            music.play();
        }

        function showImage(id) {
            let allImages = document.querySelectorAll(".image-container img");
            allImages.forEach(img => img.style.display = "none");

            document.getElementById('loveMessage').style.display = "none";

            let img = document.getElementById(id);
            img.style.display = "block";
        }

        function showMessage() {
            let allImages = document.querySelectorAll(".image-container img");
            allImages.forEach(img => img.style.display = "none");

            document.getElementById('loveMessage').style.display = "block";
        }
    </script>

</body>
</html>
