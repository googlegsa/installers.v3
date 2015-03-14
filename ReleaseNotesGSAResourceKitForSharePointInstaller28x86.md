# Release Notes for the GSA Resource Kit for SharePoint Installer v2.8 32-bit #


This document contains the release notes for Google Search Appliance Resource Kit for SharePoint 2.8 (32-bit).
The following sections describe the release in detail and provide information that supplements the main documentation.
See the Issues Tab on the Code Site for the current list of known issues and workarounds.

Web Site: http://code.google.com/p/google-enterprise-connector-sharepoint/issues/list


**Release 2.8, October 2011**


**INTRODUCTION**

---

This is an early access release for wide evaluation and usage. Your feedback is important to us. Keep in mind that we are continuing to work on Google Search Appliance Resource Kit for SharePoint 2.8 (32-bit) and things may change in the future.

**Pre-requisites**

---

SharePoint 2007 (WSS 3.0, MOSS 2007) or SharePoint 2010 server.

Windows Server 2003 Enterprise server/Windows Server 2008 Enterprise server.

Microsoft .Net Framework 2.0.

IIS 6.0/IIS 7.0.

**Note:**

---

If you have already installed Google Services for SharePoint or Google Search Box for SharePoint earlier using the old installer (i.e. GSS.msi or GSBI.msi or Google Search Appliance Resource Kit for SharePoint 1.x.x), please uninstall them before trying the Google Search Appliance Resource Kit for SharePoint 2.8 installer.

**Features**

---

1. Google Search Appliance Resource Kit for SharePoint 2.8 (32-bit) installer bundles following components:

a) Google Search Box for SharePoint 2.6.10: It represents Google Search Box for SharePoint. When selected, the Google Search Box for SharePoint is enabled on all SharePoint web applications on a machine, which share the same search control.

b) Google Services for SharePoint 2.8: The Google Services for SharePoint are custom web services used by the Google Search Appliance Connector 2.8 for Microsoft SharePoint 2007 and Microsoft SharePoint 2010.

c) GSA Resource Kit for SharePoint: It represents the following utilities:

> -Google Search Box for SharePoint Test Utility : It is used to verify the Google Search Box for SharePoint parameters, cookies and headers.

> -GSA Security SPI Simulator: It is used to test Google SAML Bridge for Windows without involving the complexity of the search appliance. Once you know that the SAML Bridge works, you can reconfigure it to work with the search appliance.

> -Google SAML Bridge for Windows 2.8: It enables Google Search Box for SharePoint to perform search on NTLM contents.

**Issues fixed in the Google Search box SharePoint 2.6.10:**

---


1. [4326112](Issue.md) - Google watermark is present in GSA SearchBox for SharePoint even when it contains text

2. [4325126](Issue.md) - Default Search type changed form secure to public in latest GSA SearchBox for SharePoint 2.6.8

3. [4343920](Issue.md) - GSA SearchBox for SharePoint front-end style-sheet does not have "Search Tips" link

4. [4310682](Issue.md) - Effective space utilization of results displayed by GSA SharePoint SearchBox


**SharePoint Version Compatibility**

---


**Google Services for SharePoint 2.8**

SharePoint Server 2010

SharePoint Foundation Server 2010


Microsoft Office SharePoint Server 2007 (MOSS 2007)

Microsoft Windows SharePoint Services 3.0 (WSS 3.0)

**Google Search box for SharePoint 2.6.10**

Microsoft Office SharePoint Server 2007 (MOSS 2007)

Microsoft Windows SharePoint Services 3.0 (WSS 3.0)


**Note:**

SharePoint 2010 requires 64-bit processor. Hence, this installer will not work for SharePoint 2010.

**Platform Support**

---

Google Resource Kit for SharePoint 2.8 (32-bit) can be installed on Windows Server 2003 Enterprise (32-bit)/Windows Server 2008 Enterprise (32-bit) Operating Systems.

**Note:**

---


There are separate installers for 32-bit and 64-bit Operating Systems.


**Certified Against**

---

1. Microsoft Windows Server 2008

Enterprise Edition

Intel  Xeon  CPU

E5504 @ 2.00GHz, 4.00 GB of RAM


2. Microsoft Windows Server 2003

Enterprise Edition

Intel  Xeon  CPU

E5504 @ 2.00GHz, 2.00 GB of RAM

**Known Issues/Limitations**

---


1. The Installer does not validate the port number for 'GSA Resource Kit for SharePoint'. User needs to enter a valid non-conflicting port during installation. Assigned port number could be changed even after Installation directly through IIS Manager.

2. The Installer does not validate the 'Artifact Consumer' URL on "Google SAML Bridge for Windows - Configuration Wizard".

3. Cancelling Installer does not intiate rollback of the installed components. You need to run installer again in 'remove' mode to clean up the installed components.

4. If a new web application is added after the installation of search box,this web application does not show search box.