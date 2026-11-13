# Data files (rules)

- Read every column of a spreadsheet or CSV as text. ZIP codes, phone numbers, account numbers and IDs are not numbers: they keep their leading zeros and their exact format.
- If a program changes the data, tell it so (for example in pandas: dtype=str).
- Before you say done, compare the result with the originals: row counts, and at least 5 rows side by side, including ones with leading zeros, accents or empty fields.
- Never overwrite the original files. Write the result to a new file.
- Tell me what you changed, what you dropped and why.
