## IBM SPSS Modeler Server Social Network Analysis installation

IBM SPSS Modeler Server Social Network Analysis adds the ability to perform social network analysis to
the IBM SPSS Modeler Server environment. IBM SPSS Modeler Server Social Network Analysis efficiently
processes massive amounts of network data, which may include millions of individuals and relationships,
into a relatively small number of fields for further analyses. es. IBM SPSS Modeler Server Social Network
Analysiscan handle all of the analytical processing itself, or it can function in a clustered environment
with nodes sharing the computational load.  

## Installing on Windows systems

Note: IBM SPSS Modeler Server Social Network Analysis must be installed to the IBM SPSS Modeler
Server installation location. If IBM SPSS Modeler Server is not installed, the IBM SPSS Modeler Server
Social Network Analysis installation will fail.

To install IBM SPSS Modeler Server Social Network Analysis on Windows Server, perform the following
steps:

1. If you downloaded the product, double-click the downloaded file and extract the installation files. then
   follow the instructions that appear on the screen

   ​

## Installing on Linux systems

Note: IBM SPSS Modeler Server Social Network Analysis must be installed to the IBM SPSS Modeler
Server installation location. If IBM SPSS Modeler Server is not installed, the IBM SPSS Modeler Server
Social Network Analysis installation will fail. To install IBM SPSS Modeler Server Social Network
Analysis, perform the following steps:

1. Log in as root
2. Run the install script corresponding to your Linux environment. Make sure the install script can be executed by root . Use the -i console option to execute the script in console mode. For example,  run the script as follows: sna_server_installer_linux64.bin -i console



## Installing on Mac systems

Note: IBM SPSS Modeler Server Social Network Analysis must be installed to the IBM SPSS Modeler
Server installation location. If IBM SPSS Modeler Server is not installed, the IBM SPSS Modeler Server
Social Network Analysis installation will fail. To install IBM SPSS Modeler Server Social Network
Analysis, perform the following steps:

1. If you downloaded the product, double-click the downloaded file and extract the installation files. then
   follow the instructions that appear on the screen

2. Log in as root

3. After installing the Social Network Analysis, Create below links for TABI and MPICH2 by root user, For example, run the scripts as follows:

    ln -snf  /Applications/IBM/SPSS/Modeler/18.1/SPSSModeler.app/Contents//TABI/pmlexec /usr/bin/pmlexec
    ln -snf  /Applications/IBM/SPSS/Modeler/18.1/SPSSModeler.app/Contents//TABI/tabi-loader /usr/bin/tabi-loader
    ln -snf  /Applications/IBM/SPSS/Modeler/18.1/SPSSModeler.app/Contents//MPICH2/bin/* /usr/bin/

4. Add executable permissions for TABI and MPICH2

   chmod +x /Applications/IBM/SPSS/Modeler/18.1/SPSSModeler.app/Contents/TABI/* 

   chmod +x /Applications/IBM/SPSS/Modeler/18.1/SPSSModeler.app/Contents/MPICH2/bin/*

## Removing from Windows systems

To uninstall IBM SPSS Modeler Server Social Network Analysis, perform the following steps:

1. From the Windows Start menu choose:

   Settings > Control Panel

2. From the Control Panel, choose "Add or Remove Programs".

3. Click "Change or Remove Programs"

4. Select IBM SPSS Modeler Server Social Network Analysis from the list of currently installed programs, and click "Change/Remove". If you have more than one version installed on the computer, be sure to select the version that you want to remove.

   A message will be displayed when the uninstallation process completes.

## Removing from Linux and Mac systems

To uninstall IBM SPSS Modeler Server Social Network Analysis, remove the following program files:

​     $installLoc/ext/bin/pasw.sna

​     $installLoc/ext/lib/pasw.sna

​     $installLoc/MPICH2

​     $installLoc/TABI

​     /usr/bin/pmlexec

​     /usr/bin/tabi-loader

The value of $installLoc corresponds to the IBM SPSS Modeler Server installation path.