Modeled after <http://www.upriss.org.uk/python/session5.html>
## Lists and List Comprehensions #

### Examples #

    zoo = ["giraffe", "crow"]               # define a list

    zoo[0]                                  # a single element

    zoo[0] = "zebra"                        # change an element

    zoo.append("marmot")                    # add element at end of list

    zoo = ["cat"] + zoo                     # add element at beginning

    type(raw_input("Type a string: "))      # returns str

    type(    input("Type a number: "))      # returns int or float

    [x for x in zoo if len(x) > 4]          # list comprehension

    zoo2 = zoo[:]                           # create a list copy

    zoo.pop()                               # delete last element

    del zoo[0]                              # delete element by index

    zoo.remove('crow')                      # delete element by value

    "abc"[::-1]                             # reverse a string: "cba"
                                            # Unspecified range takes all; step value of -1 reverses.
### Exercises #

1. Create a list that contains "Apples", "Pears", "Oranges" and "Peaches". Display the list. Ask the user for another fruit and add it to the end of the list. Display the list. Ask the user for a number and display the number back to the user and the fruit corresponding to that number (on a 1-is-first basis). Add another fruit to the beginning of the list using "+" and display the list. Display all the fruits that begin with "P", first using a for loop and then using a list comprehension.

2. Using the list above: Display the list. Remove the last fruit from the list. Display the list. Ask the user for a fruit to delete and find it and delete it. (Bonus: Multiply the list times two. Keep asking until a match is found. Once found, delete all occurrences.)

3. Using the list in item 1: Ask the user for input displaying a line like "Do you like apples?" for each fruit in the list (making the fruit all lowercase). For each "no", delete that fruit from the list. Display the list.

4. Using the list in item 1: Make a copy of the list and reverse the letters in each fruit in the copy. Delete the last item of the original list. Display the original list and the copy.

---

## Dictionaries and Sets #

### Examples #

    d = {}                                  # define a dictionary
    d = {"item": "tea", "country": "China"} # define a dictionary
    d["price"] = 1                          # add an item
    del d["price"]                          # delete an item
    d.keys()                                # list of dictionary keys
    d.values()                              # list of dictionary values
    "tea" in ["tea", "China"]               # membership...
    "coffee" in ["tea", "China"]            # or lack thereof
    hex(x)                                  # hexadecimal string for x
    [(x, x + 1) for x in range(7)]          # list comprehension of two-item tuples
    dict([(x, x + 1) for x in range(7)])    # dictionary of the previous item
    "abc".count("a")                        # count the number of occurrences of a substring
    [x for x in range(51) if x % 5 == 0]    # list comprehension for multiples of 5 under 51
    set([1,2])                              # set of items in a list
    set("Hi!")                              # set of characters in a string
    frozenset("Hi!")                        # frozen set of characters in a string
    set("Hi!").issubset(set("Hi there!"))   # the first set a subset of the second? Returns True
    set("Hi!").union(set(" there"))         # union- Returns set(['!', ' ', 'e', 'i', 'H', 'r', 't', 'h'])
    set("Hi!").intersection(set(" there"))  # intersection- Returns set([])
    x = set("Hi")                           # x is set(['i', 'H'])
    x.add("!")                              # x is set(['i', 'H', '!'])

### Exercises #

1. Create a dictionary containing name, city, and cake for Dan from Edmonds who likes German Chocolate. Display the dictionary. Delete the entry for cake. Display the dictionary. Add an entry for fruit with "Mango" and display the dictionary. Display the dictionary keys. Display the dictionary values. Display whether or not cake is a key in the dictionary (i.e. False). Display whether or not "Mango" is a value in the dictionary.

2. Using the dict constructor and a list comprehension, build a dictionary of numbers from zero to fifteen and the hexadecimal equivalent (string is fine).

3. Using the dictionary from item 1: Make a dictionary using the same keys but with the number of 'n's in each value.

4. Create sets s2, s3 and s4 that contain numbers from zero through twenty divisible 2, 3 and 4. Display the sets. Display if s3 is a subset of s2 (False) and if s4 is a subset of s2 (True).

5. Create a set with the letters in 'Python' and add 'i' to the set. Create a frozenset with the letters in 'marathon' and display the union and intersection of the two sets.
