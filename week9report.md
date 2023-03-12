# Lab Report 5
## `find` Command-line Options

(current directory is `~/Documents/Github/docsearch/written_2`)


**-depth**
*Source: found using `man find`*

```
find non-fiction -depth 2
non-fiction/OUP/Berk
non-fiction/OUP/Abernathy
non-fiction/OUP/Rybczynski
non-fiction/OUP/Kauffman
non-fiction/OUP/Fletcher
non-fiction/OUP/Castro
```
This command allows us to see the contents that are a depth of two within the `non-fiction` path, which, in this case, is useful for easily seeing the directories, or authors, that the path has.


```
$ find non-fiction -depth 3
non-fiction/OUP/Berk/ch2.txt
non-fiction/OUP/Berk/ch1.txt
non-fiction/OUP/Berk/CH4.txt
non-fiction/OUP/Berk/ch7.txt
non-fiction/OUP/Abernathy/ch2.txt
non-fiction/OUP/Abernathy/ch3.txt
non-fiction/OUP/Abernathy/ch1.txt
non-fiction/OUP/Abernathy/ch7.txt
non-fiction/OUP/Abernathy/ch6.txt
non-fiction/OUP/Abernathy/ch8.txt
non-fiction/OUP/Abernathy/ch9.txt
non-fiction/OUP/Abernathy/ch15.txt
non-fiction/OUP/Abernathy/ch14.txt
non-fiction/OUP/Rybczynski/ch2.txt
non-fiction/OUP/Rybczynski/ch3.txt
non-fiction/OUP/Rybczynski/ch1.txt
non-fiction/OUP/Kauffman/ch3.txt
non-fiction/OUP/Kauffman/ch1.txt
non-fiction/OUP/Kauffman/ch4.txt
non-fiction/OUP/Kauffman/ch5.txt
non-fiction/OUP/Kauffman/ch7.txt
non-fiction/OUP/Kauffman/ch6.txt
non-fiction/OUP/Kauffman/ch8.txt
non-fiction/OUP/Kauffman/ch9.txt
non-fiction/OUP/Kauffman/ch10.txt
non-fiction/OUP/Fletcher/ch2.txt
non-fiction/OUP/Fletcher/ch1.txt
non-fiction/OUP/Fletcher/ch5.txt
non-fiction/OUP/Fletcher/ch6.txt
non-fiction/OUP/Fletcher/ch9.txt
non-fiction/OUP/Fletcher/ch10.txt
non-fiction/OUP/Castro/chR.txt
non-fiction/OUP/Castro/chP.txt
non-fiction/OUP/Castro/chQ.txt
non-fiction/OUP/Castro/chB.txt
non-fiction/OUP/Castro/chC.txt
non-fiction/OUP/Castro/chA.txt
non-fiction/OUP/Castro/chV.txt
non-fiction/OUP/Castro/chW.txt
non-fiction/OUP/Castro/chM.txt
non-fiction/OUP/Castro/chZ.txt
non-fiction/OUP/Castro/chL.txt
non-fiction/OUP/Castro/chN.txt
non-fiction/OUP/Castro/chY.txt
non-fiction/OUP/Castro/chO.txt
```
Similarly, this command lets us see the contents that are a depth of three within `non-fiction`, thus showing all of the files that exist in it. The `-depth` option is helpful because we can easily see the different files and directories that exist at a certain point past the command's starting point.


**-empty**
*Source: found using `man find`*

```
$ find travel_guides -empty
```
This command checks for empty files and directories within `travel_guides`, but since everything in it contains data, it has no result to show. It's helpful to double check that no unnecessary files or directories are included within the given path.


```
$ find non-fiction/OUP/Kauffman -empty
```
Similarly, this command checks for something empty in `non-fiction/OUP/Kauffman`, finding nothing again because all of the files within `Kauffman/` have contents. The command is helpful to easily scan for unused files and directories and make changes accordingly.


**-name**
*Source: found using `man find`*
```
$ find travel_guides/berlitz2/ -name "*WhatToDo.txt"
travel_guides/berlitz2//Amsterdam-WhatToDo.txt
travel_guides/berlitz2//CostaBlanca-WhatToDo.txt
travel_guides/berlitz2//Poland-WhatToDo.txt
travel_guides/berlitz2//Cuba-WhatToDo.txt
travel_guides/berlitz2//Cancun-WhatToDo.txt
travel_guides/berlitz2//Berlin-WhatToDo.txt
travel_guides/berlitz2//Bermuda-WhatToDo.txt
travel_guides/berlitz2//Budapest-WhatToDo.txt
travel_guides/berlitz2//PuertoRico-WhatToDo.txt
travel_guides/berlitz2//Vallarta-WhatToDo.txt
travel_guides/berlitz2//Bali-WhatToDo.txt
travel_guides/berlitz2//Portugal-WhatToDo.txt
travel_guides/berlitz2//Bahamas-WhatToDo.txt
travel_guides/berlitz2//Barcelona-WhatToDo.txt
travel_guides/berlitz2//Algarve-WhatToDo.txt
travel_guides/berlitz2//Costa-WhatToDo.txt
travel_guides/berlitz2//Crete-WhatToDo.txt
travel_guides/berlitz2//CanaryIslands-WhatToDo.txt
travel_guides/berlitz2//California-WhatToDo.txt
travel_guides/berlitz2//China-WhatToDo.txt
travel_guides/berlitz2//Athens-WhatToDo.txt
travel_guides/berlitz2//Nepal-WhatToDo.txt
travel_guides/berlitz2//Paris-WhatToDo.txt
travel_guides/berlitz2//Beijing-WhatToDo.txt
```
This command finds files in `travel_guides/berlitz2/` whose names end with the pattern `WhatToDo.txt`. It's a helpful way to find a more specific set of files or directories.

```
$ find non-fiction/ -name "ch1*.txt"
non-fiction//OUP/Berk/ch1.txt
non-fiction//OUP/Abernathy/ch1.txt
non-fiction//OUP/Abernathy/ch15.txt
non-fiction//OUP/Abernathy/ch14.txt
non-fiction//OUP/Rybczynski/ch1.txt
non-fiction//OUP/Kauffman/ch1.txt
non-fiction//OUP/Kauffman/ch10.txt
non-fiction//OUP/Fletcher/ch1.txt
non-fiction//OUP/Fletcher/ch10.txt
```
This command finds files somewhere in the `non-fiction/` directory whose names match the pattern `ch1*.txt`, which is helpful because we don't have to specify the whole path or path structure to find files with a specific naming pattern.


**-type t**
*Source: found using `man find`*

```
$ find travel_guides -type d
travel_guides
travel_guides/berlitz1
travel_guides/berlitz2
```
This command finds contents within `travel_guides` that are of the directory type, which is helpful when we want to see only a certain type of files, especially when they are mixed in with other types.

```
$ find non-fiction/OUP/Abernathy -type f
non-fiction/OUP/Abernathy/ch2.txt
non-fiction/OUP/Abernathy/ch3.txt
non-fiction/OUP/Abernathy/ch1.txt
non-fiction/OUP/Abernathy/ch7.txt
non-fiction/OUP/Abernathy/ch6.txt
non-fiction/OUP/Abernathy/ch8.txt
non-fiction/OUP/Abernathy/ch9.txt
non-fiction/OUP/Abernathy/ch15.txt
non-fiction/OUP/Abernathy/ch14.txt
```
This command finds contents of `non-fiction/OUP/Abernathy` of the regular file type, thus letting us clearly see only the files within `Abernathy`, not also directories or other types.
