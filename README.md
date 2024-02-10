
### Documentation ###

This is the link to download OMNet++ https://omnetpp.org/download/
This is a very good documentation of OmNET++ https://doc.omnetpp.org/omnetpp5/manual/
This is where i got instructions to download FLora https://flora.aalto.fi/   --- or here https://omnetpp.org/download/models-and-tools

# GOAL #
Vanilla LoraWAN running on Omnet++  (Ubuntu VM)

# Environment #

OS: Ubuntu 22.04
Omnet++: 6.0.2
LoraWAN: ?

# Tasks # 

1. Oracle VirtualBox installed - done
2. VM Ubuntu  - 4GB RAM - done
3. Omnet++  6.0.2 installed 
4. LoraWan: installation
5. fork Flora - https://github.com/Yanek11/flora - done



3. Omnet++ installation

********************
version I
installation manual
https://omnet-manual.com/install-omnet-ubuntu-20-04/
* ubuntu 20.04

### sudo apt-get update
result: OK

### sudo apt-get install build-essential gcc g++ bison flex perl tcl-dev tk-dev libxml2-dev zlib1g-dev default-jre doxygen graphviz libwebkitgtk-1.0-0
@ error @
E: Package 'libwebkitgtk-1.0-0' has no installation candidate
solution?
https://community.hitachivantara.com/discussion/libwebkitgtk-10-0-on-ubuntu-2204-lts

@@ error
repo cannot be verified @
solution?
https://techpiezo.com/linux/fixed-updating-from-such-a-repository-cant-be-done-securely/
adding to /etc/apt/sources.list
### deb [trusted=yes] http://cz.archive.ubuntu.com/ubuntu bionic main universe
### sudo apt-get update
### sudo apt-get install libwebkitgtk-1.0-0
### sudo apt-get install build-essential gcc g++ bison flex perl tcl-dev tk-dev libxml2-dev zlib1g-dev default-jre doxygen graphviz libwebkitgtk-1.0-0
result: OK

### sudo apt-get install qt4-qmake libqt4-dev libqt4-opengl-dev openscenegraph libopenscenegraph-dev openscenegraph-plugin-osgearth osgearth osgearth-data libosgearth-dev
@@ error 
GDAL not installable

solution
https://super-unix.com/ubuntu/ubuntu-ubuntu-20-04-importerror-no-module-named-gdal/

wget all 

### sudo apt install ./*libgdal*.deb

###
cat <<EOF | sudo tee /etc/apt/preferences.d/pin-gdal
Package: gdal-data
Pin: version 2.2.3+dfsg-2
Pin-Priority: 1337

Package: libgdal20
Pin: version 2.2.3+dfsg-2
Pin-Priority: 1337

Package: python-gdal
Pin: version 2.2.3+dfsg-2
Pin-Priority: 1337
EOF
###
********************

********************
II 
installation manual
https://medium.com/@computerscienceengineering/omnet-6-0-installation-steps-4a724fbbb09d
https://drive.google.com/file/d/1hi2CaZKtXKOJoHtb8dxqOuvAYe3op_KO/view
