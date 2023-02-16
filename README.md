
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

<b>Implementing possible moves of Rook</b>

### Checklist:

- Method ChessPiece.IsThereOpponentPiece(position) [protected]

- Implement Rook.PossibleMoves

- Method ChessMatch.ValidateTargetPosition
   
- <b>OOP Topics:</b>

    - Polymorphism / Encapsulation
  
    - Exceptions / access modifiers [protected]
    
-----------------------

### Printing possible moves

### Checklist:

- Method ChessMatch.PossibleMoves

- Method UI.PrintBoard [overload]

- Refactor main program logic
   
- <b>OOP Topics:</b>

    - Overloading
  
-----------------------

### Implementing possible moves of King

### Checklist:

- Method King.CanMove(position) [private]

- Implement King.PossibleMoves
   
- <b>OOP Topics:</b>

    - Encapsulation / Polymorphism
    
-----------------------

### Switching player each turn

### Checklist:

- Class ChessMatch:

    - Properties Turn, CurrentPlayer [private set]
    - Method NextTurn [private]
    - Update PerformChessMove
    - Update ValidadeSourcePosition

- Method UI.PrintMatch
   
- <b>OOP Topics:</b>

    - Encapsulation / Exceptions
    
-----------------------

### Handling captured pieces

### Checklist:

- Method UI.PrintCapturedPieces

- Update UI.PrintMatch

- Update Program logic

- Lists in ChessMatch: _piecesOnTheBoard, _capturedPieces

    - Update constructor
    
    - Update PlaceNewPiece
    
    - Update MakeMove
   
- <b>OOP Topics:</b>

    - Encapsulation / Constructors

- <b>Data Structures Topics:</b>

    - List

-----------------------

### Check logic

### Rules:

- Check means your king is under threat by at least one opponent piece

- You can't put yourself in check

## Checklist:

- Property ChessPiece.ChessPosition [get]

- Class ChessMatch:

   - Method UndoMove

   - Property Check [private set]
   - Method Opponent [private]
   - Method King(color) [private]
   - Method TestCheck
   - Update PerformChessMove
   
- Update UI.PrintMatch

-----------------------

### Checkmate logic

### Checklist:

- Class ChessMatch:
  
  - Property Checkmate [private set]
  
  - Method TestCheckmate [private]
  
  - Update PerformChessMove

- Update UI.PrintMatch

- Update Program logic

-----------------------

### Piece move count
### Checklist:

- Class ChessPiece:

  - Property MoveCount [private set]
  
  - Method IncreaseMoveCount [internal]
  
  - Method DecreaseMoveCount [internal]
  
- Class ChessMatch:

  - Update MakeMove
  
  - Update UndoMove
  
### OOP Topics:

- Encapsulation

-----------------------

### Pawn

### Checklist:

- Class Pawn

- Update ChessMatch.InitialSetup

### OOP Topics:

- Encapsulation

- Inheritance

- Polymorphism

-----------------------

### Bishop

### Checklist:

- Class Bishop

- Update ChessMatch.InitialSetup

### OOP Topics:

- Encapsulation

- Inheritance

- Polymorphism

-----------------------

### Knight

### Checklist:

- Class Knight

- Update ChessMatch.InitialSetup

### OOP Topics:

- Encapsulation

- Inheritance

- Polymorphism

-----------------------

### Queen

### Checklist:

- Class Queen

- Update ChessMatch.InitialSetup

### OOP Topics:

- Encapsulation

- Inheritance

- Polymorphism

-----------------------

### Special move - Castling

![image](https://user-images.githubusercontent.com/29154134/219432092-709b12ef-afba-43bf-abcb-bf44dc6ff3a5.png)

### Checklist:

- Update King

- Update ChessMatch.MakeMove

- Update ChessMatch.UndoMove

-----------------------

### Special move - En Passant

![image](https://user-images.githubusercontent.com/29154134/219432362-498278b1-f9bf-4dc6-8fdd-911ba74d2d0c.png)

### Checklist:

- Register a pawn which can be captured by en passant on next turn

    - Property ChessMatch.EnPassantVulnerable

    - Update ChessMatch.PerformChessMove

- Update Pawn.PossibleMoves

- Update ChessMatch.MakeMove

- Update ChessMatch.UndoMove

- Update ChessMatch.InitialSetup

-----------------------

### Special move - Promotion

![image](https://user-images.githubusercontent.com/29154134/219432788-43962aae-47e0-4b3d-9e82-4f356c3785d7.png)

### Checklist:

- Property ChessMatch.Promoted

- Update ChessMatch.PerformChessMove

- Method ChessMatch.ReplacePromotedPiece

- Update Program logic
