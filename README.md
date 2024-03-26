# 1. Enabling copy-paste from Windows to Ubuntu Virtualbox
1. Start your Ubuntu Virtual machine in VirtualBox.
2. From the VirtualBox menu, go to **Devices** > **Insert Guest Additions CD Images**. This will mount the Guest Additions ISO file inside the virtual machine.
   ![image](https://github.com/s371506/acit2410/assets/113550989/c712d2c6-367a-4466-bc05-4bdc5d63941b)
3. Click the CD sign (highlighted in yellow) below the terminal. Once the folder is opened, click three dots, and on a drop-down menu, click **Open in Terminal**.
   ![image](https://github.com/s371506/acit2410/assets/113550989/0e8141fe-e0f9-4e7e-9616-b954865ec571)
4. Once the folder is opened in the terminal, give a *ls* command and then give **sudo ./VBoxLinuxAdditions.run**.
   ![image](https://github.com/s371506/acit2410/assets/113550989/2062dd22-6eb9-43e4-808f-235a7a6f1b32)
5. Once it is installed, go to the virtual box and click on settings.
   ![image](https://github.com/s371506/acit2410/assets/113550989/9c2138e9-4f81-4ab1-b5a5-d2eb4bfeaff7)
6. Then on **General** --> click **Advanced** tab --> **shared clipboard & drag and drop** set both **bidirectional**. Then click OK.
   ![image](https://github.com/s371506/acit2410/assets/113550989/49da590d-8b6b-465b-87df-dcc8c962506e)
7. For those that have graphical problems after installing additional features, go to **Settings** --> **Display** --> Click **Screen** tab --> and **enable 3D acceleration**.
   ![image](https://github.com/s371506/acit2410/assets/113550989/0740a4f5-d73d-47d7-a3d8-19e309df6cf4)

# 2. Installing Nginx in Ubuntu

Nginx is one of the most popular web servers in the world and is responsible for hosting some of the largest and highest-traffic sites on the internet. It is a lightweight choice that can be used as either a web server or reverse proxy.
1. Before installing Nginx, we give first a **sudo apt update**.
2. Installing Nginx.
 |  Installing Nginx       |
 | ----------------------- |  
 | sudo apt install nginx  | 






