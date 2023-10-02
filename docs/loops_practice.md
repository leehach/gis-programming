In many of the following exercises, you are asked to loop through an iterator and count something. A counter must be initialized as 0 *before* the loop, and then incremented by 1 inside the loop each time some condition is met.

In many of the following exercises, you are asked to collect results in a list, string, or other data structure. The collector must be initialized as an empty list (`[]`) or an empty string (`""`) *before* the loop, and then each element added to the end of the list or string inside the loop.

# Looping through strings

For these exercises, begin by setting a variable to any word or short string:

```python
test_string = "sample"
```

For some of these examples, you should use a string that has some numbers in it, such as:

```python
test_string = "My phone number is 800.555.1212"
```

There are many functions which can do simple things like count the number of letters (`len`) or counting the number of specific letters (`str.count()`). Do *not* use these, as the purpose is to practice looping over strings.

1. Count the number of letters.
2. Count the number of "a"-s in the word.
3. Count the number of "s"-s in the word.
4. Count the number of spaces in the word.
5. Count the number of characters that are *not* lowercase letters. Import the `lowercase` constant from the `string` module to do this.
6. Count the number of characters that are *not* letters (either upper or lowercase).
7. Count the number of letters in the string that are from the first half of the alphabet, A-M (case insensitve).
8. Count the number of vowels (case insensitive). Use the string `"AEIOU"` for comparison.
9. Count the number of digits. Import the `digits` constant from the `string` module to do this.
10. Build a string that contains only the digits, and no other characters.
11. Build a string that has all the characters of the input string, but uppercases all the vowels.
12. Build a string that has all the characters of the input string, but uppercases all the vowels and lowercases all other characters.


# Looping through lists of strings

For these exercises, begin by pasting any large block of text into a string. The following is fake text, I suggest using something in a language that you can read.

```python
test_string = """
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    """
```

Convert the string to a list of individual words using the [`str.split()`](https://docs.python.org/3.6/library/stdtypes.html#str.split) method.

1. Count the number of words that begin with "a" (case insensitive).
2. Count the number of words that begin with "b" (case insensitive).
3. Count the number of words that end with "s" (case insensitive).
4. Count the number of words that end with "ed" (case insensitive).
5. Count the number of words that begin with a capital letter.
6. Count the number of one-letter words.
7. Count the number of two-letter words.
8. Count the number of words of five or more letters.
9. Build a list that contains the number of letters in each word, using the `len` function. (**Example:** `"My paragraph"` → `[2, 9]`)
10. Build a list that contains each word in a sentence of the form `"The word is ____."`.
11. Build a list where each item is a sentence with the word, and the length of the word, in the form `"____ has ____ letters."`
12. Build a list where each item is a sentence saying what letter the word starts with, capitalized, in the form `"____ starts with ____."`
13. Build a list that contains only those words that begin with "a" (case insensitive).
14. Build a list that contains only those words begin with a capital letter.
15. Build a list that contains only those words that have four letters, but uppercase all the words in the list.
16. Build a list that capitalizes all words in the input list.
17. Build a list that contains all words in the input list, but capitalizes all words of four or more letters.

# Looping through ranges

For these exercises, use the range function to generate a range of integers of any length (e.g. `range(20)`).

1. Count the number of even numbers. An even number is an integer that, when divided by two, has no remainder.
2. Count the number of odd numbers. An odd number is an integer that, when divided by two, has a remainder of one.
3. Add all the numbers in the range. Do *not* use the sum function. Instead, iterate the range, and at each step add current value to the previously accumulated value.
4. Build a list that contains all the numbers plus 10.
5. Build a list that contains all the numbers times two.
6. Build a list that contains all the numbers converted to strings.
7. Build a list that contains all the numbers plus 1 converted to strings.
8. Build a list that contains all the numbers converted to floats.
9. Assuming that the numbers are Celsius temperature measurements, build a list that converts all the numbers to Fahrenheit.
10. Build a list containing the lagged value at each position, that is, the value of the *previous* item in the range. **Do not use list slicing to accomplish this.** Iterate the range and figure out how to access the previous value at each step in the loop. If there is no previous value, use the value `None`.
11. Build a list containing the second lagged value at each position, that is, the value of the item *two steps earlier* in the range. **Do not use list slicing to accomplish this.** Iterate the range and figure out how to access the value of the second lag at each step in the loop. If there is no second lag, use the value `None`.
12. Build a list that contains the change between values by subtracting the *previous* value from the *current* value during each step in the loop. If there is no previous number, the change should be `None`.
13. The [Fibonacci sequence](https://en.wikipedia.org/wiki/Fibonacci_number) is constructed by adding the previous two terms in the sequence. The sequence starts with 0 and 1. Thus, the first few terms are 0, 1, 1, 2, 3, 5, 8, 13, … . Build a list of Fibonacci numbers by looping over the range, adding the first lag and the second lag.

For these exercises, you will build a list of the *triangle numbers*. A triangle number is the sum from 1 to *n* of a natural number:

```
1 = 1
1 + 2 = 3
1 + 2 + 3 = 6
1 + 2 + 3 + 4 = 10
1 + 2 + 3 + 4 + 5 = 15
etc.
```

Keep in mind that ranges begin at 0, so `range(3)` generates 0, 1, 2 while you want the first numbers in the list to be 1, 3, 6. Account for the zero-based counting however you want to construct triangle numbers beginning with 1.

14. Build a list of triangle numbers by iterating a range. Calculate each triangle number by using the `sum` function on an appropriate range object.
15. Build a list of triangle numbers by iterating a range. Calculate each number by adding, at each step in the loop, the *current* value to the previously accumulated value. That is, if the current value is 5, the previous triangle number is 10, so the new triangle number is 15.
16. Build a list of triangle numbers by iterating a range using a nested loop. At each step in the loop, calculate the triangle number by iterating a new range for the current value. For example, when the outer loop is at step 4, iterate `range(4)`, adding each item in the range to get the triangle number.
