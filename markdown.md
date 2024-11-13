# Security Alerting and Monitoring 

## Monitoring Computer Resources
 (Monitor all entry points such as logins, publicly available services, data storage locations, remote access. React to security events like account access, firewall rulebase, additional scanning)

 ### Systems:
 Monitor authentications and view where people are logging in from, also monitor the services that are running on the devices including the type of activity and how much activity. You can also check if any backups have been completed on devices and what versions of software are installed. 

### Applications:
 Major part of monitoring is checking availability and making sure these systems are running, keeps lines of communication open between the software and developers or manufacturers of these applications to be notified of any security issues. Many security breaches have been identified by monitroring the amount of traffic that is being transfered, higher traffic than ususal could indicate a possible attacker attempting to exfiltrate data. 

### Infrastructure:
Monitors the outgoing acitivity for example like remote access systems that have people connecting using VPN. it also monitors how many of those connected are employees, how many are vendors and how many are guest. Firewall and IPS reports are another good source of information that could give a warning if someone is trying to gain access to the systems.

## Activities

### Log aggregation:
The mechanism for capturing, normalizing, and consolidating logs from different sources like "SIEM" to a centralized platform for correlating and analyzing the data such as tracking application access, measure and report on data transfers and viewing authentication and access. 

### Alerting:
Type of notification that is useful incase of something unusual, such as large file transfers thats being transferred out of the data center, increase of aunthentication errors that could indicate that an attacker could be using a "spring attack" (An attacker can use the vulnerability to write malicious code to disk, which can then be executed by a crafted request) to be able to gain access to someone's account.

### Scanning:
An important part in helping organizations manage cyber risks, safeguard sensistive data and maintain regulatory complience. Many organizations have software and systems that are contantly scanning all devices on their network and report on metrics, for example you could see what type of operating systems or even what drivers are installed that may be running on these devices and what version are installed as well. You could possibly see report on potential anomalies that have been identified and put into the logs of those devices, and what applications are installed on mobile devices and laptop computers. Scanning gathers valuable information that is stored into the database where you can later create very detailed reports.

### Reporting:
Reports can contain very extensive information regarding the status of these systems on our network, that could give us a clue on what to do next known as "actionable" reports. An exmaple could be where you create a report that shows how many devices are up to date or in complience with vulnerability patches but also want to identify how many devices are not in complience, the same can be done with operating systems on devices. Lets say a new vulnerability was announced, you can use this database to create reports to understand how many systems may be vulnerble to this specific vulnerability. Another thing you could do is perform some "what if" analysis and perform Ad Hoc reporting, these are reports where you're considering what could happen in the future, and you create a report that shows the systems that may be affected by that hypothetical situation.

### Archiving:
A long term backup that is critical to access. Organizations may be mandated to collect data over a certain amount of time, not only to provide information about how a business is performing but its also used from a security perspective to understand what could be happening with attackers inside of your network.


### Alert Response/Remediation/Valdation:
Alert response is the immediate action taken to reduce the impact of an incident, while remediation is the steps taken after the initial response to recover, learn from, and prevent future incidents. lastly, validation involves verifying that remediation actions have solved the problem.

- Quarantine: Once an alarm has been generated its important to quarantine that system from eveything else on the network and prevent an attacker from gaining additional access to that particular system and prevent anyone on that system jumping out to other devices on the same network.

- Alert tuning: An ongoing challenge for anyone trying to put together alerting or alarming. This is usually known as a balancing act, where you'd like to be able to view real time alarms and alerts but have some of those alerts that are not actually accurate that are known as a "false positive". There could be certain events that arent logged and therefore dont create an alert refered as a "false negative". It takes time to tune these alerts for your particular network but once done you can start making immediate decisions about the information provided in those alarms.


## Tools

### Security Content Automation Protocol (SCAP):
Allows for these vulnerabilities to integrate in a single language where all devices can understand, for example if you find a vulnerability with a next gen firewall, an intrusion prevention system,and a vulnerability scanner, SCAP will allow all of those devices to identify them as exactly the same vulnerability, which also means that these very diverse security tools can now work together and automatically detect and remove these vulnerabilities.

### Benchmarks:
Applies best security pratices to everything such as operating systems, cloud providers, mobile devices, etc. An exmaple of a security benchmark for a mobile device would be, disabling screenshots, screen recordings, prevent voice calls when locked, force encryption backups, disable additional VPN profiles, configure a "lost phone" message etc.

### Agents/Agentless:
- A agent is a software component that is installed on a device to perform security-related actions such as scanning and reporting, restarting and rebooting systems, applying software patches, making configuration changes and monitoring systems. one of the advanatages of having this agent-based system is that it's always running on while making sure the system is always in complience, it will also need to be maintained and updated.

- A agentless runs without a formal install, usually runs when you log in or connect to something similar to a VPN concentrator - (a network device that manages VPN traffic for multiple users, allowing remote workers to securely access a corporate network). The agentless will then execute in the memory of that system to check and verify that is in in compliance which will automatically remove itself from the system. Since it doesnt need to be formally installed you do not need to provide any ongoing maintenance of that software, it will also not be running 24/7.

### Security Information And Event Management (SIEM):
SIEM is commonly used to combine log files to a centrol database, which is used to create numerous reports to give an idea on how security is running on networks. SIEM includes a very powerful reporting engine, that will allow us to combine seperate data types, will give reports on prefomance for firewall and how a VPN concentrator may be authenticationg. Eventually this informaton will be stored into a large database over a long period of time that can be used to create a forensic report to show what happaneded prior to a particular security event and allow us to search back and see what information might be available to help us understand how an event occured. 

### Antivirus:
Software that is created specifically to help detect, prevent and remove malware (malicious software like torjoans, worms, macro viruses etc)

### Data loss prevention (DLP):
Is used to block any type of data you do not want running your network such as social security numbers, credit cards, medical records etc. DLP is used to contantly monitor the traffic in real time to block any sensitive inforamtion from leaving your network.

### Simple Network management Protocol (SNMP) Traps:
An SNMP trap is a message that’s sent from a network device to an SNMP management system without being solicited by the system. The trap is triggered when a specific event or condition occurs on the device, such as a link going down, an authentication or a power failure.

### NetFlow:
Is used to collect IP traffic information and monitor network flow.

### Vulnerability scanners:
Automated detection of security weaknessess in systems, networks, and applications that are sent to a management system to automate the process to patch those systems without any human intervention. Very useful in large environments with hundreds or thousands of devices that have different vulnerabilities that need to be patched.
