# Simple-Voting-System
# Python 
nominee_1 = input("Enter the Leader 1 name: ")
nominee_2 = input("Enter the Leader 2 name: ")

nom_1_votes= 0
nom_2_votes= 0
votes_id=[1, 2, 3, 4, 5, 6, 7,8]
num_of_voter=len(votes_id)

while True:
    if votes_id==[]:
        print("Voting Successfully Done!!")
        if nom_1_votes>nom_2_votes:
            print(nominee_1, "Is the Winner")
            break
        else:
            print(nominee_2, "Is the Winner!!")
            break
    voter_input = input("Enter your voter ID number: ")
    if not voter_input.isdigit():
        print("Invalid input! Voter ID must be a number.")
        continue
    voter = int(voter_input)
    if voter in votes_id:
        print("You are a Voter")
        
        vote = int(input("Enter your vote to Leader 1 or Leader 2: "))
        if vote == 1:
            nom_1_votes+= 1
            print("Successfully Voted !!")
            votes_id.remove(voter)
        elif vote == 2:
            nom_2_votes+= 1
            print("Successfully Voted !!")
            votes_id.remove(voter)
        else:
            print("Invalid vote! Vote not counted.")
    else:
        print("YOU ARE NOT A VOTER OR YOU HAVE VOTED")
