## shell disadvantages
  1. **No idempotency**
  2. **No error handling**
  3. **Shell is imperative, commands should be in order**
  4. **can't handle at a scale**
  5. **Homogenous -> works only for specific distro**
  6. **can't store secrets securely**

   ![Ansible Logo](./ansible.svg)

## #configuration
 - **plain server -> ready to host application**
     1. installing programming language
     2. creating system user
     3. creating app directory
     4. downloading code
     5. unzipping code
     6. installing dependencies
     7. creating systemctl service files
     8. loading data if necessary
     9. starting the server

# DTO --> Data Tranfor Objects
- [] -- **List**
- {} --**map/objects**
- **ansible everything is module or collection**
- **Inventory** --> machines ansible is tracking