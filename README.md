🚀 ReconStorm
Automated Web Reconnaissance Tool
By Abdallah Yasser

ReconStorm is an all-in-one automated reconnaissance script for bug bounty hunters and penetration testers. It takes a target domain and performs subdomain discovery, alive check, URL gathering, parameter discovery, and saves everything in organized text files for further testing.

⚙️ Features
🔍 Subdomain Enumeration using subfinder

🌐 Alive Subdomain Checking using httpx

📥 URL Collection from archives using gau

🕵️ Parameter Discovery using ParamSpider

📄 Clean and sorted output files

🛠 Requirements
Make sure you have the following tools installed globally on your system:

go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest
go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest
go install -v github.com/lc/gau/v2/cmd/gau@latest
pip install paramspider
Or clone and install them manually if needed.

📦 Installation

git clone https://github.com/YOUR_USERNAME/ReconStorm.git
cd ReconStorm
chmod +x reconstorm.sh
🚀 Usage

chmod +x reconS.sh
./reconS.sh

It will prompt you to enter the target domain and automatically run all the recon steps.
Results will be saved in the results/ folder.

## Usage Notes

- The tool performs several steps automatically, including gathering archived URLs using `gau`.
- **Note:** On large or historically active targets, `gau` may take several minutes to complete. This is normal as it fetches data from multiple sources (Wayback Machine, Common Crawl, etc.). Be patient for the best results.
- For faster but less comprehensive scanning, you can limit `gau` to use only the Wayback Machine by adding this flag in the script:

📁 Output Example
csharp
Copy
Edit
results/
├── subdomains.txt
├── alive.txt
├── urls.txt
└── params.txt
📝 License
This project is licensed under the MIT License.
Feel free to use, modify, and share with proper credit to Abdallah Yasser.
