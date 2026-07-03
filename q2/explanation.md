# Q2 Explanation

- I created the project workspace and its subfolders using `mkdir -p` so that the structure would be ready for project files and documentation.
- I used `chmod` to change the directory permissions from broad access to a more secure form. The directories were set to `750`, and the files were set to `640`, which limits access to the owner and the owner's group.
- I checked the ownership and confirmed that everything belonged to the `codespace` user and group. The ownership remained unchanged because no `chown` command was needed.
- I used `umask` to confirm the default permission mask. The value `0022` reduced the permissiveness of new files and directories, which is a standard secure default.
- These permissions protect project data by preventing other users from reading or altering important files unless they specifically belong to the owner or group.
