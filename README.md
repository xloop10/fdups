
## DESCRIPTION

The script finds all duplicate files in a list of files and folders.

You give it a list of files and folders, it takes all files in those folders and compares them to one another to find which ones are the same.
It doesn't care about file names, directory structure or the location of the files in that structure. It cares only about bytes - whether or not two files or more are identical in their bytes.

## How to use

It works like this:

```
import fdups
f = fdups.fdups()
f.set(["", "", ...])
f.fdups()
```

You set a list of files and folders and call fdups().  
The list can contain any mixture of files and folders.  
If you set a new list of folders it clears the previous result.  


## Example

```
>>> import fdups
>>> f = fdups.fdups()
>>> f.set(["C:\\Python27\\Scripts", "C:\\Python27\\Lib\\site-packages\\setuptools"])
>>> f.fdups()
Collecting files
Sorting
Comparing
. . . . . . 
Info:
Total number of files compared:  162
Non duplicate files:  151
Duplicate groups:  4
Total wasted space:  518.0 kB   ( 530465 )

Do you want to see the duplicate groups?
(y for Yes, anything else for No)
y

C:\Python27\Scripts\futurize.exe
C:\Python27\Scripts\pasteurize.exe
C:\Python27\Lib\site-packages\setuptools\cli-32.exe
C:\Python27\Lib\site-packages\setuptools\cli.exe

C:\Python27\Lib\site-packages\setuptools\gui-32.exe
C:\Python27\Lib\site-packages\setuptools\gui.exe

C:\Python27\Scripts\pip.exe
C:\Python27\Scripts\pip2.7.exe
C:\Python27\Scripts\pip2.exe

C:\Python27\Scripts\easy_install-2.7.exe
C:\Python27\Scripts\easy_install.exe

Do you want to see the NON duplicate files? (151 files)
(y for Yes, anything else for No)
```


