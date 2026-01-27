# CTF Resources and Cheat Sheet

This repository is a collection of essential tools, links, and commands for Capture The Flag competitions. It is designed as a quick reference for beginners to help identify, decode, and analyze challenges.

---

## Web Based Tools

### Analysis and Decoding
* CyberChef: https://gchq.github.io/CyberChef/ (The primary tool for data conversion)
* HexEd.it: https://hexed.it/ (Browser-based hex editor for file analysis)
* DCode: https://www.dcode.fr/en (Excellent for identifying and solving ciphers)
* Boxentriq: https://www.boxentriq.com/code-breaking (Logic and code-breaking tools)

### Steganography (Hidden Data)
* Aperisolve: https://www.aperisolve.com/ (Checks images for hidden layers and data)
* StegOnline: https://stegonline.georgeom.net/ (Web-based steganography tool)
* ExifView: https://exifview.com/ (Quickly view metadata in image files)

### Password Cracking and Hashes
* CrackStation: https://crackstation.net/ (Lookup for common password hashes)
* Hashes.com: https://hashes.com/en/decrypt/hash (Hash decryption service)

---

## File Signatures and Magic Bytes

In CTF challenges, files are often disguised with the wrong extension. Use a Hex Editor to check the first few bytes (headers).

| File Type | Hex Signature (Start of file) | ASCII Translation |
|-----------|-------------------------------|-------------------|
| PNG       | 89 50 4E 47 0D 0A 1A 0A     | .PNG....          |
| JPG       | FF D8 FF E0                 | ....              |
| GIF       | 47 49 46 38 39 61           | GIF89a            |
| PDF       | 25 50 44 46                 | %PDF              |
| ZIP       | 50 4B 03 04                 | PK..              |
| RAR       | 52 61 72 21 1A 07           | Rar!...           |
| ELF       | 7F 45 4C 46                 | .ELF (Linux Exec) |

---

## Command Line Basics

### Initial File Analysis
* Identify file type: `file filename`
* Extract readable text: `strings filename`
* Check metadata: `exiftool filename`
* Calculate MD5 hash: `md5sum filename`

### Linux Navigation and Search
* List all files (including hidden): `ls -la`
* Search for a file by name: `find . -name "flag*"`
* Search for text inside files: `grep -r "CTF{" .`
* Read file content: `cat filename` or `less filename`

---

## Common Encoding Formats

Use CyberChef to convert these formats:

* Base64: Uses A-Z, a-z, 0-9, / and +. Often ends with padding (=).
* Hexadecimal: Uses 0-9 and A-F. Represents bytes.
* Binary: Consists of 0s and 1s.
* ROT13: A simple shift cipher where each letter is moved 13 positions in the alphabet.

---

## Documentation and Learning

* CTF101: https://ctf101.org/ (Basic concepts for every category)
* HackTricks: https://book.hacktricks.xyz/ (Advanced techniques and checklists)
* GTFOBins: https://gtfobins.github.io/ (Linux privilege escalation reference)
* PayloadsAllTheThings: https://github.com/swisskyrepo/PayloadsAllTheThings

---

## Notes for Success
1. Always check robots.txt on web challenges.
2. View the page source code (Ctrl+U) to find hidden comments.
3. If a file does not open, check its Magic Bytes in a Hex Editor.
4. Keep track of your steps; writing down what you tried is as important as finding the flag.
