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
