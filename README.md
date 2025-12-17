# 🤖 AWS Enterprise Database Migration Analyzer AI v3.0

<div align="center">

![Python](https://img.shields.io/badge/Python-3.9+-3776ab?style=for-the-badge&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-1.28+-ff4b4b?style=for-the-badge&logo=streamlit&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-RDS%20%7C%20EC2%20%7C%20FSx-232f3e?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![Claude AI](https://img.shields.io/badge/Claude%20AI-Sonnet%203.5-d97706?style=for-the-badge&logo=anthropic&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-Auth-ffca28?style=for-the-badge&logo=firebase&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)

**Professional-Grade Migration Analysis • AI-Powered Insights • Real-time AWS Integration**

[Features](#-features) • [Installation](#-installation) • [Configuration](#-configuration) • [Usage](#-usage) • [Architecture](#-architecture) • [Screenshots](#-screenshots) • [Contributing](#-contributing)

---

</div>

## 📋 Overview

**AWS Enterprise Database Migration Analyzer AI** is a comprehensive, enterprise-grade Streamlit application that leverages **Claude AI (Anthropic)** to provide intelligent database migration analysis, cost optimization recommendations, and detailed AWS architecture planning.

Built for database administrators, cloud architects, and enterprise teams planning migrations to AWS RDS, EC2, or FSx storage solutions, this tool combines real-time AWS integration with AI-powered insights to deliver actionable migration strategies.

---

## ✨ Features

### 🧠 AI-Powered Analysis
- **Claude AI Integration** — Leverages Anthropic's Claude 3.5 Sonnet for intelligent migration recommendations
- **Natural Language Insights** — Get human-readable explanations of complex migration scenarios
- **Risk Assessment** — AI-driven evaluation of migration risks and mitigation strategies
- **Performance Predictions** — Machine learning-based performance forecasting post-migration

### 📊 Comprehensive Dashboard
- **Migration Readiness Score** — Visual assessment of your database's migration preparedness
- **Real-time Metrics** — Live monitoring of database performance indicators
- **Interactive Visualizations** — Plotly-powered charts and graphs for data exploration
- **Multi-tab Interface** — Organized views for different analysis aspects

### 💰 Cost Analysis & Optimization
- **TCO Calculator** — Total Cost of Ownership comparison between on-premises and AWS
- **Instance Sizing Recommendations** — AI-optimized EC2/RDS instance selection
- **Reserved Instance Analysis** — Savings calculations for 1-year and 3-year commitments
- **Cost Breakdown Reports** — Detailed monthly and annual cost projections

### 🏗️ AWS Architecture Planning
- **RDS Configuration** — Optimal database instance and storage recommendations
- **EC2 Sizing** — Compute resource planning for self-managed databases
- **FSx Comparisons** — File storage analysis for Windows and Lustre workloads
- **Network Architecture** — VPC, subnet, and security group recommendations

### 📄 Professional Reporting
- **Executive Reports** — High-level summaries for leadership and stakeholders
- **Technical Reports** — Detailed specifications for implementation teams
- **PDF Export** — Professional, branded PDF reports with charts and tables
- **Compliance Documentation** — Security and compliance requirement mapping

### 🔐 Enterprise Security
- **Firebase Authentication** — Secure user authentication and session management
- **Role-based Access** — Admin panel for user management
- **API Key Protection** — Secure storage for AWS and Anthropic credentials
- **Audit Logging** — Track user activities and analysis runs

---

## 🛠️ Installation

### Prerequisites

- Python 3.9 or higher
- AWS Account with appropriate IAM permissions
- Anthropic API key for Claude AI
- Firebase project (for authentication)

### Quick Start

```bash
# Clone the repository
git clone https://github.com/yourusername/aws-db-migration-analyzer.git
cd aws-db-migration-analyzer

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the application
streamlit run streamlit_app.py
```

### Docker Deployment

```bash
# Build the Docker image
docker build -t aws-migration-analyzer .

# Run the container
docker run -p 8501:8501 \
  -e ANTHROPIC_API_KEY=your_api_key \
  -e AWS_ACCESS_KEY_ID=your_access_key \
  -e AWS_SECRET_ACCESS_KEY=your_secret_key \
  aws-migration-analyzer
```

---

## ⚙️ Configuration

### Environment Variables

Create a `.env` file in the project root:

```env
# Anthropic AI Configuration
ANTHROPIC_API_KEY=your_anthropic_api_key

# AWS Configuration
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
AWS_DEFAULT_REGION=us-east-1

# Firebase Configuration (optional - for authentication)
FIREBASE_PROJECT_ID=your_firebase_project
FIREBASE_PRIVATE_KEY=your_private_key
FIREBASE_CLIENT_EMAIL=your_client_email
```

### Streamlit Secrets

For Streamlit Cloud deployment, configure secrets in `.streamlit/secrets.toml`:

```toml
[anthropic]
api_key = "your_anthropic_api_key"

[aws]
access_key_id = "your_aws_access_key"
secret_access_key = "your_aws_secret_key"
region = "us-east-1"
```

---

## 🚀 Usage

### 1. Launch the Application

```bash
streamlit run streamlit_app.py
```

The application will open in your default browser at `http://localhost:8501`.

### 2. Configure Database Parameters

Use the sidebar to input your current database specifications:

| Parameter | Description | Example |
|-----------|-------------|---------|
| Database Engine | Source database type | SQL Server, Oracle, PostgreSQL |
| Database Size (GB) | Total storage used | 500 |
| RAM (GB) | Current memory allocation | 32 |
| CPU Cores | Processor cores | 8 |
| Environment | Deployment type | Production, Development, Staging |
| IOPS Requirements | I/O operations per second | 3000 |

### 3. Run AI Analysis

Click **"🚀 Run Enhanced AI Migration Analysis"** to start the comprehensive analysis. The AI will evaluate:

- Migration complexity and timeline
- AWS service recommendations
- Cost projections and savings
- Risk factors and mitigations
- Performance expectations

### 4. Explore Results

Navigate through the analysis tabs:

| Tab | Content |
|-----|---------|
| 📊 Dashboard | Overview metrics and readiness score |
| 🧠 AI Insights | Claude AI-generated recommendations |
| 🌐 Network | Network architecture planning |
| 💰 Cost Analysis | TCO and savings calculations |
| 💻 OS Performance | Operating system optimization |
| 🎯 Sizing | AWS instance recommendations |
| 🗄️ FSx | File storage comparisons |
| 🤖 Agents | Scaling optimizer agents |
| 📄 Reports | PDF report generation |

### 5. Generate Reports

Export professional PDF reports for stakeholder presentations:

- **Executive Report** — Strategic summary for leadership
- **Technical Report** — Detailed specifications for engineering

---

## 🏛️ Architecture

```
┌─────────────────────────────────────────────────────────────────────────┐
│                         User Interface (Streamlit)                       │
├─────────────────────────────────────────────────────────────────────────┤
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐    │
│  │  Dashboard  │  │ AI Insights │  │    Cost     │  │   Reports   │    │
│  │    Tab      │  │    Tab      │  │  Analysis   │  │    Tab      │    │
│  └─────────────┘  └─────────────┘  └─────────────┘  └─────────────┘    │
├─────────────────────────────────────────────────────────────────────────┤
│                        Analysis Engine Layer                             │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │              EnhancedMigrationAnalyzer Class                       │  │
│  │  • comprehensive_ai_migration_analysis()                           │  │
│  │  • cost_calculation_engine()                                       │  │
│  │  • instance_sizing_algorithm()                                     │  │
│  └───────────────────────────────────────────────────────────────────┘  │
├─────────────────────────────────────────────────────────────────────────┤
│                        External Services                                 │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐    │
│  │  Anthropic  │  │    AWS      │  │  Firebase   │  │  ReportLab  │    │
│  │ Claude API  │  │   Boto3     │  │    Auth     │  │     PDF     │    │
│  └─────────────┘  └─────────────┘  └─────────────┘  └─────────────┘    │
└─────────────────────────────────────────────────────────────────────────┘
```

### Core Components

| Component | Technology | Purpose |
|-----------|------------|---------|
| Frontend | Streamlit | Interactive web interface |
| AI Engine | Anthropic Claude 3.5 | Intelligent analysis and recommendations |
| Cloud Integration | Boto3 | AWS service interaction |
| Authentication | Firebase Admin | User management and security |
| Visualization | Plotly, Matplotlib | Charts and interactive graphs |
| Reporting | ReportLab | Professional PDF generation |
| Data Processing | Pandas, NumPy | Data manipulation and analysis |

---

## 📸 Screenshots

### Main Dashboard
> Migration readiness overview with key metrics and visual indicators

![Main Dashboard](assets/screenshots/dashboard.svg)

### AI Insights Panel
> Claude AI-generated recommendations with detailed explanations

![AI Insights](assets/screenshots/ai-insights.svg)

### Cost Analysis
> TCO comparison with interactive cost breakdown charts

![Cost Analysis](assets/screenshots/cost-analysis.svg)

### PDF Report Export
> Professional, branded reports for stakeholder presentations

![PDF Reports](assets/screenshots/pdf-reports.svg)

---

## 📦 Dependencies

### Core Framework
```
streamlit>=1.28.0
```

### Data & Analysis
```
pandas>=2.0.0
numpy>=1.24.0
scipy>=1.11.0
```

### Visualization
```
plotly>=5.15.0
matplotlib>=3.7.0
seaborn>=0.12.0
```

### AI & Cloud
```
anthropic>=0.40.0  # Critical: Required for Claude 3.5 Sonnet
boto3>=1.34.0
botocore>=1.34.0
```

### Authentication & Security
```
firebase-admin>=6.2.0
google-cloud-firestore>=2.11.1
google-auth>=2.17.0
```

### Reporting
```
reportlab>=3.6.0
openpyxl>=3.1.0
xlsxwriter>=3.1.0
```

> ⚠️ **Important**: The `anthropic>=0.40.0` version is critical. Earlier versions do not support Claude 3.5 Sonnet and will result in 404 errors.

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Development Setup

```bash
# Install development dependencies
pip install -r requirements.txt
pip install pytest black flake8

# Run linting
flake8 streamlit_app.py
black streamlit_app.py

# Run tests
pytest tests/
```

---

## 📝 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- [Anthropic](https://www.anthropic.com/) for Claude AI
- [Streamlit](https://streamlit.io/) for the amazing framework
- [AWS](https://aws.amazon.com/) for cloud infrastructure
- [Firebase](https://firebase.google.com/) for authentication services

---

## 📧 Support

For questions, issues, or feature requests:

- **GitHub Issues** — [Create an issue](https://github.com/yourusername/aws-db-migration-analyzer/issues)
- **Email** — your.email@example.com

---

<div align="center">

**Built with ❤️ for Cloud Migration Excellence**

⭐ Star this repository if you find it helpful!

</div>
