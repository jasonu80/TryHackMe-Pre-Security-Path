
# Linux Fundamentals - Part 3 - TryHackMe Walkthrough

[Room Link](https://tryhackme.com/room/linuxfundamentalspart3)

## Table of Contents

1. How does this topic related with cyber security in Business
2. Underlying Concepts with Threats and Mitigations
3. Hands-on Labs with Challenges faced
4. Conclusion or Summary

## How does this topic relates with cyber security

## Underlying concepts

#### Terminal Text Editors 

What I know: There are multiple of text editors in Linux, the most popular are `vim` and `nano`. Both of the tools are utilised like a text editor.

What I discovered: `nano` is a standard and popular text editor in most Linux Distributions, while `vim` is the next-level text editor in Linux. 

Then what: By mastering these text editors, it will be easy for performing a number of operations in the terminal while searching in a file. For instance, if there is a giant piece of text, you would use `nano` for performing a search of a keyword, while using `vim` for navigating through different pages.

#### Processes

What I know: It shows how many memory consumed in a system.

What I discovered:

Then what:

#### General or useful Utilities

What I know: None.

What I discovered: Commands that are useful for downloading resources from a web server or file transfer, as well as serving resources. These commands are `wget`, `scp`, and `http.server` (uses python for this feature). 

Then what: By knowing that it is possible to download and upload files in any protocol, then it is also possible to upload malicious scripts or download sensitive information from a vulnerable machine. 

#### How to maintain Linux System: Automation, Package Management, Logs.

What I know: Package Management is utilised for installing tools and packages, Logs for accessing traffic history.

What I discovered:

Then what:

## Hands-on Labs with challenges faced

#### Create a file using `nano`

![Create file](Assets/0.png "Create file using nano")

The command to get the popup above is: `nano myfile`. The `myfile` is the name of the file that you want to create or edit. If there is no file name exists in the working directory, it will create the file instead. To Save, hit `Ctrl+O`, enter, then `Ctrl+X` to exit. The `Ctrl` button is located next to `Fn` and beside the shift keys in some keyboards.

#### Retrieve contents from the vulnerable machine

There are multiple ways for performing this. The first way is using a `http.server` and `wget` on the vulnerable machine and download it from the other machine (from the image above) and the second way is using `scp` command.

##### First way: Serving and downloading the contents.

![Retrieve contents from vulnerable machine](Assets/1.png "Retrieve contents from a vulnerable machine")

![Download contents and view the content](Assets/2.png "Download and view the contents of the file.")

Possible errors: direct the output into a file with the same extension, such as `wget source/filename > filenameX; cat filenameX`. I tried this and the output (`filenameX`) does not show anything. The contents of the download will be viewable with the name of that is same within the source.

Proof-of-Concept:

![wget redirection output will not work](Assets/3.png "Don't redirect the output when using wget.")

##### Second Way: Using `scp` for retrieving the file.

The `scp` syntax works only with Source and destination only, with the files that will be sent or downloaded from the web server. Still, it requires the web server, if there is no web server, it is possible to only send the file. 

Upload: `scp file_on_local source@destination:file_on_transfer`

Download: `scp source@destination:file_available name_we_want`

The screenshot below demonstrates an SCP without the need to use `http.server`:

![Using SCP to transfer files](Assets/4.png "SCP to transfer files")

![Result check](Assets/5.png "Results")

More info about `http.server` with python3: [Link](https://docs.python.org/3/library/http.server.html)

## Conclusion or Summary
