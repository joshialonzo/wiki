## Linux File System

### Notable File System Directories

* Common configuration files: `/etc`
* Common programms or commands: `/bin`, `/sbin`
* Shared libraries and modules: `/lib`
* Standard location for mounting other file systems: `/mnt`, `/media`
* Kernel and system information: `/dev`, `/proc`, and `/sys`

### Paths on Linux

* A path represents the location of a file or directory
* Paths use the slash character (`/`) as a separator between directory and file names
* Paths can be absolute or relative

### Absolute paths

* Begins from the root of the file system
* Defines an explicit location on the file system
* A slash at the beginning indicates an absolute path

```bash
/home/joshi
/home/joshi/Documents
```

### Relative paths

* Begin from the current working directory
* If the current working directory changes, what the path refers to changes
* The name `..` refers to the parent directory of the current working directory

|       Working directory | Relative Path  | Resulting Absolute Path |
|------------------------:|----------------|-------------------------|
| `/home/scott`           | `..`           | `/home`                 |
| `/home/scott/Documents` | `..`           | `/home/scott`           |
| `/home/scott/Pictures`  | `../Documents` | `/home/scott/Documents` |

### Tilde expansion

* The tilde character (`~`) refers to the current user's home directory
* My documents (and your documents) are at the path `~/Documents`
* The shell expands the character `~` to the path of the user's home directory

Examples:

* `~/Documents -> /home/scott/Documents`
* `~/Documents -> /home/your_user/Documents`

### Commands

Show all files, directories, and other objects in a directory:

```bash
ls
```

Set a colorful `ls`:

```bash
ls --color=always
```

List files and directories with details:

```bash
ls -l
```

Show all folders recursively:

```bash
ls -r Documents
```

Return to the previous directory

```bash
cd -
```