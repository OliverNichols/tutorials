---
title: 'Python Data Types'
---

## Notes
Data is classified by "data types" such that we can expect certain behaviour depending on this specification.

Python is a dynamically-typed language, meaning a given variable can change type without issue - this is not true for statically-typed languages, where we might have to declare the data type before setting its value.

---

**Strings (`str`)**

```py
>>> type("hello world") is str
```

<details>
<summary><strong>Formatting</strong></summary>

<details>
<summary>&nbsp;&nbsp;Single quotes (<strong><code>' '</code></strong>)</summary>

```py
>>> print('"dave" is his name')
```
```
"dave" is his name
```
</details>

<details>
<summary>&nbsp;&nbsp;Double quotes (<strong><code>" "</code></strong>)</summary>

```py
>>> print("dave's full name is \"david\"")
```
```
dave's full name is "david"
```
</details>

<details>
<summary>&nbsp;&nbsp;Triple quotes (<strong><code>""" """</code></strong>)</summary>

```py
>>> print("""dave paused for a moment...
    "hello world", he said""")
```
```
dave paused for a moment...
"hello world", he said
```
</details>

<details>
<summary>&nbsp;&nbsp;Concatenation (<strong><code>" " + " "</code></strong>)</summary>

```py
>>> name = "bort"
>>> print("hello" + name + "world")
```
```
hellobortworld
```
</details>

<details>
<summary>&nbsp;&nbsp;F-strings (<strong><code>f"{ }"</code></strong>)</summary>

```py
>>> name = "dave"
>>> age = 14
>>> print(f"{name} is about {age * 7}")
```
```
dave is about 84
```
</details>

</details>

<details>
<summary><strong>Escape Characters</strong></summary>

<details>
<summary>&nbsp;&nbsp;<strong><code>\\n</code></strong> (new lines)</summary>

```py
>>> print("hello\nworld")
```
```
hello
world
```
</details>

<details>
<summary>&nbsp;&nbsp;<strong><code>\\t</code></strong> (tabs)</summary>

```py
>>> print("hello\tworld")
```
```
hello   world
```
</details>

<details>
<summary>&nbsp;&nbsp;<strong><code>\\u</code></strong> (unicode)</summary>

```py
>>> print("\u4f60\u597d\u4e16\u754c")
```
```
你好世界
```
</details>

</details>

<details>
<summary><strong>Methods</strong></summary>

<details>
<summary>&nbsp;&nbsp;<strong><code>str.upper()</code></strong></summary>

```py
>>> print("bOrt WoRLd".upper())
```
```
BORT WORLD
```
</details>

<details>
<summary>&nbsp;&nbsp;<strong><code>str.casefold()</code></strong></summary>

```py
>>> print("bOrt WoRLd".casefold())  # or .lower()
```
```
bort world
```
</details>

<details>
<summary>&nbsp;&nbsp;<strong><code>str.title()</code></strong></summary>

```py
>>> print("bOrt WoRLd".title())
```
```
Bort World
```
</details>

<details>
<summary>&nbsp;&nbsp;<strong><code>str.count()</code></strong></summary>

```py
>>> print("bOrt WoRLd".count("O"))
```
```
1
```
</details>

<details>
<summary>&nbsp;&nbsp;<strong><code>str.replace()</code></strong></summary>

```py
>>> print("bOrt WoRLd".replace("oR", "ar"))
```
```
bOrt WarLd
```
</details>

<details>
<summary>&nbsp;&nbsp;<strong><code>str.index()</code></strong></summary>

```py
>>> print("bOrt WoRLd".index("O"))
```
```
1
```
</details>

<details>
<summary>&nbsp;&nbsp;<strong><code>str.startswith()</code></strong></summary>

```py
>>> print("bOrt WoRLd".casefold().startswith("bort"))
```
```
True
```
</details>

<details>
<summary>&nbsp;&nbsp;<strong><code>str.endswith()</code></strong></summary>

```py
>>> print("bOrt WoRLd".casefold().endswith("world"))
```
```
True
```
</details>

<details>
<summary>&nbsp;&nbsp;<strong><code>str.strip()</code></strong></summary>

```py
>>> print("   bOrt WoRLd ".strip())
```
```
bOrt WoRLd
```
</details>

</details>

---

**Integers (`int`) and Floats (`float`)**

```py
>>> type(5) is type(-5) is int
>>> type(5.0) is float
```

<details>
<summary><strong>Mathematical Operators</strong></summary>

<details>
<summary>&nbsp;&nbsp;Addition (<strong><code>x + y</code></strong>)</summary>

```py
>>> print(7 + 4)
```
</details>

<details>
<summary>&nbsp;&nbsp;Subtraction (<strong><code>x - y</code></strong>)</summary>

