errorlog
========
My notes:::::::::::::::::::::::::::::::::::::::::::::::
§ virtualenv --no-site-packages ~/.spreads4
§ source ~/.spreads4/bin/activate
§ unzip chdkptp-r468-Linux-x86_64.zip -d usr/local/lib/chdkptp
§ pip install stevedore==0.13 futures==2.1.4 jpegtran-cffi==0.3.1
(importerror: no module named cffi)
§ pip install git+https://github.com/matti-kariluoma/spreads.git@master
(build/temp.linux-x86_64-2.7/check_libyaml.c:2:18: fatal error: yaml.h: No such file or directory) 
§ spread configure
§ 2 (a2200)
§ (finish without plugin)
(lot of text ending with: RuntimeError: No u'spreadsplug.devices' driver found, looking for u'a2200)

Choosing web-plugin:
(ImportError: No module named flask)

End of my notes:::::::::::::::::::::::::::::::::::::::

(.spreads3)simon@Simons-Ubuntu:~$ deactivate
simon@Simons-Ubuntu:~$ virtualenv --no-site-packages ~/.spreads4
The --no-site-packages flag is deprecated; it is now the default behavior.
New python executable in /home/simon/.spreads4/bin/python
Installing distribute..............................................................................................................................................................................................done.
Installing pip...............done.
simon@Simons-Ubuntu:~$ source ~/.spreads4/bin/activate
(.spreads4)simon@Simons-Ubuntu:~$ pip install git+https://github.com/matti-kariluoma/spreads.git@master^C
(.spreads4)simon@Simons-Ubuntu:~$ unzip chdkptp-r468-Linux-x86_64.zip -d usr/local/lib/chdkptp
Archive:  chdkptp-r468-Linux-x86_64.zip
replace usr/local/lib/chdkptp/chdkptp? [y]es, [n]o, [A]ll, [N]one, [r]ename: A
  inflating: usr/local/lib/chdkptp/chdkptp  
  inflating: usr/local/lib/chdkptp/chdkptp-sample.sh  
error:  cannot delete old usr/local/lib/chdkptp/lua/chdku.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/cli.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/dngcli.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/dng.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/exposure.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/fsutil.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/gui_icon.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/gui_live.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/gui_live_stats.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/gui.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/gui_tree.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/gui_user.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/lbufutil.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/main.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/multicam.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/prefs.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/rlibs.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/tests.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/ustime.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/util.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/extras/dbgdump.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/extras/dcimdl.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/extras/hackcfa.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/extras/msgtest.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/extras/simplemulticam.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/extras/vxromlog.lua
        Permission denied
error:  cannot delete old usr/local/lib/chdkptp/lua/extras/vxtcbdump.lua
        Permission denied
  inflating: usr/local/lib/chdkptp/README.TXT  
  inflating: usr/local/lib/chdkptp/USAGE.TXT  
  inflating: usr/local/lib/chdkptp/COPYING  
  inflating: usr/local/lib/chdkptp/THANKS.TXT  
  inflating: usr/local/lib/chdkptp/README-RASPI.TXT  
  inflating: usr/local/lib/chdkptp/README-RASPI-LIBS.TXT  
  inflating: usr/local/lib/chdkptp/README-OSX.TXT  
(.spreads4)simon@Simons-Ubuntu:~$ sudo pip install stevedore==0.13 futures==2.1.4 jpegtran-cffi==0.3.1
Requirement already satisfied (use --upgrade to upgrade): stevedore==0.13 in /usr/local/lib/python2.7/dist-packages
Requirement already satisfied (use --upgrade to upgrade): futures==2.1.4 in /usr/local/lib/python2.7/dist-packages
Downloading/unpacking jpegtran-cffi==0.3.1
  Running setup.py egg_info for package jpegtran-cffi
    Traceback (most recent call last):
      File "<string>", line 14, in <module>
      File "/home/simon/build/jpegtran-cffi/setup.py", line 4, in <module>
        import jpegtran.lib
      File "jpegtran/__init__.py", line 1, in <module>
        from jpegtran.transform import JPEGImage
      File "jpegtran/transform.py", line 3, in <module>
        import jpegtran.lib as lib
      File "jpegtran/lib.py", line 9, in <module>
        from cffi import FFI
    ImportError: No module named cffi
    Complete output from command python setup.py egg_info:
    Traceback (most recent call last):

  File "<string>", line 14, in <module>

  File "/home/simon/build/jpegtran-cffi/setup.py", line 4, in <module>

    import jpegtran.lib

  File "jpegtran/__init__.py", line 1, in <module>

    from jpegtran.transform import JPEGImage

  File "jpegtran/transform.py", line 3, in <module>

    import jpegtran.lib as lib

  File "jpegtran/lib.py", line 9, in <module>

    from cffi import FFI

ImportError: No module named cffi

----------------------------------------
Command python setup.py egg_info failed with error code 1
Storing complete log in /home/simon/.pip/pip.log
(.spreads4)simon@Simons-Ubuntu:~$ pip install stevedore==0.13 futures==2.1.4 jpegtran-cffi==0.3.1
Downloading/unpacking stevedore==0.13
  Downloading stevedore-0.13.tar.gz (760Kb): 760Kb downloaded
  Running setup.py egg_info for package stevedore
    
    Installed /home/simon/.spreads4/build/stevedore/pbr-0.6-py2.7.egg
    [pbr] Excluding argparse: Python 2.6 only dependency
    [pbr] Processing SOURCES.txt
    warning: LocalManifestMaker: standard file '-c' not found
    
    warning: no previously-included files found matching '.gitignore'
    warning: no previously-included files found matching '.gitreview'
    warning: no previously-included files matching '*.pyc' found anywhere in distribution
    warning: no files found matching '*.py' under directory 'tests'
Downloading/unpacking futures==2.1.4
  Downloading futures-2.1.4.tar.gz
  Running setup.py egg_info for package futures
    
Downloading/unpacking jpegtran-cffi==0.3.1
  Downloading jpegtran-cffi-0.3.1.tar.gz (49Kb): 49Kb downloaded
  Running setup.py egg_info for package jpegtran-cffi
    Traceback (most recent call last):
      File "<string>", line 14, in <module>
      File "/home/simon/.spreads4/build/jpegtran-cffi/setup.py", line 4, in <module>
        import jpegtran.lib
      File "jpegtran/__init__.py", line 1, in <module>
        from jpegtran.transform import JPEGImage
      File "jpegtran/transform.py", line 3, in <module>
        import jpegtran.lib as lib
      File "jpegtran/lib.py", line 9, in <module>
        from cffi import FFI
    ImportError: No module named cffi
    Complete output from command python setup.py egg_info:
    Traceback (most recent call last):

  File "<string>", line 14, in <module>

  File "/home/simon/.spreads4/build/jpegtran-cffi/setup.py", line 4, in <module>

    import jpegtran.lib

  File "jpegtran/__init__.py", line 1, in <module>

    from jpegtran.transform import JPEGImage

  File "jpegtran/transform.py", line 3, in <module>

    import jpegtran.lib as lib

  File "jpegtran/lib.py", line 9, in <module>

    from cffi import FFI

ImportError: No module named cffi

----------------------------------------
Command python setup.py egg_info failed with error code 1 in /home/simon/.spreads4/build/jpegtran-cffi
Storing complete log in /home/simon/.pip/pip.log
(.spreads4)simon@Simons-Ubuntu:~$ pip install git+https://github.com/matti-kariluoma/spreads.git@master
Downloading/unpacking git+https://github.com/matti-kariluoma/spreads.git@master
  Cloning https://github.com/matti-kariluoma/spreads.git (to master) to /tmp/pip-0hrNND-build
>>  Running setup.py egg_info for package from git+https://github.com/matti-kariluoma/spreads.git@master
    
Downloading/unpacking colorama>=0.2.5 (from spreads==0.0.0)
  Downloading colorama-0.2.7.tar.gz
  Running setup.py egg_info for package colorama
    
Downloading/unpacking PyYAML>=3.10 (from spreads==0.0.0)
  Downloading PyYAML-3.10.tar.gz (241Kb): 241Kb downloaded
  Running setup.py egg_info for package PyYAML
    
Downloading/unpacking stevedore>=0.9.1,<0.14 (from spreads==0.0.0)
  Running setup.py egg_info for package stevedore
    [pbr] Excluding argparse: Python 2.6 only dependency
    [pbr] Reusing existing SOURCES.txt
Downloading/unpacking futures>=2.1.4 (from spreads==0.0.0)
  Running setup.py egg_info for package futures
    
Installing collected packages: colorama, PyYAML, stevedore, futures, spreads
  Running setup.py install for colorama
    
  Running setup.py install for PyYAML
    checking if libyaml is compilable
    gcc -pthread -fno-strict-aliasing -DNDEBUG -g -fwrapv -O2 -Wall -Wstrict-prototypes -fPIC -I/usr/include/python2.7 -c build/temp.linux-x86_64-2.7/check_libyaml.c -o build/temp.linux-x86_64-2.7/check_libyaml.o
    build/temp.linux-x86_64-2.7/check_libyaml.c:2:18: fatal error: yaml.h: No such file or directory
    compilation terminated.
    
    libyaml is not found or a compiler error: forcing --without-libyaml
    (if libyaml is installed correctly, you may need to
     specify the option --include-dirs or uncomment and
     modify the parameter include_dirs in setup.cfg)
    
  Running setup.py install for stevedore
    [pbr] Excluding argparse: Python 2.6 only dependency
    [pbr] Reusing existing SOURCES.txt
  Running setup.py install for futures
    
  Running setup.py install for spreads
    changing mode of build/scripts-2.7/spread from 664 to 775
    
    changing mode of /home/simon/.spreads4/bin/spread to 775
Successfully installed colorama PyYAML stevedore futures spreads
Cleaning up...
(.spreads4)simon@Simons-Ubuntu:~$ >>^C
(.spreads4)simon@Simons-Ubuntu:~$ spread configure
Please select a device driver from the following list:
  [1]: chdkcamera
  [2]: a2200
Select a driver: 2
Selected "a2200" as device driver
Please select your desired plugins from the following list:
    1: scantailor
    2: web
    3: tesseract
    4: djvubind
    5: gui
    6: autorotate
    7: intervaltrigger
    8: hidtrigger
    9: pdfbeads
Select a plugin (or hit enter to finish): 
stevedore.extension: Could not load 'a2200': No module named usb
stevedore.extension: No module named usb
Traceback (most recent call last):
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/stevedore/extension.py", line 134, in _load_plugins
    invoke_kwds,
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/stevedore/named.py", line 95, in _load_one_plugin
    ep, invoke_on_load, invoke_args, invoke_kwds,
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/stevedore/extension.py", line 146, in _load_one_plugin
    plugin = ep.load()
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/distribute-0.6.24-py2.7.egg/pkg_resources.py", line 1989, in load
    entry = __import__(self.module_name, globals(),globals(), ['__name__'])
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/spreadsplug/dev/chdkcamera.py", line 11, in <module>
    import usb
ImportError: No module named usb
spreads encountered an error:
Traceback (most recent call last):
  File "/home/simon/.spreads4/bin/spread", line 39, in <module>
    cli.main()
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/spreads/cli.py", line 451, in main
    args.subcommand(config)
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/spreads/cli.py", line 158, in configure
    plugin.set_default_config(config)
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/spreads/plugin.py", line 370, in set_default_config
    driver = get_driver(config["driver"].get(unicode))
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/spreads/plugin.py", line 348, in get_driver
    name=driver_name)
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/stevedore/driver.py", line 31, in __init__
    invoke_kwds=invoke_kwds,
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/stevedore/named.py", line 44, in __init__
    self._init_plugins(extensions)
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/stevedore/driver.py", line 66, in _init_plugins
    (self.namespace, name))
