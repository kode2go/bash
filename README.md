# Learning Bash

## Windows

### Basics 1

1. Install Git Bash

2. Objectives:
- learn about moving to specific directory, up a level and down a level 
- list all files and folders in a directory
- get current working directory
- copy a file or folder
- move a file or folder
- remove a file or folder
- create/edit a file

Using the following commands:
- `cd`, `ls`, `pwd`, `cp`, `mv`, `rm`, `nano`

Move inside a directory (one level down)
`cd foldername/`:

Move outside a directory (one level up)
`cd ..`:

Move oustide a directory (two levels up)
`cd ../..`:

`mv`:
- has two functions: to move files or folders or to rename them

### Basics 2

#### Flags:

`ls -l`:

`rm -r`:

`cp -R`: copy directories

`cat -n`

More commands:

`echo`

`--help`

`man`

`history`

`sudo`:

`~`:

`mkdir`

`touch`

`less`

`top`

`kill`:

`clear`

### Basics 3

`find`:

`grep`: 

`curl`:

`scp`:

`which`:

`head`:

`tail`:

`chmod`:

`exit`:

ctrl + c

`alias c = “clear”`

### Basics 4:

`>`

`|`


### Basics 5

Wildcards: 
* is a wildcard, which represents zero or more other characters
? is also a wildcard, but it represents exactly one character.

### Exercise 1

Create the following files and folder structure:

```
.
├── 2015-10-23-calibration.txt
├── 2015-10-23-dataset1.txt
├── 2015-10-23-dataset2.txt
├── 2015-10-23-dataset_overview.txt
├── 2015-10-26-calibration.txt
├── 2015-10-26-dataset1.txt
├── 2015-10-26-dataset2.txt
├── 2015-10-26-dataset_overview.txt
├── 2015-11-23-calibration.txt
├── 2015-11-23-dataset1.txt
├── 2015-11-23-dataset2.txt
├── 2015-11-23-dataset_overview.txt
├── backup
│   ├── calibration
│   └── datasets
└── send_to_bob
    ├── all_datasets_created_on_a_23rd
    └── all_november_files
```

Folders:

```
mkdir -p backup/calibration
mkdir -p backup/datasets
mkdir -p send_to_bob/all_datasets_created_on_a_23rd
mkdir -p send_to_bob/all_november_files
```

Note that `-p` creates parent directory

Files:

```
touch 2015-10-23-{calibration,dataset{1,2},dataset_overview}.txt 
touch 2015-10-26-{calibration,dataset{1,2},dataset_overview}.txt 
touch 2015-11-23-{calibration,dataset{1,2},dataset_overview}.txt

```

View with `ls -Rl`

Copy all dataset files to backup/datasets:
`cp *dataset* backup/datasets`

Copy all calibration to backup/calibration:
Mistake copy to datasets:
`cp *calibration* backup/datasets`
`cp *calibration* backup/calibration`

Cant us `rm` too easily to delete, rather use find. First find the files:

```

find . -name "*calibration*"
find . -type f -name "*calibration*"
find backup/datasets -type f -name "*calibration*" 
find backup/datasets -type f -name "*calibration*" -delete
find backup/datasets -type f -name "*calibration*" 

```

...go to the wiki!
