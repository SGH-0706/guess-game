Name : Srinithi muthukumar

ref no: 24010166

program: 
```
<!DOCTYPE html>
<html lang="en">
<head>
   
    <title>Number Guessing Game</title>
    
        
</head>
<body>
    <h1>Number Guessing Game</h1>
    <p>Guess a number between 1 and 100!</p>
    <input type="number" id="guessInput" placeholder="Enter your guess" />
    <button onclick="checkGuess()">Guess</button>
    <p id="message"></p>
    <script>
        
        const randomNumber = Math.floor(Math.random() * 100) + 1;
        let attempts = 0;

        function checkGuess() {
            const userGuess = parseInt(document.getElementById('guessInput').value);
            const messageElement = document.getElementById('message');
            attempts++;

            if (isNaN(userGuess) || userGuess < 1 || userGuess > 100) {
                messageElement.textContent = "Please enter a number between 1 and 100.";
            } else if (userGuess === randomNumber) {
                messageElement.textContent = `Congratulations! You guessed the number ${randomNumber} in ${attempts} attempts.`;
                document.getElementById('guessInput').disabled = true;
            } else if (userGuess < randomNumber) {
                messageElement.textContent = "Too low! Try again.";
            } else {
                messageElement.textContent = "Too high! Try again.";
            }
        }
    </script>
</body>
</html>
```

output : 

![Screenshot 2024-11-27 104624](https://github.com/user-attachments/assets/910dae64-93e4-4282-8768-f706fd33186e)

