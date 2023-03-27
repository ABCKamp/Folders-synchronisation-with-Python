# Folders-synchronisation-with-Python

- no third part libraries 
- use command line arguments 

Code: 
0 22 * * * root /user/path/bin/rsync -avh --delete --itemize-changes --log-file=/path/of/log/file.log "/source/folder/" "/destination/folder/" | tee -a /path/to/console.log

1. one way synchronisation of two folders - 
I used “rsync”, as it’s a standard utility, it only transfers the sections of a file that have been changed, it removes the files that don’t exist in the source folder and it preserves file permissions and ownership. 
2. periodical -
The code sets the synchronisation to each day, at 10pm (“0 22 ***”) via crontab.
3. create a logs file and output it to the console -
The “tee” syntax of crontab allows to append the output to both the logs file and the console log.

Last note: I put the source and destination folders between quotes to avoid issues related to paths containing spaces.
