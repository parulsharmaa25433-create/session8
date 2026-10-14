# Session 8: Python Unit Testing and Debugging

## Project Overview

This project demonstrates test-driven debugging using Python's `unittest` framework.

- `student_utils.py`: Contains functions to calculate the average of marks, check passing marks, and assign grades.
- `test_student_utils.py`: Contains nine unit tests that verify the expected behaviour of these functions.

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

- **RED:** The tests exposed incorrect average calculations, division by zero for a single mark, an incorrect passing boundary, and incorrect grade ordering.
- **FIX:** The implementation was corrected without weakening or changing the test expectations.
- **GREEN:** The same nine tests were run again, and all passed.

This workflow demonstrates how unit tests can identify bugs and verify that corrections work as expected.
