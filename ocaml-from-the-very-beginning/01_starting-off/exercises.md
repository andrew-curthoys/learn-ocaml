# OftVB Exercises

## Chapter 1
### 1. What are the types of the following expressions and what do they evaluate to, and why?

17
* Type `int`; evaluates to `- : int = 17`; 17 is an integer

1 + 2 * 3 + 4
* Type `int`; evaluates to `- : int = 11`; all the operands are integers, order
of operations gets to the answer of 11

800 / 80 / 8
* Type `int`; evaluates to `- : int = 1`; this one is a little trickier, since
we are doing integer evaluations on integers the final answer will be an
integer, which will just be the whole number part of the answer. If we want to
do float operations we'll need to add a period after the operator (/.) but I
only know that from reading ahead

400 > 200
* Type `bool`; evaluates to `- : bool = true`

1 <> 1
* Type `bool`; evaluates to `- : bool = false`

true || false
* Type `bool`; evaluates to `- : bool = true`; since one of the operands is
true and the || operator is 'or' it will evaluate to true

true && false
* Type `bool`; evaluates to `- : bool = false`; the opposite of the above, since
one of the operands is false & the operator is 'and' we get false

if true then false else true
* Type `bool`; evaluates to `- : bool = true`; the first if statement evaluates
to true, hence the answer will be false

’%’
* Type `char`; evaluates to `- : char = '%'`; just reads as a character since
the operand is inside single quotes

’a’ + ’b’
* This gives us a type error since the operator was expecting an `int` but the
operands are `char`

### 2. Consider the evaluations of the expressions 1 + 2 mod 3, (1 + 2) mod 3, and 1 + (2 mod 3). What can you conclude about the + and mod operators?
* `mod` has a higher precedence than `+`, so it is evaluated first

### 3. A programmer writes 1+2 * 3+4. What does this evaluate to? What advice would you give him?
* This would evaluate to 11, it seems lby the way the input is structured that
he wanted the addition done first, to which I would suggest he put those parts
of the expression in parentheses

### 4. The range of numbers available is limited. There are two special numbers: min_int and max_int. What are their values on your computer? What happens when you evaluate the expressions max_int + 1 and min_int - 1?
* `max_int` evaluates to `- : int = 4611686018427387903` & `min_int` evaluates
to `- : int = -4611686018427387904`. When we add one to `max_int` or subtract
one from `min_int` the value overflows and wraps around to the complementing
max or min value

### 5. What happens when you try to evaluate the expression 1 / 0? Why?
* We get a divide by zero exception, this results from the mathematical
nature of division by zero, which is undefined

### 6. Can you discover what the mod operator does when one or both of the operands are negative? What about if the first operand is zero? What if the second is zero?
* First operand negative: the negative of the mod when both operands are positive
* Second operand negative: same value when both operands are positive
* Both operands negative: negative of positive mod
* First operand 0: int value of 0
* Second operand 0: division by zero exception

### 7. Why not just use, for example, the integer 0 to represent false and the integer 1 for true? Why have a separate bool type at all?
* This keeps the `bool` values explicitly bools, i.e. if you used 0 and 1, then
you'd have them defined as both `ints` and `bools`

### 8. What is the effect of the comparison operators like < and > on alphabetic values of type char? For example, what does ’p’ < ’q’ evaluate to? What is the effect of the comparison operators on the booleans, true and false?
* It returns a `bool`, which I'm guessing has to do with the value that the
char is encoded to, since `'p' < 'q'` evaluates to `true`, however `'p' < 'Q'`
evaluates to `false`