RuntimeError: No u'spreadsplug.devices' driver found, looking for u'a2200'

(.spreads4)simon@Simons-Ubuntu:~$ spread configure
Please select a device driver from the following list:
  [1]: chdkcamera
  [2]: a2200
Select a driver: 2
Selected "a2200" as device driver
Please select your desired plugins from the following list:
    1: scantailor
    2: web
    3: tesseract
    4: djvubind
    5: gui
    6: autorotate
    7: intervaltrigger
    8: hidtrigger
    9: pdfbeads
Select a plugin (or hit enter to finish): 2
    1: scantailor
  x 2: web
    3: tesseract
    4: djvubind
    5: gui
    6: autorotate
    7: intervaltrigger
    8: hidtrigger
    9: pdfbeads
Select a plugin (or hit enter to finish): 
spreads encountered an error:
Traceback (most recent call last):
  File "/home/simon/.spreads4/bin/spread", line 39, in <module>
    cli.main()
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/spreads/cli.py", line 451, in main
    args.subcommand(config)
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/spreads/cli.py", line 158, in configure
    plugin.set_default_config(config)
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/spreads/plugin.py", line 368, in set_default_config
    pluginmanager = get_pluginmanager(config)
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/spreads/plugin.py", line 342, in get_pluginmanager
    name_order=True)
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/stevedore/named.py", line 43, in __init__
    invoke_kwds)
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/spreads/plugin.py", line 76, in _load_plugins
    ext = self._load_one_plugin(ep, *args, **kwargs)
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/stevedore/named.py", line 95, in _load_one_plugin
    ep, invoke_on_load, invoke_args, invoke_kwds,
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/stevedore/extension.py", line 146, in _load_one_plugin
    plugin = ep.load()
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/distribute-0.6.24-py2.7.egg/pkg_resources.py", line 1989, in load
    entry = __import__(self.module_name, globals(),globals(), ['__name__'])
  File "/home/simon/.spreads4/local/lib/python2.7/site-packages/spreadsplug/web/__init__.py", line 4, in <module>
    from flask import Flask
ImportError: No module named flask
