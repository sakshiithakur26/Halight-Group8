# Halight Information Radiator AI - Live KPI Dashboards

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![AWS](https://img.shields.io/badge/AWS-Athena-orange.svg)](https://aws.amazon.com/athena/)
[![Streamlit](https://img.shields.io/badge/Streamlit-Dashboard-red.svg)](https://streamlit.io/)

## 📋 Project Overview

EdTech LMS for Halight: Real-time dashboards pulling KPIs (user engagement, client health) from Amazon Athena with ML trends/anomalies. This platform provides actionable insights into user behavior patterns, gamification performance, verification workflows, referral effectiveness, and retention dynamics through interactive dashboards and in-depth exploratory analysis.

**Epic:** Information Radiator AI - Live KPI Dashboards  
**Problem Solved:** Scattered KPIs delay decisions; enables shared real-time visibility for data-driven decision making.

---

## 🔗 Project Links

**Jira Board:** [https://ahmadfaiyaz24.atlassian.net/jira/software/projects/SAM1/boards/1](https://ahmadfaiyaz24.atlassian.net/jira/software/projects/SAM1/boards/1)

---

## 🎯 Key Features

- **Real-time Data Pipeline**: Direct connection to AWS Athena database for live analytics from 32+ tables
- **User Engagement Tracking**: Monitor sign-ups, logins, learning completions, and gamification achievements
- **ML-Powered Insights**: Automated trend detection and anomaly identification
- **Behavioral Analytics**: Deep-dive into user activity patterns, point balances, and engagement scores
- **Verification & Referral Analytics**: Track verification completion rates and referral program ROI
- **Geographical Insights**: Analyze user distribution across countries, regions, and locations
- **Retention Analysis**: Identify at-risk users, lost users, and reactivation opportunities
- **Gamification Metrics**: Evaluate achievement completions, badges, ranks, and reward claims
- **Interactive Dashboards**: Visual representation of KPIs through Streamlit/Plotly Dash

---

## 🗂️ Repository Structure

```
halight-business-analytics/
├── .gitignore                          # Git ignore file
├── README.md                           # Project documentation
├── requirements.txt                    # Python dependencies
├── .env.example                        # Environment variables template
│
├── data/                               # Data directory
│   ├── samples/                        # Athena sample data
│   └── mocks/                          # Mock data for testing
│
├── src/                                # Source code
│   ├── etl/                           # ETL scripts
│   │   ├── data_extraction.py         # AWS Athena data extraction
│   │   └── data_preprocessing.py      # Data cleaning and transformation
│   └── ml/                            # Machine learning models
│       ├── trend_analysis.py          # Trend detection algorithms
│       └── anomaly_detection.py       # Anomaly identification
│
├── dashboards/                         # Dashboard applications
│   ├── streamlit_app.py               # Main Streamlit dashboard
│   └── components/                     # Dashboard components
│       ├── user_engagement.py
│       ├── client_health.py
│       └── kpi_metrics.py
│
├── Exploratory_Analysis/               # Jupyter notebooks for EDA
│   ├── EDA_users_table.ipynb         # User demographics and behavior analysis
│   ├── EDA_rcs_lifetime_stats_by_month_v_table.ipynb  # Monthly engagement metrics
│   └── EDA_rcs_historic_users.ipynb  # Historical user status analysis
│
├── docs/                               # Documentation
│   ├── milestone_reports/             # Project milestone documentation
│   ├── Data_Preparation_Guide.md      # Data extraction and preparation guide
│   ├── Data_Dictionary.md             # Database schema and field descriptions
│   └── Users_Data_Cleaning_Report.docx
│
└── assets/                             # Supporting files
    └── images/                         # Screenshots and visuals
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- AWS Account with Athena access
- AWS Access Key ID and Secret Access Key
- Git installed on your machine

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Aum-gajjar/halight-business-analytics.git
   cd halight-business-analytics
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv

   # On Windows
   venv\Scripts\activate

   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**

   Create a `.env` file in the project root directory:
   ```env
   AWS_Acess_Key_ID=your_aws_access_key_id
   AWS_Secret_Access_Key=your_aws_secret_access_key
   AWS_REGION=us-east-1
   ATHENA_S3_OUTPUT=s3://your-output-bucket/
   ATHENA_DATABASE=s3_atmos_stclair
   ```

5. **Run the Streamlit dashboard**
   ```bash
   streamlit run dashboards/streamlit_app.py
   ```

6. **Run exploratory analysis notebooks**
   ```bash
   jupyter notebook Exploratory_Analysis/
   ```

---

## 📊 Data Sources

The project connects to AWS Athena database (`s3_atmos_stclair`) containing **32 tables**:

### Core Tables Analyzed

| Table Name | Description | Records Analyzed |
|------------|-------------|------------------|
| `users` | User demographics, account status, verification, and engagement metrics | 1.18M+ users |
| `rcs_lifetime_stats_by_month_v` | Monthly aggregated user engagement statistics | 978 monthly records |
| `rcs_historic_users` | Historical user status transitions and login patterns | 1000+ status changes |
| `achievement_user_completions` | Gamification achievement tracking | - |
| `reward_user_claims_v` | Reward redemption data | - |
| `li_attempts` | Learning module completion attempts | - |
| `instances_v` | Client and site configuration details | Multiple clients |

*For complete table schema and field descriptions, refer to [Data Dictionary](docs/Data_Dictionary.md)*

---

## 🛠️ Tech Stack

| Category | Technologies |
|----------|-------------|
| **Programming** | Python 3.8+ |
| **Data Processing** | Pandas, NumPy, scikit-learn |
| **Visualization** | Matplotlib, Seaborn, Plotly |
| **Dashboard** | Streamlit / PowerBI / Flask |
| **Cloud & Database** | AWS Athena, AWS S3, Boto3, AWS Wrangler |
| **ETL** | SQL (Athena queries) |
| **Environment Management** | python-dotenv |
| **Deployment** | TBD |
| **Version Control** | Git, GitHub |


---

## 👥 Team

**Group 8** - This project is a collaborative effort by 5 members:

- **[Aum Gajjar]** 
- **[Souravdeep Singh]** 
- **[Priyanka Sharma]** 
- **[Sakshi Sakshi]** 
- **[Faiyaz Ahemad]**  

*Team coordination managed through [Jira Board](https://ahmadfaiyaz24.atlassian.net/jira/software/projects/SAM1/boards/1)*

---

## 📝 Documentation

- [Milestone Reports](docs/milestone_reports/)
- [Data Preparation Guide](docs/Data_Preparation_Guide.md)
- [Data Dictionary](docs/Data_Dictionary.md)
- [User Data Cleaning Report](docs/Users_Data_Cleaning_Report.docx)

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Check the [Jira Board](https://ahmadfaiyaz24.atlassian.net/jira/software/projects/SAM1/boards/1) for assigned tasks
2. Fork the repository
3. Create a feature branch (`git checkout -b feature/JIRA-TICKET-ID`)
4. Commit your changes (`git commit -m 'JIRA-XXX: Add feature description'`)
5. Push to the branch (`git push origin feature/JIRA-TICKET-ID`)
6. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- St. Clair College - Data Analytics for Business Program
- Halight Team for providing access to production data
- AWS for cloud infrastructure support
- Project mentors and instructors

---

## 🔗 Related Resources

- [AWS Athena Documentation](https://docs.aws.amazon.com/athena/)
- [Streamlit Documentation](https://docs.streamlit.io/)
- [Plotly Dash Documentation](https://dash.plotly.com/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [scikit-learn Documentation](https://scikit-learn.org/)

---

*Last Updated: February 09, 2026*  
*Project Status: Active Development*
