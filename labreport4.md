# Week 8 Lab Report

**1. Setup: Delete any existing forks of the repository you have on your account**
  (In my ieng6 account)
  cd ..
  `rm -r lab7`
  `exit`
  
  rm -r la<tab>
**2. Setup: Fork the repository**
**3. The real deal Start the timer!**
**4. Log into ieng6**
  `ssh cs15lwi23aww@ieng6.ucsd.edu`
**5. Clone your fork of the repository from your Github account**
  git clone https://github.com/sydneyzhang18/lab7
  <Cmd-C> the link of my github repository from the browser
  git clone <Cmd-V>
**6. Run the tests, demonstrating that they fail**
  `cd lab7/`
  Keys pressed: cd l<tab>
  `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java`
  `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`

**7. Edit the code file to fix the failing test**
  nano ListExamples.java
  result.add(s);
  index2 += 1;
**8. Run the tests, demonstrating that they now succeed**
  Keys pressed: <up><up><up>
  javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
  Keys pressed: <up><up><up>
  java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
**9. Commit and push the resulting change to your Github account (you can pick any commit message!)**
  git add ListExamples.java
  git commit -m "Updated"
  git push git@github.com:sydneyzhang18/lab7.git
  
  git add L<tab>.j<tab>
  git commit -m "Updated"
  <Cmd-C> the ssh link of my repository from GitHub
  git push <Cmd-V>



exit
