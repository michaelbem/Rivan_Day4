** NOTE **

Run python file in VSCODE with the Script folder opened to avoid any issues with the CWD(Current Working Directory)

When using telnet, the IOU Web Interface will connect you to the line console 0 of the specified device, which means only 1 connection is allowed.
When running the python script make sure there no established connections to any of the device in RSTLab.

//
ConnectHandler(
device_type = cisco_ios_telnet
secret = pass
)
//


Requirements for Activity
1. RSTHayupLab
2. VMware
3. VScode
4. Install VScode Extensions

	VScode Extension					Publisher
	___________________________________________________
	Github CoPilot  					Github.com
	autoDocstring - Python Docstring  	Nils Werner
	Python Snippets  					Ferhat Yalçın
	AREPL for python  					Almenon
	Better Comments  					Aaron Bond			
	Python Indent						Kevin Rose
	Python Test Explorer				Little Fox Team
	___________________________________________________

4. Python
5. SecureCRT		
****

Upgrade Libraries
Create a folder then open it on VScode

	create File: update.py
	*Refer to updateLib.py	
	
___________________________________________________

(Not Needed if you are simply running the script) 
 TextFSM Templates - only for properly formatting show commands to be stored as a variable in python script
		How to install TextFSM Templates:
		 1. create a folder in a directory of your choice
		 2. In that folder,
				git clone https://github.com/networktocode/ntc-templates
		 3. In Environment Variables,
				Create a new variable
					Variable name : NET_TEXTFSM
					Variable value : the path file of the templates folder in the ntc_templates\ntc_templates
						if you're still having trouble installing here's a link: https://ntc-templates.readthedocs.io/en/latest/admin/install/
	

NOTES:
The connection is TELNET because you cannot SSH
	Therefore, connectHandler must have: 
		device_type = cisco_ios_telnet
	
	and .enable() command must be used.

When accessing a device from outside the Cisco IOU ip address, the Cisco IOU Web interface will connect you the console 0 of each device, 
which means you need to make sure there are no connections to any of the devices before running the python script. 


Possible Errors:
Format strings must alternate between single then double quotes.
	f'I am a {format["string"]}'
