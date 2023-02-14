# Lab 3 Report

## Find method and some examples
1. The first find option is the -empty option. This searches for any empty folders and files in the entered directory or sub-directory

``
$ find ./written_2 -name Berk -empty
Output:
``

``
$ find ./written_2 -empty
Output:
``

As you can see, there were no empty files located in the written_2 directory and it just returned blank. This option is useful in case you want to find any empty files and clean up space. 

2. The second option is the -name option. This searches for a file/directory in the directory with a matching name

``
$ find ./written_2 -name ch1.txt

./written_2/non-fiction/OUP/Abernathy/ch1.txt
./written_2/non-fiction/OUP/Berk/ch1.txt
./written_2/non-fiction/OUP/Fletcher/ch1.txt
./written_2/non-fiction/OUP/Kauffman/ch1.txt
./written_2/non-fiction/OUP/Rybczynski/ch1.txt
``

``
$ find ./written_2 -name Berk
./written_2/non-fiction/OUP/Berk
``

The -name option is very useful for finding the path to a specific directory or for finding files that match the requested name. If you ever lose track of important files, be sure to use find -name!

3. For those who only vaguely remember the file name, the -iname option is for you! It searches for any files who have a similar name pattern and is case-insensitive
``
$ find ./written_2 -iname "*ch*txt"
./written_2/non-fiction/OUP/Abernathy/ch1.txt
./written_2/non-fiction/OUP/Abernathy/ch14.txt
./written_2/non-fiction/OUP/Abernathy/ch15.txt
./written_2/non-fiction/OUP/Abernathy/ch2.txt
./written_2/non-fiction/OUP/Abernathy/ch3.txt
./written_2/non-fiction/OUP/Abernathy/ch6.txt
./written_2/non-fiction/OUP/Abernathy/ch7.txt
./written_2/non-fiction/OUP/Abernathy/ch8.txt
./written_2/non-fiction/OUP/Abernathy/ch9.txt
~
``

``
find ./written_2 -iname "*Berlitz*"
./written_2/travel_guides/berlitz1
./written_2/travel_guides/berlitz2
``

Quick side note: The first example's output with "~" is to simply signify there were a lot more results.
The -iname option is extremley useful if you can't remember the exact name of your file, in fact I found the file of a game I had downloaded through this method!

4. If you only know if the thing you're looking for is a file or directory, then the -type option will prove useful

``
find ./written_2 -type d
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
``

``
$ find ./written_2 -type f
./written_2/non-fiction/OUP/Abernathy/ch1.txt
./written_2/non-fiction/OUP/Abernathy/ch14.txt
./written_2/non-fiction/OUP/Abernathy/ch15.txt
./written_2/non-fiction/OUP/Abernathy/ch2.txt
./written_2/non-fiction/OUP/Abernathy/ch3.txt
./written_2/non-fiction/OUP/Abernathy/ch6.txt
./written_2/non-fiction/OUP/Abernathy/ch7.txt
./written_2/non-fiction/OUP/Abernathy/ch8.txt
./written_2/non-fiction/OUP/Abernathy/ch9.txt
./written_2/non-fiction/OUP/Berk/ch1.txt
./written_2/non-fiction/OUP/Berk/ch2.txt
./written_2/non-fiction/OUP/Berk/CH4.txt
./written_2/non-fiction/OUP/Berk/ch7.txt
./written_2/non-fiction/OUP/Castro/chA.txt
./written_2/non-fiction/OUP/Castro/chB.txt
./written_2/non-fiction/OUP/Castro/chC.txt
./written_2/non-fiction/OUP/Castro/chL.txt
./written_2/non-fiction/OUP/Castro/chM.txt
./written_2/non-fiction/OUP/Castro/chN.txt
~

``
The -type option is useful if you want to see all the sub directories or files contained within a directory. Especially if you have no clue to the name of what you're looking for.

### Sources
[Find methods](https://www.redhat.com/sysadmin/linux-find-command)
