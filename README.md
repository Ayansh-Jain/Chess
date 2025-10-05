# ♟️ Chess AI with Python

## 1. Introduction
Chess, known as the *"game of kings"*, is one of the most renowned strategic board games, with origins tracing back to ancient India. With over 1,500 years of history, it remains a symbol of intelligence and strategy.  

This project focuses on developing a **fully functional chess game with an AI opponent** using **Python** for its simplicity and versatility. The AI uses the **Minimax algorithm** enhanced with **Alpha-Beta pruning** for optimal decision-making. The game also features an interactive GUI built with **Tkinter**.

### 🎯 Objectives
- **Accurate Rule Implementation:** Support for all chess rules — including castling, en passant, and pawn promotion — with correct detection of checkmate and stalemate.
- **Efficient AI Decision-Making:** Implementation of Minimax with Alpha-Beta pruning for competitive play and optimized performance.
- **Dynamic State Management:** Use of efficient data structures for move history, undo/redo, and board management.
- **User-Friendly Interface:** Tkinter-based GUI with real-time move display, move history, and status updates.

---

## 2. Literature Survey

### 2.1 Existing Chess Engines
- **Stockfish:** A leading open-source engine using advanced algorithms like Monte Carlo Tree Search (MCTS). Integrated into major platforms such as Chess.com and Lichess.  
- **AlphaZero:** Developed by DeepMind, AlphaZero learns chess via reinforcement learning without human guidance — a revolutionary self-learning AI model.

### 2.2 Algorithms in Chess AI
- **Minimax Algorithm:** Evaluates possible moves for both players to choose the one maximizing the AI’s advantage.  
- **Alpha-Beta Pruning:** Reduces computation time by pruning unnecessary branches in the Minimax tree.  
- **Heuristic Evaluation:** Evaluates board states based on material score, king safety, piece mobility, and control of the center.

### 2.3 Data Structures Used
- **2D Arrays/Matrices:** Represent the 8×8 chessboard.  
- **Stacks/Linked Lists:** Manage move history for undo/redo functionality.  
- **Hash Tables:** Enable fast lookups for move validation and piece location.

---

## 3. Problem Statement

### Core Challenges
- **Accurate Rule Validation:** Handling all move types including special cases.  
- **AI Optimization:** Balancing between computation time and decision depth.  
- **User Interface:** Maintaining responsiveness and clarity during gameplay.

### Additional Challenges
- Handling special moves like castling, en passant, and promotion.  
- Balancing Minimax depth and performance.  
- Ensuring smooth, lag-free GUI responsiveness.

---

## 4. Methodology

### 4.1 System Architecture
- **Game Engine:** Manages board state, move validation, and rule enforcement (using the `chess` library).  
- **AI Module:** Uses Minimax with Alpha-Beta pruning for intelligent move decisions.  
- **GUI Module:** Built with Tkinter, handling rendering, input, and move tracking.

### 4.2 Algorithms & Data Structures

| Component | Implementation |
|------------|----------------|
| Board Representation | 8x8 Matrix (`chess.Board`) |
| Move Validation | Python `chess` library + custom rules |
| AI Decision-Making | Minimax + Alpha-Beta pruning |
| Move History | Stack (Undo/Redo) |
| Piece Lookup | Dictionary (Hash Table) |
| Game State | Object-based (turns, checks, etc.) |

---

## 5. Implementation

### 5.1 Chess Rules
- **Standard Moves:** Pawn, knight, bishop, rook, queen, and king movements.  
- **Special Moves:**  
  - **Castling:** King and rook move under specific conditions.  
  - **En Passant:** Special pawn capture under specific conditions.  
  - **Promotion:** Pawn converts to a queen (default).  
- **End Conditions:** Checkmate, stalemate, or insufficient material.

### 5.2 AI Logic
- **Minimax Algorithm:** Builds a recursive game tree of possible moves.  
- **Alpha-Beta Pruning:** Optimizes Minimax by ignoring irrelevant branches.  
- **Heuristic Evaluation:** Scores positions using piece values and positional advantages.

### 5.3 GUI Development
- **Board Rendering:** 8x8 grid built with Tkinter Canvas.  
- **Move Highlighting:** Selected squares highlighted for clarity.  
- **Side Panel:** Displays move history, player turns, and check/checkmate status.

---

## 6. Testing & Results

### 6.1 Test Cases

| Test Case | Expected Result | Actual Result |
|------------|----------------|----------------|
| Pawn Moves | Forward + Captures | ✅ Pass |
| Castling | King & Rook swap | ✅ Pass |
| Checkmate | Game ends | ✅ Pass |
| AI Move Validity | Legal moves only | ✅ Pass |

### 6.2 Performance Analysis

| Depth | Time per Move (ms) |
|--------|--------------------|
| 2 | 200 |
| 3 | 800 |
| 4 | 3000 |

**Optimization:** Alpha-Beta pruning improved search efficiency by ~40%.

---


## 7. Future Enhancements
- **Improved AI:** Integration of neural networks for self-learning AI (AlphaZero-style).  
- **Opening Books:** Precomputed databases for strong early-game performance.  
- **Multiplayer Mode:** Online player-vs-player using sockets or peer connections.  
- **Advanced Features:** Game saving/loading with PGN format for analysis.

---

## 8. Conclusion
This project successfully implements a **fully functional chess game with AI** using Python.  
### ✅ Key Achievements:
- Accurate rule enforcement (castling, en passant, promotion).  
- Optimized AI using Minimax with Alpha-Beta pruning.  
- Interactive Tkinter GUI with move highlighting and history tracking.

### 🧩 Applications:
- **Educational Tool:** Helps players learn chess rules.  
- **AI Research:** Demonstrates classical game-playing algorithms.

---

## 9. How to Run

### Install Dependencies
```bash
pip install chess
python chess_game.py
