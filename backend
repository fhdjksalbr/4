// Import required modules
const express = require('express');
const bodyParser = require('body-parser');

// Create an instance of Express.js
const app = express();

// Use body-parser middleware to parse JSON requests
app.use(bodyParser.json());

// Define an in-memory variable to store the total tap count
let totalTapCount = 0;

// Endpoint to store tap count
app.post('/tap', (req, res) => {
    // Extract tap count from request body
    const { count } = req.body;

    // Update total tap count
    totalTapCount += count;

    // Respond with updated total tap count
    res.json({ totalTapCount });
});

// Endpoint to retrieve total tap count
app.get('/total', (req, res) => {
    // Respond with the current total tap count
    res.json({ totalTapCount });
});

// Start the server and listen on a port
const PORT = process.env.PORT || 3000;
app.listen(PORT, () => {
    console.log(`Server is running on port ${PORT}`);
});
