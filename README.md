# compile-python

check `python --version` and you'll see that right now you have `Python 3.12.1`
This is a repo for compiling and installing python from scratch
open a second terminal and `htop` it to watch how cores and memory will be saturated. Fun!

## Compile Python and Create a VirtualEnv with it

`sudo apt-get install build-essential gdb lcov libbz2-dev libffi-dev libgdbm-dev liblzma-dev libncurses5-dev libreadline6-dev libsqlite3-dev libssl-dev lzma lzma-dev tk-dev uuid-dev zlib1g-dev`

`wget https://www.python.org/ftp/python/3.11.10/Python-3.11.10.tgz`

`tar zxvf Python-3.11.10.tgz`

`./configure --enable-optimizations`

`make -j 16` assuming you have at least 16 cores for this codespace

`sudo make altinstall`

Add `alias python="/usr/local/bin/python3.11"` to ~/.bashrc
then `source ~/.bashrc`

create virtual environment in ~ 
`python -m venv ~/.venv`
then activate it
`source ~/.venv/bin/activate`


run `make install` to make file