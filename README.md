
# Basic Linux Operations

## Allowing Users to Connect via SSH

To allow specific users to connect to your SSH server using the "AllowUsers" directive in the **sshd_config** file, follow these steps:

1. Open the sshd_config file. This file is usually located in the "/etc/ssh/" directory. You can use any text editor to open the file.
    ```powershell
    vi /etc/ssh/sshd_config
    ```
2. Search for the **"AllowUsers"** directive in the file. If the directive is commented out with a "#" at the beginning of the line, remove the "#" to uncomment it
    To find a character string, type **/** followed by the string you want to search for, and then press **Return**. 
    vi positions the cursor at the next occurrence of the string. For example, to find the string “meta,” type /meta followed by Return.    

3. Add the usernames of the users you want to allow separated by spaces after the "AllowUsers" directive. For example, if you want to allow users "user1" and "user2" to connect to the server, you should add the following line:
     ```powershell
        AllowUsers user1 user2
        ```
4. Save the changes to the sshd_config file and exit the text editor.
5. Restart the SSH service to apply the changes. You can use the following command to restart the SSH service | comando | accion | servicio
    ```powershell
    
        sudo systemctl restart ssh
        ```

## Modes & Controls

| Command             | Description                                 |
| ------------------- | ------------------------------------------- |
| vi *filename*       | Edit *filename*                             |
| vi -r *filename*    | Edit last version of *filename* after crash |
| vi + n *filename*   | Edit *filename* at end of file              |
| vi + *filename*     | Edit *filename* at end of file              |
| vi +/str *filename* | Edit *filename* at first occurance of str   |



