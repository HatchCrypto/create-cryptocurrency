Creating your own cryptocurrency by forking litecoin
====================================

Read this article completely: https://www.hackster.io/pjdecarlo/how-to-make-a-cryptocurrency-using-litecoin-v0-15-source-fb5e82

If on a Mac
-----------
* Use GNU sed/find or run these commands on a linux box.  warning: 'sed' and 'find' commands on Mac are POSIX and not GNU, and therefore have different options
* https://www.topbug.net/blog/2013/04/14/install-and-use-gnu-command-line-tools-in-mac-os-x/

Steps
-----
1. Fork and clone litecoin, pull, switch to branch 0.15, then compile litecoin.  Compilation should take 15-30 minutes.
2. Complete the renaming and recompile
  * if you get compilation errors, you may need to rename some files from litecoin* to hatchcoin* (in ./src/qt/res and ./doc/man)
3. Create the docker image
  * what is docker?: 
    * Docker Tutorial, Part 1: https://www.youtube.com/watch?v=pGYAg7TMmp0
    * Docker Tutorial, Part 2: https://www.youtube.com/watch?v=JBtWxj9l7zM
    * warning: Docker Tutorial, Part 3 is deprecated
    * Docker Docs, Get Started: https://docs.docker.com/get-started/ (read part 1, 2)
    * Debug Broken Docker Builds: https://www.youtube.com/watch?v=RH_I0KXHBcA
    * Tip: build your docker image from a fresh git clone of hatchcoin so that .gitignore files are ignored
    




