
# 📘 Module 3 Cheat Sheet — Loops, Strings, and Recursion
Crash Course on Python (Coursera)

## 🟦 WHILE LOOPS
A while loop repeats code as long as a condition is True.

```python
x = 0
while x < 5:
    print(x)
    x += 1
```

### Infinite Loops
Occurs when the loop condition never becomes False.

```python
while x > 0:
    print(x)  # x never changes
```

Fix with variable updates, stronger conditions, or `break`.

```python
while True:
    if done:
        break
```

---

## 🟦 FOR LOOPS & range()

```python
for i in range(5):
    print(i)
```

### range(start, stop, step)
- start: included (default 0)
- stop: excluded (required)
- step: increment (default 1)

Examples:
```python
range(5)        # 0–4
range(2, 7)     # 2–6
range(0, 11, 2) # even numbers
range(5, 0, -1) # countdown
```

---

## 🟦 COMMON FOR LOOP ERRORS

❌ Integers are not iterable:
```python
for x in 25:
    print(x)
```

✅ Correct:
```python
for x in range(25):
    print(x)

for x in [25]:
    print(x)
```

Strings are iterable character-by-character:
```python
for c in "Barry":
    print(c)
```

---

## 🟦 NESTED FOR LOOPS

```python
for left in range(7):
    for right in range(left, 7):
        print(left, right)
```

Pairing example:
```python
for a in teams:
    for b in teams:
        if a != b:
            print(a, "vs", b)
```

⚠️ Nested loops multiply runtime.

---

## 🟦 STRINGS, SLICING, JOINING

Strings are immutable sequences.

```python
text = "Hello"
text[0]    # 'H'
text[-1]   # 'o'
```

### Slicing
```python
text[:3]
text[3:6]
text[-4:]
```

### Joining
```python
" ".join(["Hello", "World"])
"Hello" + " " + "World"
```

Phone number formatting:
```python
def format_phone(p):
    return "(" + p[:3] + ") " + p[3:6] + "-" + p[-4:]
```

---

## 🟦 RECURSION

A function that calls itself.

```python
def factorial(n):
    if n < 2:
        return 1
    return n * factorial(n-1)
```

### Rules
- Must have a base case
- Must progress toward it
- Python recursion limit ≈ 1000

Best for recursive structures like directories or group hierarchies.

---

## 🧠 QUICK COMPARISON

| Use Case | Best Tool |
|-------|-----------|
| Unknown repetitions | while loop |
| Known sequences | for loop |
| Tree-like data | recursion |
| List filtering | list comprehensions |
