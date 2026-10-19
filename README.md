# CodeAlpha_ProjectName
A basic network sniffer built in Python with Scapy. It captures live
packets, analyzes their structure, and prints useful details.

## Features
- Captures live network traffic
- Shows timestamp, source IP, destination IP, protocol and ports
- Identifies TCP, UDP and ICMP packets
- Displays the first 50 bytes of each payload
- Prints a protocol summary at the end

## Requirements
- Python 3
- Scapy: `pip install scapy`
- Windows: install [Npcap](https://npcap.com) and run as Administrator
- Linux/Mac: run with `sudo`

## How to run
    python sniffer.py

## Sample output
(<img width="865" height="459" alt="snifffff3" src="https://github.com/user-attachments/assets/c81d5a4d-da8e-4035-be91-8cd2839a6ef4" />
)

<img width="923" height="482" alt="snifffff" src="https://github.com/user-attachments/assets/808e95d4-c401-493c-aa31-eaedd89e6f32" />

<img width="903" height="476" alt="snifffff 2" src="https://github.com/user-attachments/assets/df8d5883-4c5e-4365-8aff-3b2b9e7ecfdf" />


## What I learned
- Packets have layers: IP, then TCP/UDP/ICMP, then payload
- HTTPS and QUIC payloads are encrypted, so they look like random bytes
- ICMP (ping) payloads are unencrypted and readable

## Disclaimer
Use this only on networks you own or have permission to monitor.



            
              
              
              












              
              
              
              
              
              <img width="1600" height="900" alt="task2-banner-toc" src="https://github.com/user-attachments/assets/e6e2c4c8-960a-430e-ac0e-fdb55404291d" />

              
           
           
        


# 🎣 Phishing Awareness Training

Task 2 of my cybersecurity internship: a training module that teaches people how to recognize, resist and report phishing attacks.

**Estimated time:** about 15 minutes, with a quiz at the end.

## 📑 Table of Contents
1. [What is Phishing?](#what-is-phishing)
2. [Recognizing Phishing Emails](#1-recognizing-phishing-emails)
3. [Spotting Fake Websites](#2-spotting-fake-websites)
4. [Social Engineering Tactics](#3-social-engineering-tactics)
5. [Best Practices to Stay Safe](#4-best-practices-to-stay-safe)
6. [Real-World Examples](#5-real-world-examples)
7. [Quiz](#6-test-your-knowledge)

---

## What is Phishing?

Phishing is a type of **social engineering** attack in which an attacker pretends to be a trusted person or organization to trick you into revealing credentials, sending money, or installing malware. It usually arrives by email, but also by SMS (**smishing**), phone call (**vishing**), and chat or social media messages.

**Social engineering** is the psychological manipulation of people into giving up confidential information or performing actions that compromise security. It exploits human trust and emotion rather than technical flaws.

| Type | Description |
|------|-------------|
| **Mass phishing** | Generic emails sent to thousands of people |
| **Spear phishing** | Targeted at one person, using details about them |
| **Whaling / BEC** | Impersonating executives to trigger payments or data leaks |

---

## 1. Recognizing Phishing Emails

**Sample phishing email:**

> **From:** PayPal Support <service@paypa1-secure.co>
> **Subject:** URGENT: Your account will be suspended in 24 hours!
>
> Dear Customer,
>
> We noticed unusual activity. Your account have been limited. To restore access, click here to verify your password and card details immediately.
>
> **Attachment:** Account_Form.zip

**Red flags in this email:**

| Red flag | Why it is suspicious |
|----------|----------------------|
| Sender address | The display name says PayPal, but the real address belongs to an unrelated domain |
| Urgent subject | Urgency and threats make you act before you think |
| "Dear Customer" | Generic greeting; real providers usually use your name |
| Poor grammar | Odd phrasing is a common sign, although modern attacks can be polished |
| "Click here to verify" | The link text may hide a different destination; always hover first |
| Attachment (.zip) | Unexpected attachments can carry malware |

**Quick checklist:**
- ✅ Check the **actual sender address**, not just the display name
- ✅ Look for **urgency, fear or too-good-to-be-true offers**
- ✅ Hover over links to preview the real URL before clicking
- ✅ Be wary of unexpected attachments and requests for passwords, OTPs or payments

---

## 2. Spotting Fake Websites

Attackers clone login pages and host them on look-alike domains.

| Type | Example | Note |
|------|---------|------|
| ✅ Legitimate | `https://accounts.google.com` | Correct domain |
| ❌ Typosquatting | `https://accounts.g00gle.com` | Zeros replace letters |
| ❌ Subdomain trick | `https://google.com.login-verify.net` | The real domain is `login-verify.net` |
| ❌ Misleading path | `https://evil-site.xyz/paypal.com/login` | Brand name is only in the path |

**Tips:**
- Read the domain **right to left from the first single slash**: the part just before the TLD (.com, .net) is who owns the site.
- A padlock (HTTPS) only means the connection is encrypted. **Phishing sites can have it too.**
- Type known addresses yourself or use bookmarks instead of clicking email links.
- Watch for odd login prompts, missing pages, low-quality logos and unusual requests for extra data.

---

## 3. Social Engineering Tactics

Phishing works because it targets **human psychology**, not just technology.

| Tactic | Example |
|--------|---------|
| **Authority** | "This is the CEO / IT department / tax office." |
| **Urgency** | "Act now or your account will be closed." |
| **Fear** | "Suspicious login detected from another country." |
| **Greed or curiosity** | "You have won a prize", "See who viewed your profile" |
| **Trust and familiarity** | Messages that appear to come from a colleague or friend |
| **Pretexting** | A made-up scenario, such as a fake support call, to extract information |
| **Baiting** | Infected USB drives or free downloads left as bait |
| **Quid pro quo** | A "free service" in exchange for credentials or access |

> **Rule of thumb:** when a message pressures you to skip normal procedure, stop and verify through a separate, trusted channel.

---

## 4. Best Practices to Stay Safe

- 🛑 **Pause and verify:** call the sender using a known number, not one in the message.
- 🔐 **Enable MFA:** prefer authenticator apps or hardware keys over SMS codes.
- 🗝️ **Use a password manager:** it won't autofill on look-alike domains, which is a useful warning sign.
- 🔄 **Keep software updated:** patch browsers, OS and email clients.
- 🚫 **Never share OTPs:** no legitimate support agent will ask for them.
- 📣 **Report it:** use your organization's report button or tell the IT/security team, then delete the message.

**If you already clicked:**
1. Disconnect from the network if you opened an attachment.
2. Change the affected password immediately, and any others that reuse it.
3. Enable MFA, check account activity, and notify IT or your bank.

---

## 5. Real-World Examples

### Google and Facebook invoice scam (2013 to 2015)
A fraudster posed as a legitimate hardware supplier and sent convincing fake invoices, tricking both companies into paying over $100 million in total. Much of it was later recovered.
**Lesson:** verify payment-detail changes through a separate channel.

### RSA Security breach (2011)
Employees received a spear-phishing email with an Excel attachment titled "2011 Recruitment plan". Opening it exploited a vulnerability and gave attackers a foothold in the network.
**Lesson:** even security companies are targeted, so be careful with unexpected attachments.

### Twitter hack (2020)
Attackers used phone-based social engineering against employees to gain access to internal tools and took over high-profile accounts.
**Lesson:** vishing is real, so verify callers claiming to be IT.

---

## 6. Test Your Knowledge

**Q1.** You receive an email from "IT Support" asking you to verify your password through a link within 1 hour. What should you do?
- A. Click the link quickly to avoid lockout
- B. Reply with your password
- C. Ignore the link and contact IT through a known channel
- D. Forward it to colleagues as a warning

**Q2.** Which URL is most likely the real PayPal login page?
- A. `https://paypal.com.secure-login.net`
- B. `https://www.paypal.com/signin`
- C. `https://paypa1.com/login`
- D. `https://secure-paypal.xyz/signin`

**Q3.** A website shows a padlock icon. What does that guarantee?
- A. The site is legitimate
- B. The connection is encrypted, but not that the site is trustworthy
- C. The site is free of malware
- D. The owner has been verified by your bank

**Q4.** Which of these is a social engineering tactic?
- A. Port scanning
- B. Impersonating a senior executive to request an urgent transfer
- C. Installing a firewall
- D. Applying a software patch

**Q5.** You clicked a suspicious link and entered your password. What is the best first step?
- A. Do nothing, it was probably fine
- B. Change the password, enable MFA and report the incident
- C. Delete your email account
- D. Wait to see if anything happens

<details>
<summary>Answer key</summary>

1. **C**: urgency plus a credential request is a classic phishing pattern. Verify through a trusted channel.
2. **B**: the domain `paypal.com` comes right before the first single slash, with no look-alike characters.
3. **B**: HTTPS only encrypts traffic. Phishing sites commonly use it too.
4. **B**: impersonating authority to create pressure is classic social engineering (whaling or BEC).
5. **B**: change the password (and any reused ones), turn on MFA, and notify IT or the provider.

</details>

---

## 📁 Files in This Repository
- `phishing-awareness-training.html`: interactive version (open in any browser)
- `Phishing_Awareness_Training.pptx` / `.pdf`: presentation version

## 👤 Author
Kena Okhunkhun
