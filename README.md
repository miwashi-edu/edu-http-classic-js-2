# Create Backend Server

## Instructions

```bash
cd ~
cd ws
cd gomoku-backend
```

## ./src/service.js
```bash

cat > ./src/service.js << 'EOF'
const express = require('express');
const app = express();
app.use(express.json());
app.use((req,res)=>{
    console.log({query:req.query});
    console.log({body: req.body});
    console.log({params: req.params});
    console.log({header: req.headers});
    res.send({status:"success"});
})

const PORT = process.env.PORT || 3000
app.listen(PORT, () => {
    console.log(`http server listening on port ${PORT}`)
});
EOF
```
