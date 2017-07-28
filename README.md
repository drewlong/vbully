# vBully
____

This is a simple suite of tools for exploiting vBulletin forums v3.8.5 - 4.2.3, parsing the output, and cracking the passwords. 

- `vbdump` is used for site exploitation, it returns the SQL Injection response (you should pipe into a file)
- `vbparse`is used to parse the response file for v3 & v4 hashes
- `vbcrack` is the vBulletin hash cracker, it utilizes the Gibberish ruby gem to parse a wordlist, hash the entries, and crack the hashes.

To install: 

    gem install gibberish mechanize

Depends on Ruby v2.3 or higher. 
