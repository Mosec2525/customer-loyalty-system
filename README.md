<div align="center">
  <img src="https://n8n.io/favicon.ico" width="80" alt="n8n logo" />
  <h1>🎁 Customer Loyalty & Retention System</h1>
  <p><strong>Automated purchase tracking, loyalty milestones, and re-engagement powered by n8n</strong></p>
</div>

---

## ⚡ Overview

**Customer Loyalty & Retention System** is an n8n workflow that transforms your post-purchase experience. It automatically tracks customer purchase behavior, rewards loyalty milestones, and proactively re-engages customers with personalized offers.

Instead of manually tracking who bought what and when, this workflow operates continuously in the background to ensure your customers feel valued and are nudged to purchase again at exactly the right time.

## 🎯 When to Use It

This workflow is perfect for:
- **E-commerce Stores:** Automatically reward customers on their 5th purchase to increase Customer Lifetime Value (LTV).
- **Subscription Services:** Send automated reminders right before a product is expected to run out (e.g., 30-day consumable supplies).
- **Retail Brands:** Send personalized birthday emails with exclusive discount codes to drive off-season traffic.

## 🏗️ Architecture & Features

- **🛒 Milestone Tracking:** Triggers upon every purchase to increment loyalty points and track total purchase volume.
- **🏆 Automated Rewards:** Uses conditional logic to instantly detect when a customer crosses a threshold (e.g., 5 purchases) and sends an immediate reward.
- **⏳ Smart Re-engagement:** Employs long-running Wait nodes (e.g., 30 days) to pause the customer journey and send a well-timed "Time to restock?" reminder email.
- **🎂 Daily Birthday Checker:** Features a secondary scheduled trigger that runs every morning at 8:00 AM, queries your database for birthdays, and sends automated celebratory offers.

## 🚀 How to Use It (Quickstart)

### 1. Prerequisites
- An active [n8n](https://n8n.io/) instance (cloud or self-hosted)
- Credentials for your chosen CRM or Database (e.g., PostgreSQL, HubSpot)
- Credentials for your Email/Messaging provider (e.g., Mailgun, SendGrid)

### 2. Installation
1. Clone this repository or download the `workflow.json` file.
2. In your n8n workspace, click **Add Workflow** -> **Import from File**.
3. Select the `workflow.json` file.

### 3. Configuration
1. **Purchase Trigger Setup:** Connect the initial Webhook to your e-commerce platform (e.g., Shopify, WooCommerce).
2. **Database Integration:** Replace the mock "Update CRM & Points" and "Fetch Birthdays" Set nodes with real database queries (e.g., Postgres nodes) that match your schema.
3. **Wait Node Timing:** The "Wait 30 Days" node is configured for 1 minute for testing. Adjust this to match your product's lifecycle (e.g., 30 days).

---

<div align="center">
  <i>Built with ❤️ for the e-commerce and automation community.</i><br>
  Created by <a href="https://github.com/Mosec2525">Mohammad Almashahreh</a>
</div>
