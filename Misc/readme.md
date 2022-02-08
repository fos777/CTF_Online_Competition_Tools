# Thanks
[ctf-tools](https://github.com/ctf-wiki/ctf-tools/blob/master/docs/misc.md)
# WHAT'S THIS?
This folder mainly stores the software related to the MISC type of competition questions in CTF.
# MISC TOOLS
## Picture Steganography
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
## Compressed packet
### misc-008 [Ziperello](https://ziperello-2-1.softonic.cn/)
Ziperello recovers lost or forgotten passwords to zip archives.

Have you ever used encrypted zip archives? Perhaps you received such a file with important data from your business partner by e-mail or maybe you keep data in encrypted zip archives to prevent illegal access. If so, you've probably forgotten or lost a password more than once. This is not a problem any more! Just download Ziperello and recover the zip password easily.

### misc-009 [Advanced Rar Password Recovery download](https://www.portalprogramas.com/en/advanced-rar-password-recovery/)
Have you lost the password of one of your .rar files? Have you downloaded a really important file and it did not come with the password? You have he solution to a single click. Advanced RAR Password Recovery is an advanced tool that will achieve to recover the lost keys of any .rar file in just some seconds.

How does it work? It is based in an algorithm which tries more than 3 million combinations per minute, so after some minutes, it will have to find the correct password. Of course, that the speed of the program will depend on how long the key is. If it is less than 5 characters, it will only take some minutes, but if it has 8 characters combining letters and numbers, symbols and capital letters, the truth is that it can take almost a day to find it, but at the end it will find it!

This technique is called attack to dictionaries, and it has been tested and used in all kind of files, pages and emails (it is because of that that it is always recommended to have complicated passwords). But it has been developed especially for .RAR files.


### misc-010 [Advanced Zip Password Recovery](https://www.elcomsoft.com/help/en/azpr/)
```
Advanced ZIP Password Recovery (or AZPR) is a program to recover lost or forgotten passwords to ZIP archives (compressed files) created in programs like WinZip, PKZip etc. The key features of AZPR are:

·	The program has a convenient user interface  
·	The program is very fast: for ZIP, brute-force attack speed is up to fifteen million passwords per second on modern CPUs like Pentium 4 (Prescott)  
·	The program can work with archives containing only one encrypted file  
·	Archives created by various software packages are supported  
·	Self-extracting archives are supported  
·	The program is customizable: you can set the password length (or length range), the character set to be used to generate the passwords, and a couple of other options  
·	You can select the custom character set for brute-force attack (non-English characters are supported)  
·	Dictionary-based attack (with word mutations) is available  
·	The "brute-force with mask" attack is available  
·	Very fast known-plaintext attack is available  
·	You can interrupt the program at any time, and resume from the same point later  
·	The program can work in the background, using the CPU only when it is in idle state  
```
## Wireless password
### misc-011 [Elcomsoft Wireless Security Auditor](https://cn.elcomsoft.com/ewsa.html)
Elcomsoft Wireless Security Auditor is an all-in-one tool to help administrators verify how secure and how busy a company’s wireless network is. The tool will attempt to break into a secured Wi-Fi network by analyzing the wireless environment, sniffing Wi-Fi traffic and running an attack on the network’s WPA/WPA2-PSK password. Featuring patented cost-efficient GPU acceleration technologies and employing a range of smart attacks targeting the human factor, Elcomsoft Wireless Security Auditor runs a highly efficient accelerated attack on the network for a pre-defined amount of time in order to test how secure your wireless environment is.

## Editor
### misc-012 [010 Editor](https://www.sweetscape.com/download/010editor/)
010 Editor is a commercial hex editor and text editor for Microsoft Windows, Linux and macOS. Typically 010 Editor is used to edit text files, binary files, hard drives, processes, tagged data (e.g. XML, HTML), source code (e.g. C++, PHP, JavaScript), shell scripts (e.g. Bash, batch files), log files, etc.
## NTFS file stream
### misc-013 [Alternate Stream View](https://www.nirsoft.net/utils/alternate_data_streams.html)
AlternateStreamView is a small utility that allows you to scan your NTFS drive, and find all hidden alternate streams stored in the file system. After scanning and finding the alternate streams, you can extract these streams into the specified folder, delete unwanted streams, or save the streams list into text/html/csv/xml file.

## Audio steganography
### misc-014 [Audacity](https://www.audacityteam.org/)
Audacity is an easy-to-use, multi-track audio editor and recorder for Windows, macOS, GNU/Linux and other operating systems.Audacity is free, open source software.

### misc-015 [Detect DTMF Tones](http://dialabc.com/sound/detect/)
DialABC lets you find DTMF tones within audio clips. All you have to do is to upload an audio file to the dialabc web site using the form below. Our software then analyzes the audio recording and presents you with some statistics, a graph and a table showing you what DTMF tones are contained in the data and where.

eg.article:   
https://blog.csdn.net/offbye/article/details/7940848
