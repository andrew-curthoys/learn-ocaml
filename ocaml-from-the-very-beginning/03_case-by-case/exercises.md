# OftVB Exercises

## Chapter 1
### 1. Rewrite the not function from the previous chapter in pattern matching style.
```
# let not x =
  match x with
  true -> false
|    _ -> true;;
val not : bool -> bool = <fun>
```
### 2. Use pattern matching to write a recursive function which, given a positive integer n, returns the sum of all the integers from 1 to n.
```
# let rec sum_n n =
  match n with
    1 -> 1
  | _ -> n + sum_n(n - 1);;
val sum_n : int -> int = <fun>
```

### 3. Use pattern matching to write a function which, given two numbers x and n, computes xn.
```
# let rec power x n =
  match n with
    0 -> 1
  | _ -> x * power x (n - 1);;
val power : int -> int -> int = <fun>
```

### 4. For each of the previous three questions, comment on whether you think it is easier to read the function with or without pattern matching. How might you expect this to change if the functions were much larger?
* I actually think for these simpler functions the `if ... then` structure is
easier to read, however as we get more conditionals I can see where the pattern
matching will be easier

### 5. What does match 1 + 1 with 2 -> match 2 + 2 with 3 -> 4 | 4 -> 5 evaluate to?
* This evaluates to 5, after matching 1 + 1 with 2, then matching 2 + 2 with 4
in the "other" category of the match, giving 5

### 6. There is a special pattern x..y to denote continuous ranges of characters, for example ’a’..’z’ will match all lowercase letters. Write functions islower and isupper, each of type char → bool, to decide on the case of a given letter.
```
# let islower c =
  match c with
    'a'..'z' -> true
         | _ -> false;;
```
```
# let islower c =
  match c with
    'A'..'Z' -> true
         | _ -> false;;

```