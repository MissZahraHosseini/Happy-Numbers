# -Happy-Numbers
# 😊 Happy Number Checker

A simple Python program to check whether a number is **happy** or not.

## 🧠 What is a Happy Number?

A **happy number** is defined by the following process:

1. Start with any positive integer.
2. Replace the number by the **sum of the squares of its digits**.
3. Repeat the process until:
   - the number becomes **1** → it's a **happy number**, or
   - it loops endlessly in a cycle that does **not include 1** → it's **not happy**.

**Example:**

19 → 1² + 9² = 82
82 → 8² + 2² = 68
68 → 6² + 8² = 100
100 → 1² + 0² + 0² = 1 ✅ (Happy)


---

## 🧩 Code Overview

```python
def is_happy(n: int) -> bool:
    seen_numbers = set()
    while n != 1 and n not in seen_numbers:
        seen_numbers.add(n)
        n = sum(int(i) ** 2 for i in str(n))
    return n == 1

🚀 Usage
Run the script directly

python happy_number.py

Expected output:

All test cases pass

🧪 Test Cases

The script includes several assertions:
Test	Input	Expected	Result
✅	19	True	Happy
✅	2	False	Not happy
✅	44	True	Happy
✅	86	True	Happy
✅	139	True	Happy
📦 Requirements

No external dependencies — works with Python 3.6+.


