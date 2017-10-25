Open Source Project:  Pi-hole
-----------------------------

Authors:  
<ul>            
<li>Michael Galde </li>
<li>Carmel Waka </li>
<li>Olivier Avande</li>
<li>Srikanth Vadla</li>
</ul>
Team Name: R3tr0

Our group "R3tr0" focused on the software security aspect for the open source project Pi-hole and have developed the following five assurance claims


Assurance Claims
-----------------
<ul>
<li>Claim 1: The Pi-hole user interface has no exploitable HTTP weakness.
The Pi-hole makes use of lighhtpd software package due to its minimal framework and the ease of which the system can be configured.
</li>
<li>Claim 2: Pi-hole attack surface is minimized
The attack surface of the Pi-hole software is minimized by utilizing best practices approaches to software development and community involvement.
</li>
<li>Claim 3: The Pi-Hole minimizes the possibility of device compromised during patching
and some details about this claim are
</li>
<li>Claim 4: <  Will edit this>
and some details about this claim are
</li>
<li>Claim 5: The Pi-hole DNS server is adequately safe from denial of service attacks**
The Pi-hole system uses dnsmasq as the underlying dns server to provide ad filtering. It is lightweight and requires minimal resources.
Like all dns services, it is exposed to denial of service. However, using the appropriate configuration it can be adequately secured.
</li>
</ul>

Security Requirements
---------------------
The development of assurance cases for each and every assurance claim allowed us to develop misuse cases to address each assurance claim. The misuse cases as they relate to the assurance claims can be found on lucid chart located https://www.lucidchart.com/invitations/accept/03df13bf-2fe3-4b3c-a4bb-1493b038bd23. The development within these misuse cases allowed this team to develop the following security requirements.
<ul>
<li>Web admin interface must have a username and password set up by default with no default credentials</li>
<li>Web portal must be deployed with basic login authentication</li>
<li>Pi-hole must utilize input validation</li>
<li>Web portal must include account lockout policies</li>
<li>Whitelist mist utilize ACL</li>
<li>A user must be able to conduct a update of the software</li>
<li>Configuration implements least privilege access</li>
<li>Implements strong encryption from Pi-hole to user</li>
<li>Logs all security information</li>
<li>Disable user accounts with consecutive failed attempts</li>
<li>Utilize encryption with storage</li>
<li>Must include backup and recovery options</li>
<li>Applies recent security patches to dependent packages</li>
<li>Log all DNS query attempts</li>
</ul>

Open Source Project Pi-hole Documentation review
------------------------------------------------

This project can be found at https://pi-hole.net

The Pi-hole service is both a local DNS server and a web portal and the securing of these various functions is key for consumers who wish to place the devices on there internal network. Comparing the first assurance claim which is that the Pi-hole has no exploitable HTTP weakness the group took a look at what features were utilized to enable this feature. The web interface was first established in version 2.1 as a default service. The Pi-hole team decided to utilize Lighttpd as the web service as it is advertised as a secure service. Lighttpd encourages its open source community to review its product and to recommend changes for stability and security. Pi-hole pushes out updates from Lighttpd and also encourages its community to review the Pi-hole platform as well. These two sources of review allow Pi-hole to provide a web portal service with a minimized attack surface.

Reviewing the Pi-hole open source software project allows a user to see to type of community that this project attracts. The project has been a fan based project and is providing a service that fairly unique. For one the members of the Pi-hole community are united in the desire of blocking ads by utilizing a device connected to the users home network. The user of this software is more likely going to be somewhat familiar with basic networking concepts. The open source project is also focusing on low powered computers like a raspberry pi which allows the software to be deployed on multiple Linux distributions natively. With all of this combined the user base for this software appears to be more willing to contribute to both stability and feature development which appears to be the case with the amount of contributors to this project which is currently 76. These members are encouraged by the Pi-hole developers to communicate and desired features or requests.

## Add a paragraph for section 3

## Add a paragraph for section 4

## Add a paragraph for section 5

Open Source Project Pi-hole security installation and configuration
--------------------------------------------------------------------
Reviewing the instillation procedures and how the security relates to this is quite to opposite as the initial instillation method given was to run a <curl> script which is "curl -sSL https://install.pi-hole.net | bash". Even the website states that piping this to bash is dangerous and encourages the user to review the code before running it but this will introduce a complacency for users who begin to trust the marketing name Pi-hole and land on a phishing portal mimicking the Pi-hole website and the user runs a malicious script within bash. Even today the website recommends new users run this curl script into bash. This complacency allows the products "good name" to be utilized by a phishing site and users who have utilized this instillation method in the past would not be concerned when asked to run this script once again. 
