<!DOCTYPE html>
<html>
<head>
    <title>Rhythmic Mathematics | Music 2</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 20px; background: #f0f8ff; }
        .section { background: white; padding: 20px; margin: 10px 0; border-radius: 10px; }
        button { padding: 10px; margin: 5px; background: #4CAF50; color: white; border: none; border-radius: 5px; }
        .interactive { background: #e7f3ff; padding: 15px; }
        .term-card { background: #d4edda; padding: 10px; margin: 5px; border-radius: 5px; }
        .quiz-option { background: #e9ecef; padding: 10px; margin: 5px; cursor: pointer; }
        .correct { background: #d4edda; }
        .incorrect { background: #f8d7da; }
    </style>
</head>
<body>
    <div class="section" style="background: #e8f5e8;">
        <h1>👋 From Mrs. Burnie</h1>
        <p><em>"Remember, every great composition has mathematical beauty at its core. Think of rhythm as fractions and form as geometry!"</em></p>
    </div>

    <div class="section">
        <h1>🎵 Rhythmic Mathematics</h1>
        <p>Explore how mathematics creates musical structure and rhythm.</p>
    </div>

    <div class="section">
        <h2>Rhythmic Terminology</h2>
        <div class="term-card">
            <strong>Simple Time:</strong> Beats divided into 2 equal parts (2/4, 3/4, 4/4)
        </div>
        <div class="term-card">
            <strong>Compound Time:</strong> Beats divided into 3 equal parts (6/8, 9/8, 12/8)
        </div>
        <div class="term-card">
            <strong>Triplet:</strong> Three notes played in the time of two
        </div>
        <div class="term-card">
            <strong>Syncopation:</strong> Emphasis on weak beats or off-beats
        </div>
        <div class="term-card">
            <strong>ABA Form:</strong> Three-part structure (Statement-Contrast-Restatement)
        </div>
    </div>

    <div class="section interactive">
        <h2>Rhythm Quiz</h2>
        <div id="quiz-container">
            <p><strong>Question 1:</strong> How many quavers in a 4/4 bar?</p>
            <div class="quiz-option" onclick="checkAnswer(this, 8)">8</div>
            <div class="quiz-option" onclick="checkAnswer(this, 4)">4</div>
            <div class="quiz-option" onclick="checkAnswer(this, 16)">16</div>

            <p><strong>Question 2:</strong> What is the ratio of an ABA form with 16-bar sections?</p>
            <div class="quiz-option" onclick="checkAnswer(this, '1:1:1')">1:1:1</div>
            <div class="quiz-option" onclick="checkAnswer(this, '2:1:2')">2:1:2</div>
            <div class="quiz-option" onclick="checkAnswer(this, '16:16:16')">16:16:16</div>

            <p><strong>Question 3:</strong> A triplet quaver equals how many normal quavers?</p>
            <div class="quiz-option" onclick="checkAnswer(this, '0.666')">0.666 (2/3)</div>
            <div class="quiz-option" onclick="checkAnswer(this, '1.5')">1.5</div>
            <div class="quiz-option" onclick="checkAnswer(this, '1')">1</div>
        </div>
    </div>

    <div class="section">
        <h2>Resources</h2>
        <button onclick="window.open('https://www.miasalsjo.com/sydney-harbour-bridge-score-drawings')">Mia Salsjö's Graphic Scores</button>
        <button onclick="window.open('https://www.youtube.com/watch?v=qMg0boyByj8')">William Barton Performance</button>
    </div>

    <script>
        function checkAnswer(element, correctAnswer) {
            const userAnswer = element.textContent;
            const allOptions = element.parentElement.querySelectorAll('.quiz-option');
            
            allOptions.forEach(opt => {
                opt.classList.remove('correct', 'incorrect');
                if (opt.textContent.includes(correctAnswer)) {
                    opt.classList.add('correct');
                }
            });
            
            if (!element.textContent.includes(correctAnswer)) {
                element.classList.add('incorrect');
            }
        }
    </script>
</body>
</html>
