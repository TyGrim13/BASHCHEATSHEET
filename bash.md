# **Bash**

ls # lists your files in current directory, ls <dir> to print files in a specific directory

ls -l # lists your files in 'long format', which contains the exact size of the file, who owns the file and who has the right to look at it, and when it was last modified

ls -a # lists all files in 'long format', including hidden files (name beginning with '.')

ln -s <filename> <link> # creates symbolic link to file

readlink <filename> # shows where a symbolic links points to

tree # show directories and subdirectories in easilly readable file tree

mc # terminal file explorer (alternative to ncdu)

touch <filename> # creates or updates (edit) your file
mktemp -t <filename> # make a temp file in /tmp/ which is deleted at next boot (-d to make directory)

cat <filename> # prints file raw content (will not be interpreted)

any_command > <filename> # '>' is used to perform redirections, it will set any_command's stdout to file instead of "real stdout" (generally /dev/stdout)

more <filename> # shows the first part of a file (move with space and type q to quit)

head <filename> # outputs the first lines of file (default: 10 lines)

tail <filename> # outputs the last lines of file (useful with -f option) (default: 10 lines)

vim <filename> # opens a file in VIM (VI iMproved) text editor, will create it if it doesn't exist

mv <filename1> <dest> # moves a file to destination, behavior will change based on 'dest' type (dir: file is placed into dir; file: file will replace dest (tip: useful for renaming))

cp <filename1> <dest> # copies a file

rm <filename> # removes a file

find . -name <name> <type> # searches for a file or a directory in the current directory and all its sub-directories by its name

diff <filename1> <filename2> # compares files, and shows where they differ

wc <filename> # tells you how many lines, words and characters there are in a file. Use -lwc (lines, word, character) to ouput only 1 of those informations

sort <filename> # sorts the contents of a text file line by line in alphabetical order, use -n for numeric sort and -r for reversing order.

sort -t -k <filename> # sorts the contents on specific sort key field starting from 1, using the field separator t.

rev # reverse string characters (hello becomes olleh)

chmod -options <filename> # lets you change the read, write, and execute permissions on your files (more infos: SUID, GUID)

gzip <filename> # compresses files using gzip algorithm

gunzip <filename> # uncompresses files compressed by gzip

gzcat <filename> # lets you look at gzipped file without actually having to gunzip it

lpr <filename> # prints the file

lpq # checks out the printer queue

lprm <jobnumber> #
removes something from the printer queue

genscript # converts plain text files into postscript for printing and gives you some options for formatting

dvips <filename> # prints .dvi files (i.e. files produced by LaTeX)

grep <pattern> <filenames> # looks for the string in the files

grep -r <pattern> <dir> # search recursively for pattern in directory

head -n file_name | tail +n # Print nth line from file.

head -y lines.txt | tail +x # want to display all the lines from x to y. This includes the xth and yth lines.
