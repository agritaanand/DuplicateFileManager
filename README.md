# DuplicateFileManager
**DUPLICATE FILE MANAGER**
✅ Core Features:
1.	Folder Selection:
o	Users can browse and select a folder using FolderBrowserDialog.
2.	Duplicate File Detection:
o	Files are scanned in the selected folder.
o	Duplicates are detected using MD5 hash comparison (via GetFileHash method).
3.	ListView UI:
o	Displays file path, size, type, and status.
o	Differentiates between original and duplicate files.
o	Original files are highlighted in light green.
o	Supports checkbox selection for deleting files.
4.	Delete Functionality:
o	Deletes selected duplicate files.
o	Tracks deleted files using a Stack<string> for undo.
o	Also stores backup content using a Dictionary<string, string> to allow undoing deletions.
5.	Undo Feature:
o	Restores the last deleted file using its backed-up content.
o	Provides error handling if the file path no longer exists.
6.	Asynchronous Scanning:
o	btnScan_Click uses async Task.Run to keep the UI responsive while scanning.
7.	Error Handling:
o	Gracefully handles errors for scanning, deleting, and undoing with try-catch.
8.	Automatic UI Refresh:
o	After deletion or undo, the ListView is refreshed automatically using btnScan_Click

