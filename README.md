# Git Activity#
###### Prepared by: Ciprian D. Billones Jr. ######

## Setup SSH ##
1. Generating a new SSH key

  In your terminal, just type `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`. After that just press enter to create a the file `~/.ssh/id_rsa`. For the sake of this activity, we can skip working with SSH key passphrases so just press enter again twice.

2. Adding your SSH key to your Github account

  Go to your Github account, click the arrow tick at the upper right corner of the site then select settings. In the sidebar of the settings, click the SSH and GPG keys. Click the `New SSH key` button in the SSH keys table. Add a title (You can name it to the PC you are using plus the OS. For example, TL1-Linux). To get your key, type `cat ~/.ssh/id_rsa.pub`. Copy the text that appears in the terminal (Ctrl + Shift + C) then paste it in the key field in your Github. Lastly, click `Add SSH key` button.

3. Adding Github in list of authorized hosts.

  In your terminal, just type `ssh-keyscan -t rsa github.com >> ~/.ssh/known_hosts`.

## Setup Git Configurations ##
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

  ## Activity ##

  General Instruction: Find a partner. Assign person A and person B then follow the instructions given below. Use your knowledge in git to complete the activity. Also follow the known git conventions/practices discussed in class.

  1. Setting up for collaboration

    - Person A: Go to (https://github.com/CjayBillones/git-tutorial) and for the repository. After that, go to your own forked repository that can be found at `https://github.com/<Person A's username>/git-tutorial`.
    - Person A: Go to the settings of your own forked repository and add Person B as a collaborator of your forked project.
    - Person B: Go to your email and accept that invitation to collaborate.
    - Person A & B: Clone the project via SSH. You can find the link for ssh by clicking the `clone or download` button. Once you've got the link, clone it in your local machines using the terminal.
    - Person A: Run `git fetch --all`
    - Person B: Open the `pairs.txt` file and follow the instructions given there. After doing so, commit your changes and push it to the master branch. Fix any conflict that you might encounter.
    - Person A: Go to the original project (https://github.com/CjayBillones/git-tutorial)and send a `New Pull Request` to sync your repository's master branch with the owner's master branch.
