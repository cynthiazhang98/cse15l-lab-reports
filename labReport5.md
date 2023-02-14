### the `find` command in bash
#### 1) `-type`
`find /path/to/search -type f #` - This function finds only files in the path given
```
[cs15lwi23auy@ieng6-201]:skill-demo1-data:381$ find ./written_2 -type f
./written_2/non-fiction/OUP/Abernathy/ch1.txt
./written_2/non-fiction/OUP/Abernathy/ch14.txt
./written_2/non-fiction/OUP/Abernathy/ch15.txt
./written_2/non-fiction/OUP/Abernathy/ch2.txt
./written_2/non-fiction/OUP/Abernathy/ch3.txt
...
./written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt
./written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt
./written_2/travel_guides/berlitz2/Vallarta-History.txt
./written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt
./written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
```
`find /path/to/search -type d` - This function finds only directories in the path given
```
[cs15lwi23auy@ieng6-201]:skill-demo1-data:380$ find ./written_2 -type d                        
./written_2
./written_2/non-fiction
./written_2/non-fiction/OUP
./written_2/non-fiction/OUP/Abernathy
./written_2/non-fiction/OUP/Berk
./written_2/non-fiction/OUP/Castro
./written_2/non-fiction/OUP/Fletcher
./written_2/non-fiction/OUP/Kauffman
./written_2/non-fiction/OUP/Rybczynski
./written_2/travel_guides
./written_2/travel_guides/berlitz1
./written_2/travel_guides/berlitz2
```
#### 2) `-size`
`find /path/to/search -size +100M` - find files larger than 100 MB
```
[cs15lwi23auy@ieng6-201]:skill-demo1-data:377$ find ./written_2 -size +100k
./written_2/non-fiction/OUP/Berk/CH4.txt
./written_2/non-fiction/OUP/Berk/ch2.txt
./written_2/travel_guides/berlitz1/WhereToFrance.txt
./written_2/travel_guides/berlitz1/WhereToIndia.txt
./written_2/travel_guides/berlitz1/WhereToItaly.txt
./written_2/travel_guides/berlitz1/WhereToJapan.txt
./written_2/travel_guides/berlitz1/WhereToMalaysia.txt
./written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
./written_2/travel_guides/berlitz2/China-WhereToGo.txt
./written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
```
```
[cs15lwi23auy@ieng6-201]:skill-demo1-data:382$ find ./written_2 -size +200k
./written_2/travel_guides/berlitz1/WhereToFrance.txt
./written_2/travel_guides/berlitz1/WhereToItaly.txt
./written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
```
#### 3) `-mtime`
`find /path/to/search -mtime +7` - find files modified more than 7 days ago
```
[cs15lwi23auy@ieng6-201]:skill-demo1-data:388$ find ./written_2 -mtime -1
./written_2
./written_2/non-fiction
./written_2/non-fiction/OUP
./written_2/non-fiction/OUP/Abernathy
...
./written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt
./written_2/travel_guides/berlitz2/Vallarta-History.txt
./written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt
./written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
```
```
[cs15lwi23auy@ieng6-201]:skill-demo1-data:389$ find ./written_2 -mtime -2
./written_2
./written_2/non-fiction
./written_2/non-fiction/OUP
...
./written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt
./written_2/travel_guides/berlitz2/Vallarta-History.txt
./written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt
./written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
```
#### 4) `-exec`
`find /path/to/search -name "name.txt" -exec cat {} \;` - prints everything in the `name` file 
```
[cs15lwi23auy@ieng6-201]:skill-demo1-data:394$ find ./written_2 -name "Algarve-History.txt" -exec cat {} \;
A Brief History
Little is known of the earliest Stone Age inhabitants of Europe’s southwestern extremity.
The ancient Greeks called them the Cynetes (or Cunetes). Whatever their origins, their culture 
evolved under the pressure and influence of foreign forces. Among the many invading armies that 
...
With aid from the EU, Portugal became one of the fastest-growing countries in Europe. The Algarve, 
already a favorite of sun-seeking beach lovers from England and Northern Europe, also benefited
from EU funds to build up its infrastructure and to invest in tourism. 
```
```
[cs15lwi23auy@ieng6-201]:skill-demo1-data:395$ find ./written_2 -name "Bahamas-History.txt" -exec cat {} \;
A Brief History
Centuries before the arrival of Columbus, a peaceful Amerindian people who called themselves the Luccucairi
had settled in the Bahamas. Originally from South America, they
...
Will it be possible to enjoy the natural splendors of places like Inagua without upsetting the delicate balance
of nature? At the moment, the thinking is that it’s perhaps best to leave these smaller, 
less developed islands in peace.
```
