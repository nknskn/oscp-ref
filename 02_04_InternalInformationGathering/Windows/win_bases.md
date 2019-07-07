# builtin commands
- find files
  ~~~cmd
  dir /s /b network-secret.txt
  
  dir /q calc.exe //display ownership
  dir /a:d calc.exe
  # d: Directories
  # h: Hidden files
  # s: System files
  ~~~

- network
  ~~~sh
  # Show all listening ports
  netstat -aon | find /i "listening" | findstr 127.0.0.1
  netstat -an | find /i "Listening"
  netstat -an | find /i "Established"

  # with PID
  netstat -abno
  
  type C:\Windows\system32\drivers\etc\hosts
    type c:\Winnt\system32\drivers\etc\hosts   # Windows 2000
  
  arp -a
  routeprint
  # From WinXP upwards
  netsh firewall show state
  netsh firewall show config
  
  ~~~

- Systems
  ~~~sh
  wmic os get osarchitecture
  systeminfo | findstr /B /C:"OS Name" /C:"OS Version"
  systeminfo
  echo %USERDOMAIN%\%USERNAME% # later win7 or win2008
  ~~~

- Windows services
  ~~~sh
  tasklist /svc
  # Queries the configuration information for a specified service.
  sc qc <service_name>
  ~~~

- check security policy
  ~~~sh
  net accounts
  ~~~

- list users
  ~~~sh
  net users
  # needs admin
  WMIC /NODE: "BOB" COMPUTERSYSTEM GET USERNAME
  ~~~

- check cacls
  ~~~sh
  #list privileges via cmd
  cacls *
  cacls "C:\Program Files" /T | findstr Users
  # lists permissions of *.exe and searches for the user and his full permissions string "IUSR_BOB:F". 
  cacls *.exe | findstr "IUSR_BOB:F"
  ~~~

- check registory
  ~~~sh
  #search for passwords in the Windows Registry
  reg query "HKLM\Software\Microsoft\WindowsNT\Currentversion\Winlogon"
  reg query "HKLM\System\CurrentControlSet\Services\SNMP"
  ~~~


