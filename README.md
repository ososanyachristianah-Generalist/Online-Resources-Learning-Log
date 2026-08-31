# Online-Resources-Learning-Log
## Sharing what I learnt from YouTube,Chatgpt,Claude and Google AI 

#### YOUTUBE
#### VIDEO 1 - Incident Response to Phishing
What I learnt - The steps taken when a phishing email is reported, from triage to containment
Key takeaway - Speed matters, the faster a phishing report is handled the less damage it can do.

#### VIDEO 2 - Some terms & clarifications
What I learnt - Cleared up cybersecurity terms I kept seeing but didn't fully understand
#### VIDEO 3 - A great roadmap (Unix Guy)
What I learnt - A clear path for learning cybersecurity step by step
Key takeaway - Linux and networking fundamentals come before anything else.

#### GOOGLE AI & CLAUDE
#### TOPIC 1 - Clarifications
What I learnt - Used both to clarify terms and concepts I ran into while studying
#### TOPIC 2 - Installed Termux (terminal) on my android
What I learnt - Termux lets me run a Linux terminal on my phone
Key takeaway - I can practice basic Linux commands even without my laptop.

### CHATGPT

## Web Recon & Basic Vulnerability Assessment (ZeroBank Lab)

Started with directory enumeration using dirb to map out the application surface. Identified key endpoints including /login.html, /admin, /feedback.html, and /server-status.

Manually explored each route to understand functionality and data exposure. The application includes authentication, administrative access, and user input forms, making it a good target for basic testing.

Interacted with the feedback form using curl to simulate POST requests. Confirmed how the backend processes user input and observed response behavior.

Tested for XSS by injecting script payloads into input fields. The application properly escapes user input, indicating basic input sanitization is in place.

Discovered an exposed /server-status page leaking server details (Apache version, OpenSSL, worker activity). This is a clear case of information disclosure due to misconfiguration.

Accessed /admin without authentication and retrieved sensitive user data (credentials and SSNs). This indicates broken access control and is 
a critical issue.

Also observed that the application runs on outdated components, which could increase exposure to known vulnerabilities.

## Key Findings

Broken access control on /admin
Information disclosure via /server-status
Outdated server components
Proper handling of user input (XSS mitigated)

# Takeaway: 
Focused on understanding how the application works before testing it. Identified entry points, interacted with them directly, and analyzed responses to determine where controls fail and where they hold.
## Screenshots
<img width="720" height="1600" alt="Screenshot_2026-08-29-10-46-57-418_com android chrome" src="https://github.com/user-attachments/assets/e3969425-ffe2-4351-9aab-ed6c60fcd368" />
<img width="720" height="1600" alt="Screenshot_2026-08-29-10-39-39-367_com termux" src="https://github.com/user-attachments/assets/04c1f459-6dc6-417e-9553-849fd30a7f7c" />
<img width="720" height="1600" alt="Screenshot_2026-08-29-10-48-09-442_com android chrome" src="https://github.com/user-attachments/assets/32f0be67-ad4f-484f-abc3-d369f555dfc8" />
<img width="720" height="1600" alt="Screenshot_2026-08-29-11-57-12-302_com android chrome" src="https://github.com/user-attachments/assets/909eea71-73cb-4006-ae7f-cfb0542ea9e4" />
<img width="720" height="1600" alt="Screenshot_2026-08-29-11-57-07-120_com android chrome" src="https://github.com/user-attachments/assets/0653bdcb-74cf-4965-b8d1-0b40e122b7bc" />
<img width="720" height="1600" alt="Screenshot_2026-08-29-11-56-15-328_com android chrome" src="https://github.com/user-attachments/assets/344898e3-8f24-4087-8779-d47d35d490f0" />



