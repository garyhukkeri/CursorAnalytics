# Cursor Analytics Agent Template

A ready-to-use template for transforming Cursor into a powerful analytics agent with browser-first visualization workflow. This template configures Cursor to automatically create, update, and display interactive analytics dashboards using ECharts.

> **⚠️ Important**: This template is designed to work with **Cursor's built-in browser** and works best when using **Cursor's browser-focused layout**. The dashboard opens directly within Cursor's integrated browser panel, providing a seamless analytics experience without switching to external browsers.

## 🎯 What This Template Provides

- **Browser-First Analytics Canvas**: All analyses are displayed and updated in a single interactive HTML dashboard
- **Cursor's Built-in Browser**: Designed specifically for Cursor's integrated browser panel
- **Browser-Focused Layout**: Optimized for Cursor's browser-focused layout for the best experience
- **ECharts-Only Visualization**: Strict policy ensuring consistent, high-quality visualizations
- **Append-Based Workflow**: New analyses are added to the dashboard without replacing existing content
- **Automated Browser Integration**: Cursor automatically opens and updates the dashboard in Cursor's built-in browser
- **Pre-configured Rules**: Ready-to-use Cursor rules that guide the AI agent's behavior

## 📁 Project Structure

```
your-project/
├── .cursor/
│   └── rules/              # Cursor AI agent configuration
│       ├── analytics-agent.mdc          # Core analytics workflow
│       ├── browser-analytics-canvas.mdc  # Browser-first canvas rules
│       ├── echarts-only.mdc              # Visualization policy
│       └── package-policy.mdc            # Package restrictions
├── data/                   # Place your CSV/data files here
├── analysis/               # Optional: Save analysis reports/notes here
└── visualizations/         # Analytics dashboard HTML files
    └── analytics_dashboard.html  # Main dashboard (auto-created/updated)
```

## 🚀 Quick Start

### 0. Try the Example (Optional)

This template includes example data (`data/Pune FinancialHealth2022.csv`) and a sample dashboard (`visualizations/analytics_dashboard.html`). Try it out:

```
@Pune FinancialHealth2022.csv analyze this data
```

This will demonstrate the full workflow!

### 1. Clone or Copy This Template

```bash
# Option 1: Clone this repo
git clone <your-repo-url> my-analytics-project
cd my-analytics-project

# Option 2: Copy the .cursor/rules directory to your existing project
cp -r .cursor/rules /path/to/your/project/.cursor/
mkdir -p data analysis visualizations
```

### 2. Install Required Python Packages (Optional)

The template uses Python for data processing. Install approved packages:

```bash
pip install pandas numpy scipy statsmodels scikit-learn
```

**Note**: Python packages are optional. The template works with CSV files and can process data using JavaScript in the browser if needed.

### 3. Add Your Data

Place your data files in the `data/` directory:

```bash
cp your-data.csv data/
```

### 4. Start Using Cursor

Simply ask Cursor to analyze your data:

```
@your-data.csv analyze this data and create visualizations
```

Cursor will:
1. ✅ Process your data
2. ✅ Create/update `visualizations/analytics_dashboard.html`
3. ✅ Start a local HTTP server (if needed)
4. ✅ **Open the dashboard in Cursor's built-in browser** (appears in Cursor's browser panel)
5. ✅ Display the results interactively

> **💡 Tip**: For the best experience, use **Cursor's browser-focused layout**. The dashboard will open in Cursor's integrated browser panel, allowing you to see your code, chat, and analytics dashboard all in one view.

## 🌐 Cursor's Built-in Browser Integration

### Why Cursor's Browser?

This template is **specifically designed** to work with **Cursor's built-in browser**, not external browsers like Chrome or Firefox. Here's why:

**✅ Seamless Integration**
- Dashboard opens directly in Cursor's browser panel
- No need to switch between applications
- See code, chat, and analytics in one unified interface

**✅ Browser-Focused Layout**
- Optimized for Cursor's split-view layouts
- Dashboard appears alongside your code editor
- Perfect for iterative analysis workflows

**✅ Persistent Session**
- Browser tab stays open across multiple analyses
- Dashboard updates automatically without manual refresh
- All analyses accumulate in one view

