* **************** *
# TWAIN SANE Interface for MacOS (10.10 and Next Versions) #
## Make your OLD Scanner back to Service !! ##
* **************** *
This Repository contains corrected SDK for recent MACOS(10.10-10.13) and was newly improved in form of bundled Package Installation.  
All original sources (1.0.25) are originaly only for MacOS 10.10 installation and was get from its Ancestral MacOS Maintener [ Mattias Ellert's Official site ] 

For Other Operating Systems (Linux, Windows, Beos/Zeta, SunOS ...) 
And Further Resivions may/will be designed around more appropriate versions from Offical SANE Project's Site

**** For Documentation and more Information, Please Refer to : [http://sane-project.org/] Official Site ****

* **************** *
## Installation and USAGE ##
* **************** *
Download packages
    
  For (Yosemite)
  
    MACOS-10.10
      NOT TESTED / NOT CURRENTLY AVAILBLE
      L__ libusb-(PKGVERSION)-MACOS-10.10-10.10-SDK-(SDKVERSION).pkg
      L__ gettext-(PKGVERSION)-MACOS-10.10-10.10-SDK-(SDKVERSION).pkg
      L__ sane-backends-(PKGVERSION)-MACOS-10.10-10.10-SDK-(SDKVERSION).pkg 
      L__ TWAIN-SANE-Interface-(PKGVERSION)-MACOS-10.10-10.10-SDK-(SDKVERSION).pkg
  
  For (Captain / Sierra)
      
    MACOS-10.11-10.12
      L__ libusb-(PKGVERSION)-MACOS-10.11-10.12-SDK-(SDKVERSION).pkg
      L__ gettext-(PKGVERSION)-MACOS-10.11-10.12-SDK-(SDKVERSION).pkg
      L__ sane-backends-(PKGVERSION)-MACOS-10.11-10.12-SDK-(SDKVERSION).pkg
      L__ TWAIN-SANE-Interface-(PKGVERSION)-MACOS-10.11-10.12-SDK-(SDKVERSION).pkg
  
  For ( HighSierra )

    MACOS-10.13
      NOT TESTED / NOT CURRENTLY AVAILBLE
      L__ libusb-(PKGVERSION)-MACOS-10.13-10.13-SDK-(SDKVERSION).pkg
      L__ gettext-(PKGVERSION)-MACOS-10.13-10.13-SDK-(SDKVERSION).pkg
  
  For ( Mojave )
  
    MACOS-10.14 
      NOT TESTED / NOT CURRENTLY AVAILBLE
  
  All Versions
  
    SANE-Preference-Pane-(PKGVERSION)-MACOS-(MACOSMINORVERSION)-(MACOSMAJORVERSION)-SDK-(SDKVERSION).pkg
  
Install all packages and follow instructions

* **************** 
### Test scanner : 

- Open Terminal.app 
and enter the following command :
```sh
scanimage --format jpg > test.jpg
```
Your scanner should react and make a picture sample (100px X 100px)

* **************** 
## Note about TWAIN Support ##
* **************** 
Beside some fact, We Love Twain integration.
Adobe annouced in 2015 there is no Further support in Photoshop for TWAIN Integration, dues to "Some Resitrictions Caused by Twain", that means Money not in us Pokets 
Apple make it more difficult to interfacing with ImageCapture.app


* **************** 
# About Remote / Shared Scan
## Server sonfiguration
* **************** 

Server side configuration taken [here](https://forum.keenetic.net/topic/240-sane-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-usb-%D0%BC%D1%84%D1%83-%D0%B8%D0%BB%D0%B8-%D1%81%D0%BA%D0%B0%D0%BD%D0%B5%D1%80%D0%B0/?do=findComment&comment=3599)

* **************** 
## Client configuration
* **************** 

- Download and Install all packages
- Modify sane config file

```sh
sudo vi /usr/local/etc/sane.d/net.conf
```

Add IP of your Sane scaner at the last line

```sh
# This is the net backend config file.

## net backend options
# Timeout for the initial connection to saned. This will prevent the backend
# from blocking for several minutes trying to connect to an unresponsive
# saned host (network outage, host down, ...). Value in seconds.
# connect_timeout = 60

## saned hosts
# Each line names a host to attach to.
# If you list "localhost" then your backends can be accessed either
# directly or through the net backend.  Going through the net backend
# may be necessary to access devices that need special privileges.
# localhost
192.168.1.1  # Add this line with correct IP address
```
* ******************
## Test scan

```sh
scanimage --format jpg > test.jpg
```
* ******************
** Thanks to Mattias Ellert, for all this Year of Maintaining SANE TWAIN for MacOS **

[ Mattias Ellert's Official site ]:http://www.ellert.se/twain-sane/
