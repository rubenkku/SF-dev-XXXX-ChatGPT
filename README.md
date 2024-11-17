# SF-dev-XXXX-ChatGPT

## Stockfish-dev with Enhanced Functionalities and Modifications

This is a private version of Stockfish-dev (latest Stockfish development source code) with added functionalities and slight modifications to specific areas of interest. 

The name "ChatGPT" is included because this project was made possible in part with the assistance of ChatGPT in modifying the required parts of the source code. Nevertheless, it also involves significant human effort and trial-and-error to achieve the desired outcomes.

The code for creating this modified version will not be publicly available for now, as it is under active experimentation and development. At some point, the compiled engine or one of its variants may be shared privately with supporters of the project.

## Current Changes and Added Functionalities

### Functionalities Already Implemented and Working:
- **7-man Tablebases Integration**: Moves are made instantly by querying the tablebases, and the engine chooses the best move accordingly.
- **BIN Book Support**: Added support for two BIN books with a "best move" option (true or false).
- **Enhanced BIN Polybook Functionality**:
  - Moves are picked based on their exact weight percentage (`% = move weight / sum of all move weights for that position`) when the "best move" option is set to false.
  - Added a "minimum %" threshold: moves below this percentage will not be chosen.
  - This improves book variety while maintaining controlled risk factors.
- **Enhanced Book Move Information**:
  - Include more details in the engine output about the chosen book move, such as the book it originates from and the other available moves for the position.
- **Streamlined Engine Output**:
  - Removed NNUE-related messages from every move.
  - Displayed book moves with their respective probabilities in the output.
- **"Minimum Thinking Time" Option**:
  - Ensures the engine searches for at least a specified number of milliseconds before choosing the best move.
  - Helps prevent instant 1-ply moves under time pressure.
- **More Book Slots**:
  - It has been added 4 BIN Book slots in total

### Planned Functionalities:
- **"No-Move Book" Option**:
  - A BIN book slot where, if the selected book move exists in the "no-move-book," the engine will enter MultiPV search mode to find a different move.

## Purpose and Vision

This project does not aim to create a stronger Stockfish engine but rather to add new functionalities and explore innovative ideas. All enhancements are implemented without altering the core search functions that make Stockfish the strongest chess engine.

If you're interested in testing this engine, consider showing your support in exchange for collaboration or resources you can offer. 

Thank you for reading!

