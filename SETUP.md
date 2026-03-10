# Nexus Live Demo - Setup Instructions

## Repository Not Yet Created

The demo files are ready, but you need to create the GitHub repository manually.

### Step 1: Create Repository on GitHub

1. Go to: https://github.com/new
2. Repository name: `nexus-demo-display`
3. Owner: `Grandjig` (your GitHub account)
4. Set to Public
5. Click "Create repository"

### Step 2: Push to GitHub

```bash
cd ~/projects/nexus-demo-display
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/github
git push -u origin master
```

### Step 3: Enable GitHub Pages

1. Go to: https://github.com/Grandjig/nexus-demo-display/settings/pages
2. Under "Build and deployment":
   - Source: Deploy from a branch
   - Branch: `master` → `/ (root)`
   - Click Save

3. Or create `gh-pages` branch:
```bash
cd ~/projects/nexus-demo-display
git checkout -b gh-pages
git push origin gh-pages
```

Then in GitHub settings, select `gh-pages` as the source branch.

### Step 4: Access Your Demo

Once GitHub Pages is enabled, your demo will be live at:

```
https://grandjig.github.io/nexus-demo-display/
```

---

## What's Included

### `index.html`
Complete standalone fraud detection demo with:
- **Live transaction ticker** - Shows 12 fraudulent transactions one by one
- **Real-time fraud scoring** - Color-coded (Red=Blocked, Yellow=Review, Green=Approved)
- **Nigerian banks** - FirstBank, GTBank, Access Bank, Zenith, UBA, Diamond
- **Naira currency** - All amounts in ₦
- **Fraud analytics** - Charts showing fraud types and transaction status
- **Impressive metrics**:
  - 94% detection rate
  - 39ms average detection time
  - 3% false positive rate
  - ₦8.15M blocked today

### `nexus-demo-seed.json`
The actual transaction data used in the demo (for reference/modification)

---

## Demo Features

✅ **Animations**: Transactions slide in smoothly
✅ **Color coding**: Red (blocked), Yellow (review), Green (approved)
✅ **Fraud signals**: Shows detected fraud patterns
✅ **Live indicator**: Pulsing green dot shows it's "live"
✅ **Responsive**: Works on desktop, tablet, mobile
✅ **Fast loading**: No external dependencies - everything is self-contained
✅ **Professional design**: Dark theme with tech-forward UI

---

## For CTOs

This demo is designed to impress technical decision-makers:

1. **Speed**: "39ms average detection" - faster than email notifications
2. **Accuracy**: "94% detection rate" with only 3% false positives
3. **Real fraud patterns**: Shows actual Nigerian fraud vectors (SIM swap, account takeover, etc.)
4. **Concrete impact**: "₦8.15M blocked today"
5. **Technical depth**: Device fingerprinting, behavioral baseline, signal breakdown

---

## How to Use with Outreach

1. Send CTOs the link: `https://grandjig.github.io/nexus-demo-display/`
2. "Watch fraud detection in real-time"
3. Follow up with Nexus demo video call
4. Use 15-minute demo to close pilot deal

---

## Customization

To change the transaction data:
1. Edit `index.html` in the `<script>` section
2. Modify the `transactionData` object with your own transactions
3. Commit and push: `git add . && git commit -m "Update demo data" && git push`

To update the seed data used:
1. Edit `nexus-demo-seed.json`
2. Copy values into `transactionData.sample_transactions` in `index.html`

---

**Status**: Ready to push to GitHub Pages
**Created**: 2026-03-10
**For**: Nexus Pilot Outreach (27-day sprint)
