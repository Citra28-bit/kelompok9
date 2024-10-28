tugas game

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }
        body {
            background: #75cde8;
        }
        .content {
            text-align: center;
            margin-top: 20px;
        }
        .content h1 {
            color: #ffffff;
            margin-bottom: 5px;
            font-size: 28px;
        }
        .content p {
            color: white;
            font-size: 16px;
        }
        .container {
            margin-top: 50px;
        }
        .box {
            width: 300px;
            height: 240px;
            margin: auto;
            background: #444654;
            border-radius: 10px;
            padding: 10px;
        }
        .box h1 {
            text-align: center;
            font-size: 26px;
            margin-bottom: 20px;
            color: white;
        }
        .box .atas {
            color: white;
            margin-top: 30px;
        }
        .box input {
            margin-top: 20px;
            color: rgb(239, 231, 231);
            height: 28px;
            background: #010101;
            border: none;
            border-radius: 3px;
            cursor: pointer;
            outline: none;
            width: 100%;
        }
        .box input::placeholder {
            color: white;
            padding-left: 5px;
        }
        .box .kirim {
            background: #10a37f;
            border: none;
            width: 120px;
            height: 30px;
            border-radius: 3px;
            cursor: pointer;
            color: white;
            margin-top: 10px;
        }
        .box .bawah {
            margin-top: 20px;
            width: 170px;
            height: 30px;
            border-radius: 3px;
            border: none;
            background: #151111;
            color: white;
            cursor: pointer;
        }
        .box .isi {
            color: white;
            font-size: 15px;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="content">
        <h1>Game Tebak Angka</h1>
        <p>Seberapa kuat hoki anda!!!</p>
    </div>

    <div class="container">
        <div class="box">
            <h1>Tebak Angka</h1>
            <p class="atas">Tebak angka antara 1 sampai 10 :</p>
            <input type="number" id="guess" placeholder="masukan angka" min="1" max="10">
            <button class="kirim" onclick="checkGuess()">Tebak</button>
            <p class="isi" id="result"></p>
            <button class="bawah" onclick="location.reload()">Main lagi</button>
        </div>
    </div>
    <script>
        function checkGuess() {
            var guess = parseInt(document.getElementById("guess").value);
            var randomNumber = Math.floor(Math.random() * 10) + 1;

            if (guess === randomNumber) {
                document.getElementById("result").innerHTML = "Tebakan anda benar!";
            } else {
                document.getElementById("result").innerHTML = "Tebakan anda salah. Angka yang benar adalah " + randomNumber + ".";
            }
        }
    </script>
</body>
</html>
