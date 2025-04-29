# 🛠️ IT Troubleshooting Notes (Windows & Linux)

This is a personal collection of basic troubleshooting guides and commands I’ve used or practiced during my IT learning journey and home lab experiments.

---

## Windows Issues

### No Internet / Network Issues
- Check physical connection
- Run:
  ```
  ipconfig /release
  ipconfig /renew
  ipconfig /flushdns
  ```
- Reset network stack:
  ```
  netsh winsock reset
  netsh int ip reset
  ```

### Printer Not Responding
- Restart Print Spooler:
  ```
  net stop spooler
  net start spooler
  ```

---

## Linux (Ubuntu/Debian)

### User Locked Out
- Boot into recovery mode
- Remount filesystem:
  ```
  mount -o remount,rw /
  ```
- Reset password:
  ```
  passwd <username>
  ```

### Disk Full
- Check usage:
  ```
  df -h
  du -sh /*
  ```
- Clean logs:
  ```
  sudo journalctl --vacuum-size=200M
  sudo apt-get autoremove && sudo apt-get clean
  ```

### Service Won’t Start
- Check status:
  ```
  systemctl status <service>
  ```
- Look at logs:
  ```
  sudo journalctl -xe
  ```

---

## What I’m Practicing
- System command-line tools  
- Troubleshooting methodology  
- Creating mini SOPs (standard operating procedures)

