# Shmeeks

Random trivia where close counts. Ten questions per game, no multiple choice: type your answer and score up to 100 points per round based on how close you get.

- **Numbers** are scored by how far off your guess is (80 piano keys when the answer is 88 still earns 80 points).
- **Years** lose points for every year you're off.
- **Words** forgive typos and accept common alternate answers.

Play **Today's ten** (the same set for everyone each day) or a **Random ten** as often as you like. Your best score and today's score are saved in your browser.

## Running it

It's a single static file. Open `index.html` in a browser, or serve the repo with GitHub Pages.

## Adding questions

Questions live in the `BANK` object near the top of the script in `index.html`, split into `number`, `year` and `text`. For `text` questions, `a` is a list of accepted answers; the first one is shown as the correct answer.
