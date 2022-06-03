GitHub: Push your first file to new repo

We created new repo in my previous post, now we will push a file for the first time.

1. Firstly enter your github account and open your repo.
   
2. Open your terminal, go to your file. 

For example I have a test file(Name: PAFNR) on my Desktop for use this post. And there is a .md file(Markdown/.md is a plain-text file format.) inside of PAFNR file.

3. You should see on terminal your file. Write `git init` command on your terminal and enter. You will create a .git file in your file. 
Terminal gives an info like that : Initialized empty Git repository in `../Desktop/PAFNR/.git/`
.git file can be hidden. Write the google 'showing hidden files on Mac / Windows / Linux'

4. Write `git add .` It adds / stages all of the files in the current directory.
To view the git status enter `git status` and you will see your file as red. Which means that your file is not staged yet. 

5. Enter `git commit -m "Write here your message"`.
   
6. In your terminal/command line, type `git remote add origin https…` 
You will get https… part from your github repo, click code and you will see HTTPS as screenshoot.
`git remote add origin https://github.com/Hvlkrs/TestMedium.git`
Connects local repository to remote one.

7. Push your branch to Github; `git push -u origin main`
   
8. Go back to the folder/repository screen on Github that you just left, and refresh it, and you should see your files there.