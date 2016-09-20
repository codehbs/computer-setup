# Computer Set-Up Instructions - Windows

## Citation
This guide was originally created by [DevBootcamp](http://devbootcamp.com/) for its students in 2015.

## Learning Competencies
By the end of this lesson, you should be able to:
- Install technologies from the command line
- Understand what a package manager is and why it is helpful

## Summary
You will need to have your computer set up with the following tools for CODE. Make sure to go through this guide step-by-step. You'll need to have each of these technologies installed to have a smooth start to CODE and your future career!

Here is the instructions for getting your windows environment set up. We will be installing:

- Chocolatey
- Sublime
- Ruby
- Rspec
- Node
- Git
- SQLite
- Postgresql

## Releases
(i.e. directions - each release is necessary for the next release, so be sure to do everything in the order specified for all challenges)

## Release 0: Download Sublime Text

Download and follow instructions from [their site](http://www.sublimetext.com). Make sure to move it to your applications folder. You can choose to download either Sublime Text 2 or 3.

If you have done this correctly, you should be able to open files from the command prompt using `subl "filename"` now.

You don't have to purchase your license right away, you can "cancel" out of the dialog box as many times as you would like, but it is good practice to buy a license after you decide you like it. (Since eventually you're hoping to get paid for writing programs, you want to pay it forward in advance.)

## Release 1: Install Chocolatey
Now lets install our package manager to get the libraries we need.

Chocolatey works like howbrew for mac or apt-get for linux. We download this program and say:

"Chocolatey, download Ruby!" or "Chocolatey, download Nodejs!"

Chocolatey takes care of downloading and installing these programs for you. It even adjusts your PATH variable to make sure the OS accesses these languages correctly.

The first step is to install chocolatey, it can be found [here](http://chocolatey.org/).

Navigate to your root directory C:/ for cmd.exe or PS:/ if you are using powershell and run one of these commands.

```shell
cmd.exe
 C:/ @powershell -NoProfile -ExecutionPolicy unrestricted -Command "iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin
 ```

For the Powershell Users. Note that you do not want to run both of these, just use whichever relates to which terminal you use.

 ```shell
Powershell
PS:/ iex ((new-object net.webclient).DownloadString('https://chocolatey.org/install.ps1'))
```

It will give you a message to say that chocolatey has finished installing and your cursor will be under your control again. Now we can start installing packages. You can search a list of all the available for chocolatey on their website [Chocolatey packages](http://chocolatey.org/packages).

## Release 2: Install Ruby

Now we can install our first package, Ruby. In your root directory type:

```shell
C:/ choco install  ruby
```

This will install Ruby 2.1.5, type ruby -v, if you get an output that declares your Ruby version, you are good to go!

## Release 3: Install Rspec

Rspec is a testing framework built in Ruby and is the current front runner in testing framworks. We have some test driven challenges that use rspec, so we will install it as well.

```shell
gem install rspec
```

now type:

```shell
rspec -v
```
to check your install

## Release 4: Install Node

Similar to Ruby, we just use a different command.

```shell
C:/ choco install nodejs.install
```

Restart your command line terminal.

Type node -v to test your succcess.

## Release 5: Install and Configure Git

You get the idea:

```shell
C:/ choco install git.install
```

Restart your command line terminal.

Type git --version to test your install.

Now we can configure some of the git settings.

First thing is to set your username and email you have related to your GitHub account

```shell
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

Then we want to set up our default git editor to sublime. Follow [these instructions](http://stackoverflow.com/questions/8951275/git-config-core-editor-how-to-make-sublime-text-the-default-editor-for-git-on/9408117#9408117).

## Release 6: Install SQLite

The DLL
```shell
C:/ choco install  sqlite
```
And the SQLite shell
```shell
C:/ choco install  sqlite.shell
```
Restart your terminal.

Type this to test:

```shell
sqlite3 -version
```

## Release 7: Set up Sublime
Create a symlink (symbolic link) to open Sublime from your console.

-[Sublime Text from the Command Line for Windows 7](http://stackoverflow.com/questions/9440639/sublime-text-from-command-line-win7)

## Release 8: Install Postgresql

Note that you will not need postgres until you work on a backend project. If you plan on making this your primary development machine, postgres is a much better option than SQLite for larger apps.

For Postgresql we will use the postgres recommended windows installation. Here is the installation page [spalsh page](http://www.postgresql.org/download/windows/) the installation page [install](http://www.enterprisedb.com/products-services-training/pgdownload#windows) and the instructions [instructions](http://www.enterprisedb.com/docs/en/9.3/pginstguide/Table%20of%20Contents.htm)

The step we don't want is using stack builder, it is unncessary for our purposes.

Here is a video that is a bit old but may be helpful for the visual learners out there [youtube](https://www.youtube.com/watch?v=-f9lke78g2U)

When finished, type:

```shell
psql -V
```

make sure its a capital V, this prints the version and exits. If you get into psql command line hit CTRL + D to exit.

NOTE: If you have trouble installing postgres, don't worry about it. You won't need it until Phase 2. We wanted to have it set up in advance when your path was all sqeakly clean and wonderful, but if you have trouble, just move on.

## Release 9: Thats all

You now have a set up environment for development! If you are interested in this kind of thing, there is a whole job created around automating server and terminal set up. It is called DevOps, they do lots of things to make software development more efficient. Check it out! [devopsreactions](http://devopsreactions.tumblr.com/)

## Congrats - you're ready to take the CODE member challenge!
Add your name and photo to the [CODE open-source website](https://github.com/codehbs/codehbs-official-homepage).
