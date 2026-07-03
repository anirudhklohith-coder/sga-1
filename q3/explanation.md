# Q3 Explanation

- I created a regular file, a hard link, and a symbolic link to compare how Linux handles each type of link.
- I used `ls -li` and `stat` to inspect inode numbers and link counts. The hard link shared the same inode as the original file, while the symbolic link had a different inode.
- I deleted the original file and observed the behavior. The hard link still displayed the file contents, but the symbolic link stopped working because its target path no longer existed.
- This experiment shows that hard links are direct aliases to the same inode, whereas symbolic links are pointer-like entries that depend on a target path.
