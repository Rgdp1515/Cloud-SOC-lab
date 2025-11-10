# Cloud-SOC-Lab

Creating a SOC environment in VULTR to generate telemetry, investigate incidents, and analyze network traffic/malware.

---

## Architecture Diagram

![Architecture Diagram](assets/screenshots/SOC-Chart.png)

---

## 1. Initial Setup

<details>
<summary>Ubuntu Server & ELK Stack Setup</summary>

1. **Servers on VULTR**  
   ![VULTR Servers](assets/screenshots/VULTRServers.png)

2. **Downloading Elasticsearch**  
   ![Downloading Elasticsearch](assets/screenshots/DLElasticsearchUbuntuserver.png)

3. **Starting Elasticsearch**  
   ![Starting Elasticsearch](assets/screenshots/StartingElasticsearchUbuntuserver.png)

4. **Downloading & Initializing Kibana**  
   ![Kibana Setup](assets/screenshots/DLKibanaUbuntuserver.png)

5. **Kibana Authentication & Key Storage**    
   ![Storing Security Keys](assets/screenshots/Keygeneratestorage.png)

6. **Fleet Server Enrollment**  
   ![Centralized Fleet Server](assets/screenshots/ElasticFleet.png)  
  

</details>

<details>
<summary>Windows Server Setup</summary>

1. **Windows 10 Server with RDP Open**  
   ![Windows Server RDP](assets/screenshots/Windowsserversetup.png)

2. **Sysmon Installation & Configuration**  
   ![Sysmon Download](assets/screenshots/DLandConfigureSysmon.png)

3. **Ingesting Windows Event Logs in Elastic**  
   ![Elastic Windows Event Logs](assets/screenshots/ConfigureElasticWindowsEventlogsingestion.png)  
   ![Elastic Defender Logs](assets/screenshots/ConfigureElasticWindowsDefenderlogs.png)

4. **Elastic is properly ingesting Sysmon logs**  
   ![Sysmon Logs](assets/screenshots/ElasticPOVSysmonLogIngestion.png)

</details>

---

## 2. Blue Team – Detection & Monitoring

<details>
<summary>Alerts & Dashboards</summary>

1. **Linux Host Enrollment for SSH Monitoring**  
   ![Linux Host](assets/screenshots/LinuxHostCLI.png)  
   ![Linux Host Fleet Enrollment](assets/screenshots/SuccessEnrollLinuxElasticFleet.png)

2. **SSH Brute Force Alert**  
   ![SSH Alert Setup](assets/screenshots/AlertCreateSSHonLinux.png)  
   ![SSH Dashboard Map](assets/screenshots/DashboardCreateSSHActivity.png)

3. **RDP Brute Force Alert**  
   ![RDP Alert Setup](assets/screenshots/AlertCreateRDPonWindows.png)  
   ![RDP Dashboard Table](assets/screenshots/DashboardUpdateRDPAttempt.png)

4. **Elastic Correlation Rules**  
   ![SSH Rule](assets/screenshots/RuleCreateSSHLinuxActivity.png)  
   ![RDP Rule](assets/screenshots/RuleCreateRDPWindowsActivity.png)

</details>

<details>
<summary>MITRE Mapping & Elastic Correlation</summary>

1. **MITRE ATT&CK Tactics & Techniques**  
   - Initial Access: Brute Force (T1110)  
   - Execution: Command and Control (T1071)  
   - Defense Evasion: Masquerading (T1036)  
   - Exfiltration: Data from Local System (T1005)

2. **Elastic Detection**  
   ![Elastic MITRE Dashboard](assets/screenshots/PEC2Dashboard.png)
   ![Elastic MITRE Dashboard](assets/screenshots/PEC2Dashboard1.png) 
   ![Elastic Query Setup](assets/screenshots/PEC2DetectQueryStructure.png)
   ![Elastic Query Setup](assets/screenshots/PEC2DetectQuery.png)
   ![Elastic Query Setup](assets/screenshots/PECreateC2Detect.png)
</details>

---

## 3. Red Team – Adversary Simulation

<details>
<summary>Mythic C2 Server Setup</summary>

1. **Ubuntu Mythic Server Installation**
   ![Mythic Install](assets/screenshots/MythicCLIHistoryforSetup.png)
   ![Mythic Install](assets/screenshots/MythicCLIHistoryforSetupInstall.png)
   ![Mythic Install](assets/screenshots/MythicCLIHistoryforSetupInstall2.png) 
   ![Mythic CLI Setup](Phase4-2MythicCLIhttpagent.png)
   ![Mythic CLI Setup](assets/screenshots/MythicCLILogin.png)
   ![Mythic Web Setup](assets/screenshots/MythicLogin.png)
   ![Mythic Web Setup](Phase4-1MythicPOV.png)
3. **Payload Generation & Execution**  
   ![Payload Config](Phase4-3-1PayloadCreate.png)  
   ![Payload CLI download](Phase4-4PayloadCLI.png)

</details>

<details>
<summary>Attack Phases & Detection</summary>

