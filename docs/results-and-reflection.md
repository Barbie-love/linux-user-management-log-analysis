# Results and Reflection

## 1. What does grep do?

The `grep` command is used to search for specific words or patterns in a file. In this practical, I used grep to find all log entries containing `ERROR` and to extract lines mentioning `root` or `user01`.

## 2. What does chown do?

The `chown` command is used to change the ownership of files and directories in Linux. I used it to change the owner of `confidential.txt` from `forensic01` to `root`.

## 3. What does usermod do?

The `usermod` command is used to modify existing user accounts in Linux. I used it to add `forensic01` and `guest1` to the sudo group, giving them administrative privileges.

## 4. What did you learn from trying to access confidential.txt after changing ownership?

After changing the ownership of `confidential.txt` to root, I tried to read the file while logged in as `forensic01`. The terminal displayed a "Permission denied" message.

This happened because the file permissions were set to 600, meaning only the file owner had read and write access. Since root was now the owner, `forensic01` could no longer access the file.

## 5. Practical Completion Notes

- **Operating System:** Kali Linux 2026.2
- **Virtualization Platform:** Oracle VirtualBox
- **Activity:** Linux Task 03 – User Management, Log Analysis and Permissions
- **Status:** Completed

## 6. Conclusion

This practical helped me understand Linux user management, file permissions, ownership, and log analysis. I gained practical experience using commands such as grep, chmod, chown, and usermod. I also learned how Linux controls access to files and directories through ownership and permissions.