# -LinuxCnc-OpenDDS-Work


Initial openDDS install Guide and the goals of this project

    12/18/2022
    
    I have created my install guide for openDDS on my Linux Mint 20
    development system for LinuxCnc. This file is located in the
    Install-Notes folder with the "first.dds.install".
    
    
    This is my project for using openDDS for use within LinuxCnc
    to handle all communications and data movement between LinuxCnc
    internal modules, and to provide network wide access to all data
    being routed to and from those individual modules using the
    openDDS standard. 

    The final step if successful would be to completely
    remove NML and all its associated code after everything
    has been rerouted to methods that are available in openDDS. 

    My initial work is expected to start in the Task and IO modules.
    Some commands routed to the IO module are simple on/off types
    which makes convering those a bit simpler. Those commands
    will be modified to route to and from openDDS. From there
    other will be modified and tested.

    Each of the modules metioned above has communication channels
    that link the modules together for data that needs to move
    netween them. Providing communication channels is what openDDS 
    is designed  to do and openDDS can route the data anywhere
    it is required both inside and outside of an application.

    Drawbacks:
    ----------

    This involves a great deal of work in analyzing each functional
    module of LinuxCnc and fully understand what each module
    requires and each communcates with other modules,
    such as HAl, IO, Motion and so on.
 
    openDDS does seem to have a drawback due to its size in
    comparison to the size of LinuxCnc itself. This drawback may
    be completly wiped out by the increase in flexibility it offers.

    A second issue may appear for some users of small single board
    computers that run LinuxCnc that do not have the resources
    required to run openDDS.

