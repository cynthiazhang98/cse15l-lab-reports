## Lab Report 1
### I. Downloading VScode to your local Computer
1) Go to Visual Studio Code website: https://code.visualstudio.com/
2) On the website click the little dropdown arrow next to the "Download for Windows" button and select the right option for downloading VScode on your computer:
  ![image](https://user-images.githubusercontent.com/108198218/212444650-1e5607ba-b6d9-48e6-8884-629341686f60.png)
3) Opening the download should lead to a window that looks similar to:
  ![image](https://user-images.githubusercontent.com/108198218/212445020-9bfdaa30-b67b-4335-9191-2277ff634cb8.png)
4) Yay! You downloaded VScode!

### II. Remotely Connecting
  1) Make sure git is downloaded on your computer, if not go on website: https://gitforwindows.org/ and download git for your computer
  2) Open VScode and open a terminal with shortcut: `Ctrl` + " ` " or by clicking "Terminal" >> "New Terminal" :
  ![image](https://user-images.githubusercontent.com/108198218/212520085-a9192d66-8c27-4c2d-ab3d-57b7d0f73127.png)
  3) Open the command palette using 'Ctrl' + 'Shift' + 'P' and type "Select Default Profile" then select the "Git Bash" Option
  ![image](https://user-images.githubusercontent.com/108198218/212520190-25f18dc0-9ae2-4676-9fdd-1beb62e2e2c1.png)
  4) Now open a new Terminal and it should be in the git bash terminal and should look like:
  ![image](https://user-images.githubusercontent.com/108198218/212520265-10365005-2ed0-4c80-87c3-1a9f60c279ea.png)
  5) In the terminal type `ssh cs15lwi23zz@ieng6.ucsd.edu`
    - `cs15lwi23zz` should be replaced with your own ucsd course-specific account that you can look up in: https://sdacs.ucsd.edu/~icc/index.php. Your account should be similar to `cs15lwi23zz` but replaces "zz" with your own ID.
  
  6) If this is your first time connecting, a question asking about authenticity should pop up and just type 'yes' as the answer. 

  7) A Password request should pop up and enter your password that is linked to the account. You shouldn't see anything when typing your password and it should look:
![image](https://user-images.githubusercontent.com/108198218/212570404-0a675662-79ca-439b-b95d-18e380d44c80.png)
  8) Your screen should look similar:
![image](https://user-images.githubusercontent.com/108198218/212570640-58305114-137e-4136-9713-8fc4a6c3a9f3.png)
  9) You are now connected!

### III. Trying Commands
  1) Some commands to type in:
  - `pwd` - shows you the path of the current directory you are in.
  - `ls` - lists the content in your directory.
  - `cat` - prints all contents in a file in terminal.
  - `cd` - changes directory
  - `cd ..` - changes directory to the current directory's parent directory.
  - `cd <existing directory name>` - changes current directory to the existing directory in the current directory.
  2) Example:
![image](https://user-images.githubusercontent.com/108198218/212571490-805f40d8-4c7a-4025-b4df-e6defc038b3f.png)
`pwd` shows that you are in your current directory.
`cd ..` changes the dirctory to the class's directory.
`ls` shows all the student directories in your class directory.
  3) Example:
![image](https://user-images.githubusercontent.com/108198218/212571667-7cd2cd34-81c8-4193-b5d9-98df9a72a47b.png)
`cd ~` returns to your home directory which is you cs15lwi23zz directory. `ls` lists the files in the directory. `cat hello.txt` prints the contents in "hello.txt".
