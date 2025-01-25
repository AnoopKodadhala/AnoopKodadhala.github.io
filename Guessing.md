# Guessing Game Flowchart

```mermaid
flowchart TD
    Start([Start]) --> GenerateNumber([Generating Number between 1 and 100])
    GenerateNumber --> NumberVal[Enter in a number between 1 and 100]
    NumberVal --> IsNum{Is this a number?}
    
    IsNum -- "No" --> NotInRange["This is not a number"] --> NumberVal
    IsNum -- "Yes" --> InRange{Is this number between 1 and 100?}
    InRange -- "No" --> NotInRange["This is not a valid number"] --> NumberVal
    InRange -- "Yes" --> NumCheck{Is this correct?}
    NumCheck -- "Equal" --> Correct{This Number is correct}
    Correct --> YouWin{You Win!}
    NumCheck -- "Greater Than" --> ResultHigh{This Number is too High}
    ResultHigh --> NumberVal
    NumCheck -- "Less Than" --> ResultLow{This Number is too Low}
    ResultLow --> NumberVal
```

1. The Game starts of with the computer generating a number from 1 to 100. 
2. It then takes the the users input for a number. 
3. The number is then checked to make sure its a number, if it is not it send it back to the user input stage. 
4. The Number is then checked to make sure its in range, if it is not it send it back to the user input stage. 
5. The Number is then checked to see where it compares to the generated number
   - If the Number is higher, it states that it is too high and sends the user back to the user input stage. 
   - If the Number is lower, it states that it is too low and sends the user back to the user input stage. 
   - If the Number is equal, it states that the user wins.
