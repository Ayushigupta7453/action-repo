# 🚀 action-repo

This repository is part of a GitHub monitoring system that tracks key repository activities using webhooks.

---

## 📌 Purpose

This repo is used to **trigger GitHub events** (`push`, `pull_request`, and `merge`) that are sent via webhook to a Flask server (`webhook-repo`) where the data is stored in MongoDB.

---

## ⚙️ Setup Instructions

1. Clone the repository:

```bash
git clone https://github.com/<your-username>/action-repo.git
cd action-repo
Make a code change and push to trigger a push event:
echo "hello" >> test.txt
git add .
git commit -m "Trigger push"
git push
To test pull_request or merge events:

Create a new branch

Push it to GitHub

Create a pull request from that branch to main or another base

Merge the pull request (to trigger merge)
📬 Webhook Configuration
The webhook is configured in this repo's Settings → Webhooks:

Payload URL: Provided by Ngrok and should point to your /webhook endpoint from the webhook-repo

Content type: application/json

Events to trigger:

✅ push

✅ pull_request

✅ merge_group


🧠 Author & Credit
This repository is part of the GitHub Webhook Monitoring System project.
Created by AYUSHI GUPTA

📂 Related Repositories
webhook-repo — backend endpoint that receives and stores GitHub events