# SIADS_591_MILESTONE1
Scripts for milestone 1 Project Data Collection, Manip and cleaning

/assets/images/74ef3f9fa08cd876398503a8ce24ea50.jpeg
 
First script Pytrens_ACNH_version2-3 takes the villagers names from villagers.csv and creates a list(appended Animal Crossing to the name for each item in the list) from the names which using the built in API function pulls the Google Trends Related Queries and fetches the historical searches per villager name.  Returns a dictionary of the names searched and the "rising" key contains the query (search conducted) and value of number of all time searches related to the animal crossing villager name.  It then pulls out the rising and parses with for loop to pull back and append to empty df all queries and values of villagers names where there were searches on Google and ignore the none's

Second script combining_ACP_Polls takes all 2020 and 2021 ACP MONTHLY POLL VOTE RESULTS and reads in each file and only keeps the Villagers and Tally column which represents the villager name and number of votes received for each character based on favs from ACNH player votes.  Groupby is used to sum up the tally votes by villager name and then the two dataframes (2020 and 2021) are stacked to create one df and then the group by is done one last time to get each character and total number of votes (Tally as sum).  

Third script will clean and pull the villager name from the resultant first script csv file final_append.csv, the villagers that are missing are assumed to have a google search value of zero.

Fourth script will take the resultant csv files from first two scripts (final_append.csv and ACP_FinalDF.csv) and do some cleaning/normalizing of names to join on the villagers.csv and add on the Tally field and total google searches per villager from each csv.
