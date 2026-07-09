# 📂 Stash — Modern Cloud Storage Solution

Stash is a sleek, secure, and feature-rich cloud storage and file management application. Built using **Next.js 15 (App Router)** and **Appwrite Cloud**, Stash provides users with a premium Google Drive-like experience for uploading, organizing, sharing, and managing files of any type.

---

## ✨ Features

*   **🔐 Secure OTP Authentication:** Passwordless sign-in and registration powered by Appwrite User Sessions.
*   **📊 Dynamic Dashboard:** Get a visual summary of your storage limit (2GB budget), category-wise space usage, and your most recent uploads.
*   **📁 File Management & Operations:**
    *   Drag-and-drop file uploads with progress trackers.
    *   Preview files in a media-viewer modal.
    *   Download, rename, or delete files seamlessly.
*   **✉️ Real-Time sharing:** Share your uploaded files with colleagues or friends simply by entering their email addresses.
*   **🔍 Advanced Search & Filtering:**
    *   Instant global search by file names.
    *   Filter files by category (Images, Documents, Media, Others).
    *   Sort files by date created, alphabetical order, or size.
*   **📱 Responsive Premium Design:** Beautiful dark-accented sidebar, clean cards, fluid modals, and responsive layout for desktop, tablet, and mobile views.

---

## 🛠️ Tech Stack

| Technology | Purpose |
| :--- | :--- |
| **Next.js 15** | React Framework (App Router, Server Actions, Server Components) |
| **Appwrite Cloud** | Backend-as-a-Service (Database, Storage Buckets, OTP Auth) |
| **Tailwind CSS** | Premium Utility-First Styling & Transitions |
| **Shadcn UI & Radix** | Accessible & Interactive UI Components |
| **Recharts** | Interactive SVG Charts for Storage Usage Visualizations |
| **React Hook Form + Zod** | Form validation and typed schemas |

---

## 🚀 Getting Started

### Prerequisites

*   Node.js (v18.x or higher)
*   An active [Appwrite Cloud](https://cloud.appwrite.io) account.

### 1. Installation

Clone the repository and install the dependencies:

```bash
git clone https://github.com/mailmeatdarshan/stash.git
cd stash
npm install
```

### 2. Environment Variables Setup

Create a `.env.local` file in the root of the project and populate it with your Appwrite project configuration:

```env
NEXT_PUBLIC_APPWRITE_ENDPOINT="https://sgp.cloud.appwrite.io/v1"
NEXT_PUBLIC_APPWRITE_PROJECT=""
NEXT_PUBLIC_APPWRITE_PROJECT_NAME=""
NEXT_PUBLIC_APPWRITE_DATABASE=""
NEXT_PUBLIC_APPWRITE_USERS_COLLECTION=""
NEXT_PUBLIC_APPWRITE_FILES_COLLECTION=""
NEXT_PUBLIC_APPWRITE_BUCKET=""
NEXT_APPWRITE_KEY="your_secret_appwrite_api_key"
```

### 3. Run Development Server

Launch the development server locally:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to view your local deployment of Stash!

---

## 📂 Project Structure

```text
stash/
├── app/                  # Next.js App Router (pages & layouts)
│   ├── (auth)/           # Authentication routes (Sign-In, Sign-Up)
│   ├── (root)/           # Main application dashboard & file views
│   └── layout.tsx        # Global HTML structure and font setup
├── components/           # Reusable UI React Components
│   ├── ui/               # Radix UI wrapper primitives (dialog, form, select, etc.)
│   ├── FileUploader.tsx  # Drag-and-drop file uploader
│   ├── Sidebar.tsx       # Desktop navigation pane
│   └── MobileNavigation.tsx # Responsive mobile sheet menu
├── constants/            # Global navigation paths, sorters & sizes
├── lib/                  # Appwrite configuration & server actions
│   ├── actions/          # Server Actions (Auth, File uploads, space metrics)
│   └── utils.ts          # Date formatters, file-type icons, size calculators
├── public/               # Static assets (brand logos, SVG icons)
└── package.json          # Node dependencies & custom script keys
```

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to open a pull request or submit an issue to help improve Stash.