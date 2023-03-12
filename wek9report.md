# Lab Report 5
## `find` Command-line Options

(current directory is `~/Documents/Github/docsearch/written_2`)


**-type t**
*Source: found using `man find`*
```
$ find travel_guides -type d
travel_guides
travel_guides/berlitz1
travel_guides/berlitz2
```
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

**-empty**
*Source: found using `man find`*
```
$ find travel_guides -empty
```

```
$ find non-fiction/OUP/Kauffman -empty
```

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

**-depth**
*Source: found using `man find`*
```
$ find non-fiction -depth 1
non-fiction/OUP
```

```
find non-fiction -depth 2
non-fiction/OUP/Berk
non-fiction/OUP/Abernathy
non-fiction/OUP/Rybczynski
non-fiction/OUP/Kauffman
non-fiction/OUP/Fletcher
non-fiction/OUP/Castro
```
