# Q4 Explanation

- I created a sample log file and opened it with a file descriptor using `exec 3<q4/app.log`. This demonstrated that Linux tracks open files through descriptors rather than by name alone.
- I inspected the current shell's open file descriptors with `lsof` and `/proc/$$/fd`. The output showed that the log file was associated with descriptor 3, while standard input, output, and error remained attached to the terminal.
- I redirected output and errors using `>`, `2>`, and `2>&1` into separate files. This showed how Linux separates standard output from standard error and how both can be combined into one stream.
- I checked resource limits with `ulimit -a`. The output confirmed that the shell allows a large number of open files, which is important for applications that handle many file descriptors.
