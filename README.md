# Blue Iris Polyglot
This is the Blue Iris Node Server for the ISY Polyglot V3 interface.  
(c) fahrer16 aka Brian Feeney.  
MIT license. 

Blue Iris uses a JSON API documented in the software's help file.  See the Blue Iris website here: http://blueirissoftware.com/.
The Polyglot v2 Template written by Einstein42 was used as a template: https://github.com/Einstein42/udi-polyglot-interface
The Blue Iris python project developed by magapp was used as an example for utilizing the Blue Iris JSON API: https://github.com/magapp/blueiriscmd
This node server will import cameras as ISY Nodes, continuously poll for new events, and allow for commands to be issued to cameras.


# Installation Instructions:
1. Install the Blue Iris node server from the Polyglot v3 Node Server Store.
2. Configure the node server with the Blue Iris server info (see below)

## Polyglot Custom Configuration Parameters
* REQUIRED: Key:'host' Value: The IP address or host name of the Blue Iris server.  If port 80 is not used, add the port into the host value. i.e. "192.168.1.100:81", "BlueIrisServer:90", etc...
* REQUIRED: Key:'user' Value: The Blue Iris user name to be used when connecting to Blue Iris.  This user will need to have administrator access in order to be able to trigger cameras.
* REQUIRED: Key:'password' Value: The password of the Blue Iris user.
 
## Version History:
* 1.0.0: Initial Release
* 1.0.1: Corrected "bool" editor in profile
* 1.1.0: Added command to set server profile
* 1.2.0: Added "Disconnected" state to Blue Iris Server Status displayed in ISY if the Blue Iris server does not respond to a request for its status.  Also added 'requests' to requirements file so it will be automatically installed if not already present.
* 1.3.0: Corrected "cmd" function to operate with Blue Iris v5.  Added command to report drivers on connection.
* 1.3.1: Corrected default polyglot connection status
* 1.3.2: Correct server profile and status on controller node
* 2.0.0: Ported to work on PG3
