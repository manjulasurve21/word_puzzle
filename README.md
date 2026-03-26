# 🎯 Word Masters

**Word Masters** is a browser-based word puzzle game inspired by the popular game **Wordle**.  
Players have **six attempts** to guess a **secret five-letter English word**, with visual feedback provided after each guess.

This project is built using **HTML, CSS, and Vanilla JavaScript**, and integrates with a real-world API to fetch and validate words.

> ⚠️ Unlike the original demo, this version is **fully responsive** and works smoothly on **mobile devices**.

---

## 🕹️ How to Play

1. A secret **five-letter word** is chosen by the system.
2. You have **6 guesses** to find the correct word.
3. After each guess, letters are highlighted:
   - 🟩 **Green** → Correct letter in the correct position
   - 🟨 **Yellow** → Correct letter but wrong position
   - ⬜ **Gray** → Letter not in the word
4. Duplicate letters are handled accurately.
5. Guess the word correctly to **win**.
6. Fail after six attempts and the game reveals the correct word.

---

## ✨ Features

- 🎯 Wordle-style gameplay logic
- 🔄 Real-time keyboard input handling
- 🌐 API-based word fetching and validation
- 🎨 Visual feedback with animations
- 📱 Fully responsive (mobile, tablet, desktop)
- ⏳ Loading indicator during API calls
- ❌ Invalid word detection with UI feedback
- 🏆 Win and lose states with animations

---

## 🧠 Game Rules Logic

- Only **valid English 5-letter words** are accepted.
- Green letters are matched first to ensure accuracy.
- Yellow letters are marked only if unused instances exist.
- Example:
  - Guess: `SPOOL`
  - Word: `OVERT`
  - Result: One `O` marked yellow, second `O` ignored.

---

## 🔌 APIs Used
GET  https://words.dev-apis.com/word-of-the-day


**Response:**
```json
{
  "word": "humph",
  "puzzleNumber": 3
}
```

POST https://words.dev-apis.com/validate-word

# Request Body:

```json
{
  "word": "crane"
}
```

# Response:

```json
{
  "word": "crane",
  "validWord": true
}
```


## 🧪 Input Validation Helper

```js
function isLetter(letter) {
  return /^[a-zA-Z]$/.test(letter);
}
```
Ensures only alphabetic characters are processed and ignores invalid keystrokes.

# 🛠️ Tech Stack

- HTML5 – Structure

- CSS3 – Styling, animations, responsiveness

- JavaScript (ES6+) – Game logic & API handling

- Fetch API – Network requests

## 🧩 Project Breakdown
# Development Steps

1. Designed the HTML structure (grid, header, loader)

2. Styled the UI using CSS Grid and animations

3. Implemented keyboard input handling

4. Integrated API to fetch the secret word

5. Added word validation logic

6. Implemented color-coded feedback (green, yellow, gray)

7. Handled duplicate letter logic correctly

8. Added loading spinner and invalid word animation

9. Implemented win/lose conditions

10. Made the UI fully responsive for mobile and desktop


# 📂 Project Structure
```
Word-Masters/
│
├── index.html
├── style.css
├── index.js
└── README.md
```
# 🚀 Future Improvements

- On-screen mobile keyboard

- Dark mode toggle

- Custom modal instead of browser alerts

- Keyboard color feedback

- Daily streak tracking

# 📚 What I Learned

- Working with real-world APIs

- Async JavaScript using async/await

- DOM manipulation and event handling

- Input validation and UX feedback

- Implementing complex game logic similar to Wordle

#  🙌 Acknowledgements

- Inspired by Wordle

- API provided by Frontend Masters

# 🔗 Project Preview

-- GitHub Repository:
https://github.com/manjulasurve21/word_puzzle

