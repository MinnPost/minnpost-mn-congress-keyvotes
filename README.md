# Minnesota Key Votes

Visualization of congressional key-votes.

## Data processing

We need to convert the CSV to JSONP.

1. Install [csvkit](http://csvkit.readthedocs.org/en/latest/index.html).
1. `csvjson -k "id" data/mn-delegation-key-votes.csv > visualizations/data/bills.json; echo "bills_callback(" > visualizations/data/bills.jsonp; cat visualizations/data/bills.json >> visualizations/data/bills.jsonp; echo ");" >> visualizations/data/bills.jsonp;`