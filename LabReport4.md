### Lab Assignment
1)  `$ ssh cs15lwi23auy@ieng6.ucsd.edu` < enter >
- switches to remote desktop
![image](https://user-images.githubusercontent.com/108198218/224517685-b64e8349-1412-40b7-8fd4-cba3aab462d6.png)

2)  `$ git clone git@github.com:cynthiazhang98/lab7.git` < enter >
- clones the forked repository into current directory
![image](https://user-images.githubusercontent.com/108198218/224517717-d09da10e-11e3-45d8-93c1-b5bc770e9c93.png)

3)  `$ cd lab7` < enter >
- changes directory into the just cloned directory
![image](https://user-images.githubusercontent.com/108198218/224517736-3ca23414-7745-472a-8610-881c13c1bfb6.png)

4)  `$ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` < enter >
- compiles all the .java files in the current directory "lab7"
![image](https://user-images.githubusercontent.com/108198218/224517749-e6fca065-e7b6-44e4-946b-dbd899c873e7.png)

5)  `$ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` < enter >
- runs the JUnit Tests of ListExamples and shows that there is 1 error
![image](https://user-images.githubusercontent.com/108198218/224517934-376c45bb-57b6-4303-aaec-14d9b45e23b6.png)

6)  `$ nano ListExamples.java` < enter >
- opens and allows you to edit everything in the .java files in the terminal
![image](https://user-images.githubusercontent.com/108198218/224517944-ee3234aa-2a9a-43f0-9162-a2a78ee8a4f1.png)
![image](https://user-images.githubusercontent.com/108198218/224517787-781dee77-71cc-4f97-ad54-8376ebc37d41.png)

7)  < down > until cursor is at or < down >x42:
![image](https://user-images.githubusercontent.com/108198218/224517974-50195da8-838a-472b-b492-322056eb7db0.png)
- < right >x11 < backspace > < 2 > index1 should be changed to index2 on line 43
  result:
  
![image](https://user-images.githubusercontent.com/108198218/224518005-b6cf97af-05f8-4af3-becf-b20ae4aa1ad7.png)


8)  `ctrl -O` < enter > `ctrl -X` < enter >
- `ctrl -O` saves the changes made `ctrl -X` exits the file. Leads you to:
![image](https://user-images.githubusercontent.com/108198218/224517944-ee3234aa-2a9a-43f0-9162-a2a78ee8a4f1.png)

9)  < up >< up >< up >< enter > 
- used to access the previous written "javac..." in step 4 to compile code again
![image](https://user-images.githubusercontent.com/108198218/224517749-e6fca065-e7b6-44e4-946b-dbd899c873e7.png)

10) < up >< up >< up >< enter >
- used to access the previous written "java..." in step 5 to run the JUnit tests again
![image](https://user-images.githubusercontent.com/108198218/224518049-734b7be3-0288-4607-8cc0-a6be2fea1b88.png)

11) `$ git add .` < enter >
- used to stage the changes just made.
![image](https://user-images.githubusercontent.com/108198218/224518081-7ef88be9-94de-4a9c-8d32-f98cae3ce9e3.png)

12) `$ git commit -m "ListExample changes"` < enter >
- commits the changes made to the local git repository
![image](https://user-images.githubusercontent.com/108198218/224518084-95dea7ed-becf-4470-93bd-3ecdc067731c.png)

13) `$ git push origin main` <enter> <enter password>
- pushes changes to the remote git repository
![image](https://user-images.githubusercontent.com/108198218/224518106-f021ab9f-578d-490c-80c7-f80b04bcd2e7.png)

Done Yay.

