# lab8# Project 9 Solutions

# Student Name: Michael Harshman

# 1a. (2 pt)
# Comment about method of solution: Use awk to sum up amounts in colum 4
Solution itself 
cat /class/datamine/data/taxi/yellow/yellow_tripdata_2019-06.csv | awk -F, '{mytotal = mytotal + $4} END{print mytotal}'
# Output from the solution
10878820

# 1b. (2 pt)
# Comment about method of solution: Used awk to add up the total from last part as well as total rides, then ended it by dividing total by rides.
Solution itself 
cat /class/datamine/data/taxi/yellow/yellow_tripdata_2019-06.csv | awk -F, '{mytotal = mytotal + $4; myrides = myrides + 1} END{print mytotal / myrides}'
# Output from the solution 
1.56732

# 2a. (2 pts)
# Comment about method of solution: I used awk to add up all transactions using the if on date to select only Dec 23, 17 and printed the total.
Solution itself 
cat /class/datamine/data/8451/The_Complete_Journey_2_Master/5000_transactions.csv | awk -F, '{if ($3 == "23-DEC-17") {mysum = mysum + $5}} END{print mysum}'
# Output from the solution
108408

# 2b. (2 pts)
# Comment about method of solution: I used awk to get total dollar amount on Dec 23, 2017 and found total transactions, then divided to get average.
Solution itself 
cat /class/datamine/data/8451/The_Complete_Journey_2_Master/5000_transactions.csv | awk -F, '{if ($3 == "23-DEC-17") {mysum = mysum + $5; total = total + 1}} END{print mysum / total}'
# Output from the solution
4.07045

# 3a. (2 pt)
# Comment about method of solution: I found the total amount of money donated with awk and divided by the total amount of donations.
Solution itself 
cat /class/datamine/data/election/itcont2018.txt | awk -F\| '{mysum = mysum + $15; total = total + 1} END{print mysum / total}'
# Output from the solution 
257.348
