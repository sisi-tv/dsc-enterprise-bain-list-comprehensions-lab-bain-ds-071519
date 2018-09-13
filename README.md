
# List Comprehension

Following exercises require to put the skills you've learned in the previous lesson to practice. All exercises simply require you to create a list **using list comprehension** to address the question. Let's get started. 

### Exercise 1:
Create a list of  all of the numbers from 1-100 that are divisible by 7


```python
[num for num in range(100) if num % 7 == 0]

# [0, 7, 14, 21, 28, 35, 42, 49, 56, 63, 70, 77, 84, 91, 98]
```




    [0, 7, 14, 21, 28, 35, 42, 49, 56, 63, 70, 77, 84, 91, 98]



### Exercise 2:

Create a list all of the numbers from 1-100 that have a 9 in them


```python
[num for num in range(100) if '9' in list(str(num))]

# [9, 19, 29, 39, 49, 59, 69, 79, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99]
```




    [9, 19, 29, 39, 49, 59, 69, 79, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99]



### Exercise 3:

Remove all the wovels and spaces from the string "A quick brown fox jumped over the lazy dog". Output a list with only letters from the string - minus the vowels and spaces, as shown the comments.


```python
# Use this string in your list comprehension
string = "A quick brown fox jumped over the lazy dog"
```


```python
[letter for letter in string if letter.lower() not in vowels]


# ['q',
#  'c',
#  'k',
#  'b',
#  'r',
#  'w',
#  'n',
#  'f',
#  'x',
#  'j',
#  'm',
#  'p',
#  'd',
#  'v',
#  'r',
#  't',
#  'h',
#  'l',
#  'z',
#  'y',
#  'd',
#  'g']
```




    ['q',
     'c',
     'k',
     'b',
     'r',
     'w',
     'n',
     'f',
     'x',
     'j',
     'm',
     'p',
     'd',
     'v',
     'r',
     't',
     'h',
     'l',
     'z',
     'y',
     'd',
     'g']



### Exercise 4:
Find all of the words in a string that have less than 4 letters. Use the string "A quick brown fox jumped over the lazy dog" as before.




```python
string = "A quick brown fox jumped over the lazy dog"
```


```python
[word for word in string.split() if len(word) < 4]

# ['A', 'fox', 'the', 'dog']
```




    ['A', 'fox', 'the', 'dog']



### Exercise 5:

Use a nested list comprehension to find all of the numbers from 1-25 that are divisible by any single digit besides 1 (2-9)


```python
[number for number in range(1,26) if True in [True for divisor in range(2,10) if number % divisor == 0]]

# [2, 3, 4, 5, 6, 7, 8, 9, 10, 12, 14, 15, 16, 18, 20, 21, 22, 24, 25]
```




    [2, 3, 4, 5, 6, 7, 8, 9, 10, 12, 14, 15, 16, 18, 20, 21, 22, 24, 25]



## Conclusion

So now you have a good understanding of how to write list comprehensions in different situations. IN certain situations, such list comprehensions can be used to replace (nested) for loops or lambda functions with map(), filter() and reduce(). You are encouraged to implement these in your coding practice as these would produce a neat looking code that is more efficient and easy to troubleshoot.  
