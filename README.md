## Description

The goal was to create a timed quiz that will discount for each incorrect answer and save scrores into local storage. 

## Features

Some of the features I included was a visible bar where the user can see which question they are on at the top left. Other features included the time and score on the top right using CSS for user experience. I also wanted the user to see immediately when clicking the chosen answer if it was correct or incorrect by turning it green or red. 

## Code-Example

Javascript for the countdown clock:

<!-- document.addEventListener('DOMContentLoaded', () => {
    const timeLeftDisplay = document.querySelector('#time-left')
    const startBtn = document.querySelector('#start-button')
    let timeLeft = 10

    function countDown(){
        setInterval(function(){
            if(timeLeft <= 0 ) {
                clearInterval(timeLeft = 0)
            }

            timeLeftDisplay.innerHTML = timeLeft
            timeLeft -=1
        }, 1000)

        startBtn.addEventListener('click', countDown)
    }
 -->

 Javascript for the scoreboard:

 <!-- getNewQuestion = () => {
    if(availableQuestions.length === 0 || questionCounter > MAX_QUESTIONS) {
        localStorage.setItem('mostRecentScore', score)

        return window.location.assign('end.html')
    }

    questionCounter++
    progressText.innerText = `Question ${questionCounter} of ${MAX_QUESTIONS}`
    progressBarFull.style.width = `${(questionCounter/MAX_QUESTIONS) * 100}%`

    const questionsIndex = Math.floor(Math.random() * availableQuestions.length)
    currentQuestion = availableQuestions[questionsIndex]
    question.innerText = currentQuestion.question

    choices.forEach(choice => {
        const number = choice.dataset['number']
        choice.innerText = currentQuestion['choice' + number]
    })

    availableQuestions.splice(questionsIndex, 1)

    acceptingAnswers = true
}

choices.forEach(choice => {
    choice.addEventListener('click', e => {
        if(!acceptingAnswers) return

        acceptingAnswers = false
        const selectedChoice = e.target
        const selectedAnswer = selectedChoice.dataset['number']

        let classToApply = selectedAnswer == currentQuestion.answer ? 'correct' : 'incorrect'

        if(classToApply === 'correct') {
            incrementScore(SCORE_POINTS)
        }

        selectedChoice.parentElement.classList.add(classToApply)

        setTimeout(() => {
            selectedChoice.parentElement.classList.remove(classToApply)
            getNewQuestion()

        }, 1000)
    }) -->

## References

https://www.w3schools.com/
https://stackoverflow.com/questions/44314897/javascript-timer-for-a-quiz
www.youtube.com
