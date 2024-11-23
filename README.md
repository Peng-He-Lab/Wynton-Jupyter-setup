# Wynton_setup
This repository provides instructions to set up your account on UCSF Wynton server based on the experience of He Lab members

## 1. Preparation
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

1.3 Log into [development nodes](https://wynton.ucsf.edu/hpc/get-started/development-prototyping.html)
[alice@log1 ~]$ ssh dev1.wynton.ucsf.edu
alice1@dev1:s password: XXXXXXXXXXXXXXXXXXX
[alice@dev1 ~]$ 

1.4 Install miniconda

1.4.1 Download miniconda from the [official download page](https://repo.anaconda.com/miniconda/)
`wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh`

1.4.2 Run installation script
`bash Miniconda3-latest-Linux-x86_64.sh`

1.4.2 Edit `~/.bashrc` to activate miniconda

`nano ~/.bashrc` and then include XXXXXXXXXX



