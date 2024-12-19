# **Fun with Linux for Cloud & DevOps Engineers**  

![Linux Banner](https://imgur.com/VpPW8PM.png)  

***New to Linux? This assignment covers all the essential Linux basics required for a DevOps engineer.***  

![Linux Skills](https://imgur.com/xedzuwy.png)  

---

## **Skills Required**  
To complete the assignment, you’ll need proficiency in:  
- Linux User Management  
- Permissions  
- Directory Structure  
- File Systems  
- File Management  

---

## **Pre-Requisites**  
- Create a Linux-based EC2 instance in AWS to perform the following tasks.  

---

## **Deployment Steps**  

### **1. Superuser Tasks**  
- Log in as `root` and perform:  
  1. **User Management:**  
     - Create users: `user1`, `user2`, `user3` with passwords.  
     - Create groups: `devops`, `aws`.  
     - Change primary group: Assign `devops` as the primary group for `user2` and `user3`.  
     - Add secondary group: Add `aws` as a secondary group for `user1`.  
  2. **Filesystem Structure:**  
     - Create the directories and files per the diagram.  
     - Assign ownership and permissions:  
       - Change group ownership of `/dir1`, `/dir7/dir10`, `/f2` to `devops`.  
       - Change ownership of `/dir1`, `/dir7/dir10`, `/f2` to `user1`.

### **2. User1 Tasks**  
- Log in as `user1` and perform:  
  - Create users: `user4`, `user5` with passwords.  
  - Create groups: `app`, `database`.  

### **3. User4 Tasks**  
- Log in as `user4` and perform:  
  - Create directories: `/dir6/dir4`.  
  - Create a file: `/f3`.  
  - File management:  
    - Move `/dir1/f1` to `/dir2/dir1/dir2`.  
    - Rename `/f2` to `/f4`.  

### **4. User2 and Other Users’ Tasks**  
**For `user2`:**  
- Create a file: `/dir1/f2`.  
- Directory operations: Delete `/dir6` and `/dir8`.  
- Modify files:  
  - Replace "DevOps" with "devops" in `/f3` using a single command.  
  - Use `vi` to copy line 1 and paste it 10 times in `/f3`.  
  - Search and replace "Engineer" with "engineer" in `/f3`.  
- Delete `/f3`.  

**For `user1`:**  
- Create a directory: `/home/user2/dir1`.  
- Create and move files:  
  - Use relative paths to create `/opt/dir14/dir10/f1` from `/dir2/dir1/dir2/dir10`.  
  - Move `/opt/dir14/dir10/f1` to the home directory of `user1`.  
- Recursive deletion: Delete `/dir4` and all contents under `/opt/dir14` in a single command.  
- Write to a file: Add the text *"Linux assessment for a DevOps Engineer!! Learn with Fun!!"* to `/f3`.  

---

### **5. Root User Tasks**  
- **File operations:**  
  - Search for files named `f3` and list all absolute paths.  
  - Count files in `/`.  
  - Print the last line of `/etc/passwd`.  

---

### **6. AWS EBS Setup**  
1. Create a 5 GB EBS volume in the same Availability Zone as your EC2 instance.  
2. Attach the volume to your instance.  

**For root user:**  
- Create a file system on the volume and mount it to `/data`.  
- Verify the mount using `df -h`.  
- Create a file `/data/f1`.  

---

### **7. Cleanup Steps**  
1. **Users and Groups Cleanup:**  
   - Delete users: `user1`, `user2`, `user3`, `user4`, `user5`.  
   - Remove groups: `app`, `aws`, `database`, `devops`.  
   - Delete all remaining home directories for the users.  
2. **File System Cleanup:**  
   - Unmount `/data`.  
   - Delete `/data` directory.  
3. **AWS Resource Cleanup:**  
   - Detach and delete the EBS volume.  
   - Terminate the EC2 instance.  

---

### **Conclusion**  
Practice the steps as often as needed for confidence!  
#### Authored by [Arunesh Dwivedi](https://github.com/AruneshDwivedi)  
