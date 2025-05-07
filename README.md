# Using-Wireshark---analyzing-web-browser-artifacts-email-header-analysis
## AIM:
To use Wireshark to analyze web browser activities and inspect email headers from captured network traffic.

## DESIGN STEPS:
### Step 1:
Launch Wireshark and start capturing traffic on the appropriate network interface.

### Step 2:
Use filters like http, dns, or tcp.port == 80 to monitor web browser artifacts such as visited URLs, cookies, and user-agent strings.

### Step 3:
Apply filters like smtp, pop, or imap to locate and analyze email header details (e.g., sender, receiver, subject) from email communications.

## PROGRAM:
Wireshark Web and Email Traffic Filtering Steps

## OUTPUT:
# A. Capturing Traffic in Wireshark

1.Open Wireshark and start capturing on the active interface (Wi- Fi/Ethernet).

2.Perform activities like opening a website or sending an email through a client (e.g., Gmail via browser or Thunderbird).

3.Stop the capture once done.
![440248994-6a654494-4cde-405f-a45b-9505ea0e6ea5](https://github.com/user-attachments/assets/fc2a89e5-8736-433a-a14f-2e722d57919f)


Analyze DNS Queries: o Filter: dns

Reveal domains the browser tried to resolve.
![440249060-0650a35c-dd56-4231-9800-7b09045f2588](https://github.com/user-attachments/assets/0ac92e2d-99f1-416f-a071-7540d79df433)


Email Header Analysis

# Apply relevant filters:
 For POP3: tcp.port == 110

For SMTP: tcp.port == 25 or 587

 For IMAP: tcp.port == 143 or 993

# Locate email data:
 Look for SMTP packets to see sender/receiver email addresses.

 Use "Follow TCP Stream" to view the full email headers and body if unencrypted.

# Extract Email Header Fields:

 Analyze From, To, Subject, Date, Message-ID, and relay servers used in sending the email.
![440249188-c0c6d519-cc46-4433-88af-c8f265a3d1a6](https://github.com/user-attachments/assets/f86be8ff-0cfe-4dc7-9161-ffc8ec00f037)

![440249205-3c7ffbef-51ed-495e-803b-1f137c32c5c2](https://github.com/user-attachments/assets/e7792681-2150-4759-9ab6-a9b5cdc336bc)


![440249215-c3cb3788-34f7-45ba-a318-4a51b9be027a](https://github.com/user-attachments/assets/523a935e-8ce3-46e2-98f1-6b37399797a9)



## RESULT:
Web browser artifacts and email headers were successfully analyzed using Wireshark.

