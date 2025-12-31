
# Linux Fundamentals - Part 2 - TryHackMe Walkthrough

[Room Link](https://tryhackme.com/room/linuxfundamentalspart2)

## Table of Contents

1. How does this topic relates with Cyber Security Business
2. Underlying concepts with security relevance
3. Hands-on Labs with challenges faced
4. Conclusion followed with a key takeaway

## How does this topic relates with Cyber Security in Business

## Underlying concepts with security relevance

#### SSH 

Secure shell or SSH is a protocol that are encrypted to connect between two different devices.

*Security Relevance*: Make sure that the client has implemented cyber hygiene when connecting 2 different devices, for example: If device A wants to connect to device B via SSH, then implementing a unique and long password are the security principles. 

**Possible threats and mitigation**: The SSH port can be checked using a tool called `nmap`, whether it is opened or not based on the results that the tool shows. One possible mitigation is to perform a hardening on the device, which is disable certain features that the device has enabled by default.

## Hands-on Labs with challenges faced

#### Creating a SSH connection between the AttackBox and the target

![How to connect a target via SSH](Assets/0.png "How to connect machine target via SSH")

This is the thing that I never knew before. Sometimes, I always forget on how to connect machines when there is a SSH port opened. On the image given above, it provides the command and the output itself. It needs 2 things, the username and the IP address of the target. If there is missing one of the two credentials, then it is not possible to connect the target. You will gain access to the target's machine once you have logged in via the SSH. 

#### Answering the discussion question about Flags and Switches

![How to answer the flag and switches question](Assets/1.png "What flag to use")

I encountered the question in the section about Flags and Switches, which is written "What flag would we use to display the output in a "human-readable" way?". My initial thought was: What is the context, and what command is it? This question is a trap and requires me to analyse what the command is. Because the first question requires the reader to see the `ls` manual command, so I assume this third question is related about the `ls` command as well. I went through the man page of `ls`, and to make things a little easier, I search the command with the word "readable", which is written on the question. To search in the man page, type the symbol `/`, followed by a keyword that you want to search for. In this context, the word is "readable".

#### Discovering what is -R flag in rm

![The meaning of -R](Assets/2.png "What is -R in rm?")

My curiosity spikes when I read the terminal in one of TryHackMe's guide in "filesystem interaction continued". One of the walkthroughs provided by TryHackMe gave this command:
```
tryhackme@linux2:~$ rm -R mydirectory
tryhackme@linux2:~$ ls           
folder1
```

This is useful for removing directory, even if the directory contains something in it. After searching through the terminal, it provides the output above. I do not understand what is the relation between the recursive process of removing a directory. Well, it is already a fact since the manual has written its relationship:

`By default, rm does not remove directories.  Use the --recursive (-r or -R) option to remove each listed directory, too, along with all of its contents.`

(Source: manual of `rm` command).

## Conclusion/Summary followed with a key takeaway
