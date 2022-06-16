# Linux System Admin Primer

### Challenge
https://github.com/livialima/linuxupskillchallenge

### Linux Guide
https://tldp.org/LDP/intro-linux/html/index.html

### Basic Commands
- ps - report a snapshot of the current processes.
- df - report file system space usage
- du - Disk usage
- vim - visual editor
- top - display Linux processes
- less - show text in a pager
- more - display text
- zless - less in compressed mode
- grep - search text through files.
- cat - concatenate files and print on the standard output
- tail - Output the end of the files
- find - Use it to find files

### Check if SSH is enabled
```
systemctl status sshd
```
### Check for a Port that is listening on the server
```
ss -patun | grep 2222
```

## Firewall management

Install a package
```
yum install -y firewalld
```

List Firewall ports
```
firewall-cmd  --list-all
```

Add predefined services
```
firewall-cmd --permanent --add-service=httpd
```

List predefined services
```
firewall-cmd --get-services
```

Add a service to the firewall
```
firewall-cmd --permanent --add-service=http
firewall-cmd --reload
```

Open a port in linux, replace tcp with udp for UDP ports
```
firewall-cmd --add-port=portnumber/tcp --permanent
firewall-cmd --reload
```

### Selinux (Advanced) Turn it off for now

```
setenforce 0
```

Read about SELinux first

https://wiki.gentoo.org/wiki/SELinux/Tutorials

https://wiki.gentoo.org/wiki/Category:SELinux

https://wiki.gentoo.org/wiki/SELinux/Tutorials/How_SELinux_controls_file_and_directory_accesses

### Package Management
Install a package or multiple
```
yum install -y vim tmux
```
#### To view files owned by package
```
repoquery -l httpd
```
#### Get installed packages with the name httpd
```
yum list installed *httpd*
```
### Process Management

#### Grep Httpd pid
```
pgrep httpd
```

#### Grep process list
```
ps aux | grep httpd
```

#### Filter per process
```
ps -ylC httpd
```

#### File Processing

- vim → press i to go to insert mode, vimtutor will help you learn basic vim
- wc → Word Count for lines → wc -l ||  https://tldp.org/LDP/GNU-Linux-Tools-Summary/html/text-information-tools.html
- shell redirection, >, >>, 2>1  || https://tldp.org/LDP/abs/html/io-redirection.html

Basic file commands https://tldp.org/LDP/abs/html/basic.html
- less => View files in a pager mode -> Ability to view and search text
- cat → Spit all the lines to the terminal
- zless → compressed files 
- zgrep → grep through compressed files
