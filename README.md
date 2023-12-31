<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rock, Paper, Scissors Game</title>
    <style>
        button {
            font-size: 16px;
            margin: 5px;
            padding: 10px;
        }
    </style>
</head>
<body>

    <h1>Rock, Paper, Scissors Game</h1>

    <button onclick="playGame('rock')">Rock</button>
    <button onclick="playGame('paper')">Paper</button>
    <button onclick="playGame('scissors')">Scissors</button>

    <p id="result"></p>

    <script>
        function playGame(playerChoice) {
            var choices = ['rock', 'paper', 'scissors'];
            var computerChoice = choices[Math.floor(Math.random() * choices.length)];

            var result = '';

            if (playerChoice === computerChoice) {
                result = 'It\'s a tie!';
            } else if (
                (playerChoice === 'rock' && computerChoice === 'scissors') ||
                (playerChoice === 'paper' && computerChoice === 'rock') ||
                (playerChoice === 'scissors' && computerChoice === 'paper')
            ) {
                result = 'You win!';
            } else {
                result = 'You lose!';
            }

            document.getElementById('result').innerText = 'Your choice: ' + playerChoice +
                '\nComputer\'s choice: ' + computerChoice +
                '\nResult: ' + result;
        }
    </script>

</body>
</html>

