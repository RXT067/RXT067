Every contribution is welcomed as long as it follows ethical codex.

# ETHICAL CODEX
#### 1) Security is the most important!
Sacrificing performance and optimization over security is allowed if neccesary.


#### 2) Never sacrifice optimization over automatization.
Sacrificing optimization over automatization is not acceptable and won't be approved without additional confirmation from an end-user. Codeblocks which sacrifice performance has to have `TODO` comment describing what needs to be done for it to achieve full optimization even if it's seemingly impossible.

**Example:** Using `-march=native` instead of `-march=sandybridge` in `/etc/portage/make.conf` for systems that has been confirmed to perform worse on this preset.


#### 3) Keep the code clean and readable.
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


#### 4) If it's not broken, it doesn't have enough features!
Feel free to add or suggest additional features, overengineering is endorsed.

If the overengineering reaches a point where it affects end-user system with low storage or processing power (possible simmilar usecase) then using `lite` version should be prioritized.
