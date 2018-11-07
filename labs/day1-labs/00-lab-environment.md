# Lab Environment

## Classroom Setting

These labs are can be used for delivery in both a classroom setting with an Azure Technical Specialist or self-guided on your own machine.

* For these specific labs, we are assuming you will be using your own Azure subscription, as a relatively small set of Azure resources are required.

* Setup Azure Cloud Shell: 

    1. Browse to http://portal.azure.com
    2. Click on the cloud shell icon to start your session.

        ![alt text](img/cloud-shell-start.png "Spektra ready")

    3. Select `Bash (Linux)`
    4. You will be prompted to setup storage for your cloud shell. Click `Show advanced settings`

        ![alt text](img/cloud-show-advanced.png "Spektra ready")

    6. Provide a unique value for Storage account name. This must be all lower case and no punctuation. Use "cloudshell" for File share name. See example below.

        ![alt text](img/cloud-storage-config.png "Spektra ready")

    7. Click `Create storage`

    > Note: You can also use the dedicated Azure Cloud Shell URL: http://shell.azure.com 


## Self-guided

It is possible to use your own machine outside of the classroom. You will need the following in order to complete these labs: 

* Azure subscription
* Linux, Mac, or Windows with Bash
* Docker
* Azure CLI
* Visual Studio Code
* Helm
* Kubernetes CLI (kubectl)
* GitHub account and git tools

### Instructions for Windows 7/10 to add required development tooling
1. From the Windows Command Prompt, install the Chocolatey Package Manager by running the following command:
```
 powershell.exe -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin" 
 ```
 2. From Powershell (all examples will use Powershell going forward), execute the following command to install the additional developer tooling and utilities
 ```
 cup git visualstudiocode azure-cli docker docker-for-windows kubernetes-cli -y
 ```
 3. When the package installation is complete, close Powershell session and use Desktop Icon to start Docker initialization.  You will be prompted to initially logout, just restart the VM.  Two restarts will be required to fully initialize the Hyper-V subsystem for Docker to operate.  Follow the prompts from Docker.  
 4. After the 2nd VM restart and successful Docker startup, open a Powershell session and execute the following command to verify Docker install
 ```
 docker run -it centos bash
 ```
 5. You should see something like the following (exit the container as shown)
 ```
Unable to find image 'centos:latest' locally
latest: Pulling from library/centos
469cfcc7a4b3: Pull complete
Digest: sha256:989b936d56b1ace20ddf855a301741e52abca38286382cba7f44443210e96d16
Status: Downloaded newer image for centos:latest
[root@e2584d2044c8 /]# exit
exit
```
