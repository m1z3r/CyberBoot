## Virtual Machine Download

You will use a local virtual machine for several units of this program, **beginning with Terminal Week and through the Linux weeks.**

You should have already downloaded and installed Virtual Box as part of pre-work. You should do so now if you have not already. 

Following Virtual Box installation, you will install a tool called Vagrant, which you will use to download the VM. 



The steps below can feel intimidating, especially if you are new to the command line. By lesson 2.3, make sure you have the correct versions of Virtual Box and Vagrant installed. Windows users also need to confirm that GitBash is installed. 

In 2.3, your instructor will demonstrate how to download the virtual machine. If you run into any issues, please use office hours afterwards to make sure that you have everything set up prior to Week 3, Day 1. 

### Downloading & Running the Machine

#### Windows and Mac Users

Windows users will need to install Git Bash. 
- If you have not yet downloaded GitBash, please do so here: [Git for Windows](https://gitforwindows.org/)

Mac users will use Terminal.
- You can open Terminal by clicking on the magnifying glass icon at the top right corner of your computer. Type in Terminal and press enter in order to open it. 

#### Virtual Box

Download and install `Virtual Box` at https://www.virtualbox.org/wiki/Download_Old_Builds_6_0

- Note that Vagrant requires Virtual Box version 6.0. It **will not work** with version 6.1, so please be sure to download from the link above.

- In pre-work you may have downloaded a more recent version. If this is the case, please make sure to download Virtual Box **version 6.0**

#### Vagrant

- Download and install the latest version of `Vagrant`, currently `2.2.7` at https://www.vagrantup.com/downloads.html

Select the appropriate installer for your operating system:

- The installer should save to your `~/Downloads` directory. 

- Open this folder, then double-click the installer. 

- This will install Vagrant on your system.


### Downloading the Virtual Machine 

**Note:** Your instructor will demonstrate this during Week 2, Day 3. If you run into any issues, please use office hours after that class to ensure that you are properly set up. 

After Vagrant is installed, unzip the directory and verify that you see `vagrant-linux.sh` and `Vagrantfile`.
Download and run the two files:

- Download the script, called `vagrant-linux.sh` 

- Download the `Vagrantfile`

Open **Git Bash** (Windows) or **Terminal** (Mac).

- **Note:** Windows users should make sure they open Git Bash as an administrator. This usually happens by default, but to verify, complete the following:

    - Search for **Git Bash** in the Windows search bar (bottom-left).
    - Right-click **Git Bash** and then click **Run as administrator**

On the command line, move to the directory where you downloaded the script and Vagrantfile. 

- Type  `cd ~/Downloads`  and press enter

Next, complete the following:

- **Windows** users type `bash vagrant-linux.sh --create` and press enter. 

- **Mac** users type `sudo bash vagrant-linux.sh --create` and press enter. 

This will download and start the VM. It will automatically appear in a GUI after it is downloaded and started. 

### **Accessing Your Virtual Machine**

You will learn how to access your virtual machine via the command line in the upcoming units. 

For now, you can open VirtualBox. You will see the machine you downloaded in the left hand pane. 

- Click the Linux machine.
- Then, click the Start icon in the top menu. 
- Allow 3-5 minutes for the machine to start up. 

Enter in the log-in credentials, when prompted:

* Username: `sysadmin`
* Password: `cybersecurity`

When you are done using the machine, you can close the window on the GUI (graphical user interface). This will give you options as to how to shut down. Make sure to select the first option **"Save the Machine State"**.

---

© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.   
