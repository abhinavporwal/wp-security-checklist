# WordPress Security Assessment Checklist

Here's the comprehensive WordPress Security Assessment Checklist with descriptions for each point:

## Note:
- **Ethical Practices**: Adhere to ethical hacking practices throughout the assessment to maintain trust and legality.
- **Tailoring the Checklist**: Customize the checklist to fit the specific needs and context of the website being tested for optimal results.
- **Staying Updated**: Keep up-to-date with the latest vulnerabilities and best practices in WordPress security to provide effective assessments.

<html><body><article id="120c971f-d199-80be-a32e-c7bb49592fe0" class="page sans"><header><h1 class="page-title"></h1><p class="page-description"></p></header><div class="page-body"><h3 id="120c971f-d199-802e-b69a-cf73d7e46075" class="">Complete Security Assessment Checklist for WordPress</h3><table id="120c971f-d199-8016-9c18-f2fc4fed58de" class="simple-table"><tbody><tr id="120c971f-d199-8025-b5ba-cf0f4ce2ce98"><td id="Nqx@" class=""><strong>Phase</strong></td><td id="aP=t" class=""><strong>Checklist Item</strong></td><td id="WfrY" class=""><strong>Commands/Steps</strong></td></tr><tr id="120c971f-d199-8089-8b7b-f5cc2282cb3d"><td id="Nqx@" class=""><strong>1. Pre-Engagement</strong></td><td id="aP=t" class=""><strong>Define Scope</strong></td><td id="WfrY" class="">- Document the scope of the engagement, including URLs and services to be tested.</td></tr><tr id="120c971f-d199-8066-aa42-ebc1923c3d73"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Obtain Permissions</strong></td><td id="WfrY" class="">- Ensure written permission from the website owner for testing.</td></tr><tr id="120c971f-d199-80af-932e-cc7132ce32f3"><td id="Nqx@" class=""><strong>2. Information Gathering</strong></td><td id="aP=t" class=""><strong>Whois Lookup</strong></td><td id="WfrY" class="">- Use <code>whois domain.com</code> to gather domain registration details.</td></tr><tr id="120c971f-d199-8072-8057-d01bc5e558de"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>DNS Enumeration</strong></td><td id="WfrY" class="">- Use <code>dig domain.com ANY</code> or <code>nslookup domain.com</code> to gather DNS records.</td></tr><tr id="120c971f-d199-8003-8263-e483548e7fd6"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Service Discovery</strong></td><td id="WfrY" class="">- Use <code>nmap -sS -sV -p- domain.com</code> to discover open ports and services.</td></tr><tr id="120c971f-d199-807a-8a0c-e05a7f695b1a"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>CMS Version</strong></td><td id="WfrY" class="">- Access <code>domain.com/readme.html</code> or <code>domain.com/wp-admin</code> to find the WordPress version.</td></tr><tr id="120c971f-d199-8070-9fea-f8407acbd4b5"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Plugins and Themes</strong></td><td id="WfrY" class="">- Use WPScan: <code>wpscan --url domain.com --enumerate p,t</code> to list active plugins and themes.</td></tr><tr id="120c971f-d199-800b-8bbb-edcd6d21bf98"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>User Enumeration</strong></td><td id="WfrY" class="">- Test for user enumeration via login pages, e.g., <code>curl -X POST -d &quot;log=admin&amp;pwd=admin&quot; domain.com/wp-login.php</code>.</td></tr><tr id="120c971f-d199-808b-ac11-c26044e2cc7d"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>OSINT Gathering</strong></td><td id="WfrY" class="">- Use tools like <code>Maltego</code>, <code>Recon-ng</code>, or <code>theHarvester</code> to gather information from public sources.</td></tr><tr id="120c971f-d199-8009-8f5e-fc9f677bdaea"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Check SSL/TLS Configuration</strong></td><td id="WfrY" class="">- Use <code>ssllabs.com</code> or <code>nmap --script ssl-enum-ciphers domain.com</code> to evaluate SSL/TLS configuration.</td></tr><tr id="120c971f-d199-80b9-bd7f-e508ba53da14"><td id="Nqx@" class=""><strong>3. Reconnaissance</strong></td><td id="aP=t" class=""><strong>Website Structure</strong></td><td id="WfrY" class="">- Manually map out the site or use tools like <code>Screaming Frog</code> or <code>Burp Suite</code> to crawl the website.</td></tr><tr id="120c971f-d199-8074-8ea7-c798ecd41916"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Identify Third-Party Services</strong></td><td id="WfrY" class="">- Check for integrations by inspecting the website’s source code or using tools like <code>BuiltWith</code>.</td></tr><tr id="120c971f-d199-807f-8b86-f8f6f5540969"><td id="Nqx@" class=""><strong>4. Vulnerability Scanning</strong></td><td id="aP=t" class=""><strong>Automated Scanning</strong></td><td id="WfrY" class="">- Use WPScan: <code>wpscan --url domain.com --api-token YOUR_API_TOKEN</code> for automated vulnerability scanning.</td></tr><tr id="120c971f-d199-80c9-bb3e-f0145d13a6f9"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Manual Testing</strong></td><td id="WfrY" class=""></td></tr><tr id="120c971f-d199-8048-ae89-c68356e8204f"><td id="Nqx@" class=""></td><td id="aP=t" class="">- <strong>Cross-Site Scripting (XSS)</strong></td><td id="WfrY" class="">- Test with payloads in forms, e.g., <code>&lt;script&gt;alert(&#x27;XSS&#x27;)&lt;/script&gt;</code>.</td></tr><tr id="120c971f-d199-8090-af32-df3ba9016748"><td id="Nqx@" class=""></td><td id="aP=t" class="">- <strong>SQL Injection</strong></td><td id="WfrY" class="">- Test with SQL payloads in input fields, e.g., <code>1&#x27; OR &#x27;1&#x27;=&#x27;1</code>.</td></tr><tr id="120c971f-d199-80de-aa30-c6a36107f627"><td id="Nqx@" class=""></td><td id="aP=t" class="">- <strong>File Inclusion Vulnerabilities</strong></td><td id="WfrY" class="">- Test for LFI with payloads like <code>../../etc/passwd</code>.</td></tr><tr id="120c971f-d199-8017-91f2-fc41e297a9e4"><td id="Nqx@" class=""></td><td id="aP=t" class="">- <strong>Cross-Site Request Forgery (CSRF)</strong></td><td id="WfrY" class="">- Analyze forms for missing CSRF tokens.</td></tr><tr id="120c971f-d199-807f-9601-e5a0fa263571"><td id="Nqx@" class=""></td><td id="aP=t" class="">- <strong>Authentication Flaws</strong></td><td id="WfrY" class="">- Use <code>hydra -l admin -P password_list.txt domain.com http-get /wp-login.php</code> for brute-force testing.</td></tr><tr id="120c971f-d199-80a2-beef-c0397602e588"><td id="Nqx@" class=""></td><td id="aP=t" class="">- <strong>Check for Security Headers</strong></td><td id="WfrY" class="">- Use <code>curl -I domain.com</code> to check for security headers (Content Security Policy, X-Content-Type-Options, etc.).</td></tr><tr id="120c971f-d199-8065-b8a6-d81d3649e2ef"><td id="Nqx@" class=""></td><td id="aP=t" class="">- <strong>Review File Permissions</strong></td><td id="WfrY" class="">- Check permissions on critical files and directories, e.g., <code>ls -la /path/to/wordpress/</code>.</td></tr><tr id="120c971f-d199-802f-9cdb-e7e11d3f03ea"><td id="Nqx@" class=""></td><td id="aP=t" class="">- <strong>Database Configuration Review</strong></td><td id="WfrY" class="">- Check for database security, e.g., ensure <code>wp-config.php</code> is not world-readable.</td></tr><tr id="120c971f-d199-808d-9bf6-e75778c58254"><td id="Nqx@" class=""></td><td id="aP=t" class="">- <strong>Check for XML-RPC Vulnerabilities</strong></td><td id="WfrY" class="">- Test <code>domain.com/xmlrpc.php</code> for vulnerabilities like DDoS amplification.</td></tr><tr id="120c971f-d199-8067-829d-c908dd5503c6"><td id="Nqx@" class=""><strong>5. Exploitation</strong></td><td id="aP=t" class=""><strong>Privilege Escalation</strong></td><td id="WfrY" class="">- If access is gained, attempt to elevate privileges via <code>/wp-admin/</code> or other admin areas.</td></tr><tr id="120c971f-d199-80ea-be01-ea76cb232e57"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Payload Delivery</strong></td><td id="WfrY" class="">- Test file upload functionalities, e.g., upload a PHP shell as an image.</td></tr><tr id="120c971f-d199-804e-b857-cf925d91367d"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Session Management</strong></td><td id="WfrY" class="">- Analyze cookies with tools like <code>Burp Suite</code> to check for secure flags.</td></tr><tr id="120c971f-d199-80c0-8380-de112d326ea0"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Social Engineering</strong></td><td id="WfrY" class="">- Test user awareness via phishing or social engineering techniques to assess overall security awareness.</td></tr><tr id="120c971f-d199-803e-8a3d-e13ac8c90854"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Plugin/Theme Vulnerabilities</strong></td><td id="WfrY" class="">- Manually exploit known vulnerabilities in outdated plugins/themes; check WPVulnDB for specific exploit examples.</td></tr><tr id="120c971f-d199-80e1-9ec1-f1f55d919b7f"><td id="Nqx@" class=""><strong>6. Post-Exploitation</strong></td><td id="aP=t" class=""><strong>Data Exfiltration</strong></td><td id="WfrY" class="">- Look for sensitive files, e.g., <code>curl domain.com/wp-config.php</code> to check for database credentials.</td></tr><tr id="120c971f-d199-8006-87ab-e97d500595a7"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Log Review</strong></td><td id="WfrY" class="">- Review server logs (e.g., <code>access.log</code>, <code>error.log</code>) for suspicious activities.</td></tr><tr id="120c971f-d199-8086-b78d-f6c603bde9ea"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Service Accounts Review</strong></td><td id="WfrY" class="">- Review user roles and permissions for unnecessary privileges.</td></tr><tr id="120c971f-d199-807c-a79f-c86291485aad"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Backup Configuration</strong></td><td id="WfrY" class="">- Check if backups are being stored securely and are not publicly accessible.</td></tr><tr id="120c971f-d199-8031-b123-c8b09f9ef4b8"><td id="Nqx@" class=""><strong>7. Reporting</strong></td><td id="aP=t" class=""><strong>Vulnerability Summary</strong></td><td id="WfrY" class="">- Compile findings into a report format, detailing vulnerabilities and their impacts.</td></tr><tr id="120c971f-d199-8007-a374-c9d7729de0de"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Steps to Reproduce</strong></td><td id="WfrY" class="">- Clearly document how to reproduce each vulnerability identified.</td></tr><tr id="120c971f-d199-8033-9a69-f0186224ceef"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Recommendations</strong></td><td id="WfrY" class="">- Provide detailed remediation steps for each issue found.</td></tr><tr id="120c971f-d199-805e-bafb-e37cd6c35147"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Visual Aids in Reporting</strong></td><td id="WfrY" class="">- Use screenshots and diagrams to visualize vulnerabilities and their impacts.</td></tr><tr id="120c971f-d199-807f-b0d5-fff1ab0e9811"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Compliance Checks</strong></td><td id="WfrY" class="">- Check for compliance with relevant standards (e.g., GDPR, PCI-DSS) and document findings.</td></tr><tr id="120c971f-d199-8091-8402-f0d6a4468560"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Executive Summary</strong></td><td id="WfrY" class="">- Summarize key findings and overall security posture for stakeholders.</td></tr><tr id="120c971f-d199-801f-9835-f29e129bfa3a"><td id="Nqx@" class=""><strong>8. Remediation</strong></td><td id="aP=t" class=""><strong>Patch Vulnerabilities</strong></td><td id="WfrY" class="">- Work with the development team to apply patches and updates.</td></tr><tr id="120c971f-d199-8050-916b-ce3054b77096"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Harden WordPress</strong></td><td id="WfrY" class="">- Implement best practices, e.g., update <code>wp-config.php</code> to secure settings, and disable directory listings.</td></tr><tr id="120c971f-d199-80c7-974e-e254811e7569"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Training and Awareness</strong></td><td id="WfrY" class="">- Recommend security training for website administrators and content creators.</td></tr><tr id="120c971f-d199-80a9-8acd-d30ee81a3b59"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Change Management</strong></td><td id="WfrY" class="">- Implement a change management process for future updates to prevent re-introduction of vulnerabilities.</td></tr><tr id="120c971f-d199-80d3-ac9b-feae7a6e0203"><td id="Nqx@" class=""><strong>9. Follow-Up</strong></td><td id="aP=t" class=""><strong>Retesting</strong></td><td id="WfrY" class="">- Conduct follow-up tests using the same tools and techniques to verify issues are resolved.</td></tr><tr id="120c971f-d199-8026-a019-f1a67ec5de97"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Continuous Monitoring Setup</strong></td><td id="WfrY" class="">- Recommend setting up continuous monitoring tools (e.g., intrusion detection systems) for real-time alerts.</td></tr><tr id="120c971f-d199-8089-ad08-dee5e13863bc"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Regular Assessments</strong></td><td id="WfrY" class="">- Schedule periodic assessments using a calendar reminder.</td></tr><tr id="120c971f-d199-80b1-ad43-dfab0f4ae8b5"><td id="Nqx@" class=""><strong>10. Tools and Resources</strong></td><td id="aP=t" class=""><strong>Tools for Scanning</strong></td><td id="WfrY" class="">- WPScan, Burp Suite, Acunetix, OWASP ZAP.</td></tr><tr id="120c971f-d199-8085-831f-d2d615d23d55"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Plugins for Security</strong></td><td id="WfrY" class="">- Wordfence, Sucuri Security, iThemes Security.</td></tr><tr id="120c971f-d199-8039-86e2-ccf85c8e6555"><td id="Nqx@" class=""></td><td id="aP=t" class=""><strong>Documentation</strong></td><td id="WfrY" class="">- Refer to OWASP Top Ten, WordPress Codex on Security.</td></tr></tbody></table></div></article><span class="sans" style="font-size:14px;padding-top:2em"></span></body></html>
