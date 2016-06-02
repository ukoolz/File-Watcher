# File-Watcher
Design a File watcher program in C which has the following functionalities.

Assume you have three directories ‘DummyDloads’,’DummyDManager’,’DummyTemp’ in your

home(or DummyHome) directory.

You need to watch these three directories for any change and notify the changes that happens in

the directories. The changes will occur through the GUI/Terminal existing in the system.

The notifications should be saved in a file log.txt saved in DummyHome.

Part 1 :

The notifications should include

1) Creation of a file/Directory

2) Deletion of a file/Directory

3) Renaming of a file/Directory

4) Opening a file

5) Modifying a file

The monitoring and notification is applicable for files/directory that resides in any subdirectory of

given three directories.

Part 2 :

Depending on the filetype of the file that occurs in ‘DummyDloads’,’DummyDManager’ (or its

subdirectories), the file should be copied to a destination directory automatically as given in the

‘fileMap.txt’ file.

For example, consider the sample entry in fileMap.txt

wav,oga#DummyHome/Music

mp3#DummyHome/Music/MP3

jpg#DummyHome/Pictures

wav and oga type files should be copied to ‘Music’ directory in ‘DummyHome’

mp3 files will be copied to ‘MP3’ directory in Music Directory.

Note: ‘fileMap.txt’ provided is a sample file for showing the format. More entries may be available

at the time of evaluation. If a destination directory doesn't already exist while copying, then the

same needs to be created through the program before copying the file to destination.

Part 3 :

You should also watch for any possible duplicates in the directories ‘DummyDloads’,

’DummyDManager’ and keep the newer copy among the duplicates.

For finding duplicates you may use the bash command

‘diff ­srq DummyDloads DummyDManager’ and then ‘grep identical’

Piping, I/O redirection and exec implemented in previous assignments should be used here.

For the ‘DummyTemp’ directory, check for the files in the directory and copy the files to

DummyDloads, if any of the following happens:

| A ­ M | is less than 2 minutes

| A ­ C | is less than 1 minute

| M ­ C | is less than 30 seconds

Note: A is Time of last file access

M is Time of last file modification

C is Time of last status change

Part 4:

Write a C program which combines all of the above functionalities and those in the assignment

2, such that a working shell with an added functionality of watcher is implemented.