```py
>>> print(7 - 4)
```
```
3
```
</details>

<details>
<summary>&nbsp;&nbsp;Multiplication (<strong><code>x * y</code></strong>)</summary>

```py
>>> print(7 * 4)
```
```
28
```
</details>

<details>
<summary>&nbsp;&nbsp;Power (<strong><code>x ** y</code></strong>)</summary>

```py
>>> print(7 ** 4)
```
```
2401
```
</details>

<details>
<summary>&nbsp;&nbsp;Division (<strong><code>x / y</code></strong>)</summary>

```py
>>> print(7 / 4)
```
```
1.75
```
</details>

<details>
<summary>&nbsp;&nbsp;Division (<strong><code>x // y</code></strong>)</summary>

```py
>>> print(7 // 4)
```
```
1
```
</details>

<details>
<summary>&nbsp;&nbsp;Modulo (<strong><code>x % y</code></strong>)</summary>

```py
>>> print(7 % 4)
3
```
</details>

</details>

<details>
<summary><strong>Functions & Methods</strong></summary>

<details>
<summary>&nbsp;&nbsp;<strong><code>int()</code></strong></summary>

```py
>>> print(int("5"))
```
```
5
```
</details>

<details>
<summary>&nbsp;&nbsp;<strong><code>str.isdigit()</code></strong></summary>

```py
>>> print("5".isdigit())
```
```
True
```
</details>

<details>
<summary>&nbsp;&nbsp;<strong><code>round()</code></strong></summary>

```py
>>> print(round(1.75))
```
```
2
```
</details>

</details>

---

**Booleans (`bool`)**

```py
>>> type(True) is type(False) is bool
```


<details>
<summary><strong>Comparators</strong></summary>

<details>
<summary>&nbsp;&nbsp;Equality (<strong><code>x == y</code></strong>)</summary>

```py
>>> print((10 // 2) == 5 == 5.0 == float("5"))
```
```
True
```
</details>

<details>
<summary>&nbsp;&nbsp;Inequality (<strong><code>x != y</code></strong>)</summary>

```py
>>> print(5 != 4)
```
```
True
```
</details>

<details>
<summary>&nbsp;&nbsp;Greater Than (<strong><code>x > y</code></strong>)</summary>

```py
>>> number = int(input("give me a positive number"))
>>> print(number > 0)
```
```
give me a positive number
$ 10
True
```
```
give me a positive number
$ -1
False
```
</details>

</details>

---

## Exercises

Replace "`???`" in question 1 and write programs to solve questions 2-3.

---

**1.**
```py
>>> number = int(input("what is your number?"))
>>> number_is_even = ???
>>> if number_is_even:
>>>     out = "even"
>>> else:
>>>     out = "odd"
>>> print(???)
```
```
what is your number?
$ 8
8 is even!
```
```
what is your number?
$ 7
7 is odd!
```

---

**2. Write a program that takes a name as an input and outputs the amount of vowels found.**

```
what's your name?
$ gavin
gavin has 2 vowels!
```
```
what's your name?
$ cheesecake
cheesecake has 5 vowels!
```

<details>
<summary><strong>Extension</strong> (optional)</summary>

**Have the program also output the vowels that were found. (Don't worry about how the output for this bit is formatted.)**

```
what's your name?
$ gavin
found 'a'
found 'i'
gavin has 2 vowels!
```

</details>

---

**3. Write a program that takes the name (of an item), an amount and a price as inputs, and outputs the total price for the given amount of the item. The price inputted should always start with a £.**

```
what's the item?
$ cheesecake
how many cheesecake(s) do you want?
$ 5
how much is each cheesecake?
$ £1.95
5 cheesecake(s) costs £9.75
```

```
what's the item?
$ pizza
how many pizza(s) do you want?
$ 2
how much is each pizza?
$ £10
2 pizza(s) costs £20.00
```

<details>
<summary><strong>Extension 1</strong> (optional)</summary>

**Have the program properly tell the user if their inputs are not valid. (Take this as far as you want.)**

```
what's the item?
$ cheesecake
how many cheesecake(s) do you want?
$ bert
'bert' isn't a valid amount!
```

</details>

<details>
<summary><strong>Extension 2</strong> (optional)</summary>

**Have the program allow any currency be specified instead of £, and continue to use that currency in the final output.**

```
what's the item?
$ cheesecake
how many cheesecake(s) do you want?
$ 10
how much is each cheesecake?
$ $3
3 cheesecake(s) costs $30.00
```

```
what's the item?
$ cheesecake
how many cheesecake(s) do you want?
$ 2
how much is each cheesecake?
$ ¥10
2 cheesecake(s) costs ¥20.00
```

</details>
