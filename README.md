# apology

This repository contains the **ASCII Apology Modulator** skill for Claude. The skill augments apology messages with a simple ASCII meter that grows as the severity of a mistake increases.

## Getting Started

1. Clone this repository and enter the skill directory:

   ```
   git clone https://github.com/paperli/apology.git
   cd apology/ascii-apology-modulator
   ```

2. (Optional) Create and activate a virtual environment.

3. Run the example script to see the meter in action:

   ```
   python scripts/apology_ascii.py
   ```

## Usage

To use the skill in your own code, import the `build_apology` function and pass a severity score between `0.0` and `1.0`:

```python
from ascii_apology_modulator.scripts.apology_ascii import build_apology

print(build_apology(0.2))
print(build_apology(0.8))
```

The severity score should reflect how far your response deviates from the user's expectations. Scores outside the range are clamped.

## Testing in Claude Code

You can test the skill within Claude’s coding environment by running the same import and function calls in a Python cell. The output will display the apology and the ASCII meter corresponding to your severity score.
