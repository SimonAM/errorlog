Note to self: 

§ virtualenv --no-site-packages ~/.nameofvirtualenv
§ source ~/.nameofvirtualenv/bin/activate
(.spreads4)simon@Simons-Ubuntu:~$ unzip chdkptp-r468-Linux-x86_64.zip -d usr/local/lib/chdkptp
(.spreads4)simon@Simons-Ubuntu:~$ pip install stevedore==0.13 futures==2.1.4 jpegtran-cffi==0.3.1
§ pip install spreads    OR    § pip install git+git://github.com/jbaiter/spreads.git@master


When installed
§ spreads configure

At configure you should choose a2200 and no plugins to be able to capture through following command:

§ spread capture [OPTIONS]



::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
Other fixes

If problems with no spreads.log use following: 
§ mkdir -p ~/.config/spreads
§ touch ~/.config/spreads/spreads.log

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
My problems: 

"§ Unzip chdkptp...", is not putting chdkptp inside virtualenv. Maby thats a problem. 
"§ pip install stevedore"   is getting following error code: 

ImportError: No module named cffi
----------------------------------------
Command python setup.py egg_info failed with error code 1 in /home/simon/.spreads4/build/jpegtran-cffi

virtualenv§ pip install cffi 
Gives:
Downloading/unpacking cffi
  Downloading cffi-0.8.1.tar.gz (195kB): 195kB downloaded
  Running setup.py (path:/home/simon/.spreads4/build/cffi/setup.py) egg_info for package cffi
    Package libffi was not found in the pkg-config search path.
    Perhaps you should add the directory containing `libffi.pc'
    to the PKG_CONFIG_PATH environment variable
    No package 'libffi' found
    Package libffi was not found in the pkg-config search path.
    Perhaps you should add the directory containing `libffi.pc'
    to the PKG_CONFIG_PATH environment variable
    No package 'libffi' found
    Package libffi was not found in the pkg-config search path.
    Perhaps you should add the directory containing `libffi.pc'
    to the PKG_CONFIG_PATH environment variable
    No package 'libffi' found
    Package libffi was not found in the pkg-config search path.
    Perhaps you should add the directory containing `libffi.pc'
    to the PKG_CONFIG_PATH environment variable
    No package 'libffi' found
    Package libffi was not found in the pkg-config search path.
    Perhaps you should add the directory containing `libffi.pc'
    to the PKG_CONFIG_PATH environment variable
    No package 'libffi' found
    
Downloading/unpacking pycparser (from cffi)
  Downloading pycparser-2.10.tar.gz (206kB): 206kB downloaded
  Running setup.py (path:/home/simon/.spreads4/build/pycparser/setup.py) egg_info for package pycparser
    
Installing collected packages: cffi, pycparser
  Running setup.py install for cffi
    Package libffi was not found in the pkg-config search path.
    Perhaps you should add the directory containing `libffi.pc'
    to the PKG_CONFIG_PATH environment variable
    No package 'libffi' found
    Package libffi was not found in the pkg-config search path.
    Perhaps you should add the directory containing `libffi.pc'
    to the PKG_CONFIG_PATH environment variable
    No package 'libffi' found
    Package libffi was not found in the pkg-config search path.
    Perhaps you should add the directory containing `libffi.pc'
    to the PKG_CONFIG_PATH environment variable
    No package 'libffi' found
    Package libffi was not found in the pkg-config search path.
    Perhaps you should add the directory containing `libffi.pc'
    to the PKG_CONFIG_PATH environment variable
    No package 'libffi' found
    Package libffi was not found in the pkg-config search path.
    Perhaps you should add the directory containing `libffi.pc'
    to the PKG_CONFIG_PATH environment variable
    No package 'libffi' found
    building '_cffi_backend' extension
    gcc -pthread -fno-strict-aliasing -DNDEBUG -g -fwrapv -O2 -Wall -Wstrict-prototypes -fPIC -DUSE__THREAD -I/usr/include/ffi -I/usr/include/libffi -I/usr/include/python2.7 -c c/_cffi_backend.c -o build/temp.linux-x86_64-2.7/c/_cffi_backend.o
    c/_cffi_backend.c:14:17: fatal error: ffi.h: No such file or directory
    compilation terminated.
    error: command 'gcc' failed with exit status 1
    Complete output from command /home/simon/.spreads4/bin/python -c "import setuptools, tokenize;__file__='/home/simon/.spreads4/build/cffi/setup.py';exec(compile(getattr(tokenize, 'open', open)(__file__).read().replace('\r\n', '\n'), __file__, 'exec'))" install --record /tmp/pip-RLR_MQ-record/install-record.txt --single-version-externally-managed --compile --install-headers /home/simon/.spreads4/include/site/python2.7:
    Package libffi was not found in the pkg-config search path.

