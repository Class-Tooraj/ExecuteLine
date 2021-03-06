

# EXECUTELINE

---

### What does it do?

This Module Executes your Python Program "Callable Objects" one by one.

this module speedup your program. because focused  only one object at time.

### Quick Start

First must Install library with **pip**

```shell
pip install executeline
```

after installation must be **import** this library

```python
import executeline
```

 **or** if you need only **Exeline** module

```python
from executeline import Exeline
```

Now **executeline** ready to use .

lets initialize **Exeline** Get One Arguments name **run** type **bool**

```python
execute = Exeline()		# run arguments default is True
```

> **argument run** :
>
> > **True** mean **run method** called after every add to line.
> >
> > **False** mean when the **run method** is called.

lets connected **return signal**

```python
show_me = lambda *x: print(f"PocketIndex: {x[0]}\tName: {x[1]}\tObjectName: {x[2]}\tReturnEx{x[-1]}")
execute.Return_Connect(show_me)		# Connect To Callable Object Return Signal Manager
```

now must append **Callable Objects** and **Arguments** into The **pocket**

for this you have One method with Tow **namespace**  !

```python
# Append To Pocket Method
execute.append_pocket("MyObj", dosomething, (10, 15), {'NameOnlyArgu': 'Hello', 'other': 'World'})

# Other Name For Appending To Packet
execute.to_line("MyObj", dosomething, (10, 15), {'NameOnlyArgu': 'Hello', 'other': 'World'})
```

After Appending **object** to pocket **run method** is called and execute **object** in line.

other example with **run** is **False** and use **iteration**

```python
execute = Exeline(False)	# run is False
# Append To Pocket
execute.append_pocket("MyObj", dosomething, (10, 15), {'NameOnlyArgu': 'Hello', 'other': 'World'})
# Iteration
itex = iter(execute)
# Execute first Object
ex = next(itex)
```

example wait for call **run method**

```python
# Initialize Exeline
execute = Exeline(False)	# run is False
# Connect Return Signal
show_me = lambda *x: print(f"PocketIndex: {x[0]}\tName: {x[1]}\tObjectName: {x[2]}\tReturnEx{x[-1]}")
execute.Return_Connect(show_me)
# Append To Pocket
execute.append_pocket("MyObj", dosomething, (10, 15), {'NameOnlyArgu': 'Hello', 'other': 'World'})
# Iteration
execute.run()
```

---

### Exeline Map

![image-exelinemap](https://github.com/Class-Tooraj/ExecuteLine/blob/main/exemap.png)

---



