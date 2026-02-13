# Template Structure Reference

This document describes the complete structure of the Cursor Analytics Agent Template.

## 📁 Complete Directory Structure

```
cursor-analytics-template/
│
├── .cursor/                          # Cursor AI configuration
│   └── rules/                        # AI agent behavior rules
│       ├── analytics-agent.mdc       # Core analytics workflow
│       ├── browser-analytics-canvas.mdc  # Browser-first canvas rules
│       ├── echarts-only.mdc          # Visualization policy (ECharts only)
│       └── package-policy.mdc        # Python package restrictions
│
├── data/                             # Data files directory
│   └── [your-data-files].csv        # Place your CSV/data files here
│
├── analysis/                         # Optional: Analysis reports/notes
│   └── [analysis-notes].md          # Optional text reports
│
├── visualizations/                   # Generated visualizations
│   ├── analytics_dashboard.html     # Main dashboard (auto-created/updated)
│   └── [other-visualizations].html  # Optional: Separate visualizations
│
├── README.md                         # Main documentation
├── QUICKSTART.md                     # Quick start guide
├── TEMPLATE_STRUCTURE.md            # This file
└── .gitignore                        # Git ignore rules
```

## 📄 File Descriptions

### Cursor Rules (`.cursor/rules/`)

#### `analytics-agent.mdc`
- **Purpose**: Defines core analytics workflow
- **Key Features**:
  - Data processing workflow
  - Approved Python libraries
  - Output requirements
  - Browser-first display

#### `browser-analytics-canvas.mdc`
- **Purpose**: Browser-first analytics canvas workflow
- **Key Features**:
  - Single dashboard pattern
  - Append-only workflow
  - Browser interaction protocol
  - Update patterns

#### `echarts-only.mdc`
- **Purpose**: Strict ECharts-only visualization policy
- **Key Features**:
  - ECharts CDN loading
  - HTML template structure
  - Chart best practices
  - Restricted libraries list

#### `package-policy.mdc`
- **Purpose**: Package approval and restriction policy
- **Key Features**:
  - Pre-approved packages list
  - Restricted packages list
  - Approval process

### Data Directory (`data/`)

**Purpose**: Store your input data files

**Supported Formats**:
- CSV files (`.csv`)
- Excel files (`.xlsx`, `.xls`) - requires pandas
- JSON files (`.json`)
- Other formats supported by pandas

**Example**:
```
data/
├── sales_data.csv
├── customer_data.xlsx
└── financial_records.json
```

### Analysis Directory (`analysis/`)

**Purpose**: Optional storage for analysis notes and reports

**Usage**: 
- Save text-based analysis summaries
- Store statistical reports
- Keep analysis notes
- Document findings

**Note**: This is optional. The main output is the HTML dashboard.

### Visualizations Directory (`visualizations/`)

**Purpose**: Generated visualization files

**Main File**: `analytics_dashboard.html`
- Single dashboard file
- Contains all analyses
- Auto-updated by Cursor
- Opens in browser

**Optional Files**: Additional HTML files if explicitly requested

## 🔄 Workflow Files

### Analytics Dashboard (`visualizations/analytics_dashboard.html`)

**Structure**:
```html
<!DOCTYPE html>
<html>
<head>
  <!-- ECharts CDN -->
  <!-- Styles -->
</head>
<body>
  <div class="container">
    <h1>Analytics Dashboard</h1>
    <div id="analytics-content">
      <!-- Analysis sections appended here -->
      <div class="analysis-section" id="analysis-[unique-id]">
        <!-- Section content -->
      </div>
    </div>
  </div>
  <script>
    // Chart initialization code
  </script>
</body>
</html>
```

**Key Features**:
- Single file containing all analyses
- Each analysis is a separate section
- Sections have unique IDs
- Timestamps for each analysis
- Responsive design
- Interactive ECharts visualizations

## 🎯 Usage Patterns

### Pattern 1: Single Analysis Session
```
1. User: "Analyze data.csv"
2. Cursor creates analytics_dashboard.html
3. Browser opens showing results
```

### Pattern 2: Multiple Analyses
```
1. User: "Analyze data.csv"
2. Cursor appends to dashboard
3. User: "Show correlation"
4. Cursor appends new section
5. Dashboard grows with all analyses
```

### Pattern 3: Updating Analysis
```
1. User: "Update the correlation chart"
2. Cursor finds section by ID
3. Updates chart configuration
4. Reloads browser
```

## 🔧 Customization Points

### 1. Dashboard Styling
**File**: `visualizations/analytics_dashboard.html`
**Location**: `<style>` section
**Customize**: Colors, fonts, layout, spacing

### 2. Chart Defaults
**File**: `.cursor/rules/echarts-only.mdc`
**Customize**: Default chart options, colors, tooltips

### 3. Approved Packages
**File**: `.cursor/rules/package-policy.mdc`
**Customize**: Add/remove approved Python packages

### 4. Workflow Behavior
**File**: `.cursor/rules/browser-analytics-canvas.mdc`
**Customize**: Dashboard structure, update patterns

## 📊 Data Flow

```
User Request
    ↓
Cursor reads rules
    ↓
Processes data (Python)
    ↓
Generates analysis
    ↓
Creates/updates dashboard HTML
    ↓
Starts HTTP server (if needed)
    ↓
Opens browser
    ↓
Displays results
```

## 🎨 Visualization Components

### Chart Containers
- Each analysis section can have multiple charts
- Charts are initialized with unique IDs
- Responsive sizing (100% width, 500px height default)

### Stat Cards
- Summary metrics displayed as cards
- Gradient backgrounds
- Large, readable numbers

### Section Structure
- Title
- Timestamp
- Description
- Charts/visualizations
- Insights text

## 🔐 Security Considerations

- **Data Files**: Consider adding `data/` to `.gitignore` if sensitive
- **Dashboard**: HTML files may contain data - review before sharing
- **CDN**: ECharts loads from CDN (jsdelivr.net) - verify if needed

## 📦 Dependencies

### Required
- **Cursor**: AI code editor (cursor.sh)
- **Python 3**: For data processing (optional)
- **Web Browser**: For viewing dashboard

### Optional Python Packages
- pandas: Data manipulation
- numpy: Numerical computing
- scipy: Scientific computing
- statsmodels: Statistical modeling
- scikit-learn: Machine learning

### External (CDN)
- **ECharts 5.4.3**: Loaded from jsdelivr.net CDN

## 🚀 Getting Started Checklist

- [ ] Copy `.cursor/rules/` to your project
- [ ] Create `data/`, `analysis/`, `visualizations/` directories
- [ ] Add your data files to `data/`
- [ ] Install Python packages (optional)
- [ ] Test with: "Analyze this data"
- [ ] Verify dashboard opens in browser
- [ ] Customize rules if needed

---

For more details, see [README.md](README.md) and [QUICKSTART.md](QUICKSTART.md)
