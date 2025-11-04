# SOC-Automation-Project-2.0
Objective: Develop an end-to-end automated SOC workflow using n8n. Configure Splunk as the SIEM for log ingestion from a Windows 10 VM. Generate alerts in Splunk, route them to n8n for processing, enrich with OSINT tools, summarize findings using OpenAI, and deliver actionable notifications to Slack.


<img width="1052" height="400" alt="Image" src="https://github.com/user-attachments/assets/baf7253d-c6cd-43d7-ac20-204adc06e0bc" />




Start by installing a VMware Wowrkstaion 

<img width="1069" height="653" alt="Image" src="https://github.com/user-attachments/assets/9660d897-f7e4-48f5-a6ef-39b63d0bc756" />

Install  windowns 10

<img width="1082" height="635" alt="Image" src="https://github.com/user-attachments/assets/bf6a8df6-24d9-4617-a014-4974be8487e8" />


install Splunk SIEM / Universal forward 

<img width="1672" height="749" alt="Image" src="https://github.com/user-attachments/assets/6c0d7b4b-e2d3-4b74-94e5-01264790e980" />

<img width="1719" height="704" alt="Image" src="https://github.com/user-attachments/assets/091f2e44-bf69-40c9-a1e7-f6f91bd054ed" />


Virtual machine IP and Host machine IP

<img width="770" height="527" alt="Image" src="https://github.com/user-attachments/assets/5782c999-fb53-47f9-8263-9d69d1a0b772" />

<img width="711" height="412" alt="Image" src="https://github.com/user-attachments/assets/17305691-2c85-46ba-851f-67e6904a9c66" />


Both Devices Hostnames 

<img width="1481" height="472" alt="Image" src="https://github.com/user-attachments/assets/b8991d64-886b-4bf3-84f1-da542aa0f31b" />


Both ingesting logs into Splunk 

<img width="1730" height="660" alt="Image" src="https://github.com/user-attachments/assets/f77f50f8-148e-4026-8733-90fbd2fbbcad" />



In order to generate relevent telemetry data.

i remotely invoked an SSH session from the host to test VM and carried out a controlled brute-force login simulation to produce relevent logs alerts.



<img width="1237" height="524" alt="Image" src="https://github.com/user-attachments/assets/61d0660d-40d6-4d2b-acf1-ed1fdbb40d39" />


<img width="1726" height="880" alt="Image" src="https://github.com/user-attachments/assets/db729e71-3f34-43e3-b2f2-9d0f22591cdc" />


<img width="1736" height="702" alt="Image" src="https://github.com/user-attachments/assets/75c52004-e357-425a-ac3a-a48b05869cf5" />

Afer remote login failed 

Write a Query 

index= mydfir-project

| stat count by _time , Computername, user . Src_IP


<img width="1743" height="429" alt="Image" src="https://github.com/user-attachments/assets/136b6284-a9eb-46a2-ae77-bc43e1ac3d1c" />



Save Alert 


<img width="1738" height="431" alt="Image" src="https://github.com/user-attachments/assets/71706577-3c48-4c7c-8a47-6f3d8adfec3f" />



Install and download N8N


<img width="1543" height="782" alt="Image" src="https://github.com/user-attachments/assets/1b84fc50-01b7-485f-8522-2d6fe7b971d4" />



Solunk creates an alerting mechanism and N8N catches the alerts.



actomatically build an automation workflow enrich alerts using OSINT AbuseIPSB and VirusTotal 



Summmurize Finding to OPEN AI and deliver actionable notification to Slack 



<img width="1735" height="701" alt="Image" src="https://github.com/user-attachments/assets/b9d6bb8e-3141-42e5-889d-c3f927449a86" />



Eexcution Steps 


<img width="1730" height="919" alt="Image" src="https://github.com/user-attachments/assets/1c2412bb-dd0d-4ca5-b4cc-309a23177434" />



Actionable Notification is sent to Slack 



<img width="1731" height="859" alt="Image" src="https://github.com/user-attachments/assets/ba88c9d0-da78-4ac0-a01d-042c584e2d4e" />

