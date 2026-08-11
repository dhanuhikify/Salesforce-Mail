# Salesforce Outbound Email via Apex

This repository contains a simple, lightweight Apex script to send a single outbound email from Salesforce using the `Messaging.SingleEmailMessage` class. It is ideal for testing email deliverability and learning Apex scripting via the Developer Console.




## 💻 Apex Source Code

You can copy and paste the following snippet directly into your environment:
apex
// 1. Initialize the email object
Messaging.SingleEmailMessage email = new Messaging.SingleEmailMessage();

// 2. Set your target recipient email address
String[] toAddresses = new String[] {'mbpraneeth03@gmail.com'};
email.setToAddresses(toAddresses);

// 3. Set the Subject and Body of the email
email.setSubject('Hello from Salesforce Developer Console!');
email.setPlainTextBody('Success! This email was sent using Apex code in the Developer Console.');

// 4. Send the email
Messaging.sendEmail(new Messaging.SingleEmailMessage[] { email });

// 5. Print a confirmation message to your logs
System.debug('🚀 Email command sent to Salesforce servers!');
```

---

## 🚀 Step-by-Step Execution Guide

Follow these steps to run the code using the Salesforce Developer Console:

### Step 1: Open the Developer Console
Click the **Gear Icon** ⚙️ in the top-right corner of your Salesforce lightning homepage and select **Developer Console**.

### Step 2: Open the Execute Anonymous Window
In the Developer Console menu bar, click on **Debug** and choose **Open Execute Anonymous Window** (or press `Ctrl + E` on Windows / `Cmd + E` on Mac).

### Step 3: Paste and Modify Code
Clear any existing text in the window, paste the Apex code from this README, and update the `'mbpraneeth03@gmail.com'` string to your preferred testing email address if needed.

### Step 4: Execute the Script
Check the box next to **Open Log** in the bottom right corner of the execution popup window, then click the **Execute** button.

### Step 5: Verify the Logs
Once the log opens, check the **Debug Only** checkbox filter at the bottom of the log viewer. You should see your custom rocket message:
`USER_DEBUG|[14]|DEBUG|🚀 Email command sent to Salesforce servers!`

### Step 6: Check Your Inbox
Open your email client. Remember to check your **Spam/Junk** folder if the message does not appear in your primary inbox within a few minutes.

