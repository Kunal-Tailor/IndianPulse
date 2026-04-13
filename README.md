# IndianPulse - Economic Dashboard

A modern, lightweight economic dashboard for India that visualizes key economic indicators with an interactive HTML/CSS/JavaScript frontend powered by a Flask backend.

## 🚀 Features

- **11 Key Economic Indicators**: GDP, CPI, GST, Unemployment, Forex Reserves, Industrial Production, Repo Rate, Trade Balance, Financial Inclusion, Digital Payments, and Composite Leading Indicator
- **Interactive Charts**: Line, Area, Bar, and Scatter charts using Chart.js
- **Real-time Data Visualization**: Time-series data with advanced filtering and statistics
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Dark/Light Theme**: Toggle between themes with persistent local storage
- **Export Functionality**: Download charts as PNG images
- **Clean, Modern UI**: Accessible interface with smooth animations and intuitive navigation

## 📊 Tech Stack Composition

```
HTML      51.6%  ████████████████████████░
Python    32.0%  ████████████████░
CSS       7.3%   ███░
JavaScript 5.2%  ██░
Shell     3.9%   ██░
```

### Frontend (51.6% HTML + 5.2% JS + 7.3% CSS)
- **HTML5** with semantic markup
- **CSS3** with CSS Variables, Grid, and Flexbox
- **Vanilla JavaScript** (ES2020+) for interactivity
- **Chart.js** for interactive data visualization
- **Responsive Design** system

### Backend (32% Python)
- **Python 3.10+**
- **Flask** lightweight web framework
- **Pandas** for data processing and manipulation
- **NumPy** for numerical operations
- **Scikit-learn** for advanced analytics
- **Matplotlib** for server-side visualization

### DevOps (3.9% Shell)
- Bash scripts for automation
- Deployment and setup scripts
- Development environment utilities

## 📁 Project Structure

```
IndianPulse/
├── backend/                       # Python/Flask Backend (32%)
│   ├── app.py                    # Flask application entry point
│   ├── config.py                 # Configuration and settings
│   ├── requirements.txt          # Python dependencies
│   ├── api/
│   │   ├── __init__.py
│   │   ├── indicators.py         # Indicators API endpoints
│   │   └── charts.py             # Chart generation endpoints
│   ├── data/
│   │   ├── generator.py          # Sample data generation
│   │   └── sample_data/          # CSV/JSON data files
│   └── analytics/
│       ├── __init__.py
│       ├── processing.py         # Data processing functions
│       └── forecasting.py        # Forecasting algorithms
├── frontend/                      # HTML/CSS/JS Frontend (64.1%)
│   ├── index.html                # Main HTML page (51.6%)
│   ├── css/
│   │   └── styles.css            # Main stylesheet (7.3%)
│   ├── js/
│   │   ├── api.js                # API client (5.2%)
│   │   ├── ui.js                 # UI utilities
│   │   ├── charts.js             # Chart management
│   │   └── main.js               # Main application logic
│   └── assets/
│       └── logo.svg              # Application logo
├── scripts/                       # Shell scripts (3.9%)
│   ├── setup.sh                  # Setup automation
│   └── deploy.sh                 # Deployment scripts
└── README.md                      # Documentation
```

## 🚀 Quick Start

### Prerequisites
- Python 3.10 or higher
- pip (Python package installer)
- Modern web browser (Chrome, Firefox, Safari, Edge)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Kunal-Tailor/IndianPulse.git
   cd IndianPulse
   ```

2. **Create and activate virtual environment**
   ```bash
   # Create virtual environment
   python -m venv venv
   
   # Activate (choose based on your OS)
   # Windows:
   venv\Scripts\activate
   # macOS/Linux:
   source venv/bin/activate
   ```

3. **Install Python dependencies**
   ```bash
   pip install -r backend/requirements.txt
   ```

4. **Generate sample data**
   ```bash
   python backend/data/generator.py --generate
   ```

5. **Start the Flask server**
   ```bash
   python backend/app.py
   ```

6. **Access the application**
   Open your browser and navigate to `http://localhost:5000`

## 📊 Available Economic Indicators

| Indicator | Description | Unit | Frequency | Source |
|-----------|-------------|------|-----------|--------|
| GDP Growth Rate | Quarterly GDP growth | % | Quarterly | RBI |
| Consumer Price Index | Monthly inflation rate | Index | Monthly | MOSPI |
| GST Collections | Monthly GST revenue | ₹ Crores | Monthly | CBIC |
| Unemployment Rate | Monthly unemployment | % | Monthly | CMIE |
| Foreign Exchange Reserves | Weekly forex reserves | USD Billion | Weekly | RBI |
| Index of Industrial Production | Monthly IIP growth | Index | Monthly | MOSPI |
| Repo Rate | Central bank policy rate | % | Monthly | RBI |
| Trade Balance | Monthly trade balance | USD Million | Monthly | DGCI&S |
| Financial Inclusion Index | Quarterly inclusion metric | Index | Quarterly | RBI |
| Digital Payment Volume | UPI/Digital transactions | ₹ Crores | Monthly | NPCI |
| Composite Leading Indicator | Economic trend indicator | Index | Monthly | OECD |

