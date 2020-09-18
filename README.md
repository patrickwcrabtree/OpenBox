# OpenBox
A white box testing automation proof of concept for detecting and testing susceptibility of CVEs

OpenBox take a source code path as its input and runs a suite of open source static testing tools to determine if an application is impacted by a given CVE and static vulnerability that could lead exploitation of the CVE

Attempts to map these vulnerabilities to the application endpoint for end-to-end testing

Proof on concept will be for detecting a Java Deserialization vulnerability that leads to Remote Code Execution (RCE)

Currently supports CVE-2017-15708

OpenBox leverages the following static analysis and testing tools:
1) OWASP dependency-check
2) SpotBugs with FindSecBugs plugin
3) CallGraph
4) attack-surface-detector
5) ysoserial

OpenBox_0_0_1.zip contains all of the tools used in the automation as well as the OpenBox jar.

To run, just unzip the package somewhere on your system, and open a command terminal and from that location run:
java -jar OpenBox-0.0.1-all.jar [Source Path]
Optional Parameters:
-hostname=[i.e.http://localhost:8080/spiracle]
-component-path=<path to 3rd party libraries> (Used if your 3rd party libraries are not located in your provided [Source Path]
-debug (just prints the info to a log.txt, if not set it will print everything to console)

TestApp.zip containts the modified version of Waratek Spiracle I used to test with. This just needs to be unzipped for testing, but to run you can just place the generate war file in an application server, such as Tomcat.

