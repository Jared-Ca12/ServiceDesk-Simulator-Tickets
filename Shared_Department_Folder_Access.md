# ServiceDesk Simulator — Ticket Log

## INC563406 — Need access to shared department folder

- **Priority:** Medium
- **Reported by:** Michael Brown (mbrown@servicedesk-simulator.com)
- **Department / Location:** Engineering / Floor 2
- **Contact:** x6270

### Issue Description
> I don't have my team's shared folder on my computer. My teammates can open it just fine. I need to be able to get to those files to do my work.

### Troubleshooting Performed (per requester)
- Teammates can open the shared folder fine
- The drive isn't showing up on his computer

### Business Impact
Cannot access shared team files needed for daily work.

### Actions Taken
1. Opened **Tools → AD (Directory)** and searched for Michael Brown. Checked his **Groups** tab — he was already a member of Domain Users, Engineering, CodeRepo-Access, Server-Admins, and Management, so a missing group wasn't the cause.
2. Opened **Tools → Remote Support**, connected to his workstation (SD1027), and logged in with admin credentials.
3. Checked **File Explorer** — Cloud Drive (personal cloud storage) was present and synced, but that's separate from the department share.
4. Checked **VPN Client** — connected and active (not a VPN issue; connected via Ethernet anyway).
5. Checked **Settings → Network** — connected to the CORP.LOCAL domain, network healthy.
6. In **File Explorer → This PC**, found the actual problem: a **"D: Engineering Department Drive"** was listed but showing **Offline**.
7. Checked **Tools → Server Room** (Overview, Topology, Servers tabs) to rule out a backend outage — all 13 nodes up, all 5 servers healthy, including the file server (FILESERV01).
8. Opened a **Terminal** on the remote PC and ran `ping 10.0.2.0` (server VLAN) — 0% packet loss, confirming network connectivity was fine.
9. Removed the broken offline D: drive mapping and reopened **Map Network Drive** (Drive letter D:).
10. Opened **Tools → Documentation Station → Server Documentation → File Server** to look up the correct share path convention. Docs confirmed: `D: = Department` share, mapped to `\\FILESERV01\departments\{dept}`.
11. Entered `\\FILESERV01\departments\Engineering` as the folder path and finished the drive mapping.
12. Ticket automatically marked **"Solution complete."**
13. Reviewed the resolution and clicked **Close Ticket**.

### Resolution
The department shared drive (D:) was mapped to a broken/offline path on Michael Brown's workstation, even though he had the correct AD group membership and the file server was healthy. Re-mapping the D: drive to the correct UNC path (`\\FILESERV01\departments\Engineering`, per the File Server documentation) restored his access. Ticket closed.
