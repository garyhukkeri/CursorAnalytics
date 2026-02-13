# Quick Start Guide

> **🌐 Important**: This template uses **Cursor's built-in browser** and works best with **Cursor's browser-focused layout**. The dashboard opens directly in Cursor's browser panel, not in external browsers.

## 🚀 Get Started in 3 Steps

### Step 1: Copy the Rules

Copy the `.cursor/rules/` directory to your project:

```bash
# If starting a new project
mkdir my-analytics-project
cd my-analytics-project
cp -r /path/to/template/.cursor ./
mkdir -p data analysis visualizations
```

### Step 2: Add Your Data

Place your CSV or data files in the `data/` directory:

```bash
cp your-data.csv data/
```

### Step 3: Ask Cursor to Analyze

In Cursor, simply ask:

```
@your-data.csv analyze this data and create visualizations
```

That's it! Cursor will:
- ✅ Process your data
- ✅ Create the dashboard
- ✅ **Open it in Cursor's built-in browser** (appears in Cursor's browser panel)
- ✅ Show interactive charts

> **💡 Tip**: Make sure Cursor's browser panel is enabled and use Cursor's browser-focused layout for the best experience!

## 📝 Common Commands

### Basic Analysis
```
Analyze the trends in this data
Show me a correlation analysis
Create visualizations for this dataset
```

### Specific Requests
```
Calculate correlation between column1 and column2
Show distribution of sales by region
Analyze revenue trends over time
```

### Adding More Analysis
```
Add a regression analysis
Show me outliers in this data
Create a time series forecast
```

Each request automatically appends to your dashboard!

## 🎯 What Happens Behind the Scenes

1. **Cursor reads your data** → Processes with pandas/numpy
2. **Generates analysis** → Calculates statistics, correlations, etc.
3. **Creates visualizations** → Uses ECharts to build interactive charts
4. **Updates dashboard** → Appends new section to `analytics_dashboard.html`
5. **Opens Cursor's browser** → Shows results in Cursor's built-in browser panel at `http://localhost:8000/visualizations/analytics_dashboard.html`

## 💡 Pro Tips

- **Use Cursor's browser panel**: Enable Cursor's built-in browser for the best experience
- **Browser-focused layout**: Arrange windows to see code, chat, and browser simultaneously
- **Keep browser tab open**: Cursor reuses the same tab in Cursor's browser for all analyses
- **Be specific**: "Analyze correlation" is better than "analyze data"
- **Iterate**: Build up your dashboard with multiple analyses
- **Export**: Save `analytics_dashboard.html` to share your work

## 🔧 Troubleshooting

**Dashboard not opening in Cursor's browser?**
1. **Check Cursor's browser panel**: Make sure Cursor's built-in browser is enabled
2. **Use browser-focused layout**: Enable Cursor's browser panel view
3. Start HTTP server if needed:
```bash
python3 -m http.server 8000
```
4. In Cursor's browser panel, navigate to: `http://localhost:8000/visualizations/analytics_dashboard.html`

> **Note**: If dashboard opens in external browser instead, ensure Cursor's browser panel is enabled.

**Charts not showing?**
- Check browser console (F12) for errors
- Verify data file is readable
- Ensure column names are correct

**Want to start fresh?**
- Delete `visualizations/analytics_dashboard.html`
- Cursor will create a new one on next analysis

## 📚 Next Steps

- Read the full [README.md](README.md) for detailed documentation
- Explore example analyses in the dashboard
- Customize rules in `.cursor/rules/` for your needs

---

**Ready?** Add your data and start analyzing! 🎉
