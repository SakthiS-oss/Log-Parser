This is a solid, functional tool for log analysis and text processing. Below is a structured README.md that explains how it works, how to use it, and its core features.

Text & Log Analyzer
A lightweight, browser-based tool to upload, search, and extract data from text files or logs. This utility is designed for developers and system administrators who need to quickly parse log files, highlight specific patterns, or identify IP addresses without uploading sensitive data to a server.

🚀 Features
Local Processing: All file reading and searching happens in your browser. Your data never leaves your machine.

Search & Highlight: Search for specific strings with case-insensitive matching and visual highlighting.

IP Address Detection: Automatically identifies IPv4 addresses and maps out which lines they appear on.

Export Matches: Filter your file by a search term and export the resulting lines to a new .txt file.

Log Support: Specifically handles .txt and .log file extensions.

🛠️ Installation
Since this is a front-end application, no backend installation or npm install is required.

Clone or Download the repository.

Ensure the following files are in the same directory:

index.html

style.css

upload.js

Open index.html in any modern web browser (Chrome, Firefox, Edge, or Safari).

📖 How to Use
1. Upload a File
Click "Choose File" to select a .txt or .log file from your computer, then click "Upload and Display". The content will appear in the scrollable viewer.

2. Search Text
Enter a keyword or phrase in the search box and click "Search and Display Matches".

The app will filter the view to show only lines containing your term.

The search term will be highlighted in yellow.

A Match Counter will appear in the top-right corner.

3. Detect IP Addresses
Click the "Detect IP Addresses" button. The app will scan the document for IPv4 patterns and display:

The total count of unique IPs.

A list of each IP found.

The specific line numbers where each IP address was detected.

4. Export Results
After performing a search, click "Export Matches to Text File". This will download a new file named matched_text.txt containing only the filtered lines.

📝 Technical Details
Language: HTML5, CSS3, Vanilla JavaScript (ES6+).

RegEx: Uses /\b(?:\d{1,3}\.){3}\d{1,3}\b/g for robust IP detection.

FileReader API: Utilizes the native browser FileReader to handle asynchronous file loading.
