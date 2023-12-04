#  Linux
**update local package database**
```
sudo apt update
sudo apt-get update
```
**install new versions of available packages**
```
sudo apt upgrade
sudo apt-get upgrade
```


**print shell name**
```
echo $SHELL
```

### deb package install
```
dpkg -i //install package
dpkg -r package_name //remove package
dpkg -l //list all installed packages.
dpkg -L package_name //Lists the files by specific package
```


### openssh
```
sudo apt update
sudo apt install openssh-server
sudo service ssh start
sudo systemctl status ssh
sudo systemctl start ssh
sudo systemctl enable ssh
```
**ssh connection** 
`ssh username@pc_ip`

**Find file or directory**
```
find search_path -name search_text*
find search_path -type d -name search_directory_name // d for find directory
find / -size +20G
```

**Make tar file**
```
tar -cvf new_file_name.tar source_directory
```

### File copy and Synchronization
- **Securly copy from base mechine to server mechine** 
```
scp -P port_number tar_file username@host_ip:/destination_path
```
- **Securly copy from base mechine to windows mechine** 
```
scp -r source_file_or_dir username@ip:"E:\\destination_direcory"
```

- **Securly copy from server mechine to base mechine**
```
scp -P port_number username@host_ip:/source_file_path destination_path
```
- **Synchronize file and directories between systems.**
```
rsync -avz source_directory username@host_ip:destination_directory
```

```
df // display information about disk space
```

```
sudo apt install net-tools
```