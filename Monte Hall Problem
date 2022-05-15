import random
import numpy as np

Rounds = 1000

Wins_with_switch = [0]*Rounds
Wins_with_no_switch = [0]*Rounds

#simulating the process

for Process in range(Rounds):

    Doors = [1,2,3]
    Door_with_prize = random.randint(1,3)
    Door_chosen_by_user = random.randint(1,3)

    Door_chosen_by_host = random.randint(1,3)
    while Door_chosen_by_host==Door_chosen_by_user or Door_chosen_by_host==Door_with_prize:
        Door_chosen_by_host= random.randint(1,3)
    
    if Door_chosen_by_host==Door_with_prize:
        Wins_with_no_switch[Process]=1

    #if the user decides to switvh the door
    Door_chosen_after_switching = 6 - (Door_chosen_by_host + Door_chosen_by_user)

    if Door_chosen_after_switching == Door_with_prize:
        Wins_with_switch[Process] = 1 

print("Probability : [wins with switch]: [", np.mean(Wins_with_switch), "]")
print("Probability : [wins with no switch]: [", 1- np.mean(Wins_with_switch), "]")
