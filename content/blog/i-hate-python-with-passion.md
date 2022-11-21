+++
title = "I Hate Python with a Passion"
date = 2022-11-22
template = "blog/page.html"
draft = true

[taxonomies]
authors = ["nafkhanzam"]
+++

A bit of a background.
Now that I'm pursuing a master's degree majoring in system intelligence, I have to really focus on data science, machine learning, deep learning, natural language processing, image processing, etc.

And I found that the most used programming language for those things is Python.
I can't do anything about it. Whether I like it or not, I have to use it, since other languages do not have the libraries I need to do the researches.

## 1 What I like about Python

First, let's talk about what I like about Python.

Nothing.

## 2 What I hate about Python

### 2.1 Dynamically-typed Language

Python is a dynamically-typed language.
Which means we cannot for sure know what these variables' types are.
We would have to manually track the flow of the program by reading a lot of line of codes to understand the type possibilities the variables might have.

### 2.2 If-else

```python
enabled = 1 if user == "admin" else 0
```

As a programmer, it's **VERY** hard to follow the logic of that pattern.
Especially if the declaration is long.
When I read an if-else code, I always read the boolean evaluation first, like what's the logic behind this code, and what will it return if it's true, then if it's false.

My thought process on reading the code above is:

1. So, I'm creating a new variable called `enabled`. Wait, is that even a new variable? Or is it a reassignment? I have to check the codes above this line.
2. Ok, so it is a new variable. Now I want to understand what variable is this.
3. `1`? Hmm, okay, it's a number `1`. Maybe it's use as a counter or a boolean thingy.
4. `if user == "admin"`. Oh, so it's evaluating whether the variable `user` equals `"admin"` or not. I see. Now I kinda understand what variable `enabled` is doing.
5. `else 0`. Ok, so when user is not an admin, `enabled` will equal `0`.
6. Wait what happens if the user is not admin again?
7. \**Looks left*\*. `1`. Oh right, enabled becomes `1`.

Compare the code above with this below on Typescript.

```typescript
const enabled = user === "admin" ? 1 : 0;
```

My thought process:

1. So, I'm creating a new variable called `enabled`.
2. Ok, so it's checking whether variable `user` equals `admin` or not. Ok, now I kinda understand what variable `enabled` is doing.
3. `? 1`. Oh, so it's a ternary operator. If the user is indeed an admin, it will return `1`.
4. `: 0`. And when it's not, it will return `0`. So it's a boolean thingy. Ok, clear.

Way cleaner. The code tells the story linearly.
