Creating your own cryptocurrency by forking litecoin
====================================

Read this article completely: https://www.hackster.io/pjdecarlo/how-to-make-a-cryptocurrency-using-litecoin-v0-15-source-fb5e82

If on a Mac
-----------
Using a normal sed: http://daoyuan.li/a-normal-sed-on-mac/

Steps
-----
1. Fork and clone litecoin, pull, change branch to 0.15, then compile litecoin.  Compilation should take 15-30 minutes.
2. Complete the renaming and recompile
  * use `find ./ -type f  -exec sed -i "s/Litecoin/Hatchcoin/g" {} \;` on mac (using "normal sed" above)
  * if you get error: `make[2]: *** No rule to make target 'qt/res/icons/hatchcoin_splash.png', needed by 'qt/qrc_bitcoin.cpp'.  Stop.` you'll need to rename ./src/qt/res/icons/litecoin_splash.png to hatchcoin_splash.png
3. Create the docker image
  * what is docker?: 
    * Part 1: https://www.youtube.com/watch?v=pGYAg7TMmp0
    * Part 2: https://www.youtube.com/watch?v=JBtWxj9l7zM
    * Part 3: https://www.youtube.com/watch?v=K6WER0oI-qs

