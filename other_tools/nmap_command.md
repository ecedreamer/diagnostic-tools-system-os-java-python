Nmap (Network Mapper) is a powerful and widely used network scanning and security auditing tool. It is available for various operating systems, including Linux, Windows, and macOS. Nmap helps discover hosts on a network, identify open ports, determine service and version information, and perform various network-related tasks. Here's some information about Nmap and its command-line usage:

1. Command Syntax:
   ```
   nmap [Scan Type(s)] [Options] {target specification}
   ```

   - `[Scan Type(s)]`: Specifies the type of scan to perform, such as TCP SYN scan, UDP scan, OS detection, service/version detection, and more.
   - `[Options]`: Optional command-line options to customize the scan and output.
   - `{target specification}`: Specifies the target hosts, IP addresses, or network ranges to scan.

2. Commonly Used Scan Types:
   - `-sS`: TCP SYN scan (default), also known as stealth scan, to determine open ports.
   - `-sU`: UDP scan to discover open UDP ports.
   - `-sT`: TCP connect scan, which performs a full three-way handshake for each port.
   - `-sV`: Service and version detection, to determine the services running on open ports.
   - `-O`: Operating system detection, to identify the operating system of the target host.
   - `-A`: Aggressive scan, enabling OS detection, version detection, script scanning, and traceroute.

3. Commonly Used Options:
   - `-p <port(s)>`: Specifies the ports to scan (e.g., `-p 22` or `-p 1-100`).
   - `-F`: Fast scan mode, to scan only the most common ports.
   - `-oN <file>`: Saves the output in normal format to a file.
   - `-oX <file>`: Saves the output in XML format to a file.
   - `-v`: Increases verbosity, providing more detailed output.
   - `--script <script(s)>`: Runs specific Nmap scripts to perform targeted scanning or vulnerability checks.

4. Examples:
   - To perform a basic TCP SYN scan on a target host:
     ```
     nmap <target>
     ```

   - To perform a TCP SYN scan on multiple hosts in a network range:
     ```
     nmap <network>/24
     ```

   - To scan specific ports on a target host:
     ```
     nmap -p 80,443 <target>
     ```

   - To perform OS detection on a target host:
     ```
     nmap -O <target>
     ```

   - To perform an aggressive scan with script scanning:
     ```
     nmap -A <target>
     ```

   - To save the output in normal format to a file:
     ```
     nmap -oN output.txt <target>
     ```

5. Output Analysis:
   Nmap provides detailed information about discovered hosts, open ports, services, operating systems, and more. You can analyze this output to identify open ports, detect vulnerable services, understand network topology, and assess the security posture of the scanned hosts.

6. Additional Resources:
   - The official Nmap documentation provides comprehensive information about Nmap usage and options: [Nmap Reference Guide](https://nmap.org/book/man.html)
   - Nmap Scripting Engine (NSE) documentation covers the available scripts and their usage: [Nmap Scripting Engine Documentation](https://nmap.org/book/nse.html)

Nmap is a versatile tool used for network exploration, security auditing, and vulnerability assessment. It is important to use Nmap responsibly and ensure you have the necessary permissions before scanning networks or hosts.