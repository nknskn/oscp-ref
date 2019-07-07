# builtin commands
- search files
~~~sh
find / -name "network-secret.txt"
locate "network-secret.txt"
~~~

- passwords
~~~sh
strings ./*.txt | grep password
grep -l -i pass /var/log/*.log 2>/dev/null
# searches for the string 'password' and output the line number
find / -maxdepth 10 -name *.conf -type f | grep -Hn pass; 2>/dev/null
find / -maxdepth 10 -name *etc* -type f | grep -Hn pass; 2>/dev/null  # as above, but in *etc*
~~~

- check permissions
~~~sh
find / -perm -4000 -type f 2>/dev/null        # Find SUID files
find / -uid 0 -perm -4000 -type f 2>/dev/null # Find SUID files owned by root
find / -perm -2000 -type f 2>/dev/null        # Find files with GUID bit set
find / -perm -2 -type f 2>/dev/null           # Find world-writable files
find / -perm -2 -type d 2>/dev/null           # Find word-writable directories
find /home –name .rhosts -print 2>/dev/null   # Find rhost config files
ls -ahlR /root/                               # list files recursively
~~~

- service information
~~~sh
ps aux | grep root
cat /etc/inetd.conf  # List services managed by inetd
cat /etc/xinetd.conf # As above for xinetd
~~~

- check using shell
~~~sh
ps -p $$
echo $PATH
export PATH=${PATH}:/some/path2
~~~

# My tools


# Third tools
- LinEnum.sh
~~~
wget https://raw.githubusercontent.com/s0wr0b1ndef/OSCP-note/e937ed11b3d66459e14c9ca4f823a9b3da7a88d3/PRIVESC/Linux/LinEnum.sh
chmod 755 ./LinEnum.sh
./LinEnum.sh
~~~
