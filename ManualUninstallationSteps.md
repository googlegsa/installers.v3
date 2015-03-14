## Introduction ##

This document will guide you through steps to manually  un-install connector installed by the Google Connector installer.


## Details ##

**Steps For Windows:**

_Step 1:_ Stop connector service

_Step 2:_ Delete connector service

_Step 3:_ Delete connector folders

_Step 4:_ Registry cleanup

**_Step 1:_** Stop connector service: Connector service can be stopped from

Start menu ->> Program files ->> Google Search Appliance Connectors ->> <_Connector Name_> ->> Stop <_connector type_> Connector Service

OR

Goto Services (Start -->> run -->> services.msc)
and stop the connector service.

**_Step 2:_** To delete connector service, launch command prompt and execute command

SC delete <_Connector service name_>

**_Step 3:_** Delete folder <_installation path_>\<_Connector Name_>

**_Step 4:_** To delete registry entry, follow these steps:

  * Launch Registry Editor : Start -->> Run -->> regedit

  * Goto path My Computer\HKEY\_LOCAL\_MACHINE\SOFTWARE\JavaSoft\Prefs\

  * Delete folder entry /Google/Connectors/<_Connector Name_>

**Steps For Linux:**

_Step 1:_ Stop connector process

_Step 2:_ Delete connector folders

_Step 3:_ Delete connector entries from preferences


**_Step 1:_** To stop connector process, execute the command at <_installation path_>/<Connector Name>


_./Stop\_SharePoint\_Connector\_Console_

**_Step 2:_** Delete connector folders

delete folder <_installation path_>/<Connector Name>

**_Step 3:_** To delete connector entries from preferences

  * Navigate to /etc/.java/.systemPrefs/Google/Connectors/

  * Delete folder <Connector Name>