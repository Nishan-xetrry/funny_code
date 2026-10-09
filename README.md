<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Question For You ❤️</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 99%, #fecfef 100%);
            height: 100vh;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        .container {
            text-align: center;
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            position: relative;
            width: 350px;
        }

        h1 {
            color: #ff4757;
            margin-bottom: 30px;
            font-size: 24px;
        }

        .btn-group {
            display: flex;
            justify-content: center;
            gap: 20px;
            position: relative;
            height: 50px;
        }

        button {
            padding: 12px 30px;
            font-size: 16px;
            font-weight: bold;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: 0.2s;
        }

        #yesBtn {
            background-color: #2ed573;
            color: white;
        }

        #yesBtn:hover {
            background-color: #26af5f;
            transform: scale(1.05);
        }

        #noBtn {
            background-color: #ff4757;
            color: white;
            position: absolute;
        }

        .hidden {
            display: none;
        }

        #message {
            margin-top: 20px;
            font-size: 20px;
            color: #2ed573;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1 id="question">Do you love me? ❤️</h1>
        <div class="btn-group" id="buttonGroup">
            <button id="yesBtn" onclick="sayYes()">Yes</button>
            <button id="noBtn" onmouseover="moveButton()" onclick="moveButton()">No</button>
        </div>
        <div id="message" class="hidden">Thank you so much! I know that you love me! 🥰</div>
    </div>

    <script>
        function moveButton() {
            const noBtn = document.getElementById('noBtn');
            const x = Math.random() * 200 - 100; // Random horizontal movement
            const y = Math.random() * 200 - 100; // Random vertical movement
            noBtn.style.transform = `translate(${x}px, ${y}px)`;
        }

        function sayYes() {
            document.getElementById('question').style.display = 'none';
            document.getElementById('buttonGroup').style.display = 'none';
            document.getElementById('message').classList.remove('hidden');
        }
    </script>

</body>
</html>
