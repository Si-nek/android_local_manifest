Local manifest for Jiayu s3 (Official Resurrection Remix android 7.1.2) 

Getting Started

Make directory for the repo binary

  $ mkdir ~/bin

Add directory for the repo binary to its path

  $ PATH=~/bin:$PATH

Downloading repo binary and placing it in the proper directory

  $ curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo

Giving the repo binary the proper permissions

  $ chmod a+x ~/bin/repo

Creating directory for where the RR repo will be stored and synced

  $ mkdir ~/RR
  $ cd ~/RR

Initializing the RR repo and downloading the manifest

  $  repo init -u https://github.com/ResurrectionRemix/platform_manifest.git -b nougat


Copy "mtk.xml" under android_src/.repo/local_manifests

repo sync -j7

Build the code:

source build/envsetup.sh

breakfast s3_h560

make -j4 bacon showcommands 2>&1 | tee build.log

