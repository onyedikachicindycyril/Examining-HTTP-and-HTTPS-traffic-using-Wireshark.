# Examining-HTTP-and-HTTPS-traffic-using-Wireshark.
Examining HTTP and HTTPS traffic using Wireshark is crucial for troubleshooting web applications, detecting security threats like unencrypted data transmission, and optimizing network performance. It allows for packet capture, protocol dissection, and filtering, providing valuable insights into network behavior and potential issues.
Wireshark is a powerful network protocol analyzer used to inspect traffic in real-time. When analyzing HTTP and HTTPS traffic, it allows for the observation of both unencrypted and encrypted communication between clients and servers
1. Capturing Traffic
To begin analyzing HTTP or HTTPS traffic, follow these steps:
Step 1: Install Wireshark: Ensure that Wireshark is properly installed on the system intended for traffic capture.
 
Step 2: Start Capture: Launch Wireshark, select the appropriate network interface (e.g., Ethernet or Wi-Fi), and initiate a live capture session. 
 
Step 3: Generate Traffic: Access websites or use applications that produce HTTP or HTTPS requests.
 
Step 4: Stop Capture: Once a sufficient amount of data is collected, stop the capture session to begin analysis.
 
________________________________________
2. Examining HTTP Traffic
Step 1: Apply HTTP Filter: Use the display filter http in Wireshark’s filter bar to isolate HTTP packets.
 
Step 2: Analyze Plaintext Data:
HTTP traffic is unencrypted. Selecting an HTTP packet allows you to view detailed layers including:
•	HTTP headers (e.g., method, URI, user-agent)
•	Request or response body.
This means sensitive data (such as usernames or passwords transmitted over HTTP) can be viewed in clear text under the "Packet Details" and "Packet Bytes" panes.
 
________________________________________
3. Examining HTTPS Traffic
Step 1: Apply TLS/SSL Filter:
Use filters such as tls or ssl to display HTTPS-related packets.
 
Step 2: Observe Encrypted Communication:
HTTPS uses TLS (or SSL) to encrypt application data. In Wireshark, the encrypted contents appear as:
•	“Application Data” segments
•	Binary data in the packet bytes pane
The TLS handshake and certificate exchange processes are visible but the actual content is encrypted, preventing direct inspection.
