Note to self:


VIRTUAL ENVIRONMENT

§ virtualenv --no-site-packages ~/.nameofvirtualenv

§ source ~/.nameofvirtualenv/bin/activate


CHDKPTP FOR UBUNTU X86 and X64

1. Remove old
2. 
§ sudo rm -rf /usr/local/lib/chdkptp

2. Download
3. 
§ wget --continue https://www.assembla.com/spaces/chdkptp/documents/acLgv2yhOr44ksacwqjQWU/download/acLgv2yhOr44ksacwqjQWU -O /tmp/chdkptp.zip

3. Unzip then remove
4. 
§ sudo unzip -d /usr/local/lib/chdkptp /tmp/chdkptp.zip

§ rm -rf /tmp/chdkptp.zip


# according to raspberry tutorial Install spreads from GitHub through:
git clone https://github.com/jbaiter/spreads.git /usr/src/spreads || exit 1
cd /usr/src/spreads || exit 1
git checkout webplugin || exit 1
# https://github.com/openxc/openxc-python/issues/18
pip install --pre pyusb || exit 1
pip install colorama futures flask flask-compress zipstream \
waitress requests jpegtran-cffi || exit 1
pip install git+https://github.com/dreamhost/stevedore.git@0.13
python setup.py install || exit 1

#BUT WORKS BETTER WITH
In virtual environment
§ cd/tmp
§ git clone https://github.com/jbaiter/spreads.git
§ cd spreads
now: (.venv3)kampsnigel@nya-datorn-ubuntu:/tmp/spreads
§ python setup.py install
§ pip install -e .[web]
§ deactivate
§ sudo su
§  cat /etc/udev/rules.d/99-usb.rules 
This means correct: GOOD ACTION=="add", SUBSYSTEM=="usb", MODE:="666"
§ exit

ACTIVATE VIRTUAL ENVIRONMENT WITH:
§ source ~/.nameofvirtualenv/bin/activate
§ which spread (SHOULD BE IN VIRTUAL ENVIRONMENT)
§ deactivate
$ sudo apt-get -y remove libgphoto2*
§ source ~/.nameofvirtualenv/bin/activate



§ pip install pyyaml
§ python setup.py install
§ pip install -e .[web]

WHEN INSTALLED. CONFIGURING

§ spreads configure


DONT CONNECT CAMERAS UNTIL ASKED BY TERMINAL

At configure you should choose a2200 then web. 

§ spread capture [OPTIONS]



::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::

OTHER FIXES

If problems with no spreads.log use following: 

§ mkdir -p ~/.config/spreads

§ touch ~/.config/spreads/spreads.log


Had problems with following:

apt-get -y install build-essential cython libffi-dev libjpeg8-dev liblua5.1-0\
            libudev-dev libusb-1.0-0-dev libusb-dev nginx python2.7-dev\
            python-pyexiv2 python-netifaces python-pip python-yaml unzip
          
            
Should have used sudo apt-get
This fixes cffi. 

DONT DO FOLLOWING!
INSTALL STEVEDORE (MABY FAULTY?)

$ pip install stevedore==0.13 futures==2.1.4 jpegtran-cffi==0.3.1
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




