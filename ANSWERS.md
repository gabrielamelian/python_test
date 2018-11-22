
2. What is a possible problem with the following Python function?

```py
def update_list(new_value, current_list=[]):
    current_list.append(new_value)
    return current_list
```

The issue is that python will initialize the default value for arguments once
at the function declaration, not every time the function is called. This means
that on each subsequent call to the `update_list` function we will be modifying
the same list.

In order to avoid this issue we have to use `None` to define default arguments
like this:

```py
def update_list(new_value, current_list=None):
    if current_list is None:
        current_list = []
    current_list.append(new_value)
    return current_list
```

4. What are `*args` and `**kwargs` in Python, and why would we use them?

5. What is the difference between a list and a tuple in Python?

6. What does the Python built-in zip function do?

7. What does a “with” statement do in Python?

8. Explain one common use of a one way hash algorithm

The advantage of a one way hash funtion is that it allows to create a hash code
(fixed string of digits) easily which would be hard to revert by any means. By
revert I mean convert back into the original message using the hash. This makes
it very useful for use in authentication as it is a safer way to create digital
signatures.
