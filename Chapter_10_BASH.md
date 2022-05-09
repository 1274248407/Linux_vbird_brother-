# BASH

## 10.6.4

>Let's say you have a lot of accounts today, and you want to know where the largest user ID is currently
```bash
 last | cut -d ' ' -f1 | sort
```
-------
## 10.6.4

```bash
cat /etc/group	|	paste /etc/passwd /etc/shadow -	|	head -n 3
```
> '-' = /etc/group 
-------
## 10.6.7

```bash
tar -cvf - /home | tar -xvf - -C /tmp/homeback
```
> '-' = home.tar 

the above example says: 'i package the files in /home for him, but the packaged data is not recorded to the archives, but to stdout; after going through the pipeline, the tar -cvf -/home is transmitted to the later tar -xvf -'. 

the latter one - takes the stdout of the previous directive, so we don't need to use filename! 

------------