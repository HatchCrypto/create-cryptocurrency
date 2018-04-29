Creating your own cryptocurrency by forking litecoin
====================================

Read this article completely: https://www.hackster.io/pjdecarlo/how-to-make-a-cryptocurrency-using-litecoin-v0-15-source-fb5e82

If on a Mac
-----------
Use GNU sed/find or run these commands on a linux box
warning: 'sed' and 'find' commands on Mac are POSIX and not GNU, and therefore have different options
https://www.topbug.net/blog/2013/04/14/install-and-use-gnu-command-line-tools-in-mac-os-x/

Steps
-----
1. Fork and clone litecoin, pull, switch to branch 0.15, then compile litecoin.  Compilation should take 15-30 minutes.
  * `git checkout 0.15`
2. Complete the renaming and recompile
3. Create the docker image
  * what is docker?: 
    * Part 1: https://www.youtube.com/watch?v=pGYAg7TMmp0
    * Part 2: https://www.youtube.com/watch?v=JBtWxj9l7zM
    * Part 3: https://www.youtube.com/watch?v=K6WER0oI-qs



  * run also `find ./ -type f -exec sed -i "s/LITECOIN/HATCHCOIN/g" {} \;`
  * if you get compilation errors, you may need to rename some assets from litecoin* to hatchcoin* (assets are in ./src/qt/res)
