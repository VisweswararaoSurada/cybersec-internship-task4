# Cybersecurity Internship - Task 4 (Linux Firewall with UFW)
**Task:** Configure firewall rules on Linux using UFW

## Objective
Learn how to configure and manage firewall rules in Linux to allow and block specific network traffic.

## Steps I Followed
1. Installed UFW (if not already installed):  
   ```bash
   sudo apt install ufw -y
   ```

2. Checked firewall status:  
   ```bash
   sudo ufw status
   ```

3. Enabled UFW:  
   ```bash
   sudo ufw enable
   ```

4. Set default policies:  
   ```bash
   sudo ufw default deny incoming
   sudo ufw default allow outgoing
   ```

5. Allowed SSH (port 22):  
   ```bash
   sudo ufw allow 22/tcp
   ```

6. Blocked Telnet (port 23):  
   ```bash
   sudo ufw deny 23/tcp
   ```

7. Listed rules:  
   ```bash
   sudo ufw status numbered
   ```

8. Deleted a rule (example: delete rule #2):  
   ```bash
   sudo ufw delete 2
   ```

## Example Output
```
Status: active

To                         Action      From
--                         ------      ----
22/tcp                     ALLOW       Anywhere
23/tcp                     DENY        Anywhere
```

## Files in this Repo
- `README.md` — explanation of steps and learning outcome  
- `firewall_commands.txt` — actual commands and outputs (to be filled by me)  
- `screenshots/` — screenshots of commands and results  

## What I Learned
- How to enable and configure UFW on Linux.  
- Difference between allowing and denying ports.  
- Why blocking unused services (like Telnet) is important.  
- How to check, add, and remove firewall rules.  
