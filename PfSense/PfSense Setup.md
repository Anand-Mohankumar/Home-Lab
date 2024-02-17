# Setting up pfSense in Virtualbox

pfSense is a free and open source firewall and router that can be installed on a variety of hardware platforms or as a virtual machine. It offers many features such as network address translation (NAT), port forwarding, VPN, traffic shaping, firewall rules, and more. In this article, we will show you how to set up pfSense as a virtual machine in Virtualbox

## Prerequisites

Before we begin, you will need the following:

- A computer with Virtualbox installed. You can download Virtualbox from here.
- A pfSense ISO image file. You can download the latest version of pfSense from here.
- A network adapter that supports bridged mode. This will allow your pfSense virtual machine to communicate with your physical network.

## Step 1: Create a new virtual machine

- Open Virtualbox and click on the **New** button to create a new virtual machine.
- Give your virtual machine a name, such as **pfSense**, and choose **BSD** as the type and **FreeBSD (64-bit)** as the version.
- Click on **Next** and allocate some memory for your virtual machine. The recommended minimum is **512 MB**, but you can increase it if you have enough RAM.
- Click on **Next** and choose to create a virtual hard disk. The recommended minimum size is **8 GB**, but you can increase it if you have enough disk space.
- Click on **Create** and choose **VDI (VirtualBox Disk Image)** as the hard disk file type.
- Click on **Next** and choose **Dynamically allocated** as the storage on physical hard disk.
- Click on **Next** and select a location and a name for your virtual hard disk file.
- Click on **Create** to finish creating your virtual machine.

## Step 2: Configure the network settings

- Select your virtual machine and click on the **Settings** button.
- Click on the **Network** tab and select **Adapter 1**.
- Check the **Enable Network Adapter** box and choose **Bridged Adapter** as the attached to option.
- Select your physical network adapter from the name drop-down menu. This will allow your virtual machine to get an IP address from your router or DHCP server.
- Click on **OK** to save the settings.

## Step 3: Attach the pfSense ISO image file

- Select your virtual machine and click on the **Settings** button.
- Click on the **Storage** tab and select the **Empty** controller under the **Controller: IDE** section.
- Click on the **Optical Drive** icon and choose **Choose a disk file**.
- Browse to the location where you downloaded the pfSense ISO image file and select it.
- Click on **Open** and then **OK** to attach the ISO image file to your virtual machine.

## Step 4: Start the virtual machine and install pfSense

- Select your virtual machine and click on the **Start** button to boot it up.
- You will see a welcome screen with some options. Press **Enter** to accept the default option of **Boot Multi User**.
- You will see a license agreement screen. Press **Accept** to continue.
- You will see a menu with some options. Choose **Quick/Easy Install** to start the installation process.
- You will see a warning screen. Press **OK** to confirm that you want to erase the entire disk and install pfSense.
- You will see a screen asking you to choose a kernel. Choose **Standard Kernel** and press **OK**.
- You will see a screen asking you to reboot. Press **Reboot** to restart your virtual machine.
- You will see a screen asking you to eject the installation media. Press **F12** and choose **Devices > Optical Drives > Remove disk from virtual drive**.
- Press **Enter** to continue booting your virtual machine.

## Step 5: Configure the pfSense web interface

- After your virtual machine reboots, you will see a screen with some information and options. Note down the **LAN** IP address, which is usually **192.168.1.1** by default.
- Open a web browser on your host computer and enter the LAN IP address of your pfSense virtual machine. You will see a security warning. Click on **Advanced** and **Proceed** to continue.
- You will see a login screen. Enter **admin** as the username and **pfSense** as the password. Click on **Sign In** to access the web interface.
- You will see a setup wizard. Click on **Next** to start the configuration process.
- You will see a screen asking you to set a new password for the admin account. Enter a strong password and confirm it. Click on **Next** to continue.
- You will see a screen asking you to set the hostname and domain name for your pfSense system. Enter a hostname, such as **pfSense**, and a domain name, such as **localdomain**. Click on **Next** to continue.
- You will see a screen asking you to configure the time zone and NTP settings. Choose your time zone and NTP server. Click on **Next** to continue.
- You will see a screen asking you to configure the WAN interface. Choose **DHCP** as the type and leave the other settings as default. Click on **Next** to continue.
- You will see a screen asking you to configure the LAN interface. You can change the IP address and subnet mask if you want, but make sure they are compatible with your physical network. Click on **Next** to continue.
- You will see a screen asking you to set the admin web interface port. Leave it as **443** by default. Click on **Next** to continue.
- You will see a screen asking you to reload the configuration. Click on **Reload** to apply the changes.
- You will see a confirmation screen. Click on **Finish** to complete the setup wizard.

## Step 6: Test the pfSense firewall

- You can now test the pfSense firewall by accessing the web interface from your host computer or any other device on your network. You can also ping the WAN IP address of your pfSense virtual machine from your host computer or any other device on the internet.
- You can also use the pfSense web interface to configure various features and settings, such as firewall rules, NAT, VPN, traffic shaping, and more. For more information, you can refer to the official documentation of pfSense here.

### Congratulations, you have successfully set up pfSense firewall in Virtualbox! 🎉