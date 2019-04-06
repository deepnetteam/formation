Python3 installation using virtualenv - Ubuntu
======================================

## 1. Installation
We expect the user to be using on Ubuntu 18.04, though most of the command should work on previous versions. Most of the commands are to be run in a terminal, as indicated by the symbol `$` at the beginning of a line. Let's start by updating our packages:

```bash
$ sudo apt update
$ sudo apt upgrade
```

We then install python3, along with its development headers:

```bash
$ sudo apt install python3.7-dev
```

We will be using [pip](https://en.wikipedia.org/wiki/Pip_(package_manager), a python package manager, to install libraries such as numpy or tensorflow:

```bash
$ sudo apt install python3-pip
```

We can now install virtualenv, along with virtualenvwrapper, which allows us to use virtualenv easily:

```bash
$ sudo -H pip3 install virtualenv virtualenvwrapper
```

You should now edit the `.bashrc` file in your home folder, and add the following lines. Remember this is a [hidden file](https://askubuntu.com/questions/470837/how-to-show-hidden-folders-in-ubuntu-14-04#470849) !

```bash
# virtualenv and virtualenvwrapper
export WORKON_HOME=$HOME/.virtualenvs
export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
source /usr/local/bin/virtualenvwrapper.sh
```

The `~/.bashrc`  file is simply a shell script that Bash runs whenever you launch a new terminal. You normally use this file to set various configurations. In this case, we are setting an environment variable called `WORKON_HOME`  to point to the directory where our Python virtual environments live. We then load any necessary configurations from `virtualenvwrapper`. If you don't want to edit the file yourself you could run these commands in the shell

```bash
$ echo -e "\n# virtualenv and virtualenvwrapper\nexport VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3\nexport WORKON_HOME=$HOME/.virtualenvs\nsource /usr/local/bin/virtualenvwrapper.sh" >> ~/.bashrc
```

Let's force our terminal to update to the new configuration :
```bash
$ source ~/.bashrc
```

## 2. Usage

In order to create a virtual environment, you can use the following command in your shell:

```bash
mkvirtualenv yourvirutalenv
```

To start working in the environment, use ```workon yourvirutalenv```, and ```deactivate``` to exit. When activated, the name of the environment is written before the symbol `$`:

```bash
user@computer~$ workon tensorflow
(tensorflow) user@computer~$    
(tensorflow) user@computer~$ deactivate
user@computer~$
```
