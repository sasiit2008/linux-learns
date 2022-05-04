#### user management 
---

_what is user management?_

User Administration is the process of managing different user accounts and their respective permissions in an operating system.In Linux or Unix-based 
operating systems, we can create different user accounts, sort them into groups, change their set of permissions or delete them. The terminal commands 
for each of the above-stated actions are discussed below.

**Requirements**


|operating system | username | groupname |
|---|---|---|
|Ubuntu| dodo | lucas |

_**group creation details**_

```bash
# Create group 
sudo groupadd lucas
```
```bash
# One group into one user
sudo usermod -a -G lucas dodo 
```

```bash
# Muliple group in one user
usermod -a -G group1,group2,group3 dodo
```

```bash
# Remove a user from group
sudo gpasswd -d  dodo lucas
```

```bash
# User information
sudo usermod -c "This is dodo user" dodo
```

```bash
# Add the users into docker group
sudo usermod -aG docker ubuntu4
```

```bash
# List out the created group
cat /etc/group
```

```bash
# set a password in group user
sudo gpasswd groupname
```


## User Creation Details:

```bash
# create the user
sudo useradd username

# Login to the user
su username
   (or)
ssh username@ip_address
   (or)
ssh username@localhost

# Delete the user
sudo userdel username

# set a password in user
sudo passwd username

# List out the created users
cat /etc/passwd

```
#### Give the Permission - File to Group
```bash
# Create a file 
touch filename

# Ggive the permission - group to file
chgrp groupname filename

# To give the read, write, execute permission
chmod g+rwx filename

# view the file content in the user
cat filename
```
#### Output 
![image](https://user-images.githubusercontent.com/91359308/166628994-2dc3f3f6-87f2-4c7a-a8e0-cc3f557c8a92.png)
![image](https://user-images.githubusercontent.com/91359308/166631218-3d6ef51f-5fc9-447e-bf2c-d9d09dd5ec10.png)

