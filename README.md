<!DOCTYPE html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Baby Brain Games - Fun Learning for Toddlers</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

```
    body {
        font-family: 'Comic Sans MS', 'Chalkboard SE', 'Arial Rounded MT Bold', cursive, sans-serif;
        background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
        min-height: 100vh;
        overflow-x: hidden;
    }

    /* Navigation */
    nav {
        background: rgba(255, 255, 255, 0.95);
        padding: 1rem 2rem;
        box-shadow: 0 4px 20px rgba(0,0,0,0.1);
        position: sticky;
        top: 0;
        z-index: 100;
    }

    .nav-content {
        max-width: 1400px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        gap: 1rem;
    }

    .logo {
        font-size: 2rem;
        font-weight: bold;
        color: #667eea;
        display: flex;
        align-items: center;
        gap: 0.5rem;
        cursor: pointer;
    }

    .nav-links {
        display: flex;
        gap: 0.5rem;
        flex-wrap: wrap;
    }

    .nav-btn {
        padding: 0.75rem 1.2rem;
        background: linear-gradient(135deg, #667eea, #764ba2);
        color: white;
        border: none;
        border-radius: 25px;
        font-size: 0.9rem;
        font-weight: bold;
        cursor: pointer;
        transition: transform 0.2s, box-shadow 0.2s;
    }

    .nav-btn:hover {
        transform: translateY(-2px);
        box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
    }

    /* Container */
    .container {
        max-width: 1400px;
        margin: 0 auto;
        padding: 2rem;
    }

    /* Page Sections */
    .page {
        display: none;
        animation: fadeIn 0.5s;
    }

    .page.active {
        display: block;
    }

    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
    }

    /* Home Page */
    .hero {
        text-align: center;
        padding: 3rem 0;
        color: white;
    }

    .hero h1 {
        font-size: 3.5rem;
        margin-bottom: 1rem;
        text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
    }

    .hero p {
        font-size: 1.5rem;
        margin-bottom: 2rem;
    }

    .game-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 2rem;
        margin-top: 2rem;
    }

    .game-card {
        background: white;
        border-radius: 25px;
        padding: 2rem;
        text-align: center;
        cursor: pointer;
        transition: transform 0.3s, box-shadow 0.3s;
        box-shadow: 0 10px 30px rgba(0,0,0,0.2);
    }

    .game-card:hover {
        transform: translateY(-10px);
        box-shadow: 0 15px 40px rgba(0,0,0,0.3);
    }

    .game-icon {
        font-size: 5rem;
        margin-bottom: 1rem;
    }

    .game-card h3 {
        font-size: 1.8rem;
        color: #667eea;
        margin-bottom: 0.5rem;
    }

    .game-card p {
        color: #666;
        font-size: 1rem;
    }

    /* Game Pages */
    .game-container {
        background: white;
        border-radius: 25px;
        padding: 2rem;
        box-shadow: 0 10px 40px rgba(0,0,0,0.2);
    }

    .game-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 2rem;
        flex-wrap: wrap;
        gap: 1rem;
    }

    .game-title {
        font-size: 2.5rem;
        color: #667eea;
    }

    .score-display {
        background: linear-gradient(135deg, #ffd89b, #19547b);
        color: white;
        padding: 1rem 2rem;
        border-radius: 50px;
        font-size: 1.5rem;
        font-weight: bold;
    }

    .instruction {
        background: linear-gradient(135deg, #a8edea, #fed6e3);
        padding: 2rem;
        border-radius: 20px;
        text-align: center;
        margin-bottom: 2rem;
        font-size: 1.5rem;
        font-weight: bold;
        color: #333;
    }

    .target-display {
        font-size: 8rem;
        text-align: center;
        margin: 2rem 0;
    }

    .game-grid-items {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
        gap: 1.5rem;
        margin-top: 2rem;
    }

    .game-item {
        aspect-ratio: 1;
        border-radius: 20px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 5rem;
        cursor: pointer;
        transition: transform 0.2s, box-shadow 0.2s;
        box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }

    .game-item:hover {
        transform: scale(1.05);
        box-shadow: 0 8px 25px rgba(0,0,0,0.2);
    }

    .game-item:active {
        transform: scale(0.95);
    }

    /* Colors */
    .color-red { background: linear-gradient(135deg, #ff6b6b, #ee5a6f); }
    .color-blue { background: linear-gradient(135deg, #4facfe, #00f2fe); }
    .color-yellow { background: linear-gradient(135deg, #ffd89b, #ffa500); }
    .color-green { background: linear-gradient(135deg, #43e97b, #38f9d7); }
    .color-purple { background: linear-gradient(135deg, #a8c0ff, #3f2b96); }
    .color-orange { background: linear-gradient(135deg, #fa709a, #fee140); }
    .color-pink { background: linear-gradient(135deg, #fbc2eb, #a6c1ee); }
    .color-brown { background: linear-gradient(135deg, #d4a574, #8b6f47); }

    /* Drawing Canvas */
    #drawing-canvas {
        border: 5px solid #667eea;
        border-radius: 20px;
        cursor: crosshair;
        touch-action: none;
        display: block;
        margin: 0 auto;
        background: white;
    }

    .color-palette {
        display: flex;
        gap: 1rem;
        justify-content: center;
        margin: 1rem 0;
        flex-wrap: wrap;
    }

    .color-btn {
        width: 60px;
        height: 60px;
        border-radius: 50%;
        border: 4px solid white;
        cursor: pointer;
        transition: transform 0.2s;
        box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    }

    .color-btn:hover {
        transform: scale(1.1);
    }

    .color-btn.active {
        border-color: #333;
        transform: scale(1.2);
    }

    .tool-btn {
        padding: 1rem 2rem;
        margin: 0.5rem;
        background: linear-gradient(135deg, #667eea, #764ba2);
        color: white;
        border: none;
        border-radius: 15px;
        font-size: 1.2rem;
        font-weight: bold;
        cursor: pointer;
        transition: transform 0.2s;
    }

    .tool-btn:hover {
        transform: scale(1.05);
    }

    /* Piano Keys */
    .piano-container {
        display: flex;
        justify-content: center;
        gap: 0.5rem;
        margin: 2rem 0;
        flex-wrap: wrap;
    }

    .piano-key {
        width: 80px;
        height: 250px;
        background: white;
        border: 3px solid #333;
        border-radius: 0 0 10px 10px;
        cursor: pointer;
        display: flex;
        align-items: flex-end;
        justify-content: center;
        padding-bottom: 1rem;
        font-size: 2rem;
        font-weight: bold;
        transition: transform 0.1s, background 0.1s;
        position: relative;
    }

    .piano-key:hover {
        background: #f0f0f0;
        transform: translateY(-5px);
    }

    .piano-key:active {
        background: #e0e0e0;
        transform: translateY(5px);
    }

    .piano-key.c { background: linear-gradient(to bottom, #ff6b6b, #ee5a6f); color: white; }
    .piano-key.d { background: linear-gradient(to bottom, #ffd89b, #ffa500); color: white; }
    .piano-key.e { background: linear-gradient(to bottom, #43e97b, #38f9d7); color: white; }
    .piano-key.f { background: linear-gradient(to bottom, #4facfe, #00f2fe); color: white; }
    .piano-key.g { background: linear-gradient(to bottom, #a8c0ff, #3f2b96); color: white; }
    .piano-key.a { background: linear-gradient(to bottom, #fa709a, #fee140); color: white; }
    .piano-key.b { background: linear-gradient(to bottom, #fbc2eb, #a6c1ee); color: white; }

    /* Memory Game */
    .memory-grid {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 1rem;
        max-width: 600px;
        margin: 2rem auto;
    }

    .memory-card {
        aspect-ratio: 1;
        background: linear-gradient(135deg, #667eea, #764ba2);
        border-radius: 15px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 4rem;
        cursor: pointer;
        transition: transform 0.3s;
        box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    }

    .memory-card:hover {
        transform: scale(1.05);
    }

    .memory-card.flipped {
        background: white;
    }

    .memory-card.matched {
        background: linear-gradient(135deg, #43e97b, #38f9d7);
        pointer-events: none;
    }

    /* Puzzle Game */
    .puzzle-grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 1rem;
        max-width: 500px;
        margin: 2rem auto;
    }

    .puzzle-piece {
        aspect-ratio: 1;
        border-radius: 15px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 5rem;
        cursor: pointer;
        transition: transform 0.2s;
        box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    }

    .puzzle-piece.empty {
        background: rgba(255,255,255,0.3);
        border: 3px dashed #667eea;
    }

    .puzzle-piece:not(.empty) {
        background: white;
    }

    .puzzle-piece:hover:not(.empty) {
        transform: scale(1.05);
    }

    /* Celebration */
    .celebration {
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 10rem;
        animation: bounce 0.5s infinite;
        pointer-events: none;
        z-index: 1000;
    }

    @keyframes bounce {
        0%, 100% { transform: translate(-50%, -50%) scale(1); }
        50% { transform: translate(-50%, -50%) scale(1.2); }
    }

    /* Sound Control */
    .sound-btn {
        position: fixed;
        bottom: 2rem;
        right: 2rem;
        width: 70px;
        height: 70px;
        border-radius: 50%;
        background: linear-gradient(135deg, #667eea, #764ba2);
        color: white;
        border: none;
        font-size: 2rem;
        cursor: pointer;
        box-shadow: 0 5px 20px rgba(0,0,0,0.3);
        transition: transform 0.2s;
        z-index: 50;
    }

    .sound-btn:hover {
        transform: scale(1.1);
    }

    /* Responsive */
    @media (max-width: 768px) {
        .hero h1 { font-size: 2.5rem; }
        .hero p { font-size: 1.2rem; }
        .game-icon { font-size: 4rem; }
        .game-item { font-size: 3rem; }
        .target-display { font-size: 5rem; }
        .piano-key { width: 60px; height: 200px; font-size: 1.5rem; }
        .memory-grid { grid-template-columns: repeat(3, 1fr); }
        #drawing-canvas { width: 100% !important; height: 300px !important; }
    }
</style>
```

