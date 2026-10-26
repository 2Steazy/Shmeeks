# Shmeeks

A Price-is-Right style trivia game about the most expensive version of everything. Seven questions per round, 30 seconds each, no multiple choice: type your answer and get paid based on how pricey it is.

| Tier | Points | Example (most expensive pet bird) |
|---|---|---|
| 💰 Jackpot! | 1,000 | Hyacinth Macaw |
| 🥇 Big Spender | 600 | Scarlet Macaw |
| 🥈 Pricey | 350 | African Grey |
| 🥉 Mid-Range | 150 | Amazon |
| 🪙 Bargain Bin | 50 | Cockatiel |
| 🏷️ Clearance | 10 | Parakeet |

Anything that doesn't fit the category scores 0. Answers forgive typos, capitalization and filler words ("the ruby roman grapes" counts as Ruby Roman).

Play **today's round** (the same seven for everyone each day) or **bonus rounds** as often as you like. Today's score and your best score are saved in your browser, and **Share** copies an emoji summary of your round.

## Running it

It's a single static file. Open `index.html` in a browser, or serve the repo with GitHub Pages.

## Adding questions

Questions live in the `BANK` array near the top of the script in `index.html`. Each entry has:

- `q`: the question text, and `cat`: a short category label
- `noun`: words stripped from answers before matching (e.g. `["grape","grapes"]`)
- `tiers`: six lists of accepted answers, from Jackpot down to Clearance
- `ladder`: six labels shown on the reveal screen, one per tier
- `fact`: the fun fact shown after answering

When an answer matches more than one list, the longest (most specific) match wins, so "black summer truffle" scores as Summer rather than Black.
