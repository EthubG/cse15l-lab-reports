# Lab Report 4

## Step 4
![image one](Screen%20Shot%202024-02-27%20at%209.24.55%20AM.png)

Keys pressed: s s h `<space>` e t g u o @ i e n g 6 . u c s d . e d u `<enter>`

Summary: I logged onto the ieng6 machine with the `ssh` command. 

## Step 5
![image two](Screen%20Shot%202024-02-27%20at%205.01.44%20PM.png)

Keys pressed: g i t `<space>` c l o n e `<space>` `<command v>` `<enter>`

Summary: I cloned the fork of the repository from Github with the SSH URL. The SSH URL was copied onto my clipboard so `<command v>` pasted the URL. 

## Step 6
![image three](Screen%20Shot%202024-02-27%20at%205.07.12%20PM.png)

Keys pressed: c d `<space>` l `<tab>` `<enter>` b a s h `<space>` t `<tab>` `<enter>`

Summary: I changed into the lab7report directory so I could access the files in there. The `<tab>` auto completed the name of the lab7report directory. I then ran the bash test script within the directory. Again `<tab>` auto completed the name for the test.sh bash script. The bash script contains the code to compile and run the `ListExamplesTests.java` file.

## Step 7
![image four](Screen%20Shot%202024-02-27%20at%205.16.22%20PM.png)

Keys pressed: v i m `<space>` L `<tab>` . `<tab>` `<enter>` 4 3 j e x i 2 `<esc>` : w q ! `<enter>`

Summary: The keys pressed before the first enter are to enter vim for the ListExamples.java file. The first tab results in the command `vim ListExamples` because `ListExamples.java` and `ListExamplesTest.java` both exist. The tab after the period fills in `.java`. After pressing enter we enter into `vim`. The command `43j` automatically goes to the line that the error is on (moves cursor 43 lines down). Then the command `e` moves the cursor to the end of the first word. `x` deletes the `1` in `index1` and `i2` writes a `2` in its place. `esc` exits the inserting mode and `:wq! <enter>` saves the code and exits `vim`. 

## Step 8
![image five](Screen%20Shot%202024-02-27%20at%205.23.19%20PM.png)

Keys pressed: b a s h `<space>` t `<tab>` `<enter>`

Summary: I ran the bash script that contains the code to compile and run the `ListExamplesTests.java` file. `<tab>` auto completes the name for the test.sh bash script.

## Step 9
![image six](Screen%20Shot%202024-02-27%20at%205.31.18%20PM.png)

Keys pressed: g i t `<space>` a d d `<space>` L `<tab>` `<enter>` g i t `<space>` c o m m i t `<enter>` i i n d e x 1 `<space>` e r r o r `<space>` f i x e d `<esc>` : w q ! `<enter>` g i t `<space>` p u s h `<enter>`

Summary: First I added the new ListExamples.java with `git add`. Again I used `<tab>` to autocomplete the name of the file. Then I used `git commit` to commit the change on the file, and entered the commit message `index1 error fixed`. The first `i` is to go into insertion mode for `vim`. Then I saved the commit message and exited `vim` with `:wq!`. Finally I pushed the changed to github with the `git push` command.