</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-content">
            <div class="logo" onclick="showPage('home')">🎮 Baby Brain Games</div>
            <div class="nav-links">
                <button class="nav-btn" onclick="showPage('home')">🏠 Home</button>
                <button class="nav-btn" onclick="showPage('shapes')">🔷 Shapes</button>
                <button class="nav-btn" onclick="showPage('colors')">🎨 Colors</button>
                <button class="nav-btn" onclick="showPage('animals')">🐾 Animals</button>
                <button class="nav-btn" onclick="showPage('numbers')">🔢 Numbers</button>
                <button class="nav-btn" onclick="showPage('drawing')">✏️ Draw</button>
                <button class="nav-btn" onclick="showPage('piano')">🎹 Piano</button>
                <button class="nav-btn" onclick="showPage('memory')">🧠 Memory</button>
                <button class="nav-btn" onclick="showPage('puzzle')">🧩 Puzzle</button>
            </div>
        </div>
    </nav>

```
<div class="container">
    <!-- Home Page -->
    <div id="home" class="page active">
        <div class="hero">
            <h1>🌟 Welcome to Baby Brain Games! 🌟</h1>
            <p>Fun learning adventures for little ones ages 2-4</p>
        </div>
        
        <div class="game-grid">
            <div class="game-card" onclick="showPage('shapes')">
                <div class="game-icon">🔷</div>
                <h3>Shape Fun</h3>
                <p>Learn circles, squares, stars & hearts!</p>
            </div>
            
            <div class="game-card" onclick="showPage('colors')">
                <div class="game-icon">🎨</div>
                <h3>Color Magic</h3>
                <p>Discover beautiful colors!</p>
            </div>
            
            <div class="game-card" onclick="showPage('animals')">
                <div class="game-icon">🐾</div>
                <h3>Animal Friends</h3>
                <p>Meet cute animals & their sounds!</p>
            </div>
            
            <div class="game-card" onclick="showPage('numbers')">
                <div class="game-icon">🔢</div>
                <h3>Number Land</h3>
                <p>Count from 1 to 5!</p>
            </div>

            <div class="game-card" onclick="showPage('drawing')">
                <div class="game-icon">✏️</div>
                <h3>Drawing Fun</h3>
                <p>Create colorful masterpieces!</p>
            </div>

            <div class="game-card" onclick="showPage('piano')">
                <div class="game-icon">🎹</div>
                <h3>Music Piano</h3>
                <p>Play beautiful sounds!</p>
            </div>

            <div class="game-card" onclick="showPage('memory')">
                <div class="game-icon">🧠</div>
                <h3>Memory Match</h3>
                <p>Find matching pairs!</p>
            </div>

            <div class="game-card" onclick="showPage('puzzle')">
                <div class="game-icon">🧩</div>
                <h3>Slide Puzzle</h3>
                <p>Solve the emoji puzzle!</p>
            </div>
        </div>
    </div>

    <!-- Shapes Game -->
    <div id="shapes" class="page">
        <div class="game-container">
            <div class="game-header">
                <h2 class="game-title">🔷 Shape Fun</h2>
                <div class="score-display">⭐ <span id="shapes-score">0</span></div>
            </div>
            <div class="instruction">Find the: <span id="shapes-target-name"></span></div>
            <div class="target-display" id="shapes-target"></div>
            <div class="game-grid-items" id="shapes-grid"></div>
        </div>
    </div>

    <!-- Colors Game -->
    <div id="colors" class="page">
        <div class="game-container">
            <div class="game-header">
                <h2 class="game-title">🎨 Color Magic</h2>
                <div class="score-display">⭐ <span id="colors-score">0</span></div>
            </div>
            <div class="instruction">Find the: <span id="colors-target-name"></span></div>
            <div class="target-display" id="colors-target"></div>
            <div class="game-grid-items" id="colors-grid"></div>
        </div>
    </div>

    <!-- Animals Game -->
    <div id="animals" class="page">
        <div class="game-container">
            <div class="game-header">
                <h2 class="game-title">🐾 Animal Friends</h2>
                <div class="score-display">⭐ <span id="animals-score">0</span></div>
            </div>
            <div class="instruction">Find the: <span id="animals-target-name"></span></div>
            <div class="target-display" id="animals-target"></div>
            <div class="game-grid-items" id="animals-grid"></div>
        </div>
    </div>

    <!-- Numbers Game -->
    <div id="numbers" class="page">
        <div class="game-container">
            <div class="game-header">
                <h2 class="game-title">🔢 Number Land</h2>
                <div class="score-display">⭐ <span id="numbers-score">0</span></div>
            </div>
            <div class="instruction">Find: <span id="numbers-target-name"></span></div>
            <div class="target-display" id="numbers-target"></div>
            <div class="game-grid-items" id="numbers-grid"></div>
        </div>
    </div>

    <!-- Drawing Game -->
    <div id="drawing" class="page">
        <div class="game-container">
            <h2 class="game-title" style="text-align: center; margin-bottom: 1rem;">✏️ Drawing Fun</h2>
            <div class="color-palette">
                <div class="color-btn active" style="background: #ff0000;" onclick="changeColor('#ff0000', this)"></div>
                <div class="color-btn" style="background: #0000ff;" onclick="changeColor('#0000ff', this)"></div>
                <div class="color-btn" style="background: #ffff00;" onclick="changeColor('#ffff00', this)"></div>
                <div class="color-btn" style="background: #00ff00;" onclick="changeColor('#00ff00', this)"></div>
                <div class="color-btn" style="background: #ff00ff;" onclick="changeColor('#ff00ff', this)"></div>
                <div class="color-btn" style="background: #ffa500;" onclick="changeColor('#ffa500', this)"></div>
                <div class="color-btn" style="background: #000000;" onclick="changeColor('#000000', this)"></div>
            </div>
            <div style="text-align: center;">
                <button class="tool-btn" onclick="clearCanvas()">🗑️ Clear</button>
            </div>
            <canvas id="drawing-canvas" width="800" height="500"></canvas>
        </div>
    </div>

    <!-- Piano Game -->
    <div id="piano" class="page">
        <div class="game-container">
            <h2 class="game-title" style="text-align: center; margin-bottom: 2rem;">🎹 Music Piano</h2>
            <div class="instruction">Press the keys to play music!</div>
            <div class="piano-container">
                <div class="piano-key c" onclick="playNote(261.63, '🎵 C')">C</div>
                <div class="piano-key d" onclick="playNote(293.66, '🎵 D')">D</div>
                <div class="piano-key e" onclick="playNote(329.63, '🎵 E')">E</div>
                <div class="piano-key f" onclick="playNote(349.23, '🎵 F')">F</div>
                <div class="piano-key g" onclick="playNote(392.00, '🎵 G')">G</div>
                <div class="piano-key a" onclick="playNote(440.00, '🎵 A')">A</div>
                <div class="piano-key b" onclick="playNote(493.88, '🎵 B')">B</div>
            </div>
        </div>
    </div>

    <!-- Memory Game -->
    <div id="memory" class="page">
        <div class="game-container">
            <div class="game-header">
                <h2 class="game-title">🧠 Memory Match</h2>
                <div class="score-display">⭐ <span id="memory-score">0</span></div>
            </div>
            <div class="instruction">Find matching pairs!</div>
            <div class="memory-grid" id="memory-grid"></div>
            <div style="text-align: center; margin-top: 2rem;">
                <button class="tool-btn" onclick="initMemoryGame()">🔄 New Game</button>
            </div>
        </div>
    </div>

    <!-- Puzzle Game -->
    <div id="puzzle" class="page">
        <div class="game-container">
            <div class="game-header">
                <h2 class="game-title">🧩 Slide Puzzle</h2>
                <div class="score-display">Moves: <span id="puzzle-moves">0</span></div>
            </div>
            <div class="instruction">Slide the pieces to arrange them in order!</div>
            <div class="puzzle-grid" id="puzzle-grid"></div>
            <div style="text-align: center; margin-top: 2rem;">
                <button class="tool-btn" onclick="shufflePuzzle()">🔄 Shuffle</button>
            </div>
        </div>
    </div>
</div>

<!-- Sound Button -->
<button class="sound-btn" id="sound-btn" onclick="toggleSound()">🔇</button>

<!-- Celebration -->
<div id="celebration" style="display: none;"></div>

<script>
    let soundEnabled = false;
    let currentScores = {
        shapes: 0,
        colors: 0,
        animals: 0,
        numbers: 0,
        memory: 0
    };

    // Audio Context for Piano
    let audioContext = null;

    const games = {
        shapes: [
            { name: 'Circle', display: '🔵', id: 'circle' },
            { name: 'Square', display: '🟦', id: 'square' },
            { name: 'Star', display: '⭐', id: 'star' },
            { name: 'Heart', display: '❤️', id: 'heart' },
            { name: 'Triangle', display: '🔺', id: 'triangle' },
            { name: 'Diamond', display: '💎', id: 'diamond' }
        ],
        colors: [
            { name: 'Red', display: '🔴', id: 'red', class: 'color-red' },
            { name: 'Blue', display: '🔵', id: 'blue', class: 'color-blue' },
            { name: 'Yellow', display: '🟡', id: 'yellow', class: 'color-yellow' },
            { name: 'Green', display: '🟢', id: 'green', class: 'color-green' },
            { name: 'Purple', display: '🟣', id: 'purple', class: 'color-purple' },
            { name: 'Orange', display: '🟠', id: 'orange', class: 'color-orange' },
            { name: 'Pink', display: '💗', id: 'pink', class: 'color-pink' },
            { name: 'Brown', display: '🟤', id: 'brown', class: 'color-brown' }
        ],
        animals: [
            { name: 'Cat', display: '🐱', sound: 'Meow!', id: 'cat' },
            { name: 'Dog', display: '🐶', sound: 'Woof!', id: 'dog' },
            { name: 'Cow', display: '🐮', sound: 'Moo!', id: 'cow' },
            { name: 'Duck', display: '🦆', sound: 'Quack!', id: 'duck' },
            { name: 'Pig', display: '🐷', sound: 'Oink!', id: 'pig' },
            { name: 'Sheep', display: '🐑', sound: 'Baa!', id: 'sheep' },
            { name: 'Lion', display: '🦁', sound: 'Roar!', id: 'lion' },
            { name: 'Frog', display: '🐸', sound: 'Ribbit!', id: 'frog' }
        ],
        numbers: [
            { name: 'One', display: '1️⃣', id: '1' },
            { name: 'Two', display: '2️⃣', id: '2' },
            { name: 'Three', display: '3️⃣', id: '3' },
            { name: 'Four', display: '4️⃣', id: '4' },
            { name: 'Five', display: '5️⃣', id: '5' },
            { name: 'Six', display: '6️⃣', id: '6' },
            { name: 'Seven', display: '7️⃣', id: '7' },
            { name: 'Eight', display: '8️⃣', id: '8' }
        ]
    };

    let currentTargets = {};

    function showPage(pageId) {
        document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
        document.getElementById(pageId).classList.add('active');
        
        if (pageId !== 'home') {
            if (['shapes', 'colors', 'animals', 'numbers'].includes(pageId)) {
                initGame(pageId);
            } else if (pageId === 'drawing') {
                initDrawing();
            } else if (pageId === 'memory') {
                initMemoryGame();
            } else if (pageId === 'puzzle') {
                initPuzzle();
            }
        }
    }

    function initGame(gameType) {
        const items = games[gameType];
        const target = items[Math.floor(Math.random() * items.length)];
        currentTargets[gameType] = target;

        document.getElementById(`${gameType}-target-name`).textContent = target.name;
        document.getElementById(`${gameType}-target`).textContent = target.display;

        const grid = document.getElementById(`${gameType}-grid`);
        grid.innerHTML = '';
```
