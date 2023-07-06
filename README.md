# tasks1037
## BASH SCRIPTING

### Suppose we have a text file that contains some file names, for example:
jobe
/var/www/html/index.html
/var/www/html/jobe
Write a shell script that takes the name of such a text file as an argument and shows its content
For example:

| Test 	| Input | Result |
| ------ | ------ | ------ |
| # Test 1  | data1.txt |  jobe |
| | | /var/www/html/index.html |
| | | /var/www/html/jobe |

Answer:
```#!/usr/bin/env bash
fname=$1
showcont=`cat $fname`
echo "$showcont"\
```

### Write a shell script that takes arguments as a string of multiple words separated by spaces, and prints the words one per line.

For example:

| Test 	| Input | Result |
| ------ | ------ | ------ |
| # Test 1  | a ab abc | a |
| | |  ab |
| | | abc |

Answer:

```#!/usr/bin/env bash
for words in $*; do
echo "$words"
done
```

### Write pattern without script
For example:

| Test 	| Input | Result |
| ------ | ------ | ------ |
| Test case 1 | a | matched |
| Test case 2 | b | not matched |

Answer:

```[^b-z]```

### Write a regular expression pattern that matches strings according to the example:
For example:

| Test 	| Input | Result |
| ------ | ------ | ------ |
| Test1 | abcdefg | matched |
| Test2 | gabcdef | matched |
| Test3 | defg | not matched |
| Test4 | gadbec | not matched |

Answer:

```[abcdefg]{7}```