**✅ AI Agent Integration**
- Cursor's AI can interact with the browser directly
- Automatic scrolling to new sections
- Real-time updates as analyses are added

### Setting Up Cursor's Browser Panel

1. **Enable Browser View**: In Cursor, open the browser panel (usually via View menu or keyboard shortcut)
2. **Use Browser-Focused Layout**: Arrange your windows to see code editor, chat, and browser simultaneously
3. **Keep Browser Tab Open**: The dashboard will persist in Cursor's browser across your analytics session

### What You'll See

When you request an analysis:
- Cursor's browser panel opens (or updates if already open)
- Dashboard loads at `http://localhost:8000/visualizations/analytics_dashboard.html`
- New analysis sections appear automatically
- Browser scrolls to show the latest analysis

> **Important**: If the dashboard opens in an external browser instead, check that Cursor's browser panel is enabled and you're using Cursor's browser-focused layout.

## 💡 How It Works

### The Browser-First Workflow

This template leverages **Cursor's built-in browser** to provide a seamless analytics experience. When you request an analysis, Cursor follows this workflow:

1. **Data Processing**: Uses approved Python libraries (pandas, numpy, etc.) to process your data
2. **Analysis Creation**: Generates insights and statistical analysis
3. **Dashboard Update**: Appends a new section to `analytics_dashboard.html` with:
   - Unique section ID
   - Timestamp
   - Description
   - Interactive ECharts visualizations
4. **Browser Display**: Automatically opens/updates **Cursor's built-in browser** to show results
5. **Session Continuity**: Keeps the same browser tab open in Cursor's browser panel for all analyses

### Using Cursor's Built-in Browser

**Key Benefits:**
- ✅ **No external browser needed**: Everything happens within Cursor
- ✅ **Integrated experience**: See code, chat, and analytics in one window
- ✅ **Browser-focused layout**: Optimized for Cursor's split-view layouts
- ✅ **Persistent session**: Browser tab stays open across multiple analyses
- ✅ **Automatic updates**: Dashboard refreshes automatically when new analyses are added

**Recommended Layout:**
- Use Cursor's **browser-focused layout** for the best experience
- The dashboard opens in Cursor's browser panel (not external browser)
- You can split your view to see code editor, chat, and browser simultaneously

### Example Interaction

```
You: Analyze the correlation between revenue and expenditure
```

**Cursor automatically:**
- Calculates correlation coefficient
- Creates scatter plot with regression line
- Appends new section to dashboard
- Opens browser showing the analysis
- Scrolls to the new section

### Adding More Analyses

