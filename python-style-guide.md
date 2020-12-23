# Python3 styling guidelines

### Naming

**variables** and **functions** are to follow snake_case_convention. Examples:
- `variable_name`
- `function_name(argument_name)`
- `num_of_vowels`
- `get_num_of_vowels()`
- `reverse_string()`

**Classes** and **Exceptions** should be named using UpperCamelCase convention. Examples:
- `EmployeeRecords`
- `FactoryStaff`
- `Vehicles`

**Constants** should be names using all-caps snake_case. Examples:
- `MATH_PI`
- `GOLDEN_RATIO`

**Note**: Private members (both data members and methods) of a Class or interface, should have an underscore 
before their names, since Python doesn't support private members. Examples:
- `_employee_name`
- `_employee_age`

### '__main__'

Every single python module should have the following clause: `if __name__ == '__main__':`
Read more about this construct [here](https://stackoverflow.com/questions/419163/what-does-if-name-main-do)

### import statements

Statements of this type are **forbidden**: `from this import something`.  
imports should be in this format only: `import this`  
import of whole module, instead of specific part is recommended for readability and coherence.

### Global variables

**Don't** use global variables. They should be avoided as much as possible.

### Comprehensions and generators

Allowed only if the expression is simple.

### lambda expressions

Okay to use for single lines. Longer lambda expressions should be broken into a nested function.

### Conditionals

Conditions like:
- `value = 5 if something == true else 10`
- `is_true = 'yes' if is_satisfied(condition) else 'no'` are allowed, provided they fit in a single line.  

**if** should not have parentheses, unless order of expressions is to be enforced. Example:
- `if (condition):    # Not allowed`
- `if condition:    # Allowed`

### method param: self

The first argument for each class method **should be** `self`.

### Semicolons

**Strictly not allowed**

### looping

No parantheses around loop conditions, unless required for expression ordering. Examples
- `while (condition):    # Not Allowed`
- `while condition:    # Allowed`


### Indentation

Code blocks should be indented exactly **4 spaces**. Set your tab to 4-space length, if not set already.

### Blank Spaces

- 2 blank lines between a class and another class or a function and another function.

  ```python
  class SomeClass:
    # Code here


  class SomeOtherClass:
    # Code here
  ```

- 1 blank line between class definition and first method, and between two methods of the same class.

  ```python
  class SomeClass:

    def __init__(self):
      # do something

    def some_function():
      # do something
  ```

- No blank lines between function definition and function body.

  ```python
  def some_function():
      some_val = 4
  ```

- There has to be a space after each comma.

- There has to be a space before and after **binary operators** only. Don't put spaces in the slice operators.

### Comments and docstrings

- Each python source should have a top-level [docstring](https://www.python.org/dev/peps/pep-0257/), explaining the program or module, like this:

  ```python
  """This program is intended for providing multiple string related functionalities.

  Further description about the program here.
  """
  ```

- Each function should have a one-liner docstring before the function body, **iff** its purpose is not self explanatory. Example:

  ```python
  def some_function():
    """Does something and retuns a list"""
    # Function Body Here
  ```

- Each class should have its own multi-line docstring describing the class's behaviour and **attributes**.

  ```python
  class Person:
      """A class to describe a person.

      Attributes :-
      name_first: first name of the person (str)
      name_list: last name of the person (str)
      age: age of the person (int)
      phone: contact of the person (str)
      """
      
      # Class Body here
  ```

- One-line comments like `# calculate y using x` should be used where necessary.
