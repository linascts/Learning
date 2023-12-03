# Data Collections

There is Lists, Tuples, Sets and Dictionaries.

Lists are the most used for data collection, since they are mutable and flexible, we can make any changes to the list. A tuple is immutable, meaning it cannot be changed later on, which is also welcomed in some cases.

A set is good for having a linear data collection, it's unordered and will not allow duplicate elements. It's sometimes used to remove the duplicates from a list data collecion.

A dictionary is a good way for storing organized data with keys and values, i.e Name: John, Age: 15, and so on.

Note the syntax, different type of data collection uses different brackets [], (), {}.
```py

    list_data = ['History', 'Math', 'Physics', 'Geography']
    tuple_data = ('History', 'Math', 'Physics', 'Geography')
    set_data = set('History', 'Math', 'Physics', 'Geography')
    dictionary_data = {'courses': ['History', 'Math', 'Physics', 'Geography']}

```

Next, we have soem useful functions, here are some examples:
```py
    list_data = ['History', 'Math', 'Physics', 'Geography']

    # Gets the length of the list, and stores the value to a new variable
    length = len(list_data)
    # Output = 4

    # Add new value to a existing list (append)
    list_data.append('Chemistry')
    # Output = ['History', 'Math', 'Physics', 'Geography', 'Chemistry']

    # Add new value to a specific location in a existing list (insert)
    list_data.insert(0, 'Chemistry')
    # Output = ['Chemistry', 'History', 'Math', 'Physics', 'Geography']

    # Add a new list in a existing list properly (extend).
    # P.S using append with lists will add the whole list into a one element instead
    list_data2 = ['Biology', 'Art']
    list_data.extend(list_data2)
    # Output = ['History', 'Math', 'Physics', 'Geography', 'Biology', 'Art']

    # Remove a value from a existing list
    list_data.remove('Math')
    # Output = ['History', 'Physics', 'Geography']

    # Remove a value from a existing list, while also getting the value into a new variable (pop). By default it pops the last value of the list.
    popped = list_data.pop()
    # popped Output = Geography
    # list_data Output = ['History', 'Math', 'Physics']

    # Reverse the existing list
    list_data.reverse()
    # Output = ['Geography', 'Physics', 'Math', 'History']

    # Sort the existing list
    list_data.sort()
    # Output = ['Geography', 'History', 'Math', 'Physics']

    # Sort the existing list in a reverse order
    list_data.sort(reverse=True)
    # Output = ['Physics', 'Math', 'History', 'Geography']

    # Get a sorted list without sorting the source list
    sorted_list = sorted(list_data)
    # list_data Output = ['History', 'Math', 'Physics', 'Geography']
    # sorted_list Output = ['Geography', 'History', 'Math', 'Physics']

    # Get the maximum, minimum and summed values from the list
    nums = [3, 5, 1, 7, 15, 9]
    num_max = max(nums)
    num_min = min(nums)
    num_sum = sum(nums)
    # num_max Output = 15
    # num_min Output = 1
    # num_sum Output = 40

    # Get the index of a element in the list, gets an error if value not found
    list_data.index('Math')
    # Output = 1

```

Looping through lists, should be like this:
```py
    courses = ['History', 'Math', 'Physics', 'Geography']

    # simple loop through the list
    for course in courses:
        print(course)

    # loop through the list while getting the index, and starting at the second element
    for index, course in enumerate(courses, start=1):
        print(index, course)

```

String conversion, here:
```py

    courses = ['History', 'Math', 'Physics', 'Geography']

    # Converts list to string
    course_str = ', '.join(courses)
    # course_str Output = History, Math, Physics, Geography

    # Converts string to list
    new_list = course_str.split(', ')
    # new_list Output = ['History', 'Math', 'Physics', 'Geography']

```


Some useful functions for sets:
```py
    car_makes = {'Honda', 'Dodge', 'BMW', "Toyota"}
    car_makes2 = {'Suzuki', 'Lada', 'Mercedes-Benz', 'BMW', 'Honda'}

    # Search for duplicate values in different sets
    car_makes.intersection(car_makes2)
    # Output = {'BMW', 'Honda'}

    # Check what is the difference between sets (outputs values that are not in another set)
    car_makes.difference(car_makes2)
    # Output = {'Dodge', 'Toyota'}

    # Add the sets together
    car_makes.union(car_makes2)
    # Output = {'Honda', 'Dodge', 'BMW', "Toyota", 'Suzuki', 'Lada', 'Mercedes-Benz}


```

Some useful knowledge about dictionaries:
```py
    # Accessing elements in dictionaries
    # Method 1:
    print(dictionary_data['courses'])
    # Output = ['History', 'Math', 'Physics', 'Geography']
    # But if the value does not exist in the dictionary, it will throw an error That's why it's sometimes better to use Method 2

    # Method 2:
    print(dictionary_data.get['courses'])
    # Output = ['History', 'Math', 'Physics', 'Geography']
    # if the value  does not exist in the dictionary, it will return None, or can be customized if needed

    # Display from dictioanry
    dictionary_data.items()
    # Output = dict_items([('courses', ['History', 'Math', 'Physics', 'Geography'])])
    
    dictionary_data.values()
    # Output = dict_values(['History', 'Math', 'Physics', 'Geography'])

    dictionary_data.keys()
    # Output = dict_keys(['courses'])


    
    # Updating the dictioanry
    # Method 1:
    dictionary_data['name'] = 'Thomas'
    # Output = {'courses': ['History', 'Math', 'Physics', 'Geography'], 'name': 'Thomas'}

    # Method 2:
    dictionary_data.update({'name': 'Thomas', 'age': 25})
    # Output = {'courses': ['History', 'Math', 'Physics', 'Geography'], 'name': 'Thomas', 'age': 25}
    # Method 2 is better for adding more than one key and value pair at a time

    # Deleting from the dictionary
    # Method 1:
    del dictionary_data['courses']
    # Output = {}

    # Method 2:
    courses = dictionary_data.pop('courses')
    # dictionary_data Output = {}
    # courses Output = ['History', 'Math', 'Physics', 'Geography']
    # By popping instead of delete, we are eligible to store the deleted data into a variable


```

Looping through dictionaries:
```py

    for key, value in dictionary_data.items():
        print(key, value)

    # Output = courses ['History', 'Math', 'Physics', 'Geography']

```