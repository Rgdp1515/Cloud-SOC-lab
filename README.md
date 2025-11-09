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

Downloading Sysmon and installing Sysmon. Sysmon must be configured with a specific configuration file to work correctly.
For this I will be using Olafhartong's Sysmon Configuration for my Windows Server.

<img width="818" height="379" alt="image" src="https://github.com/user-attachments/assets/eb3810c1-3fac-4e8f-8935-4a6a19b8348c" />

Configuring Elastic to ingest Windows Event Logs

<img width="1865" height="623" alt="image" src="https://github.com/user-attachments/assets/c0d12278-a4fd-46fb-8dcf-1e6f87c4dc62" />

Configured Elastic to ingest Windows Defender logs and Windows Event logs

<img width="1672" height="316" alt="image" src="https://github.com/user-attachments/assets/02bf223a-f9e7-4f0b-b26d-e5bcdab208e8" />

Elastic is properly ingesting Sysmon logs

<img width="1543" height="636" alt="image" src="https://github.com/user-attachments/assets/c1821ead-59da-4b94-8d01-e139dfb517b3" />

Created a Linux host for SSH usage. I will be using this to create custom queries, alerts, and dashboards on Elastic.

<img width="482" height="114" alt="image" src="https://github.com/user-attachments/assets/2d557d06-ae34-4dd4-9bf0-5780022e5c1b" />

Successfully enrolled the Linux host into Kibana Fleet

<img width="1861" height="215" alt="image" src="https://github.com/user-attachments/assets/04769dfd-2502-4805-af12-a3c6d80ef106" />

Creating an alert on Elastic to notify for suspicious SSH activity on the Linux host

<img width="720" height="723" alt="image" src="https://github.com/user-attachments/assets/cc1522e7-4db2-42ba-88e3-5e428a0f8f4d" />

The alert will generate when there are more than 5 unsuccessful SSH attempts within any 2 minute period (I updated this to check every minute afterwards)

Created a dashboard with a map visual highlighting the SSH attempts on the linux server by country, Vietnam had the most unsuccessful attempts with over 400 in less than 12 hours (This ended up being over 30,000 in under 3 days)

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

Moving and Renaming the executable file, it is now "svchost-Rengoku.exe" (Later on I ended up having to redownload the payload because Microsoft Security came back to life, and then Elastic EDR took over after that)

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

Created a new Windows server for osTicket, we are now at 6 total servers on VULTR (Kali Linux was run from VirtualBox)

<img width="1416" height="519" alt="image" src="https://github.com/user-attachments/assets/4bdb8321-cc3d-4d1c-bcba-3a36364032ea" />

Downloading Xampp version 8.2.12 for the web host

<img width="516" height="267" alt="image" src="https://github.com/user-attachments/assets/c3f2750f-92c5-458f-b2b5-c01ec8bd68f1" />

Configuring the Xampp properties file

<img width="808" height="690" alt="image" src="https://github.com/user-attachments/assets/551a4e06-9ca1-47a7-b52d-d5069fdd8a84" />

Now configuring the config.inc.php file. Will first make a copy and then edit the original.

<img width="987" height="705" alt="image" src="https://github.com/user-attachments/assets/4f15b1fa-0359-4b3d-8332-6a19a83ff028" />

Moving into Windows Defender to configure the Firewall

<img width="1219" height="327" alt="image" src="https://github.com/user-attachments/assets/5ec8b9a8-cee6-400a-a834-c124190a04f6" />

The Firewall Rule description

<img width="882" height="549" alt="image" src="https://github.com/user-attachments/assets/406f7aea-ad78-4a8e-a811-a624bce1deeb" />

Configuring the 'Root' account for phpMyAdmin to bind to the IP of my osTicket server

<img width="853" height="780" alt="image" src="https://github.com/user-attachments/assets/e9a935a6-f71c-4bad-980f-7cfb111cb639" />

Configuring the 'Pma' account to bind to the IP as well

