# Chess & Variants, written in C/C++
Chess is a two-player board game, whose current form emerged in Southern Europe during the late 15th century after evolving from the ancient Indian game, Chaturanga.
Today, chess is one of the world's most popular games, played by millions of people worldwide.

Chess is an abstract strategy game with no hidden information. It is played on a square chessboard of eight-by-eight grid.
At the start, each player (one controlling the white pieces, the other controlling the black pieces) controls sixteen pieces: one king, one queen, two rooks, two knights, two bishops, and eight pawns.
The game object is to checkmate the opponent's king, whereby the king is under immediate attack (in "check") and there is no way for it to escape. There are also several ways a game can end in a draw:
1. Stalemate: the player to move has no legal move, but is not in check;
2. Threefold repetition;
3. Dead position: no player can force a checkmate to the other;
4. 50-move rule: no pawn has been moved and no capture has been made during the previous 50 moves, the game results in draw.
5. Draw by agreement;

##Set up
- Uppercase for black, lowercase for white.
````
RNBQKBNR
PPPPPPPP
........
........
........
........
pppppppp
rnbqkbnr
````

##Basic Moves
- The following piece can and only can move to places with # sign.

- **P**awn(1) moves one step forward, and possibly two for the first move, but captures one step diagonally, for instance, both the black rooks (R).
-- Promotes when reach the final line (8 for white and 1 for black)
````
....#...
....p...
........
........
..#.....
.R#R....
..p.....
........
````

- **R**ook(5) moves any number of squares orthogonally.
````
....#...
....#...
....#...
####r###
....#...
....#...
....#...
....#...
````
- K**n**ight(3) moves to any of the closest squares that are not on the same rank, file, or diagonal.
````
........
........
..#.#...
.#...#..
...n....
.#...#..
..#.#...
........
````
- **B**ishop(3) moves any number of squares diagonally.
````
#.......
.#.....#
..#...#.
...#.#..
....b...
...#.#..
..#...#.
.#.....#
````
- **Q**ueen(9) combines the power of a rook and bishop.
````
.#..#..#
..#.#.#.
...###..
####q###
...###..
..#.#.#.
.#..#..#
#...#...
````
- **K**ing moves one square in any direction, in case of not being captured.
````
........
........
........
........
...###..
...#k#..
...###..
........
````
## Check and Checkmate
With a king under immediate attack, the player is **in check**, whose legal moves are the only ones that rid the king of immediate attack. This can involve:
- Capturing the checking piece;
- interposing a piece between the checking piece and the king;
- moving the king to a square where it is not under attack.
Castling is impermissible in response to a check.

The object of the game is to checkmate the opponent: leave the opponent's king in check, without legal way to rid it.
It is never legal for a player to make a move that puts or leaves the player's own king in check.

##Castling
Once in every game, each king can make a special move, known as castling. Castling consists of moving the king two squares along the player's first rank toward a rook on the same rank, and then placing the rook on the last square that the king crossed.

Castling is permissible if the following conditions are met:[1]

Neither the king nor the rook has previously moved during the game.
There are no pieces between the king and the rook.
The king is not in check, and will not pass through or land on any square attacked by an enemy piece.
Castling is still permitted if the rook is under attack, or if the rook crosses an attacked square.
