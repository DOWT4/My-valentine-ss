<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will you be my Valentine?</title>
    <style>
        body {
            text-align: center;
            background-color: #ffffff;
            font-family: Arial, sans-serif;
        }
        .container {
            margin-top: 50px;
        }
        h1 {
            font-size: 2.5rem;
            color: #d63384;
        }
        .gif-container, #image-response {
            margin-top: 20px;
        }
        .buttons {
            margin-top: 20px;
        }
        button {
            font-size: 1.5rem;
            padding: 12px 25px;
            margin: 10px;
            border: none;
            cursor: pointer;
            border-radius: 20px;
            transition: 0.3s;
            font-weight: bold;
        }
        .yes {
            background-color: #ff4081;
            color: white;
            box-shadow: 0px 4px 10px rgba(255, 64, 129, 0.5);
        }
        .yes:hover {
            background-color: #e60073;
        }
        .no {
            background-color: #dc3545;
            color: white;
            position: absolute;
        }
        #image-response, #response-text {
            display: none;
        }
    </style>
</head>
<body>
    <div class="container" id="question">
        <h1>Will you be my Valentine, Piccolina? ❤️</h1>
        <div class="gif-container">
            <img src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExcW5pdjJjNG1hczMybmk1MTAyMWM3NHJ4ODkxbHJnZG51MXZwbWRkZyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/oH9DJbJJr42lO/giphy.gif" alt="Cute question GIF" width="300">
        </div>
        <div class="buttons">
            <button class="yes" onclick="showResponse()">Yes</button>
            <button class="no" onmouseover="moveButton(this)">No</button>
        </div>
    </div>
    <div id="response" style="display: none;">
        <h1>I knew you would say yes, Piccolina! ❤️</h1>
        <div id="image-response">
            <img src="https://st2.depositphotos.com/1146092/44148/i/450/depositphotos_441484920-stock-photo-valentines-mothers-fathers-day-dachshund.jpg" alt="Happy response image" width="300">
        </div>
    </div>
    <script>
        function moveButton(button) {
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            button.style.left = `${x}px`;
            button.style.top = `${y}px`;
        }
        function showResponse() {
            document.getElementById("question").style.display = "none";
            document.getElementById("response").style.display = "block";
        }
    </script>
</body>
</html>
