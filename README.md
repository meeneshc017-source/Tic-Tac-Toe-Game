# Tic-Tac-Toe-Game
A simple Tic Tac Toe game built with HTML, CSS, and JavaScript.

## How to play

Open `index.html` in your browser.

## Features

- Play against another person
- Simple UI

## Example Code

```html
<!-- index.html -->
<!DOCTYPE html>
<html>
<head>
  <title>Tic Tac Toe Game</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Tic Tac Toe</h1>
  <div id="board"></div>
  <script src="script.js"></script>
</body>
</html>
```

```css
/* style.css */
body {
  background: #f0f0f0;
  font-family: Arial, sans-serif;
}
#board {
  display: grid;
  grid-template-columns: repeat(3, 60px);
  grid-gap: 5px;
}
```

```javascript
// script.js
const board = document.getElementById('board');
let currentPlayer = 'X';

// Create 9 cells
for (let i = 0; i < 9; i++) {
  const cell = document.createElement('button');
  cell.className = 'cell';
  cell.addEventListener('click', function() {
    if (!cell.textContent) {
      cell.textContent = currentPlayer;
      currentPlayer = currentPlayer === 'X' ? 'O' : 'X';
    }
  });
  board.appendChild(cell);
}
```

## License

MIT