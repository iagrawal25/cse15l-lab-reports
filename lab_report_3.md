# Lab Report 3: Testing Commands
## Setting Up
- Today we will be testing out the _find_ command.
- First, we will clone the repository [click here](https://github.com/ucsd-cse15l-w23/skill-demo1-data) to work with different files.

```
git clone https://github.com/ucsd-cse15l-w23/skill-demo1-data
```

```
Cloning into 'skill-demo1-data'...
remote: Enumerating objects: 237, done.
remote: Counting objects: 100% (237/237), done.
remote: Compressing objects: 100% (235/235), done.
remote: Total 237 (delta 0), reused 237 (delta 0), pack-reused 0
Receiving objects: 100% (237/237), 3.25 MiB | 5.58 MiB/s, done.
```

- Now, we have the files that we need to work with.

## Command 1

We will use _find_ to search for particular directories or files. [(citation link)](https://www.redhat.com/sysadmin/linux-find-command)
```
find ./written_2 -name berlitz2
```
- This searches for the _berlitz2_ directory in the _written_2_ directory and returns its path.

- Output

```
./written_2/travel_guides/berlitz2
```

Another example of the same thing:
```
find ./written_2 -name  ch2.txt
```
- This searches for the _ch2.txt_ file in the _written_2_ directory and returns each file's path.

- Output

```
./written_2/non-fiction/OUP/Berk/ch2.txt
./written_2/non-fiction/OUP/Abernathy/ch2.txt
./written_2/non-fiction/OUP/Rybczynski/ch2.txt
./written_2/non-fiction/OUP/Fletcher/ch2.txt
```

## Command 2

_find_ can be used to find files of a particular extension that end with a particular name [(citation link)](https://www.redhat.com/sysadmin/linux-find-command). To do this, we write:
```
find ./written_2 -name *India.txt
```
- _./written_2_ makes sure to search for all directories and files inside written_2 and _*_ acts as a wildcard. We search for all files that end with India.txt

- Output

```
./written_2/travel_guides/berlitz1/HistoryIndia.txt
./written_2/travel_guides/berlitz1/WhereToIndia.txt
./written_2/travel_guides/berlitz1/WhatToIndia.txt
./written_2/travel_guides/berlitz1/IntroIndia.txt
```

Another example of the same thing:
```
find ./written_2 -name *History.txt
```
- This searches for all files that end with History.txt.

- Output

```
./written_2/travel_guides/berlitz2/Portugal-History.txt
./written_2/travel_guides/berlitz2/Costa-History.txt
./written_2/travel_guides/berlitz2/Barcelona-History.txt
./written_2/travel_guides/berlitz2/Berlin-History.txt
./written_2/travel_guides/berlitz2/Bali-History.txt
./written_2/travel_guides/berlitz2/Athens-History.txt
./written_2/travel_guides/berlitz2/California-History.txt
./written_2/travel_guides/berlitz2/Vallarta-History.txt
./written_2/travel_guides/berlitz2/Cancun-History.txt
./written_2/travel_guides/berlitz2/CostaBlanca-History.txt
./written_2/travel_guides/berlitz2/NewOrleans-History.txt
./written_2/travel_guides/berlitz2/PuertoRico-History.txt
./written_2/travel_guides/berlitz2/Nepal-History.txt
./written_2/travel_guides/berlitz2/China-History.txt
./written_2/travel_guides/berlitz2/Canada-History.txt
./written_2/travel_guides/berlitz2/Crete-History.txt
./written_2/travel_guides/berlitz2/Amsterdam-History.txt
./written_2/travel_guides/berlitz2/Beijing-History.txt
./written_2/travel_guides/berlitz2/CanaryIslands-History.txt
./written_2/travel_guides/berlitz2/Algarve-History.txt
```

## Command 3

Now, we will use _find_ to search for files in a directory [(citation link)](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/). Unlike _ls_ it allows you to filter out files based on its type.
```
find ~/skill-demo1-data -type d
```
- This searches for files of type 'd' which means directory.

- Output

```
/Users/ishikaagrawal/skill-demo1-data
/Users/ishikaagrawal/skill-demo1-data/.git
/Users/ishikaagrawal/skill-demo1-data/.git/objects
/Users/ishikaagrawal/skill-demo1-data/.git/objects/pack
/Users/ishikaagrawal/skill-demo1-data/.git/objects/info
/Users/ishikaagrawal/skill-demo1-data/.git/info
/Users/ishikaagrawal/skill-demo1-data/.git/logs
/Users/ishikaagrawal/skill-demo1-data/.git/logs/refs
/Users/ishikaagrawal/skill-demo1-data/.git/logs/refs/heads
/Users/ishikaagrawal/skill-demo1-data/.git/logs/refs/remotes
/Users/ishikaagrawal/skill-demo1-data/.git/logs/refs/remotes/origin
/Users/ishikaagrawal/skill-demo1-data/.git/hooks
/Users/ishikaagrawal/skill-demo1-data/.git/refs
/Users/ishikaagrawal/skill-demo1-data/.git/refs/heads
/Users/ishikaagrawal/skill-demo1-data/.git/refs/tags
/Users/ishikaagrawal/skill-demo1-data/.git/refs/remotes
/Users/ishikaagrawal/skill-demo1-data/.git/refs/remotes/origin
/Users/ishikaagrawal/skill-demo1-data/written_2
/Users/ishikaagrawal/skill-demo1-data/written_2/non-fiction
/Users/ishikaagrawal/skill-demo1-data/written_2/non-fiction/OUP
/Users/ishikaagrawal/skill-demo1-data/written_2/non-fiction/OUP/Berk
/Users/ishikaagrawal/skill-demo1-data/written_2/non-fiction/OUP/Abernathy
/Users/ishikaagrawal/skill-demo1-data/written_2/non-fiction/OUP/Rybczynski
/Users/ishikaagrawal/skill-demo1-data/written_2/non-fiction/OUP/Kauffman
/Users/ishikaagrawal/skill-demo1-data/written_2/non-fiction/OUP/Fletcher
/Users/ishikaagrawal/skill-demo1-data/written_2/non-fiction/OUP/Castro
/Users/ishikaagrawal/skill-demo1-data/written_2/travel_guides
/Users/ishikaagrawal/skill-demo1-data/written_2/travel_guides/berlitz1
/Users/ishikaagrawal/skill-demo1-data/written_2/travel_guides/berlitz2
```

Now, we will try looking for another file type.
```
find ~/skill-demo1-data -type b
```
- This searches for files of type 'b' which means block device file.
- However, there is no output since no such file type exists in out directory.


## Command 4

Now, we will use _find_ to search for files of a particular size [(citation link)] (https://www.geeksforgeeks.org/find-command-in-linux-with-examples/).
```
sudo find ./written_2 -size +20k -size -22k
```
- This searches for files that are between 20KB and 22KB.
- Imp: Sudo is used to grant permission.

- Output

```
./written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt
./written_2/travel_guides/berlitz1/WhatToDublin.txt
./written_2/travel_guides/berlitz1/WhatToIsrael.txt
./written_2/travel_guides/berlitz1/WhatToEdinburgh.txt
./written_2/travel_guides/berlitz1/HistoryEdinburgh.txt
./written_2/travel_guides/berlitz1/WhatToItaly.txt
./written_2/travel_guides/berlitz1/WhatToEgypt.txt
./written_2/travel_guides/berlitz2/Berlin-History.txt
./written_2/travel_guides/berlitz2/Athens-History.txt
./written_2/travel_guides/berlitz2/Bermuda-WhatToDo.txt
./written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt
./written_2/travel_guides/berlitz2/NewOrleans-History.txt
./written_2/travel_guides/berlitz2/Beijing-WhatToDo.txt
```

Instead of a range, files of a particular size can also be found
```
sudo find ./written_2 -size +100k
```
- This searches for files of 100KB.

- Output

```
./written_2/non-fiction/OUP/Berk/ch2.txt
./written_2/non-fiction/OUP/Berk/CH4.txt
./written_2/travel_guides/berlitz1/WhereToIndia.txt
./written_2/travel_guides/berlitz1/WhereToItaly.txt
./written_2/travel_guides/berlitz1/WhereToMalaysia.txt
./written_2/travel_guides/berlitz1/WhereToJapan.txt
./written_2/travel_guides/berlitz1/WhereToFrance.txt
./written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
./written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
./written_2/travel_guides/berlitz2/China-WhereToGo.txt
```
