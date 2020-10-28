## Ubuntu

* **Create a virtual machine containing Ubuntu**

— Click the "New" button.

![path](pictures/fig-8.png)

— In the settings window specify the "Name" (in the future you can change), the "Type" and "Version" of the operating system and click "Next".  For example - Name: My_Ubuntu (o_0), Type: Linux, Version: Ubuntu (64-bit).

![path](pictures/fig-9.png)

— The machine claims that the minimum memory size (RAM) requirements for full-fledged work Linux,, 1024MB. But if you want your machine to work well, then select the volume for more depending on the RAM of your computer (2 GB if RAM of your computer 8 GB) and click "Next". Sometimes even more, it all depends on the tasks and how many Virtual Machines you will run at the same time.

![path](pictures/fig-10.png)

— So we went to create a virtual hard disk. Click "Create":

![path](pictures/fig-10-1.png)

— Specify the type of hard disk (VDI - VirtualBox Disk Image) and click "Next":

![path](pictures/fig-11.png)
(Choose the first item, as it is easier. You have created a file that will simulate the hard disk of your virtual machine. If necessary, you can transfer it to another computer and run there).

— In the window that appears, put a tick in "Dynamically allocated", after click "Next":

![path](pictures/fig-12.png)

-The  hard disk size set at least 80 GB (or more) and click "Create".

![path](pictures/fig-12-1.png)

— Now the Virtual Machine is ready, but without an operating system. Start the Virtual Machine by clicking on the right mouse button and select **"Start" -> "Normal start"**.

![path](pictures/fig-12-2.png)

— When you first start you will be prompted to select the installation file from which the installation will be performed. You can download the installation file from the [official website](https://ubuntu.com/download/desktop). Select the installation file from the Downloads folder (or where you saved it) and click "Start".

![path](pictures/fig-13.png)

— In the window that appears, select the operating system language and click on "Install Ubuntu". Next, select the keyboard language.

![path](pictures/fig-14.png)

— After selecting the keyboard language, just click on "Continue"

![path](pictures/fig-15.png)

— *Disk layout*. You can choose installation type. Simply format the entire hard drive and install Ubuntu on it, or select the manual option (Set the checkbox to "Something else" option and click "Continue"):

![path](pictures/fig-16.png)

— In the opened window, if you have not yet marked up the hard drive, you need to create a partition table, to do this, click "New Partition Table...".

![path](pictures/fig-17.png)

— Four sections are recommended for Linux:

* / - ext4, size 10-50 GB, for system installation
* /boot - ext2, size 100 MB, for bootloader files
* swap - swap, size equals RAM, for swap
* /home - ext4, all remaining space

— To create a new section, click the "+" button:

![path](pictures/fig-18.png)

— Here you need to specify the mount point, for example, **/** or **/home**, size, file system and you can set a label:

 ![path](pictures/fig-19.png)

— In the end, you should have something like this:

![path](pictures/fig-20.png)
Then click "Install Now".

— You should have this window:

![path](pictures/fig-21.png)
Check that everything is correct, click "Continue".

— Select your time zone:

![path](pictures/fig-22.png)

— Enter your Username, computer name and password:

![path](pictures/fig-23.png)

— Installing your operating system:

![path](pictures/fig-24.png)

— Enjoy your virtual machine:

![path](pictures/fig-25.png)

## VM with Docker container and Jupyter Lab
