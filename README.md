### **Overview**

**Phoenix** is an original chess engine that implements the UCI communication protocol. The project originated as "Rises", developed in Python, and was later rewritten from scratch in C to achieve a competitive performance level.

### **Key Features**

*   **Protocol:** UCI (Universal Chess Interface).
*   **Search Algorithm:** The search is based on a Negamax framework with Alpha-Beta pruning.
*   **Search Techniques:**
    *   **Iterative Deepening:** Allows the engine to progressively deepen its analysis and manage time effectively.
    *   **Quiescence Search:** Evaluates tactically "unstable" positions to mitigate the horizon effect.
    *   **Transposition Table:** Uses Zobrist hashing to store and retrieve analyses of previously visited positions, significantly speeding up the search.
*   **Move Ordering:** To enhance the efficiency of alpha-beta pruning, the following methods are implemented:
    *   Hash Move (from the Transposition Table)
    *   MVV-LVA (Most Valuable Victim - Least Valuable Aggressor) for captures
    *   Killer Move Heuristic
    *   History Heuristic
*   **Evaluation:** The evaluation function considers material, piece-square tables (PSTs), pawn structure (doubled and isolated pawns), and king safety.

### **Future Development**

Plans for future versions include:
*   Continuous improvement of the evaluation function and move ordering.
*   Exploration and potential implementation of an NNUE (Efficiently Updatable Neural Network) architecture.

### **License and Source Code**

Phoenix is a **closed-source** engine. However, for originality and integrity verification purposes, the author is willing to provide the source code for private review by trusted testing teams (such as the CCRL team), under the strict condition that the code remains confidential.

### **Infos**

Author: Matheus (magyn)
Name: Phoenix
Version: 5
