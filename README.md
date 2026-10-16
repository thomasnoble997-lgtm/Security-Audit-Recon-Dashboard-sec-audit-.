# Security-Audit-Recon-Dashboard-sec-audit-.
This script automates a structured initial audit for a local machine or authorized host by combining multiple checks—port mapping, service identification, header checks, and log monitoring—into a single formatted HTML report.
🛡️ Interactive Security Audit & Recon Dashboard (sec-audit)

An interactive, automated Bash script that performs rapid security checks and target reconnaissance on local or remote systems. It generates a clean, standalone HTML dashboard report displaying reachability, HTTP security headers, and common open port statuses.

✨ Features

📊 Automated HTML Reporting: Automatically generates and saves findings in a styled, easy-to-read .html report.

💬 Interactive Terminal UI: Prompts for the target IP address or domain upon launch—no need to memorize command-line flags.

🌐 HTTP Security Header Audit: Automatically checks for critical security headers such as X-Frame-Options, HSTS, Content-Security-Policy, and X-Content-Type-Options.

🔌 Fast Common Port Check: Scans essential TCP service ports (21, 22, 80, 443, 8080, 3306) to identify running listening services.

⚡ Zero Heavy Dependencies: Built using standard Unix system utilities (bash, curl, ping).

📋 Requirements

Ensure the following common utilities are available on your Linux machine:

bash

curl

ping

🚀 Installation

Clone the repository:

git clone https://github.com/YOUR_USERNAME/sec-audit.git
cd sec-audit


Make the script executable:

chmod +x sec-audit


(Optional) Install system-wide as a command:

sudo mv sec-audit /usr/local/bin/sec-audit


💻 Usage

Run the script and enter the target IP or domain when prompted:

./sec-audit


Interactive Input Prompt:

========================================
       INTERACTIVE SECURITY AUDIT       
========================================
Enter target IP or domain (e.g., 127.0.0.1 or example.com): 127.0.0.1

[*] Starting Security Audit for target: 127.0.0.1
[*] Generating report: audit_report_20261016_114534.html
[*] Checking target reachability...
[*] Checking HTTP response headers...
[*] Scanning common services...
[+] Audit complete! Open 'audit_report_20261016_114534.html' in your web browser to view results.


👁️ How to View Your HTML Audit Report

Once the scan completes, open the output .html file in any web browser:

Using the terminal:

xdg-open audit_report_*.html


Or manually: Open your file manager, locate the generated file (e.g., audit_report_20261016_114534.html), and double-click it to open in Firefox, Chrome, or Brave.

📂 Project Structure

.
├── sec-audit                     # Interactive Bash automation script
├── audit_report_YYYYMMDD.html    # Generated HTML audit report
└── README.md                     # Project documentation


⚠️ Disclaimer

This tool is developed strictly for educational purposes, security auditing, and authorized system testing. Ensure you have proper authorization before scanning remote hosts or networks.