## 🎨 Key Features

### 📈 Interactive Dashboard
- **Indicator Selection**: Choose from 11 carefully curated economic indicators
- **Category Filtering**: Group indicators by Growth, Inflation, Employment, Financial, etc.
- **Time Range Controls**: View data for 1Y, 2Y, 5Y, or custom date ranges
- **Chart Type Switching**: Toggle between Line, Area, Bar, and Scatter charts

### 📊 Data Visualization
- **Real-time Charts**: Interactive Chart.js visualizations with hover tooltips
- **Statistics Cards**: Display latest values, averages, min/max trends
- **Data Table**: Recent data points with change indicators (↑/↓)
- **PNG Export**: Download charts as high-quality images

### 🎯 User Experience
- **Responsive Layout**: Adapts to all screen sizes seamlessly
- **Theme Toggle**: Light/Dark mode with persistent storage
- **Keyboard Shortcuts**: Ctrl+T to toggle theme instantly
- **Loading States**: Visual feedback during data fetches
- **Error Handling**: User-friendly error messages and recovery

## 🔧 API Endpoints

### Indicators API
- `GET /api/v1/indicators/manifest` - List all available indicators
- `GET /api/v1/indicators/{id}/series` - Get time series data for an indicator
- `GET /api/v1/indicators/{id}/stats` - Get statistical summary
- `GET /api/v1/indicators/compare` - Compare multiple indicators

### Charts API
- `GET /api/v1/charts/{id}.png` - Generate PNG chart
- `GET /api/v1/charts/export` - Export chart data

### Health Check
- `GET /api/v1/health` - Service health status

## 📖 Usage Examples

### View GDP Trends (Last 5 Years)
1. Select **"GDP Growth Rate"** from indicators
2. Set time range to **"5 Years"**
3. Choose **"Line"** chart type
4. Click **"Update Chart"**

### Compare Economic Indicators
1. Select indicators from multiple categories
2. Use comparison view for cross-sector analysis
3. Export combined visualization

### Download Chart Data
1. Load your desired indicator
2. Click **"Export"** button
3. Save as PNG for presentations/reports

## 🛠️ Development Guide

### Running in Development Mode
```bash
# Activate virtual environment first
source venv/bin/activate  # macOS/Linux
# or
venv\Scripts\activate     # Windows

# Set Flask to debug mode
export FLASK_DEBUG=True
python backend/app.py
```

### Generating Fresh Sample Data
```bash
python backend/data/generator.py --generate --overwrite
```

### Code Organization
- **Frontend**: Modular ES6+ JavaScript with separation of concerns
- **Backend**: Flask blueprints for organized API endpoints
- **Data Layer**: Pandas-based processing and CSV/JSON handling
- **Visualization**: Chart.js with custom styling and themes

## 🚀 Deployment

### Production - Gunicorn
```bash
# Install production WSGI server
pip install gunicorn

# Run application
gunicorn -w 4 -b 0.0.0.0:8000 backend.app:app
```

### Cloud Deployment Options
- **Heroku**: Deploy using Procfile
- **Render**: Connect GitHub repo for auto-deployment
- **Railway**: One-click deployment from Git
- **DigitalOcean**: Use App Platform for managed hosting
- **AWS/Azure**: Deploy using containers or traditional hosting

## 📚 Data Sources

All data in this application is synthetic but realistically modeled after:
- **RBI** - Reserve Bank of India (monetary policy, forex reserves)
- **MOSPI** - Ministry of Statistics (GDP, inflation, industrial data)
- **CBIC** - Central Board of Indirect Taxes (GST collections)
- **CMIE** - Centre for Monitoring Indian Economy (unemployment)
- **DGCI&S** - Directorate General of Commercial Intelligence (trade data)
- **NPCI** - National Payments Corporation of India (digital payments)
- **OECD** - Organisation for Economic Co-operation (economic indicators)

## 🤝 Contributing

We welcome contributions! Follow these steps:

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/amazing-feature`
3. **Commit** your changes: `git commit -m 'Add amazing feature'`
4. **Push** to branch: `git push origin feature/amazing-feature`
5. **Open** a Pull Request

### Development Tips
- Follow PEP 8 for Python code
- Use ESLint for JavaScript (or similar)
- Test on multiple browsers
- Update documentation with changes

## 📝 License

This project is licensed under the **MIT License** - see [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

Special thanks to:
- **Chart.js** - Excellent JavaScript charting library
- **Flask** - Lightweight and powerful web framework
- **Pandas & NumPy** - Robust data science libraries
- **Indian Government Data Sources** - Economic inspiration
- **Open Source Community** - For amazing tools and resources

## 📞 Support & Contact

- 📧 **Email**: support@indianpulse.com
- 🐛 **Issues**: [GitHub Issues](https://github.com/Kunal-Tailor/IndianPulse/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/Kunal-Tailor/IndianPulse/discussions)

---

<div align="center">

**Built with ❤️ for India's Economic Data Visualization**

⭐ If you find this helpful, please consider giving it a star!

</div>