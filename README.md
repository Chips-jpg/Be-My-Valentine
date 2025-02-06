<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Question</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #ffe6f7;
        }
        .container {
            text-align: center;
            background-color: #fff;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #d6336c;
        }
        .question {
            font-size: 24px;
            margin-bottom: 20px;
        }
        .buttons {
            margin-top: 20px;
        }
        button {
            background-color: #d6336c;
            color: white;
            font-size: 18px;
            border: none;
            padding: 10px 20px;
            margin: 0 10px;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        button:hover {
            background-color: #c13554;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Happy Valentine's Day!</h1>
        <p class="question">Will you be my Valentine?</p>
        <div class="buttons">
            <button onclick="alert('Yay! Thank you! 💖')">Yes</button>
            <button onclick="alert('Aww, maybe next time! 💔')">No</button>
        </div>
    </div>
</body>
</html>
