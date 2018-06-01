---
title: Setting Up Python on Windows
date: 2018-03-24 14:40:23
---
Here's what you need to do to set up your Windows machine. If you already think you have Python 3 installed, please check with a staff member before completing these instructions.

1. Open [this Python download link](https://www.python.org/ftp/python/3.6.0/python-3.6.0-amd64.exe). Click "run" if prompted. Otherwise, save the file to your computer and double-click to start the installer.
2. Windows may prompt you on whether you want to run or install Python. Click **Run** or **Yes** when these prompts may appear.
3. Check the box to "Add Python 3.6 to PATH".
4. Click **Install Now**. This will also install IDLE (official Python IDE), pip (used to install Python packages), and documentation tools that will make your Python learning experience much easier. Follow the instructions to complete the installation, and click CLOSE when complete.
5. Open a command prompt (we will be doing this multiple times, so make a note of how to do this!):
  - **Windows 8 or Windows 10**: Open the Start Menu and search for "command prompt"
  - **Windows 7 or Vista**: Click on the Start menu (the Windows logo in the lower left of the screen), type `cmd` into the Search field directly above the Start menu button, and click "cmd" in the search results above the Search field.
  - **Windows XP**: Click Start menu, click "Run...", type `cmd` into the text box, and hit enter.

You now have what's called a command prompt. This command prompt is another way of navigating your computer and running programs -- just textually instead of graphically. We are going to be running Python and Python scripts from this command prompt.

3. At the command prompt (which will look something like `C:\Users\username>`, type:
  ```
  python
  ```
  You should see something that looks like this:

  ```
  Python 3.6.0 (v3.6.0:41df79263a11, Dec 23 2016, 08:06:12) [MSC v.1900 64 bit (AMD64)] on win32
  Type "help", "copyright", "credits" or "license" for more information.
  >>>
  ```
  You just started Python! The `>>>` indicates that you are at a new type of prompt -- a Python prompt. The command prompt lets you navigate your computer and run programs, and the Python prompt lets you write and run Python code interactively. If the number after Python is not 3 or greater, please tell an instructor or assistant.

4. To exit the Python shell, type `exit()` and hit enter.  You'll now be back at the Windows command prompt (the `C:\` that you saw earlier).

# Prepare a Text Editor

While you can absolutely write Python code in any text editor, it is a lot easier to use one that is aware of code content and provides relevant features. To that end, we'll be using Sublime Text 3. While there are a multitude of other options, Sublime 3 provides a good blend of simplicity and functionality.

1. [**Download Sublime Text here**](http://www.sublimetext.com/3). Install as you would any other program.
2. Be sure that you've set tabs equal to 4 spaces and the tabs to spaces setting is set to True. Add the lines below to the file under **"Preferences" -- "Settings - User"**. Make sure that it is inside the curly braces at the top of your file.
  ```
  {

      // The number of spaces a tab is considered equal to
      "tab_size": 4,

      // Set to true to insert spaces when tab is pressed
      "translate_tabs_to_spaces": true,

      ... rest of file
  }
  ```
  ```
    // The number of spaces a tab is considered equal to
    "tab_size": 4,

    // Set to true to insert spaces when tab is pressed
    "translate_tabs_to_spaces": true,
  ```

This ensures that when you hit the Tab button on your keyboard, your text editor will do the equivalent of typing four spaces.

# Accessing the Python Interpreter

Practice doing this a few times until you are comfortable entering and exiting the Python shell.

1. Open a command prompt.
2. To start Python, type `python` at the command prompt and hit enter. You should see something like this:

  ```
  Python 3.6.0 (v3.6.0:41df79263a11, Dec 23 2016, 08:06:12) [MSC v.1900 64 bit (AMD64)] on win32
  Type "help", "copyright", "credits" or "license" for more information.
  >>>
  ```

  The `>>>` indicates that you are at a Python prompt.
3. Exit the Python prompt by typing `exit()` and hitting enter. Now you're back at the Windows command prompt `C:\Users\username>`.

# Navigating From a Command Prompt

The filesystem on your computer is like a tree made up of folders (also called "directories") and files. The filesystem has a root directory called `/`, and everything on your computer lives in subdirectories of this root directory. We often navigate the filesystem graphically by clicking on graphical folders. We can do the exact same navigation from the command line.

There are two commands that we'll be using at a command prompt to navigate the filesystem on your computer:

- `dir` - lists the contents of a directory.
- `cd` - moves you into a new directory (it stands for "change directory").

Let's practice using these commands. Open a command prompt, type each of these commands and hit enter:

`dir` - *This lists all the files in your home directory.*
`cd C:\` - *This will change you into the C:\ directory.*
`dir` - *This lists the contents of the C:\ directory.*
`cd Users` - *This will change you into the Users subdirectory of the C:\ directory.*
`dir` - *You should see the names of all the files and directories in C:\Users.*
`cd ..` - *The two dots mean "parent directory", so this command moved you up to the parent directory. You were in `C:\Users`, so now you are in `C:\`, the root directory.*
`dir` - *This lists the contents of the current directory (root).*

#### Tips

- You can use Tab to auto-complete directory and file names. So from inside the root directory, if you type `cd Use` and hit Tab, the command prompt will auto-complete the directory name, and you can then hit enter to change into the `C:\Users` directory.
- The command prompt maintains a command history. You can use the up arrow to cycle through old commands. Note that the text that makes up the command prompt changes as you move around directories. The command prompt will always give the full directory path to your current directory.

#### Check Your Understanding

Answer these questions. Experiment at the command line if you need to! If you aren't sure about an answer, ask a helper.

* What directory are you in after starting a new command line prompt?
* After starting a new command line prompt, how would you get to the root directory?
* How do you check what files and directories are in your current working directory?
* If you are in directory `C:\Users`, and you want to get to `C:\Users\PythonWork\projects`, how would you do that?
* What are 2 ways to avoid typing out a full navigation command? (hint: one requires that you've run the command before)
* What is the difference between a command prompt and a Python prompt?

#### Success!

You've practiced using dir and cd to navigate your computer's filesystem from the command prompt.

# Start Learning Python!

- You may want to just quickly go through the [onboarding page](/onboarding).
- Go through this [self-directed tutorial](/day_one_tutorial/) to start learning to read and write in Python. These concepts will be reviewed in the day two lesson, along with some more advanced topics.

## Install Dependencies for the Projects

- Download the [Wordplay Project](https://github.com/PhillyPythonWorkshop/Wordplay/archive/master.zip).
- Download the [Colorwall Project](https://github.com/PhillyPythonWorkshop/Colorwall3/archive/master.zip) for Python 3.  

## Practice

Try some [practice exercises](/practice/). If you've been working on any other tutorials, feel free to go to those too, and ask an instructor to help anywhere you get stuck.

## Checkoff

When you're ready, let an instructor or assistant know. Together you will go through the following check off steps:

1. Start a new command prompt, and from that command prompt start Python 3. Then quit Python 3.
2. Create a new Python file (with a `.py` extension). In that file, type the following and save the file. From a command prompt, navigate to this file and execute that Python script.

    `print("Hello world!")`

3. Open your text editor and press `Tab`. Use the left arrow key to go back in that line and show that your text editor is using spaces to indent, not tabs.  
4. Test the Wordplay and ColorWall installations.
    - Navigate to the Wordplay directory. Run the `words1.py` script from your computer's terminal. You should see a list of words that have two consecutive letter u's.
    - Navigate to the Colorwall directory. Run the `run.py` script from your computer's terminal. You should see a grid with color animations that lasts about a minute.
5. Show the instructor a practice exercise that seemed particularly challenging and how you worked it out.
