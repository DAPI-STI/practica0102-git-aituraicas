## Quick context

Small GitHub Classroom exercise: two pure helper functions to implement so unit tests pass. Keep changes limited to `src/` and preserve `test/` and `README.md` content.

## Big picture

- Purpose: educational repo to practise clone→implement→test→commit. No services, network calls or external APIs.
- Major files:
  - `src/math_ops.py` — implement `add(a, b)` (type-hinted floats).
  - `src/strings.py` — implement `shout(text)` (returns uppercase string).
  - `test/` — `test_math_ops.py`, `test_strings.py` contain pytest cases that define the required behavior.
- Design choices visible in code: small, pure functions with type hints and doctest examples inside docstrings. Implementations must match both the doctest examples and the pytest assertions.

## Developer / agent workflow (commands tested on PowerShell)

1. Create & activate a virtual environment (PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install deps:

```powershell
pip install -r requirements.txt
```

3. Run all tests (quiet):

```powershell
pytest -q
```

4. Run a single test file or test name (debug):

```powershell
pytest test/test_strings.py -q
pytest -k shout -q
```

Notes: GitHub Actions / Classroom autograding runs tests on push. Keep commits focused and atomic (example: "Implementa add y shout").

## Project-specific patterns & conventions

- Functions are tiny and pure: avoid prints, logging or side effects. Return values must match types in hints and tests.
- Docstrings include doctest examples — implement behavior consistent with those examples (they are authoritative as tests mirror them).
- Tests import public functions from `src` (e.g., `from src.math_ops import add`). Keep module names and function signatures unchanged.
- TODO markers and NotImplementedError are intentionally present in `src/` to indicate the required edits. Replace the NotImplementedError with the minimal implementation.

Specific examples to follow:
- In `src/math_ops.py` implement:
  - def add(a: float, b: float) -> float: return a + b
- In `src/strings.py` implement:
  - def shout(text: str) -> str: return text.upper()

## When tests fail — targeted debugging steps

1. Re-run the failing test with -k or the file path to isolate.
2. Compare function docstring examples with test assertions; tests are small and explicit.
3. Ensure no changes to test files; only modify `src/` files unless asked otherwise.

## Integration points & external deps

- Only external dependency is `pytest` (listed in `requirements.txt`). No other integrations.

## Editing and commit guidance for agents

- Keep edits minimal and focused: implement the TODOs, keep docstrings intact, avoid reformatting unrelated files.
- Use a concise commit message in Spanish as shown in `README.md`.

If any part of the repo intent is unclear (e.g., different target branch for push or classroom autograder settings), ask for clarifying info before making structural changes.

---

If you'd like, I can now implement the two functions and run the tests locally — shall I proceed?
