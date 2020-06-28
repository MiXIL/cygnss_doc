# Download CYGNSS data using Wget

## Table of Contents

* Downloading Wget (windows)
* Running the App
* Examples
* Notes

## Downloading Wget

### for windows
you can download it from [this link](https://eternallybored.org/misc/wget/). follow the steps in [this page](https://builtvisible.com/download-your-website-with-wget/) to install Wget in windows  

### for Linux

use the following command
```shell script
$ apt install wget
```

## Running the app

you can download any file using the following command either in cmd or bash
```shell script
$ wget url
```

you can get more info about the options using the following code
```shell script
$ wget --help
```
## Examples

The following example is for cygnss data and can be applied to other data from NASA PO.DAAC service.
you'll need a user name and a password which you can get from [The PO.DAAC Drive API Credentials
](https://podaac-tools.jpl.nasa.gov/drive/)

* Downloading a folder <br>

```shell script
wget --user=USER --password=PASS -r -nc -np -nH -l 0 -t 0 -A ".nc, .md5" "https://podaac-tools.jpl.nasa.gov/drive/files/allData/cygnss/L1/v2.1/2019/001/"
```

* Downloading days from 1-9 in year 2019 (cmd only) <br>

```shell script
FOR /L %%a IN (1,1,9) DO  wget --user=USER --password=PASS -r -nc -np -nH -l 0 -t 0 -A ".nc, .md5" "https://podaac-tools.jpl.nasa.gov/drive/files/allData/cygnss/L1/v2.1/2019/00%%a/"
```

* Downloading days from 1-294 in year 2019 (cmd only) <br>

```shell script
FOR /L %%a IN (1,1,9) DO  wget --user=USER --password=PASS -r -nc -np -nH -l 0 -t 0 -A ".nc, .md5" "https://podaac-tools.jpl.nasa.gov/drive/files/allData/cygnss/L1/v2.1/2019/00%%a/"

FOR /L %%a IN (10,1,99) DO  wget --user=USER --password=PASS -r -nc -np -nH -l 0 -t 0 -A ".nc, .md5" "https://podaac-tools.jpl.nasa.gov/drive/files/allData/cygnss/L1/v2.1/2019/0%%a/"

FOR /L %%a IN (100,1,294) DO  wget --user=USER --password=PASS -r -nc -np -nH -l 0 -t 0 -A ".nc, .md5" "https://podaac-tools.jpl.nasa.gov/drive/files/allData/cygnss/L1/v2.1/2019/%%a/"

```
<br>

Note: you can put those command in ``.cmd`` file and then you can run them by a click. you need to replace ``USER`` and ``PASS`` by yours from [PO.DAAC Drive API Credentials](https://podaac-tools.jpl.nasa.gov/drive/).



## Notes
* Sometimes Wget doesn't download all the data, so make sure to run the code multiple times.
* if your machine is out of space, Wget will not tell you that, it will simply doesn't download the data.
