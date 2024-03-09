# Automation with Ansible
The objective of this repository is to provide Ansible playbooks to automate current tasks for deploying, hardening and managing RHEL servers.  
- Deploying RHEL on remote host
- Hardening the SSH configuration
- Deploying Traefik as reverse proxy

## Useful commands

Verify your RHEL OS version:  
```
cat /etc/redhat-release
```

Verify the kernel version on your RHEL OS:  
```
uname -r
```

Update packages list:  
```
sudo dnf update
```

Check for updates:  
```
sudo dnf check-update
```

Apply updates:  
```
sudo dnf upgrade
```

You might have the latest kernel version installed on your system but not active yet  
*Security: kernel-core-5.14.0-284.30.1.el9_2.x86_64 is an installed security update*    
*Security: kernel-core-5.14.0-284.25.1.el9_2.x86_64 is the currently running version*    
In this case you need to reboot the server:  
```
sudo dnf reboot
```

List all installed packages:  
```
rpm -qa
```

This can return a lot of packages. To count the installed packages:  
```
rpm -qa | wc -l
```
