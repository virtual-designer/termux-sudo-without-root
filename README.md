# Termux Sudo Without Root  
In this repository, I've created a Sudo Script That Provides Sudo Utilities For Termux. It can run on both rooted & **Non-rooted** devices!  

__Support My Work By Starring This Repository on Github.__  

**WARNING: Sudo will run on Non-rooted devices but It doesn't provide root permissions on your device!**  

### Installation  
  1. First, Download My Repository As ZIP or Clone it via your terminal. So, Run  
  ```
    apt update && apt upgrade  
    apt install git
  ```  

    After That, Run  


  ```  

    git clone http://github.com/virtual-designer/termux-sudo-without-root  
    cd termux-sudo-without-root/  
    ./install.exec
  ```  

  And voila!  
  You're ready use sudo!  
  Just type 'sudo' on your terminal.  
  
### Configuring Sudo  
  **By default, sudo will allow only root user to execute commands with it.**  
  But You add your own users.  


	**By Default, Password for root is __admin__**  


  Run  
  ```
    cd /data/data/com.termux/files/usr/etc
    nano sudoers
  ```
  
  You will see a error now.  
  
  It wiil say that the file 'sudoers' has no write permission.  
  
  So, you may run  
  
  ```
    chmod +w sudoers
  ```  
  
  And You can also change permissions of **sudoers.d/** directory.  
  
  run  
  
  ```
    chmod 755 sudoers.d/
  ```  
  
  Then open the file 'sudoers' with a text editor and add your custom users.  
  
  <br>
  <br>


  **Commands are not Running as Root (This topic is only for the root users)**  

  
  Then you may face a problem that the commands are not running as root!  
  Don't fare!  
  Just open that **sudoers.d/** directory and then run  
  ```
    nano config.yml
  ```  
  
  Now this will open the file 'config.yml'.  
  
  Just Edit the first line:
    ```
      exec_as_root: true
    ```  
  Then restart your terminal.
  
  Now it will Start to execute commands as root if you have root & you have granted it.
  
> Email: admin@coding-master.ml  

##### If you got a bug, plese report me to my Email address.  


*Don't forget to follow my profile!*  

Thanks For Taking a Look to This Repository.

