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
    body { font-family: Arial, sans-serif; background-color: #f8f8f8; margin: 0; }
    header { background-color: #b71c1c; color: #fff; padding: 1rem; text-align: center; }
    main { padding: 1rem; }
    section { margin-bottom: 1.5rem; }
    #search-section input {
      width: 70%; padding: 0.5rem; font-size: 1rem; border: 1px solid #ccc; border-radius: 4px;
    }
    #search-section button {
      background-color: #b71c1c; color: #fff; border: none; padding: 0.5rem 1rem; font-size: 1rem;
      border-radius: 4px; cursor: pointer; margin-left: 0.5rem;
    }
    #search-section button:hover { opacity: 0.9; }
    #pictures img { max-width: 100%; height: auto; margin: 0.5rem 0; border-radius: 8px; }
    footer { background-color: #e0e0e0; padding: 1rem; text-align: center; }
    details { margin-bottom: 1rem; }
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
        <p>Enter the car problem you’re experiencing (e.g., “flat tire”, “engine overheating”) into the search box and click “Search Wikipedia”. A new tab will open with Wikipedia search results for troubleshooting guides.</p>
        <p>Browse the image gallery below to identify common issues visually.</p>
      </details>
    </section>

    <section id="pictures">
      <h2>Image Gallery</h2>
      <!-- Place your own images in an 'images/' folder -->
      <img src="images/car1.jpg" alt="Car engine compartment">
      <img src="images/car2.jpg" alt="Mechanic fixing a tire">
    </section>
  </main>

  <footer>
    <p>Need more help? Call us: <strong>(815) 419-3003</strong></p>
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
```

#### File: README.md
```markdown
# CarFixHelper

CarFixHelper is a simple web application that helps users find car repair solutions via Wikipedia and provides visual guidance and contact support.

## Features Implemented
- **Wikipedia Search**: Enter your car issue to search Wikipedia troubleshooting pages.
- **Help System**: Collapsible instructions section using HTML `<details>`.
- **Image Gallery**: Showcase of common car problems. Add your own photos in `images/`.
- **Contact Support**: Displayed phone number for direct assistance.

## Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/CarFixHelper.git
   ```
2. Add your images to the `images/` folder, naming them `car1.jpg`, `car2.jpg`, etc.
3. Open `index.html` in your browser, or deploy to GitHub Pages by:
   - Pushing to the `main` branch
   - Enabling GitHub Pages in the repository settings (root `/`)

## Project Proposal Reference
This implementation covers the core features from the Class Project Proposal:
- Production deployment ready on GitHub Pages
- Public GitHub repository URL shared above
- Help system and user instructions included
- README updated with proposal reference and delivered features

## Next Steps
If more time were available, I would:
- Integrate an autocomplete search using the Wikipedia API
- Add a modal-based help tutorial
- Improve the image gallery with pagination or filtering

## License
MIT © <Atahan Ors>
