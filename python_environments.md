# Environment
#### Python code can be run in many different environments, with different configurations and capabilities. Code in one environment might not run in another, if they are not configured in same way. Problems with your python environment lead to frustrating learning experience, thus managing them is the first thing you want to learn.

## What is python "Environment"?

Python environments are a way to manage different dependencies and configurations for Python projects. They allow developers to isolate project dependencies from each other, preventing conflicts and ensuring reproducibility. Two common types of Python environments are bare and virtual environments.

1. **Bare Python Environment**:
   - Also known as the system Python environment, it refers to the Python interpreter and libraries installed directly on your system.
   - When you install Python on your machine, it typically comes with a set of default libraries and packages. Any additional packages you install using tools like pip are added to this system environment.
   - The main drawback of using the bare Python environment is that it lacks isolation. Changes made to the environment, such as installing or upgrading packages, affect all Python projects running on that system.

2. **Virtual Environment**:
   - A virtual environment is a self-contained directory that contains a Python interpreter and its own set of libraries and packages. It allows you to create isolated environments for different projects.
   - Virtual environments are created using tools like `virtualenv` or `venv` (built-in since Python 3.3).
   - When you activate a virtual environment, it modifies the system's PATH environment variable so that when you run Python or install packages, it operates within the isolated environment rather than the system environment.
   - Virtual environments are beneficial because they prevent dependency conflicts between projects. Each project can have its own set of dependencies, which can be specified in a `requirements.txt` file, making it easy to reproduce the environment on another machine.
   - Additionally, virtual environments are lightweight and can be easily created and deleted as needed.

In summary, while the bare Python environment is the default system environment with no isolation between projects, virtual environments provide isolation by creating separate environments for each project, ensuring dependency management and reproducibility. It is recommended to never use the bare environment. Next up we will go over how to setup virtual environment and what you need to start coding.

# Putting together a python development environment and tools
#### To write programs in python, you need python itself, a code editor/IDE and the suggested virtual environment

**Here is a list of what you need:**
1. [Python](https://www.python.org/downloads/)
2. Popular and free code editor [VSCode](https://code.visualstudio.com/download)

#### Installing Python
 After getting the installer software, there is one important thing to note: **You need to add python to your PATH environment variable. Click the small box at the bottom as you start the install. It is not highlighted as default** After that you can follow the suggestions. Start from the "Install Now". I am assuming that the user has Windows 10/11 as OS

![PythonAddToPATH.png](images%2FPythonAddToPATH.png)

#### Installing VSCode
VSCode can be installed with the default suggestions. They already include adding it to the PATH and other defaults should serve you just fine too. After the install, you can open VSCode. We will install the Python extension next.

![PythonExtensionsToVSCode.png](images%2FPythonExtensionsToVSCode.png)

*You can find the extension on the left with the "lego blocks icon"*

The python extension is just simple click install on the extensions page.

### Making your first virtual environment

First I suggest making a folder for storing your python projects. After that make one folder inside the first one and name it to "MyFirstPythonProject" or something similar.  When you have made the folder, you can open it in VSCode by clicking the top left corner "File" and then "Open Folder..."

This will open the VSCode in the desired location. Now you should open a PowerShell terminal. You can open terminal from the button "Terminal" at the top next to "Help" and choosing "New Terminal". A command line should open at the bottom of VSCode. Check that you are in the right folder in the terminal. After this, you can follow these instructions to make the virtual environment:

Making virtual environment using `venv` (Python 3 built-in):

   Navigate to the directory where you want to create your virtual environment in the command prompt and run:

   ```powershell
   python -m venv myenv
   ```

   This will create a new directory called `myenv` containing the virtual environment.

   To activate the virtual environment, run:

   ```powershell
   myenv\Scripts\activate
   ```

   You'll see `(myenv)` appear at the beginning of your command prompt, indicating that the virtual environment is active. The command has run a file myenv\Scripts\activate, where the first folder is named the same as the virtual environment. 

To deactivate the virtual environment, simply run:

```powershell
deactivate
```

This will return you to the system's default Python environment.

#### Note! The python environment needs to be active when running your code. Typical mistake is forgetting to activate the environment and trying to run the code in the bare environment. Basic python code might run just fine, but anything with dependencies like libraries might not work at all. You also need to tell the VSCode to use the python interpreter in your virtual environment that you have created for your project.

### Choosing the python interpreter

1. **Open VSCode**: Launch Visual Studio Code.

2. **Open your Python project**: Open the folder or workspace containing your Python project in VSCode.

3. **Open the Command Palette**: You can do this by pressing `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (Mac).

4. **Select Python interpreter**: Type "Python: Select Interpreter" in the Command Palette and select it when it appears in the list. Alternatively, you can navigate to `View` > `Command Palette...` from the menu bar and then type "Python: Select Interpreter".

5. **Choose interpreter from list**: VSCode will list the available Python interpreters detected on your system, including virtual environments if any. Select the interpreter you want to use for your project from the list.

6. **Confirm selection**: Once you select the interpreter, VSCode will update its settings to use the chosen interpreter for your project.

7. **Verify interpreter**: You can verify that the correct interpreter is selected by looking at the bottom-left corner of the VSCode window. It should display the Python interpreter you selected.

By following these steps, you can easily choose the Python interpreter for your project in Visual Studio Code, whether it's the system interpreter or one from a virtual environment. This ensures that your project uses the correct Python environment and dependencies.

# Now you have a proper development environment for your first project: Learning basics of python
#### At first this setup work might seem like an extra hurdle, but you will learn the importance of environments once you start working with libraries. By the way libraries refer to ready made packages of other peoples code that can be used to write your programs.


## What next?
#### Time to start learning. Here is some materials you might find useful:

### [Python Tutorial for Beginners with VS Code](https://www.youtube.com/watch?v=6i3e-j3wSf0)
*A lot of the same stuff as in this text. Does not go over the environment setup, but introduces python files and terminal*
### [Python's official tutorial](https://docs.python.org/3/tutorial/index.html)
*All the basic concepts and more*
### [W3School's Python Tutorial](https://www.w3schools.com/python/default.asp)
*A bit more friendly way to python than the official tutorial*
### Python Data Science Handbook - Jake VanderPlas.pdf
*Start reading this when you feel familiar with the basics of python. Not just for data science, despite what the name suggests*

