# Sales Summary 374959384

This is a single-page website intended to be deployed on GitHub Pages. It fetches `data.csv` from the repository root, sums the `sales` column, sets the page title to "Sales Summary 374959384", and displays the total inside the `#total-sales` element.

New feature:
- Currency selector (#currency-picker) that converts the computed total using `rates.json` from the repository and mirrors the selected currency code inside `#total-currency`.

Behavior:
- The page attempts to load `rates.json`. If it's valid JSON mapping currency codes to numeric rates, those currencies populate the selector.
- If `rates.json` fails to load or parse, the selector will at least contain USD and conversion defaults to 1:1.
- The CSV parser expects well-formed CSV (no quoted commas). Sales values are parsed as floats.

How to deploy:
1. Push this repository to GitHub.
2. In the repository settings, enable GitHub Pages and select the branch that contains index.html.
3. Visit the GitHub Pages URL. The page will load `data.csv` and `rates.json` (if present) and display the total sales in the selected currency.

Notes:
- Ensure `data.csv` and `rates.json` are in the repository root (same directory as index.html on GitHub Pages).
- The element IDs required by automated checks are present: #currency-picker (with an option USD) and #total-currency.

License: MIT