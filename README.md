SentinelAI: AI-Powered Incident Response and Threat Analysis


SentinelAI is an automated cybersecurity solution designed to detect vulnerabilities, analyze system behavior, and recommend mitigation strategies using real-time forensic data. It combines memory, disk, and network forensics with Python automation for accurate and fast threat detection.


🎯Features

Live Forensic Analysis: Capture and analyze disk, memory, and network data using trusted forensic tools.
Python-Powered Threat Detection: Custom Python scripts parse and detect known anomalies or suspicious behavior.
Graphical Reporting: Generates graphs and tables that highlight IP traffic patterns and DNS queries.
Real-Time Incident Response: Suggests mitigation strategies immediately upon detecting threats.
Modular Design: Easily extendable for AI integration or compatibility with other forensic tools.


🛠️Tools & Technologies

FTK Imager – For live disk imaging and extraction
Volatility Framework – For memory dump analysis
Wireshark – For real-time network traffic capture
Python – For automated analysis, vulnerability detection, and report generation
PowerShell – For selective parsing and filtering (optional)


📁Project Structure

SentinelAI/
├── memory_analysis/
│ └── volatility_outputs.txt
├── network_analysis/
│ └── wireshark_logs.pcap
├── disk_analysis/
│ └── ftk_output.txt
├── analysis_engine/
│ ├── analyzer.py
│ └── graph_generator.py
├── reports/
│ ├── threat_report.txt
│ ├── ip_traffic_graph.png
│ └── dns_query_graph.png
└── README.md


🔄Workflow Overview

1. Data Collection:
   - Live memory dump using `winpmem` → analyzed via Volatility.
   - Disk snapshot using FTK Imager.
   - Network capture using Wireshark (`.pcap`).

2. Analysis:
   - Volatility plugins extract hidden processes, memory injections, and malware signatures.
   - Wireshark captures DNS, HTTP, and suspicious IP connections.
   - Python script reads and correlates all outputs.

3. Reporting:
   - Vulnerabilities are classified (Critical, Warning, Info).
   - Generates visual graphs + action recommendations.


📊Sample Results

Average detection time: ~13 seconds (from raw data to report)
Visuals: Bar graphs showing top IPs and frequent DNS queries
Output: Text-based incident reports with actionable solutions


⚙️Requirements

- Python 3.8+
- Volatility 3
- Wireshark
- FTK Imager
- Libraries:
  - `matplotlib`
  - `pandas`
  - `re`, `os`, `json`


Install required Python packages:
```bash
pip install matplotlib pandas





