# Create Backend Server

## Instructions

```bash
```

## ./src/routes/gomoku_routes.js
```bash
cat > ./src/routes/gomoku_routes.js << 'EOF'
const express = require('express');
const router = express.Router();
const gameData = require('./game.json');  // adjust the path if the file is in a different directory

router.get('/create_game', (req, res) => {
    res.json(gameData);
});

router.get('/add_player', (req, res) => {
    res.json(gameData);
});

router.get('/play', (req, res) => {
    res.json(gameData);
});

module.exports = router;
EOF
```

## ./src/routes/game.json
```bash
cat > ./src/routes/game.json << 'EOF'
{
    "id": "015cdc04-4d22-46f7-8d8e-f1879bb9bf1b",
    "name": "empty game",
    "round": 256,
    "player": 1,
    "player1": {
        "id": "",
        "name": "name1"
    },
    "player2": {
        "id": "",
        "name": "name2"
    },
    "state":"playing",
    "board": {
        "minInRow": 5,
        "cols": 16,
        "rows": 16,
        "tiles": [
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
            [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0]
        ]
    }
}
EOF
```
