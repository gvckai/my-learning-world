## User management
- Narmal user indicates -> **$**
- Root User indicates -> **#**
- /root -> **roor user home folder**
## Group - > A list of humans, A group will have more users
 - Authentication ( Prove your self)
 - Authorization(Do you have access to this resource)

# Authorization

| Role | Permissions |
|---|---|
|Trainee|Read only access|
|Junior|Write access|
|Senior|Read, Write and Update access|
|TL|Read, Write, Update and Delete access|

## A group will have role -> Permissions

| User | Role | Group| Permissions|
|---|---|---|---|
|ramesh|Trainee|devops|Read only access|
|suresh|Junior|devops|Write access|
|gamesh|Senior|devops|Read, Write and Update access|
|siva|TL|devops|Read, Write, Update and Delete access|

- **Create user and add him to devops group.**
  - **useradd username**
    -   when we create user, linux will create a group also on the same user name
        A user in linux will have 1 primary group and 0 or more secondary groups
u       serid 0 means, it is root user
  ```
  useradd ramesh
  ```

-  /etc/passwd -> passwd file contains user infermation
- /etc/group -> group file contains group information
- useradd username  -> It is used to create user
- usermod -g groupname username --> it is used to add primary group to ramesh|
- **Create User**
```useradd ramesh
```
**Create primary group**

|usermod -aG <secondary group> <user name>| it is used to add secondary group ramesh |
|passwd ramesh| set passwd to user|
