# Elastic SIEM SOC Home Lab

## Objective

The Detection Lab project aimed to establish a controlled environment for simulating and detecting cyber attacks. The primary focus was to ingest and analyze logs within a Security Information and Event Management (SIEM) system, generating test telemetry to mimic real-world attack scenarios. This hands-on experience was designed to deepen understanding of network security, attack patterns, and defensive strategies.

### Skills Learned

- Elastic Stack SIEM configuration and management: Successfully set up and configured Elastic Stack SIEM in a Home Lab Environment. Demonstrated Proficiency in deploying a Kali Linux VM, Configuring Elastic Agents for log collection, and forwarding data to the SIEM for effective security event monitoring.

- Security Event Simulation and Analysis: Acquired hands-on experience in generating and analyzing security events using NMAP on Kali Linux. Gained experience in querying Elastic SIEM to identify and investigate security incidents, enhancing skills in network security monitoring and threat detection.

- Visualization and Alerting in SIEM: Developed a custom dashboard in Elastic SIEM to visualize security events, demonstrating skills in data interpretation and pattern recognition. Successfully created and tested alert rules for detecting specific security events, forwarding the alerts via E-Mail, showing competency in proactive Incident Respose and Alert Management.

### Tools Used

- Elastic Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Telemetry generation tools to create realistic network traffic and attack scenarios, Such as NMAP.

## Steps

The first step was to Download and Setup a Kali Linux VM on Oracle VM VirtualBox.
After setting everything up, i proceeded to the Elastic SIEM website to create an account and configuring the Elastic Agent. 
The Elastic Agent was set up at my personal desktop, to simulate an SOC Analyst terminal. 

After setting up the Agent, i proceeded to install the Elastic Defend on the Kali machine, which will simulate the company server. 
by the end of the configuration, we want to generate alerts and want them to be send via e-mail, so we will have the following datagram:

Ref 1: Lab datagram

![image](https://github.com/user-attachments/assets/efb98a6f-594f-4f99-9e17-1302bfd12007)


Once the Elastic Defend was set up on the Kali machine, i proceeded to perform a NMAP scan on itself, to generate some log entries.



Ref 2: Nmap Scan

![image](https://github.com/user-attachments/assets/a6b40621-f653-4865-924d-dc7323ff2a09)



Ref 3: Log Entries

![image](https://github.com/user-attachments/assets/06535a3a-59e1-4fd8-8c9f-4c2144b9eeaa)

Once we receive the logs, we can check on the details about the event, which among all other detailed info, shows the commands executed and IP info.



Ref 4: host info

![image](https://github.com/user-attachments/assets/1b2407d0-e0d9-4d7c-b0e8-a6c1be9d5129)



Ref 5: command info

![image](https://github.com/user-attachments/assets/17de6d61-7dba-480b-a4e4-ecee2df86c60)


For better visualisation of the security events, i created a custom dashboard, as follows: 

Ref 6: Custom Dashboard

![image](https://github.com/user-attachments/assets/052e5a77-f5e5-4f1e-ae46-09b4e59049da)


After that, i proceeded to create custom alerts, so when NMAP scans are performed on the Kali machine, the SOC Analyst will get Alerts and E-mails about it.

The first step was to configure the custom alert do constantly scan for NMAP entries on the logs. When it is detected, the alert is configured to send the alerts by mail, as follows:

Ref 7: Custom Alert Created

![image](https://github.com/user-attachments/assets/cf8e4a2a-2cc1-4286-b56e-8d68a47f13de)

Once the alert was configured, i proceeded once again to perform a NMAP scan, which triggered the alert and sent the SOC analyst machine E-mail notifications.

Ref 8: Alert Triggered

![image](https://github.com/user-attachments/assets/ed270d1a-faf6-43c5-bc44-6ff4b155a990)


Ref 9: E-mail Alert

![image](https://github.com/user-attachments/assets/f1a0d60c-7a2d-4217-989b-83e516cf8afe)










