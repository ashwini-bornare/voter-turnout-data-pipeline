# Voter Turnout Analysis - Maharashtra Parliamentary Constituencies

Analysis of voter turnout patterns across 10 parliamentary constituencies in Maharashtra, India for the 2014, 2019, and 2024 General Elections.

## Project Structure

```
├── data/                                    # Raw election data
│   ├── pc_wise_voters_turn_out_2014.xlsx
│   ├── pc_wise_voters_turn_out_2019.xls
│   └── pc_wise_voters_turn_out_2024.xls
├── assignment-docs/                         # Assignment requirements
├── step_1_Creation of data set.ipynb        # Data preparation notebook
├── step_2_data_visualization.ipynb          # Bokeh visualizations
├── step_2_Visualization Development.ipynb   # Alternate visualization notebook
├── step_3_Powerbi Dashboard.pbix            # Power BI dashboard
├── step_3_Powerbi Dashboard.pdf             # Dashboard PDF export
├── voters_turnout_10_constituencies.csv     # Processed dataset
└── README.md
```

## Constituencies Analyzed

Dhule, Jalgaon, Nagpur, Dindori, Nashik, Pune, Baramati, Shirur, Ahmednagar, Shirdi

## Dataset Variables

| Column | Description |
|--------|-------------|
| STATE_NAME | State (Maharashtra) |
| PC_NO | Constituency number |
| PC_NAME | Constituency name |
| ELECTORS | Total registered voters |
| EVM_MALE / EVM_FEMALE / EVM_OTHERS | Votes cast by gender |
| EVM_TOTAL | Total EVM votes |
| POSTAL_VOTES | Postal ballot count |
| TOTAL_VOTERS | Total votes cast |
| VOTER_TURN_OUT_PERCENT | Overall turnout % |
| VOTER_TURNOUT_MALE_PERCENT | Male turnout % |
| VOTER_TURNOUT_FEMALE_PERCENT | Female turnout % |
| YEAR | Election year (2014/2019/2024) |
| MALE_ELECTORS / FEMALE_ELECTORS | Registered voters by gender (derived) |

## Workflow

### Step 1: Data Preparation
- Load raw Excel data for 2014, 2019, 2024
- Clean and standardize column formats
- Handle missing state names in 2024 data
- Filter for 10 selected constituencies
- Derive gender-wise elector counts
- Export to `voters_turnout_10_constituencies.csv`

### Step 2: Visualization (Bokeh)
- **Voter Turnout Over Time** - Line chart showing yearly trends
- **Gender-wise Turnout** - Grouped bar chart comparing male vs female participation
- **Constituency × Time Distribution** - Scatter plot of turnout by constituency and year
- **Constituency × Gender Distribution** - Grouped bars for gender comparison per constituency

### Step 3: Power BI Dashboard
Interactive dashboard combining all visualizations for presentation.

## Requirements

```
pandas
openpyxl
xlrd
bokeh
jupyter
```

Install with:
```bash
pip install pandas openpyxl xlrd bokeh jupyter
```

## Usage

1. Run `step_1_Creation of data set.ipynb` to generate the processed CSV
2. Run `step_2_data_visualization.ipynb` to create Bokeh charts
3. Open `step_3_Powerbi Dashboard.pbix` in Power BI Desktop

## Data Source

Election Commission of India - Parliamentary Constituency-wise voter turnout data.
