# Process Monitoring

## Tools

### Ps (Process Status)

(Cheatsheet)[<https://www.sysadmin.md/ps-cheatsheet.html>]

The ps utility displays a header line, followed by lines containing information about all of your processes that have controlling terminals.

```sh
# Show all proceses with MEM and CPU use
ps aux # Main command to commit to memory

# Show information for single process
ps -p pid
ps uax | grep process_name
```

### Top (UNIX Process Inspector)

(Cheatsheet)[<https://gist.github.com/ericandrewlewis/4983670c508b2f6b181703df43438c37>]

The top program periodically displays a sorted list of system processes. The default sorting key is pid, but other keys can be used instead. Various output options are available.

```sh
# Display Linux processes
top

# While in top
q # quit/exit
h # show help menu
```

### Htop

(Cheatsheet)[<https://www.maketecheasier.com/power-user-guide-htop/>]

htop is a cross-platform ncurses-based process. It is similar to top, but allows you to scroll vertically and horizontally, and interact using a pointing device (mouse). You can observe all processes running on the system, along with their command line arguments, as well as view them in a tree format, select multiple processes and act on them all at once.

```sh
# Install
sudo apt-get install htop

```

### atop

(Command Guide)[<https://www.digitalocean.com/community/tutorials/atop-command-in-linux>]

An interactive monitor to view the load on a Linux system. It shows the occupation of the most critical hardware resources (from a performance point of view) on system level, i.e. cpu, memory, disk and network.

### lsof (LiSt Open Files)

(Cheatsheet)[<https://neverendingsecurity.wordpress.com/2015/04/13/lsof-commands-cheatsheet/>]

Lsof lists on its standard output file information about files opened by processes.
