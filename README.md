# githubTest

Git and Github - Enable git commands autocomplete adn colors on Mac

For autocomplete

1. add git-completion.bash script in your home directory
open terminal
run this command

curl https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash -o ~/.git-completion.bash


2. add following to .bash_profile. Script will run git-completion if exists

vi ~/.bash_profile

if [ -f ~/.git-completion.bash ]; then
	. ~/.git-completion.bash
fi


Enabling colors
1. check if coloring current value
git config color.ui
if return false

2. enable 
git config --global color.ui true



Branching and Merging

1. git branch "branch name"
2. git checkout "branch name"  > all changes from now on are done on the new branch
3. touch "filename" > add file name
4. git status > shows your newly added file
5. git add .
6. git commit -m "added new file"
7. git push -u origin "branch name"
8. navigate to github. Notice the newly created branch include files from master and new file added in this branch
9. merge new branch in master branch
git checkout master
git merge "branch name"
git push -u origin master >> now both branches are in sync.

10. Delete branch
git branch -d "branch name" >> this deltes only the local copy 
git push origin --delete "branch name" >> this will delete from remote



Enable email notifications in Github
Githug > Settings > Notifications > 
- Enter your email in the Address field
- Enter header
- Setup notifications

Make changes > add > commit > push >> this should trigger an email message.


Tagging
- Tagging in VCS refers to creating specific points in history for your repository / data.
- Taggin is usually done to mark release points

1. git checkout "branch name" > go to the branch you want to tag
2. git tag "branch name" v1.0
3. git tag >> to check if the tag was created

you can tag an annotated tag
git tag -a v1.1 -m "tag for release version 1.1"


Display or Show a tag
- git tag >> shows the tag
- git show v1.0 >> shows details of tag
- git tag -l "v1.*" >> shows all tags starting with V1.


Push tag to remote
- git push origin v1.0  >> command push tag to remote and create a tag under releases.
- git push --tags >> push all tags to remote

Delete tag
- git tag -d v1.0 >> deletes on local
- git tag --delete v1.1 >> delete on local

- git push origin -d v1.0 >> deletes tag in remote
- git push origin --delete v1.1 >> another way to delete a tag in remote



How to check out a tag
- in order to check out a tag, you need to create a branch from the tag and checkout the branch

- git checkout <branch name> <tag name>


How to create a tag from past commit

- git log >> retrieves the checksum number of the commit
- git tag v1.3 <checksum>
- git tag >> to verify a tag was created
- git push --tags >> push tags to remote repository



Git Merge vs Git Rebase

there are two ways to integrate changes from one branch to another

git merge > merges between two branches commits
git rebase > adds a brach to the tip of the latest commit in the master branch

git merge
- create a branch >> git branch feature
- check to branch >> git checkout feature
- create folder >> mkdir folder1
- navigate to the folder
- create file inside folder1 >> touch m1.txt
- git log >> to view the commitments

- git checkout master
- git touch m2.txt >> create a file in master as well.


So now we have two branches and each branch has different files

To MERGE between the branches 
- git checkout feature
- git merge master  >> 

