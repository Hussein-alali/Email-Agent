# 📧 Email Agent - AI-Powered Email Management

An intelligent email assistant built with n8n that uses AI to manage your Gmail account through natural language conversations.

## 🌟 Features

- ✉️ **Send Emails** - Compose and send professional emails
- 📝 **Create Drafts** - Save emails as drafts for later
- 📥 **Read Emails** - Retrieve and search through your inbox
- 🏷️ **Label Management** - Organize emails with labels
- 👁️ **Mark as Unread** - Flag important emails
- 💬 **Reply to Emails** - Respond to messages intelligently
- 🤖 **Natural Language** - Just chat naturally, the AI handles the rest

---

## 🎯 How It Works

Simply chat with the assistant using natural language:
- "Send an email to john@example.com about tomorrow's meeting"
- "Get my last 5 emails from sarah@company.com"
- "Reply to the latest email from boss@work.com saying I'll be there"
- "Create a draft for client@example.com about the project update"

---

## 🚀 Quick Start

### Prerequisites

- n8n instance (cloud or self-hosted)
- Gmail account
- OpenAI API key (or Groq for free alternative)

### Installation

1. **Import the Workflow**
   ```
   - Download the Email Agent.json file
   - In n8n: Import from File → Select Email Agent.json
   ```

2. **Set Up Credentials**

   **Gmail:**
   - Click on any Gmail node
   - Add new credential
   - Authenticate with your Google account
   - Accept permissions

   **OpenAI API:**
   - Click "OpenAI Chat Model" node
   - Add your OpenAI API key
   - Or replace with Groq for free usage (see below)

3. **Activate the Workflow**
   - Toggle "Active" switch at the top
   - Click "Chat" button to start using

---

## 💡 Usage Examples

### Send Email
```
Send an email to ahmed@example.com with subject "Project Update" 
and message "The project is on track for Friday delivery"
```

### Get Emails
```
Get the last 10 emails
```

```
Show me emails from boss@company.com
```

### Create Draft
```
Create a draft email to client@example.com about the quarterly report
```

### Reply to Email
```
Get emails from john@example.com and reply to the latest one 
saying "Thanks for the update, I'll review by EOD"
```

### Label Email
```
Get the latest email from support@example.com and label it as "Important"
```

### Mark as Unread
```
Mark the latest email from team@company.com as unread
```

---

## 🌍 Multi-Language Support

The agent works in **Arabic** and **English**:

```
أرسل إيميل إلى ali@example.com بعنوان "اجتماع الغد" 
ونص "سنلتقي الساعة 3 عصرا"
```

---

## 🔧 Configuration

### Chat Interface

The workflow includes a **Chat Trigger** that provides an intuitive interface:
- No coding required
- Conversational interaction
- Message history
- Works on web and mobile

### Customization

Edit the **Email Agent** node to customize behavior:

```javascript
System Message:
"You are an email management assistant. 
All emails must be formatted professionally in HTML 
and signed off as 'Your Name'."
```

Change "Nate" to your preferred signature name.

---

## 💰 Using Free Alternatives

### Replace OpenAI with Groq (Free)

1. **Get Groq API Key**
   - Sign up at [console.groq.com](https://console.groq.com)
   - Create API Key (free, no credit card)

2. **In n8n:**
   - Delete "OpenAI Chat Model" node
   - Add "Groq Chat Model" node
   - Connect to "Email Agent" node
   - Add Groq credentials
   - Select model: `llama-3.1-70b-versatile`

**Why Groq?**
- ✅ Completely free
- ✅ Faster than OpenAI
- ✅ No credit card required
- ✅ Great Arabic support

---

## 🔐 Security & Privacy

- **Credentials**: Stored securely in n8n
- **Email Access**: Limited to actions you authorize
- **AI Processing**: Your emails are sent to OpenAI/Groq for processing
- **Best Practice**: Use with a dedicated email account for testing

---

## 📊 Workflow Structure

```
Chat Trigger
    ↓
Email Agent (AI)
    ↓
├─ Send Email
├─ Create Draft
├─ Get Emails
├─ Email Reply
├─ Get Labels
├─ Label Emails
└─ Mark Unread
    ↓
Success / Error Response
```

---

## 🐛 Troubleshooting

### "Insufficient Quota" Error
**Problem**: OpenAI account has no credits

**Solution**:
- Add credits to OpenAI account, OR
- Switch to Groq (free alternative)

### Gmail Authentication Failed
**Problem**: Can't connect to Gmail

**Solution**:
- Re-authenticate Gmail in credentials
- Check if "Less secure app access" is enabled
- Try using App-Specific Password

### Agent Not Responding
**Problem**: Chat doesn't work

**Solution**:
- Ensure workflow is Active
- Check OpenAI/Groq API key is valid
- Verify Chat Trigger webhook is enabled

### Email Not Sending
**Problem**: No emails being sent

**Solution**:
- Check Gmail credentials are connected to all Gmail nodes
- Verify email addresses are valid
- Check Gmail sending limits

---

## 🎨 Advanced Usage

### Integration with Other Workflows

You can call this agent from other workflows using **Execute Workflow** node:

```json
{
  "query": "Send email to user@example.com"
}
```

### Webhook API

Convert to API by replacing Chat Trigger with Webhook:

```bash
POST https://your-n8n.com/webhook/email-agent
Content-Type: application/json

{
  "query": "Get latest emails"
}
```

### Scheduled Tasks

Combine with Schedule Trigger for automated email management:
- Daily email summaries
- Auto-labeling
- Scheduled sending

---

## 📝 Notes

- All emails are formatted in **HTML** for professional appearance
- Default signature is "Nate" (customizable)
- Timestamps are automatically included
- Agent intelligently chains actions (e.g., gets emails before replying)

---

## 🤝 Contributing

Have ideas to improve this workflow?
- Add more Gmail features
- Improve AI prompts
- Add additional integrations
- Enhance error handling

---

## 📄 License

This workflow is provided as-is for educational and commercial use.

---

## 🆘 Support

Need help?
- Check n8n documentation: [docs.n8n.io](https://docs.n8n.io)
- Visit n8n community: [community.n8n.io](https://community.n8n.io)
- OpenAI docs: [platform.openai.com/docs](https://platform.openai.com/docs)
- Groq docs: [console.groq.com/docs](https://console.groq.com/docs)

---

## ⚡ Quick Tips

1. **Test Safely**: Use a test email address first
2. **Be Specific**: Clear commands = better results
3. **Check Drafts**: Review drafts before sending
4. **Use Groq**: Save money with free alternative
5. **Customize Prompts**: Adjust for your use case

---

Made with ❤️ using n8n and AI

**Star this workflow if you find it useful!** ⭐
