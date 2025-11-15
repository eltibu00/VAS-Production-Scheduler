# 🎯 VAS Production Control Center

> **Stop losing money on every work order!** Real-time profitability tracking with automated alerts and beautiful analytics.

![Status](https://img.shields.io/badge/status-production%20ready-green)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## 🚨 The Problem This Solves

- ❌ Creating jobs without knowing if they're profitable
- ❌ Finding out you lost money AFTER work is done
- ❌ No visibility into which clients/work types are unprofitable
- ❌ Guessing at pricing instead of using data

## ✅ The Solution

A complete enterprise-grade production management system with **profitability tracking at its core**.

### Key Features

- 💰 **Real-Time Profit Calculation** - Know immediately if a job will lose money
- 🔔 **Automatic Email Alerts** - Get notified when jobs are unprofitable
- 📊 **Beautiful Dashboard** - Charts showing revenue vs labor trends
- 💡 **Smart Recommendations** - AI-powered suggestions to improve margins
- 📈 **Progress Tracking** - Monitor job completion in real-time
- 📧 **Automated Reports** - Weekly profitability summaries

---

## 🚀 Quick Start (15 Minutes)

### Step 1: Deploy Google Apps Script (5 min)

1. Open your Google Sheet → **Extensions** → **Apps Script**
2. Delete existing code and paste **[Code_Enterprise.gs](Code.gs)**
3. **Update line 7** with your email:
   ```javascript
   const NOTIFICATION_EMAIL = 'youremail@company.com';
   ```
4. Click **Deploy** → **New deployment**
   - Type: **Web app**
   - Execute as: **Me**
   - Who has access: **Anyone**
5. Click **Deploy** and copy the URL

### Step 2: Set Up Email Alerts (3 min)

1. Click the **Clock icon** ⏰ (Triggers) in left sidebar
2. Add trigger for **Daily SLA Check**:
   - Function: `dailySLACheck`
   - Event: Time-driven → Day timer → 8am to 9am
3. Add trigger for **Weekly Reports**:
   - Function: `weeklyProfitabilityReport`
   - Event: Time-driven → Week timer → Monday 8am

### Step 3: Update Website (5 min)

1. Open **[index.html](index.html)**
2. Find line ~186 and update:
   ```javascript
   SCRIPT_URL: 'https://script.google.com/macros/s/YOUR_ID/exec',
   ```
3. Upload to GitHub Pages

### Step 4: Test (2 min)

1. Create a test job with Revenue: $100, Labor: $270
2. Check for red highlighting in sheet
3. Verify email alert arrives

**Done! You now have enterprise profitability tracking!** 🎉

---

## 📊 Key Metrics Tracked

| Metric | What It Means | Target |
|--------|---------------|--------|
| **Margin %** | (Revenue - Labor) / Revenue | 25-30% |
| **$/Hour Rate** | Revenue / Labor Hours | $50-75 |
| **Profit** | Revenue - Labor | Positive |
| **Jobs Losing Money** | Count with negative margin | 0 |

---

## 💰 Stop Losing Money: The Pricing Formula

### ❌ OLD WAY (Losing Money):
```
Labor Cost: $270
Your Quote: $250
Result: -$20 LOSS ❌
```

### ✅ NEW WAY (Profitable):
```
Formula: Minimum Price = Labor Cost ÷ 0.75

Labor Cost: $270
Minimum Price: $270 ÷ 0.75 = $360
Result: $90 PROFIT (25% margin) ✅
```

**This is your MINIMUM. Add 10-20% more for complex/rush jobs.**

---

## 📧 Email Alerts You'll Receive

### 1. Immediate Profit Alerts
```
⚠️ PROFIT ALERT: Job #12345 is LOSING MONEY

Revenue: $250
Labor: $270
Margin: -$20 (-8%)

ACTION NEEDED: Review pricing or decline job
```

### 2. Daily SLA Reminders (8am)
```
VAS Production - SLA Alert: 3 items need attention

🚨 OVERDUE: Job #111
⚠️  DUE TOMORROW: Job #222
📅 DUE IN 2 DAYS: Job #333
```

### 3. Weekly Profitability Reports (Monday 8am)
```
Total Revenue: $12,450
Total Profit: $3,250
Average Margin: 26.1% ✅

✅ Profitable: 12 jobs
🚨 Losing Money: 1 job

LOSING MONEY:
• Job #456: -$150 ← FIX THIS!
```

---

## 🎯 What Success Looks Like

### Month 1: STABILIZE
- Goal: Stop losing money
- Target: 15%+ margin on all jobs
- Action: Raise prices using formula

### Month 2: OPTIMIZE
- Goal: Improve efficiency
- Target: 20%+ average margin
- Action: Track actual vs planned hours

### Month 3: SCALE
- Goal: Grow profitably
- Target: 25%+ average margin
- Action: More volume, better clients

---

## 📸 Screenshots

### Profitability Dashboard
![Dashboard](https://via.placeholder.com/800x400?text=Profitability+Dashboard)

### Jobs Losing Money Alert
![Alert](https://via.placeholder.com/800x300?text=Red+Alert+for+Unprofitable+Jobs)

### Email Notification
![Email](https://via.placeholder.com/600x400?text=Email+Alert+Example)

---

## 📁 Repository Structure

```
vas-control-center/
├── README.md                      ← You are here
├── index.html                     ← Main web application
├── Code.gs                        ← Google Apps Script
├── docs/
│   ├── IMPLEMENTATION_GUIDE.md   ← Complete setup guide
│   ├── TROUBLESHOOTING.md        ← Common issues & fixes
│   └── ENTERPRISE_ENHANCEMENTS.md ← Future features
└── screenshots/                   ← Dashboard images
```

---

## 🛠️ Technical Stack

- **Frontend**: HTML5, Tailwind CSS, Chart.js
- **Backend**: Google Apps Script
- **Database**: Google Sheets
- **Notifications**: Gmail API
- **Deployment**: GitHub Pages

---

## 📚 Documentation

### Full Guides
- 📖 [Complete Implementation Guide](docs/IMPLEMENTATION_GUIDE.md) - Detailed setup, training, strategies
- 🆘 [Troubleshooting Guide](docs/TROUBLESHOOTING.md) - Common issues and fixes
- 🚀 [Enterprise Enhancements](docs/ENTERPRISE_ENHANCEMENTS.md) - Future feature ideas

### Quick References
- [Pricing Formula Explained](docs/IMPLEMENTATION_GUIDE.md#pricing-formula-to-stop-losing-money)
- [Understanding Metrics](docs/IMPLEMENTATION_GUIDE.md#understanding-the-metrics)
- [Training Your Team](docs/IMPLEMENTATION_GUIDE.md#training-your-team)

---

## ⚙️ Configuration

### Required Settings

Update these in your files:

**Code.gs (Line 7):**
```javascript
const NOTIFICATION_EMAIL = 'your-email@company.com'; // ← Change this!
```

**index.html (Line 186):**
```javascript
const SCRIPT_URL = 'https://script.google.com/macros/s/YOUR_ID/exec'; // ← Paste deployment URL
```

**Optional Settings:**

```javascript
const LABOR_RATE = 27;  // Adjust if your labor rate is different
```

---

## 🐛 Troubleshooting

### Email alerts not working?
- ✅ Check NOTIFICATION_EMAIL is set correctly
- ✅ Verify triggers are created (Clock icon)
- ✅ Run function manually to test

### Jobs not showing?
- ✅ Check SCRIPT_URL is correct
- ✅ Hard refresh browser (Ctrl+Shift+R)
- ✅ Check browser console for errors

### Still stuck?
👉 [Read the Troubleshooting Guide](docs/TROUBLESHOOTING.md)

---

## 🤝 Contributing

Have ideas for improvements? Found a bug?

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

---

## 📜 License

MIT License - Feel free to use for your business!

---

## 🎓 Support

- 📖 [Full Documentation](docs/IMPLEMENTATION_GUIDE.md)
- 💬 [Open an Issue](https://github.com/yourusername/vas-control-center/issues)
- 📧 Email: support@yourcompany.com

---

## 🙏 Acknowledgments

Built with:
- [Tailwind CSS](https://tailwindcss.com/) - Styling
- [Chart.js](https://www.chartjs.org/) - Analytics charts
- [Lucide Icons](https://lucide.dev/) - Beautiful icons
- [Google Apps Script](https://developers.google.com/apps-script) - Backend

---

## 🚀 Get Started Now!

Ready to stop losing money? [Follow the Quick Start Guide](#-quick-start-15-minutes) above!

---

**Made with ❤️ for VAS Operations**

*Stop losing money. Start making data-driven decisions. Build a profitable business.*
