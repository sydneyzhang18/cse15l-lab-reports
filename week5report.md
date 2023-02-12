# Lab Report 3
## `grep` Command-line Options

(current directory is `~/Documents/Github/docsearch/written_2`)

**-c (count)**
*Source: found using `man grep`*
```
$ grep -c "William" non-fiction/OUP/Abernathy/*.txt
non-fiction/OUP/Abernathy/ch1.txt:0
non-fiction/OUP/Abernathy/ch14.txt:0
non-fiction/OUP/Abernathy/ch15.txt:0
non-fiction/OUP/Abernathy/ch2.txt:0
non-fiction/OUP/Abernathy/ch3.txt:1
non-fiction/OUP/Abernathy/ch6.txt:1
non-fiction/OUP/Abernathy/ch7.txt:0
non-fiction/OUP/Abernathy/ch8.txt:0
non-fiction/OUP/Abernathy/ch9.txt:0
```
This command counts the occurrences of "William" in each of the .txt files in the `non-fiction/OUP/Abernathy/` directory. It's useful because it can easily tell us when there are multiple occurences of a string in each file, and it outputs a concise summary.

```
$ grep -c "Lucayans" */*/Bahamas*.txt
travel_guides/berlitz2/Bahamas-History.txt:2
travel_guides/berlitz2/Bahamas-Intro.txt:0
travel_guides/berlitz2/Bahamas-WhatToDo.txt:0
travel_guides/berlitz2/Bahamas-WhereToGo.txt:0
```
This command counts the occurrences of "Lucayans" in each of the .txt files in specified path whose file name begins with Bahamas. It's useful because it allows us to easily count string occurrences without having to scroll through blocks of text, like with using -r.


**-i (ignore case)** 
*Source: found using `man grep`*
```
$ grep -i "lacquerware" travel_guides/berlitz1/WhatToJapan.txt
        lacquerware, ceramics, or whatever around the country with you.
        antique furniture, ceramics, masks, lacquerware, and Buddhist
        Lacquerware. You are least likely to go wrong in terms of
        uniformly high quality if you’re in the market for lacquerware. Trays,
```
This command searches `travel_guides/berlitz1/WhatToJapan.txt` for case-insensitive occurrences of "lacquerware". It's useful because we might not always want to search for string case-sensitively.

```
$ grep -l -i "gold" */*/California*.txt
travel_guides/berlitz2/California-History.txt
travel_guides/berlitz2/California-WhatToDo.txt
travel_guides/berlitz2/California-WhereToGo.txt
```
This command combines the -l option (see below) with the -i option to search for case-insensitive occurences of the string "gold" in the specified path and output only the file names in which it is found. It's useful because it allows us to combine grep options so that we can output only file names and search without case sensitivity.


**-l (files with matches)**
*Source: found using `man grep` and while collaborating during Lab 4*
```
$ grep -l "Parisien" travel_guides/berlitz2/*.txt
travel_guides/berlitz2/Cuba-WhatToDo.txt
```
This command searches all of the .txt files in the `travel_guides/berlitz2/` subdirectory for the string "Parisien" and outputs the name of the file in which it occurs. This is helpful because it provides an easy-to-read search output that consists only of file names.

```
$ grep -l "Greece" */*/*.txt
travel_guides/berlitz1/HistoryGreek.txt
travel_guides/berlitz1/HistoryIstanbul.txt
travel_guides/berlitz1/IntroGreek.txt
travel_guides/berlitz1/WhatToGreek.txt
travel_guides/berlitz1/WhereToEgypt.txt
travel_guides/berlitz1/WhereToGreek.txt
travel_guides/berlitz1/WhereToIstanbul.txt
travel_guides/berlitz1/WhereToItaly.txt
travel_guides/berlitz1/WhereToJerusalem.txt
travel_guides/berlitz2/Athens-History.txt
travel_guides/berlitz2/Athens-Intro.txt
travel_guides/berlitz2/Athens-WhatToDo.txt
travel_guides/berlitz2/Athens-WhereToGo.txt
travel_guides/berlitz2/Barcelona-WhereToGo.txt
travel_guides/berlitz2/Budapest-History.txt
travel_guides/berlitz2/CostaBlanca-History.txt
travel_guides/berlitz2/Crete-History.txt
travel_guides/berlitz2/Crete-WhatToDo.txt
travel_guides/berlitz2/Crete-WhereToGo.txt
```
This command outputs the names of files in the specified path that include the string "Greece". It's helpful because we might only need to know the file names rather than the context in which the string occurs.


**-r (recursive)**
*Source: found using `man grep`*
```
$ grep -r "Xtebentun"
./travel_guides/berlitz2/Cancun-WhatToDo.txt:Tequila and other alcohol. Tequila is the national drink of Mexico, made from the distilled juice of the agave plant (100% agave tequila is the best quality), and it can be bought under numerous trade names. It is produced only in a very small region of Mexico, around the town of Tequila near Guadalajara, and is in reality a refined version of the agave drink Mezcal. You can also take home a bottle of the Yucatecan liquor Xtebentun, with its flavor of anise, honey, and flowers.
```
This command recursively searches the subdirectories of `written_2` for the case sensitive string "Xtebentun", and it outputs the occurrences as a block of text, giving the string context. It's helpful when we don't know the specific subdirectory we want to search or want to search the entire directory, and when we want to see the string in the context of the file.

```
$ grep -r "Lacquerware"
./travel_guides/berlitz1/WhatToJapan.txt:        Lacquerware. You are least likely to go wrong in terms of
./travel_guides/berlitz2/China-WhatToDo.txt:Lacquerware. Numerous layers of lacquer, individually polished, are applied to trays, cups, vases, and boxes. Lacquer also makes the ideal finish for tea and coffee services, since the material resists boiling water as well as the chemicals in tea and coffee.
```
This command recursively searches the subdirectories of `written_2` for the case sensitive string "Lacquerware". It's helpful because we don't have to specify any path; it just searches the entire directory.
