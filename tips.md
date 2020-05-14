### 创建任意大小文件：
``` bash 
head -c 25MB /dev/urandon > test.file  
dd if=/dev/urandom of=test.file bs=25MB count=1   #if=input file;of=output file; bs=block size; count=被复制的块数
truncate -s 25M test.file  #-s 指定大小
```

### 修改文件拥有者和群组
``` bash 
chgrp 群组名 文件名 -R
chown 用户名 文件名 -R
```

### 安装supervisor四种方法
1. pip install  supervisor
``` bash
  #!/bin/bash
  wget http://pypi.python.org/packages/source/s/setuptools/setuptools-0.6c11.tar.gz
  tar zxvf setuptools-0.6c11.tar.gz
  cd setuptools-0.6c11
  python setup.py build
  python setup.py install
  wget "https://pypi.python.org/packages/source/p/pip/pip-1.5.4.tar.gz#md5=834b2904f92d46aaa33326"
  tar -xzvf pip-1.5.4.tar.gz
  cd pip-1.5.4
  python setup.py install
```
2. esay_install
``` bash
  yum install python-setuptools
  easy_install supervisor
```
3. python 
``` bash
　　wget https://pypi.python.org/packages/source/s/supervisor/supervisor-3.1.3.tar.gz
　　tar zxvf supervisor-3.1.3.tar.gz
　　cd supervisor
　　python setup.py install
```
4. epel
``` bash
　　yum install -y epel-release
　　yum install -y supervisor
```
