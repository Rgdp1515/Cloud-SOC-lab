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

I have set up a new Ubuntu server as my C2 Server

<img width="730" height="134" alt="image" src="https://github.com/user-attachments/assets/5f1ac196-a221-47be-9fda-c2b575e423a8" />

And will be Using Kali Linux on VirtualBox to simulate real-life attack scenarios

<img width="1021" height="801" alt="image" src="https://github.com/user-attachments/assets/74ddc43f-19c0-4b84-96c7-8283fe6b4340" />

On the Ubuntu Mythic server:

<img width="617" height="176" alt="image" src="https://github.com/user-attachments/assets/9330f04c-05ff-4d7a-83ca-fc5f3c852b4e" />

The above commands: 
1. Update the repositories and dependencies
2. Installed docker-compose for later use
3. Installed make for later use
4. Cloned the Mythic repository from github

I then installed Mythic onto my Ubuntu server using Docker

<img width="512" height="22" alt="image" src="https://github.com/user-attachments/assets/3af09292-8a82-4d49-8899-b2746f658c5f" />

Restarted docker to activate the application, "Make" command to create and run Mythic cli

<img width="846" height="407" alt="image" src="https://github.com/user-attachments/assets/bfb9c4eb-005f-4bc7-9948-97f3dc249ad8" />

Troubleshooting my VULTR firewall settings to figure out the connection error

<img width="893" height="763" alt="image" src="https://github.com/user-attachments/assets/7576b93b-f43c-488f-a239-7d7076e207c0" />

Fixed the issue... Mythic wasn't properly started...

<img width="937" height="175" alt="image" src="https://github.com/user-attachments/assets/b9e95808-3a4a-47bb-bb5d-310545608ba8" />

And we have this beauty

<img width="1054" height="802" alt="image" src="https://github.com/user-attachments/assets/0f095d45-0225-4ba0-9904-587be33e4351" />

To find our password for the Mythic admin account

<img width="652" height="674" alt="image" src="https://github.com/user-attachments/assets/f907a27f-33c8-42ac-ae3e-011df5283d20" />

We can now begin with Phase 1 of attacking the target host, "Initial Access"
Using rockyou.txt wordlist to attempt our brute-force attack, unzipping the file

<img width="595" height="467" alt="image" src="https://github.com/user-attachments/assets/dc36fff4-3114-4c39-95e1-d01bc365fb2c" />

Installing Crowbar in Kali. Crowbar is a brute-force tool that supports OpenVPN, SSH, and RDP.

<img width="488" height="70" alt="image" src="https://github.com/user-attachments/assets/60cf401b-b412-4411-85ee-7f7a3b91ee26" />

The configuration for Crowbar to bruteforce the target host

<img width="642" height="62" alt="image" src="https://github.com/user-attachments/assets/35b29c10-6dde-412d-b7de-47754e60af91" />
 The command initiates Crowbar. "-b" signals to use RDP. "-u" is the username "Administrator." "-C" is the wordlist to test the authentication with (for automation). "-S" is the target IP (My Windows Server)

 Crowbar didnt recognize the path that xfreerdp was using (because it was xfreerdp3) so i pointed it to the original file and crowbar should work now

<img width="621" height="760" alt="image" src="https://github.com/user-attachments/assets/8d0126c1-b0e7-4465-bfae-18952f7e46aa" />

Switched to Hydra (built-in to kali linux) because Crowbar wasn't able to do the job.

<img width="635" height="221" alt="image" src="https://github.com/user-attachments/assets/c65d1929-9ef3-4cb2-8cbe-6f675a0ffd92" />
<img width="614" height="42" alt="image" src="https://github.com/user-attachments/assets/7749c9d7-a6c9-47b3-8ee4-d81ebbcad528" />

Using the compromised credentials and successfully RDP'ing (?) into the Windows server

<img width="1010" height="843" alt="image" src="https://github.com/user-attachments/assets/5e07ec28-1ba2-4311-a593-1742eb37f6f3" />

Phase 2 "Discovery"

<img width="741" height="609" alt="image" src="https://github.com/user-attachments/assets/cb27b0bc-325c-49a9-81b5-88d47a7778e6" />

Phase 3 "Defense Evasion"

<img width="922" height="762" alt="image" src="https://github.com/user-attachments/assets/5a22106f-a373-4ed3-87d3-63a4d4bcd3fb" />

Downloading the Apollo agent onto the Mythic C2 server.

