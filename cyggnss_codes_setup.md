# CYGNSS codes setup

## Setting Enviroment Variables
```shell
export CYGNSS_L1_PATH = PATHNAME
export SRTM_PATH = PATHNAME
```
e.g ``export CYGNSS_L1_PATH = /mnt/d/cygnss_data/drive/files/allData/cygnss/L1/v2.1/``

## How to set Environment Variables
### Linux
write this in the bash  
```shell script
$ nano ~/.bashrc
```
then add this line with replacing ```PATHNAME``` with the dir of the L1 data folder  
```bash
export CYGNSS_L1_PATH = PATHNAME 
```

You can paste in nano by ``Shift+right mouse click`` or ``CTRL + Shift + V``  

For more info visit [this page](https://www.digitalocean.com/community/tutorials/how-to-read-and-set-environmental-and-shell-variables-on-a-linux-vps) 

To check if everything is working  
```shell script
$ source  ~/.bashrc  
$ echo $CYGNSS_L1_dir  
```

### Windows
in search look for "Edit environment variables for your account"
click **New...**  

A new window will open, enter the following:  
Variable name: ``CYGNSS_L1_PATH``  
Variable Value: ``PATHNAME``  
Then click OK  

The same thing can be done for ``SRTM_PATH``  
for more info check [this link](https://www.architectryan.com/2018/08/31/how-to-change-environment-variables-on-windows-10/) and [this link](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/setx)
## Calling environment variables in python
you can call and set environment variables in python. However, setting env var in python is temporary, it get removed as you close the session.  

```python 
import os  
os.environ["CYGNSS_L1_PATH"]
os.environ["SRTM_PATH"]
```
