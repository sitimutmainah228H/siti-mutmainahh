<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ucapan Ulang Tahun</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #ffccff;
            overflow: hidden;
        }
        .container {
            text-align: center;
        }
        h1 {
            font-size: 3rem;
            color: #ff0066;
            animation: fadeIn 3s infinite alternate;
            cursor: pointer;
        }
        p {
            font-size: 1.5rem;
            color: #6600cc;
            animation: bounce 2s infinite;
        }
        @keyframes fadeIn {
            from {
                opacity: 0.5;
            }
            to {
                opacity: 1;
            }
        }
        @keyframes bounce {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-20px);
            }
        }
        .cake {
            margin-top: 20px;
            animation: rotate 5s infinite linear;
            cursor: pointer;
        }
        @keyframes rotate {
            from {
                transform: rotate(0deg);
            }
            to {
                transform: rotate(360deg);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 id="clickText">Selamat Ulang Tahun!</h1>
        <p>Klik kue atau teks untuk pesan spesial 🎉</p>
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/ac/Cupcake_icon.svg/512px-Cupcake_icon.svg.png" alt="Kue Ulang Tahun" class="cake" id="cakeImage" width="150">
        <audio id="birthdaySong" autoplay loop>
            <source src="https://www.bensound.com/bensound-music/bensound-birthdaysong.mp3" type="audio/mpeg">
            Browser Anda tidak mendukung audio HTML5.
        </audio>
    </div>

    <script>
        // Tambahkan event untuk klik pada teks
        document.getElementById("clickText").addEventListener("click", function() {
            alert("Semoga hari ini menjadi awal yang indah untuk masa depan yang cerah!");
        });

        // Tambahkan event untuk klik pada gambar
        document.getElementById("cakeImage").addEventListener("click", function() {
            alert("Selamat menikmati harimu yang spesial! Jangan lupa potong kuenya 🎂");
        });
    </script>
</body>
</html>
