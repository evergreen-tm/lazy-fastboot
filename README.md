# lazy-fastboot
LFB (Lazy Fastboot) is intended for fastboot commands that you may need to run often, and would take more time to do manually, e.g. flashing stock and similar tasks.
This is done through the use of packs. Packs are essentially sister scripts to lfb, which contain the commands for fastboot to run. Whereas a normal fastboot command may be something like "fastboot flash recovery recovery.img", it is presented in a pack like "try "$fbdir" flash recovery "$fldir"/recovery.img".
Defaults may be hard-coded via the config file. As I am lazy (and such was the inspiration of this project), you'll need to edit them to be your own username. Without them, lfb takes three arguments: Path to fastboot, directory containing the files to flash, and name of pack.
With defaults, lfb takes two arguments. The first should always be -d or --default, to signify that you want to use them. The second should be the pack name.

## Setting up
Just make sure that lfb, config, and the packs directory are in the same place.

## Making a pack
As packs are bash scripts, they can be adapted as needed. As long as they are sourced from the main script, they can communicate.
There is no real correct way to do it, because there are so many ways, but something like the template may be a good place to start.
