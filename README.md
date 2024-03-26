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
   Installing Nginx |
   -----------------|
   *sudo apt install nginx* |
3. Before testing Nginx, the firewall software needs to be configured to allow access to the service. Nginx registers itself as a service with ufw upon installation, making it straightforward to allow Nginx access
   Checking services in firewall |
   :------------------------------:|
   *sudo ufw app list* |
4. From the output list that will be we allow “Nginx HTTP”
   Allowing Nginx HTTP |
   :------------------:|
   *sudo ufw allow 'Nginx HTTP'*|
   *sudo ufw status*
6. At the end of the installation process, Ubuntu 22.04 starts Nginx. The web server should already be up and running.
To check if the nginx is running and active, we use this command:
   Checking nginx status |
   :--------------------:|
   *systemctl status nginx*|

    ![image](https://github.com/s371506/acit2410/assets/113550989/8cf59924-5cbf-460f-9b75-06bb0476b92c)


# 3. Installing Docker in Ubuntu

1. The Docker installation package available in the official Ubuntu repository may not be the latest version. We’ll install Docker from the official Docker repository to ensure we get the latest version. To do that, we’ll add a new package source, add the GPG key from Docker to ensure the downloads are valid, and then install the package.
**sudo apt update**
2. Next, install a few prerequisite packages which let apt use packages over HTTPS:
   Installing prerequisite packages|
   :------------------------------: |
   *sudo apt install apt-transport-https ca-certificates curl software-properties-common*|
3. Then add the GPG key for the official Docker repository to your system:
   Adding GPG key for Docker repository|
   :----------------------------------:|
   *curl -fsSL https://download.docker.com/linux/ubuntu/gpg  \| sudo gpg -dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg*|
4. Even though this one is especially long, still it needs to be used in one line:
   Past this in one line |
   :------------------:|
   *echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null* |
5. Update your existing list of packages again for the addition to be recognized: **sudo apt update**.
6. Lastly, install Docker by giving this command:
   Installing Docker |
   :----------------:|
   *sudo apt-get install -y docker-ce docker-ce-cli containerd.io*
7. To verify that the Docker is installed properly, you can give the docker—v command. If it’s installed properly, it will show you the version of the Docker.
   Checking if Docker is installed |
   :------------------------------:|
   *docker -v*|

# 4. Creating an image and running containers in Docker.
Before I show you how to create an image and run a container in Docker, we first need to create a simple HTML file.
1. Create a new directory.
   Creating a new directory |
   :------------------------:|
   *mkdir* <name of the directory> |
2. Create an HTML file in that directory.
   Creating HTML file |
   :-----------------:|
   *nano index.html*|
3. Inside the index.html put this:
    ```html           
    <html>            
    <head>            
    </head>           
    <body>            
    <h1> Hello World </h1> 
    </body>           
    </html>           
    ```
4. Save it, and then create a Dockerfile (A Dockerfile contains the commands or instructions used during the build to create the Docker image).
   Creating a Dockerfile |
   :-------------------:|
   *nano Dockerfile* |
        


   







