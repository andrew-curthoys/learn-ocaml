# OftVB Exercises

## Chapter 2
### 1. Write a function which multiplies a given number by ten. What is its type?
```
# let tenx x = x * 10;;
val tenx : int -> int = <fun>
```
* It is a function with an argument & output of type `int`

### 2. Write a function which returns true if both of its arguments are non-zero, and false otherwise. What is the type of your function?
```
# let non0 a b = a*b <> 0;;
val non0 : int -> int -> bool = <fun>
```
* It is a function which takes two `int`s & returns a `bool`

### 3. Write a recursive function which, given a number n, calculates the sum 1 + 2 + 3 + … + n. What is its type?
```
# let rec sum_n n =
  if n = 1 then 1 else n + sum_n (n - 1);;
val sum_n : int -> int = <fun>

```
* It is a function that takes an `int` and returns an `int`

### 4. Write a function power x n which raises x to the power n. Give its type.
```
# let rec power x n =
  if n = 0 then 1 else x * power x (n - 1);;
val power : int -> int -> int = <fun>
```
* It is a function that takes two `int`s and returns an `int`

### 5. Write a function isconsonant which, given a lower-case character in the range ’a’…’z’, determines if it is a consonant.

```
'o' || c='u');;
val isconsonant : char -> bool = <fun>

```
* It is a function that takes a `char` and returns a `bool`

### 6. What is the result of the expression  let x = 1 in let x = 2 in x + x ?
```
# let x = 1 in let x = 2 in x + x;;
Line 1, characters 4-5:
Warning 26: unused variable x.
- : int = 4
```
* I thought this was going to be an error of trying to re-define an immutable
variable, however it seems you can re-define variables if you use the `let`
keyword. This is a result of the expression evaluating to `let x = 1 in 4`,
which doesn't make sense

### 7. Can you suggest a way of preventing the non-termination of the factorial function in the case of a zero or negative argument?
* You could check if the input were greater than zero before executing the
function