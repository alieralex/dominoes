# 🎲 Caribbean Dominoes Manager

A comprehensive web application for exploring, learning, and scoring traditional Caribbean domino games. This app preserves and celebrates the rich domino culture of the Dominican Republic, Puerto Rico, and Cuba by providing detailed rules, interactive scoring systems, and game history tracking for 11 different regional variations.

![Caribbean Dominoes](https://img.shields.io/badge/Made%20with-❤️-red) ![Caribbean Culture](https://img.shields.io/badge/Caribbean-Culture-blue) ![Dominoes](https://img.shields.io/badge/Game-Dominoes-green)

---

## 📖 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Game Variations](#game-variations)
- [How It Works](#how-it-works)
- [Technical Architecture](#technical-architecture)
- [Usage Guide](#usage-guide)
- [Installation & Deployment](#installation--deployment)
- [File Structure](#file-structure)
- [Browser Compatibility](#browser-compatibility)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [Cultural Context](#cultural-context)

---

## 🎯 Overview

**Caribbean Dominoes Manager** is a single-page web application designed to help players:
1. **Learn** the rules and scoring systems of 11 different Caribbean domino variations
2. **Track scores** during live games with an intuitive interface
3. **Review history** of completed games with detailed statistics

The app works entirely in the browser with no server required, making it perfect for sharing via WhatsApp or deploying to GitHub Pages. All data is stored locally in the browser's localStorage, so game history persists between sessions.

### Target Audience
- Caribbean diaspora wanting to preserve cultural games
- Domino players learning regional variations
- Families playing together who need score tracking
- Game enthusiasts interested in Caribbean culture

---

## ✨ Features

### 1. Game Explorer
- **11 Caribbean Domino Variations** organized by country (🇩🇴 🇵🇷 🇨🇺)
- Detailed rule explanations for each game
- Scoring system documentation
- Country-specific terminology and traditions
- Direct game start from rule pages

### 2. Interactive Score Tracker
- **Dynamic player/team setup** based on game type
- Real-time score calculation
- Round-by-round score entry
- Automatic winner detection
- Visual scoreboard with color-coded display
- Score reset and game management controls

### 3. Game History
- Automatic saving of completed games
- Date/time stamps for each game
- Winner and final scores display
- Detailed player/team breakdown
- Persistent storage across browser sessions

### 4. Help & Documentation
- Comprehensive user guide in Spanish
- Step-by-step instructions for each feature
- Cultural context about Caribbean dominoes
- Tips for optimal app usage

### 5. Responsive Design
- **Mobile-first approach** - optimized for phones
- Works on tablets and desktop computers
- Touch-friendly interface
- Adaptive layouts for all screen sizes

---

## 🎮 Game Variations

### 🇩🇴 Dominican Republic (5 variations)

#### 1. Dominó Clásico (Por Parejas)
- **Players**: 4 (2 teams of 2)
- **Description**: The most popular game in the Dominican Republic
- **Key Rules**: 7 tiles per player, double-9 set, first to 200 points wins
- **Scoring**: Winning team scores the sum of losing team's remaining tiles

#### 2. Dominó Individual
- **Players**: 4 (everyone plays solo)
- **Description**: Each player for themselves, no teams
- **Key Rules**: Same basic rules but individual scoring
- **Scoring**: Winner takes points from all other players' hands

#### 3. Dominó Capicú
- **Players**: 4 (2 teams of 2)
- **Description**: Bonus points for ending with doubles (capicú)
- **Key Rules**: Ending with a double matching both ends scores double points
- **Scoring**: Normal scoring but capicú can win instantly or double points

#### 4. Dominó de Chivo
- **Players**: 4 (2 teams of 2)
- **Description**: Reverse scoring - losers accumulate points ("el chivo")
- **Key Rules**: Goal is to have FEWER points
- **Scoring**: Losing team gets points from their remaining tiles, team with fewer points wins

#### 5. Dominó Cerrado
- **Players**: 4 (2 teams of 2)
- **Description**: Game ends when blocked ("trancado")
- **Key Rules**: When no one can play, game is closed
- **Scoring**: Team with fewer tile points wins and scores the difference

### 🇵🇷 Puerto Rico (3 variations)

#### 6. Dominó Puertorriqueño
- **Players**: 4 (2 teams of 2)
- **Description**: Boricua version with "tranca" and "pegao" traditions
- **Key Rules**: Allows "cantar" (announcing) to communicate with partner
- **Scoring**: Special scoring for "tranca" situations and "pegao" wins

#### 7. Dominó a 100
- **Players**: 4 (2 teams of 2)
- **Description**: Fast-paced version, first to 100 points
- **Key Rules**: Same as Puertorriqueño but shorter game
- **Scoring**: First team to exactly 100 points wins

#### 8. Dominó de Seis (Doble Seis)
- **Players**: 4 (2 teams of 2)
- **Description**: Played with double-6 set (28 tiles only)
- **Key Rules**: Only tiles 0-0 through 6-6, more strategic
- **Scoring**: Standard scoring but faster, more tactical gameplay

### 🇨🇺 Cuba (3 variations)

#### 9. Dominó Cubano
- **Players**: 4 (2 teams of 2)
- **Description**: Cuba's national game, very social
- **Key Rules**: 10 tiles per player using double-9 set
- **Scoring**: Winning team scores all losing team's tile points

#### 10. Dominó de Bateo
- **Players**: 4 (2 teams of 2)
- **Description**: Special scoring for playing consecutive same-number tiles
- **Key Rules**: "Bateo" = starting with double and continuing that number
- **Scoring**: Complete bateo can double points or win instantly

#### 11. La Pareja Cubana
- **Players**: 4 (2 teams of 2)
- **Description**: Emphasizes partner communication with allowed signals
- **Key Rules**: Hand signals to communicate strong suits
- **Scoring**: Standard scoring but strategy heavily partner-dependent

---

## 🔧 How It Works

### User Flow

```
┌─────────────────────────────────────────────────────────────┐
│                     USER OPENS APP                          │
└─────────────────────┬───────────────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────────────┐
│               TAB NAVIGATION SYSTEM                         │
│  ┌──────────┬──────────┬───────────┬───────────┐          │
│  │ EXPLORE  │  SCORE   │  HISTORY  │   HELP    │          │
│  └──────────┴──────────┴───────────┴───────────┘          │
└─────────────────────────────────────────────────────────────┘
                      │
        ┌─────────────┼─────────────┬─────────────┐
        │             │             │             │
        ▼             ▼             ▼             ▼
┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐
│ EXPLORE  │  │  SCORE   │  │ HISTORY  │  │   HELP   │
│  GAMES   │  │  GAMES   │  │  REVIEW  │  │  GUIDE   │
└──────────┘  └──────────┘  └──────────┘  └──────────┘
     │             │             │
     │             │             │
     ▼             ▼             ▼
┌──────────┐  ┌──────────┐  ┌──────────┐
│ View     │  │ Setup    │  │ Browse   │
│ Rules    │  │ Players  │  │ Past     │
│ By       │  │ & Teams  │  │ Games    │
│ Country  │  └─────┬────┘  └──────────┘
│          │        │
│ Select   │        ▼
│ Game     │  ┌──────────┐
│ Type     │  │ Track    │
└────┬─────┘  │ Scores   │
     │        │ Round by │
     │        │ Round    │
     │        └─────┬────┘
     │              │
     │              ▼
     │        ┌──────────┐
     │        │ Auto     │
     │        │ Detect   │
     │        │ Winner   │
     │        └─────┬────┘
     │              │
     │              ▼
     │        ┌──────────┐
     │        │ Save to  │
     │        │ History  │
     └────────┴─────┬────┘
                    │
                    ▼
            ┌──────────────┐
            │ localStorage │
            │  (persist)   │
            └──────────────┘
```

### Component Interaction

1. **Navigation System**: Four main tabs control which content panel is visible
2. **Game Detail System**: Click any game card → shows full rules → can start game directly
3. **Score Tracking System**: Setup form → live scoreboard → automatic winner detection
4. **Storage System**: All games saved to browser localStorage automatically

---

## 🏗️ Technical Architecture

### Technology Stack

- **HTML5**: Semantic structure, single-page application
- **CSS3**: Responsive design, animations, gradient backgrounds
- **Vanilla JavaScript**: No frameworks or dependencies
- **localStorage API**: Client-side data persistence

### Design Patterns

#### 1. Single-Page Application (SPA)
```javascript
// Tab-based navigation without page reloads
function showTab(tab) {
    // Hide all content panels
    document.querySelectorAll('.content-panel').forEach(panel => {
        panel.classList.remove('active');
    });
    
    // Show selected panel
    document.getElementById(tab + '-panel').classList.add('active');
}
```

#### 2. Game State Management
```javascript
// Global game state object
let currentGame = {
    type: 'clasico',          // Game variation ID
    name: 'Dominó Clásico',   // Display name
    teams: true,              // Team vs individual
    winningScore: 200,        // Target score
    players: [],              // Player/team array
    scores: [],               // Round-by-round history
    startTime: new Date()     // Timestamp
};
```

#### 3. Dynamic Form Generation
```javascript
// Forms adapt based on game type (teams vs individual)
function updatePlayerInputs() {
    const game = gameDetails[gameType];
    
    if (game.teams) {
        // Generate team input structure
        container.innerHTML = `
            <div class="player-input">
                <span>Equipo 1:</span>
                <input type="text" id="team1-player1">
                <input type="text" id="team1-player2">
            </div>
            <!-- Team 2 inputs -->
        `;
    } else {
        // Generate individual player inputs
        // 4 separate player input fields
    }
}
```

#### 4. Automatic Winner Detection
```javascript
function renderScoreboard() {
    // Check for winner based on game rules
    let winner = currentGame.players.find(p => {
        if (currentGame.type === 'chivo') {
            // Chivo: reverse scoring, lowest wins
            return p.score >= currentGame.winningScore;
        } else {
            // Normal: highest score wins
            return p.score >= currentGame.winningScore;
        }
    });
    
    // Display winner announcement if found
    if (winner) {
        // Show celebration UI
    }
}
```

#### 5. Data Persistence
```javascript
// Games automatically saved to browser storage
function endGame() {
    currentGame.endTime = new Date();
    gameHistory.push({...currentGame});
    
    // Saved in localStorage (implicit in browser)
    // Retrieved on next page load
    updateHistory();
}
```

### CSS Architecture

#### Responsive Design Strategy
```css
/* Mobile-first base styles */
.game-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 20px;
}

/* Tablet and desktop adjustments */
@media (max-width: 768px) {
    .game-grid {
        grid-template-columns: 1fr; /* Single column on mobile */
    }
}
```

#### Color System
- **Primary**: Purple gradient (`#667eea` to `#764ba2`)
- **Success**: Green (`#4CAF50`)
- **Danger**: Red (`#ff6b6b`)
- **Neutral**: Grays for text and backgrounds

#### Component Styling
- **Cards**: Gradient backgrounds, hover effects, rounded corners
- **Buttons**: Gradient fills, shadow on hover, smooth transitions
- **Tables**: Alternating row colors, centered data, responsive

---

## 📱 Usage Guide

### For Players

#### Starting a New Game
1. Click **"Anotar Partida"** (Score Game) tab
2. Select game type from dropdown (organized by country)
3. Set winning score (default: 200 points)
4. Enter player/team names
5. Click **"Comenzar Partida"** (Start Game)

#### Tracking Scores
1. After each round, enter points for each player/team
2. Click **"Agregar Mano"** (Add Round)
3. App automatically calculates totals
4. Winner announced when target score reached

#### Managing Games
- **"Reiniciar Puntos"** (Reset Scores): Clear all scores, keep game setup
- **"Terminar Partida"** (End Game): Save to history and start new game

#### Viewing History
1. Click **"Historial"** (History) tab
2. Browse past games with dates, winners, and final scores
3. See detailed breakdown of all player scores

### For Developers & AI Agents

#### Key Functions Reference

```javascript
// NAVIGATION
showTab(tab)                    // Switch between main app tabs
showGameDetail(gameType)        // Show detailed rules for a game
hideGameDetail()                // Return to game list
startGameFromDetail(gameType)   // Quick start from rules page

// GAME MANAGEMENT
updatePlayerInputs()            // Generate player/team input forms
startGame()                     // Initialize new game session
renderScoreboard()              // Update scoreboard display
addRoundScore()                 // Record round results
resetScores()                   // Clear scores but keep game
endGame()                       // Finalize and save game

// HISTORY
updateHistory()                 // Refresh history display with saved games
```

#### Data Structures

```javascript
// GAME DETAILS (configuration object)
gameDetails = {
    'clasico': {
        name: string,           // Display name
        players: number,        // Number of players (always 4)
        teams: boolean,         // true = 2 teams, false = 4 individuals
        country: string,        // Country of origin
        description: string,    // Brief description
        rules: string[],        // Array of rule statements
        scoring: string         // Scoring explanation
    },
    // ... 10 more game variations
}

// CURRENT GAME (runtime state)
currentGame = {
    type: string,               // Game variation ID ('clasico', 'pr-100', etc)
    name: string,               // Display name
    teams: boolean,             // Team vs individual mode
    winningScore: number,       // Target score to win
    players: [                  // Player/team array
        {
            name: string,       // Player or "Player1 & Player2"
            score: number       // Current total score
        }
    ],
    scores: [                   // Round history
        {
            round: number,
            scores: number[]    // Snapshot of all scores after this round
        }
    ],
    startTime: Date,            // Game start timestamp
    endTime: Date               // Game end timestamp (added on completion)
}

// GAME HISTORY (persisted array)
gameHistory = [
    currentGame,                // Completed game objects
    currentGame,
    // ... all past games
]
```

#### Extending the App

**Adding a New Game Variation:**

1. Add to `gameDetails` object:
```javascript
gameDetails['new-game'] = {
    name: 'New Game Name 🇩🇴',
    players: 4,
    teams: true,
    country: 'Dominican Republic',
    description: 'Game description',
    rules: [
        'Rule 1',
        'Rule 2',
        // ...
    ],
    scoring: 'Scoring explanation'
};
```

2. Add to game selection dropdown:
```html
<optgroup label="🇩🇴 República Dominicana">
    <option value="new-game">New Game Name</option>
</optgroup>
```

3. Add game card to explorer:
```html
<div class="game-card" onclick="showGameDetail('new-game')">
    <h3>🎯 New Game Name</h3>
    <p>Brief description for card</p>
</div>
```

**Modifying Scoring Logic:**

Edit `renderScoreboard()` and `addRoundScore()` functions to implement custom scoring rules for specific game types.

---

## 🚀 Installation & Deployment

### Local Development

**Option 1: Direct File Open**
```bash
# Simply open index.html in any browser
open index.html  # macOS
start index.html # Windows
xdg-open index.html # Linux
```

**Option 2: Local Server (Recommended)**
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js (if you have http-server installed)
npx http-server

# Then visit: http://localhost:8000
```

### GitHub Pages Deployment

1. **Create GitHub Repository**
```bash
git init
git add index.html
git commit -m "Initial commit: Caribbean Dominoes app"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/dominoes.git
git push -u origin main
```

2. **Enable GitHub Pages**
   - Go to repository Settings
   - Navigate to Pages section
   - Select Source: `main` branch
   - Click Save

3. **Access Your App**
   - URL: `https://YOUR-USERNAME.github.io/dominoes/`
   - Share this link via WhatsApp or any messaging app

### Other Deployment Options

- **Netlify**: Drag and drop `index.html` to netlify.com/drop
- **Vercel**: Push to GitHub, connect repo, auto-deploy
- **Firebase Hosting**: `firebase init` → `firebase deploy`

---

## 📁 File Structure

```
dominoes/
│
├── index.html              # Single-file application (HTML + CSS + JS)
├── README.md              # This comprehensive documentation
│
└── (Optional files)
    ├── .gitignore
    └── LICENSE
```

### Single-File Architecture Rationale

The entire application is contained in one `index.html` file for several reasons:

1. **Easy Sharing**: Single file can be sent via WhatsApp, email, or any file sharing
2. **No Dependencies**: Works immediately without npm install or build steps
3. **Offline Capable**: Once loaded, works without internet (except initial load)
4. **Simple Deployment**: Just upload one file to any web host
5. **Version Control**: Entire app state in one file, easy to track changes

**Structure within index.html:**
```html
<!DOCTYPE html>
<html>
<head>
    <style>
        /* All CSS (~500 lines) */
    </style>
</head>
<body>
    <!-- All HTML structure -->
    
    <script>
        /* All JavaScript (~600 lines) */
    </script>
</body>
</html>
```

---

## 🌐 Browser Compatibility

### Fully Supported
✅ **Chrome/Edge** 90+ (Chromium-based)  
✅ **Firefox** 88+  
✅ **Safari** 14+ (iOS and macOS)  
✅ **Mobile Browsers** (iOS Safari, Chrome Mobile, Samsung Internet)

### Required Browser Features
- ES6 JavaScript (arrow functions, template literals, spread operator)
- CSS Grid and Flexbox
- localStorage API
- HTML5 semantic elements

### Known Issues
- **Internet Explorer**: Not supported (EOL browser)
- **Safari < 14**: Some CSS gradient animations may not render perfectly
- **Old Android browsers**: Use Chrome or Firefox for best experience

---

## 🔮 Future Enhancements

### Planned Features
- [ ] **Online Multiplayer Mode**: Play dominoes online with real tiles
- [ ] **Advanced Statistics**: Win rates, average scores, player rankings
- [ ] **More Regional Variations**: Jamaica, Venezuela, Colombia variations
- [ ] **Dark Mode**: Toggle for night play
- [ ] **Export/Import Games**: Share game history between devices
- [ ] **Multi-language Support**: English, Spanish, French Creole
- [ ] **Progressive Web App (PWA)**: Install as native-like app
- [ ] **Sound Effects**: Optional audio feedback
- [ ] **Tile Animations**: Visual tile movements

### Technical Improvements
- [ ] Cloud sync for game history (Firebase/Supabase)
- [ ] User accounts and profiles
- [ ] Social features (share results, leaderboards)
- [ ] Offline-first architecture with Service Workers

---

## 🤝 Contributing

Contributions are welcome! This project aims to preserve and share Caribbean domino culture.

### How to Contribute

1. **Report Issues**: Found a bug or have a suggestion?
   - Open an issue on GitHub
   - Describe the problem or idea clearly
   - Include screenshots if applicable

2. **Add New Game Variations**
   - Research authentic regional rules
   - Follow existing game structure in `gameDetails`
   - Test scoring logic thoroughly
   - Submit pull request with clear description

3. **Improve Documentation**
   - Fix typos or unclear explanations
   - Add more cultural context
   - Translate to other languages

4. **Code Improvements**
   - Keep single-file architecture
   - Maintain vanilla JavaScript (no frameworks)
   - Follow existing code style
   - Test on multiple devices/browsers

### Development Guidelines

- **Code Style**: Use clear variable names, add comments for complex logic
- **Commits**: Write descriptive commit messages
- **Testing**: Verify on mobile and desktop before submitting
- **Documentation**: Update README if adding features

---

## 🎲 Cultural Context

### Dominoes in Caribbean Culture

Dominoes is not just a game in the Caribbean—it's a social institution. You'll find domino games happening:

- **Colmados** (corner stores): The classic setting for afternoon games
- **Parks and plazas**: Public gathering spaces
- **Family gatherings**: Weddings, birthdays, holidays
- **Beaches**: Weekend tournaments and casual play
- **Neighborhood streets**: Impromptu games with folding tables

### The Social Experience

Caribbean dominoes is loud, competitive, and joyful:
- **"Capicú!"**: The triumphant shout when winning with a double
- **"Trancao!"**: Called when the game is blocked
- **Table slapping**: Emphasizing plays with dramatic flair
- **Trash talk**: Good-natured banter is part of the game
- **Spectators**: Games often draw crowds of onlookers

### Regional Differences

While the basic game is similar across islands, each culture has developed unique variations:

- **Dominican Republic**: Fast-paced, emphasis on partnership communication
- **Puerto Rico**: More formal rules, "tranca" situations common
- **Cuba**: Very social, longer games, double-9 set standard

### Preservation Goal

This app aims to:
1. **Document authentic rules** before they're lost to generational changes
2. **Teach younger generations** these traditional games
3. **Connect diaspora communities** with their cultural heritage
4. **Facilitate gameplay** in modern contexts (digital scorekeeping)

---

## 📄 License

This project is open source and available under the MIT License.

You are free to:
- Use commercially
- Modify
- Distribute
- Private use

Please maintain attribution and share improvements back to the community.

---

## 💬 Contact & Support

- **Issues**: Open a GitHub issue for bugs or feature requests
- **Discussions**: Use GitHub Discussions for questions and ideas
- **Email**: [Your contact email]

---

## 🙏 Acknowledgments

- The Caribbean domino community for preserving these traditions
- Family members who taught us these games
- Open source community for tools and inspiration

---

**Made with ❤️ for the Caribbean community** 🇩🇴 🇵🇷 🇨🇺

*¡Que gane el mejor!* (May the best player win!)

---

## 📊 Quick Stats

- **11 Game Variations**
- **3 Caribbean Countries**
- **Single HTML File**
- **0 Dependencies**
- **100% Offline Capable**
- **Mobile-First Design**
- **100% Free & Open Source**# dominoes
Webapp for playing all the variations of dominoes.
