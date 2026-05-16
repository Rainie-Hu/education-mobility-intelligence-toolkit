# International Education Mobility Intelligence Toolkit

A practical analytical toolkit that integrates and standardizes international education and credential-related datasets to support mobility analysis, forecasting, and credential evaluation intelligence.

## Features

- **Dataset Crosswalks** — Standardized mappings between UNESCO, Open Doors, IPEDS, and OECD datasets
- **Country Mapping** — ISO 3166-1 compliant country name and code standardization
- **Institution Mapping** — Fuzzy-matched institution name resolution with master registry
- **Mobility Dashboard** — Interactive visualizations of international student mobility flows
- **Credential Evaluation Trends** — Historical trend analysis with change-point detection
- **Forecasting** — Demand forecasting using exponential smoothing, ARIMA, and gradient boosting
- **Report Generation** — Standardized analytical report templates (PDF, HTML, Markdown)

## Project Structure

```
education-mobility-intelligence-toolkit/
├── src/
│   ├── parsers/          # Data file parsers (UNESCO, Open Doors, IPEDS, OECD)
│   ├── crosswalks/       # Dataset crosswalk mapping engine
│   ├── mappers/          # Country and institution standardization
│   ├── dashboard/        # Visualization and dashboard engine
│   ├── forecasting/      # Time-series forecasting modules
│   ├── reports/          # Report template engine
│   └── quality/          # Data quality and audit modules
├── data/
│   ├── raw/              # Raw source data files
│   ├── processed/        # Cleaned and standardized data
│   ├── mappings/         # Country/institution mapping tables
│   └── config/           # YAML configuration files
├── tests/                # Unit and property-based tests
├── docs/                 # Documentation
├── notebooks/            # Jupyter notebooks for exploration
└── reports/              # Generated report outputs
```

## Getting Started

### Prerequisites

- Python 3.10+
- pip or conda

### Installation

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/education-mobility-intelligence-toolkit.git
cd education-mobility-intelligence-toolkit

# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

### Quick Start

```python
from src.parsers import UNESCOParser
from src.mappers import CountryMapper

# Parse a UNESCO data file
parser = UNESCOParser()
dataset = parser.parse("data/raw/unesco_mobility_2023.csv")

# Standardize country names
mapper = CountryMapper()
standardized = mapper.standardize(dataset, country_column="country_name")
```

## Data Sources

| Source | Description | URL |
|--------|-------------|-----|
| UNESCO UIS | International education statistics | [uis.unesco.org](http://uis.unesco.org) |
| Open Doors | IIE international student data | [opendoorsdata.org](https://opendoorsdata.org) |
| IPEDS | U.S. postsecondary education data | [nces.ed.gov/ipeds](https://nces.ed.gov/ipeds) |
| OECD | Education at a Glance indicators | [oecd.org/education](https://www.oecd.org/education) |

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](docs/CONTRIBUTING.md) for guidelines.

## License

This project is licensed under the MIT License - see [LICENSE](LICENSE) for details.
