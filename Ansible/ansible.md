## shell disadvantages
  1. **No idempotency**
  2. **No error handling**
  3. **Shell is imperative, commands should be in order**
  4. **can't handle at a scale**
  5. **Homogenous -> works only for specific distro**
  6. **can't store secrets securely**

  ## Configuration
 - **Plain server -> ready to host application**
     - **Installing programming language**
     - **Creating system user**
     - **Creating app directory**
     - **Downloading code**
     - **Unzipping code**
     - **Installing dependencies**
     - **Creating systemctl service files**
     - **Loading data if necessary**
     - **Starting the server**

**CRUD**
- **Reading the configuration -> what is there inside server**
- **updating the configuration -> update the script and run it**
- **Delete the configuration -> write the script and run it**
 
 ![Ansible Logo](./ansible.svg)

# DTO --> Data Tranfor Objects
- [] -- **List**
- {} --**map/objects**
- **ansible everything is module or collection**
- **Inventory** --> machines ansible is tracking