# Unsolve

> "I put [Sudoku] down, flip it and reverse it.
> (ti esrever dna ti pilf ,nwod [ukoduS] tup I)."

Unsolve is a puzzle game where you start with a full sudoku board, and have to continuously eliminate elements while making sure that the solution board stays unique.

## Development
For some reason, Safari doesn't seem to work in the dev environment with SharedArrayBuffer. When developing, use Chrome. This does not effect the production build.

## Deployment
This app depends on Service Workers having access to shared memory, and therefore requires a SharedArrayBuffer. Make sure the web app is served with the following headers:
```
Cross-Origin-Embedder-Policy: require-corp
Cross-Origin-Opener-Policy: same-origin
```

## Team Project Proposal
Professor: Benjamin Cosman (bcosman)

Team Members:
Aidan Glickman (aidantg2)
Aakash Narayan (aakashn3)
Adam Aaronson (adamla3)

Project: Unsolve is a reverse Sudoku game. We plan to leverage constraint solving to create a game (and eventually a framework) where a filled Sudoku board is given at the start, and the player must eliminate numbers while keeping the solution to the board unique. As an actual game, this isn't too useful, but accompanied with a parallel search algorithm this framework could be used to generate Sudoku puzzles with a minimal number of clues. This framework can also be extended to any other game which can be modeled as a constraint satisfaction problem, which is the part which excites us the most.
