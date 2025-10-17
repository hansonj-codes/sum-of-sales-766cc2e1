Task: sum-of-sales

Brief: Publish a single-page site that fetches data.csv from attachments, sums its sales column, sets the title to "Sales Summary 374959384", displays the total inside #total-sales, and loads Bootstrap 5 from jsdelivr.

Checks:
- {'js': 'document.title === `Sales Summary 374959384`'}
- {'js': '!!document.querySelector("link[href*=\'bootstrap\']")'}
- {'js': 'Math.abs(parseFloat(document.querySelector("#total-sales").textContent) - ${result}) < 0.01'}
