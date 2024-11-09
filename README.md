## Mini Lab 8: Ready, SET, Go - Social-Engineer Toolkit (SET)
This mini-lab demonstrates how to use the Social-Engineer Toolkit (SET), an open-source Python tool for conducting penetration tests with a focus on social engineering tactics. In this lab, you’ll create a fake login page using SET, capture login credentials, and verify successful data capture.

# Overview
The goal of this lab is to simulate a credential harvesting attack using SET’s Website Attack Vector. You will learn to create a mock Google-like login page that stores submitted credentials.

# 🎯 Objectives
By the end of this lab, you will be able to:

# Run setoolkit and set up a credential harvesting webpage.
Capture and view credentials entered into the fake Google login form.
Resources
Kali SET Tool Documentation: Learn more about installing and configuring SET on Kali Linux.
TrustedSec SET Page: Overview of SET capabilities.
Linux Hostname Command: Learn more about using hostname to find local IP addresses.


# Lab Instructions
Prerequisites
Ensure that your hosts file on the Kali machine is set to default (e.g., no manual redirects). This lab requires proper DNS functionality for accessing real sites.

# Step 1: Set Up Credential Harvester in SET
Launch SET:

Open a terminal and type:
bash
Copy code
sudo setoolkit

Select Social-Engineering Attacks:

From the SET main menu, type 1 and press Enter.
Choose Website Attack Vectors:

At the next menu, select 2 for Website Attack Vectors.
Choose the Harvester Attack Method:

Select 3 for the Credential Harvester Attack.
Set Up the Fake Website:

Select 1 to use the Web Template option.
When prompted, enter your Kali Linux IP address as the POST back address:
bash
Copy code
hostname -I
Copy the second IP address in the list and paste it as the POST back address.
Select the Google Template:

Choose option 2 to create a mock Google login page.
Activate Credential Harvester:

SET will display a message indicating the credential harvester is active. Keep this terminal window open to view harvested data.

 # Step 2: Testing the Credential Harvester
Open the Firebrowser Browser:

In Kali, navigate to Applications -> Internet -> Firebrowser and open a new browser window.
Access the Fake Login Page:

In Firebrowser, type in the IP address you set earlier as the POST back address and press Enter.
Enter Credentials:

On the fake Google login page, enter a test email and password in the fields and click Sign In.
Verify Redirection:

You should be redirected to the actual Google Search Engine page.
Check Credential Capture:


# Return to the terminal window running SET and view the output to see the captured credentials.
## Important Notes
Ethical Use: This lab should only be conducted in a controlled, authorized environment, and with proper permissions. Unauthorized credential harvesting is illegal and punishable by law.
Learning Objective: This exercise is intended for educational purposes, demonstrating how social engineering attacks can occur to help you understand and defend against such methods.
License
The Social-Engineer Toolkit is developed by TrustedSec and distributed under an open-source license. For full licensing details, visit SET on GitHub.
