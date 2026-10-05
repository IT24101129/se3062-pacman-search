# Search Algorithms in Pac-Man

**SE3062 — Intelligent Systems | Take-Home Assignment 04**
BSc (Hons) in Computer Science, Year 3, 2026 | Faculty of Computing
Lecturer: Mr. Jeewaka Perera

## Objective

Implement classic uninformed and informed search algorithms — **DFS, BFS, Uniform Cost Search, and A\*** — and design admissible, consistent heuristics for two structured problems:
- Finding all four corners of the maze
- Eating all the food dots

This is a **group assignment (4 members)**. Everyone is individually evaluated on their understanding of the *entire* solution, not just the parts they personally wrote.

## Project Structure

| File | Role | Description |
|---|---|---|
| `search.py` | **Edit** | Search algorithms (DFS, BFS, UCS, A\*) — Q1–Q4 |
| `searchAgents.py` | **Edit** | Search-based agents & problems (CornersProblem, heuristics) — Q5–Q7 |
| `util.py` | Read only | Provides `Stack`, `Queue`, `PriorityQueue` — must be used instead of built-ins |
| `pacman.py` | Reference | Runs the game; defines `GameState` |
| `game.py` | Reference | Game logic — `AgentState`, `Agent`, `Directions`, `Grid` |
| `autograder.py` | Run | Automated testing / grading script |
| `test_cases/` | Auto-used | Test cases for each question |

> ⚠️ **Do not rename** any files, functions, or classes. The autograder imports them by name — a rename means zero marks for that question.

## Setup

```bash
conda create -n cs188 python=3.11
conda activate cs188
pip install numpy matplotlib
```

Verify the setup:
```bash
python pacman.py
```
A Pac-Man window should open, playable with arrow keys.

## Questions & Marks (Autograder — 40 marks total)

| # | Task | File | Autograder | Marks |
|---|---|---|---|---|
| Q1 | Depth First Search (`depthFirstSearch`) | `search.py` | `python autograder.py -q q1` | 4 |
| Q2 | Breadth First Search (`breadthFirstSearch`) | `search.py` | `python autograder.py -q q2` | 4 |
| Q3 | Uniform Cost Search (`uniformCostSearch`) | `search.py` | `python autograder.py -q q3` | 4 |
| Q4 | A\* Search (`aStarSearch`) | `search.py` | `python autograder.py -q q4` | 4 |
| Q5 | Finding All Corners — `CornersProblem` | `searchAgents.py` | `python autograder.py -q q5` | 8 |
| Q6 | Corners Heuristic — `cornersHeuristic` | `searchAgents.py` | `python autograder.py -q q6` | 8 |
| Q7 | Food Heuristic — `foodHeuristic` | `searchAgents.py` | `python autograder.py -q q7` | 8 |

Run everything at once: `python autograder.py`

## Team & Work Division

| Member | Name | Questions | Branch |
|---|---|---|---|
| A | _TBD_ | Q1 — DFS, Q2 — BFS | `a-dfs-bfs` |
| B | _TBD_ | Q3 — UCS, Q4 — A\* | `b-ucs-astar` |
| C | _TBD_ | Q5 — CornersProblem | `c-corners-problem` |
| D | _TBD_ | Q6 — Corners Heuristic, Q7 — Food Heuristic | `d-heuristics` |

**Rule:** Q1/Q2 and Q3/Q4 live in `search.py`; Q5–Q7 live in `searchAgents.py`. Avoid two people editing the same file at once — coordinate before starting.

Before submission, all 4 members must walk through the full merged `search.py` and `searchAgents.py` together — the individual viva tests understanding of the *whole* codebase, not just your own part.

## Git Workflow

1. Clone the repo, create your own branch off `main` (see table above).
2. Commit frequently with descriptive messages (this is graded — 10 marks).
3. Push your branch and open a Pull Request into `main`.
4. Merge one PR at a time; `git pull main` before continuing your own branch.
5. Resolve any conflicts together as a group call.
6. Run the full `python autograder.py` after everything is merged.

## Grading Breakdown (100 Marks)

| Component | Marks |
|---|---|
| Autograder Score (Q1–Q7) | 40 |
| Group Report | 10 |
| Individual Git Contribution | 10 |
| Individual Viva (Algorithm Knowledge 20 + Code Comprehension 20) | 40 |

## Report Requirements (`Report.pdf`)

For **each question Q1–Q7**, include:
- The specific functions/code blocks edited
- A screenshot of the autograder output proving the score
- A concise explanation (max 200 words/question) of logic, data structures, heuristic design

At the end of the report:
1. Public Git repository link (this repo)
2. Git contribution evidence (commit history/graph screenshots)
3. Individual contribution table (names, student IDs, tasks)
4. AI usage declaration (tool used + exact prompts, or "No AI tools were utilized")

## Submission

Submit **two** items to the course portal:
1. `Group_XX_Report.pdf` (standalone)
2. `Group_XX_Code.zip` — containing **only** `search.py` and `searchAgents.py`

## Notes

- Replace `Group_XX` with your actual group number once assigned.
- Fill in member names/IDs in the Team table above once finalized.