<img width="1311" height="806" alt="image" src="https://github.com/user-attachments/assets/4ee0c0ad-6b3d-42b9-9eb7-6d9abeda8bb0" />

Downloading osTicket v1.18.2

<img width="1405" height="769" alt="image" src="https://github.com/user-attachments/assets/c22f447c-fc48-4a95-99fd-532d575d17d4" />

Creating a 'New Folder' for osTicket in this directory because the default web contents are stored here

<img width="915" height="680" alt="image" src="https://github.com/user-attachments/assets/7abd369a-009c-4596-b3ac-302af1848239" />

And now we have access to the web host for osticket installer

<img width="1418" height="506" alt="image" src="https://github.com/user-attachments/assets/3aa413a2-a589-4c71-a5b4-1a547bcba1d6" />

Creating a new database 'Rengoku-DB' from phpMyAdmin

<img width="1351" height="694" alt="image" src="https://github.com/user-attachments/assets/b4ac47df-46a2-46d8-94cf-db91c1c68e4c" />

Then, configuring the settings of the 'Rengoku-DB' database from the osticket server

<img width="1061" height="822" alt="image" src="https://github.com/user-attachments/assets/cf64cebb-3eff-46a8-a91e-fff5349f8926" />

We now have osticket properly installed!

<img width="1354" height="898" alt="image" src="https://github.com/user-attachments/assets/5ce6a945-bc89-4ebe-b3e0-b19bd934c00c" />

The first step of the file configurations, using PowerShell

<img width="1041" height="330" alt="image" src="https://github.com/user-attachments/assets/6758fc70-0ed5-4183-8eac-630b1e1ca40a" />

Accessing the Staff Control Panel of osTicket from my host

<img width="1275" height="588" alt="image" src="https://github.com/user-attachments/assets/a8c3203d-6c0c-4cde-b357-d92dfa304ab9" />

Generating an API key to integrate osTicket with Elastic

<img width="1221" height="288" alt="image" src="https://github.com/user-attachments/assets/b8e6af0b-7a05-4dfe-be74-fdfb1b58d19a" />

Starting a Free Trial is necessary to integrate web API's

<img width="1418" height="753" alt="image" src="https://github.com/user-attachments/assets/f91d3f40-60d9-4b50-b373-5700aa5179c2" />

Using a 'Webhook' connector

<img width="891" height="769" alt="image" src="https://github.com/user-attachments/assets/108b96c2-e99d-48bf-91bd-042ea5d4086b" />

Stealing this Example

<img width="1205" height="898" alt="image" src="https://github.com/user-attachments/assets/f0354a72-178f-46ed-b3dd-977ee565445f" />

Great Success!

<img width="867" height="758" alt="image" src="https://github.com/user-attachments/assets/1348d76f-2908-4d59-a4df-564f9da4ee45" />

The POC from osTicket

<img width="1205" height="456" alt="image" src="https://github.com/user-attachments/assets/a846df8d-0570-4481-a6e8-7f1690c9abc6" />

Investigating an alert on Brute Force activity

<img width="1863" height="888" alt="image" src="https://github.com/user-attachments/assets/c1077387-b3ad-4549-ac7a-58da05f4b913" />

Checking the IP on AbuseIPDB: Originates from Thailand

<img width="1793" height="659" alt="image" src="https://github.com/user-attachments/assets/3c65f5cf-9018-4409-af96-e57d921e1cb4" />

From GreyNoise:

<img width="452" height="151" alt="image" src="https://github.com/user-attachments/assets/756ccdfc-000b-4644-b673-c890e87ed4b0" />
 This shows that the IP scans the internet for vulnerable servers, not indicative of a targeted attack (yet)

 Further investigation into the IP, to check for successful attempts
 
<img width="971" height="657" alt="image" src="https://github.com/user-attachments/assets/48a4e247-e4d5-4207-b4d2-39a1a9fbea84" />

