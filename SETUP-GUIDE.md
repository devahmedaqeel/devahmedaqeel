# 🚀 SETUP GUIDE — Profile Repo (README + Snake)

Is package mein sab kuch ready hai. Bas neeche ke steps follow karein — 5 minute ka kaam hai.

## 📦 Package mein kya hai

```
profile-repo/
├── README.md                        ← Aapki profile ka pura design
└── .github/
    └── workflows/
        └── snake.yml                ← Snake animation ka workflow (sahi jagah par)
```

Folder structure pehle se bilkul sahi hai — kuch move/rename nahi karna.

---

## ✅ Step-by-Step (Roman Urdu)

### Step 1 — Profile repo banayein (agar nahi hai)
1. https://github.com/new par jayein
2. Repository name: **devahmedaqeel** (bilkul apne username jaisa)
3. **Public** select karein → Create repository
4. GitHub khud bataega: "You found a secret! This is a special repository."

### Step 2 — Files upload karein
**Option A (Easy — browser se):**
1. Repo mein **Add file → Upload files**
2. `profile-repo` folder ke ANDAR ki sab cheezein drag karein
   (README.md aur .github folder dono)
3. ⚠️ Agar browser `.github` folder upload na kare to:
   - Pehle README.md upload karein
   - Phir **Add file → Create new file** → naam likhein:
     `.github/workflows/snake.yml`
   - snake.yml ka content paste karein → Commit

**Option B (Git se):**
```bash
cd profile-repo
git init
git add .
git commit -m "🚀 Launch profile"
git branch -M main
git remote add origin https://github.com/devahmedaqeel/devahmedaqeel.git
git push -u origin main
```

### Step 3 — Actions permission ON karein
1. Repo → **Settings → Actions → General**
2. Neeche scroll karein → **Workflow permissions**
3. **"Read and write permissions"** select karein → **Save**

### Step 4 — Snake pehli dafa run karein
- `snake.yml` push hote hi **khud run ho jayegi** (push trigger laga hua hai) ✅
- Ya manually: **Actions tab → Generate Contribution Snake → Run workflow**
- 1–2 minute mein green ✅ tick aayega
- Iske baad har raat 12 baje (UTC) khud update hogi

### Step 5 — Profile check karein
- https://github.com/devahmedaqeel kholein
- Sab kuch live hoga: banner, typing animation, stats, snake 🐍
- Snake na dikhe to hard refresh: **Ctrl + Shift + R**

---

## 🔧 Troubleshooting

| Problem | Hal |
| :--- | :--- |
| Snake image broken ❌ | Workflow abhi run nahi hui — Step 3 & 4 dobara check karein |
| Workflow fail (permission error) | Step 3 — "Read and write permissions" set nahi hui |
| Stats cards nahi dikh rahe | Kuch minute wait karein — pehli dafa cache banta hai |
| README profile par nahi dikh raha | Repo ka naam exactly `devahmedaqeel` hona chahiye + Public |

---

## ✏️ Baad mein customize karna

- **Project links:** README mein `[Demo](#) · [Repo](#)` ke `#` ko apne asli links se replace karein
- **Roadmap update:** 🟢🟡🔵 status apni progress ke hisab se badalte rahein
- **Snake ka time:** `snake.yml` mein cron `"0 0 * * *"` change kar sakte hain

Done! 🎉
