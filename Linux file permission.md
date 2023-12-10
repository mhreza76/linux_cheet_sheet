**Permission Groups**
```
u - owner
g - group
o - other
a - all(u, g, o)
```

**Permission types**
➔ **read** – The Read permission refers to a user’s capability to read the contents
of the file.
➔ **write** – The Write permissions refer to a user’s capability to write or modify a
file or directory.
➔ **execute** – The Execute permission affects a user’s capability to execute a file
or view the contents of a directory
```
r = 4
w = 2
x = 1
```



![linux-permission-details.png](../_resources/linux-permission-details.png)



![linux-permission.png](../_resources/linux-permission.png)


- Default permission for directory created by **root**
`755`
-  Default permission for file created by **root**
`644`
- Default permission for directory created by **user**
`775`
-  Default permission for file created by **user**
`664`


**Soft Link**
```
sudo ln -s source_absolute_path destination
```

**Add permissions**
```
chmod -R u+rw file_or_directory
chmod -R g+rw file_or_directory
chmod -R o+rw file_or_directory
chmod -R a+rw file_or_directory
chmod -R 644 file_or_directory
```

**Remove permissions**
```
chmod -R u-rw file_or_directory
chmod -R g-rw file_or_directory
chmod -R o+rw file_or_directory
chmod -R a-rw file_or_directory
```

**Change Owner of a File/ Directory**
```
chown -R owner_name file_or_directory
chown owner_name file_or_directory  // without recursive
chown -R owner_name:group_name file_or_directory
```
**Change Group of a File/ Directory**
```
chgrp -R group_name file_or_directory
chgrp group_name file_or_directory // without recursive
```
