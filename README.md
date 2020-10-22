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

