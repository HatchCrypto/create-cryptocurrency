Creating your own cryptocurrency by forking litecoin
====================================

Read this article completely: https://www.hackster.io/pjdecarlo/how-to-make-a-cryptocurrency-using-litecoin-v0-15-source-fb5e82

If on a Mac
-----------
Using a normal sed: http://daoyuan.li/a-normal-sed-on-mac/

Steps
-----
1. Fork and clone litecoin, pull, change branch to 0.15, then compile litecoin.  Compilation should take 15-30 minutes.
2. Complete the renaming
  * use `find ./ -type f  -exec sed -i "s/Litecoin/Hatchcoin/g" {} \;` on mac (using "normal sed" above)
3. Create the docker image

