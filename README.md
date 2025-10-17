# Sales Summary 374959384

This is a single-page website intended to be deployed on GitHub Pages. It fetches `data.csv` from the repository root, sums the `sales` column, sets the page title to "Sales Summary 374959384", and displays the total inside the `#total-sales` element.

Features:
- Loads Bootstrap 5 from jsDelivr CDN.
- Parses a simple CSV (expects a header row and comma-separated values).
- Graceful error handling if `data.csv` cannot be fetched.

How to deploy:
1. Push this repository to GitHub.
2. In the repository settings, enable GitHub Pages and select the main branch (or the branch you used).
3. Visit the provided GitHub Pages URL. The page will load `data.csv` and display the total sales.

Notes:
- The page expects `data.csv` to be located at the repository root (same directory as index.html on GitHub Pages).
- The CSV parser is a lightweight implementation suitable for well-formed CSV without embedded commas or quotes.

License: MIT