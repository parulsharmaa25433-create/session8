# Bug Notes — Session 8

## 1. Average Calculation Bug

**Bug evidence:**
- Expected average for `[80, 90, 100]`: `90.0`
- Actual result: `135.0`
- For `[40]`, the program raised `ZeroDivisionError`.

**Cause:** The function divided the total by `len(marks) - 1` instead of `len(marks)`.

**Fix:**
```python
return total / len(marks)
```

## 2. Passing Boundary Bug

**Bug evidence:**
- Expected: `is_passing(40)` returns `True`.
- Actual: It returned `False`.

**Cause:** The code used `>` instead of `>=`.

**Fix:**
```python
if mark >= PASS_MARK:
```

## 3. Grade Ordering Bug

**Bug evidence:**
- Expected: `get_grade(95)` returns `"Distinction"`.
- Actual: It returned `"First"`.

**Cause:** The `average >= 60` condition was checked before `average >= 90`.

**Fix:** Check the Distinction condition first, followed by First and Second.

## Final Verification

The original implementation failed tests during the RED stage. After fixing the implementation without changing the test expectations, all nine tests passed during the GREEN stage.