<img width="834" height="411" alt="image" src="https://github.com/user-attachments/assets/972e564f-7e9a-44a6-869d-ae644c6cca10" />
 Can close out the ticket as benign

 Configuring Elastic to send a ticket to our osTicket server when the 'Brute Force' alert is triggered

 <img width="1421" height="836" alt="image" src="https://github.com/user-attachments/assets/1f76a750-df4d-4775-b7ff-f6b31d858731" />

Adding a link to click from the ticket to go into elastic to being investigating the alert

<img width="983" height="412" alt="image" src="https://github.com/user-attachments/assets/9e9d433a-b2ce-42f8-896d-2c00bb873088" />

configuring the kibana.yml file for my ELK server so the hyperlink will work

<img width="864" height="643" alt="image" src="https://github.com/user-attachments/assets/8ab30342-8ce1-460b-8812-81ef56cf4841" />

Configuring RDP Alert to send tickets to osTicket

<img width="1607" height="670" alt="image" src="https://github.com/user-attachments/assets/11563fa4-d5cc-4ab6-be64-ce42a46903aa" />

Beginning RDP Brute Force investigation within the Alert Dashboard

<img width="721" height="711" alt="image" src="https://github.com/user-attachments/assets/a0ae4fd3-2597-4545-98bd-1b3eb15d582e" />

Checking the IP on AbuseIPDB

<img width="848" height="199" alt="image" src="https://github.com/user-attachments/assets/c5ab900a-d662-41fe-821b-ca8338e84947" />

Then on GreyNoise

<img width="1118" height="417" alt="image" src="https://github.com/user-attachments/assets/225df863-5fe5-4bfc-9059-8f4ba6c6b1da" />
 UH OH

<img width="1328" height="542" alt="image" src="https://github.com/user-attachments/assets/b85a7e07-83df-4c65-b18d-544fa5edfd28" />

The IP was able to RDP into the Administrator Account Successfully

<img width="1566" height="530" alt="image" src="https://github.com/user-attachments/assets/ee9ed11c-cbea-4933-bea6-1cdc23e4fa33" />

Capturing the 'TargetLogonID' and searching for further activity on the host system with that ID

<img width="1835" height="842" alt="image" src="https://github.com/user-attachments/assets/d16f0343-6871-4121-b5b7-9670b37adf01" />

There are 3 Events that occurred, the timing and sequence of events signals a scan of the host. Time to pivot

<img width="1696" height="692" alt="image" src="https://github.com/user-attachments/assets/7a08f378-b9e4-405e-944f-b2d689eb0103" />

Using the Dashboard, we see that there is potential suspicious activity

<img width="1868" height="424" alt="image" src="https://github.com/user-attachments/assets/bf7314fe-7aa1-4976-a016-6fe9479aea12" />

Searching for Network Connections with that Destination IP address


<img width="1624" height="391" alt="image" src="https://github.com/user-attachments/assets/54b1ddca-4a8c-48bd-b191-7dc7fbe5b2f8" />

Using ProcessGUID to search for events that occurred in that specific PowerShell session

<img width="672" height="473" alt="image" src="https://github.com/user-attachments/assets/f6c1c124-641b-4212-8739-64a3b24cba0e" />

We see a "File Created" with Event.code:11 

<img width="1824" height="919" alt="image" src="https://github.com/user-attachments/assets/6ca7c22e-0a76-427b-9dd3-bd3c43a2f736" />

The file name:

<img width="634" height="595" alt="image" src="https://github.com/user-attachments/assets/45bb6723-ea86-479f-a21b-e0180ddcbb9d" />

Event.Code:29 Is the Sysmon ID for creation of new executable files

<img width="634" height="387" alt="image" src="https://github.com/user-attachments/assets/5ae12e8f-35df-4394-aebc-7996a6b11e11" />

We find the 'Process:Create' which is Event.ID: 1. This shows a different ProcessGUID which is unique to the executable (Rengoku)

