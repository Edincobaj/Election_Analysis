# Election_Analysis
The purpose of this election audit analysis is to determine the results of this election along with the voter turnout for each county, the percentage of votes from each county out of the total count and determine the county with the highest turnout.

# Election-Audit Results
## From the analysis we can determine several key factors in this election:
* There were a total of 369,711 votes cast in this congressional election.
* We were able to determine the number of votes and the percentage of total votes for each county in the precint: Denver had the largest population at 306,055 which made up 82.8% of the total votes. Jefferson came in second at 38,855 which made up 10.5% of the total votes. Lastly Arapahoe at 24,801 which made up 6.7% of the total votes.
* From our analysis we were able to see that Denver had the largest number of votes.
* The following shows a breakdown of the number of votes and the percentage of the total votes each candidate recieved: Charles Casper Stockham 23.0% with 85,213 votes, Diana DeGette 73.8% with 272,892 votes, and Raymon Anthony Doane at 3.1% with 11,606 votes.
* The clear winner of this election was Diana DeGette with 272,892 votes which covered 73.8% of the total votes. 

#### Below is an overview of all the aforementioned information- 

### ![image](https://user-images.githubusercontent.com/41974323/140670081-911ef683-18fd-4ceb-b0a1-dfbee329e411.png)

#### To derive the above results of the election, we wrote the following for loop in the following code:
```
for county in county_list:
        # 6b: Retrieve the county vote count.
        county_vote = county_votes.get(county)

        # 6c: Calculate the percentage of votes for the county.
        county_vote_percentage = float(county_vote) / float(total_votes) * 100


         # 6d: Print the county results to the terminal.
        county_results = f"{county}: {county_vote_percentage:.1f}% ({county_vote:,})\n"

        print(county_results
        )
         # 6e: Save the county votes to a text file.
        txt_file.write(county_results)

         # 6f: Write an if statement to determine the winning county and get its vote count.
        if (county_vote > largest_county_turnout_count) and (
            county_vote_percentage > largest_county_percentage
        ):
            # True
            largest_county_turnout_count = county_vote
            largest_county_percentage = county_vote_percentage
            largest_county_turnout = county

    # 7: Print the county with the largest turnout to the terminal.
    winning_county_print = (
        f"-------------------------\n"
        f"Largest County Turnout: {largest_county_turnout}\n"
        f"-------------------------\n"
    )
    print(winning_county_print)
 ```
# Election-Audit Summary

If we were to submit a business proposal to the election commission on how this script can be used for any election, I believe there would be a couple different ways it can be used. For example this code can be scaled up to larger national elections or even smaller elections. We could also make some modifications to the code to include the parties of the candidates to give a little more insight on how they might affect outcomes.