<img width="874" height="39" alt="image" src="https://github.com/user-attachments/assets/6a84db27-3274-4199-843b-1048022a2122" />

Now we move into our Mythic C2 server.

<img width="1436" height="284" alt="image" src="https://github.com/user-attachments/assets/76bee6ba-b493-457d-8f8b-3552381d1e31" />

Now downloading a C2 Profile, Here were have selected the http agent profile

<img width="866" height="49" alt="image" src="https://github.com/user-attachments/assets/648df30a-9841-4b18-9d9a-9ccb8889650a" />

<img width="1836" height="105" alt="image" src="https://github.com/user-attachments/assets/40bd2bdf-8b5e-4173-8f1a-cf2ddf7e1390" />

Now we want to "generate new payload"

<img width="1592" height="123" alt="image" src="https://github.com/user-attachments/assets/0d65f41a-c49b-4a0b-837e-827f7c35a684" />

Configuring the C2 Server (Must use the IP of the Mythic host)

<img width="1544" height="581" alt="image" src="https://github.com/user-attachments/assets/0049e483-635d-48dd-b9ed-e3817da581c1" />

We're doing things

<img width="778" height="165" alt="image" src="https://github.com/user-attachments/assets/0731c987-48c9-450b-b653-e59d3aeaa375" />

On the Mythic C2 server

<img width="952" height="525" alt="image" src="https://github.com/user-attachments/assets/7722caa7-710f-4a30-9b2c-5a2e31b3ec77" />

Moving and Renaming the executable file, it is now "svchost-Rengoku.exe"

<img width="813" height="178" alt="image" src="https://github.com/user-attachments/assets/499f5877-fbfd-4823-9581-2f6f73467e2b" />

Hosting an http server

<img width="557" height="56" alt="image" src="https://github.com/user-attachments/assets/0db56baa-eec6-4b75-ae24-cad497d6d233" />

Completing Phase 4 "Execution": Using RDP from my Kali Linux to download the payload from the C2 Server onto the compromised Windows machine

<img width="1002" height="79" alt="image" src="https://github.com/user-attachments/assets/870cc839-dd1e-425e-9b02-12eda2f03982" />

Phase 5 "Command and Control": Shows that the connection has been established with PID 6044

<img width="647" height="86" alt="image" src="https://github.com/user-attachments/assets/51450ea3-b8d4-404c-9247-c73eca9cd283" />

The view of the connection from Mythic web interface

<img width="1578" height="78" alt="image" src="https://github.com/user-attachments/assets/03e2446e-a228-4cd6-8b85-dadc799c256e" />

Phase 6: "Exfiltration" of data on the compromised system

<img width="1594" height="693" alt="image" src="https://github.com/user-attachments/assets/81375663-82d2-472e-9845-70a42572def0" />

Interesting information: MITRE ID T1036 Masquerading

<img width="1586" height="647" alt="image" src="https://github.com/user-attachments/assets/4b32b985-00d0-41ba-84d1-4914caf1e958" />

That's exactly right

<img width="919" height="395" alt="image" src="https://github.com/user-attachments/assets/984ec2dc-cd06-4f2c-aa93-d2d90bc71ada" />

Even though the file name was downloaded as "svchost-Rengoku.exe" The Original file name is "Apollo.exe"

<img width="593" height="493" alt="image" src="https://github.com/user-attachments/assets/1b6cbcb5-a32a-4947-b4fc-a4d9245e3455" />

Now to create a Rule in Elastic to detect potential Mythic C2 Apollo agents

<img width="1522" height="740" alt="image" src="https://github.com/user-attachments/assets/63a12afe-ce9b-4831-8068-569d40ab2d6f" />

Building out the query to use for the Elastic dashboard

<img width="1864" height="831" alt="image" src="https://github.com/user-attachments/assets/2d2b20e1-c64c-49df-98e6-8d6da7be78c7" />

This is a key aspect: if it were true this means the server has a process that initiates the connection, however, this is false meaning that the connection was initiated from a different server than the host.

<img width="718" height="406" alt="image" src="https://github.com/user-attachments/assets/7a7e06c7-d908-4ed2-995a-a3c64916d504" />

New dashboard created to scan for potential C2 activity

<img width="1874" height="795" alt="image" src="https://github.com/user-attachments/assets/33f3f422-306d-406b-8cc6-0f519da0dd54" />
<img width="1883" height="225" alt="image" src="https://github.com/user-attachments/assets/962b0020-2a1f-4184-b7a5-2148f7030592" />





