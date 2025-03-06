# Create a window using an exernal file

File name : _window.py_

compile file in a venv environement :
```bash

mkdir PythonTuto
cd PythonTuto
# For linux (module venv of Python)
python3 -m venv env
# Windows
python -m venv env

#code into the env using command
# Linux
source env/bin/activate

# Window
env/Scripts/activate

```
Python Code example using Tkinter

```bash
#Linux and Window --> in venv
pip install tkinter
# Or
sudo apt install python3-tk
```

External file 
```bash 
window.py :
```

```python

import tkinter as tk

#traditional form
root = tk.Tk()
root.geometry("500x500")
root.title("Tkinter tutorial")

root.mainloop()


# My form
def createWindow(title, size):
    window = tk.Tk()
    window.geometry(size)
    window.title(title)
    return window

```

In the main script : 
```bash
main.py
```

```python

import window as win

root = win.createWindow("A Tk window", "500x500")
root.mainloop

```
