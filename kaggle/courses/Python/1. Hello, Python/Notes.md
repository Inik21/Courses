 # A quick introduction to Python syntax, variable assignment, and numbers

 ## Hello, Python!

```
spam_amount = 0
print(spam_amount)

# Ordering Spam, egg, Spam, Spam, bacon and Spam (4 more servings of Spam)
spam_amount = spam_amount + 4

if spam_amount > 0:
    print("But I don't want ANY spam!")

viking_song = "Spam " * spam_amount
print(viking_song)
```

There's a lot to unpack here! This silly program demonstrates many important aspects of what Python code looks like and how it works. Let's review the code from top to bottom.

 ### Variable assignment

```
spam_amount = 0
```

 Here we create a variable called `spam_amount` and assign it the value of `0` using `=`, which is called the assignment operator.

 **Note:** If you've programmed in certain other languages (like Java or C++), you might be noticing some things Python doesn't require us to do here:

- we don't need to "declare" `spam_amount` before assigning to it
- we don't need to tell Python what type of value `spam_amount` is going to refer to. In fact, we can even go on to reassign `spam_amount` to refer to a different sort of thing like a string or a boolean.

### Function calls

```
print(spam_amount)
```

`print` is a Python function that displays the value passed to it on the screen. We call functions by putting parentheses after their name, and putting the inputs (or arguments) to the function in those parentheses.

### Comments and reassignments

```
# Ordering Spam, egg, Spam, Spam, bacon and Spam (4 more servings of Spam)
spam_amount = spam_amount + 4
```

The first line above is a **comment**. In Python, comments begin with the `#` symbol.

Next, we see an example of reassignment. Reassigning the value of an existing variable looks just the same as creating a variable - it still uses the `=` assignment operator.

In this case, the value we're assigning to spam_amount involves some simple arithmetic on its previous value. When it encounters this line, Python evaluates the expression on the right-hand side of the `=` (0 + 4 = 4), and then assigns that value to the variable on the left-hand side.

### Code blocks

```
if spam_amount > 0:
    print("But I don't want ANY spam!")

viking_song = "Spam Spam Spam"
print(viking_song)
```

Note how we indicated which code belongs to the `if`. "But I don't want ANY spam!" is only supposed to be printed if `spam_amount` is positive. But the latter code (like `print(viking_song)`) should be executed no matter what. How do we (and Python) know that?

The colon `:` at the end of the `if` line indicates that a new code block is starting. Subsequent lines that are indented are part of that code block.

**Note:** If you've coded before, you might know that some other languages use {curly braces} to mark the beginning and end of code blocks. Python's use of meaningful whitespace can be surprising to programmers who are accustomed to other languages, but in practice, it can lead to more consistent and readable code than languages that do not enforce indentation of code blocks.

The later lines dealing with `viking_song` are not indented with an extra 4 spaces, so they're not a part of the `if` code block. We'll see more examples of indented code blocks later when we define functions and use loops.

### Strings

The above code snippet is also our first sighting of a string in Python

Strings can be marked either by double or single quotation marks. (But because this particular string contains a single-quote character, we might confuse Python by trying to surround it with single-quotes, unless we're careful.)

### The `*` operator

```
viking_song = "Spam " * spam_amount
print(viking_song)
```

The `*` operator can be used to multiply two numbers (`3 * 3` evaluates to 9), but we can also multiply a string by a number to get a version that's been repeated that many times. Python offers a number of cheeky little time-saving tricks like this, where operators like `*` and `+` have a different meaning depending on what kind of thing they're applied to. (The technical term for this is operator overloading.)

## Numbers and arithmetic in Python

"Number" is a fine informal name for the kind of thing, but if we wanted to be more technical, we could ask Python how it would describe the type of thing that `spam_amount` is:

```
type(spam_amount)
```

It's an `int` - short for integer. There's another sort of number we commonly encounter in Python:

```
type(19.95)
```

A `float` is a number with a decimal place - very useful for representing things like weights or proportions.

`type()` is the second built-in function we've seen (after `print()`), and it's another good one to remember. It's very useful to be able to ask Python, "What kind of thing is this?".

A natural thing to want to do with numbers is perform arithmetic. We've seen the `+` operator for addition, and the `*` operator for multiplication. Python also has us covered for the rest of the basic buttons on your calculator:

<img width="449" height="287" alt="image" src="https://github.com/user-attachments/assets/663d6050-ef47-499b-b208-365305872651" />

### Order of operations

The arithmetic we learned in primary school has conventions about the order in which operations are evaluated. Some remember these by a mnemonic such as PEMDAS - Parentheses, Exponents, Multiplication/Division, Addition/Subtraction.

Python follows similar rules about which calculations to perform first. They're mostly pretty intuitive.

### Builtin functions for working with numbers

`min` and `max` return the minimum and maximum of their arguments, respectively.

```
print(min(1, 2, 3)) -> 1
print(max(1, 2, 3)) -> 3
```

`abs` returns the absolute value of an argument:

```
print(abs(32))  -> 32
print(abs(-32)) -> 32
```

In addition to being the names of Python's two main numerical types, `int` and `float` can also be called as functions which convert their arguments to the corresponding type:

```
print(float(10)) -> 10.0
print(int(3.33)) -> 3
# They can even be called on strings!
print(int('807') + 1) -> 808
```
