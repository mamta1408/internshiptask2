 # Task 2: Phishing Email Analysis

## Objective
Identify phishing characteristics in a suspicious email sample.

## Tools Used
- Email client (e.g., Gmail)
- Online email header analyzers:
  - MXToolbox: https://mxtoolbox.com/EmailHeaders.aspx
  - Google Admin Toolbox: https://toolbox.googleapps.com/apps/messageheader/
  - IPVoid Email Header Analyzer: https://emailheader.org/


*Sample Phishing Email: "Account Verification Required – Action Needed"*

From: no-reply@support-google.com

Subject: [Action Required] Verify your Google Account to avoid suspension

Date: Tue, 5 Aug 2025 10:14:32 +0530

To: you@example.com

Dear Google User,

We noticed suspicious activity on your Google account that may indicate unauthorized access. For your protection, we’ve temporarily locked certain features until we can verify your identity.

What you need to do:

Please verify your account by clicking the button below. This will help us ensure your account remains secure and uninterrupted.

 Verify My Account Now

   This link is valid for the next 24 hours. Failure to verify within this time may result in temporary suspension of your Google services including Gmail, Drive, and YouTube access.

Need Help?

If you think this is a mistake or you did not request this, please visit our Help Center.

Thank you for choosing Google.

– The Google Security Team


## Red Flags Identified

### 1. Sender’s Email Address
- **Address:** no-reply@support-google.com
- This is not a valid Google domain. Legitimate Google emails use domains like `@google.com` or `@accounts.google.com`.
- The domain "support-google.com" is a lookalike used for deception.

---

### 2. Email Header Discrepancies
Use online analyzers to check:

- SPF/DKIM/DMARC: Failures indicate the sender is not authorized.
- Reply-To: May differ from the From address.
- Source IP: May not be associated with Google servers.

**Steps to Analyze Email Headers:**
1. In Gmail: Open the message, click the three dots, and select "Show original".
2. Copy the full email header.
3. Paste it into a header analysis tool.
4. Review SPF, DKIM, DMARC results and IP location.

---

### 3. Suspicious Links or Attachments
- Button text: "Verify My Account Now"
- Hovering over the button reveals: `http://secure-google-verification.com/xyz`
- Legitimate Google URLs always begin with `https://accounts.google.com/`

---

### 4. Urgent or Threatening Language
The email uses phrases like:
- "Action Required"
- "Avoid suspension"
- "Failure to verify within this time may result in suspension"

These are intended to create panic and pressure the user to act without thinking.

---

### 5. Mismatched or Misleading URLs
Example:

- Displayed link: `https://google.com/verify`
- Actual link: `http://verify-now.security-checks.io`

This kind of mismatch is a clear indicator of phishing.

---

### 6. Generic Greeting and Unusual Language
- The email begins with "Dear Google User" rather than a personalized greeting.
- Ends with "Thank you for choosing Google" — a phrase not commonly used by Google.

---

## Conclusion

The email shows multiple signs of phishing, including:

- Fake or spoofed sender address
- Suspicious links and misleading button URLs
- Use of urgency and scare tactics
- Lack of personalization
- Failed email authentication (SPF, DKIM, DMARC)

---

## Precautions to Avoid Phishing Attacks

1. **Check the Sender’s Address**  
   Ensure the domain is official (e.g., `@google.com`).

2. **Avoid Clicking Suspicious Links**  
   Hover over links to preview their destination. Type URLs directly when in doubt.

3. **Look for Personalization**  
   Legitimate services use your name, not "Dear User".

4. **Watch for Urgency or Threats**  
   Be cautious of emails pressuring you to act quickly.

5. **Enable Two-Factor Authentication (2FA)**  
   Adds an extra layer of protection.

6. **Keep Software Updated**  
   Regularly update your browser, OS, and antivirus tools.

7. **Never Share Passwords or OTPs**  
   No trusted company will ask for them via email.

8. **Report Phishing Emails**  
   In Gmail: Click the three dots and select "Report phishing".

9. **Use a Password Manager**  
   Helps manage strong passwords and can alert you to fake sites.

10. **Educate Yourself and Others**  
    Stay informed about new scams and help others recognize them.

---



