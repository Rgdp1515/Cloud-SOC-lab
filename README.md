# Cloud-SOC-lab
Creating a SOC environment in VULTR to generate telemetry, investigate incidents, and analyze network traffic/malware

 # Screenshots

 Ubuntu Server on VULTR

 <img width="1392" height="724" alt="image" src="https://github.com/user-attachments/assets/f20f1347-c7ef-4bb3-a761-b0f79135f27a" />

Downloading Elasticsearch onto the Ubuntu server

<img width="1060" height="222" alt="image" src="https://github.com/user-attachments/assets/d78195c0-25fb-46dd-ac57-4ba9373b78b8" />

Starting Elasticsearch on the Ubuntu server

<img width="1084" height="433" alt="image" src="https://github.com/user-attachments/assets/a0b4b72d-39ef-4462-8e3f-d9b32cae9640" />

Downloading and initializing Kibana on the Ubuntu server

<img width="1089" height="590" alt="image" src="https://github.com/user-attachments/assets/41735b82-22d8-4503-9179-e6491091a192" />

Successfully enrolling and Authenticated into Kibana

<img width="1868" height="630" alt="image" src="https://github.com/user-attachments/assets/2b0f1d4e-e94b-41f3-a115-e601fad77e85" />

Generating and storing security keys into the Kibana Key storage

<img width="949" height="130" alt="image" src="https://github.com/user-attachments/assets/3aa90d88-82a9-4f96-93d3-2f6e7f0487b6" />

Windows 10 Server Installed with RDP open to the internet

<img width="1217" height="823" alt="image" src="https://github.com/user-attachments/assets/0d73aa99-d218-484e-b2f3-d17fdb622272" />

Adding an Ubuntu Fleet Server 

<img width="600" height="116" alt="image" src="https://github.com/user-attachments/assets/b0039191-f0d3-49bc-8913-16b1ef114e1c" />

Connecting the Fleet Server to Kibana

<img width="902" height="534" alt="image" src="https://github.com/user-attachments/assets/25203a64-fa58-4753-864f-3f4b30461ce4" />

Successfully enrolling my Fleet Server into the Elastic Fleet

<img width="1106" height="127" alt="image" src="https://github.com/user-attachments/assets/bee49c6d-df8d-4756-b90b-3f81c5c4d5ff" />

Successfully enrolling my Windows Server into the Elastic Fleet

<img width="1219" height="168" alt="image" src="https://github.com/user-attachments/assets/f4899d34-3fc4-4e15-a640-1de0b77b9dde" />

Downloading Sysmon and Olafhartong's Sysmon Configuration into my Windows Server

<img width="818" height="379" alt="image" src="https://github.com/user-attachments/assets/eb3810c1-3fac-4e8f-8935-4a6a19b8348c" />

Configuring Elastic to ingest Windows Event Logs

<img width="1865" height="623" alt="image" src="https://github.com/user-attachments/assets/c0d12278-a4fd-46fb-8dcf-1e6f87c4dc62" />

Configured Elastic to ingest Windows Defender logs and Windows Event logs

<img width="1672" height="316" alt="image" src="https://github.com/user-attachments/assets/02bf223a-f9e7-4f0b-b26d-e5bcdab208e8" />

Elastic is properly ingesting Sysmon logs

<img width="1543" height="636" alt="image" src="https://github.com/user-attachments/assets/c1821ead-59da-4b94-8d01-e139dfb517b3" />

Created a Linux host for SSH usage

<img width="482" height="114" alt="image" src="https://github.com/user-attachments/assets/2d557d06-ae34-4dd4-9bf0-5780022e5c1b" />

Successfully enrolled the Linux host into Kibana Fleet

<img width="1861" height="215" alt="image" src="https://github.com/user-attachments/assets/04769dfd-2502-4805-af12-a3c6d80ef106" />

Creating an alert on Elastic to notify for suspicious SSH activity on the Linux host

<img width="720" height="723" alt="image" src="https://github.com/user-attachments/assets/cc1522e7-4db2-42ba-88e3-5e428a0f8f4d" />

The alert will generate when there are more than 5 unsuccessful SSH attempts within any 2 minute period

Created a dashboard with a map visual highlighting the SSH attempts on the linux server by country, Vietnam had the most unsuccessful attempts with over 400 in less than 12 hours

<img width="1895" height="703" alt="image" src="https://github.com/user-attachments/assets/823913b4-e0ea-4b17-927a-fe5b193e2dae" />

With this dashboard, I will be easily alerted on any new suspicious SSH activity and can view the origin of the activity

Creating an alert on Elastic to notify for failed RDP activity on the Windows server

<img width="1389" height="636" alt="image" src="https://github.com/user-attachments/assets/3d9ce17a-82b0-46ea-a555-e409898e1343" />

The alert will trigger when there are more than 5 unsuccessful RDP attempts within any 2 minute period

Created a Rule within Elastic for SSH Brute Force attempts

<img width="1625" height="634" alt="image" src="https://github.com/user-attachments/assets/1cfab15d-3e52-4f67-9ce3-c0ddd0c40fe9" />

Created a scon Rule within Elastic for RDP Brute Force attempts with the same fields and threshold

<img width="1587" height="119" alt="image" src="https://github.com/user-attachments/assets/99b09b71-fe2f-4620-ab0c-1d4d371c306f" />

Updating and adding new Visualization to the Elastic Dashboard to include RDP Attempts

<img width="1853" height="973" alt="image" src="https://github.com/user-attachments/assets/8935ee68-5dc9-4be2-a403-e162dbc1581c" />

Updating the Dashboard to include Table views of Authentication attempts alongside the map view

<img width="1891" height="861" alt="image" src="https://github.com/user-attachments/assets/c91aee4c-d5ba-45a3-83a3-c39b03349833" />

This is the Authentication attempts for RDP in the same dashboard

<img width="1887" height="866" alt="image" src="https://github.com/user-attachments/assets/69a86dc5-31de-42c6-8dae-c4dfe8cb027e" />


