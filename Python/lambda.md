# Lamba

Lammda Function = Function written in 1 line using lambda keyword, it accepts any number of arguments, but only has one expression. (Let's think of it as a shortcut. Useful if needed for a short periof of time, throw-away)


```py

    double = lambda x:x * 2
    print(double(4))
    # Output = 8

    full_name = lambda first_name, last_name: first_name + " " + last_name
    print(full_name("Thomas", "Pepperoni"))
    # Output = Thomas Pepperoni

    age_check = lambda age: True if age >= 18 else False
    print(age_check(18))
    # Output = True

```