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

###### IPv4 forward for a temp on any session:
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

## How to install a deb file, by dpkg -i or by apt?
Install your `foo.deb` file with `sudo dpkg -i foo.deb`.

If there are some errors with unresolved dependencies, run `sudo apt-get install -f` or `sudo apt-get install -f --fix-missing` afterwards.

[ref: how-to-install-a-deb-file-by-dpkg](https://unix.stackexchange.com/questions/159094/how-to-install-a-deb-file-by-dpkg-i-or-by-apt)

## Installing a root/CA Certificate in ubuntu

Given a CA certificate file `alamin.crt`, follow these steps to install it on Ubuntu:
1.  [ **Optional** ] Create a directory for extra CA certificates in `/usr/share/ca-certificates`:
  
  `sudo mkdir /usr/share/ca-certificates/extra`

2.  Copy the `CA` `.crt` file to this directory:
  
  `sudo cp alamin.crt /usr/share/ca-certificates/extra/alamin.crt`

3.  Let Ubuntu add the `.crt` file's path relative to `/usr/share/ca-certificates` to `/etc/ca-certificates.conf`:

  `sudo dpkg-reconfigure ca-certificates`

- In case of a .pem file on Ubuntu, it must first be converted to a `.crt` file:

  `openssl x509 -in foo.pem -inform PEM -out foo.crt`

###### To do this non-interactively, run:

```sh
sudo update-ca-certificates
```

[ref: Installing a root/CA Certificate in ubuntu](https://askubuntu.com/questions/73287/how-do-i-install-a-root-certificate)


## Configure a network interface into promiscuous mode
Your interface is not in promiscous mode. Use:
`ip link set eth1 promisc on`
`netstat -i`
**The flag will be updated to `BMPRU`. Flag details are as follows:**

- `B` flag is for broadcast
- `M` flag is for multicast
- `P` flag is for promisc mode
- `R` is for running
- `U` is for up

[ref: configure-a-network-interface-into-promiscuous-mode](https://askubuntu.com/questions/430355/configure-a-network-interface-into-promiscuous-mode)


## Cheat Sheet
- [ref: Linux command line for you and me Documentation By Kushal Das](https://media.readthedocs.org/pdf/lym/latest/lym.pdf)
- [ref: best-linuxunix-command-cheat-sheet ](https://rumorscity.com/2014/08/16/6-best-linuxunix-command-cheat-sheet/)

## cat command

```cat filename``` - to see the content of a file

## head command
```head filename``` - to see first 10 lines of the content of a file \
```head -20 filename``` - to see first 20 lines of the content of a file

## tail command
```tail filename``` - to see last 10 lines of the content of a file \
```tail -20 filename``` - to see last 20 lines of the content of a file

## Numbering the Lines
```nl filename``` - to see the content of a file with number

## Filtering Text with grep
```cat filename | grep some_text``` - to see the content of a file with filtered text only

# Mac-command-line-cheat-sheet

## How to Allow Apps from Anywhere in macOS Gatekeeper (Mojave, Sierra, High Sierra)
- [ref: How to Allow Apps from Anywhere in macOS Gatekeeper -Mojave](http://osxdaily.com/2016/09/27/allow-apps-from-anywhere-macos-gatekeeper/)



###### To do disable, run:
      
```sh
sudo spctl --master-disable
```


###### To do enable, run:

```sh
sudo spctl --master-enable
```

###### Checking for existing SSH keys

Before you generate an SSH key, you can check to see if you have any existing SSH keys.

1. Open Terminal.
Enter `ls -al ~/.ssh` to see if existing SSH keys are present:
`$ ls -al ~/.ssh`
Lists the files in your `.ssh` directory, if they exist
Check the directory listing to see if you already have a **public SSH key**.


##  What is the correct way to alias applications in OS X through bash?

**TEMP**

`alias tmc='/Users/alamin/work/gitLab/machine-learning/MOOC_Data_Analysis_with_Python_Summer_2019/./tmc'`

NOTICE the /./ at the end,

**For PERMANENT**
`ln -s /Users/alamin/work/gitLab/machine-learning/MOOC_Data_Analysis_with_Python_Summer_2019/./tmc /usr/local/bin/tmc`

[reference: configure-a-network-interface-into-promiscuous-mode](https://superuser.com/questions/386345/what-is-the-correct-way-to-alias-applications-in-os-x-through-bash)
