# Create Backend Server

## Instructions

```bash
cd ~
cd ws
cd gomoku-backend
mkdir {public,src}
touch ./src/service.js
npm init -y
npm install express
npm pkg set scripts.start="node ./src/service.js"
npm pkg set scripts.dev="node --watch ./src/service.js"
```

## ./src/service.js
```bash
cat > ./src/service.js << 'EOF'
const express = require('express');
const app = express();
app.use(express.static('public'))
const PORT = process.env.PORT || 3000
app.listen(PORT, () => {
    console.log(`http server listening on port ${PORT}`)
});
EOF
```
