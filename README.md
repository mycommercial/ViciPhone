# ViciPhone
An improved webphone for the Vicidial Call Center Suite.

This code is a fork from the original code by Michael Cargile (https://github.com/vicimikec/ViciPhone), and as such contains the following enhancements:

- Uses SIPJS version 0.15.11 as of 2021-02-27, supporting all modern browsers.
- Allows SIPJS to be downloaded from a CDN as minified version.
- Support for multiple translations. Currently adds spanish support, but is open for more.
- Can call the agent instantly after the webphone has loaded (like a regular softphone), saving time and human error.

Several other improvements can be read in the commits logfile.

### WebRTC template
To use it on Vicidial, you must set up a webrtc template as follows:
```
type=friend
host=dynamic
encryption=yes
icesupport=yes
directmedia=no
transport=wss
dtlsenable=yes
dtlsverify=no
dtlscertfile=/PATH/TO/YOUR/SSL/CERT
dtlsprivatekey=/PATH/TO/YOU/SSL/KEY
dtlssetup=actpass
rtcp_mux=yes
```
The field ```rtcp_mux``` is the most important change since Viciphone 1.0, so that is a must.
