## verifying if it's root or not

```
if [[ $EUID -ne 0 ]]; then
    echo "$0 is not running as root. Try using sudo."
    exit 2
fi
```

OR 

```
if [ ! "`whoami`" = "root" ]
then
    echo "\nPlease run script as root."
    exit 1
fi
```

OR

**a simpler way is to start shell with root the following path ***
```
 #!/bin/su root
```
