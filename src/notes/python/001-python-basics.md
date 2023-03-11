---
title: 'Python Basics'
---

## Notes
Python is a high-level programming language.

A **high-level programming** language is "abstracted" from the computer code so it is **easier for humans to understand**.

We also learned that "memory" (or RAM) is short-term storage that gets lost when the session ends.

---

**`print()`**
```py
>>> print("hello world")
```
```
hello world
```

---

**`input()`**
```py
>>> print("hello", input("what's your name?"))
```
```
what's your name?
$ steve
hello steve
```

---

**`variable = ...`**
```py
>>> name = input("what's your name?")
>>> mood = input("how are you?")
>>> print(name, "is", mood)
```
```
what's your name?
$ dave
how are you?
$ very good
dave is very good
```

---

## Exercises

Replace "`???`" in each question.

---


**1.**
```py
>>> name = input("who are you?")
>>> print("hello", ???)
```
```
who are you?
$ zixuan
hello zixuan
```

---

**2.**
```py
>>> secret = ???
>>> if secret == "strawberry":
>>>     print("welcome!")
>>> else:
>>>     print(???)
```
```
what's the secret word?
$ strawberry
welcome!
```
```
what's the secret word?
$ pizza
go away!
```

---

**3.**
```py
>>> number = int(input("give me a number!"))
>>> print(number + 100)
```
```
give me a number!
$ ???
110
```

---

**4.**
```py
>>> weather = input("what's the weather like in england?")
>>> weather = "rain, always"
>>> print("the weather in england is", weather)
```
```
what's the weather like in england?
$ sunny
???
```

---

**5.**
```py
>>> person_1 = "ollie"
>>> person_2 = "zixuan"
>>> print(f"{person_1} has healthy food and {person_2} has unhealthy food") 
>>> dog = "dave"
>>> print(f"{dog} is on a diet")
>>> print(f"{dog} wants {persons_2}'s food anyway")
```
```
ollie has healthy food and zixuan has unhealthy food
dave is on a diet
???
```

---
