# Rock-Paper-Scissors-Game

print(f"Welcome to Rock, Paper, Scissors Game! You will be playing against computer.")
def game():
    choice = input("Select from options: Rock, Paper and Scissors: ").lower().strip()

    if choice == "rock" or choice == "paper" or choice == "scissors":
        option = ["rock", "paper", "scissors"]
        import random

        computer_chooice = random.choice(option)
        print(f"Computer is selecting...", end="\n" "{computer_choice}")

        if choice == computer_chooice:
            print("It's a tie!")
            
        elif(choice == "rock" and computer_chooice == "scissors") or \
            (choice == "paper" and computer_chooice == "rock") or \
            (choice == "scissors" and computer_chooice == "paper"):
            print("You WIN!!!!")
            
        else:
            print("HAHAHAHA!! You LOSE! ")
            
    else:
        print("Invalid input. Please select between Rock, Paper and Scissors.")
        
    continue_play = input("Do you want to continue playing (yes/no): ").lower().strip()
    while True:
        if continue_play == "no":
            print("Thank you for playing Rock, Paper, Scissors Game!")
            print(f"Credits:",end="\n""Made by Shrey")
            quit()
        
        elif continue_play == "yes":
            game()
        
        else:
            print("Invalid input. Please select yes or no.")
            continue_play = input("Do you want to continue playing (yes/no): ").lower().strip()
game()
