RiXotStudio's project 067 (RXT067 for short) is work in progress name of Linux distribution based on Gentoo Linux, Argent GNU/Linux and LinuxFromSource.

# INSTALLATION

*WORK IN PROGRESS*

## ABSTRACT

Gentoo Linux fork that works Out Of The Box (OOTB) without sacrificing end-users performance and optimization for multiple configurations including Desktop Environments (DE) and Window Managers (WM) presets.

Optionally binhosts provided by Argent GNU/Linux will/are also available in our fork, but are optional untill Argent GNU/Linux Developer team is able to make them to not sacrifice the optimization and performance.

Our goal is to make gentoo fork with additional features that works on all devices at the best possible performance and optimization.

## ETHICAL CODEX
#### 1) Security is the most important!
Sacrificing performance and optimization over security is allowed if neccesary.


**2) Never sacrifice optimization over automatization.**<br />
Sacrificing optimization over automatization is not acceptable and won't be approved without additional confirmation from an end-user. Codeblocks which sacrifice performance has to have `TODO` comment describing what needs to be done for it to achieve full optimization even if it's seemingly impossible.

**Example:** Using `-march=native` instead of `-march=sandybridge` in `/etc/portage/make.conf` for systems that has been confirmed to perform worse on this preset.

**3) Keep the code clean and readable.**<br />
Pull requests that doesn't contain comments or are hard to read won't be accepted. Depending on the situation the pull request will be redone by RXT067 team or by other contributors or won't be accepted at all. 

Adding comments with usefull info/suggestions is also acceptable for pull request depending on the situation.

If script is used always inform the end-user about what the script is doing and always doublecheck for user-input if the script is about to remove any user data. 

**Example:** 
```bash
# ROOT CHECK
checkroot () {
	if [ $UID == 0 ]; then
	echo "Root is detected."

	# Using `su`
	elif [ $UID != 0 ]; then 
		echo "This script needs root permission to proceed, trying to log-in as root."
		su -c "avasile"   
fi
}
``` 

**4) If it's not broken, it doesn't have enough features!**<br />
Feel free to add or suggest additional features, overengineering is endorsed.

If the overengineering reaches a point where it affects end-user system with low storage or processing power (possible simmilar usecase) then using `lite` version should be prioritized.


### TODO
- Add wine-any
- Add wine-staging in wine-any
- Add wine-d3d9 in wine-any
- Add DXVK
