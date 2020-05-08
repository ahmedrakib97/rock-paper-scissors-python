# Rock Paper Scissor game in Python #

prompt takes an input from user through `prompt` and stores it in `user_choice` variable.

### You (user) can pick between four things  ###

    *Rock if you press `r`
    *Paper if you press `p`
    *Scissors if you press `s`
    *Quit the game if you press `r`

##### This part of the code compels the user to take an input between rock,paper or scissors #####

`    while user_choice not in ['r', 'p', 's', 'q']:
        user_choice =input(prompt) `

----

##### This part of the code defines the computer's move using `random.choice()` #####

`    if user_choice == 'q':
        break
    else:
        computer_choice = random.choice(['r', 'p', 's'])
        if computer_choice == 'r':
            move = 'rock'
        elif computer_choice == 'p':
            move = 'paper'
        else:
            move = 'scissors'
        print('Computer gives a '+ ''+ move)  `
----

##### This part of the code shows the result and stores the output until you press `'q'` #####

`        if computer_choice == user_choice:
            print('Draw!')
            draws += 1
        elif(computer_choice == 'r' and user_choice == 'p') or \
            (computer_choice == 'p' and user_choice == 's') or \
            (computer_choice == 's' and user_choice == 'r'):
            print('You win!')
            wins += 1
        else:
            print('You lost!!!')
            losses += 1  `
----
