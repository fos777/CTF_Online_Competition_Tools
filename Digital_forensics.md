
# Digital forensics
## Decryption program
### dif-001 [BrowsingHistoryView](https://www.elcomsoft.com/efdd.html)
BrowsingHistoryView extracts browsing history information from all major Web browsers, including Firefox, Chrome, Opera, Internet Explorer, Microsoft Edge.
In order to extract the browsing history from external drive, you should use the 'Load history from the specified profiles folder' option or the 'Load history from the specified profile' option or the 'Load history from the specified custom folders' option or the 'Load history from the specified history files' option (In the 'Advanced Options' window).

**System Requirements**

This utility works on any version of Windows, starting from Windows 2000, and up to Windows 11. Both 32-bit and x64 systems are supported.
The following Web browsers are supported:

- Internet Explorer (Version 4.00 and greater)
- Mozilla Firefox (Version 3.00 and greater)
- Microsoft Edge
- Google Chrome
- Safari
- Opera (Version 15 or later, which is based on Chrome Web browser)
- Yandex Web browser
- Vivaldi Web browser
- SeaMonkey Web browser
- Brave Web browser

**Known Limitations and Problems**
- 'Visit Count' on Internet Explorer Web browser: The 'Visit Count' column is taken "as is" from the history file of Internet Explorer. Unfortunately, Internet Explorer tend to extremely bloat the 'Visit Count' number, which means that you cannot assume that the 'Visit Count' number represents the actual number of times that the user visited the specified Web site. This remark is only relevant for Internet Explorer. Other Web browsers count the number of visits properly, as far as I know.
- Limitations and problems with reading the history of IE10, IE11 and Microsoft Edge: Version 10 and 11 of Internet Explorer stores the history data inside WebCacheV01.dat, and this file is locked by the operating system most of the time, even when IE is closed.
In order to unlock the history database file, you should turn on the 'Automatically stop the cache task of IE10/IE11/Edge' option. If you use the 'Load history from remote computer' option - BrowsingHistoryView will stop the cache task of IE10/IE11/Edge on the specified remote system, so you'll be able to see the history of IE10/IE11/Edge remotely.

### dif-002 [CredentialsFileView](https://www.nirsoft.net/utils/credentials_file_view.html)
CredentialsFileView is a simple tool for Windows that decrypts and displays the passwords and other data stored inside Credentials files of Windows. You can use it to decrypt the Credentials data of your currently running system, as well as the Credentials data stored on external hard drive.

**Data Stored In Credentials Files**

Windows operating system stores the following information inside Credentials files:
- Login passwords of remote computers on your LAN.
- Passwords of mail accounts on exchange server (stored by Microsoft Outlook)
- Windows Live session information.
- Remote Desktop 6 user\password information.
- Internet Explorer 7.x and 8.x: passwords of password-protected Web sites ("Basic Authentication" or "Digest Access Authentication")
- Password of MSN Messenger / Windows Messenger accounts

**Credentials File Location**

You can find the Credentials files of Windows in the following locations:
- C:\Users\[User Profile]\AppData\Roaming\Microsoft\Credentials (Windows Vista and later)
- C:\Users\[User Profile]\AppData\Local\Microsoft\Credentials (Windows Vista and later)
- C:\Windows\system32\config\systemprofile\AppData\Local\Microsoft\Credentials (Windows 8 and later)
- C:\Documents and Settings\[User Profile]\Application Data\Microsoft\Credentials (Windows XP)
- C:\Documents and Settings\[User Profile]\Local Settings\Application Data\Microsoft\Credentials (Windows XP)

### dif-003 [VaultPasswordView](https://www.nirsoft.net/utils/vault_password_view.html)
VaultPasswordView decrypts and displays the passwords and other data stored inside 'Windows Vault'.
Windows operating system stores the following information inside 'Windows Vault':