Perhaps you should add the directory containing `libffi.pc'

to the PKG_CONFIG_PATH environment variable

No package 'libffi' found

Package libffi was not found in the pkg-config search path.

Perhaps you should add the directory containing `libffi.pc'

to the PKG_CONFIG_PATH environment variable

No package 'libffi' found

Package libffi was not found in the pkg-config search path.

Perhaps you should add the directory containing `libffi.pc'

to the PKG_CONFIG_PATH environment variable

No package 'libffi' found

Package libffi was not found in the pkg-config search path.

Perhaps you should add the directory containing `libffi.pc'

to the PKG_CONFIG_PATH environment variable

No package 'libffi' found

Package libffi was not found in the pkg-config search path.

Perhaps you should add the directory containing `libffi.pc'

to the PKG_CONFIG_PATH environment variable

No package 'libffi' found

running install

running build

running build_py

creating build

creating build/lib.linux-x86_64-2.7

creating build/lib.linux-x86_64-2.7/cffi

copying cffi/lock.py -> build/lib.linux-x86_64-2.7/cffi

copying cffi/vengine_gen.py -> build/lib.linux-x86_64-2.7/cffi

copying cffi/backend_ctypes.py -> build/lib.linux-x86_64-2.7/cffi

copying cffi/commontypes.py -> build/lib.linux-x86_64-2.7/cffi

copying cffi/gc_weakref.py -> build/lib.linux-x86_64-2.7/cffi

copying cffi/api.py -> build/lib.linux-x86_64-2.7/cffi

copying cffi/ffiplatform.py -> build/lib.linux-x86_64-2.7/cffi

copying cffi/verifier.py -> build/lib.linux-x86_64-2.7/cffi

copying cffi/model.py -> build/lib.linux-x86_64-2.7/cffi

copying cffi/__init__.py -> build/lib.linux-x86_64-2.7/cffi

copying cffi/vengine_cpy.py -> build/lib.linux-x86_64-2.7/cffi

copying cffi/cparser.py -> build/lib.linux-x86_64-2.7/cffi

running build_ext

building '_cffi_backend' extension

creating build/temp.linux-x86_64-2.7

creating build/temp.linux-x86_64-2.7/c

gcc -pthread -fno-strict-aliasing -DNDEBUG -g -fwrapv -O2 -Wall -Wstrict-prototypes -fPIC -DUSE__THREAD -I/usr/include/ffi -I/usr/include/libffi -I/usr/include/python2.7 -c c/_cffi_backend.c -o build/temp.linux-x86_64-2.7/c/_cffi_backend.o

c/_cffi_backend.c:14:17: fatal error: ffi.h: No such file or directory

compilation terminated.

error: command 'gcc' failed with exit status 1

----------------------------------------
Cleaning up...
Command /home/simon/.spreads4/bin/python -c "import setuptools, tokenize;__file__='/home/simon/.spreads4/build/cffi/setup.py';exec(compile(getattr(tokenize, 'open', open)(__file__).read().replace('\r\n', '\n'), __file__, 'exec'))" install --record /tmp/pip-RLR_MQ-record/install-record.txt --single-version-externally-managed --compile --install-headers /home/simon/.spreads4/include/site/python2.7 failed with error code 1 in /home/simon/.spreads4/build/cffi
Storing debug log for failure in /home/simon/.pip/pip.log




