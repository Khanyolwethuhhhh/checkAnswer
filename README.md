// Define the checkAnswer function
function checkAnswer() {
    // Define the correct answer
    var correctAnswer = "4";

    // Retrieve the user's answer
    var userAnswer = document.querySelector('input[name="quiz"]:checked');

    // Check if userAnswer exists and compare it with correctAnswer
    if (userAnswer !== null && userAnswer.value === correctAnswer) {
        // If the user's answer is correct
        document.getElementById("feedback").textContent = "Correct! Well done.";
    } else {
        // If the user's answer is incorrect or no answer selected
        document.getElementById("feedback").textContent = "That's incorrect. Try again!";
    }
}

// Add an event listener to the "Submit Answer" button
document.getElementById("submit-answer").addEventListener("click", checkAnswer);
