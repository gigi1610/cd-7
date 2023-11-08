const express = require('express');
const app = express();
const port = 8080;

app.get('/', (req, res) => {
    res.send('GET request to the home page');
});

app.get('/about', (req, res) => {
    res.send('GET request to the about page');
});

app.post('/create', (req, res) => {
    res.send('POST request to create a new item');
});

app.put('/update/:id', (req, res) => {
    res.send(`PUT request to update the item with id ${req.params.id}`);
});

app.delete('/delete/:id', (req, res) => {
    res.send(`DELETE request to delete the item with id ${req.params.id}`);
});

app.listen(port, () => {
    console.log(`Servidor rodando na porta ${port}`);
});# cd-7
