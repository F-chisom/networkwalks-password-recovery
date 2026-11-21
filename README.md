# networkwalks-password-recovery
Internship practical (Networkwalks, Week 3) demonstrating PDF password recovery via two routes: a browser-based dictionary attack and an offline John the Ripper attack against an extracted pdf2john hash.
PDF Password Recovery with JTR & Online Tools

Internship practical (Networkwalks Cybersecurity Program, Week 3 — W3-PM1 & W3-PM2) demonstrating two routes to recovering the password of an encrypted PDF file: a browser-based online workflow and an offline John the Ripper (JTR) workflow.

Overview

Two password-protected PDF files were issued as practice targets. The objective was to recover each file's password using hash-extraction and dictionary-attack tools, then document the process as a formal assessment report.

W3-PM1 — Networkwalks Free Tools: Extracted a crackable hash from the locked PDF using Networkwalks' Hash Calculator, then ran a dictionary attack against that hash using Networkwalks' Password Cracker (built-in 100-password list).
W3-PM2 — John the Ripper (JTR): Extracted a hash from a second locked PDF using Online HashCrack's PDF Hash Extractor, then cracked it offline in Kali Linux with John the Ripper using the rockyou.txt wordlist.
Tools Used
Tool	Purpose
Kali Linux	OS used to run John the Ripper and inspect wordlists
Networkwalks Hash Calculator	Extracts a crackable hash (pdf2john/hashcat-compatible) from a protected PDF
Networkwalks Password Cracker	Runs a dictionary attack against an extracted PDF hash
Online HashCrack — PDF Hash Extractor	Alternative browser-based hash extraction tool
John the Ripper (JTR)	Offline password-cracking tool
rockyou.txt	Common password wordlist used as the JTR dictionary
Results
File	Method	Password Recovered	Flag
My-Locked-PDF1.pdf	Networkwalks Hash Calculator + Password Cracker	password1	nw{networkwalks_flag1_jtr_270521_1}
My Locked PDF1.pdf	Online HashCrack extractor + John the Ripper (rockyou.txt)	good-luck	nw{cybersecurity_flag_captured_2608}

John the Ripper cracked the second hash in 21 seconds at roughly 42,810 passwords/second — a reminder of how quickly weak or common passwords fall once a hash is obtained.

Repository Contents
├── report/        # Full Password Recovery Assessment Report (.docx)
├── evidence/       # Screenshots documenting each step of both practicals
└── README.md
Key Takeaways
A PDF's encryption is only as strong as the password protecting it — strong AES encryption still falls quickly to a weak or dictionary password.
Hashes can be extracted from protected PDFs without any authentication, using free, widely available tools.
Offline cracking (JTR + rockyou.txt) is dramatically faster than online brute-force at scale, underscoring the value of long, random passphrases over short or common ones.
Disclaimer

All activities in this repository were performed only on practice files issued for this internship, for education and research purposes only. No unauthorized systems or files were accessed. Misuse of password-recovery or cracking techniques against systems or files you do not own, or do not have explicit written permission to test, is illegal in most jurisdictions even when no damage occurs.

Author

Jonathan Favour Chisom Cybersecurity Professional, Batch B084 — Networkwalks Academy LinkedIn
