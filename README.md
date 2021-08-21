# HighLvlAss-Kicker

## Installation

Short guide for future me, by the way you won't need to download all the files listed, I'll probably sort it out later when Im more acquainted with github \o/, for now just follow this guide! 

*Note: This guide assumes you still use windows*

### Setting Up

**Assembly_Root**

ASSEMBLY_ROOT address is `C:\TEMP\ASSEMBLY`

Meaning go ahead and make a folder called TEMP in your C drive
Then make a sub-folder called ASSEMBLY in TEMP
Ta-da!

**Installing FHLA**

Theres a file called `fhla.setup.exe` in here somewhere
Find it, download it into your Assembly folder
Double-click it to begin installation,  a dialogue box will appear. Press `Yes`.

The `Setup Wizard` will appear, press `Next` to continue with the installation. Then you'll be asked to select your Assembly_Root directory. Rememnber our setup? That is your Assembly_Root directory. You'll be asked to confirm installation, press `Install`. Click `Finish` to close the wizard `^-^`

You should have an `hla` sub-folder in your Assembly folder that contains several folders and files like the `include` folder, the `hlalib` folder, `pomake`, `polib`, `fasm`, `fhla`, etc.

**Making A Batch File**

Use a text editor, like Notepad to make a batch file, write the following
```
path=c:\temp\assembly\hla;%path%
set lib=c:\temp\assembly\hla\hlalib
set hlainc=c:\temp\assembly\hla\include
set hlalib=c:\temp\assembly\hla\hlalib\hlalib.lib
```

Save as `ihla.bat` within the `c:\temp\assembly\hla` subdirectory
Notepad might save it as a `.txt` file, you can "override" this by saving it an "All Files" type.

**Testing 1, 2, 3**

Open a DOS window, you can do so by searching `cmd` in the start menu
Type in the following commands one=by-one please
```
cd c:\temp\assembly\hla
ihla
fhla
```
A bunch of stuff that I dont know the meaning of, will appear >.<
You can test out if it runs correctly with the `HELLO.hla` file in the `hlahello` folder. Running .hla files will be explained in the next section!

### Running HLA Files

**Viewing and Writing Code**

The course I took utlizied Notepad to write and view code. Much like the batch file we needed to create, we save our code as `[FileName].hla`, please make sure to save it as an "All Files" type otherwise you'll get something like `[FileName].txt`

All the `.hla` files in this repo can be opened and viewed with Notepad.

**Running Code**

You'll notice that within each folder under Assembly, apart from a `.hla` file there are also a ton of other files. I wish I could tell you what each file is but I am not yet privy to that knowledge. Those extra files are generated the first time you run your `.hla` file, so don't waste time downloading them, only worry about creating sub-folders in ASSEMBLY to contain your `.hla` files. 

Okies! Running your an `.hla` for the first time `^-^` We will make use of our batch file. Go ahead and open a DOS window and type in the following commands one-by-one:
```
cd c:\temp\assembly\hla
ihla
cd c:\temp\assembly\[FolderName]
fhla [hlaFileName]
[hlaFileName]
```
The above is a template and below is a an example using it to test-run `HELLO.hla`
```
cd c:\temp\assembly\hla
ihla
cd c:\temp\assembly\hlahello
fhla hello
hello
```
Our `HELLO.hla` file is stored in our `hlahello` folder. Also you can treat the `HELLO.hla` file as your typical HelloWorld code `^-^` Oh right case doesnt matter, and when referring to an `.hla` file in DOS, omit the `.hla` bit.

After successfully running your `.hla` file for the first time a wierd message should pop up. The Professor said to ignore it and that he hadn't found a way to get rid of it, so we too shall ignore it `:D`

The message in question:
```
POLINK:warning: /SECTION:.bss ignored; section is missing.
```

**Notes**

When running stuff for a second time, you open a DOS window and issue the following command:
```
cd c:\temp\assembly\[FolderName]
[hlaFileName]
```
Notice the similarity between our files and the template in the previous section. Please do it in this order otherwise it may not recognize the path.

You may also spy the `.exe` file generated within your folder upon first running an `.hla` file. Technically, you can click on it to run the program, but it always closes as soon as you input data. It doesn't give any output. I'm not entirely sure what thats all about, hmmm... maybe future me will know `^-^`

### Warnings!
Given that this is the first time Ive uploaded something to github, I haven't cleaned up my files and code. If you see folders that have a B attached to them, those are second attempts at homeworks that run properly. In short there are files that don't run properly but feel free to peruse through the files!
