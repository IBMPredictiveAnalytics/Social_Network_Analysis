## IBM SPSS Modeler Server Social Network Analysis installation

IBM SPSS Modeler Server Social Network Analysis adds the ability to perform social network analysis to
the IBM SPSS Modeler Server environment. IBM SPSS Modeler Server Social Network Analysis efficiently
processes massive amounts of network data, which may include millions of individuals and relationships,
into a relatively small number of fields for further analyses. es. IBM SPSS Modeler Server Social Network
Analysiscan handle all of the analytical processing itself, or it can function in a clustered environment
with nodes sharing the computational load.  

## Installing on Windows systems
### Prerequisite:
* IBM SPSS Modeler Server Social Network Analysis must be installed to the IBM SPSS Modeler Server installation location.
* JRE installed  (Java 8 is prefer).
* Python installed (Python 2.6 and upper is prefer).

### Steps:
1. Get your modeler's version from "Help-About"
2. Download the SNA package from https://github.com/IBMPredictiveAnalytics/Social_Network_Analysis/${YOUR_MODELER_VERSION}/VC9_64
3. Copy the MPICH2, TABI, ext and Demos directory to Modeler installation folder 
4. Copy MPICH2/bin dll files into C:\windows\system32 directory
5. Add TABI and MPICH2/bin to system path.
6. Run smpd.exe in command from MPICH2\bin.
    ```
    smpd.exe -install
    ```
    
7. Open Modeler and execute SNA stream.   ​

## Installing on Linux systems

### Prerequisite:
* IBM SPSS Modeler Server Social Network Analysis must be installed to the IBM SPSS Modeler Server installation location.
* JRE installed  (Java 8 is prefer).
* Python installed(Python 2.6 and upper is prefer).

### Steps:
1. Login as root.
2. Get your modeler's version.
3. Download the SNA package from https://github.com/IBMPredictiveAnalytics/Social_Network_Analysis/${YOUR_MODELER_VERSION}/Linux64
4. Copy the MPICH2, TABI, ext and Demos directories to the Modeler installation folder ( for example /root/IBM/SPSS/Modeler/${YOUR_MODELER_VERSION}/SPSSModeler.app/Contents)
5. Create software links 
    
    ```
    ln -snf  ${YOUR_MODEL_INSTALLED_DIERECTORY}/TABI/pmlexec /usr/bin/pmlexec
    ln -snf ${YOUR_MODEL_INSTALLED_DIERECTORY}/TABI/tabi-loader /usr/bin/tabi-loader
    ln -snf ${YOUR_MODEL_INSTALLED_DIERECTORY}/MPICH2/bin/* /usr/bin/
    cd /usr/bin
    ls -al tabi-loader pmlexec
    (if pmlexec can not execute, chmod 777 on pmlexec).
```
6. setup MPICH2 config file
    * cd ${YOUR_USER_HOME}
    * touch mpd.conf
    * chmod 600 mpd.conf
    * vi mpd.conf
    * secretword=***(type your password)
    * run mpdboot or mpdroot
7.  Open modeler and execute SNA stream.


## Installing on Mac systems

### Prerequisite:
* IBM SPSS Modeler Server Social Network Analysis must be installed to the IBM SPSS Modeler Server installation location.
* JRE installed  (Java 8 is prefer).
* Python installed(Python 2.6 and upper is prefer).
* Run "csrutil disable" and close SIP (System Integerity Protection).

### Steps:

1. Get your modeler's version from "Help-About"
2. Download the SNA package from https://github.ibm.com/ruiwcdl/sna_installer/${YOUR_MODELER_VERSION}/MacOS64
3. Copy the MPICH2, TABI, ext and Demos to Modeler installation folder ( for example /Applications/IBM/SPSS/Modeler/${YOUR_MODELER_VERSION}/SPSSModeler.app/Contents)
4. Create software links 
    ```
    sudo ln -snf  ${YOUR_MODEL_INSTALLED_DIERECTORY}/TABI/pmlexec /usr/bin/pmlexec
    sudo ln -snf  ${YOUR_MODEL_INSTALLED_DIERECTORY}/TABI/tabi-loader /usr/bin/tabi-loader
    sudo ln -snf  ${YOUR_MODEL_INSTALLED_DIERECTORY}/MPICH2/bin/* /usr/bin/
    cd /usr/bin
    ls -al tabi-loader pmlexec
    (if pmlexec can not execute, chmod 777 on pmlexec).
    ```

5. Setup config file
    * cd YOUR_USER_HOME
    * touch mpd.conf
    * chmod 600 mpd.conf 
    * vi mpd.conf
    * secretword=***(type your password)
    * run mpdboot or mpdroot
6. Open modeler and execute SNA stream.

## Removing from Windows systems

To uninstall IBM SPSS Modeler Server Social Network Analysis, remove the following program files:

*  ${YOUR_MODEL_INSTALLED_DIERECTORY}/ext/bin/pasw.sna
* ${YOUR_MODEL_INSTALLED_DIERECTORY}/ext/lib/pasw.sna
* ${YOUR_MODEL_INSTALLED_DIERECTORY}/MPICH2
* ${YOUR_MODEL_INSTALLED_DIERECTORY}/TABI
* MPICH2/bin dll files in C:\windows\system32 directory

The value of ${YOUR_MODEL_INSTALLED_DIERECTORY} corresponds to the IBM SPSS Modeler Server installation path.

## Removing from Linux and Mac systems

To uninstall IBM SPSS Modeler Server Social Network Analysis, remove the following program files:

* ​     ${YOUR_MODEL_INSTALLED_DIERECTORY}/ext/bin/pasw.sna
* ​     ${YOUR_MODEL_INSTALLED_DIERECTORY}/ext/lib/pasw.sna
* ​     ${YOUR_MODEL_INSTALLED_DIERECTORY}/MPICH2
* ​     ${YOUR_MODEL_INSTALLED_DIERECTORY}/TABI
* ​     /usr/bin/pmlexec
* ​     /usr/bin/tabi-loader

The value of ${YOUR_MODEL_INSTALLED_DIERECTORY} corresponds to the IBM SPSS Modeler Server installation path.