
# Basic Linux Vi Commands

## Modes & Controls

| Command             | Description                                 |
| ------------------- | ------------------------------------------- |
| vi *filename*       | Edit *filename*                             |
| vi -r *filename*    | Edit last version of *filename* after crash |
| vi + n *filename*   | Edit *filename* at end of file              |
| vi + *filename*     | Edit *filename* at end of file              |
| vi +/str *filename* | Edit *filename* at first occurance of str   |

## sshd_config
cat /etc/ssh/sshd_config
To find a character string, type / followed by the string you want to search for, and then press Return. 
vi positions the cursor at the next occurrence of the string. For example, to find the string “meta,” type /meta followed by Return.
