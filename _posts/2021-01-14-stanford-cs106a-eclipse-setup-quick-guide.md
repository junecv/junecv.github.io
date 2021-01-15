---
layout: post
title: Stanford CS106A (2007 SEE version) Eclipse Setup Quick Guide
---

This is a quick reference for [CS106A](https://see.stanford.edu/Course/CS106A) self-learners when they encounter difficulties installing and setting up Eclipse, or having blank Karel screen problem. I use Macbook M1, but below included links shall make it easy for anyone using other versions of Macbook or PC.

### Installing Eclipse and Java Runtime Environment

There is a handout [05-downloading-eclipse.pdf](https://see.stanford.edu/materials/icspmcs106a/05-downloading-eclipse.pdf), but you won't be here if it helped you found Karel. Instead, refer to [this newer version](https://web.stanford.edu/dept/cs_edu/eclipse/) (*the manual*) and below notes.

Do not use the links provided in the installation sections. I suggest using the [Eclipse Installer](https://www.eclipse.org/downloads/) as it includes a JRE (Java Runtime Environment).

### Configuring Eclipse

Then go back to the manual, and follow the configuration part. Note that for Step 4, the correct entry is "https://web.stanford.edu/dept/cs_edu/eclipse/plugin" as stated, which is different than the screen captured.

The screenshot in the manual shows that the software Stanford CS106 is of Version 2.1.0.201609271618, but you should see at least 4.0.1.

The rest is quite straight forward.

### Importing Assignments (aka seeing Karel for real)

I put together a Blank Karel [here](https://drive.google.com/file/d/1cv1tH6tL5Zg6yAPNx11ETCnMb2bZLXv6/view?usp=sharing) that has work files for Assignment 1, all worlds (should cover all assignments), and most importantly a good and working .jar.

Download the zip file and use the "Import Project" function and guideline stated in the manual, then you're good to go.

To work on other assignments, download the files from SEE, then Import Project, then copy or move the src files from each assignment to the Blank Karel project.

Good luck.

### Other notes

#### *I tried this[https://cs.stanford.edu/people/eroberts/courses/cs106a/materials/], it doesn't work*

Not even after changing the BlankKarel.jar name to spl.jar.

#### *Credit*

I first solved the blank screen problem by following the answer from Anonymous [here](https://stackoverflow.com/questions/43929424/karel-screen-is-blank-when-trying-to-run-in-eclipse-on-mac). But as the course design has changed from using Java to using Python as teaching medium, the current course website no longer have blank Karel project.

#### *Why I'm doing this*

Stanford [SEE](https://see.stanford.edu) is an amazing platform that provides free resources for software engineering newbies who want to learn the *science* in computer science, and the *methodology* in programming, and not just coding. I have a lot of pleasure "attending" Professor Sahami's class and know exactly how Karel sounds like.

But the materials are from 2007, so understandably there are some broken links. When it happens multiple times during the setup phase, it can be frustrating and discouraging to someone with zero experience in computer programing, *exactly* whom this course is supposed to teach. In 2020, the course design took a turn to use Python instead of Java, meaning it's more difficult to find help to fill in the gap. I feel that such precious collection of materials should not go obsolete.
