# TrueNAS Scale & TrueCharts Install and Setup Guide
A step by step guide to installing TrueNAS Scale and TrueCharts. I wrote this guide to assist my students in installing TrueNAS Scale and TrueCharts. TrueCharts has great documentation, but this guide serves to simplify and structure the install and setup process for those who have not done this type of work before.

### What is TrueNAS Scale?
TrueNAS Scale is a Linux based NAS (Network Attached Storage) operating system by [IX Systems](https://www.ixsystems.com) which allows you to not only operate NAS in your environment but also run container applications within it. Containers in Scale are based on Kubernetes and Docker.

### What is TrueCharts?
TrueCharts is a open source project that works to easily operate containers based on kubernetes from several "charts", one of those being TrueNAS Scale. It is in active development and is generally very stable. It is not considered "Production Ready" but is stable if managed correctly and a excellent entry to containers and working with containerized software. [Project Scope](https://truecharts.org/manual/scope)

## TrueNAS Scale

1. Download the TrueNAS SCALE ISO image from the official website (https://www.truenas.com/download-truenas-scale/).

2. Create a bootable USB drive using the downloaded ISO image. You can use tools like Rufus, UNetbootin, or Etcher to create a bootable USB drive.
   I have a preference to [SUSE Image Writer](https://software.opensuse.org/package/imagewriter) on Linux, but others listed will work also depending on your platform.

4. Insert the bootable USB drive into the computer where you want to install TrueNAS SCALE.

5. Boot the computer from the USB drive. To do this, **you may need** to enter the BIOS settings and change the boot order to prioritize the USB drive. On the HP ProLiant servers i have installed this on several times, this is usually **F9** for example. On most hardware it is usually **DEL** key.

6. Once the computer boots from the USB drive, you will see the TrueNAS SCALE installer screen. Select the language and keyboard layout that you want to use.

7. Next, you need to select the disk or disks where you want to install TrueNAS SCALE. You can choose to install on a single disk or set up a RAID array for better data protection.

8. After selecting the disks, you will be prompted to create a root password for the TrueNAS SCALE installation.

9. Once you have set up the root password, the installation process will begin. This may take some time, depending on the speed of your computer and the size of the disks.

10. When the installation is complete, you will be prompted to remove the USB drive and reboot the computer.

11. After the computer reboots, you can access the TrueNAS SCALE web interface by entering the IP address of the computer in a web browser on another device on the same network.

12. The first time you log in to the TrueNAS SCALE web interface, you will be prompted to set up a storage pool and share.

Finally, you can start using TrueNAS SCALE to manage your storage and data.

## TrueCharts

Adding TrueCharts is easy and requires you add several "trains" of software charts.

1. Select Apps on the left menu
![Screenshot of TrueNAS Scale Menu with Apps marked.](truenas_1.png)
2. Click on Manage Catalogs
![Screenshot of TrueNAS Scale Menu with Apps marked.](truenas_2.png)
3. Click Add Catalog
![Screenshot of TrueNAS Scale Menu with Apps marked.](truenas_3.png)
4. Skip over the iXsystems notice, click Continue and enter the following information: 
  - Name: truecharts 
  - Repository: https://github.com/truecharts/catalog 
  - Preferred Trains: enterprise,stable and operators (type each one manually) 
  - Branch: main

![Screenshot of TrueNAS Scale Menu with Apps marked.](truenas_4.png)

5. Click Save and wait for the App Catalog to update. This can take a minute to several minutes.

## Guides for installing Applications

List of applications and guides i keep here.

- [Nextcloud](ruecharts.org/charts/stable/nextcloud/](https://truecharts.org/charts/stable/nextcloud/)https://truecharts.org/charts/stable/nextcloud/).
