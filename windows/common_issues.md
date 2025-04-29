# Windows Troubleshooting Notes

## Printer Not Responding
Restart the print spooler service:
```
net stop spooler
net start spooler
```

## Network Reset
```
netsh winsock reset
netsh int ip reset
```