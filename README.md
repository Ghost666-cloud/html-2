<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday, Princess Dsouza</title>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&display=swap">
    <style>
        body {
            text-align: center;
            font-family: 'Dancing Script', cursive;
            color: brown;
            margin: 0;
            padding: 0;
        }
        .slideshow-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
        }
        .slide {
            position: absolute;
            width: 100%;
            height: 100%;
            background-size: cover;
            background-position: center;
            opacity: 0;
            transition: opacity 2s ease-in-out;
        }
        .active {
            opacity: 1;
        }
        .container {
            position: relative;
            margin-top: 100px;
            z-index: 10;
        }
        h1 {
            font-size: 4em;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        p {
            font-size: 2em;
            margin: 20px;
        }
        button {
            background-color: #ff69b4;
            border: none;
            padding: 15px 30px;
            font-size: 1.5em;
            cursor: pointer;
            border-radius: 10px;
            color: brown;
            font-family: 'Dancing Script', cursive;
        }
        button:hover {
            background-color: #ff1493;
        }
        .hidden {
            display: none;
            margin-top: 20px;
            font-size: 1.8em;
        }
        .music {
            position: absolute;
            bottom: 10px;
            left: 10px;
        }
    </style>
</head>
<body>
    <div class="slideshow-container">
        <div class="slide active" style="background-image: url('uploaded-image-1.jpg');"></div>
        <div class="slide" style="background-image: url('uploaded-image-2.jpg');"></div>
        <div class="slide" style="background-image: url('uploaded-image-3.jpg');"></div>
        <div class="slide" style="background-image: url('uploaded-image-4.jpg');"></div>
    </div>
    <div class="container">
        <h1>Happy Birthday, My Love ❤️</h1>
        <p>Princess Dsouza, today is your special day! You are the most precious gift in my life.</p>
        <p><strong>My Dearest Princess,</strong> 👑💖</p>
        <p>On this special day, I just want to remind you how incredibly precious you are to me. Every moment with you feels like a beautiful fairytale, and I’m so grateful to have you in my life. ✨</p>
        <p>May your birthday be filled with love, laughter, and all the happiness your heart desires. You deserve nothing but the best, my love! 💕</p>
        <p>Happiest birthday, my beautiful princess! 🎂🎉 I love you more than words can ever express. 💖😘</p>
        <p><strong>Forever yours,</strong><br>[Your Name]</p>
        <button onclick="showSurprise()">Click for a Surprise 🎁</button>
        <div id="surpriseMessage" class="hidden">
            <p>"My love for you grows every day. You are my heart, my soul, my everything. Happy Birthday, my love! 💖"</p>
        </div>
    </div>
    <audio class="music" autoplay loop>
        <source src="https://www.bensound.com/bensound-music/bensound-love.mp3" type="audio/mp3">
        Your browser does not support the audio element.
    </audio>
    <script>
        function showSurprise() {
            document.getElementById("surpriseMessage").style.display = "block";
        }
        
        let slides = document.querySelectorAll(".slide");
        let currentIndex = 0;
        function showSlides() {
            slides.forEach((slide, index) => {
                slide.classList.remove("active");
                if (index === currentIndex) {
                    slide.classList.add("active");
                }
            });
            currentIndex = (currentIndex + 1) % slides.length;
        }
        setInterval(showSlides, 3000);
    </script>
</body>
</html>
