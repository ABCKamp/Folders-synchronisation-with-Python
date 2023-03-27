# Folders-synchronisation-with-Python

#no third part libraries #use command line arguments 

# one way synchronisation of two folders
## I used “rsync”, as it’s a standard utility, it only transfers the sections of a file that have been changed, it removes the files that don’t exist in the source folder and it preserves file permissions and ownership. 

#periodical
## The code sets the synchronisation to each day, at 10pm (“0 22 ***”) via crontab.

#create a logs file and output it to the console
## the “tee” syntax of crontab allows to append the output to both the logs file and the console log.

###I put the source and destination folders between quotes to avoid issues related to paths containing spaces.
