# Session 8: Python Unit Testing and Debugging

## Project Overview

This project demonstrates test-driven debugging using Python's `unittest` framework.

- `student_utils.py`: Contains functions to calculate the average of marks, check passing marks, and assign grades.
- `test_student_utils.py`: Contains nine unit tests that verify the expected behaviour of these functions.
- `bug_notes.md`: Documents the identified bugs, their causes, and fixes.
- `audit.md`: Records the code review findings and suggestions for further testing.

## How to Run the Tests

Run the following command in a terminal from the project directory:

```bash
python test_student_utils.py
```

## Test Results

- Total tests: 9
- Final result: All 9 tests pass.
- Framework: Python `unittest`

## RED → FIX → GREEN

**RED:** The initial tests identified bugs in average calculation, division by zero for a single mark, the passing-mark boundary, and grade ordering.

**FIX:** The implementation in `student_utils.py` was corrected without changing the expected results in `test_student_utils.py`.

**GREEN:** The same nine tests were run again, and all nine passed successfully.

## Audit Findings and Future Improvements

The code audit recommends adding tests for:

- An empty marks list in `calculate_average`.
- Grade boundary values such as 45, 60, and 90.
- Additional edge cases to improve test coverage.

The expected behaviour for an empty marks list should be decided before implementing that case.
