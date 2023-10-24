# Create Backend Server

## Instructions

```bash
cd ~
cd ws
cd gomoku-backend
mkdir __tests__
touch ./__tests__/integration_test.js
npm pkg set scripts.test="jest"
npm pkg set scripts.test:watch="jest --watchAll"
npm install -D jest
npm install --save-dev supertest
```

## ./__tests__/integration_test.js
```bash
cat > ./__tests__/integration_test.js << 'EOF'
const request = require('supertest');
const baseUrl = 'http://localhost:3000';
describe('Gomoku Routes', () => {

    test('GET /api/gomoku/create_game', async () => {
        const response = await request(baseUrl).get('/api/gomoku/create_game');
        expect(response.status).toBe(200);
        expect(response.body).toEqual({status: "success"});
    });

    test('GET /api/gomoku/add_player', async () => {
        const response = await request(baseUrl).get('/api/gomoku/add_player');
        expect(response.status).toBe(200);
        expect(response.body).toEqual({status: "success"});
    });

    test('GET /api/gomoku/play', async () => {
        const response = await request(baseUrl).get('/api/gomoku/play');
        expect(response.status).toBe(200);
        expect(response.body).toEqual({status: "success"});
    });

});
EOF
```
