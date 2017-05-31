# git-and-pharo
Getting Git and Pharo to play nicely.

## Description
Smalltalk is a great language, but to me it has the characteristic of not playing nice with others outside of its own virtual machine. This is a playground repository for getting experience in using Git with Pharo Smalltalk.

## Resources
This repository is done with guidance from [Peter Uhnak's blog](https://www.peteruhnak.com/blog/2016/07/25/how-to-use-git-and-github-with-pharo/).

## Conclusions
Using GitFileTree integrates Git operations into the Monticello tools. This is still not a good Git experience. Proper branching is not available. For future Git operations it is easier just to add a FileTree repository to the Monticello browser, and point the FileTree repository at your Git repository on your local file system. In Pharo use the Monticello tools for commiting to the FileTree repository. Then use a console or other Git client outside Pharo for branching, pushing to remotes etc.

One downside to using version control with Pharo is that it saves entire classes inside a package. If you have made additions to the built in class libraries, this can be a very big package even if you only changed a few methods. For example, this repository has the packages containing all the Kernel and Kernel-Test classes, even though I only added one method to each package. On the upside each package is neatly broken down into directories of each class, with each instance or class method in its own text file. These text files are human readable Smalltalk source code.
