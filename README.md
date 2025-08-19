![Title Block: Front-end BASH Scripts](./images-for-readme/a_title-block.png)

# Front-End Revert Backup and Build with BASH

A simple solution for local control for front-end web development projects.

Designed specifically for managing small to medium sized projects using BASH scripts. 

[HW HTML Drafting Project](https://github.com/dckimMysteryAuthor/HW-HTML-Drafting-Project) is an example of an Open-Source Project which made use of this system. It is clear that with a few minor adaptations, the system of scripts can be utilized in many cases, with myriad benefits, and still function along-side GIT.

This is not designed as a replacement for GIT by any means. A possible workflow might be: Make changes locally, and make backups locally at will. This way the safety of a complete backup is available locally without needing to rely completely on GIT for recovery after a potentially bad local change. This should promote a more free atmosphere within the local context, and improve control and quality of final commits made through git.

You are just a few tweaks and maybe one script away from possibly aligning this system with a scripted transfer to the local GIT repository.

Whether you choose to work from within the latest chronologically named directory, or write a script to maintain a constant top working directory: That's completely up to you.

## For anyone who is kinda new to web development and has just discovered this:

The struggle is over, and the easy part is now here. You can backup at any time, so you will never step back from the progress you have made. The revert will only take you back a single step but, you can always change into an earlier directory manually and then use the backup script that is inside of that directory. Then that one becomes the top. **Good To Go**.

## As for me? I like it just how it is.

I might change it around a little to see if it can be even better but, you never know how good something is until you try something else and it's bad.

# Here is a diagram

![File Map for the backup/revert system](./images-for-readme/a_file-map.png)

This still might seem somewhat complex, and so I will now describe the structure of the files, and how the user will perceive this in daily work.

There are three directories shown in the diagram labelled '**abc**'.

This explanation will focus on the **combined example usage**. First I will tell about the script named '**setup**'. This is a BASH script which must be first placed in the intended project's directory, then it must be run by typing '**. ./setup**'

This will build the basic **backup/revert system** and the starter folders. We will then be brought into the folder with the latest date, where I recommend that an initial backup be performed by typing '**. ./backup**'

For information: The revert script will be accessed the same way as the others, and will only allow us to be brought back one step. If we wish to revert further than one step, we must manually change directories and then use the backup script from the desired directory. Then that directory will become the latest directory.

The script named '**setup**' can be used indepently from the stuff in the folder labelled '**b_chalk-script**', so, it is a very easy and versatile single file solution for **local backup/revert**, independent of GIT.

I will now explain the second part, which contains the script named '**chalk**'.

The '**chalk**' script expects certain directories to be present, and then it produces certain files.

It is expected that the folders that you see are all present, and that there is a '**style.css**' file inside of the '**e_stylesheets**' directory.

These files are what our script will write for us:
- **index.html**
- **JS_treeDiagram.html**
- **a_jsObject.js**

These files have different purposes and are assembled in different ways.

If you look inside of the '**chalk**' script, you will know immediately how the files are assembled. I will describe it briefly:

The '**index.html**' file is assembled with a minimal header, which has a reference to the '**style.css**' file, that's why we needed it. Then there are references made to link all of the scripts that are found in the '**js**' folder. Good thing that we made the **a_jsObject.js** script first. That will give a nice extra way of accessing out list of functions from the browser console. Just start typing '**js**'. and you will get a list automatically. Then we put a footer on to the end, and that's pretty much it.

We also draw up the '**JS_treeDiagram.html**' file. That one gives a useful map of our '**a_programFunctions**' folder.

## Now I will tell about the '**a_programFunctions**' folder.

This is very simple to use. We can put as many folders inside, and with whatever names we want. The script will later find them all out, and the files whcich are inside of them, and then include them for processing. The best thing that we can do is to name the folders with leading alphabetical letters. Like this: '**a_folder**', then '**b_otherFolder**', etc.

This results in a very fast and convenient way of navigating out directories using BASH. It also keeps everything lined up the way we wanted it.

## A special rule

There is one special rule about the names of the files within the '**a_programFunctions**' directory:

The file names are of this form:

'**a_fileName**' OR '**1_filename**'.

Letters are the best because there are 26;

Try it out, see how it works.

Inside of the file there should be a function which has the exact same name. For example:

file name is '**a_myFunctionName**';

inside the file it should use this: '**function myFunctionName**() {'

## That is pretty much it

Best wishes,

-dckimGUY
