# Popular Spelling Suggestions


## Description
When users perform searches on Iconduck (and no results are found), I use a 3rd
party service to see if the user misspelled their query.

If they did, I'll then suggest that they perform a search for the "suggested
query".

Over time, this has allowed me to generate a map of 80,000+ (likely) misspelled
queries that can be mapped to a "more likely" correct query.

I've open sourced the CSV and JSON of this map in this repo for others to use.


## How to use it
One way `map.json` can be used is:  
When a user performs a search in your product, and no results are found, check
the map to see if it corresponds with another query.

If it does, you could either:
- Run the query again using the "more likely" correct query, or;
- Suggest the "more likely" correct query to them as something that can search


## Additional information
I've included `map.csv` incase that's useful for your data processing context.


## Maintenance
I'll aim to update this map at the beginning of each annual-quater.
Specifically:
- 01 January
- 01 April
- 01 July
- 01 October


## Feedback
Send it over to: [onassar@gmail.com](mailto:onassar@gmail.com)


## Notes to self:
- JSON converter: https://www.convertcsv.com/csv-to-json.htm
- Query: ```SELECT `query`, `suggestion` FROM `searchSuggestions` WHERE `suggestion` != '' ORDER BY `query`;```
