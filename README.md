# Subdomain_Enumeration
Overview
The Subdomain Enumeration Tool is a Python-based utility designed to identify subdomains of a specified domain using DNS lookups and certificate transparency logs from crt.sh. This tool is useful for security researchers and penetration testers seeking to gather information about a target domain.

Features
Fetch subdomains from crt.sh.
Generate common subdomains.
Resolve subdomains to IP addresses.
Save results to a specified output file.
Installation
Prerequisites
Make sure you have Python 3 installed on your system. You can download it from python.org.

Required Libraries
You need to install the following Python libraries:

pip install aiohttp dnspython requests pyfiglet colorama

git clone https://github.com/abhinavRajput1/Subdomain_Enumeration.git

cd Sub-Enum
Usage
Bash Script
The easiest way to use this tool is through the provided Bash script.

Running the Bash Script
./subenum.sh -d <domain> [-o <output-file>]
-d <domain>: Specify a single domain to enumerate subdomains for.
-dL <domain-list>: Specify a file containing a list of domains to enumerate.
-o <output-file>: Specify a file to store resolved subdomains.
-h: Display help information.
Example:

./subenum.sh -d example.com -o output.txt
To enumerate a list of domains from a file:

./subenum.sh -dL domains.txt -o output.txt
Python Script
You can also run the Python script directly:

python3 subenum.py -d <domain> [-o <output-file>]
Example:

python3 subenum.py -d example.com -o output.txt
Output
The tool will print resolved subdomains to the console and save the results to the specified output file. If no subdomains are resolved, it will notify the user accordingly.

Example Output
Resolved Subdomains:
www.example.com: 192.0.2.1, 192.0.2.2
api.example.com: 192.0.2.3
Contributing
Contributions are welcome! If you have suggestions for improvements or new features, feel free to open an issue or submit a pull request.

Acknowledgments
crt.sh for providing certificate transparency logs.
dnspython for DNS queries.
aiohttp for asynchronous HTTP requests.
