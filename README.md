# Online-Resources-Learning-Log
## Sharing what I learnt from YouTube,Claude and Google AI 

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
