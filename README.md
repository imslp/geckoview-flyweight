# geckoview-flyweight
Geckoview can be built on Windows or Linux. This instruction is mainly for Linux and tested on Ubuntu. To build it on Windows, you'll have to install MozillaBuild, compilers, and some other tools.

1. System Preparation

    1.1 Install Python
    
    Install Python using the system package manager:

    ``` sudo apt-get install curl python3 python3-pip ```

    1.2. Install Mercurial

    ``` python3 -m pip install --user mercurial ```

    You can test that Mercurial is installed by running

    ``` hg version ```
    
2. Bootstrap the build environment

    Go to the root of the source directory and run the following command. It'll install dependencies and prepare the build environment.

    ``` ./mach bootstrap ```

    
    Among the list of projects, choose *"4. GeckoView/Firefox for Android"*

3. Build

    - Copy the mozconfig file from ./trick/mozconfig (or ./trick/mozconfig-flyweight and rename it to mozconfig) and replace the one in the root directory.
    - Run ``` ./mach build ``` to build Geckoview

    Note that building Geckoview is quite complicated and takes time. Sometimes rebuilding the source also produces errors.