# Lab 9 — Introduction to Continuous Integration (CI)

## Project files
- `calculator.py`: Python addition function.
- `test_calculator.py`: three automated unit tests using `unittest`.
- `.github/workflows/ci.yml`: GitHub Actions workflow that runs tests on every push.

## Run locally
Open a terminal in this folder and run:

```bash
python -m unittest -v
```

If your system uses `python3`, run:

```bash
python3 -m unittest -v
```

Expected result: all 3 tests pass and the final status is `OK`.

## Upload to GitHub
1. Create a GitHub repository named `CI_Experiment`.
2. Upload `calculator.py`, `test_calculator.py`, and the `.github/workflows/ci.yml` file, preserving the folder path.
3. Open the repository's **Actions** tab and select the **Python CI** workflow.
4. Open the latest run and inspect the test step.

## Demonstrate a failing run (as required by the lab)
Temporarily change `return a + b` in `calculator.py` to `return a - b`, save, and push the change.
The workflow should run again and the addition tests should fail.
Then restore `return a + b`, push again, and verify that the workflow passes.

Important: Do not leave the incorrect subtraction implementation in your final submission.
