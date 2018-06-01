---
title: Setting Up Python on Mac
date: 2018-03-24 14:40:27
---

**Important**: While Macs come with Python 2.7.x pre-installed, but because Python 2's end-of-life is just around the corner, we'll be working with Python 3 during this session so there's some light installation ahead of us. This will require administrative privileges on your computer since the Python installation is usually done to protected directories. Along the way, we'll also set up a more advanced text editor that will help us by providing some really specific programming features.

To install Python 3 for Mac:

1. Download the package available here: [**Python 3.6.0 Installation Package for Mac**](https://www.python.org/ftp/python/3.6.0/python-3.6.0-macosx10.6.pkg).
2. Double-click the downloaded file to start the installation process.
3. Click through the wizard. The default settings are all fine to use. Close the wizard when complete. By default, the package installs into a central location which will require you to enter your system username and password during the process.

## Accessing the Python Interpreter

Let's test that your installation went well by running the `python3` interpreter in the `Terminal`. Practice doing this a few times until you are comfortable entering and exiting the Python shell.

1. Open Terminal.
2. Enter the following into the terminal and press `enter`:
  ```
  $ python3
  ```
  You should then see something like this:
  ```
  Python 3.6.0 (v3.6.0:41df79263a11, Dec 22 2016, 17:23:13)
  [GCC 4.2.1 (Apple Inc. build 5666) (dot 3)] on darwin
  Type "help", "copyright", "credits" or "license" for more information.
  >>> quit()
  ```
  While inside the python interpreter:
    - The `>>>` indicates that you are at a Python prompt.
    - You can exit the Python prompt by typing `quit()` and pressing enter or by using `control+d`.

# Installing a Text Editor (Sublime)

While you can absolutely write Python code in any text editor, it is a lot easier to use one that is aware of code content and provides relevant features. To that end, we'll be using Sublime Text 3. While there are a multitude of other options, Sublime 3 provides a good blend of simplicity and functionality.

- [**Download Sublime Text 3 from here**](http://www.sublimetext.com/3)

Once downloaded, install it as you would any other OS X application. Being explicit, this means double-clicking the downloaded `dmg` file, letting it open up, and subsequently dragging the `Sublime Text` application into your `Applications` folder.

Be sure that you've set tabs equal to 4 spaces and the tabs to spaces setting is set to True.

1. Go **Sublime Text > Preferences > Settings**.
2. In the `Preferences.sublime - settings-User` file, paste the following. This ensures that when you hit the Tab button on your keyboard, your text editor will do the equivalent of typing four spaces.

  ```
  {

      // The number of spaces a tab is considered equal to
      "tab_size": 4,

      // Set to true to insert spaces when tab is pressed
      "translate_tabs_to_spaces": true,

      //... rest of file

  }
  ```

3. Save the file.

# Navigating From a Terminal

The way your computer organizes storage is called a filesystem. This filesystem is organized like a tree with folders (also called `directories`) and `files`. The highest point in the tree is the _root_ directory located at `/`. Everything you can access on your computer lives within the sub-directories of this root directory.

We often navigate the filesystem graphically (using Finder) where we can click and move deeper and across this directory tree. We can do that exact same navigation from the command line.

To do this, there are three commands that we'll be using:

- `ls` lists the contents of a directory ("what's in this folder?").
- `pwd` prints the full directory path to your current directory. It stands for "print working directory." ("where am I?")
- `cd` moves you into a new directory (it stands for "change directory").
    - `cd folder_name` - Go into `folder_name` directory.
    - `cd ..` - Go up one level in the folder heirarchy.

Let's practice using these commands.

1. Open up a Terminal (it's under `Applications/Utilities`)
2. Type each of these commands in order and hit `enter`:

  `ls` - This lists all the files in your home directory.
  `pwd` - This displays the full directory path to your current directory, which is your home directory.
  `cd /` - This will change you into the `/` (root) directory.
  `ls` - This lists the contents of the `/` (root) directory.
  `cd Users` - This will change you into the home subdirectory of the `/` (root) directory.
  `ls` - You should see a list of all the computer's users' home directories (and possibly a Shared folder).
  `pwd` - This displays the full directory path to your current directory, which in this case is `/Users`.
  `cd ..` - `..` is a relative location meaning "parent directory". You were in `/Users`, so now you have moved up to your "parent", `/`, the root directory.
  `ls` - This lists the contents of the root directory, confirming where you are.
  `cd ~` - Just like how `..` means "parent directory", `~` means "home" directory. When you execute this command, you'll change back to your home directory, where all your user files are.

#### Tips

1. You can use `tab` to auto-complete directories, files, and programs. So from inside the root directory `/`, if you type `cd Us` and press the `tab` key, the command prompt will auto-complete the directory name, and you can then hit `enter` to change into the `/Users` directory.
2. The command prompt maintains a command history. You can use the up arrow to cycle through old commands. You can also see a list of your history by using the `history` command.
3. If you'd like to open a Finder window wherever you are in the Terminal, you can use the `open .` command. Turns out `.` is another "special place" that means "the current directory". So this command opens the current directory, which OS X generally does with the help of Finder.
4. If you'd like to change to a specific location in the Terminal, and you have a Finder window open already to that place, you can type in `cd ` to the Terminal, drag the little blue folder at the top of the Finder window into the Terminal, and then press `enter`.

#### Check Your Understanding

Answer these questions. Experiment at the command line if you need to! If you aren't sure about an answer, ask a helper.

* What directory are you in after starting a new command line prompt?
* After starting a new command line prompt, how would you get to the root directory?
* How do you check what files and directories are in your current working directory?
* If you are in directory `/`, and you want to get to `/Users/Shared/`, how would you do that?
* What are 2 ways to avoid typing out a full navigation command? (hint: one requires that you've run the command before)
* What is the difference between a command prompt and a Python prompt?

#### Success!

You've practiced using `ls` and `cd` to navigate your computer's filesystem using Terminal.

# Start learning Python!

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
