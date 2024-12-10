# Wynton_setup (this .md is still under construction)
This repository provides instructions to set up your account on UCSF Wynton server based on the experience of He Lab members

## 1. Preparation on Wynton
1.1 [Request a Wynton account](https://wynton.ucsf.edu/hpc/about/join.html)
1.2 Log in using your credentials
```
{local}$ ssh alice@log1.wynton.ucsf.edu
alice@log1.wynton.ucsf.edu:s password: 
[alice@log1 ~]$
```
<details><summary>For setting up login atlas, follow this extra step🔽</summary>
XXXXXX
  </details>

<details><summary>For password-free login, follow this extra step🔽</summary>
XXXXXX
  </details>

1.3 Log into [development nodes](https://wynton.ucsf.edu/hpc/get-started/development-prototyping.html)
```
[alice@log1 ~]$ ssh dev1.wynton.ucsf.edu
alice1@dev1:s password: XXXXXXXXXXXXXXXXXXX
[alice@dev1 ~]$ 
```

1.4 Install miniconda

1.4.1 Download miniconda from the [official download page](https://repo.anaconda.com/miniconda/)
`wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh`

1.4.2 Run installation script
`bash Miniconda3-latest-Linux-x86_64.sh`

1.4.2 Edit `~/.bashrc` to activate miniconda

`nano ~/.bashrc` and then include XXXXXXXXXX

## 2. Set up Jupyter notebook

2.1 install jupyter
```
pip3 install jupyter
```

2.2 set up the port
```
jupyter notebook --generate-config
```
Then edit the generated configuration file `jupyter_notebook_config.py` through
```
nano ~/.jupyter/jupyter_notebook_config.py
```
Then choose a port number (i.e. 8888) and uncomment and edit the line 
```
## The port the server will listen on (env: JUPYTER_PORT).
#  Default: 0
c.ServerApp.port = 8888
```

2.3 run jupyter notebook from server

Open a `screen` or `tmux` window. See detailed `screen` [usage](https://www.liquidweb.com/blog/how-to-use-the-screen-command-in-linux/) or `tmux` [usage](https://www.linuxtrainingacademy.com/tmux-tutorial/),
```
screen
```
Then initiate a jupyter notebook
```
jupyter notebook --no-browser
```
You will see something like
```
Or copy and paste one of these URLs:
        http://localhost:8888/tree?token=XXXXXXX
        http://127.0.0.1:8888/tree?token=XXXXXXX
```
Copy the token XXXXXXX


2.4 login from local machine

Open a new terminal session and connect to the jupyter notebook running on the Wynton through
```
ssh -J alice@log1.wynton.ucsf.edu -L 8080:localhost:8888 alice@dev1
```

2.5 open notebooks from browser

Now open a browser and go to `http://localhost:8080/`. You might need to paste the token copied above. Then you are all set. 
