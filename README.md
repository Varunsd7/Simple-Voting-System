# Simple-Voting-System
1. Project Overview
This project is a simple Python-based voting system that allows a group of registered voters to cast votes for one of two nominated leaders. Each voter is identified by a unique voter ID, and the system ensures that only eligible voters can vote and that each voter can vote only once. The program collects votes, keeps track of each nominee’s vote count, and determines the winner based on who receives the majority of votes. The voting concludes once all voters have cast their votes, and the system then announces the winner.


2. Problem Statement
In many real-world scenarios such as elections, polls, or group decisions, a reliable system is needed to collect and process votes securely and fairly. Manual voting methods are time-consuming and prone to errors or manipulation. This project aims to develop a simple yet effective Python program that simulates a basic voting system. It ensures that only eligible users with valid voter IDs can vote and that each voter can cast only one vote. The system automates the process of vote collection, verification, and winner declaration, reducing the possibility of human error and ensuring transparency in small-scale voting operations.

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
