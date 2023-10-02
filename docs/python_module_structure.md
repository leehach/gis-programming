# Python Module Structure

While any Python file is a "module", to be both easily understood and usable, many Python developers use this specific module structure.

The structure of the module should be as follows:

```python
"""module_name: information on modules general purpose
usage as script: module_name opt1 opt2
    Explanation of how to call the module as a script, if possible
"""

# All import statements go at the top
import math, sys # etc...

# All global objects, variables, CONSTANTS, [lists], etc...
PI = 3.14159
new_england = ["Massachusetts", "Connecticut", "Rhode Island", 
               "Vermont", "New Hampshire", "Maine"]

# All active code should go in functions except for the 
# script/module conditional at the end

def func1():
    """Function docstring
    """
    # function statements

# Additional functions

# Include one controlling function named main() which is called if 
# the module is called as a script
# 
# main() should not take any parameters

def main():
    # Typical uses for main are to run or call a test or to run a 
    # significant or commonly used function from the command line

if __name__ == "__main__":
    main()
# else:
    # optionally, module initialization code in an else-block
```
