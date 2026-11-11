# ServiceDesk Simulator — Ticket Log

## INC503081 — Printer says offline and will not print since yesterday

- **Priority:** High
- **Reported by:** Ivana Petrova (ipetrova@servicedesk-simulator.com)
- **Department / Location:** Engineering / Remote (Working from home)
- **Contact:** x6180
- **Printer:** Floor1-Printer-A

### Issue Description
> My printer just shows as offline today. I tried restarting my computer and it's still offline in the settings. I think it started after the maintenance over the weekend.

### Troubleshooting Performed (per requester)
- Printer says offline
- Restarted computer, still offline
- Started after the weekend maintenance

### Business Impact
Cannot print important reports needed for Monday morning meeting.

### Actions Taken
1. Checked **Tools → Server Room** to confirm the print server was online.
2. Opened **Tools → Remote Support** and connected to Ivana Petrova's desktop.
3. Checked for and installed any pending **system updates**.
4. Went to **Devices** and removed the old/stale printer entry.
5. Checked **Tools → Documentation Station** and found the correct current IP address for Floor1-Printer-A (the weekend maintenance had apparently changed it).
6. Went back to the remote desktop and added/connected the printer using the correct IP address.
7. Ticket automatically marked **"Solution complete."**
8. Reviewed the resolution and clicked **Close Ticket**.

### Resolution
The weekend maintenance changed the printer's IP address, so the old printer entry on Ivana's machine pointed to a stale address and showed as offline. Removed the old printer, looked up the correct IP in Documentation Station, and reconnected the printer with the updated address. Ticket closed.
