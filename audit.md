# Code Audit — Session 8

## Scope

Reviewed `student_utils.py` and `test_student_utils.py` against the stated requirements.

## Audit Findings

1. **Average calculation:** The denominator must be the number of marks, not the number of marks minus one.
2. **Single-mark input:** A list containing one mark must not cause division by zero.
3. **Passing boundary:** A mark equal to `PASS_MARK` must be considered passing.
4. **Grade ordering:** Distinction must be checked before First and Second.

## Test Coverage

The test suite contains nine tests covering average calculation, the passing boundary, and grade assignment.

## Verification

The same nine tests passed after the implementation was corrected. Test expectations were not weakened to make the tests pass.

## Further Improvement

Consider adding tests for an empty marks list and grade boundary values such as 45, 60, and 90. The expected behaviour for an empty list should be specified before implementing that case.
