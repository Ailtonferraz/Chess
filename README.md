
### ♟️ Chess Game System Project :


### First class: Position</b>

### Checklist:

- Class Position [public]</b>


- <b>OOP Topics:</b>

    - Associations
  
    - Encapsulation / Constructors
    
    - ToString (Object / overriding)
    
-----------------------

<b>Starting to implement Board and Piece</b>

<b>Checklist:</b>

- Classes Piece, Board [public]</b>


- <b>OOP Topics:</b>

    - Associations
  
    - Encapsulation / Access Modifiers
   
- <b>Data Structures Topic:</b>

    - Associations

-----------------------


<b>Chess layer and printing the board</b>

![image](https://user-images.githubusercontent.com/29154134/219197840-5decb61a-d178-44a8-9336-be9b4858cc2b.png)


### Checklist:

- Methods: Board.Piece(row, column) and Board.Piece(position)

- Enum Chess.Color

- Class Chess.ChessMatch [public]

- Class ChessConsole.UI

- <b>OOP Topics:</b>

    - Enumerations
  
    - Encapsulation / Access Modifiers
    
    - Inheritance / Downcasting

    - Static members / Layers pattern
 
 - <b>Data Structures Topics:</b>

    - Matrix
   
-----------------------

<b>Placing pieces on the board</b>

### Checklist:

- Method: Board.PlacePiece(piece, position)

- Classes: Rook, King [public]

- Method: ChessMatch.InitialSetup

- Class ChessConsole.UI

- <b>OOP Topics:</b>

    - Overriding
  
    - Inheritance 
    
    - Polymorphism (ToString)
  
-----------------------

<b>BoardException and defensive programming</b>

### Checklist:

- Class BoardException [public]

- Methods: Board.PositionExists, Board.ThereIsAPiece

- Implement defensive programming in Board methods

- <b>OOP Topics:</b>

    - Exceptions
  
    - Constructors (a string must be informed to the exception) 
    
-----------------------


<b>ChessException and ChessPosition</b>

### Checklist:

- Class ChessException [public]

- Class ChessPosition [public]

- Refactor ChessMatch.InitialSetup

- <b>OOP Topics:</b>

    - Exceptions
  
    - Encapsulation

    - Constructors (a string must be informed to the exception)

    - Overriding
    
    - Static members
    
    - Layers pattern
    
-----------------------

<b>Moving pieces</b>

### Checklist:

- Method Board.RemovePiece

- Method UI.ReadChessPosition

- Method ChessMatch.PerformChessMove

    - Method ChessMatch.MakeMove
    
    - Method ChessMatch.ValidadeSourcePosition
    
- Write basic logic on Program.cs

- <b>OOP Topics:</b>

    - Exceptions
  
    - Encapsulation

-----------------------  
  
 ## Handling exceptions and clearing screen
 
 ## Clear screen using Java:
 
 ```java
// https://stackoverflow.com/questions/2979383/java-clear-the-console
public static void clearScreen() {
System.out.print("\033[H\033[2J");
System.out.flush();
}
```
## Checklist:

  - ChessException
  - InputMismatchException

-----------------------

## Possible moves of a piece

![image](https://user-images.githubusercontent.com/29154134/219222653-00ddf5b4-4804-41c0-9ab5-65101459013d.png)



### Checklist:

- Methods in Piece:

- PossibleMoves [abstract]

   - PossibleMove
   
   - IsThereAnyPossibleMove

- Basic PossibleMove implementation for Rook and King

- Update ChessMatch.ValidadeSourcePosition

- <b>OOP Topics:</b>

    - Abstract method / class
  
    - Exceptions
    
-----------------------
