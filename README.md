Note to self:


VIRTUAL ENVIRONMENT

§ virtualenv --no-site-packages ~/.nameofvirtualenv

§ source ~/.nameofvirtualenv/bin/activate

CHDKPTP FOR UBUNTU X86 and X64

1. Remove old

§ sudo rm -rf /usr/local/lib/chdkptp

2. Download

§ wget --continue https://www.assembla.com/spaces/chdkptp/documents/acLgv2yhOr44ksacwqjQWU/download/acLgv2yhOr44ksacwqjQWU -O /tmp/chdkptp.zip

3. Unzip 

§ sudo unzip -d /usr/local/lib/chdkptp /tmp/chdkptp.zip

4. Remove zip

§ rm -rf /tmp/chdkptp.zip


Raspberry tutorial nstall spreads through:
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



