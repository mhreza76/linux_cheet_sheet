**show existing user informations**
```
cat /etc/passwd
```
**show groups**
```
cat /etc/group
```

**create user**
```
sudo adduser new_user_name // higher level utility
sudo adduser --no-create-home new_user_name // create user without home
sudo useradd new_user_name // lower leve utility
```


**delete user**
```
sudo deluser user_name
```
**delete user and remove user home/profile**
```
sudo deluser --remove-home user_name
sudo deluser -r user_name
```
**switch user**
```
su username	\\ stwich user
su - username \\ switch user with target user environment  
```

**assign group to a user**
- **a** for Add the user to the specified groups without removing them from other groups.
- **G**  Specify the groups to which the user should belong..
```
sudo usermod -aG group_name user_name
```
- **anotherway**
add user to the group in `/etc/group`

**change username**
`sudo usermod -l new_user_name old_user_name`
**change user home directory**
`sudo usermod -d /new/home/directory username`
**change user full name**
`sudo usermod -c "user full name" user_name`
**Set expire date for a user account**
`sudo usermod --expiredate 2023-07-22 user_name`
**master command for create user using low level utility**
```
useradd -g group_name -s /bin/bash -c "user full name" -m -d /user/home/directory username
```



### Password
**lock user**
`sudo passwd -l username` // this user will not be able to authenticate using password
**unlock user**
`sudo passwd -u username`
**set password / change password**
`sudo passwd username`
**Force user to set password in next login**
`sudo chage -d 0 user_name`

**system loging history**
```
lastlog
last user_name
```