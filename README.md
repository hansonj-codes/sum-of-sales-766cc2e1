# Sales Summary 374959384

This is a single-page website intended to be deployed on GitHub Pages. It fetches `data.csv` from the repository root, sums the `sales` column, sets the page title to "Sales Summary 374959384", and displays the total inside the `#total-sales` element.

New feature:
- A currency selector (#currency-picker) is added which converts the computed total using `rates.json`.
- The active currency code is shown in `#total-currency`.

How it works:
- The app loads `data.csv` and `rates.json` from the repository root.
- It computes the total sales (assumed in the base currency, typically USD).
- The currency selector is populated from `rates.json`'s "rates" keys (USD included).
- Changing the currency converts the displayed total using the rate from `rates.json`.

How to deploy:
1. Push this repository to GitHub.
2. In the repository settings, enable GitHub Pages and select the main branch (or the branch you used).
3. Visit the provided GitHub Pages URL. The page will load `data.csv` and `rates.json` and display the total sales with currency conversion.

Notes:
- The CSV parser is lightweight and expects well-formed CSV without embedded commas or quotes.
- If `rates.json` is missing or malformed, the page falls back to USD with a rate of 1.

License: MIT