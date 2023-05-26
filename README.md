<h1> Report </h1>

CS-2124 Gobuster Scanner

<h2>Introduction</h2>

This report provides a detailed analysis of the CS-2124 Network Scanning Tool, which comprises a port scanner and a web directory scanner. The tool is designed to assist in network security assessments by identifying open ports and accessible directories on a target host. This report explores the functionality, usage, and outcomes of the tool.


<h2>1. Tool Overview</h2>

The CS-2124 Network Scanning Tool is a Python-based application that employs the nmap and requests packages for port scanning and web directory scanning, respectively. It enables users to scan a specified target host for open ports and search for accessible directories using a provided wordlist file.

The main components of the tool are:

⦁	Port Scanner: Utilizes the nmap package to scan a target host for predefined ports.
⦁	Gobuster Scanner: Utilizes the requests package to scan a target host for accessible directories using a wordlist file.

Nmap ("Network Mapper") is an open source utility for network exploration and security verification. It was designed to quickly scan large networks, although it copes well with single targets. Nmap uses raw IP packets in an original way to determine which hosts are available on the network, which services (application name and version) they suggest which operating systems (and OS versions) they use, what types of packet filters/firewalls are used, and many more other characteristics. While Nmap is commonly used for security checks, many system administrators find it useful for common tasks such as monitoring network structure, managing service startup schedules, and keeping track of host or service hours.

Gobuster is a bruteforce tool:

URIs (directories and files) in websites;

DNS subdomains (with wildcard support);

Names of virtual hosts on the target web servers.

It is a command-line tool written in Go, it does not perform recursive bruteforce, allows you to bruteforce folders and several extensions at the same time, compiles on a variety of platforms, runs faster than interpreted scripts (such as Python), does not require a runtime environment.



<h2>2. Functionality</h2>

2.1 Port Scanning

The port scanning functionality of the tool allows users to identify open ports on a specified target host. The following steps are involved:

⦁	The tool prompts the user to enter the IP address of the target host to be scanned.

⦁	The port scanner initiates a scan on the specified target host using the nmap package.

⦁	The scan results include the host IP address and the status of each scanned port, indicating whether the port is open or closed.

2.2 Web Directory Scanning

The web directory scanning functionality helps users identify accessible directories on a target host using a wordlist file. The process is as follows:

⦁	The tool prompts the user to enter the IP address of the target host.

⦁	The tool reads the wordlist file, which contains a list of directory names to be scanned.

⦁	For each directory in the wordlist, the tool attempts to access the directory on the target host using the requests package.

⦁	If the directory is accessible and returns a status code of 200, it is considered found, and the tool displays the URL of the directory.

<h2>3. Usage</h2>

To utilize the CS-2124 Network Scanning Tool, follow the steps outlined below:

⦁	Ensure that Python is installed on your system.

⦁	Install the required packages by running the following commands:

⦁	pip install python-nmap to install the nmap package.

⦁	pip install requests to install the requests package.

⦁	Place the wordlist file, containing the directory names, in the same directory as the tool script.

⦁	Open the terminal or command prompt and navigate to the directory where the tool script is located.

⦁	Execute the script using the command python scanner.py.

⦁	When prompted, enter the IP address of the target host to be scanned.

⦁	The tool will conduct the port scan and display the results, including the status of each scanned port.

⦁	Following the port scan, the tool will perform the web directory scan using the provided wordlist file. It will display the URLs of the found directories.
 ![Image alt](https://github.com/vshigimoto/OS_Security/blob/main/2023-05-26%2022.59.51.jpg)
 
 ![Image alt](https://github.com/vshigimoto/OS_Security/blob/main/2023-05-26%2023.00.44.jpg)

 

<h2>4. Example Usage</h2>

Below is an example of the tool's usage and output:

 ![Image alt](https://github.com/vshigimoto/OS_Security/blob/main/2023-05-26%2023.03.37.jpg)
 
 ![Image alt](https://github.com/vshigimoto/OS_Security/blob/main/2023-05-26%2023.04.28.jpg)
 
 ![Image alt](https://github.com/vshigimoto/OS_Security/blob/main/2023-05-26%2023.40.27.jpg)
 
<h2>5. Conclusion</h2>
CS-2124 Gobuster Scannerl provides a straightforward and efficient solution for conducting port scans and web directory scans on a target host. By identifying open ports and accessible directories, the tool aids in assessing network security. It is important to note that the tool's usage should strictly adhere to legal and ethical guidelines, ensuring that scans are performed only on systems for which the user has proper authorization.

Overall, this tool serves as a valuable resource for individuals and organizations seeking to enhance their network security measures.

Sincerely, 

Mubarakov Amirkhan

Seytkazy Enlik

Zhumash Ayaulym

<3

