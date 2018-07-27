## Commands Cheat Sheet

### `/bin`, `/sbin`, `/usr/bin`, `/usr/local/bin`,`/usr/local/sbin/`?

* `/bin`: system management programs need before `/usr` is mounted
* `/sbin`: same as `/bin`. The main difference is the utilities in this directory is mainly and only for admin
* `/usr/bin`: distribution-managed normal user programs
* `/usr/local/bin`: normal user programs not managed by the distribution package manager
* `/usr/local/sbin`: as `/usr/bin` to `usr/sbin`

### `sudo` vs. `su`

* `sudo`: Executes a single command as another user

  * Run command as the user:

    ```
    $ sudo -u <username> <command>
    ```

  * Repeat the last command as sudo:

    ```
    $ sudo !!
    ```
  * Launch the default shell with root privileges (user password required):

    ```
    $ sudo -i
    ```

  * Launch the default shell with another user privileges (user password required):

    ```
    $ sudo -u <username> -i
    ```

* `su`: Switch shell to another user

  * Switch to superuser without simulating a full login shell (admin password required):

    ```
    $ su
    ```

  * Switch to superuser and simulate a full login shell (admin password required):

    ```
    $ su -
    ```

  * Switch shell to another user (user password required):

    ```
    $ su <username>
    ```

### Rename File(s)

* Rename file

  ```
  $ mv <old name> <new name>
  ```

* Renames multiple files

  ```
  $ rename 's/<old keyword>/<new keyword>/' <files>
  ```

  **Note**: `rename` could be installed via [Homebrew](https://brew.sh/)

### Secure Copy

Copy files between hosts using Secure Copy Protocol over SSH.

* Copy files over SSH:

  ```
  $ scp <source> <destination>
  ```

* Recursively copy the contents of a directory over SSH:

  ```
  $ scp -r <source> <destination>
  ```

### Empty the Command Hash Table

* In Zsh:

  ```
  $ rehash
  ```

* In Bash:

  ```
  $ hash -r
  ```

### Disk Usage

* Estimate disk usage of all files and subdirectories under currently directory

  ```
  $ du -h *
  ```

### Information about Running Processes

* List all running processes

  ```
  $ ps aux
  ```

* Search for a process that matches a string

  ```
  $ ps aux | grep <string>
  ```

### Transfers Data from or to a Server

* Download the contents of an URL to a file

  ```
  $ curl <URL> -o <filename>
  ```

* Send a request with an extra header, using a custom HTTP method:

  ```
  $ curl -H <header> -X <HTTP method> <URL>
  ```

* Send data in JSON format, specifying the appropriate content-type header:

  ```
  $ curl -d '{"key": "value"}' -H 'Content-Type: application/json' <URL>
  ```

* Pass a user name and password for server authentication:

  ```
  $ curl -u <username>:<password> <URL>
  ```

* Pass client certificate and key for a resource, skipping certificate validation:

  ```
  $ curl --cert <cert.pem> --key <key.pem> --insecure <URL>
  ```

### Find files under the given directory tree recursively

* Find files by pattern

  ```
  $ find <path> -name <pattern>
  ```

* Find files by type

  ```
  $ find <path> -type <type>
  ```

  Possible file types:

  | Type | Description |
  | :--: | ----------- |
  | **b** | block special |
  | **c** | character special |
  | **d** | directory |
  | **f** | regular file |
  | **l** | symbolic link |
  | **p** | FIFO |
  | **s** | socket |

* Find files modified in the last certain days

  ```
  $ find <path> -mtime <days>
    ```

> read more: https://blog.gtwang.org/linux/unix-linux-find-command-examples/
