<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Selamat Ulang Tahun</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: white;
            font-family: 'Arial', sans-serif;
            text-align: center;
            overflow: hidden;
        }

        .page {
            display: none;
            height: 100vh;
            width: 100%;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }

        .page.active {
            display: flex;
            animation: fadeIn 1s ease-in-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        h1, h2 {
            margin: 0;
        }

        .typewriter {
            display: inline-block;
            border-right: 2px solid black;
            white-space: nowrap;
            overflow: hidden;
            animation: typing 3s steps(30, end), blink 0.5s step-end infinite;
        }

        @keyframes typing {
            from { width: 0; }
            to { width: 100%; }
        }

        @keyframes blink {
            from { border-color: transparent; }
            to { border-color: black; }
        }

        .cake {
            position: relative;
            width: 200px;
            height: 300px;
            background-color: #ffcccb;
            border-radius: 10px;
        }

        .flame {
            position: absolute;
            top: -20px;
            left: 90px;
            width: 20px;
            height: 40px;
            background: radial-gradient(circle, yellow, orange);
            border-radius: 50%;
            animation: flicker 0.5s infinite alternate;
        }

        @keyframes flicker {
            from { transform: scale(1); }
            to { transform: scale(1.2); }
        }

        .next-btn {
            margin-top: 20px;
            padding: 10px 20px;
            background-color: #f06292;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
        }
    </style>
</head>
<body>
    <!-- Page 1 -->
    <div class="page active" id="page1">
        <h1>Halo Kak Tike, Selamat Ulang Tahun yang ke-18</h1>
        <button class="next-btn" onclick="nextPage()">Next</button>
    </div>

    <!-- Page 2 -->
    <div class="page" id="page2">
        <h1 class="typewriter">Aku ada sesuatu untukmu...</h1>
        <button class="next-btn" onclick="nextPage()">Next</button>
    </div>

    <!-- Page 3 -->
    <div class="page" id="page3">
        <div class="cake">
            <div class="flame"></div>
        </div>
        <h2>Happy Birthday, Kak Tike!</h2>
        <audio autoplay loop>
            <source src="https://www.bensound.com/bensound-music/bensound-birthdaysong.mp3" type="audio/mpeg">
        </audio>
    </div>

    <script>
        let currentPage = 0;
        const pages = document.querySelectorAll('.page');

        function nextPage() {
            pages[currentPage].classList.remove('active');
            currentPage++;
            if (currentPage < pages.length) {
                pages[currentPage].classList.add('active');
            }
        }
    </script>
</body>
</html>
