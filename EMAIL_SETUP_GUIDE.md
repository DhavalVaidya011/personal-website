# EmailJS Setup Guide for Contact Form

This guide will help you set up EmailJS so that messages from your contact form actually reach your email inbox.

## Step 1: Create EmailJS Account

1. Go to [EmailJS.com](https://www.emailjs.com/) and sign up for a free account
2. Verify your email address

## Step 2: Add Email Service

1. In your EmailJS dashboard, go to "Email Services"
2. Click "Add New Service"
3. Choose your email provider (Gmail, Outlook, etc.)
4. Follow the authentication steps
5. Note down your **Service ID** (you'll need this later)

## Step 3: Create Email Template

1. Go to "Email Templates" in your dashboard
2. Click "Create New Template"
3. Use this template content:

**Subject:**
```
New message from {{from_name}} - {{subject}}
```

**Body:**
```
Hello {{to_name}},

You have received a new message from your website contact form:

Name: {{from_name}}
Email: {{from_email}}
Subject: {{subject}}

Message:
{{message}}

---
This message was sent from your personal website contact form.
```

4. **IMPORTANT**: In the template settings, make sure to set the "To Email" field to your actual email address (e.g., your.email@gmail.com)
5. Save the template and note down your **Template ID**

## Step 4: Get Your Public Key

1. Go to "Account" → "API Keys" in your dashboard
2. Copy your **Public Key**

## Step 5: Update Your Code

Replace the placeholder values in your `script.js` file:

```javascript
// Line 58: Replace YOUR_PUBLIC_KEY with your actual public key
emailjs.init("YOUR_PUBLIC_KEY");

// Line 89: Replace YOUR_SERVICE_ID with your service ID
emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', templateParams)

// Line 89: Replace YOUR_TEMPLATE_ID with your template ID
emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', templateParams)
```

## Step 6: Test Your Form

1. Open your website
2. Fill out the contact form
3. Submit the form
4. Check your email inbox for the message

## Fixing the "422, recipients address is empty" Error

If you're getting this error, it means your EmailJS template doesn't have a recipient email address configured. Here's how to fix it:

1. Go to your EmailJS dashboard
2. Navigate to "Email Templates"
3. Click on your template to edit it
4. Look for the "To Email" field in the template settings
5. Enter your actual email address (e.g., your.email@gmail.com)
6. Save the template

**Alternative Method**: You can also add the recipient email in your JavaScript code:

```javascript
// Prepare email parameters
const templateParams = {
    from_name: name,
    from_email: email,
    subject: subject,
    message: message,
    to_name: 'Dhaval Kalpesh Vaidya',
    to_email: 'your.actual.email@gmail.com'  // Add this line
};
```

## Fixing the "Gmail_API: Request had insufficient authentication scopes" Error

If you're getting this error, it means your Gmail service needs to be re-authenticated with proper permissions. Here's how to fix it:

### Method 1: Re-authenticate Gmail Service
1. Go to your EmailJS dashboard
2. Navigate to "Email Services"
3. Find your Gmail service and click on it
4. Click "Edit" or "Re-authenticate"
5. Follow the Google OAuth process again
6. Make sure to grant all requested permissions

### Method 2: Use a Different Email Service (Recommended)
Gmail has strict security policies. Consider using one of these alternatives:

**Option A: Use EmailJS's Default SMTP Service**
1. In EmailJS dashboard, go to "Email Services"
2. Click "Add New Service"
3. Choose "EmailJS" (not Gmail)
4. This uses EmailJS's own SMTP servers and is more reliable

**Option B: Use Outlook/Hotmail**
1. In EmailJS dashboard, go to "Email Services"
2. Click "Add New Service"
3. Choose "Outlook"
4. Follow the authentication process

**Option C: Use Formspree (Simplest)**
See the Formspree section below for a completely different approach.

### Method 3: Update Your Code for New Service
If you change your email service, update your JavaScript:

```javascript
// Replace 'service_9opa8ql' with your new service ID
emailjs.send('YOUR_NEW_SERVICE_ID', 'template_7urvtcm', templateParams)
```

## Alternative: Using Formspree (Simpler Option)

If you prefer a simpler setup, you can use Formspree instead:

1. Go to [Formspree.io](https://formspree.io/) and create an account
2. Create a new form
3. Replace your form in `index.html` with:

```html
<form class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
    <div class="form-group">
        <input type="text" id="name" name="name" placeholder="Your Name" required>
    </div>
    <div class="form-group">
        <input type="email" id="email" name="email" placeholder="Your Email" required>
    </div>
    <div class="form-group">
        <input type="text" id="subject" name="subject" placeholder="Subject" required>
    </div>
    <div class="form-group">
        <textarea id="message" name="message" placeholder="Your Message" rows="5" required></textarea>
    </div>
    <button type="submit" class="btn btn-primary">Send Message</button>
</form>
```

4. Replace `YOUR_FORM_ID` with your actual Formspree form ID

## Security Notes

- Never expose your EmailJS private keys in client-side code
- The public key is safe to use in frontend code
- Consider adding CAPTCHA for additional spam protection
- Monitor your email service for any rate limiting

## Troubleshooting

- Check browser console for JavaScript errors
- Verify all IDs and keys are correct
- Ensure your email service is properly connected
- Test with a simple message first
- **For 422 errors**: Make sure your template has a recipient email address configured
- **For 412 errors**: Re-authenticate your email service or switch to EmailJS's default SMTP service

## Free Tier Limits

- EmailJS: 200 emails/month free
- Formspree: 50 submissions/month free

Both services offer paid plans for higher limits. 