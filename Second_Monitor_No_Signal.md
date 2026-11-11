# ServiceDesk Simulator — Ticket Log

## INC0012862 — My second monitor just went black and will not come back on

- **Priority:** Medium
- **Reported by:** Laura Santos (lsantos@servicedesk-simulator.com)
- **Department / Location:** Finance / Floor 2
- **Contact:** x4080

### Issue Description
> My second monitor just says "No Signal" and won't come on. It was working yesterday. The monitor itself powers on but my computer acts like it isn't even there.

### Troubleshooting Performed (per requester)
- Checked all the cables are plugged in
- Swapped in a different cable and tried the other video port on her PC — still "No Signal"
- Restarted the computer
- Borrowed a coworker's laptop to test the monitor — works on theirs

### Business Impact
Lost half of workspace. Productivity significantly reduced for financial reporting work during month-end close.

### Actions Taken
1. Opened the ticket and started a **Team Chat** with Laura Santos to run through troubleshooting steps.
2. Chatted with her to confirm the issue and offered to send a new video cable.
3. Went to **Ship Manager** and shipped an **HDMI Cable** (Rush Priority) to her address (5337 Sunset Boulevard, Denver, CO 80202) — **did not resolve the issue**, monitor still showed "No Signal."
4. Shipped a **DisplayPort Cable** as a second attempt (via a repeat shipment) — **also did not resolve the issue**.
5. Had her plug the cable directly into the PC — still "No Signal."
6. Had her check the monitor's on-screen buttons/menu — a menu appeared but signal was still missing.
7. Had her go into the monitor's **input menu and select HDMI** — still no change, "No Signal" persisted.
8. Opened **Tools → Remote Support**, searched for her workstation (SD1043), and connected.
9. Logged into the remote session using admin credentials.
10. Opened **System Update** on the remote PC and found 6 pending updates, including an outdated **Integrated Graphics Driver** and **discrete graphics card Driver**.
11. Installed the graphics driver updates, which triggered a system reboot/re-login on the remote session.
12. Logged back into the remote desktop after the update.
13. Confirmed with Laura in Team Chat — she reported the second monitor was back on and working.
14. Reviewed the ticket's "Solution complete" prompt and clicked **Close Ticket**.

### Resolution
The root cause was an outdated graphics driver, not a cable or monitor problem (the two cable shipments were a dead end). Updating the integrated/discrete graphics drivers via Remote Support resolved the "No Signal" issue on the second monitor. Ticket closed.
