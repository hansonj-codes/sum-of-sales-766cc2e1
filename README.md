# Sales Summary 374959384

This is a single-page website intended to be deployed on GitHub Pages. It fetches `data.csv` from the repository root, sums the `sales` column, sets the page title to "Sales Summary 374959384", and displays the total inside the `#total-sales` element.

New feature:
- A currency selector (#currency-picker) converts the computed total using rates provided in `rates.json` and mirrors the active currency code inside `#total-currency`.

How it works:
- The page loads `data.csv`, parses it, and sums the `sales` column.
- It then attempts to load `rates.json` (expected to be a JSON object mapping currency codes to numeric rates).
- The currency picker is populated from the keys in `rates.json`. USD is guaranteed to be present.
- Selecting a currency converts the base total by the corresponding rate and updates the displayed amount and the `#total-currency` element.

How to deploy:
1. Push this repository to GitHub.
2. In the repository settings, enable GitHub Pages and select the main branch (or the branch you used).
3. Visit the provided GitHub Pages URL. The page will load `data.csv` and display the total sales with the currency selector.

Notes:
- The page expects `data.csv` and `rates.json` to be located at the repository root (same directory as index.html on GitHub Pages).
- The rates file should be JSON (e.g. {"USD":1,"EUR":0.9,"GBP":0.8}). The loader has some tolerance for slightly different shapes (e.g., {"rates":{...}}).
- The CSV parser is a lightweight implementation suitable for well-formed CSV without embedded commas or quotes.

License: MIT