## _Problem_ ##

Tomcat fails to start when connector is installed on 64-bit windows using installer (GCI).

The Tomcat logs report shows following log messages:

Procrun (2.0.4.0) started

Running Service...

Starting service...

The specified module could not be found.

Failed creating java

ServiceStart returned 1

Run service finished.

Procrun finished.




**Enviornment:**

64 bit Windows 2008 [R2](https://code.google.com/p/googlesearchapplianceconnectors/source/detail?r=2)

## _Solution_ ##

> Check if the file "msvrc71.dll" is present in windows\system directory

> if the file is not present then copy the msvcr71.dll included in JDK 1.6 to
> windows\system directory





## _Problem_ ##

Even if the Java (1.5 or above) is installed, getting  error "Could not find a Valid Java Virtual machine to load" when invoke the Connector Installer.

**Enviornment:**
64 bit Windows 2008 [R2](https://code.google.com/p/googlesearchapplianceconnectors/source/detail?r=2)

## _Solution1_ ##

1) Make sure you have JDK 1.5.x or above installed on your system.

2) From the Console run the Connector Installer using following command.

> GCI.exe LAX\_VM "<path of java>"

> For Example:

> GCI.exe LAX\_VM "C:\Program Files\java\jre6\bin\java.exe"


**Reference:**

http://publib.boulder.ibm.com/infocenter/dsichelp/ds8000ic/index.jsp?topic=/com.ibm.storage.ssic.help.doc/f2c_clijavaerror_2lfq3j.html

## _Solution2_ ##

1.Set Java path under PATH environment variable. This path should be full path till ../Java/bin folder. For example: C:\Program Files\Java\JDK1.6.0\_24\bin

2. Launch the installer.

## _Problem_ ##

Connector manager registration step fails even after having correct JVM on Windows. Installer throws error "The appliance could not connect to the connector manager as specified in the location. Make sure that the URL is correct or try again later."

## _Solution1_ ##

Make sure that the GSA is reachable from the connector host.

## _Solution2_ ##

Make sure that the connector manager port is not blocked by the firewall. Check your Windows firewall settings and disable the firewall that prevents the connector manager to communicate with the GSA.