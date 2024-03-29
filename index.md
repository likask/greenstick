# Greenstick

### Being good citizen

- If you run somthing with multiprocesses and which will run longer than 5-10 minutes, be nice, i.e. run command as follows
~~~~
nice -n 10 mpirun -np 4 ./command_line
~~~~

- If you run longer problems use buckedhead

### News about Greenstick

- We can share notebooks, and snipets in directory */common_notebooks*. All of you should have primissions to read and write to it. Execute command to crate link,
~~~~
ln -s /common_notebooks $HOME/
~~~~
- Unfortunatly we do not have large hard-drive (for now) on greenstick. Please remove oboslete files, and for large computations use *Buckedhead*.

### Password and login

- On the first login, select the password
- The shell password on the SSH login is different than the JupyterHub password
- Ask admin for SSH password
- Change password in the shell using [passwd](https://man7.org/linux/man-pages/man1/passwd.1.html){:target="_blank" rel="noopener"} command
- Set up your shell with the command (e.g. bash):
~~~~
$ usermod --shell /bin/bash your_login_name
~~~~

### SSH config if you have account on cactus

Copy the following code into .ssh/config on your laptop or desktop.
~~~~
Host forward_greenstick
  HostName cactus.eng.gla.ac.uk
  ForwardX11 yes
  Compression yes
  User YOUR_LOGIN_ON_HUB
  Port 2222
~~~~

Use *forward_greenstick* when you login in VSCode. Note tha you are connecting to *cactus* from which is tunnel to *geenstick*.

### Video on JuputerHub, SSH and MoFEM

[![Watch the video](https://img.youtube.com/vi/xL3J8VHig68/hqdefault.jpg)](https://youtu.be/xL3J8VHig68){:target="_blank" rel="noopener"}

