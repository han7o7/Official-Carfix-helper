#### File: index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CarFixHelper</title>
  <style>
    /* Theme: red, white, gray */
    body {
      font-family: Arial, sans-serif;
      background-color: #f8f8f8;
      margin: 0;
      color: #333;
    }
    header {
      background-color: #b71c1c;
      color: #fff;
      padding: 1rem;
      text-align: center;
    }
    main {
      padding: 1rem;
    }
    #search-section {
      text-align: center;
      margin-bottom: 2rem;
    }
    #search-input {
      width: 60%;
      padding: 0.5rem;
      font-size: 1rem;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    #search-button {
      background-color: #b71c1c;
      color: #fff;
      border: none;
      padding: 0.55rem 1.2rem;
      font-size: 1rem;
      border-radius: 4px;
      cursor: pointer;
      margin-left: 0.5rem;
    }
    #search-button:hover {
      opacity: 0.9;
    }
    #help-section details {
      background-color: #fff;
      padding: 1rem;
      border-radius: 4px;
      border: 1px solid #ddd;
      margin-bottom: 2rem;
    }
    #help-section summary {
      font-weight: bold;
      cursor: pointer;
    }
    #pictures {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
      justify-content: center;
    }
    #pictures img {
      max-width: 300px;
      width: 100%;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }
    footer {
      background-color: #e0e0e0;
      padding: 1rem;
      text-align: center;
    }
  </style>
</head>
<body>
  <header>
    <h1>CarFixHelper</h1>
  </header>

  <main>
    <section id="search-section">
      <h2>Search Car Problems</h2>
      <input id="search-input" type="text" placeholder="Describe your car issue...">
      <button id="search-button">Search Wikipedia</button>
    </section>

    <section id="help-section">
      <details>
        <summary>Help & Instructions</summary>
        <p>Type your car problem (e.g., "flat tire", "check engine light") and click "Search Wikipedia" to open troubleshooting guides in a new tab.</p>
      </details>
    </section>

    <section id="pictures">
      <h2>Image Gallery</h2>
      <img src="images/car1.jpg" alt="Car engine compartment">
      <img src="images/car2.jpg" alt="Mechanic fixing a tire">
    </section>
  </main>

  <footer>
    <p>Need more help? Call us: <strong>(123) 456-7890</strong></p>
  </footer>

  <script>
    document.getElementById('search-button').addEventListener('click', function() {
      const query = document.getElementById('search-input').value.trim();
      if (query) {
        const url = 'https://en.wikipedia.org/wiki/Special:Search?search=' + encodeURIComponent(query);
        window.open(url, '_blank');
      } else {
        alert('Please enter a search term.');
      }
    });
  </script>
</body>
</html>
