# Flowchart
```mermaid
flowchart TD
Start([Start]) --> declare[declare int variables for the lower and higher ends of the range, the random numnber, and the user's guess] --> lowerQ[/ask the user what they want the lower bound of their random number to be/] --> lowerInp[/get the user input for lowerNum/] --> higherQ[/ask the user what they want the higher bound of their random number to be/] --> higherInp[/get the user input for higherNum/] --> loopOne{{is higherNum larger than lowerNum?}}

loopOne -->|No| warningOne[/Tell the user to make their higher bound larger than their lower bound/] --> higherInpTwo[/get the user input for higherNum/] --> loopOne

loopOne -->|Yes| randomNum[Calculate the random number] --> guessQ[/Ask the user to guess the random number/] --> guessInp[/get the user input for guess/] --> loopTwo{{Is the guess correct?}}

loopTwo -->|No| upOrDown{is the guess higher than the random number?}
upOrDown -->|Yes| lower[/Tell the user to guess a lower number/] --> guessAgain[/get the user input for guess/] --> loopTwo
upOrDown -->|No| higher[/Tell the user to guess a higher number/] --> guessAgain

loopTwo -->|Yes| win[/Tell user that their guess was correct/] --> End([End])
```
# Description
First, the prgram asks for the user's lower and higher bounds for the random number that they will guess. If the higher bound is not larger than the lower bound, the program will ask the user to re-enter it. A random number in that range is then generated and stored. Next, the program asks the user to guess the random number. The user's guess is stored in a variable named guess and is compared to the random number. If the guess is too high, the program tells the user to guess lower, and if the guess is too low, the program tells the user to guess higher. If the guess is equal to the random number, the user wins.
