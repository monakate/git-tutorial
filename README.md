# Git Activity#
###### Prepared by: Ciprian D. Billones Jr. ######

## Setup SSH ##
1. Generating a new SSH key

  In your terminal, just type `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`. After that just press enter to create a the file `~/.ssh/id_rsa`. For the sake of this activity, we can skip working with SSH key passphrases so just press enter again twice.

2. Adding your SSH key to your Github account

  Go to your Github account, click the arrow tick at the upper right corner of the site then select settings. In the sidebar of the settings, click the SSH and GPG keys. Click the `New SSH key` button in the SSH keys table. Add a title (You can name it to the PC you are using plus the OS. For example, TL1-Linux). To get your key, type `cat ~/.ssh/id_rsa.pub`. Copy the text that appears in the terminal (Ctrl + Shift + C) then paste it in the key field in your Github. Lastly, click `Add SSH key` button.

3. Adding Github in list of authorized hosts.

  In your terminal, just type `ssh-keyscan -t rsa github.com >> ~/.ssh/known_hosts`.

## Git Configurations ##
1. Setting username and password

  Make sure that you configure you git username and password before working on any project. You can accomplish this by doing the following:

  - `git config --global user.name "Your Name"`
  - `git config --global user.email "user@example.com"`

2. Setting up git over proxy connection

  If you're using a connection with proxy, aside from configuring your machine's environment proxy, you also have to setup your git's proxy by doing the following:

  - `git config --global http.proxy http://<proxy>:<port>`
  - `git config --global https.proxy https://<proxy>:<port>`

3. Changing you default editor (optional)

  If you want to modify the editor that git uses for commit messages, you can change the default editor by doing the following:

  - `git config --global core.editor "<editor-name> -w"`

  Note: Known editors are subl, atom, emacs, gedit