Each new analysis request automatically:
- ✅ Appends to the existing dashboard (doesn't replace)
- ✅ Maintains all previous analyses
- ✅ Updates the browser view
- ✅ Scrolls to the new section

## 📊 Visualization Features

### Supported Chart Types (ECharts)

- Line charts (with area fill, smooth curves)
- Bar charts (grouped, stacked)
- Scatter plots (with regression lines)
- Pie charts
- Heatmaps
- And all other ECharts chart types

### Interactive Features

- **Tooltips**: Hover over data points for details
- **Zoom & Pan**: Interactive chart controls
- **Legends**: Toggle series visibility
- **Responsive**: Charts resize with window
- **Export**: Save charts as images

## ⚙️ Configuration

### Customizing Rules

Edit files in `.cursor/rules/` to customize behavior:

- **`analytics-agent.mdc`**: Modify core workflow and approved libraries
- **`browser-analytics-canvas.mdc`**: Change dashboard structure or browser behavior
- **`echarts-only.mdc`**: Adjust visualization policies
- **`package-policy.mdc`**: Add/remove approved Python packages

### Changing Dashboard Styling

The dashboard HTML file (`visualizations/analytics_dashboard.html`) uses inline CSS. Modify the `<style>` section to customize:
- Colors and themes
- Layout and spacing
- Typography
- Chart container sizes

### Adding New Python Packages

1. Edit `.cursor/rules/package-policy.mdc`
2. Add package to approved list
3. Explain why it's needed
4. Install: `pip install package-name`

## 🎨 Example Use Cases

### Financial Analysis
```
Analyze revenue trends over time
Calculate profit margins
Compare quarterly performance
```

### Data Exploration
```
Show distribution of sales by region
Identify outliers in customer data
Analyze correlation between variables
```

### Statistical Analysis
```
Perform regression analysis
Calculate confidence intervals
Generate statistical summaries
```

## 🔧 Troubleshooting

### Dashboard Not Opening in Cursor's Browser

**Issue**: Dashboard doesn't open in Cursor's built-in browser

**Solution**: 
1. **Check Cursor's browser panel**: Look for the browser tab in Cursor's interface
2. **Enable browser view**: Use Cursor's browser-focused layout if not already enabled
3. Check if HTTP server is running: `lsof -i :8000`
4. Manually start server: `python3 -m http.server 8000`
5. Navigate manually: In Cursor's browser panel, go to `http://localhost:8000/visualizations/analytics_dashboard.html`

**Note**: If the dashboard opens in an external browser instead of Cursor's built-in browser, check that you're using Cursor's browser panel. The template is optimized for Cursor's integrated browser experience.

### Charts Not Rendering

**Issue**: Empty chart containers

**Solution**:
1. Check browser console for JavaScript errors
2. Verify ECharts CDN is loading: Check Network tab
3. Ensure chart container IDs are unique

### Multiple Dashboard Files Created

**Issue**: Cursor creates new HTML files instead of updating dashboard

**Solution**: 
1. Verify `.cursor/rules/browser-analytics-canvas.mdc` exists
2. Check that `alwaysApply: true` is set in rule files
3. Restart Cursor to reload rules

## 📚 Key Concepts

### Single Dashboard Pattern

All analyses live in **one file**: `visualizations/analytics_dashboard.html`

- ✅ Easy to share (single HTML file)
- ✅ All analyses in one place
- ✅ Maintains analysis history
- ✅ Simple to export/backup

### Append-Only Workflow

New analyses are **appended**, not replaced:

- Previous analyses remain visible
- Build up comprehensive dashboard over time
- Each analysis has timestamp and unique ID
- Easy to reference previous work

### Browser as Canvas

**Cursor's built-in browser** is the **primary interface**:

- Real-time updates directly in Cursor's browser panel
- Interactive visualizations without leaving Cursor
- No need to manually open files or switch to external browsers
- Persistent session across analyses in the same browser tab
- Seamless integration with Cursor's browser-focused layout

## 🎓 Best Practices

1. **Use Cursor's Browser-Focused Layout**: Enable Cursor's browser panel for the best experience
2. **Organize Data**: Keep data files in `data/` directory
3. **Descriptive Requests**: Be specific about what analysis you want
4. **Iterative Analysis**: Build up insights gradually
5. **Review Dashboard**: Check Cursor's browser panel regularly to see all analyses
6. **Keep Browser Tab Open**: The dashboard persists in Cursor's browser across sessions
7. **Export When Needed**: Save dashboard HTML for sharing/reporting

## 🔒 Package Restrictions

This template restricts certain packages to maintain consistency:

**❌ Restricted:**
- matplotlib, seaborn, plotly, bokeh, altair
- Any visualization library except ECharts

**✅ Approved:**
- pandas, numpy, scipy, statsmodels, scikit-learn
- ECharts (via CDN in HTML)

## 📝 Notes

- **Cursor's Built-in Browser**: This template is designed specifically for Cursor's integrated browser, not external browsers
- **Browser-Focused Layout**: Works best with Cursor's browser-focused layout for optimal viewing
- The dashboard file grows over time as analyses are added
- Each analysis section is self-contained with its own JavaScript
- Charts are responsive and work well in Cursor's browser panel
- The template uses ECharts 5.4.3 from CDN (no local installation needed)
- The dashboard opens automatically in Cursor's browser panel when analyses are created

## 🤝 Contributing

To improve this template:

1. Test with different data types
2. Add example analyses
3. Improve documentation
4. Share feedback

## 🙏 Acknowledgments

- Built for [Cursor](https://cursor.sh/) AI code editor
- Uses [Apache ECharts](https://echarts.apache.org/) for visualizations

---

**Ready to start?** Place your data in `data/` and ask Cursor to analyze it!
