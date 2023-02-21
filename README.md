#   OpenCv: Hello World programs in python and C++
made by Lucas Schmirl 20.02.2022, info.hellgineer@gmail.com, last edit: 21.02.2022

<br>

# General:

## OpenCv installation

First create a folder for the project:
```bash
mkdir openCv
```

For using openCv inside a virtual environment install `venv`:
(if not needed skip to 'installing the openCv pip pkg')

```bash
sudo apt install -y python3-venv
```

To create an virtual environment (hiding the folder is optional):
```bash
python3 -m venv .venv
```

To activate the environment:
```bash
source .venv/bin/activate
```

To deactivate the environment:
```bash
deactivate
```

Inside this `venv`, packages can be installed (f.e. `pip`) which are only accessible inside this `venv` (not system wide). If you delete the `venv`, all containing packages are deleted. 

Continue by **installing the openCv pip pkg:**
```bash
pip install opencv-contrib-python
```

If this install fails, check out your versions with:
```bash
pip --version
python --version
```
and find out (by using the internet) which versions are the minimal requirement. Maybe you need to upgrade your stuff.


<br>
<br>

# PYTHON:
### Content: 
`requirements.txt` (lists all needed pkg's)

`scripts/helloworld.py` (python script to load and display image)

`scripts/take_pic.py`   (python script to take image from webcam)

`PICs/Schaukelbub.png` (image source)

<br>

### Setup:
```bash
pip install -r requirements.txt
```
### USAGE: 
```bash
python3 scripts/hello_world.py
python3 scripts/take_pic.py
```

<br>
<br>

# C++:
### Content: 
`Makefile` (to build the project, compiling and linking)

`src/main.cpp` (source file)

`PICs/Schaukelbub.png` (image source)

<br>

### Build:
```bash
make
```
### USAGE: 
```bash
./helloWorld <path-to-image>
```

<br>
<br>
<br>

## Additional information

<br>

### System used
- WSL2 version: 1.0.3.0 on Win11
- Ubuntu 20.04.5 LTS
- Python version: 3.8.10
- opencv-contrib version: 4.7.0.68


<br>

### Weird WSL bugs

When using older version of WSL2 pics close immideately or dont close at all after using the keyboard to interact with `waitkey(0)` the key chache can get stuck. 

Workaround is to restart your WSL from `PowerShell` using:
```powershell
wsl --shutdown
```
Fix that worked for me is to simply update your WSL from `PowerShell` using:

```powershell
wsl --update
```
