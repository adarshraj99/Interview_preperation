1. Get total number of a 'text' from a file.  by loops ,Indexing and count()
by loop:
```
def countX(x):
    word = list('1223334444444')
    count = 0
    for i in word:
        if i == x:
            count = count + 1
            continue
        else:
            continue
    print("{} occured {} times".format(x, count))


countX('4')
```

by count():
```
word = list('1223334444444')
print(word.count('4'))
```

by re.findall():
```
import re
word = '1223334444444'
x= re.findall('4',word)

print(x) #prints all the occurances of x # o/p: ['4', '4', '4', '4', '4', '4', '4']
print(len(x)) o/p: 7
```


by collections.Counter():
```
from collections import Counter
word = '1223334444444'
x = Counter(word)
print(x)

o/p: Counter({'4': 7, '3': 3, '2': 2, '1': 1})
```

By using comprehension: 





3. Palindrome or not.
4. reverse
5. Open files (Excel,word,txt) ,read ,update. Get a text number of repetations.
6. Fibbonacci number,find nth.
7. Find nth largest number.
8. remove duplicates.
9. count number of all texts repetations in a letter or statement.
10. list sorting.
11. Find prime (other) numbers.
12. Factorial of a number.
