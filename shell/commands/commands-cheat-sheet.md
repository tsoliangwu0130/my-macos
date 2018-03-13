## Commands Cheat Sheet

### Rename file(s)

* Rename file

    ```
    $ mv <old_name> <new_name>
    ```

* Renames multiple files

    ```
    $ rename 's/<old_keyword>/<new_keyword>/' <files>
    ```

Note: `rename` could be installed via [Homebrew](https://brew.sh/)

### Secure copy

Copy files between hosts using Secure Copy Protocol over SSH.

* Copy files over SSH:

    ```
    $ scp <source> <destination>
    ```

* Recursively copy the contents of a directory over SSH:

    ```
    $ scp -r <source> <destination>
    ```
