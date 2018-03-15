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
    $ mv <old_name> <new_name>
    ```

* Renames multiple files

    ```
    $ rename 's/<old_keyword>/<new_keyword>/' <files>
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
