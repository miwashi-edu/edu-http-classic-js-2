# Create Backend Server

## Instructions

```bash
cd ~
cd ws
cd gomoku-backend
mkdir ./src/routes
touch ./src/routes/gomoku_routes.js
```

## ./src/service.js
```bash

cat > ./src/service.js << 'EOF'
const express = require('express');
const app = express();
app.use(express.json());
app.use('/api/gomoku', require('./routes/gomoku_routes.js'))
const PORT = process.env.PORT || 3000
app.listen(PORT, () => {
    console.log(`http server listening on port ${PORT}`)
});
EOF
```

## ./src/routes/gomoku_routes.js
```bash
cat > ./src/routes/gomoku_routes.js << 'EOF'
const router = require('express').Router();

router.get('/create_game', (req, res) =>{
    res.json({status: "success"});
});

router.get('/add_player', (req, res) =>{
    res.json({status: "success"});
});

router.get('/play', (req, res) =>{
    res.json({status: "success"});
});

module.exports = router;
EOF
```
