# linux-command-line-cheat-sheet

## Change password on root user and user account

To change the root password:

`sudo passwd`

To change your user password:

`passwd`

To change other users password:

`sudo passwd USERNAME`

[ref: change-password-on-root-user-and-user-account](https://askubuntu.com/questions/423942/change-password-on-root-user-and-user-account)


## HOST name change:

`sudo nano /etc/hosts` - then rename 

and 

`hostnamectl set-hostname new-hostname`

[ref : how-do-i-change-the-hostname](https://askubuntu.com/questions/87665/how-do-i-change-the-hostname-without-a-restart)


## ipv4 forward related permanent

```sh
cat /proc/sys/net/ipv4/ip_forward
sudo nano /etc/sysctl.conf
sudo /etc/init.d/procps restart
cat /proc/sys/net/ipv4/ip_forward
```

###### For temp on any session:
```sh
cat /proc/sys/net/ipv4/ip_forward
echo 1 > /proc/sys/net/ipv4/ip_forward
```

[ref: how-to-make-ip-forwarding-permanent](https://askubuntu.com/questions/311053/how-to-make-ip-forwarding-permanent)


## SSH:
```sh
sudo apt-get update
sudo apt-get install openssh-server
```

[ref : why-am-i-getting-a-port-22-connection-refused-error](https://askubuntu.com/questions/218344/why-am-i-getting-a-port-22-connection-refused-error)

