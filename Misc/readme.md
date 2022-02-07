# Thanks
[ctf-tools](https://github.com/ctf-wiki/ctf-tools/blob/master/docs/misc.md)
# WHAT'S THIS?
This folder mainly stores the software related to the MISC type of competition questions in CTF.
# MISC TOOLS
## Type 1
### misc-001 [stegsolve](https://github.com/eugenekolo/sec-tools/tree/master/stego/stegsolve/stegsolve)
Stegsolve is an immensly useful program for many steganography challenges, allowing you to go through dozens of color filters to try to uncover hidden text. 
### misc-002 [Stegdetect amd64 deb](https://github.com/abeluck/stegdetect)
UNMAINTAINED. USE AT OWN RISK. Stegdetect is an automated tool for detecting steganographic content in images.
### misc-003 [Steghide 0.5.1 win32](https://sourceforge.net/projects/steghide/files/steghide/0.5.1/)
install:
```bash
apt-get install steghide
```
how to use:
```
查看帮助  
steghide --help  
查看图片中嵌入的文件信息  
steghide info FILENAME  
隐藏文件  
steghide embed -cf COVERFILE -ef EMBEDFILE  
提取文件  
steghide extract -sf STEGOFILE  
```
### misc-004 [Outguess amd64 deb](https://ubuntu.pkgs.org/18.04/ubuntu-universe-amd64/outguess_0.2-8_amd64.deb.html)
OutGuess is a universal tool for steganography that allows the insertion
of hidden information into the redundant bits of data sources. The nature
of the data source is irrelevant to the core of OutGuess.
The program relies on data specific handlers that will extract redundant
bits and write them back after modification. The supported formats are
JPEG, PPM and PNM.  
This package is useful in forensics investigations and security actions.

Install Howto:
```
Update the package index:
# sudo apt-get update
Install outguess deb package:
# sudo apt-get install outguess
```
how to use
```
outguess [ -emt ] [ -r ] [ -k key ] [ -F [+-] ] [ -d datafile ] [ -s seed ] [ -i limit ] [-x maxkeys ] [ -p param ] [ inputfile [ outputfile ]]
```
### misc-005 [PNGCheck 2.3.0 win32](https://www.softpedia.com/get/Multimedia/Graphic/Graphic-Others/pngcheck.shtml)
pngcheck is a simple, easy to use application designed to verify the integrity of PNG, JNG and MNG files. The check is done by analyzing the internal 32-bit checksums and decompressing the image data, but the results are displayed in human-readable form.

The program comes with several advanced options that can provide in-depth information about the image files. Among these settings you can count printing contents of tEXt chunks, escape chars, the colorized output for ANSI terminals or print contents of PLTE, tRNS, hIST, sPLT and PPLT...

how to use:
```
pngcheck.exe - test PNG, JNG or MNG image files for corruption, and print size/type info.
pngsplit.exe - break a PNG, MNG or JNG image into constituent chunks (numbered for easy reassembly)
png-fix-IDAT-windowsize.exe - fix minor zlib-header breakage caused by libpng 1.2.6
```

### misc-006 [JPHS win32](http://www.scanwith.com/JPHS_for_Windows_download.htm)
https://github.com/h3xx/jphs

These programs make use of strong encryption technology.   
Possession, import or export may be illegal in your country.

They are licenced under GPL and you use them at your own risk.

how to use:
```
jphide  input-jpeg-file  output-jpeg-file  file-to-be-hidden

jpseek  input-jpeg-file  output-hidden-file
```
### misc-007 [OurSecret](https://www.downloadsource.net/1755402/our-secret-steganography/)
OurSecret is powerful data hider and protector which will put your private files in a secure location. Data transmissions are vital and became a necessity nowadays. Whether you share your private messages with your close friends, or business/commercial secrets with your partners, you must protect your confidential information from hackers, your boss, or your competitors. But we live in an insecure world where unwanted persons can access your personal information (like e-mails or personal documents) and often use it against you.

how to install :
```
How to install Our Secret on your Windows device:

Click on the Download button on our website. This will start the download from the website of the developer.
Once the Our Secret is downloaded click on it to start the setup process (assuming you are on a desktop computer).
When the installation is finished you should be able to see and run the program.
```