<img width="1317" height="467" alt="image" src="https://github.com/user-attachments/assets/ceedbc49-9e0d-49f7-a1d5-ed867bccc138" />

The notes of the investigation

<img width="889" height="467" alt="image" src="https://github.com/user-attachments/assets/48b139e6-22c5-47b2-a0f1-ab0a20792acd" />

Configuring the Mythic C2 Alert from Elastic to send tickets to osTicket

<img width="766" height="236" alt="image" src="https://github.com/user-attachments/assets/17bb9e63-f50e-454b-8779-2fe73b3bae81" />

Integrating Elastic Defend EDR into Elastic

<img width="1884" height="334" alt="image" src="https://github.com/user-attachments/assets/ef75f80d-2471-4b83-838f-4387935f2f5a" />

The configurations for Elastic Defend

<img width="1216" height="735" alt="image" src="https://github.com/user-attachments/assets/43f1756b-20d8-45e5-9fbc-0703d651f3df" />

<img width="1604" height="516" alt="image" src="https://github.com/user-attachments/assets/7ff69312-a1de-41f5-b54d-9b29bddf73c0" />

Lovely email that my actions were being noticed out in the wild

<img width="1371" height="973" alt="image" src="https://github.com/user-attachments/assets/da418ad3-2ebb-47e0-b847-e3f60d207b08" />

Microsoft Defender was able to delete the file, redownloaded it.

<img width="1873" height="200" alt="image" src="https://github.com/user-attachments/assets/bf04606d-4ec8-4256-acbf-10ae553c58e9" />

Elastic EDR actively blocking the malware download even with Microsoft security settings turned off

<img width="714" height="700" alt="image" src="https://github.com/user-attachments/assets/713cc05a-b7b2-44fa-b2f0-00a254ef9c67" />

Maybe we can brute force the malware onto the system?

<img width="1375" height="485" alt="image" src="https://github.com/user-attachments/assets/d32b0eac-59ae-4933-955f-0c12c354ef8a" />

The file was allowed to be downloaded, but the connection to Mythic was cut after 1 second...

<img width="744" height="791" alt="image" src="https://github.com/user-attachments/assets/22ba4686-c257-441f-bf85-d05eaf76e6e1" />

Very suspicious activity

<img width="900" height="468" alt="image" src="https://github.com/user-attachments/assets/2558b88d-6dfc-4c68-a71b-ef9f95edf812" />
<img width="890" height="518" alt="image" src="https://github.com/user-attachments/assets/c8ee32eb-7d45-4fc5-9ed8-b61728ffea7b" />

From here the steps to take: 
1. Isolate the host. Prevent any further spread of malicious activity
2. Perform OSINT. We can upload the file to VirusTotal to investigate it further  
 <img width="1024" height="420" alt="image" src="https://github.com/user-attachments/assets/856fb329-7904-48ce-adad-8f57a83e6190" />
3. Check for autoruns/scheduled tasks 
 <img width="1060" height="757" alt="image" src="https://github.com/user-attachments/assets/c95ef06d-7903-442c-90fe-21265010a1ab" />
4. Check if it is still running
<img width="918" height="222" alt="image" src="https://github.com/user-attachments/assets/8a82f4f8-664c-40b8-af55-6c04acfc6a99" />
5. Perform full antivirus scan
 <img width="1065" height="862" alt="image" src="https://github.com/user-attachments/assets/2ea30441-dfa7-4262-969d-5b8912fd5ad3" />
6. Remove the threat

7. Save the Filehash for threat intelligence

8. Lessons learned
   - Don't turn off security settings
   - Don't click links to things that are suspicious
   - Elastic EDR is more powerful than my Mythic C2 server

Configuring Elastic EDR to automatically Isolate the Windows server when detecting malware

<img width="1836" height="874" alt="image" src="https://github.com/user-attachments/assets/dbc35dba-f992-4410-9ff5-97a59073c7e0" />

   
