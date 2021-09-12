# election-analysis


# Election Audit Using Python

### Introduction

Our client, the Colorado Board of Elections, would like for us to do an audit of a US Congressional race results for one prescinct. Our liason Tom and his manager Steve want the project done in Python rather than using Excel. The python automated process can then be applied to other races and be scaled up or down depending on the usage. 

### Data Analysis

##### Data

The data is votes tabulated from three sources; mail in ballots, punch cards, and direct recording electronic counting. Mail in ballots are hand counted, punch card ballots are machine read, and the DRE memory cards are read by a computer. These results are then combined into the total election results. The specific data we've recieved from each ballot are the ballot ID, the county the ballot was cast in, and the Congress person that ballot had marked. 

##### Analysis

The data we recieved is in a csv file, so first we have to import the csv module to allow python to read in the csv. We also import os to allow us to indirectly path to the csv file so that users regardless of operating system can path to the file. The ballot ID is not necessary for the analysis, so we only set up list and dictionaries to store data regarding the county the vote was cast in and the Congressional candidate that ballot marked off. We then run through the csv data and convert the relevant data into dictionaries. We set up each key as either the county name for the county dictionary or the Congressional candidate name for the results dictionary, and the value paired with it being a count of votes that was either cast in that county or voted for that candidate. From there a quick percentage calculation is done to determine what percntage of votes each candidate recieved and the distribution of votes via counties. 

### Audit Results

![Text file of results for county and candidate votes](https://github.com/roeggealissa/election-analysis/blob/875407244e71a2e17727e6560ce6f03b9174cc1c/Screen%20Shot%202021-09-12%20at%2011.40.38%20AM.png)
