# Solutions to the tasks

### Task 1

Github repository link: https://github.com/ADHIKSHA/Timezone_to_UTC

### Task 2

Github repository link: https://github.com/ADHIKSHA/python_code

### Task 3


### Task 4
These are steps to update the fork :

1. Clone your remote fork of the repository to your local machine.\
-> git clone git@foo.bar/user/project

2. Go to the project directory in the CMD.\
-> cd project

3. Add a remote link to the original repository, named upstream.\
-> git remote add upstream git@foo.bar/project/project

4. Check for all the exisiting remote links present in your local github repository.\
-> git remote -v

   ** If you don't already have a remote link to your fork of the repository then, create a remote link called origin by using the following command. \
-> git remote add origin git@foo.bar/user/project

5. Fetch the current state of the original repository into your local repository.\
-> git fetch upstream

6. Merge the changes present between your local repository and the original repository. Here 'main' is the branch which needs to be merged with.\
-> git merge upstream/main

7. Push all the changes to your fork of the repository. This command will successfully help you to sync your fork of the repository to the original repository.\
-> git push origin main


