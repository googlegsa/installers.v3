

# Introduction #

This document walks through the installation process and features of Google Connector Installer 2.6.8 and 2.8.0 releases.

### See Also ###

  * [Guide to Connector Release 2.8](http://docs.google.com/a/googleapps.com/document/pub?id=1o400sj6_eQUh5awQJ3r96fKNj_LFkssVJKuSV0oTNnI)
  * [Version 2.6.8 Release Notes](http://code.google.com/apis/searchappliance/documentation/connectors/relnotes/RELEASE_NOTES_2.6.8.txt)
  * Step-by-step instructions for each connector in the [Google Search Appliance Connectors documentation](http://code.google.com/apis/searchappliance/documentation/connectors/).

## 1. Installation of Google Search Appliance Connector for LDAP ##

This section describes the installation prerequisites and installation process for the Google Search Appliance Connector for LDAP.

You can install the connector using an installer that installs Apache Tomcat, a connector manager, and the connector. Google recommends that you use the installer unless you are building the connector manager or connector from the source code or you are installing a patch release that is not packaged with an installer.

Installing the Connector Using the Installer

Before installing the connector using the installer, ensure that Java Development Kit (JDK) 1.5 or 1.6 is installed on the host where you are installing the connector.

The instructions that follow are in two parts. In the first part, you download and uncompress the installer package. In the second, you install the software on the connector host.

The user running the installer must have the following user privileges on the connector host:

On Windows, the user must be an administrator.
On Linux, the user must have sufficient rights to execute the installer file. The user can be a root or nonroot user.
To download and uncompress the installation package:

1.Log in to the host using an account with sufficient privileges to install the software.

2.Start a web browser.

3.Navigate to the Downloads tab of this (Google Search Appliance Connectors) site.

4.Download the correct software distribution package to the host where you are installing the software.

5.Unzip the package.

If you are on Windows, next step and go to the instructions immediately below for installing Tomcat, a connector manager, and the connector.

6.If you are on Linux, follow these instructions.
Open a terminal window and go to the base directory of the GCI.bin file in the extracted folder.

7.Give the GCI.bin file execute permission.

To run the installer in graphical mode, execute the following command:
./GCI.bin LAX\_VM/java\_location\_to\_java

For example, ./GCI.bin LAX\_VM /usr/java/j2sdk1.5.2\_15/bin/java

8. To run the installer in console mode, execute the command in Step 7 above with the -i console argument appended.

Go to the following instructions and proceed from Next step.

To install the connector and its supporting software:

Double-click the installer executable to start the installer.
Click Next.

The Licence Agreement panel appears.

Indicate whether you accept or decline the terms of the license and click Next:

To accept the license, click I accept the terms of the License Agreement.

To decline the terms, click I do NOT accept the terms of the License Agreement.

On the Connector type installation options panel, select Install single connector type and click Next.

On the Select Connector type panel, select LDAP and click Next.

If the Connector Selection panel is displayed, choose Install new Google Connector type and click Next.

On the Connector Configuration panel, enter the name you want to assign to the connector and a port number that is not already used by another application.

The checkbox Start LDAP Connector Service after installation determines whether the connector service start automatically on completion of the installation or must be started manually. It is checked by default.

Click Next.

On the Choose Java Development Kit panel, choose the correct JDK for the connector to use and or click Search for Others if the correct JDK is not in the list.

The connector requires JDK 1.5 or 1.6.

Click Next.

On the Choose Install Folder panel, click Next to accept the default location or click Choose to navigate to a different folder, then          click Next.

On the Choose Shortcut Folder panel, indicate where you want icons created for the connector and click Next.

Read the information on the Preinstallation Summary panel and click Install.

An informational panel indicates that the connector installation is in progress. The Register Connector Manager on the GSA panel is displayed.

Type the search appliance administrator user name in the GSA UserID field.

Type the password for the administrator in the GSA Password field.

Type the search appliance port number in the GSA Port field.

Type in the Connector Manager Name and Description.

Click Next.

The installer indicates whether the installation process succeeded or failed and displays information about connector manager connectivity status, the connector manager URL, search appliance status, and the search appliance display URL.

14. Click Done.

Apache Tomcat starts and deploys the connector manager.

15. If the Start LDAP Connector Service after installation checkbox was left unchecked in earlier Step, start the connector service:

To start the connector as a Windows service, click Start > Programs > GoogleConnectors > connector\_name > Start LDAP Connector Service.

You can choose the commands to stop the service or the console on the same menu.

To start the connector as a console on Windows, click Start > Programs > GoogleConnectors > connector\_name > Start LDAP Connector Console.
To start the connector as a console on Linux, open a terminal window and navigate to the installation location of the connector, then use the following command:

./Start\_LDAP\_Connector\_Console

To stop the connector as a console on Linux, use the following command:

./Stop\_LDAP\_Connector\_Console

Use the instructions in Configuring the Connector to register the connector manager (http://code.google.com/apis/searchappliance/documentation/connectors/260/connector_admin/ldap_connector.html#CreateLDAP) and add the connector on the Admin Console of the Google Search Appliance.

## 2. Installing multiple Google Search Appliance Connectors (SharePoint, LDAP, File System) ##

> <blockquote><b>Note:</b> This feature does not work correctly in version 2.8.0.</blockquote>

You can install the multiple connectors using the connector installer version 2.6.8. That installs a Apache Tomcat, a connector manager, and the multiple connectors (SharePoint, LDAP, File System). Google recommends that you use the installer unless you are building the connector manager or connector from the source code or you are installing a patch release that is not packaged with an installer.

### Installing the Multiple Connectors Using the Installer ###

Before installing the connector using the installer, ensure that Java Development Kit (JDK) 1.5 or 1.6 is installed on the host where you are installing the connector.

The instructions that follow are in two parts. In the first part, you download and uncompress the installer package. In the second, you install the software on the connector host.

The user running the installer must have the following user privileges on the connector host:

On Windows, the user must be an administrator.

On Linux, the user must have sufficient rights to execute the installer file. The user can be a root or nonroot user.
To download and uncompress the installation package:

Log in to the host using an account with sufficient privileges to install the software.

Start a web browser.

Navigate to the Google Search Appliance Connectors downloads page.
Download the correct software distribution package to the host where you are installing the software.

Unzip the package.

If you are on Windows, skip next step and go to the instructions immediately below for Windows.

If you are on Linux, follow these instructions.

Open a terminal window and go to the base directory of the GCI.bin file in the extracted folder.

Give the GCI.bin file execute permission.

To run the installer in graphical mode, execute the following command:
./GCI.bin LAX\_VM/location\_to\_java

For example, ./GCI.bin LAX\_VM /usr/java/j2sdk1.5.2\_15/bin/java

To run the installer in console mode, execute the command in above step with the -i console argument appended.

For example, ./GCI.bin LAX\_VM /usr/java/j2sdk1.5.2\_15/bin/java -i console

Go to the following instructions and proceed from Step below.

To install the connector and its supporting software on Windows/Linux in GUI mode:

Double-click the installer executable to start the installer.

Click Next. The Licence Agreement panel appears.

Indicate whether you accept or decline the terms of the license and
click Next:

To accept the license, click I accept the terms of the License Agreement.

To decline the terms, click I do NOT accept the terms of the License Agreement.

On the Connector type installation options panel, select Install multiple connector types and click Next.

On the Select Connector type panel, select connectors you want to install and click Next.

If the Connector Selection panel is displayed, choose Install new Google Connector types and click Next.

On the Connector Configuration panel, enter the name you want to assign to the connector, a port number that is not already used by another application and Google search appliance IP address.

The checkbox Start Multiple Connector Service after installation determines whether the connector service start automatically on completion of the installation or must be started manually. It is checked by default.

Click Next.

On the Choose Java Development Kit panel, choose the correct JDK for the connector to use and or click Search for Others if the correct JDK is not in the list.

The connector requires JDK 1.5 or 1.6.

Click Next.

On the Choose Install Folder panel, click Next to accept the default location or click Choose to navigate to a different folder, then click Next.

On the Choose Shortcut Folder panel, indicate where you want icons created for the connector and click Next.

Read the information on the Pre-installation Summary panel and click Install.

An informational panel indicates that the connector installation is in progress. The Register Connector Manager on the GSA panel is displayed.

Type the search appliance administrator user name in the GSA UserID field.

Type the password for the administrator in the GSA Password field.

Type the search appliance port number in the GSA Port field.

Type in the Connector Manager Name and Description.

Click Next.

The installer indicates whether the installation process succeeded or failed and displays information about connector manager connectivity status, the connector manager URL, search appliance status, and the search appliance display URL.

Click Done.

Apache Tomcat starts and deploys the connector manager.

If the Start Multiple Connector Service after installation check-box was left unchecked in earlier step, start the connector service:

To start the connector as a Windows service, click Start > Programs > GoogleConnectors > connector\_name > Start Multiple Connector Service.
You can choose the commands to stop the service or the console on the same menu.

To start the connector as a console on Windows, click Start > Programs > GoogleConnectors > connector\_name > Start Multiple Connector Console.
To start the connector as a console on Linux, open a terminal window and navigate to the installation location of the connector, then use the following command:
./Start\_Multiple\_Connector\_Console

To stop the connector as a console on Linux, use the following command:
./Stop\_Multiple\_Connector\_Console

Use the following instructions to add the connector on the Admin Console of the Google Search Appliance.

Configuring the SharePoint Connector: http://code.google.com/apis/searchappliance/documentation/50/connector_admin/sharepoint_connector.html#confconanch

Configuring the LDAP Connector: http://code.google.com/apis/searchappliance/documentation/connectors/260/connector_admin/ldap_connector.html#CreateLDAP

Configuring the File System Connector: http://code.google.com/apis/searchappliance/documentation/connectors/260/connector_admin/file_connector.html#CreateFileCon


## 3. Installing the Google Search Appliance Connector for FileNet 4.5.1 ##

### Before you install the connector ###

Java Runtime Environment (JRE) 5 or 6 installed on the connector manager host.

Ensure that the following files are available in the FileNet Workplace installation in the DOWNLOAD directory or folder:

Jace.jar
activation.jar
javaapi.jar
stax-api.jar
xlxpScanner.jar
xlxpScannerUtils.jar

### Installing the Google Search Appliance Connector for FileNet 4.5.1 ###

This section describes the installation process for the Google Search Appliance Connector for FileNet. You install the connector using an installer that installs Apache Tomcat, a connector manager, and the connector on a host computer.

The instructions that follow are in two parts. In the first part, you download and uncompress the installer package. In the second, you install the software on the connector host.

To download and uncompress the installation package:

Log in to the host using an account with sufficient privileges to install the software.
Start a web browser.
Navigate to the connector download site on code.google.com.
Download the correct software distribution package to the host where you are installing the software.

Uncompress the package.

If you are on Windows, next step and go to the instructions immediately below for installing Tomcat, a connector manager, and the connector on Windows.

1.If you are on Linux, follow these instructions.

2.Open a terminal window and go to the base directory of the GCI.bin file in the extracted folder.

3.To run the installer in graphical mode, execute the following command:
./GCI.bin LAX\_VM/java\_location\_to\_java

For example, ./GCI.bin LAX\_VM /usr/java/j2sdk1.5.2\_x/bin/java

To run the installer in console mode, execute the command in the step 3 above with the -i console argument appended.

Go to the following instructions and proceed.

#### To install Apache Tomcat, a connector manager, and the Google Search Appliance Connector for FileNet: ####

To install the connector and its supporting software:

Double-click the installer executable to start the installer.

Click Next. The Licence Agreement panel appears.

Indicate whether you accept or decline the terms of the license and

click Next:

To accept the license, click I accept the terms of the License Agreement.

To decline the terms, click I do NOT accept the terms of the License Agreement.
> 4. On the Connector type installation options panel, select Install single connector types and click Next.

> 5. On the Select Connector type panel, select FileNet and click Next.

> 6. Select FileNet P8 4.5.1 and click Next.

> 7. On the FileNet 4.5.1 Connector Dependencies panel, navigate to the location of DOWNLOAD folder.

> Ensure that all of the required .jar files (Jace.jar, activation.jar, javaapi.jar, stax-api.jar, xlxpScanner.jar,     xlxpScannerUtils.jar) are in the same folder.

> 8. On the Connector Configuration panel, enter the name you want to assign to the connector, a port number that is not already            used by another application and Google search appliance IP address.
The checkbox Start FileNET Connector Service after installation determines whether the connector service start automatically on completion of the installation or must be started manually. It is checked by default.

> 9. Click Next.

10. On the Choose Java Development Kit panel, choose the correct JDK for the connector to use and or click Search for Others if the correct JDK is not in the list.

The connector requires JDK 1.5 or 1.6.

11. Click Next.

12. On the Choose Install Folder panel, click Next to accept the default location or click Choose to navigate to a different folder, then          click Next.

13. On the Choose Shortcut Folder panel, indicate where you want icons created for the connector and click Next.

14.  Read the information on the Preinstallation Summary panel and click Install.

An informational panel indicates that the connector installation is in progress. The Register Connector Manager on the GSA panel is displayed.

Type the search appliance administrator user name in the GSA UserID field.

Type the password for the administrator in the GSA Password field.

Type the search appliance port number in the GSA Port field.

Type in the Connector Manager Name and Description.

Click Next.

The installer indicates whether the installation process succeeded or failed and displays information about connector manager connectivity status, the connector manager URL, search appliance status, and the search appliance display URL.

15. Click Done.

Apache Tomcat starts and deploys the connector manager.

16. If the Start FileNET Connector Service after installation checkbox was left unchecked in Step 6, start the connector service:

To start the connector as a Windows service, click Start > Programs > GoogleConnectors > connector\_name > Start FileNet45 Connector Service.
You can choose the commands to stop the service or the console on the same menu.

To start the connector as a console on Windows, click Start > Programs > GoogleConnectors > connector\_name > Start FileNet45 Connector Console.
To start the connector as a console on Linux, open a terminal window and navigate to the installation location of the connector, then use the following command:
./Start\_FileNet45\_Connector\_Console

To stop the connector as a console on Linux, use the following command:
./Stop\_FileNet45\_Connector\_Console

17. If you did not register the connector manager from the connector installer, continue with the instructions in this document for Registering a Connector Manager. If you registered the connector manager from the connector installer, continue with the instructions in this document (http://code.google.com/apis/searchappliance/documentation/connectors/260/connector_admin/filenet4_connector.html#deploycm) for Configuring a Connector on the Admin Console.