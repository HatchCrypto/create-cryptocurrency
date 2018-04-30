Creating your own cryptocurrency by forking litecoin
====================================

Read this article completely, we will be using it as the main guide. https://www.hackster.io/pjdecarlo/how-to-make-a-cryptocurrency-using-litecoin-v0-15-source-fb5e82

If on a Mac
-----------
* Warning: 'sed' and 'find' commands on Mac are POSIX and not GNU, and therefore behave differently than linux 'sed' and 'find'.  If you want to follow tutorial, install GNU sed & find.  https://www.topbug.net/blog/2013/04/14/install-and-use-gnu-command-line-tools-in-mac-os-x/

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
    * Configure automated builds on Docker Hub: https://docs.docker.com/docker-hub/builds/
4. Edit the code
  * pchMessageStart magic number
    * https://bitcoin.stackexchange.com/questions/43189/what-is-the-magic-number-used-in-the-block-structure/43191#43191
  * update base58Prefixes to unique values
  * create the Genesis Block and associated Merkle Root
    * important: make sure your pszTimestamp is less than 64 characters or program will crash!
  * remove dnsseeds and seednodes
  * set minimum chain work to 0x00
  * change the default port
  * run the daemon with `./src/hatchcoind --printtoconsole`
  * deploy a minimum of 2 nodes (you can use your local machine)
  * create a .conf file to configure your client to connect to nodes




