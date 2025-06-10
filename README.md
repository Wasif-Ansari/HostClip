Live Link: https://hostclip.vercel.app/

# HostClip

Welcome to the **HostClip** project repository! HostClip is a seamless clipboard-sharing tool that allows you to instantly send and receive text between devices using QR codes—no login, no friction. It’s designed for speed, privacy, and convenience, perfect for people who constantly switch between phone and desktop.

---

## Table of Contents

- [Introduction](#introduction)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Folder Structure](#folder-structure)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)
- [License](#license)

---

## Introduction

**HostClip** is a lightweight app that bridges your devices using a unique session-based QR code. You can paste any text on one device and instantly access it on another. Whether it’s a link, a note, or a snippet of code, HostClip makes cross-device sharing effortless and private.

---

## Key Features

- **Scan & Share Instantly:** Just scan a QR code to connect your mobile to the clipboard session.
- **Two-Way Clipboard Text Syncing:** View and edit text from either device.
- **Session-Based Privacy:** Each session is uniquely generated—no accounts required.
- **Cloud Storage:** Clipboard content is saved in the cloud (MongoDB) until refreshed or updated.
- **Save & Refresh Buttons:** Manual syncing to avoid unwanted overwrites.
- **Clean UI:** Built with Shadcn/UI and Tailwind for a modern experience.

---

## Tech Stack

- **Frontend:** Next.js, Tailwind CSS, Shadcn UI
- **Backend:** Next.js API Routes
- **Database:** MongoDB (with Mongoose)
- **Others:** QR Code Generator, NanoID for session IDs
- **Deployment:** Vercel

---

## Installation

To set up the project locally, follow these steps:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/Wasif-Ansari/HostClip.git
   ```

2. **Navigate to the Project Directory:**
   ```bash
   cd HostClip
   ```

3. **Install Dependencies:**
   ```bash
   npm install
   ```

4. **Set Up Environment Variables:**
   Create a `.env.local` file and add your MongoDB connection string:

   ```env
   MONGODB_URI=<your_mongodb_connection_uri>
   ```

5. **Run the App:**
   ```bash
   npm run dev
   ```

6. **Access the App:**
   Visit `http://localhost:3000` in your browser.

---

## Usage

1. Open HostClip on your computer.
2. Scan the QR code with your phone to connect.
3. Paste text from your device into the input field.
4. Click "Save" to sync the clipboard.
5. Refresh on the other device to see the updated content.

---

## Folder Structure

```
HostClip/
├── app/                  # Next.js app directory
│   ├── api/clip/         # API route for session creation and clipboard sync
│   └── session/[id]/     # Dynamic route for session-based views
│
├── lib/                  # Database connection and utility functions
├── models/               # Mongoose models
├── public/               # Static files
├── components/           # Reusable UI components
├── .env.local            # Environment variables (not committed)
├── package.json          # Dependencies and scripts
└── README.md             # Documentation
```

---

## Future Improvements

- Real-time sync using WebSockets
- Optional login and session history
- File sharing support (images, PDFs)
- Auto-expiry of old sessions for better privacy

---

## Contributing

Contributions are welcome! Here’s how you can help:

1. Fork the repo
2. Create a new branch: `git checkout -b feature-name`
3. Make your changes and commit: `git commit -m 'Add feature'`
4. Push to GitHub: `git push origin feature-name`
5. Open a Pull Request

---

## License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute this software as per the terms of the license.

---

Thanks for checking out HostClip! For questions or suggestions, feel free to open an issue on GitHub.
