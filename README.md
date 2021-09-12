# election-analysis


# Election Audit Using Python

### Introduction

Our client, the Colorado Board of Elections, would like for us to do an audit of a US congressional race results for one prescinct. Our liason Tom and his manager Steve want the project done in Python rather than using Excel. The Python automated process can then be applied to other races and be scaled up or down depending on the usage. 

### Data Analysis

##### Data

The data is votes tabulated from three sources; mail in ballots, punch cards, and direct recording electronic counting. Mail in ballots are hand counted, punch card ballots are machine read, and the DRE memory cards are read by a computer. These results are then combined into the total election results. The specific data we've recieved from each ballot are the ballot ID, the county the ballot was cast in, and the Congress person that ballot had marked. 

##### Analysis

The data we recieved is in a csv file, so first we have to import the csv module to allow Python to read in the csv. We also import os to allow us to indirectly path to the csv file so that users regardless of operating system can path to the file. The ballot ID is not necessary for the analysis, so we only set up list and dictionaries to store data regarding the county the vote was cast in and the congressional candidate that ballot marked off. We then run through the csv data and convert the relevant data into dictionaries. We set up each key as either the county name for the county dictionary or the congressional candidate name for the results dictionary, and the value paired with it being a count of votes that was either cast in that county or voted for that candidate. From there a quick percentage calculation is done to determine what percntage of votes each candidate recieved and the distribution of votes via counties. 

### Audit Results

![Text file of results for county and candidate votes](https://github.com/roeggealissa/election-analysis/blob/875407244e71a2e17727e6560ce6f03b9174cc1c/Screen%20Shot%202021-09-12%20at%2011.40.38%20AM.png)

- The total number of votes counted in the congressional election in this precinct was 369,711 votes.
- The county with the least amount of votes was Arapahoe with 24,801 votes making up 6.7% of the total votes cast. The county with the second most was Jefferson with 38,855 votes making up 10.3% of the total votes cast. The county with the most votes cast was Denver with 308,055 votes making up 82.8% of the total votes cast.
- The county with the highest percentage of votes cast was Denver with 82.8% of the total votes cast in the congressional election.
- The candidate with the least amount of votes cast for them was Raymon Anthony Doane with 11,606 votes, or 3.1% of the total votes cast in the precinct. The candidate with the second most votes was Charles Casper Stockham with 85,213 votes or 23.0% of the total votes cast in the precinct. The candidate with the most votes is Diana DeGette with 73.8% of the total votes cast in the precicnt.
- The winner of the congressional election in this precinct with 73.8% of the total votes cast and counted was Diana DeGette.

### Possible Further Use of Automated Audit Script

Fortunately we did not hard code too much of the script so it is easily adaptable. So long as the election results are concatenated into a csv file, this script is stil applicable. We could look at the same precinct but expand our results to a full audit by finding the results to all items that were voted on, from other elections to ballot issues. Since we did not hard code in looking for names, the yess/no of ballot issues would be easy to modify for. For looking further at additional items on the same ballot, all we'd need are the same types of loops we are currently using for county and candidate but edited to look specifically for the additional results. Because of this modularity, we could also look at additional precincts and count the results in the same way. This could be scaled up to the full state level since there's no limit on the number of candidates, counties, or how many votes we can total. The scale up could continue on to other states, but since no precincts cross state lines the added complexity might not be worth it compared to the additional time needed to edit the code and the additional time the code would need to run.
