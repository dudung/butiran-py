# log
Some notes


## Version 0.0.9 (2021-02-07)

### Create source and build distributions
```
S py setup.py sdist bdist_wheel
running sdist
running egg_info
writing butiran.egg-info\PKG-INFO
writing dependency_links to butiran.egg-info\dependency_links.txt
writing top-level names to butiran.egg-info\top_level.txt
reading manifest file 'butiran.egg-info\SOURCES.txt'
writing manifest file 'butiran.egg-info\SOURCES.txt'
running check
creating butiran-0.0.9
creating butiran-0.0.9\butiran
creating butiran-0.0.9\butiran.egg-info
copying files to butiran-0.0.9...
copying README.md -> butiran-0.0.9
copying setup.py -> butiran-0.0.9
copying butiran\__init__.py -> butiran-0.0.9\butiran
copying butiran\vect3.py -> butiran-0.0.9\butiran
copying butiran.egg-info\PKG-INFO -> butiran-0.0.9\butiran.egg-info
copying butiran.egg-info\SOURCES.txt -> butiran-0.0.9\butiran.egg-info
copying butiran.egg-info\dependency_links.txt -> butiran-0.0.9\butiran.egg-info
copying butiran.egg-info\top_level.txt -> butiran-0.0.9\butiran.egg-info
Writing butiran-0.0.9\setup.cfg
Creating tar archive
removing 'butiran-0.0.9' (and everything under it)
running bdist_wheel
running build
running build_py
installing to build\bdist.win-amd64\wheel
running install
running install_lib
creating build\bdist.win-amd64\wheel
creating build\bdist.win-amd64\wheel\butiran
copying build\lib\butiran\vect3.py -> build\bdist.win-amd64\wheel\.\butiran
copying build\lib\butiran\__init__.py -> build\bdist.win-amd64\wheel\.\butiran
running install_egg_info
Copying butiran.egg-info to build\bdist.win-amd64\wheel\.\butiran-0.0.9-py3.9.egg-info
running install_scripts
adding license file "LICENSE" (matched pattern "LICEN[CS]E*")
creating build\bdist.win-amd64\wheel\butiran-0.0.9.dist-info\WHEEL
creating 'dist\butiran-0.0.9-py3-none-any.whl' and adding 'build\bdist.win-amd64\wheel' to it
adding 'butiran/__init__.py'
adding 'butiran/vect3.py'
adding 'butiran-0.0.9.dist-info/LICENSE'
adding 'butiran-0.0.9.dist-info/METADATA'
adding 'butiran-0.0.9.dist-info/WHEEL'
adding 'butiran-0.0.9.dist-info/top_level.txt'
adding 'butiran-0.0.9.dist-info/RECORD'
removing build\bdist.win-amd64\wheel
```

### Check dist and wheel
```
py -m twine check dist/*
Checking dist\butiran-0.0.9-py3-none-any.whl: PASSED
Checking dist\butiran-0.0.9.tar.gz: PASSED
```

### Upload to TestPyPi
```
py -m twine upload --repository testpypi dist/*
Uploading distributions to https://test.pypi.org/legacy/
Enter your username: dudung
Enter your password:
Uploading butiran-0.0.9-py3-none-any.whl
100%|██████████████████████████████████████████████| 8.56k/8.56k [00:03<00:00, 2.25kB/s]
Uploading butiran-0.0.9.tar.gz
100%|██████████████████████████████████████████████| 7.83k/7.83k [00:01<00:00, 5.97kB/s]

View at:
https://test.pypi.org/project/butiran/0.0.9/
```

### Install from TestPyPi
```
py -m pip install --index-url https://test.pypi.org/simple/ butiran
Looking in indexes: https://test.pypi.org/simple/
Collecting butiran
  Downloading https://test-files.pythonhosted.org/packages/89/09/3df933acbc307659cba30a41d30b700781c3793bfdb246cea56db56a6ced/butiran-0.0.9-py3-none-any.whl (4.8 kB)
Installing collected packages: butiran
Successfully installed butiran-0.0.9
```

### Uninstall butiran
```
py -m pip uninstall butiran
Found existing installation: butiran 0.0.9
Uninstalling butiran-0.0.9:
  Would remove:
    c:\users\sparisoma viridi\appdata\local\programs\python\python39\lib\site-packages\butiran-0.0.9.dist-info\*
    c:\users\sparisoma viridi\appdata\local\programs\python\python39\lib\site-packages\butiran\*
Proceed (y/n)? y
  Successfully uninstalled butiran-0.0.9
```