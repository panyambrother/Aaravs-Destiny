# Aaravs-Destiny
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aarav's Destiny</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="game-container">
        <div id="story-box">
            <p id="story-text">It was a cold, moonlit night...</p>
        </div>
        <div id="action-buttons">
            <button id="option1">Explore Forest</button>
            <button id="option2">Check Satchel</button>
            <button id="option3">Talk to Siblings</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>body {
    font-family: Arial, sans-serif;
    background-color: #2c3e50;
    color: #ecf0f1;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

#game-container {
    width: 600px;
    background-color: #34495e;
    border-radius: 10px;
    padding: 20px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
}

#story-box {
    margin-bottom: 20px;
}

#action-buttons button {
    background-color: #1abc9c;
    border: none;
    padding: 10px 15px;
    margin: 5px;
    border-radius: 5px;
    cursor: pointer;
    color: #fff;
}

#action-buttons button:hover {
    background-color: #16a085;
}const storyText = document.getElementById('story-text');
const option1 = document.getElementById('option1');
const option2 = document.getElementById('option2');
const option3 = document.getElementById('option3');

// Initial Story State
let storyState = 0;

// Story Progression Logic
const story = [
    "It was a cold, moonlit night. Aarav sat clutching a photo of his mother...",
    "A strange glow filled the room, and Rayan appeared, offering guidance.",
    "You find yourself in a vibrant forest. What do you do next?"
];

// Event Listeners for Buttons
option1.addEventListener('click', () => {
    storyState++;
    if (storyState < story.length) {
        storyText.textContent = story[storyState];
    } else {
        storyText.textContent = "You explore the forest and encounter two frightened children...";
    }
});

option2.addEventListener('click', () => {
    storyText.textContent = "You check your satchel and find peculiar tools and shimmering crystals.";
});

option3.addEventListener('click', () => {
    storyText.textContent = "You talk to Meghana and Megan, who reveal their tragic story.";
});
