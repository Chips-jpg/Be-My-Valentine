<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #fce4ec;
            color: #333;
            text-align: center;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #ff4081;
            color: white;
            padding: 20px;
            font-size: 2em;
        }
        .question {
            font-size: 1.5em;
            margin: 30px 0;
        }
        .buttons {
            margin: 20px;
        }
        .button {
            padding: 10px 20px;
            font-size: 1.2em;
            color: white;
            background-color: #ff4081;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin: 0 15px;
        }
        .button:hover {
            background-color: #f50057;
        }
        .response {
            font-size: 1.2em;
            margin-top: 20px;
        }
        footer {
            background-color: #ff4081;
            color: white;
            padding: 10px;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>

<header>
    Will You Be My Valentine?
</header>

<div id="app">
    <div id="question1" class="question">
        <p>Do you like me?</p>
        <div class="buttons">
            <button class="button" onclick="nextQuestion(1, 'yes')">Yes</button>
            <button class="button" onclick="nextQuestion(1, 'no')">No</button>
        </div>
    </div>

    <div id="response1" class="response"></div>

    <div id="question2" class="question" style="display: none;">
        <p>Will you be my Valentine?</p>
        <div class="buttons">
            <button class="button" onclick="nextQuestion(2, 'yes')">Yes</button>
            <button class="button" onclick="nextQuestion(2, 'no')">No</button>
        </div>
    </div>

    <div id="response2" class="response"></div>

    <div id="question3" class="question" style="display: none;">
        <p>Do you want to go on a date with me?</p>
        <div class="buttons">
            <button class="button" onclick="nextQuestion(3, 'yes')">Yes</button>
            <button class="button" onclick="nextQuestion(3, 'no')">No</button>
        </div>
    </div>

    <div id="response3" class="response"></div>

    <div id="finalMessage" class="response" style="display: none;">
        <p>Thank you for answering! I hope we can make some wonderful memories together. 💖</p>
    </div>
</div>

<footer>
    <p>Made with ❤️ by [Your Name]</p>
</footer>

<script>
    function nextQuestion(questionNumber, answer) {
        let responseDiv = document.getElementById('response' + questionNumber);
        let questionDiv = document.getElementById('question' + questionNumber);

        // Show the response based on the answer
        if (answer === 'yes') {
            responseDiv.innerHTML = `You answered "Yes" to question ${questionNumber}!`;
        } else {
            responseDiv.innerHTML = `You answered "No" to question ${questionNumber}.`;
        }

        // Hide the current question
        questionDiv.style.display = 'none';

        // Show the next question or the final message
        if (questionNumber < 3) {
            let nextQuestion = document.getElementById('question' + (questionNumber + 1));
            nextQuestion.style.display = 'block';
        } else {
            document.getElementById('finalMessage').style.display = 'block';
        }
    }
</script>

</body>
</html>
