# Election_Analysis

# PyPoll with Python


## Overview of Project
  
### Purpose
  

## Election Audit Results

- How many votes were cast in this congressional election?

The amount of votes that were cast in this congressional election was 369,711. This information was found by incrementing the total vote count for each row in the csv file. The code for this is shown below:

![image](https://user-images.githubusercontent.com/92827264/146693460-a530e50a-7c39-489d-9a9e-f1da17ddaf6d.png)


- Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.

The breakdown of each district and the percentage of total votes is shown below:

![image](https://user-images.githubusercontent.com/92827264/146693518-44efdcbb-dad3-4d87-9ef8-047c8df72a36.png)

This information was obtained by incrementing the vote count of every county during the loop through each row of the csv. After the code finished with the csv file it analysed the vote information. Using a for loop we loop through each county that was found during the csv read. We take the vote count for the county and divide it by the total votes. Then write the results into the text file. This is done in the code below: 

![image](https://user-images.githubusercontent.com/92827264/146693719-214114aa-a371-4ab7-80af-6d98d0ec09d5.png)

- Which county had the largest number of votes?

The county with the largest number of votes is Denver county with 306,055 votes. This information was obtained during the for loop used to cycle through the counties. There is an if statement that is comparing the votes of the current county and seeing if it is larger that the largest county voter turnout. This will always start as the first county because it these variables will the 0 at the start of each analysis, but update each time the votes of the current county is larger. That is how it finds the largest county. The county and number of voters is then written into the text file. The code of this is shown below:

![image](https://user-images.githubusercontent.com/92827264/146693979-ba9a7839-5e09-4af7-9b4f-bf4321133e29.png)

- Provide a breakdown of the number of votes and the percentage of total votes each candidate received.

A breakdown of the number of votes for each candidate is:
- Charles Caspar Stockholm with 85,213 which is 23% of the votes.
- Diana DeGette with 272,892 which is 73.8% of the votes.
- Raymon Anthony Doane with 11,606 which is 3.1% of the votes.

This data was obtained during the for loop that read the csv data. Each time the candidates name was found it checks to see if the name is in the list. If the name was not found it would add it to the list. The code then increments a count based on the candidates name for a total vote count for that candidate. There is another for loop set up after the csv read to cycle through the candidates and take the number for votes for that candidate and divide it by the total votes. These numbers are written to the text file. The code for this is shown below:

![image](https://user-images.githubusercontent.com/92827264/146694238-1b42daf2-cb42-44ea-be39-ab9c83249932.png)

![image](https://user-images.githubusercontent.com/92827264/146694249-284ae0c9-018b-4113-b42d-0c623837dd4a.png)

- Which candidate won the election, what was their vote count, and what was their percentage of the total votes?

The candidate that won the election is Diana DeGette with 272,892 votes which is 73.8%. This information was detemined the same way as the larges county. During the for loop for the candidates there is an if statement to is it current candidates votes are higher than the winning candidate and will write the highest it finds into the winning candidate variable. This will copy all the data from that candidate and write it into the text file. The code is shown below:

![image](https://user-images.githubusercontent.com/92827264/146694376-636cf2fc-2bfc-4a38-ab2d-6e33ab90061a.png)

## Election Audit Summary

  From seeing the results of the election in the analysis folder there is plenty of room for expansion. The code is not limited in the number of counties or candidates that the code can handle. This code can easily be expanded to handle the entire state or Colorado instead of just three counties as long as the data of the votes is in a similar or uniform pattern.
  
  For example, one way that this code can be altered to expand on this is to change the file from csv to reading from a database. Then creating a for loop to send queries for each counties vote data. Then having our code nested in that for loop analysing each counties results.
  
  If the data comes from each precinct in the form of an excel file, then we can create a uniform naming pattern for each precinct data and run a for loop to cycle through each precinct and read their csv files with our code being nested in that for loop.
