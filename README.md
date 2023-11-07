# Repair Kindle code 2 

This is a script written in bash to repair Kindle error code 2, when Kindle shows "Your Kindle needs repairing. [...] Repair code: 2".  

### Usage :

Boot any linux distro (even from USB flash drive), open Terminal aplication and change to root user: 
```sh
$ su
```
Type root password, download script:

```sh
$ git clone https://github.com/lavix5/repair-kindle-code-2 && cd repair-kindle-code-2
```
Make it executable:
```sh
$ chmod +x ./kindle_repair.sh
```
Run script:
```sh
$ ./kindle_repair.sh 
```
Connect your Kindle to computer and force it to restart by pressing power button until it restarts. After script executes succesfully, restart your Kindle again. It should perform factory reset and boot up as a fresh device.
