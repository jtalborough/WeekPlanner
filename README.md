# 📅 WeekPlanner

> 📧 An automated weekly PDF delivery system that sends customized PDF templates via email using GitHub Actions.

## 🔄 Workflow

The system operates on the following automated workflow:

### ⏰ Scheduling 
- 🤖 Runs automatically every Monday at 00:00 UTC
- 🎮 Can also be triggered manually through GitHub Actions

### 🚀 Process
1. 🔍 Locates the template PDF file in the repository
2. ✏️ Renames it with the current week number and date (e.g., "Week01_2025-01-12.pdf")
3. 🔒 Encodes the PDF for email attachment
4. 📨 Sends the email using SendGrid

## ⚙️ Setup Requirements

### 🔑 GitHub Repository Secrets
Required secrets in your repository settings:
- `TO_EMAIL`: 📮 Recipient email address
- `FROM_EMAIL`: 📤 Sender email address
- `SENDGRID_API_KEY`: 🔐 Your SendGrid API key

### 📄 PDF Template
- 📁 Place your PDF template in the repository root
- ✨ Name it with "Template" in the filename

## 🎯 Manual Trigger

Need to send right away? No problem!
1. 🖱️ Go to the Actions tab in your GitHub repository
2. 📋 Select "Weekly Email" workflow
3. ▶️ Click "Run workflow"

## 🛠️ Technical Details

The workflow is defined in `.github/workflows/WeeklySend.yml` and uses:
- 🔄 GitHub Actions for automation
- 📧 SendGrid API for email delivery
- 🔒 Base64 encoding for PDF attachment
- 🐧 Ubuntu latest as the runner

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

---
Made with ❤️ using GitHub Actions