# Flowchart for the Guessing Game of the year, Numeran

```mermaid

%%{init: {'theme':'forest'}}%%

flowchart TD
    A("Start") --> B["Computer Generates Random Number = rnum"]
    B --> C["Computer Requests user input that is numerical between 1-100"]
    C --> D["User inputs number = guess"]
    D -- "Input is numeric & between 1-100" --> E{"Valid Input"}
    D -- Input is not numeric --> F{"Invalid Input, Retry"}
    F -- Retry --> D
    E -- guess > rnum --> G{"Output: Too high, 2 tries left"}
    E -- "guess == rnum" --> H{"Output: Correct! Well Done!"}
    E -- guess &lt; rnum --> I{"Output: Too high, 2 tries left!"}
    G --> K{"Computer Requests New Input = guess_2"}
    I --> K
    K -- "input is numeric and between 1-100" --> L{"Valid Input"}
    K -- "input is not numeric or between 1-100" --> M{"Invalid Entry, Retry"}
    M -- retry --> K
    H --> J("End Program")
    L -- guess_2 > rnum --> N["Too high, 1 try left!"]
    L -- "guess_2 == rnum" --> O["Correct! Well Done!"]
    L -- guess_2 &lt; rnum --> P["Too low, 1 try left!"]
    O --> Q["End Program"]
    N --> R{"Computer Requests New Input = guess_3"}
    P --> R
    R -- "input is numeric and between 1-100" --> S{"Valid Input"}
    R -- "input is not numeric or between 1-100" --> T{"Invalid Entry, Retry"}
    T -- Retry --> R
    S -- guess_2 > rnum --> U["Too high, Game Over!"]
    S -- "guess_2 == rnum" --> V["Correct! Well Done!"]
    S -- guess_2 &lt; rnum --> W["Too low, Game Over!"]
    U --> X("End Program")
    V --> X
    W --> X

```

