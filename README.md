# 🐍 Modern Snake: An ES6 JavaScript Experience

## 📜 Overview

**Modern Snake** is a sleek, performance-optimized reimagining of the classic arcade game. Built using a "Vanilla" approach, this project bypasses heavy frameworks to showcase the power of pure **HTML5**, **CSS3**, and **ES6+ JavaScript**. It features a "Dark Mode" aesthetic, responsive grid logic, and a high-performance rendering loop.

This isn't just a simple script; it's a demonstration of **Game Loop Architecture**, **DOM Manipulation**, and **State Management** in a browser environment.

---

## 🎮 Features

* **Dynamic Difficulty Scaling:** The game engine uses a velocity-based multiplier. Every time the snake consumes food, the `currentSpeed` is multiplied by , creating a seamless transition from "Relaxed" to "Expert" difficulty.
* **Persistent High Scores:** Utilizing the `window.localStorage` API, the game remembers your highest score even after the browser is closed or refreshed.
* **Collision Physics:** Includes logic for wall-boundary detection and self-collision (where the snake's head intersects with its own body array).
* **Responsive Engine:** The board uses CSS Variables (`--game-board-size`) and `calc()` to ensure the grid remains perfectly square and playable on mobile, tablet, and desktop screens.
* **Advanced Input Handling:** Implements "Input Buffering" logic to prevent the player from crashing by turning 180 degrees into their own neck.
![Snake Game Preview](screenshot.png)
---

## 🛠️ Technical Architecture

### 1. The Game Loop

Unlike basic `setInterval` approaches, this project uses `requestAnimationFrame`. This ensures the game logic runs in sync with the browser’s refresh rate, preventing screen tearing and reducing CPU usage.

### 2. The Coordinate System

The game operates on a  Cartesian grid. The snake is stored as an array of objects:

```javascript
let snake = [{ x: 10, y: 10 }, { x: 9, y: 10 }, { x: 8, y: 10 }];

```

Each "frame," a new head is calculated based on the current vector, and the tail is popped off—unless food is consumed, in which case the tail stays, and the snake "grows."

### 3. Styling with CSS Variables

The entire UI is controlled via a centralized `:root` palette. This allows for "Theming" by changing only a few variables:

* `--snake-color`: Emerald Green
* `--food-color`: Neon Red/Glow
* `--background-color`: Midnight Blue-Grey

---

## 🕹️ Controls

| Key | Action |
| --- | --- |
| **Arrow Up** | Move Up |
| **Arrow Down** | Move Down |
| **Arrow Left** | Move Left |
| **Arrow Right** | Move Right |
| **Space Bar** | Pause / Resume |

---

## 🚀 Installation & Usage

1. **Clone the Repository**
```bash
git clone https://github.com/null0git/snake_game_html.git

```


2. **Navigate to the Directory**
```bash
cd modern-snake

```


3. **Launch**
Open `index.html` in any modern browser (Chrome, Firefox, Safari, Edge). **No dependencies or Node.js required.**

---

## 📈 Future Roadmaps

* [ ] Add "Power-up" items (Speed slow-down, double points).
* [ ] Implementation of "Warp Walls" (going through one side to appear on the other).
* [ ] Sound effects using the Web Audio API.
* [ ] Different difficulty levels (Easy, Medium, Hard) at start.
