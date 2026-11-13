# ពិធីភ្ជាប់ពាក្យ · Chhunmeng & Maly Engagement Website

A modern, mobile-first bilingual (Khmer & English) engagement invitation website optimized for deployment on [Vercel](https://vercel.com).

---

## 📁 Project Structure

```
Chhunmeng&maly/
├── index.html          # Main invitation page (Khmer & English)
├── vercel.json         # Vercel routing, cache, and security headers
├── .gitignore          # Keeps private files and OS junk out of deployment
├── music.mp3           # Background music track
├── guest-links.html    # Offline tool to generate personalized guest links
├── img/                # All optimized photos and QR codes
│   ├── hero.jpg        # Hero screen and envelope backdrop
│   ├── words.jpg       # Arched photo beside the invitation card
│   ├── couple.jpg      # Couple portrait photo
│   ├── g1.jpg          # Love story photo 1
│   ├── g2.jpg          # Love story photo 2
│   ├── g3.jpg          # Love story photo 3
│   ├── qr1.png         # Groom KHQR (ABA)
│   ├── qr2.png         # Bride KHQR (ACLEDA)
│   └── og.jpg          # Social media share preview (1200x630)
└── README.md
```

---

## 🚀 How to Host on Vercel

### Method 1: Deploy with GitHub (Recommended)
1. Create a new repository on [GitHub](https://github.com/new).
2. Upload all the files from this folder (`Chhunmeng&maly`) to your GitHub repository:
   - Click **Add file** > **Upload files**.
   - Drag all the files and folders (`index.html`, `vercel.json`, `music.mp3`, `img/`, etc.) and commit.
3. Log in to [Vercel](https://vercel.com).
4. Click **Add New...** > **Project**.
5. Import your GitHub repository.
6. Under **Build & Development Settings**, leave Framework Preset as **Other** (no build command needed).
7. Click **Deploy**.
8. Within seconds, your site will be live at `https://your-project-name.vercel.app`!

### Method 2: Deploy using Vercel CLI
If you have Node.js installed on your computer:
1. Open PowerShell or Terminal in this folder.
2. Run:
   ```bash
   npx vercel
   ```
3. Follow the quick prompts to log in and deploy.

---

## ✏️ Customization Checklist

### 1. Replacing Photos
Drop your real photos into the `img/` folder with exact lowercase names:
- `hero.jpg`: Main backdrop (~800 KB)
- `words.jpg`: Invitation card side photo (~800 KB)
- `couple.jpg`: Couple portrait (~800 KB)
- `g1.jpg`, `g2.jpg`, `g3.jpg`: Story photos
- `qr1.png`, `qr2.png`: KHQR codes for gifts
- `og.jpg`: Preview image when sharing on Facebook/Telegram (1200×630)

*Tip: Compress photos with [squoosh.app](https://squoosh.app) to keep loading fast on mobile phones.*

### 2. Music Track
Replace `music.mp3` in the main folder with your chosen romantic song (MP3 format).

### 3. Setting Up Online RSVP & Wishes
In `index.html` (around line 557):
1. Sign up for free at [Formspree](https://formspree.io).
2. Create a form and paste the endpoint URL into `FORM_ENDPOINT`:
   ```javascript
   const FORM_ENDPOINT = "https://formspree.io/f/your_form_id";
   ```
3. Set your email in `RSVP_EMAIL`:
   ```javascript
   const RSVP_EMAIL = "your-email@gmail.com";
   ```

### 4. Sending Personalized Invitation Links
1. Open `guest-links.html` by double-clicking it on your computer (this is a local offline tool).
2. Enter your deployed Vercel URL (e.g. `https://chhunmeng-maly.vercel.app`).
3. Paste guest names (one per line).
4. Click **បង្កើតតំណ (Generate)** to get unique links with `?to=GuestName`.
5. Click **ចម្លង (Copy)** next to any guest and send via Telegram or Messenger!
