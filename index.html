<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mathalino Integer Game</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      padding: 0;
      background-color: #f9f9f9;
    }

    #puzzle-container {
      max-width: 400px;
      text-align: center;
      padding: 20px;
      background-color: #3498db;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      color: #fff;
      border-radius: 10px;
    }

    h1 {
      font-size: 28px;
      margin-bottom: 20px;
    }

    #question {
      margin-bottom: 20px;
      font-size: 24px;
      font-weight: bold;
    }

    #options {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    .option {
      padding: 15px;
      cursor: pointer;
      background-color: #2980b9;
      color: #fff;
      border: none;
      border-radius: 4px;
      font-size: 18px;
      transition: background-color 0.3s ease;
    }

    .option:hover {
      background-color: #1c6ca5;
    }

    #result {
      margin-top: 20px;
      font-weight: bold;
      font-size: 20px;
    }

    #timer {
      margin-top: 10px;
      font-size: 18px;
    }

    #rules-container {
      display: none;
      margin-top: 20px;
      padding: 20px;
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      color: #333;
      text-align: left;
      border-radius: 8px;
    }

    #continue-btn {
      padding: 12px;
      background-color: #3498db;
      color: #fff;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 16px;
      transition: background-color 0.3s ease;
    }

    #continue-btn:hover {
      background-color: #217dbb;
    }

    #statistics {
      margin-top: 20px;
      font-size: 16px;
    }
  </style>
</head>
<body>
  <div id="puzzle-container">
    <h1>Mathalino Integer Game</h1>
    <div id="question"></div>
    <div id="options"></div>
    <div id="result"></div>
    <div id="timer">Time left: 15s</div>
    <div id="rules-container">
      <h2>Explanation</h2>
      <p id="explanation"></p>
      <button id="continue-btn" onclick="continueWithGame()">Continue with the game</button>
    </div>
    <div id="statistics">Correct: 0 | Wrong: 0</div>
  </div>

  <script>
    let correctCount = 0;
    let wrongCount = 0;

    function getRandomInt(min, max) {
      return Math.floor(Math.random() * (max - min + 1)) + min;
    }

    function generateProblem() {
      const operand1 = getRandomInt(1, 10);
      const operand2 = getRandomInt(1, 10);
      const operation = ['+', '-', '*', '/'][getRandomInt(0, 3)];
      const expression = `${operand1} ${operation} ${operand2}`;
      const answer = eval(expression);
      return { expression, answer };
    }

    function shuffleArray(array) {
      for (let i = array.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [array[i], array[j]] = [array[j], array[i]];
      }
    }

    function initializePuzzle() {
      const problem = generateProblem();
      const options = [problem.answer];
      while (options.length < 4) {
        const randomOption = getRandomInt(1, 20);
        if (!options.includes(randomOption)) {
          options.push(randomOption);
        }
      }
      shuffleArray(options);

      document.getElementById('question').innerText = `What is ${problem.expression}?`;

      const optionsContainer = document.getElementById('options');
      optionsContainer.innerHTML = '';
      options.forEach((option, index) => {
        const optionButton = document.createElement('button');
        optionButton.className = 'option';
        optionButton.innerText = option;
        optionButton.onclick = () => checkAnswer(option, problem.answer);
        optionsContainer.appendChild(optionButton);
      });

      document.getElementById('result').innerText = '';
      hideRules();
      startTimer();
    }

    function checkAnswer(selectedOption, correctAnswer) {
      stopTimer();
      const resultContainer = document.getElementById('result');
      const explanationContainer = document.getElementById('explanation');
      const continueBtn = document.getElementById('continue-btn');
      const statisticsContainer = document.getElementById('statistics');

      if (parseFloat(selectedOption) === correctAnswer) {
        resultContainer.innerText = 'Correct!';
        resultContainer.style.color = 'green';
        correctCount++;

        // Update statistics
        statisticsContainer.innerText = `Correct: ${correctCount} | Wrong: ${wrongCount}`;

        // Proceed to the next problem after a correct answer
        setTimeout(() => {
          initializePuzzle();
        }, 1000);
      } else {
        resultContainer.innerText = 'Incorrect.';
        resultContainer.style.color = 'red';
        generateExplanation(selectedOption, correctAnswer, explanationContainer);
        showRules();
        continueBtn.style.display = 'block'; // Show continue button
        wrongCount++;

        // Update statistics
        statisticsContainer.innerText = `Correct: ${correctCount} | Wrong: ${wrongCount}`;
      }
    }

    function hideRules() {
      document.getElementById('rules-container').style.display = 'none';
    }

    function showRules() {
      document.getElementById('rules-container').style.display = 'block';
    }

    function generateExplanation(selectedOption, correctAnswer, explanationContainer) {
      const selectedInt = parseInt(selectedOption, 10);
      const correctInt = parseInt(correctAnswer, 10);
      const operation = document.getElementById('question').innerText.split(" ")[3];

      switch (operation) {
        case '+':
          explanationContainer.innerText = `For addition, when you add two integers with the same sign, add their absolute values and keep the sign.`;
          break;
        case '-':
          explanationContainer.innerText = `For subtraction, when you subtract an integer, add the opposite (addition of its additive inverse).`;
          break;
        case '*':
          explanationContainer.innerText = `For multiplication, the product of two integers with the same sign is positive; with different signs, it's negative.`;
          break;
        case '/':
          explanationContainer.innerText = `For division, the quotient of two integers with the same sign is positive; with different signs, it's negative.`;
          break;
        default:
          explanationContainer.innerText = `Incorrect. Try again!`;
      }
    }

    function continueWithGame() {
      hideRules();
      const continueBtn = document.getElementById('continue-btn');
      continueBtn.style.display = 'none'; // Hide continue button
      initializePuzzle();
    }

    let timer;
    let timeLeft;

    function startTimer() {
      timeLeft = 15; // Set the time limit in seconds
      updateTimer();
      timer = setInterval(() => {
        timeLeft--;
        updateTimer();
        if (timeLeft === 0) {
          stopTimer();
          showTimeoutFeedback();
        }
      }, 1000);
    }

    function stopTimer() {
      clearInterval(timer);
    }

    function updateTimer() {
      document.getElementById('timer').innerText = `Time left: ${timeLeft}s`;
    }

    function showTimeoutFeedback() {
      document.getElementById('result').innerText = 'Time is up! Try again.';
      document.getElementById('result').style.color = 'red';
      const continueBtn = document.getElementById('continue-btn');
      continueBtn.style.display = 'block'; // Show continue button
    }

    // Initialize the puzzle on page load
    window.onload = initializePuzzle;
  </script>
</body>
</html>
