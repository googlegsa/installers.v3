# Release Notes for the GSA Connectors Installer v2.6.8 #

Release Notes


Google Connector Installer

This document contains the release notes for Google Connector Installer.
The following sections describe the release in detail.

Release 2.6.8, February, 2011


Introduction:

---

This release includes the following versions of each component.

- Google Search Appliance Connector Manager: v 2.6.6
- Google Search Appliance Connector for Microsoft SharePoint: v 2.6.8
- Google Search Appliance Connector for LDAP: v 2.6.0
- Google Search Appliance Connector for Open Text Livelink: v 2.6.6
- Google Search Appliance Connector for EMC Documentum Content Server 5.x: v 2.6.6
- Google Search Appliance Connector for EMC Documentum Content Server 6.0: v 2.6.6
- Google Search Appliance Connector for IBM FileNet P8 3.5.2: v 2.6.0
- Google Search Appliance Connector for IBM FileNet P8 4.0,4.5: v 2.6.0
- Google Search Appliance Connector for IBM FileNet P8 4.5.1: v 2.6.0
- Google Search Appliance Connector for File Systems: v 2.6.0
- Google Search Appliance Connector for Databases: v 2.6.0-Preview

Please refer to respective release notes of each component for more information.
Keep in mind that we are continuing to work on Google Connector Installer and
things may change in the future.

Platform Support

---

The connector can be installed on x86/x64 Windows (2003/2008) and Linux environments.

Certified Against

---

32-bit:

---

Microsoft Windows Server 2008
Windows Server Standard Service Pack 2
Processor: Intel(R) Xeon(R) CPU    E5504 @ 2.00 GHz 2.00 GHz
Memory (RAM): 2.00 GB
System Type: 32-bit Operating System

Microsoft Windows Server 2003
Enterprise Edition
Intel(R) Xeon(R) CPU
E5504 @ 2.00GHz, 2.00 GB of RAM

Red Hat Linux 5 (32-bit)
Intel(R) Xeon(R) CPU
E5504 @ 2.00GHz, 2.00 GB of RAM

GSA version 6.8.0.G.30

64-bit:

---

Microsoft Windows Server 2008
Windows Server Standard Service Pack 2
Processor: Intel(R) Xeon(R) CPU    E5620 @ 2.40 GHz 2.39 GHz
Memory (RAM): 4.00 GB
System Type: 64-bit Operating System

Microsoft Windows Server 2008 [R2](https://code.google.com/p/googlesearchapplianceconnectors/source/detail?r=2)
Enterprise x64 Edition
Intel(R) Xeon(R) CPU
E5504 @ 2.00GHz, 4.00 GB of RAM

Microsoft Windows Server 2003
Enterprise x64 Edition
Intel(R) Xeon(R) CPU
E5504 @ 2.00GHz, 2.00 GB of RAM

GSA version 6.8.0.G.30

FEATURES/ISSUES FIXED IN THIS RELEASE:

---

1) Support for installation of Google Search Appliance Connector for LDAP.
2) Support for installation of multiple connectors (SharePoint, LDAP, File Systems).
3) Support for installation of Google Search Appliance Connector for IBM FileNet 4.5.1.

UPGRADE INSTRUCTIONS:

---

a)Google Search Appliance Connector for Open Text Livelink:

Please refer to respective connector's online documentation. Follow the
installation steps mentioned in the section "Installing the Connector Using
the Installer", however during installation, you need to choose the existing
connector instance that is to be upgraded.

b) Documentum Content Server 5x Connector:

- Stop the connector service

- Browse to '<Path till CATALINA HOME>\webapps\connector-manager\WEB-INF\connectors'
> and rename the folder 'EMC\_Documentum\_Content\_Server\_5.2.5\_5.3\_6.0' to
> 'EMC\_Documentum\_Content\_Server\_5.2.5\_5.3'.

- Edit the file '<Connector Name>.properties' located within the folder
> '\EMC\_Documentum\_Content\_Server\_5.2.5\_5.3\<Connector name>' and
> update the path for the parameter googleConnectorWorkDir to
> <Path till CATALINA HOME>\\webapps\\connector-manager\\WEB-INF\\connectors\\EMC\_Documentum\_Content\_Server\_5.2.5\_5.3\\<connector name>

- Follow the installation steps mentioned in the section "Installing the
> Connector Using the Installer".  However, during installation you need to
> choose the existing connector instance that is to be upgraded.

c) Upgrade is not supported for :
- Google Search Appliance Connector for IBM FileNet P8 3.5.2
- Google Search Appliance Connector for IBM FileNet P8 4.0,4.5
- Google Search Appliance Connector for IBM FileNet P8 4.5.1
- Google Search Appliance Connector for Databases
> with this release of the installer. Please refer to respective connector's online documentation for more details.

KNOWN ISSUES/LIMITATIONS:

---

