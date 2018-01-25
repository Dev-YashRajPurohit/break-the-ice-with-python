# Question 38
### Level 1

**Question:**

***With a given tuple (1,2,3,4,5,6,7,8,9,10), write a program to print the first half values in one line and the last half values in one line.***

----------------------
### Hints: Use [n1:n2] notation to get a slice from a tuple.

-------------------

**Main Author's Solution: Python 2**
```
tp = (1,2,3,4,5,6,7,8,9,10)
tp1 = tp[:5]
tp2 = tp[5:]
print tp1
print tp2
```
----------------
**My Solution: Python 3**
```
tpl = (1,2,3,4,5,6,7,8,9,10)

for i in range(0,5):
    print(tpl[i],end = ' ')
print()
for i in range(5,10):
    print(tpl[i],end = ' ')
```
**OR**
```
tpl = (1,2,3,4,5,6,7,8,9,10)
lst1,lst2 = [],[]

for i in range(0,5):
    lst1.append(tpl[i])

for i in range(5,10):
    lst2.append(tpl[i])

print(lst1)
print(lst2)
```
------------------

# Question 39
### Level 1

**Question:**

***Write a program to generate and print another tuple whose values are even numbers in the given tuple (1,2,3,4,5,6,7,8,9,10).***

----------------------
### Hints: Use "for" to iterate the tuple. Use tuple() to generate a tuple from a list.

-------------------

**Main Author's Solution: Python 2**
```
tp = (1,2,3,4,5,6,7,8,9,10)
li = list()
for i in tp:
	if tp[i]%2 == 0:
		li.append(tp[i])

tp2 = tuple(li)
print tp2
```
----------------
**My Solution: Python 3**
```
tpl = (1,2,3,4,5,6,7,8,9,10)
tpl1 = tuple(i for i in tpl if i%2 == 0)
print(tpl1)
```
**OR**
```
tpl = (1,2,3,4,5,6,7,8,9,10)
tpl1 = tuple(filter(lambda x : x%2==0,tpl))  # Lambda function returns True if found even element.
                                             # Filter removes data for which function returns False
print(tpl1)
```
----------------

# Question 40
### Level 1

**Question:**

***Write a program which accepts a string as input to print "Yes" if the string is "yes" or "YES" or "Yes", otherwise print "No".***

----------------------
### Hints: Use if statement to judge condition.

-------------------
**Main Author's Solution: Python 2**
```
s= raw_input()
if s=="yes" or s=="YES" or s=="Yes":
    print "Yes"
else:
    print "No"
```
----------------
**My Solution: Python 3**
```
s = input()
if s.lower() == 'yes':   # lower function returns all lowercase letters in the string
    print('Yes')
else:
    print("No")
```
----------------

# Question 41
### Level 1

**Question:**

***Write a program which can map() to make a list whose elements are square of elements in [1,2,3,4,5,6,7,8,9,10].***

----------------------
### Hints: Use map() to generate a list.Use lambda to define anonymous functions.

-------------------

**Main Author's Solution: Python 2**
```
li = [1,2,3,4,5,6,7,8,9,10]
squaredNumbers = map(lambda x: x**2, li)
print squaredNumbers
```
----------------
**My Solution: Python 3**
```
# No different way of code is written as the requirment is specificly mentioned in problem description

li = [1,2,3,4,5,6,7,8,9,10]
squaredNumbers = map(lambda x: x**2, li)  # returns map type object data
print(list(squaredNumbers))               # converting the object into list
```
--------------