Passwords of Internet Explorer 10.0/11.0 and Microsoft Edge running under Windows 8 or later. (Be aware that IE10/IE11 under Windows 7 doesn't use the Windows Vault to store passwords).
Login Information of Windows Mail application (Windows 8 or later).
In order to decrypt the data stored inside Windows Vault files on external drive, you have to know the login password of the user. In the 'Vault Decryption Options' window, you have to choose the 'Decrypt vault files of any system' option and then choose the drive letter of the external disk, click the 'Automatic Fill' button to automatically fill all other folders needed to decrypt the Windows Vault files.

### dif-004 [DataProtectionDecryptor](https://www.nirsoft.net/utils/dpapi_data_decryptor.html)
DataProtectionDecryptor is a powerful tool for Windows that allows you to decrypt passwords and other information encrypted by the DPAPI (Data Protection API) system of Windows operating system.
Here's some examples for passwords and other data encrypted with DPAPI:

Passwords of Microsoft Outlook accounts, stored in the Registry under HKEY_CURRENT_USER\Software\Microsoft\Windows NT\CurrentVersion\Windows Messaging Subsystem\Profiles or HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Outlook\Profiles or HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Outlook\Profiles (Depending on version of Outlook)
Credentials files of Windows (e.g: C:\Users\[User Profile]\AppData\Roaming\Microsoft\Credentials , C:\Users\[User Profile]\AppData\Local\Microsoft\Credentials )
Wireless network keys (Stored inside XML files under C:\ProgramData\Microsoft\Wlansvc\Profiles\Interfaces )
Passwords in some versions of Internet Explorer, stored in the following Registry key: HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\IntelliForms\Storage2
Passwords stored in the passwords file of Chrome Web browser ('Login Data' file in the profile of Chrome).
Encrypted cookies in Chrome Web browser ('Cookies' file in the profile of Chrome)
In order to decrypt the DAPI data stored on external drive, choose the 'Decrypt DPAPI data from external drive or another user' option in the 'DPAPI Decryption Options' window, choose the drive letter of the external drive and then click the 'Automatic Fill' button to automatically fill all other folders needed to decrypt the DPAPI data. You may also need to provide the logon password of the user if the password was used to decrypt the data.

DataProtectionDecryptor can read the DPAPI data for decryption from files or from text you type in hex-dump format (For example: 01 00 00 00 D0 8C 9D DF 01 15 D1 11 8C 7A 00 C0 4F C2 97 EB.... )
### dif-005 [WirelessKeyView](https://www.nirsoft.net/utils/wireless_key.html)
WirelessKeyView decrypts the wireless network keys stored by Windows operating system. In order to decrypt wireless keys stored on external drive, open the 'Advanced Options' window (F9), choose the 'Load the wireless keys from external instance of Windows installation' option and then fill the Windows directory and the Wlansvc Profiles folder on the external drive.
## EventLog
### dif-006 [FullEventLogView](https://www.nirsoft.net/utils/full_event_log_view.html)
FullEventLogView displays the details of all events from the event log of Windows (Including the event description). You can load multiple event log files and watch all of them in a single table. In order to watch events from external drive, you have to open the 'Choose Data Source' window (F7), select the 'Load events from external folder with log files' option and then type event logs folder (e.g: K:\Windows\system32\winevt\Logs )
## IE Log
### dif-007 [IEHistoryView](https://www.nirsoft.net/utils/iehv.html)
IEHistoryView extracts information from the history file (index.dat) of Internet Explorer. This history information includes the URLs that user visited, the Web site title, The number of times that this URL was visited (Hits column), and the last date/time that the Web site visit occured. The history file also contains a list of local files that the user opened with Internet Explorer (Usually .html and image files).

In order to use IEHistoryView to extract the IE history information from external drive:

- From user interface: Go to File->Select History Folder (Ctrl+H), and choose the history folder located in the external drive.
- From command-line: Use -folder command-line parameter to specify the history folder in the external disk, for example:
iehv.exe /stab "c:\temp\history.txt" -folder "J:\Documents and Settings\User01\Local Settings\History"

**Notice**:In order to insure that the date/time values are always accurate, the time zone settings in the computer you run IEHistoryView must be the same as the time zone settings of Windows in the inspected external hard-drive.
### dif-008 [IECacheView](https://www.nirsoft.net/utils/ie_cache_viewer.html)
IECacheView extracts information from the cache files (index.dat) of Internet Explorer. The information provided by IECacheView is somewhat similar to IEHistoryView. However, while the history file (IEHistoryView) stores only one record fro every Web page visit, the cache file stores multiple records for every Web page, including all images and other files loaded by the Web page.
In order to use IECacheView to extract the IE cache information from external drive:

From user interface: Go to File->Select Cache Folder (F9), and choose the cache folder ("Temporary Internet Files") located in the external drive.
From command-line: Use -folder command-line parameter to specify the cache folder in the external disk, for example:
IECacheView.exe -folder "C:\Documents and Settings\Administrator\Local Settings\Temporary Internet Files" /stab c:\temp\cache.txt
### dif-009 [IECookiesView](https://www.nirsoft.net/utils/iecookies.html)
IECookiesView extracts the content of all cookie files stored by Internet Explorer.
In order to use IECookiesView to extract the cookies information from external drive:

From user interface: Go to File->Select Cookies Folder (Ctrl+O) and type the cookies folder in the external drive
From command-line: Use /dir command-line parameter to specify the desired cookies folder, for example:
IECookiesView /dir "C:\Documents and Settings\Administrator\Cookies"
### dif-010 [IE PassView](https://www.nirsoft.net/utils/internet_explorer_password.html)
IE PassView extracts the Web site passwords stored by Internet Explorer.
IE PassView can also extract the Internet Explorer passwords from external hard-drive, but with the following limitations:

Only the new versions of Internet Explorer - 7.x and 8.x are supported.
Windows 7 is currently not supported.
You must know the logon password of Windows in order to retrieve the passwords, because the logon password is used to create the encryption key for IE passwords.
There are 2 ways to extract the IE passwords from external drive:

From user interface: Go to Options->Advanced Options (F8), choose 'Load passwords from the following user profile', and type the right profile folder and password of the external drive.
From command-line: Use /external parameter to specify the User Profile Path and the LogOn password of Windows, for example:
iepv.exe /external "C:\Documents and Settings\admin" "MyPassword"
## Firefox log
### dif-011 [MozillaCacheView](https://www.nirsoft.net/utils/mozilla_cache_viewer.html)
MozillaCacheView extracts the details of all cache files stored by Mozilla Firefox.
In order to extract the cache information of Firefox from external drive:

From user interface: Go to File->Select Cache Folder (F9) and choose or type the cache folder in the external drive.
From command-line: Use -folder command-line parameter to specify the cache folder in the external hard-drive, for example:
MozillaCacheView.exe -folder "C:\Documents and Settings\user01\Local Settings\Application Data\Mozilla\Firefox\Profiles\acf2c3u2.default\Cache" /stab c:\temp\cache.txt
### dif-012 [MozillaHistoryView](https://www.nirsoft.net/utils/mozilla_history_view.html)
MozillaHistoryView extracts the details of all browsing history stored by Mozilla Firefox. Starting from Mozilla Firefox 3, MozillaHistoryView requires that Firefox 3 will be installed on the computer that you run it, because it uses the sqlite3.dll library to read the SQLite history database of Firefox.
In order to extract the history information of Firefox from external drive:

From user interface: Go to File->Select History File (Ctrl+H) and type the Firefox history filename in the external drive.
From command-line: Use -file command-line parameter to specify the history file in the external drive. for example:
MozillaHistoryView.exe -file "C:\Documents and Settings\Administrator\Application Data\Mozilla\Profiles\test\p34kcd3y.slt\history.dat" /stab c:\temp\mz-history.txt
### dif-013 [MozillaCookiesView](https://www.nirsoft.net/utils/mzcv.html)
MozillaCookiesView extracts the content of all cookie files stored by Mozilla Firefox. Starting from Mozilla Firefox 3, MozillaCookiesView requires that Firefox 3 will be installed on the computer that you run it, because it uses the sqlite3.dll library to read the SQLite cookies database of Firefox.
In order to extract the cookies information of Firefox from external drive:

From user interface: Go to File->Select Cookies File /Profiles Folder, and type the cookies file in the external drive.
From command-line: Use -cookiesfile command-line parameter to specify the cookies file, for example:
mzcv.exe -cookiesfile "J:\Documents and Settings\Administrator\Application Data\Mozilla\Firefox\Profiles\1a2jjx2u.default\cookies.sqlite"
### dif-014 [PasswordFox](https://www.nirsoft.net/utils/passwordfox.html)
PasswordFox extracts the Web site passwords stored by Firefox Web browser. PasswordFox requires that Firefox will be installed on the computer that you run it, because it uses the decryption library of Firefox to decrypt the passwords.
In order to extract the passwords list of Firefox from external drive:

From user interface: Go to File->Select Folders, and choose the Profile folder path in the external drive.
From command-line: Use /profile command-line parameter to specify the profile folder in the external drive, for example:
PasswordFox.exe /profile "I:\Documents and Settings\User2\Application Data\Mozilla\Firefox\Profiles\1z7ccd2u.default"
## Chrome Log
### dif-015 [ChromeCacheView](https://www.nirsoft.net/utils/chrome_cache_view.html)
ChromeCacheView extracts the details of all cache files stored by Google Chrome Web browser.
In order to extract the cache information of Chrome Web browser from external drive:

From user interface: Go to File->Select Cache Folder (F9) and choose the Chrome cache folder in the external disk.
From command-line: Use -folder command-line parameter to specify the cache folder in the external drive, for example:
ChromeCacheView.exe -folder "P:\Documents and Settings\Administrator\Local Settings\Application Data\Google\Chrome\User Data\Default\Cache"
## Search Engines
### dif-016 [MyLastSearch](https://www.nirsoft.net/utils/my_last_search.html)
MyLastSearch utility scans the cache and history files of 4 Web browsers (IE, Firefox, Opera, and Chrome), and locate all search queries made with the most popular search engines (Google, Yahoo and MSN) and with popular social networking sites (Twitter, Facebook, MySpace). The search queries are displayed in a table with the following columns: Search Text, Search Engine, Search Time, Search Type (General, Video, Images), Web Browser, and the search URL.
MyLastSearch can extract the search queries data from external drive by using /loadfrom command-line parameter, for example:
MyLastSearch.exe /loadfrom "K:\Documents and Settings\Administrator\Local Settings\History" "K:\Documents and Settings\Administrator\Local Settings\Temporary Internet Files" "K:\Documents and Settings\Administrator\Application Data\Mozilla\Firefox\Profiles\dy18v2u5.default\history.dat" "K:\Documents and Settings\Administrator\Local Settings\Application Data\Mozilla\Firefox\Profiles\dy18v2u5.default\Cache"
## Windows Live Messenger 
### dif-017 [LiveContactsView](https://www.nirsoft.net/utils/live_messenger_contacts.html)
Extracts the contacts of Windows Live Messenger stored inside the contacts.edb file.
This utility has some limitations

Updated version of esent.dll (Server Database Storage Engine) must be installed on the system that you run this tool.
LiveContactsView cannot read the file if it's a contacts backup file or the file is corrupted from some reason.
In order to get the contacts list of Windows Live Messenger from external drive:

From user interface: Go to Options->Advanced Options (F9) and type/choose the contacts file from the external drive.
From command-line: Use /contactsfile parameter to specify the contacts file on the external drive, for example:
LiveContactsView.exe /contactsfile "J:\Documents and Settings\Administrator\Local Settings\Application Data\Microsoft\Windows Live Contacts\{12356999-1122-2227-c99d-13e02105a776}\DBStore\contacts.edb"
### dif-018 [WebBrowserPassView](https://www.nirsoft.net/utils/web_browser_password.html)
WebBrowserPassView is a password recovery tool that reveals the passwords stored by the following Web browsers: Internet Explorer (Version 4.0 - 8.0), Mozilla Firefox (All Versions), Google Chrome, and Opera. This tool can be used to recover your lost/forgotten password of any Website, including popular Web sites, like Facebook, Yahoo, Google, and GMail, as long as the password is stored by your Web Browser. After retrieving your lost passwords, you can save them into text/html/csv/xml file, by using the 'Save Selected Items' option (Ctrl+S).
