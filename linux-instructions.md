
# Computer Set-Up Instructions - Linux

## Learning Competencies
By the end of this lesson, you should be able to:
- Install technologies from the command line
- Use package managment tools


## Summary
You will need to have your computer set up with the following tools for CODE. Make sure to go through this guide step-by-step. You'll need to have each of these technologies installed to have a smooth start to CODE and your future career!

## Releases
(i.e. directions - each release is necessary for the next release, so be sure to do everything in the order specified for all challenges)

## Release 0: Download Sublime Text
Download and follow instructions from [their site](http://www.sublimetext.com).
You can choose to download either Sublime Text 2 or 3.

After you download, create a symlink so you can open Sublime using `subl "filename"`

Enter this command into your terminal:
```shell
mkdir ~/bin && echo 'export "$HOME/bin:$PATH"' >> ~/.bash_profile' && ln -s /opt/SublimeText2/sublime_text ~/bin/subl
```
*NOTE:* If you are using Ubuntu or Ubuntu-derived distribution, use `~/.bash_rc` instead of `~/.bash_profile`/

Test it out by typing `subl .`. It should open all files in your current directory!

You don't have to purchase your license right away, you can "cancel" out of the dialog box as many times as you would like, but it is good practice to buy a license after you decide you like it. (Since eventually you're hoping to get paid for writing programs, you want to pay it forward in advance.)

## Release 1: Your Operating System
These instructions are optimized for use with Ubuntu. If you are using a different version of Linux you may have to translate as needed to your particular OS.


## Release 2: Get ready for install

The first step is to update our package manager apt-get. This will be done using this command:

```shell
sudo apt-get update
```

If that went without error you can now get curl:

```shell
sudo apt-get curl
```

If that doesn't work, you may need to try:

```shell
sudo apt-get install curl
```


Now we are ready to install Rbenv

## Release 3: get Rbenv

Rbenv will be your Ruby version manager. Gems will get installed there and will use its copies of Ruby over the system Ruby. Yay!

Digital Ocean wrote a great how-to on getting Rbenv and Ruby running on Ubuntu. Follow the instructions [here](https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-on-ubuntu-12-04-lts-with-rbenv--2). This will also handle installing nodejs. Make sure that you install Ruby 2.2.1 instead of 1.9.3-p392.

Also the step to open the .bashrc and fix the path is done in Release 4 so no need to complete those steps during this release.

## Release 4: Set up your Path
First you need to clone this GitHub repository into your computer and install the files. Type each line separately:

```shell
git clone https://github.com/supertopher/dotfiles.git
cd dotfiles
./install
```
Installing these files will configure your bash profile, enable auto complete, and make RSpec display with color. Note: this will replace your current bash profile.

If the code runs properly, you will have a new line. The bash convention is to succeed silently, which means to not give a success message, only error messages.

Restart your terminal to have these changes take place.


## Release 5: Install Git

This should have been installed if you followed the digital ocean tutorial in release 3. Check by typing:

```shell
git --version
```

## Release 6: Configure Git
You then need to overwrite .gitconfig to your own username and password in GitHub. Use your name and your GitHub email address in the following format:

```shell
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

## Release 7: Set up Sublime
Now make Sublime text your preferred editor for git:
```shell
git config --global core.editor "subl -w"
```


## Release 8: Install Node
Node allows you to run Javascript in your terminal.

You should have installed this when installing Rbenv if yo used the digital ocean guide.

Test by typing:

```shell
node -v
```

You'll use this later in Phase 0.

## Release 9: Install Rspec
Type ```gem install rspec```

This will install RSpec, a Ruby testing framework.

## Release 10: Install SQLite
Install sqlite3 using apt-get

```shell
sudo apt-get install sqlite3 libsqlite3-dev

gem install sqlite3-ruby
```
type sqlite3 -version to test.

## Release 11: Install Postgres
Type the following commands one at a time:

NOTE: If you have trouble installing postgres, don't worry about it. You won't need it until Phase 2. We wanted to have it set up in advance when your path was all sqeakly clean and wonderful, but if you have trouble, just move on.

```shell
sudo apt-get install postgresql
```

follow the instructions during the install and you will be set. Check your install by typing:

```shell
psql -V
```
make sure it's a capital V, this prints the version and exits. If you get into psql command line hit CTRL + D to exit.

## Thats all

You now have a set up environment for development! If you are interested in this kind of thing, there is a whole job created around automating server and terminal set up. It is called DevOps, they do lots of things to make software development more efficient. Check it out! [devopsreactions](http://devopsreactions.tumblr.com/).

## Congrats - you're ready to take the CODE member challenge!
Add your name and photo to the [CODE open-source website](https://github.com/codehbs/codehbs-official-homepage).
