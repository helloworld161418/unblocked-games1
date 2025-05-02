# unblocked-games1
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Unblocked Games Site</title>
    <link rel="stylesheet" href="style.css"> </head>
<body>
    <header>
        <h1>My Unblocked Games</h1>
      
      
      <h1>scroll down!</h1>
    
 
      
        
    <footer>
        <p>&copy; 2025 My Unblocked Games</p>
    </footer>

    <script src="script.js"></script> </body>
</html>
<div class="embedded-game">
    <h2>suika game</h2>
    <iframe src="https://playsuikagame.com" width="800" height="600" frameborder="7" allowfullscreen></iframe>
</div>
<div class="embedded-game">
    <h2>2048</h2>
   <iframe src="https://mathisfun.com/games/2048" width="800" height="600" frameborder="0" allowfullscreen></iframe>
    
  <div class="embedded-games">
    <h2>4 in a line</h2>
    <iframe src="https://mathisfun.com/games/connect4"
    width="800" height="600" frameborder="0"
    allowfullscreen><iframe> 
      
      <div class="embbeded-games">
        <h2>sudoku puzzle</h2>
      <iframe src="https://www.mathsisfun.com/games/sudoku"
    width="800" height="600" frameborder="0"
    allowfullscreen><iframe>
   
     body {
    font-family: sans-serif;
    margin: 0;
    background-color: #f4f4f4;
    color: #333;
}

header {
    background-color: #333;
    color: white;
    padding: 1em;
    text-align: center;
}

header input[type="text"] {
    padding: 0.5em;
    margin-top: 0.5em;
    border: none;
    border-radius: 5px;
}

nav {
    background-color: #ddd;
    padding: 0.5em;
}

nav ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
}

nav ul li {
    margin: 0 1em;
}

nav ul li a {
    text-decoration: none;
    color: #333;
}

#game-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    padding: 20px;
    gap: 20px;
}

.game-card {
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    overflow: hidden;
}

.game-card a {
    display: block;
    text-decoration: none;
    color: inherit;
    text-align: center;
}

.game-card img {
    width: 100%;
    height: auto;
    display: block;
}

.game-card h3 {
    padding: 0.5em;
    margin: 0;
    font-size: 1em;
}

footer {
    text-align: center;
    padding: 1em;
    background-color: #333;
    color: white;
    position: fixed;
    bottom: 0;
    width: 100%;
}

document.addEventListener('DOMContentLoaded', () => {
    const gameContainer = document.getElementById('game-container');
    const searchInput = document.querySelector('header input[type="text"]');
    const gameCards = Array.from(gameContainer.querySelectorAll('.game-card'));

    // Function to load a game (replace with your actual logic)
    gameContainer.addEventListener('click', (event) => {
        const gameLink = event.target.closest('.game-card a');
        if (gameLink) {
            const gameUrl = gameLink.dataset.gameUrl;
            // For demonstration, let's just log the URL
            console.log('Loading game:', gameUrl);
            // In a real scenario, you might open the URL in a new tab
            // or embed it in a specific area of your page using an iframe.
            window.open(gameUrl, '_blank');
        }
    });

    // Search functionality
    searchInput.addEventListener('input', (event) => {
        const searchTerm = event.target.value.toLowerCase();
        gameCards.forEach(card => {
            const title = card.querySelector('h3').textContent.toLowerCase();
            if (title.includes(searchTerm)) {
                card.style.display = 'block';
            } else {
                card.style.display = 'none';
            }
        });
    });
});
