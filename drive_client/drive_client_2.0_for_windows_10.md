# SeaDrive 2.0 for Windows 10

SeaDrive 2.0 (and future versions) is redesigned with deeper integration to Windows 10 operating system. It supports Windows 10 1709 version (2017 Fall Update for Windows 10) and later versions. We recommend Windows 10 users to upgrade to SeaDrive 2.0 for more native virtual drive experience.

SeaDrive 2.0 is currently in Beta status. We'll mark it stable after we have more user feedbacks.

## Install and Access the Virtual Drive

You can download SeaDrive 2.0 from [official Seafile website](https://www.seafile.com/en/download/). After installation and logging into your Seafile account, SeaDrive will start downloading library and file lists from the server (just as in SeaDrive 1.0.x). It may take some time, depending on the number of files available in your seafile account. The download is progressive, so in the mean time you can already access some files in the virtual drive.

To access the virtual drive, just open Windows file explorer. There is a "seadrive" node in the navigation pane of Windows file explorer.

<img src="https://download.seafile.com/lib/a1d455d4-fbdb-4066-adb4-f8bbeee3743b/file/images/auto-upload/image-1584674198415.png?raw=1" width="692" height="null" />

## Accessing Files in the Virtual Drive

Libraries are grouped into 4 categories in the virtual drive: My Libraries, Shared with me, Shared with groups and Shared with all.

As you can see, the file status icons is more integrated into Windows file explorer. The icons are a bit different form version 1.0.

Files in the virtual are created as "placeholders" in the local file system. They may be in 3 states:

* **Placeholder file**: An empty representation of the file and can only be opened when there is network connection.
* **Full file**: The file has been downloaded and saved locally. Download is automatic when a placeholder file is opened for the first time. These files are available whenever you open SeaDrive regardless to network connections. The operating system may decide to clear a full file when more disk space is needed.
* **Pinned full file**: The file has been downloaded and saved locally. It is guaranteed to be available offline.

![](https://download.seafile.com/lib/a1d455d4-fbdb-4066-adb4-f8bbeee3743b/file/images/auto-upload/image-1584674764725.png?raw=1)

You can control which files or folder are cached locally. This can be changed from the context menu when you right click on a file or folder. Choose "Always keep on this device" when you want to pin a file or folder locally; choose "Free up space" when you want to clean the cache for a file or folder.

<img src="https://download.seafile.com/lib/a1d455d4-fbdb-4066-adb4-f8bbeee3743b/file/images/auto-upload/image-1584675088821.png?raw=1" width="463" height="null" />

In SeaDrive 1.0, cached files are not automatically updated when they're updated on the server. In SeaDrive 2.0, full and pinned files are automatically kept in sync with the server.

## File Download and Control

Whenever you open a placeholder file, the operating system will automatically start to download it. If the file may take some time to download, there will be a progress bar shown up in file explorer and you may cancel the download.

Sometimes a background application may try to download a file in the virtual drive (such as an Anti-Virus software). You will be notified by the operating system about this and you may choose to cancel the download or disallow the application from automatically downloading files in the future.

## Frequently Asked Questions

### Can I create, delete, rename libraries?

Yes. When you create, delete or rename library folders in the virtual drive, the operation will be reflected on the server. You can only create, delete, rename libraries under the "My Libraries" category. Creating, deleting or renaming libraries in other categories will be ignored.

### Can I create files or folders outside of a library folder?

Yes. But files created outside of a library folder will be ignored and **NOT **synced to the server. A new folder under the "My Libraries" folder will be handled as a new library.

### Can I access encrypted libraries?

Yes. By default, encrypted libraries are not synced and shown in the virtual drive. You need to manually choose which encrypted libraries to sync and enter the password. Just right click on the SeaDrive icon in the system tray area and choose "Show encrypted libraries". A windows will show up and you can choose to sync or unsync an encrypted library.

### Is it compatible to SeaDrive 1.0?

SeaDrive 2.0 will use any existing accounts and their metadata (stored under C:\\users\\username\\seadrive\\ folder). But it will not use the cached files from SeaDrive 1.0. So any locally cached files in 1.0 version will not be accessible in 2.0 version. You can start SeaDrive 1.0 again to upload the files to server or copy them out.

### How do I clean the cache?

You can manually choose which folders or files to be cached locally. If you find a folder consumes too much space, just choose to "Free up space" on that folder and all cached files in that folder will be cleaned. There is no need to set cache cleaning time and cache size limit as in SeaDrive 1.0. Because placeholders are just normal files created on your local disk, your cache size is only limited by the available disk space on your computer.
