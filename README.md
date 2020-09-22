# Termux Sudo Without Root  
In this repository, I've created a Sudo Script That Provides Sudo Utilities For Termux. It can run on both rooted & **Non-rooted** devices!  

### What's new in version 2.3.6?  
> Sudo is now compatible with su binary with direct execution  

> Minor bug fixes


### What's new in version 2.2.4?  
> Sudo is now available as compressed debian package (.deb file)  

> Minor bug fixes

__Support My Work By Starring This Repository on Github.__  

**WARNING: Sudo will run on non-rooted devices but it doesn't provide root permissions on your device!**  

### Installation  
  1. First, Download My Repository As ZIP or Clone it via your terminal. So, Run  
  
  ```
    $ apt update && apt upgrade  
    $ apt install git
  ``` 

    
After That, Run  


  ```  

    $ git clone http://github.com/virtual-designer/termux-sudo-without-root  
    $ cd termux-sudo-without-root/  
    $ apt install ./sudo.deb
  ```  


  And voila!  
  You're ready use sudo!  
  Just type 'sudo' on your terminal.  
  
### Configuring Sudo  
  **By default, sudo will allow only root user to execute commands with it.**  
  But You add your own users.  


  **By Default, you won't asked for password if the user is 'root'**  


  Run  
  ```
    $ cd /data/data/com.termux/files/usr/etc
    $ nano sudoers
  ```

Now this will throw an error.  

 
  ```
   [The file is unwritable!]
  ```  

So, We need to change permissions of sudoers file.  

  ```
    $ chmod +w sudoers
  ```

Then add users as you wish.  

For security, You could change the permission of sudoers again.  


  ```
    $ chmod -w sudoers
  ```  

  <br>
  <br>


  **Commands are not Running as Root (This topic is only for the root users)**  

  
  Then you may face a problem that the commands are not running as root!  
  Don't fare!  
  Just open that **sudoers.d/** directory and then run  
  ```
    $ nano sudo-exec.conf
  ```  
  
  Now this will open the file 'sudo-exec.conf'.  
  
  Just Edit the first line:
    ```
      exec_as_root: true
    ```  
  Then restart your terminal.
  
  Now it will Start to execute commands as root if you have root & you have granted it.
  

For more details, Run  

```
  $ sudo -h
```  


If you saw a bug, plese report me to my Email address.  


> Email: help@http.packagehouse.ml

*Don't forget to follow my profile!*  

Thanks For Taking a Look to This Repository.

