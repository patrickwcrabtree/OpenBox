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