1) Installer does not support '~' property while specifying dependency file locations.
2) Installer does not support '-' while entering connector instance name.
3) Installer does not support upgrade (for connectors) from EMC\_Documentum\_Content\_Server\_5.2.5\_5.3\_6.0 to EMC\_Documentum\_Content\_Server\_6.0.
4) On Linux, installer does not display JDK/JRE on Choose JVM panel. On clicking Next, installer proceeds to next step even if no JRE/JDK is selected.
Suggested work-around: Click on "Choose another" button and select the required JDK/JRE or click on "Search for others" button to get a complete list of JDK/JRE installed on the machine and choose the required JDK/JRE.
5) JRE 1.6 is not displayed on "Choose JVM" Panel.
Suggested work-around: Click on "Choose another" button and select the required JDK/JRE or click on "Search for others" button to get a complete list of JDK/JRE installed on the machine and choose the required JDK/JRE.
6) On Linux, Test connectivity feature is available only in GUI mode and not in console mode.
7) On Linux, in case of upgrade from 1.3.2 to 2.x, duplicate folders are created for <Install Directory>/Licenses/ConnectorManager and <Install Directory>/Docs.
8) On Linux, you need to be a root user to run the installer.
9)In case of Upgrade of FileNet 4.0 connector from 2.x to 2.6 or above, WSI option is not added to the service.bat (Windows) and catalina.sh (Linux).
> Suggested Workaround Steps for Service.bat (Windows):
  1. Append "-Dwasp.location=<SELECTED WSI FOLDER PATH>" in "%EXECUTABLE%" //US//, after "-Djava.util.logging.config.file" option.
> 2. Go to the folder INSTALL\_LOCATION/Tomcat/bin in command prompt.
> 3. Run command "Service.bat uninstall" to uninstall the service.
> 4. Run command "Service.bat install" to install the service.

> Suggested Workaround Steps for catalina.sh (Linux):
  1. Stop the connector service
> 2. Append "-Dwasp.location=<SELECTED WSI FOLDER PATH>" after "JAVA\_OPTS="$JAVA\_OPTS -Xms256m -Xmx1024m"
> 3. Start the connector service.
10) For Database Connector, if user continuously go on adding jars then, no scroll bar appears and finally "Add More" button disappears.
11) For 64-bit, GCI works only with JDK and is not supported for JRE.
12) If user skips the "Register Connector-Manager on GSA" panel and clicks "Previous" and "Skip" again, then GCI exits.
13) In GCI Console mode an extra "`*`" appears on "Register Connector Manager on GSA" panel.
14) After upgrade with 2.6.x over 2.0.x versions, older menus i.e. "Test Connector Manager Connectivity" and "Test Google Search Appliance Connectivity" does not get deleted from Start Menu for Windows and "Test\_Connector\_Manager\_Connectivity" and "Test\_Google\_Search\_Appliance\_Connectivity" does not get deleted from connector's home directory for Linux.
15) Connector Name entered on "Connector Configuration" panel remains unchanged if "Connector type" is changed by navigating "Next" and "Previous" to the "Select Connector" panel.
16) If CATALINA\_HOME is already set in system's environment, then the installed connector service does not start.
17) On "Register Connector Manager with GSA" panel, if any error message occurs on clicking "Next", then clicking "Skip" button installer dis-appears. No summary panel will be displayed. For E.g.:
> a. Execute Google Connector Installer. Continue installation process till "Register Connector Manager with GSA" panel appears. Click Next button without entering any password.
> b. An error message is displayed that Password should not be left blank.
> c. Skip GSA registration by clicking Skip button.
> d. Connector installation is successful, however, installer dis-appears. No summary panel will be displayed.
18) Few panels of Google Connector Installer are not localized.
19) After upgrade with 2.6.x over 2.x versions, an empty menu with name "Google Search Appliance Connector 2.6" is created under Start Menu Program Files. The same is applicable if upgrade is done on Windows x64 based environments
20) "Add More" button on "Database Connector Dependencies" panel does not get enabled after Deleting the last row. You need to re-browse and select the jar to get it enabled.
21) In Console/UI mode on Windows, after successful uninstallation of a connector, a message "Some items could not be removed" is displayed. This is typically the case if more than one connector installations share the same shortcut folder
22) After upgrade with 2.6.0 over the lower versions, Update complete message does not contain the version to which it is updated, This is observed in GCI console mode.
Eg: "Congratulations!Google Connector(SharePoint1) has been succesfully installed/updated to:   "
23) The page to register LDAP connector not appearing after installing connector manager on LINUX.
24)	While upgrading connector with another type of connector,  shortcut labels are not getting modified with new Connector type.
25)	While upgrading the connector with latest version, the shortcuts are not getting moved from old Shortcut group to new Shortcut group.  Example : Connector Installed with GCI 2.6 0, upgrading with GCI 2.6 8, Shortcuts  are note getting moved from <Shortcut Folder>2.6.0 to <Shortcut Folder>>2.6.8.
26)	On Console , while upgrading the connector, from the Upgrade summary message if we go back to select another JVM error message "Invalid JVM" is displayed.
27)	While upgrading one type of connector with other type, install and uninstall count for preview type of connector are not getting modified in registry entries.
28)	For very first installation of any type of connector, Uninstall count for connector is initializing to 1 in registry entries.
29)	For UI Mode, The page to display the already installed connectors does not display connector type and version of connector.
30) Warning message not displayed, when we type N during the License Agreement in Console mode Installation.
31) Start Connector Manager after installation check box is missing in Linux installer.
32) Connector manager is not running while we click on Run in Terminal option to start the Connector Manager.
33) The version string in the JAR MANIFEST of the LDAP connector is missing a closing right parenthesis.