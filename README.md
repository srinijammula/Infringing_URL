# Infringing_URL
A Json file is provided, which contains fields relevant to notices sent by companies regarding copyright material URLs. We need to flatten and transform the data so that each row corresponds to one infringing URL. Later, add the appropriate domain and IP fields.
My approach,
1. Load JSON data.
2. Extract the base information in notices before extracting infringing URLs from field works. If any data, such as nested arrays, need further flattening, change it.
3. Go to works, add a description, then loop through each infringing_url to get a row.
4. Use infringing_url to discover domain and IP addresses and add them to the data.
5. To handle enormous amounts of data, I used a multiprocessing library with four CPUs.
6. Download the data frame as a CSV file.
7. Determine the number of unique values in each column for further investigation.
8. I created three summaries: domain and IP analysis, temporal analysis using date_sent, and regional analysis by jurisdiction.
