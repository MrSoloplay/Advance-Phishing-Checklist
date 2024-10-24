## Gophish Setup Checklist
This isn't a detailed guide—just the essentials. If you're here, you know the basics. Let's keep this simple and to the point.

- **Recommended Operating System**:
  - [ ] Linux (Preferred)
  - [ ] Windows (Optional)

- **Pre-requisites**:
  - [ ] Clone Gophish (Avoid pre-built binaries) [([Link](https://github.com/gophish/gophish))]
  - [ ] Remove IOCs [([Link](https://www.sprocketsecurity.com/resources/never-had-a-bad-day-phishing-how-to-set-up-gophish-to-evade-security-controls))]
  - [ ] Build Gophish [([Link](https://docs.getgophish.com/user-guide/installation))]

- **Initial Setup**:
  - [ ] Set up admin **User/Password**
  - [ ] Create the **Landing Page**
  - [ ] Create the **Email Template**
  - [ ] Setup **Sending Profile**: (Only focus on the important fields—skiping the general ones.)
    - Host:
      - [ ] `smtpout.secureserver.net:587` (For professional/non-Microsoft services)
      - [ ] `smtp.office365.com:587` (For Microsoft O365)
    - Username/Password from email service
    - Configure important **Email Headers**: These are key to avoiding detection.
      - [ ] `Read-Receipt-To`
      - [ ] `X-Mailer`
      - [ ] `X-MimeOLE`
      - [ ] `X-Priority`

- **Users & Campaigns**:
  - [ ] Add **Users** & **Groups**
  - [ ] Launch **Campaigns**

---

## **Bonus Section: Connect EC2 with Office 365**
If you're using Office 365 mail service with an EC2 instance, here’s how to connect it:
- [ ] Load the ExchangeOnlineManagement Module
  ```powershell
  Import-Module ExchangeOnlineManagement
  
- [ ] Replace abcd@blabla.com with your actual O365 account:
  ```powershell
  Connect-ExchangeOnline -UserPrincipalName abcd@blabla.com -ShowProgress $true

- [ ] Enable SMTP Authentication
  ```powershell    
  Set-TransportConfig -SmtpClientAuthenticationDisabled $false
