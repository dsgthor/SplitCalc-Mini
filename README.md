# 🧾 SplitCalc - Split Expenses Easily

<div align="center">

### 🚀 **Try it now - No installation required!**

<a href="https://splitcalc-mini.onrender.com/" target="_blank">
  <img src="https://img.shields.io/badge/🌐%20LAUNCH%20APP-4F46E5?style=for-the-badge&logoColor=white&labelColor=6366F1" alt="Launch SplitCalc" />
</a>

*Split expenses instantly • Calculate balances fairly • Export your data*

---

</div>

A modern, intuitive web application for splitting expenses among groups. Perfect for roommates, friends, travel groups, or any situation where you need to track shared expenses and calculate who owes what.

<div align="center">

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Available-brightgreen)](https://splitcalc-mini.onrender.com/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://html.spec.whatwg.org/)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://www.w3.org/Style/CSS/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![TailwindCSS](https://img.shields.io/badge/Tailwind%20CSS-38B2AC?logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)

</div>

## 🌟 Features

### Core Functionality
- **👥 Member Management**: Add and remove group members easily
- **➕ Expense Tracking**: Record expenses with title, amount, payer, and participants
- **💰 Smart Balance Calculation**: Automatic calculation of who owes what
- **📊 Detailed Breakdown**: View complete calculation steps and methodology
- **🔄 Instant Updates**: Real-time balance updates as you add expenses

### Advanced Features
- **📜 Expense History**: Keep track of all expenses with easy removal options
- **🔄 Calculation History**: Save and restore up to 3 previous calculations
- **📥 Export/Import**: Full data export/import in JSON format
- **💾 Auto-Save**: Persistent storage using localStorage
- **📱 Responsive Design**: Works perfectly on desktop, tablet, and mobile

### User Experience
- **🎨 Modern UI**: Clean, gradient-based design with smooth animations
- **⚡ Fast Performance**: Single-file architecture for instant loading
- **🎯 Intuitive Controls**: Select all/deselect all options for shared expenses
- **✅ Smart Settlements**: Optimized payment suggestions to minimize transactions

## 🚀 Quick Start

<div align="center">

### 🌟 **Ready to split expenses?**

<a href="https://splitcalc-mini.onrender.com/" target="_blank">
  <img src="https://img.shields.io/badge/🔥%20START%20CALCULATING-FF6B6B?style=for-the-badge&logoColor=white" alt="Start Using SplitCalc" />
</a>

**No signup • No download • Works instantly**

</div>

### Option 1: Use Online (Recommended)
Visit the live application: **[https://splitcalc-mini.onrender.com/](https://splitcalc-mini.onrender.com/)**

### Option 2: Local Setup
1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/splitcalc.git
   cd splitcalc
   ```

2. **Open the application**
   ```bash
   # Simply open index.html in your browser
   open index.html
   # or
   python -m http.server 8000  # Then visit http://localhost:8000
   ```

3. **Start splitting expenses!**

## 📖 How to Use

### 1. Add Members
- Enter member names in the "Members" section
- Add all people who will be part of the expense sharing
- Remove members by clicking the × button

### 2. Record Expenses
- **Title**: Describe the expense (e.g., "Dinner at Restaurant")
- **Amount**: Enter the total amount spent
- **Paid By**: Select who paid for the expense
- **Shared With**: Check all members who should share this expense
- Use "Select All" or "Deselect All" for convenience

### 3. View Balances
- See who owes money and who should receive money
- Click "Show Calculations" for detailed breakdown
- All calculations are transparent and verifiable

### 4. Manage Data
- **New Calculation**: Start fresh while saving current data to history
- **Export**: Download your data as JSON for backup
- **Import**: Restore previous calculations or share with others
- **History**: Access up to 3 previous calculations

## 🔢 Calculation Method

SplitCalc uses a fair and transparent calculation method:

1. **Credit Assignment**: Each payer receives credit for the full amount they paid
2. **Share Calculation**: Each expense is divided equally among selected participants
3. **Balance Calculation**: Final balance = Total Credits - Total Shares
4. **Settlement Optimization**: Suggests minimum number of transactions to settle all debts

### Example
- **Expense**: Dinner ₹1200, paid by Alice, shared with Alice, Bob, Charlie
- **Calculation**: ₹1200 ÷ 3 = ₹400 per person
- **Result**: Alice gets ₹1200 credit - ₹400 share = +₹800, Bob and Charlie owe ₹400 each

## 🛠️ Technical Details

### Architecture
- **Single File Application**: Everything in one HTML file for easy deployment
- **No External Dependencies**: Only uses CDN for TailwindCSS
- **Client-Side Only**: No server required, works offline after first load
- **Progressive Enhancement**: Graceful degradation on older browsers

### Technology Stack
- **Frontend**: Vanilla JavaScript, HTML5, CSS3
- **Styling**: TailwindCSS via CDN
- **Storage**: localStorage for data persistence
- **Animations**: CSS keyframes for smooth transitions

### Browser Compatibility
- ✅ Chrome/Chromium (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ⚠️ IE11+ (limited support)

## 📱 Mobile Support

SplitCalc is fully responsive and optimized for mobile devices:
- Touch-friendly interface
- Optimized layouts for small screens
- Fast loading on mobile networks
- Works offline after first visit

## 🔒 Privacy & Security

- **No Data Collection**: All data stays on your device
- **No Server Communication**: Purely client-side application
- **Local Storage Only**: Data persists using browser's localStorage
- **No Analytics**: No tracking or analytics code included

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Reporting Issues
- Use GitHub Issues to report bugs
- Include browser version and steps to reproduce
- Attach screenshots for UI issues

### Feature Requests
- Suggest new features via GitHub Issues
- Explain the use case and expected behavior
- Consider backward compatibility

### Code Contributions
1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Make your changes in `index.html`
4. Test thoroughly across different browsers
5. Submit a pull request with detailed description

### Development Guidelines
- Maintain single-file architecture
- Use vanilla JavaScript (no external libraries)
- Follow existing code style and naming conventions
- Test on multiple devices and browsers
- Keep the application lightweight and fast

## 📊 Use Cases

### Perfect For:
- **👨‍👩‍👧‍👦 Roommate Expenses**: Rent, utilities, groceries, household items
- **✈️ Group Travel**: Hotels, meals, activities, transportation
- **🍕 Social Events**: Parties, dinners, group activities
- **💼 Team Outings**: Office lunches, team building activities
- **🎓 Student Groups**: Study materials, group projects, social events
- **👪 Family Events**: Shared costs for celebrations, trips

### Business Use:
- **Freelancer Teams**: Project expenses and resource sharing
- **Small Businesses**: Petty cash management and expense tracking
- **Event Planning**: Budget tracking for events and gatherings

## ❓ FAQ

**Q: Is my data secure?**
A: Yes, all data is stored locally on your device. Nothing is sent to external servers.

**Q: Can I use this offline?**
A: Yes, after the first load, the app works completely offline.

**Q: How many expenses can I track?**
A: No limit! The app handles any number of expenses efficiently.

**Q: Can I export my data?**
A: Yes, use the Export JSON feature to download your complete data.

**Q: What happens if I clear my browser data?**
A: Your data will be lost. Always export important calculations as backup.

**Q: Can multiple people access the same calculation?**
A: Share exported JSON files, or use the app on a shared device.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **TailwindCSS** for the excellent utility-first CSS framework
- **Modern Web Standards** for making client-side applications powerful
- **Open Source Community** for inspiration and best practices

## 📞 Support

<div align="center">

**Need help or have suggestions?**

<a href="https://splitcalc-mini.onrender.com/" target="_blank">
  <img src="https://img.shields.io/badge/💡%20TRY%20THE%20APP-6366F1?style=for-the-badge&logoColor=white" alt="Try SplitCalc" />
</a>

</div>

- **Live Demo**: [https://splitcalc-mini.onrender.com/](https://splitcalc-mini.onrender.com/)
- **Issues**: [GitHub Issues](https://github.com/yourusername/splitcalc/issues)
- **Email**: your.email@example.com

---

<div align="center">

**Made with ❤️ for fair expense sharing**

<a href="https://splitcalc-mini.onrender.com/" target="_blank">
  <img src="https://img.shields.io/badge/🎯%20USE%20SPLITCALC%20NOW-22C55E?style=for-the-badge&logoColor=white" alt="Use SplitCalc Now" />
</a>

*Star ⭐ this repository if you find it useful!*

</div>