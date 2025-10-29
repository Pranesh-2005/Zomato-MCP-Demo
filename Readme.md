# 🍴 Zomato MCP Server — Setup & Demo Guide

Zomato has officially launched an **MCP (Model Context Protocol) Server** — enabling AI assistants like **Claude** and **ChatGPT** to interact with real-world food ordering systems directly through chat.

This repository contains a **quick setup guide** and **demo videos** to help you configure and test the **Zomato MCP integration** inside **Claude Desktop**.

---

## 🚀 What You'll Learn

- 🔧 How to configure **Claude Desktop** to connect with Zomato's MCP Server  
- 🔎 Discover restaurants based on your location & preferences  
- 📒 Browse detailed menus with prices, ratings, and categories  
- 🛒 Add items to your cart and simulate food ordering  
- 💳 Experience secure QR-based payment simulation  

---

## ⚙️ Prerequisites

- Installed **Claude Desktop**
- Installed **Node.js** (verify with `node -v`)
- Basic understanding of **JSON configuration**

Download Node.js here: [https://nodejs.org](https://nodejs.org)

---

## 💬 Install in Claude Desktop

### Step 1: Open Developer Settings

1. Go to **Settings → Developer**
2. Click **Edit Config**

### Step 2: Add the Zomato MCP Server configuration

Paste the following inside your `claude_desktop_config.json` file:

```json
{
  "mcpServers": {
    "zomato-mcp": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "https://mcp-server.zomato.com/mcp"
      ]
    }
  }
}
```

### Step 3: Save and Restart

After saving the configuration, restart Claude Desktop to load the new MCP server.

---

## 📹 Demo Videos

### 🎥 1. Setting Up MCP in Claude Desktop
🔗 [Watch Setup Video](https://drive.google.com/file/d/15_m0KQEr6ft31U0svHa2HeMpzXpoMr4u/view?usp=drive_link)

### 🎥 2. Zomato MCP Demo — Restaurant Discovery to Payment
🔗 [Watch Demo Video](https://drive.google.com/file/d/15mTAkqkbzlfsSpA_98d2VYbI1oe88qbO/view?usp=drive_link)

---

## 🧠 How It Works

The Zomato MCP Server exposes APIs that Claude (or any MCP-compatible client) can call during a conversation.

This allows real-time restaurant lookup, menu retrieval, cart management, and simulated ordering — directly through chat commands.

For OAuth authentication, Zomato currently whitelists:
- `localhost`
- `chatgpt.com`

---

## 👨‍💻 Author

**Pranesh S**  
AI & Web Developer | MCP Integrator | B.Tech AIML

🌐 [GitHub](https://github.com/pranesh-2005) • 💼 [LinkedIn](https://linkedin.com/in/pranesh5264)

---

## ⭐ Support & Contribution

If this repo helped you set up or understand MCP integrations,  
🌟 **Star the repository** — it supports my work and helps others discover it!

Pull requests, improvements, and suggestions are welcome.