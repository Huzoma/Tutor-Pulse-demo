# TutorPulse 🎓
### Automated Home-Lesson Job Matching Platform

**TutorPulse** is a robust web application designed to streamline the process of finding and applying for remote or home tutoring opportunities. By continuously scanning major job boards, it gives independent tutors a "first-to-know" advantage through real-time automation.

---

## 📖 Table of Contents
- [About the Project](#about-the-project)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Configuration](#configuration)
- [Contributing](#contributing)

---

## 🧐 About the Project

Searching for tutoring gigs often involves manually refreshing multiple job sites (Indeed, Glassdoor, local boards) and engaging in repetitive data entry.

**TutorPulse solves this by:**
1.  **Eliminating Manual Browsing:** It aggregates listings from parents seeking tutors in real-time.
2.  **Reducing Missed Opportunities:** Speed is key in freelancing; TutorPulse ensures you are the first to know.
3.  **Automating Applications:** With the AutoApply toggle, the system can securely submit your CV/Cover Letter instantly using headless browser automation.

**Target Audience:**
* Independent Tutors & Teachers
* Retired Educators
* College Students (Education majors/Subject experts)
* Tutoring Agencies

---

## ✨ Key Features

* **Real-Time Scanning:** A Python-based engine that pulls new listings the moment they go live.
* **Smart Filtering:** Users can filter matches by subject, grade level (K-12/College), hourly rate, and geographic radius.
* **Instant Web Notifications:** Browser-based push alerts notify you immediately when a match is found.
* **AutoApply™:** Securely stores user credentials, Résumés, and Cover Letter templates to automate form submission.
* **Dashboard:** A responsive Next.js dashboard to manage job feeds, saved searches, and application history.

---

## ⚙️ Tech Stack

### Core Framework (Web)
* **Framework:** Next.js (React Framework)
* **Language:** JavaScript (ES6+)
* **Styling:** Tailwind CSS

### Backend Services & API
* **Server Runtime:** Node.js (via Next.js API Routes or Custom Server)
* **Job Queuing:** Redis (for managing scraper queues)
* **Real-time Updates:** Socket.io / WebSockets

### Automation & Data Engineering
* **Web Scraping:** Python (BeautifulSoup, Selenium)
* **Headless Automation:** Puppeteer / Playwright (managed via Node.js)

### Infrastructure & Database
* **Database:** MongoDB (User profiles, preferences, scraped listings)
* **Storage:** AWS S3 (Secure storage for CVs/Resumes)
* **Authentication:** NextAuth.js (OAuth 2.0)
* **Security:** AES-256 Encryption (for stored sensitive form data)

---

## 🚀 Getting Started

Follow these steps to set up the project locally.

### Prerequisites
* Node.js (v18+)
* Python (v3.8+)
* MongoDB (Local or Atlas URL)
* Redis

### Installation

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/TutorPulse/tutor-pulse.git](https://github.com/TutorPulse/tutor-pulse.git)
    cd tutor-pulse
    ```

2.  **Install Web Dependencies (Next.js)**
    ```bash
    npm install
    # or
    yarn install
    ```

3.  **Install Python Scraper Dependencies**
    Navigate to the python engine folder (if separated):
    ```bash
    cd engine
    pip install -r requirements.txt
    ```

4.  **Run the Development Server**
    ```bash
    npm run dev
    ```
    Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

---

## 🔧 Configuration

Create a `.env.local` file in the root directory for Next.js:

```env
# Database
MONGODB_URI=your_mongodb_connection_string
REDIS_URL=your_redis_url

# NextAuth / Security
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=your_auth_secret
AES_KEY=your_encryption_key

# External Services
AWS_ACCESS_KEY_ID=your_aws_key
AWS_SECRET_ACCESS_KEY=your_aws_secret
