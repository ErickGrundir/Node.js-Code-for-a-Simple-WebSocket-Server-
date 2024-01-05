# Node.js-Code-for-a-Simple-WebSocket-Server-
Node.js Code for a Simple WebSocket Server
const WebSocket = require('ws');
const wss = new WebSocket.Server({ port: 8080 });

wss.on('connection', ws => {
    ws.on('message', message => {
        console.log(`Received: ${message}`);
    });

    ws.send('Hello, WebSocket!');
});
