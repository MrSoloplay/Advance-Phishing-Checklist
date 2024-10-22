# Phishing Simulation Checklist
**(Underdevelopment)**

This repository contains a comprehensive checklist to help security teams run **ethical phishing simulations**. Phishing simulations are essential to educating employees, improving organizational security posture, and identifying vulnerabilities before attackers do. It's like a cybersecurity fire drill – but with less smoke and more sneaky emails!

⚠️ **Caution**: This checklist is for **ethical use only**! If you're thinking about using this for nefarious purposes, just remember: karma’s like a phishing email – it’ll come back to bite you when you least expect it! 😎


## 1. Environment Setup

### 1.1 Cloud Machine
- **Recommended Operating System**: 
  - [ ] Linux (Preferred)
  - [ ] Windows (Optional)
- **Cloud Providers**:
  - [ ] AWS
  - [ ] Linode (Recommended)
  - [ ] DigitalOcean
  - [ ] Optional: GCP (Google Cloud Platform), Azure
- **Additional Setup**:
  - [ ] VPN/Proxy Setup for phishing server traffic obfuscation

--- 

## 2. Domain Setup

### 2.1 Domain Services
- [ ] Godaddy
- [ ] NameCheap
- [ ] Optional: Disposable Domains or Subdomains to avoid business domain blacklisting

### 2.2 DNS Records Setup (Necessary)
- [ ] SPF
- [ ] DMARC
- [ ] DKIM
- [ ] Optional: Custom DNS records (A, CNAME, MX) for specific email needs

--- 

## 3. Email Service Setup
- [ ] Microsoft 365 Email Essentials (Recommended)
- [ ] Professional Email (e.g., G Suite Business Emails)
- [ ] Optional: Self-Hosted Email Servers for more customization

---

## 4. Tools

### 4.1 Phishing Tools
- [ ] **[Gophish](https://getgophish.com/)**: Open-source phishing framework
- [ ] **[Evilginx](https://github.com/kgretzky/evilginx2)**: Advanced phishing platform
- [ ] **Microsoft Attack Simulator**: Its your choice. :)
- [ ] **PhishMe**: For realistic phishing templates
- [ ] **SET (Social Engineering Toolkit)**: For advanced attacks

---

## 5. Techniques

### 5.1 WhiteBox (Controlled Environment)
- [ ] Finalize the domain as per the simulation's requirements
- [ ] Domain and IP whitelisting on ESG (Email Security Gateway) to ensure phishing emails are not blocked
- [ ] Add the simulation email domain to the organization's SPAM policy and apply a transport rule to route phishing emails to target users
- [ ] Whitelist IP addresses of the phishing server in the organization's anti-spam policy
- [ ] Whitelist the domain on the Web Content Filter for landing page accessibility
- [ ] **Timeframe Consideration**: Run the simulation during low-activity business hours
- [ ] Obtain a predefined target list: Ensure employees are unaware of the simulation specifics
- [ ] Test email rendering across email clients (Outlook, Gmail, etc.)
- [ ] Align email templates with the tone of typical organizational emails
- [ ] Track opened emails, clicked links, and credential submissions to measure employee behavior

### 5.2 BlackBox (Simulated Attack)
- [ ] Finalize the domain based on the phishing scenario

#### 5.2.1 Information Gathering
- [ ] ESG (Email Security Gateway) 
- [ ] Identify internal platforms (e.g., Slack, HR portals) relevant to scenario development
- [ ] Identify target employees' roles, departments, and recent activities for scenario crafting
- [ ] Research common email formats to align with the organization’s standard communications

#### 5.2.2 Target List
- [ ] Collect employee emails (if not provided)
- [ ] Sources: LinkedIn, corporate website, business directories, etc. (e.g., Hunter.io, Phonebook.cz)

#### 5.2.3 Crafting Phishing Emails
- [ ] Select a theme that aligns with employees' business context (e.g., HR updates, IT maintenance)
- [ ] Embed dynamic content (personalized names, job titles, internal systems)
- [ ] Bypass spam filters by verifying email content and headers
- [ ] Avoid common techniques that might trigger anti-phishing engines

#### 5.2.4 Advanced Techniques (Bypass Included)
- [ ] **Multi-Stage Phishing**: Send follow-up emails 
- [ ] **Redirection with Multiple Landing Pages**: Increase complexity by using multiple pages
- [ ] **Microsoft Safe-Link/Sandbox Bypass**: Gather microsoft saflink IPs and add them to Apache server config list.

---

## 6. Post-Simulation Analysis
- [ ] **Employee Feedback**: Gather feedback via surveys to assess awareness and responses
- [ ] **Lessons Learned**: Share findings and security recommendations with the organization
- [ ] **Policy Review**: Update email and internet security policies based on outcomes
- [ ] **Future Simulations**: Plan recurring simulations to measure improvement over time
