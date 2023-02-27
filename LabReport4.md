### Lab Assignment
1)  `$ ssh cs15lwi23auy@ieng6.ucsd.edu` < enter >
- switches to remote desktop

2)  `$ git clone git@github.com:cynthiazhang98/lab7.git` < enter >
- clones the forked repository into current directory

3)  `$ cd lab7` < enter >
- changes directory into the just cloned directory

4)  `$ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` < enter >
- compiles all the .java files in the current directory "lab7"

5)  `$ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` < enter >
- runs the JUnit Tests of ListExamples and shows that there is 1 error

6)  `$ nano ListExamples.java` < enter >
- opens and allows you to edit everything in the .java files in the terminal

7)  *make changes to file
- index1 should be changed to index2 on line 43

8)  `ctrl -O` < enter > `ctrl -X` < enter >
- `ctrl -O` saves the changes made `ctrl -X` exits the file.

9)  < up >< up >< up >< enter > 
- used to access the previous written "javac..." in step 4 to compile code again

10) < up >< up >< up >< enter >
- used to access the previous written "java..." in step 5 to run the JUnit tests again

11) `$ git add .` < enter >
- used to stage the changes just made.

12) `$ git commit -m "ListExample changes"` < enter >
- commits the changes made to the local git repository

13) `$ git push origin main` <enter>
- pushes changes to the remote git repository
  
Done Yay.

