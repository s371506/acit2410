# Enabling copy paste from Windows to Ubuntu Virtualbox
1. Start your Ubuntu Virtual machine in VirtualBox.
2. From the VirtualBox menu, go to **Devices** > **Insert Guest Additions CD Images**. This will mount the Guest Additions ISO file inside the virtual machine.
   ![image](https://github.com/s371506/acit2410/assets/113550989/d976e677-a092-4ef5-800d-8ec88bde01df)
3. Click the CD sign (highlighted with yellow) below the terminal. Once the folder is opened click three dots and on a drop-down menu click **Open in Terminal**.
   ![image](https://github.com/s371506/acit2410/assets/113550989/d08d95a7-e784-4f76-b15c-afa38f076223)
4. Once the folder is opened in terminal, give a *ls* command and then give **sudo ./VBoxLinuxAdditions.run**.
   ![image](https://github.com/s371506/acit2410/assets/113550989/c35fd7fc-28d5-442a-a784-817106b225bd)
5. Once it is installed go to the virtual box, click on settings.
   ![image](https://github.com/s371506/acit2410/assets/113550989/9c2138e9-4f81-4ab1-b5a5-d2eb4bfeaff7)
6. Then on **General** --> click **Advanced** tab --> **shared clipboard & drag and drop** set both **bidirectional**. Then click OK.
   ![image](https://github.com/s371506/acit2410/assets/113550989/49da590d-8b6b-465b-87df-dcc8c962506e)
7. For those that have graphical problems after installing additional features, go to **Settings** --> **Display** --> Click **Screen** tab --> and **enable 3D acceleration**.
   ![image](https://github.com/s371506/acit2410/assets/113550989/0740a4f5-d73d-47d7-a3d8-19e309df6cf4)
   




