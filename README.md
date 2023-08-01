# oneapi-devsummit-sea-2023
This repository hosts the contents of the AI handson workshop, oneAPI Devsummit South East Asia 2023

## Pre-requisites
1. You have registered and can login to the [Intel Developer Cloud](https://www.intel.com/content/www/us/en/developer/tools/devcloud/services.html). Yet to register on IDC? This [guide](https://github.com/bjodom/idc#account-registration) helps you get started
2. Your laptop has a basic ssh client installed. Most Linux distros comes pre-installed with ssh client. If you are on Microsoft Windows, open Command Prompt and verify that the commands 'ssh' and 'ssh-keygen' works. 

## Getting started with IDC **wip**
<list the basic steps getting started with screen grabs .. login to IDC, verify there are no running instances, post certificate on profile, launch instance on schedule access, verify access using command ssh user@idcbetabatch.eglb.intel.com>
Once registered on IDC follow the following steps to access the IDC "Scheduled access" nodes.<br>
1. Visit cloud.intel.com and login
2. 

## Getting started on AI workshop **wip**
<clone repo, run prepare_env.sh, note jupyter ip:port, open tunnel, access in local browser, rest of the instructions are on the ipynb notebook>
1. SSH into idc head node. <br>
Note: For the below command, replace 'user' with your actual username <br>
   ```
   ssh username@idcbetabatch.eglb.intel.com
   ```
   ==include success screenshot==
2. Request for compute node <br>
   ```
   srun -p pvc-shared --pty /bin/bash
   ```
   ==include success screenshot==
3. Clone this repository <br>
   ```
   git clone https://github.com/vishnumadhu365/oneapi-devsummit-sea-2023.git
   ```
   ==include success screenshot==
4. Prepare environment
   ```
   source prepare_env.sh
   ```
   ==include success screenshot==
5. Note down ip-address and port-number of jupyter server. Copy the url starting with localhost:xxxx <br>
   ==include success screenshot==
6. In a new terminal create an ssh tunnel to the jupyter server<br>
    ```
   ssh -L port-number:ip-address:portnumber username@idcbetabatch.eglb.intel.com
   ```
   sample ssh command --> ssh -L 8888:10.0.0.8:8888 u107456<span>@</span>idcbetabatch.eglb.intel.com
7. Open browser on laptop and hit the url copied earlier (starting with localhost:xxxx)

## Help improve IDC **wip**

## Common issues **wip**
1. I was running the ipynb notebook, then the terminal exited abrupty. How do I resume my work ?
<include answer>
2. GPU Notebook has been running for more than 10 mins, seems its stuck, what to do ?
<issue with multiple sessions on same gpu, restart kernel and try if there are other less utilized gpus to run the notebook>
3. Facing random errors ?
<restart kernel>
4. 
