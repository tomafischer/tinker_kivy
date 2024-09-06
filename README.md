# Installas

```
#### Miniconda / Anaconda
conda config --set ssl_verify <pathToYourFile>.crt

# in case you have to delete an old one
conda env remove --name py12
## create env
conda create --name py12 python=3.12

## activate conda env you created
conda activate py12

#### Venv
## create new venv
python -m venv .venv

## activat new created venv
# Windows
.venv\Scripts\activate
#Linux/Mac
. ./.venv/bin/activate

#### Install Packages via pip
## upgrade pip
python -m pip install
# or with ssl fix
python -m pip install --upgrade pip --trusted-host pypi.org --trusted-host pypi.python.org --trusted-host files.pythonhosted.org111

## install packages for requirements.txt
pip install -r requirement.txt
# ssl fix
pip install --trusted-host pypi.org --trusted-host pypi.python.org --trusted-host files.pythonhosted.org -r requirements.txt
#or
pip --cert certs\cacert.pem install -r requirements.txt

## work around ssl issues
pip install --trusted-host pypi.org --trusted-host pypi.python.org --trusted-host files.pythonhosted.org <package_name>
```
