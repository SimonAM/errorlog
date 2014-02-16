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


::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
My problems: 

"§ Unzip chdkptp...", is not putting chdkptp inside virtualenv. Maby thats a problem. 
"§ pip install stevedore"   is getting following error code: 

ImportError: No module named cffi
----------------------------------------
Command python setup.py egg_info failed with error code 1 in /home/simon/.spreads4/build/jpegtran-cffi





::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
Other fixes

If problems with no spreads.log use following: 
§ mkdir -p ~/.config/spreads
§ touch ~/.config/spreads/spreads.log

