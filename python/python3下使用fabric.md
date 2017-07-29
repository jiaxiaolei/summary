目前fabric1.x还不支持python3。虽然fabric官方称fabric2.x 会支持python3, 但至少目前还没有看到确切的时间。

在fabirc2.x发布之前，可以使用fabric3.


```
 [root@centos]#  mkvirtualenv py3.6.1env2 -p /root/.pyenv/versions/3.6.1/bin/python --no-site-packages
Running virtualenv with interpreter /root/.pyenv/versions/3.6.1/bin/python
Using base prefix '/root/.pyenv/versions/3.6.1'
New python executable in /root/.virtualenvs/py3.6.1env2/bin/python
Please make sure you remove any previous custom paths from your /root/.pydistutils.cfg file.
Installing setuptools, pip, wheel...done.

 [root@centos]# workon py3.6.1env2
/root/.virtualenvs/py3.6.1env2/bin/python: Error while finding module specification for 'virtualenvwrapper.hook_loader' (ModuleNotFoundError: No module named 'virtualenvwrapper')
(py3.6.1env2) [root@centos]# pip install fabric3
Collecting fabric3
  Downloading http://mirrors.aliyun.com/pypi/packages/9c/f6/52e233f719989b690e02c8b5d6d83130ccae456d79434dd0e5aaac4d6832/Fabric3-1.13.1.post1-py3-none-any.whl (92kB)
    100% |████████████████████████████████| 102kB 1.0MB/s
Collecting paramiko<3.0,>=2.0 (from fabric3)
  Downloading http://mirrors.aliyun.com/pypi/packages/df/1b/7519f092c12048a4346c083101f9e6b8651fe455adc005f909c9cf83407b/paramiko-2.2.1-py2.py3-none-any.whl (176kB)
    100% |████████████████████████████████| 184kB 447kB/s
Collecting six>=1.10.0 (from fabric3)
  Downloading http://mirrors.aliyun.com/pypi/packages/c8/0a/b6723e1bc4c516cb687841499455a8505b44607ab535be01091c0f24f079/six-1.10.0-py2.py3-none-any.whl
Collecting bcrypt>=3.1.3 (from paramiko<3.0,>=2.0->fabric3)
  Downloading http://mirrors.aliyun.com/pypi/packages/d6/6e/36288d1ad63d92c220c7c015d046dc0c0f873d8fc349842007064f94d1a4/bcrypt-3.1.3-cp36-cp36m-manylinux1_x86_64.whl (54kB)
    100% |████████████████████████████████| 61kB 28.4MB/s
Collecting pynacl>=1.0.1 (from paramiko<3.0,>=2.0->fabric3)
  Downloading http://mirrors.aliyun.com/pypi/packages/51/d7/97d167ae204c78d76016f765f16d30309db1ea45b0ff4a9caeda2b355ffe/PyNaCl-1.1.2-cp36-cp36m-manylinux1_x86_64.whl (536kB)
    100% |████████████████████████████████| 542kB 458kB/s
Collecting pyasn1>=0.1.7 (from paramiko<3.0,>=2.0->fabric3)
  Downloading http://mirrors.aliyun.com/pypi/packages/4a/7b/59c521d82786e6573ee1f69965fc18f887f16af4d8f418ef0b2e55eede8d/pyasn1-0.3.1-py2.py3-none-any.whl (61kB)
    100% |████████████████████████████████| 71kB 17.4MB/s
Collecting cryptography>=1.1 (from paramiko<3.0,>=2.0->fabric3)
  Downloading http://mirrors.aliyun.com/pypi/packages/d9/1c/299fc042685c288ace5d8c0a98474ff8d2e0b95e747eb89be3f93571ef3a/cryptography-2.0.2-cp36-cp36m-manylinux1_x86_64.whl (2.2MB)
    100% |████████████████████████████████| 2.2MB 391kB/s
Collecting cffi>=1.1 (from bcrypt>=3.1.3->paramiko<3.0,>=2.0->fabric3)
  Downloading http://mirrors.aliyun.com/pypi/packages/99/2f/2304b68ee2eea8395fb98702077e667849b98b9037956fafbef65fd53e0b/cffi-1.10.0-cp36-cp36m-manylinux1_x86_64.whl (406kB)
    100% |████████████████████████████████| 409kB 430kB/s
Collecting asn1crypto>=0.21.0 (from cryptography>=1.1->paramiko<3.0,>=2.0->fabric3)
  Downloading http://mirrors.aliyun.com/pypi/packages/97/ba/7e8117d8efcee589f4d96dd2b2eb1d997f96d27d214cf2b7134ad8acf6ab/asn1crypto-0.22.0-py2.py3-none-any.whl (97kB)
    100% |████████████████████████████████| 102kB 990kB/s
Collecting idna>=2.1 (from cryptography>=1.1->paramiko<3.0,>=2.0->fabric3)
  Downloading http://mirrors.aliyun.com/pypi/packages/11/7d/9bbbd7bb35f34b0169542487d2a8859e44306bb2e6a4455d491800a5621f/idna-2.5-py2.py3-none-any.whl (55kB)
    100% |████████████████████████████████| 61kB 25.9MB/s
Collecting pycparser (from cffi>=1.1->bcrypt>=3.1.3->paramiko<3.0,>=2.0->fabric3)
Installing collected packages: pycparser, cffi, six, bcrypt, pynacl, pyasn1, asn1crypto, idna, cryptography, paramiko, fabric3
Successfully installed asn1crypto-0.22.0 bcrypt-3.1.3 cffi-1.10.0 cryptography-2.0.2 fabric3-1.13.1.post1 idna-2.5 paramiko-2.2.1 pyasn1-0.3.1 pycparser-2.18 pynacl-1.1.2 six-1.10.0
(py3.6.1env2) [root@centos]# fab -V
Fabric3 1.13.1.post1
Paramiko 2.2.1
```
扩展阅读
=======

[Python 3 support for fabric](https://stackoverflow.com/questions/18736274/python-3-support-for-fabric)
简介：
So until Fabric 2.0 will be ready, this package can be used instead :)
pip3 install fabric3

http://www.fabfile.org/roadmap.html
简介：
fabirc2 的发布情况。

https://github.com/mathiasertl/fabric
简介：
Fabric3 is a Python (2.7 or 3.4+) library and command-line tool for streamlining the use of SSH for application deployment or systems administration tasks. This is a fork of the original [Fabric](http://www.fabfile.org/) ([git](https://github.com/fabric/fabric)) with the intention of providing support for Python3, while maintaining support for all non-archaic versions of Python2. Please see below for known differences with the upstream version of Fabric. To switch to Fabric3, simply do:
pip uninstall Fabricpip install Fabric3


https://pypi.python.org/pypi/Fabric3/1.13.1.post1
简介：
pypi上的fabric3.
Fabric3 is a fork of [Fabric](http://fabfile.org/) to provide compatability with Python 3.4+. The port still works with Python 2.7.
The goal is to stay 100% compatible with the original Fabric. Any new releases of Fabric will also be released here. Please file issues for any differences you find. Known differences are documented on github <https://github.com/mathiasertl/fabric/>
.
To find out what’s new in this version of Fabric, please see [the changelog](http://fabfile.org/changelog.html) of the original Fabric.
For more information, please see the Fabric website or execute fab --help
.



https://pypi.python.org/pypi/Fabric/1.13.2
简介：
pypi上的fabric

You can also install the development version via “pip install -e git+https://github.com/fabric/fabric/#egg=fabric`.

Fabric is a Python (2.5-2.7) library and command-line tool for streamlining the use of SSH for application deployment or systems administration tasks.