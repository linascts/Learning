# Numpy Arrays

Arrays are similar to lists in almost any way. The main differences are:

You can only use one data type on in a array, while in list you can have a mix without worry.

You can sue operations with an array, for example divide a matrix by 2. You can't do that with list, Arrays are more convenient to use when we want to do mathematical operations.

Arrays takes less memory, so if possible always use arrays.

Arrays are part of Numpy library which you need to install, while lists are built-in.

A few examples of array use:

```py

    import numpy as np
    a = np.array({3, 6, 9, 12})
    print(a/3)
    # Output = array([1, 2, 3, 4])

```