1. **Phase 1: Initial Access**  
   ![Brute Force](assets/screenshots/Phase1KaliConfig.png)  
   ![Brute Force RDP](assets/screenshots/Phase1KaliConfig5.png)
   ![Brute Force RDP](assets/screenshots/Phase1KaliConfig5-1.png)

2. **Phase 2: Discovery**  
   ![Discovery](Phase2.png)

3. **Phase 3: Defense Evasion**  
   ![Defense Evasion](Phase3.png)

4. **Phase 4: Execution**  
   ![Execution](Phase4-4PayloadCLI.png)
   ![Execution](Phase4-4-1PayloadCLIRename.png)
   ![Execution](Phase4-5HTTPSERVERHost.png)
   ![Execution](Phase4-6Executiong.png)

5. **Phase 5: Command & Control**  
   ![Command Control](assets/screenshots/Phase5Connect.png)
   ![Command Control](assets/screenshots/Phase5-1Connect.png)

6. **Phase 6: Exfiltration**  
   ![Exfiltration](assets/screenshots/Phase6Exfiltrate.png)  

</details>

---

## 4. osTicket Integration & Triage Process

<details>
<summary>Integration Setup</summary>

1. **XAMPP & PHPMyAdmin Configuration**  
   ![XAMPP Install](assets/screenshots/DLXampp.png)
   ![XAMPP Install](assets/screenshots/ConfigureXamppPropertiesFile.png)
   ![XAMPP Install](assets/screenshots/ConfigureXamppPHPFile.png) 
   ![DB Setup](assets/screenshots/ConfigurePHPMyAdminRengokuDB.png)
   ![DB Setup](assets/screenshots/ConfigurePHPMyAdminRengokuDB1.png)

2. **osTicket Installation & Staff Control Panel**  
   ![osTicket Install](assets/screenshots/DLosTicket.png)
   ![osTicket Install](assets/screenshots/osTicketInstaller.png)
   ![osTicket Install](assets/screenshots/osTicketInstalled.png)
   ![osTicket Install](assets/screenshots/ConfigureosTicketPowerShell.png)
   ![Staff Control Panel](assets/screenshots/osTicketStaffControlPanel.png)

3. **API Integration with Elastic**  
   ![API Key](osTicketAPIKeyGenerate.png)  
   ![Webhook Setup](assets/screenshots/osTicketWebhookConnector.png)
   ![YML File Configuration](assets/screenshots/ConfigureElasticCLIymlosTickethyperlink.png)
</details>

<details>
<summary>Triage & Investigation Workflow</summary>

1. **Investigating Alerts in osTicket**  
   ![Investigate Alert](assets/screenshots/ElasticosTicketPOC.png)
   ![Investigate Alert](assets/screenshots/InvestigationRDP.png) 
   ![AbuseIPDB Check](assets/screenshots/InvestigationRDP1.png)  
   ![GreyNoise Check](assets/screenshots/InvestigationRDP2.png)
   ![Elastic Query](assets/screenshots/InvestigationRDP3.png)
   ![Elastic Query](assets/screenshots/InvestigationRDP4.png)
   ![Elastic Query](assets/screenshots/InvestigationRDP5.png)
   ![Elastic Query](assets/screenshots/InvestigationRDP6.png)
   ![Elastic Query](assets/screenshots/InvestigationRDP7.png)
   ![Elastic Query](assets/screenshots/InvestigationRDP8.png)
   ![Elastic Query](assets/screenshots/InvestigationRDP9.png)
   ![Elastic Query](assets/screenshots/InvestigationRDP10.png)
   ![Elastic Query](assets/screenshots/InvestigationRDP11.png)
   ![Elastic Query](assets/screenshots/InvestigationRDP12.png)
   ![Elastic Query](assets/screenshots/InvestigationRDP13.png)
   ![Elastic Query](assets/screenshots/InvestigationRDP14.png)
   
   
2. **Elastic Alert Correlation & Ticketing**  
   ![Elastic Alert Ticket](assets/screenshots/Alerts.png)  
   ![Ticket Link to Elastic](assets/screenshots/ElasticosTicketFormat.png)
   ![Ticket Link to Elastic](assets/screenshots/ElasticosTicketFormat1.png)

3. **Response Actions & Lessons Learned**  
   - Isolate hosts  
   - VirusTotal checks
     ![Virustotal](assets/screenshots/IRVirusTotal.png)  
   - Autoruns / Scheduled Tasks
     ![Taskcheck](assets/screenshots/IRschTaskcheck.png)
     ![Findstr](assets/screenshots/IRMalwarefindstr.png) 
   - Full AV scans
     ![AVrun](assets/screenshots/IRAntivirusRun.png)
   - Save filehashes for threat intelligence  
   - Key lessons: Keep security on, avoid suspicious links

4. **Elastic EDR Automated Actions**
   ![Elastic Defend](assets/screenshots/ElasticDefend.png)
   ![Elastic Defend](assets/screenshots/ElasticDefendEnrolled.png)
   ![EDR Isolation](assets/screenshots/IRElasticDefendSOAR.png)
   ![EDR Isolation](assets/screenshots/ElasticDefendAlert.png)
   ![EDR Isolation](assets/screenshots/ElasticDefendAlert1.png)
</details>

