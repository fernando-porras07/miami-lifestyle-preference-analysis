# Miami-Dade Lifestyle Preference Analysis

Exploratory data analysis of lifestyle preference trends among adults aged 30–35 in Miami-Dade County. The goal is to identify which lifestyle niches could represent the strongest opportunities for a future niche-based social connection app.

## Project Objective

This project analyzes and compares five lifestyle categories among adults aged 30–35 in Miami-Dade County:

- Fitness
- Beach
- Day Weekend Activities
- Trips Outside Miami
- Nightlife

The analysis identifies which of these niches could serve as the strongest initial core communities for a niche-based social connection app.

## Dataset

The dataset contains **1,000 synthetic survey responses** generated with a fixed random seed (`np.random.seed(42)`) for full reproducibility. Each row represents one simulated survey response.

| Column | Description |
|---|---|
| `respondent_id` | Unique identifier for each response |
| `age` | Respondent age (30–35) |
| `county` | County of residence (Miami-Dade County) |
| `primary_preference` | Primary lifestyle preference (one of the five categories) |
| `app_interest` | Interest level in a social connection app (High / Medium / Low) |
| `weekend_preference` | Preferred weekend timing (Daytime / Nighttime / Both) |
| `monthly_activity_budget` | Estimated monthly activity budget in USD ($80–$400) |

## Tools and Libraries

- Python 3
- pandas — data manipulation and aggregation
- NumPy — synthetic data generation
- Matplotlib — data visualization
- Jupyter Notebook

## Analysis Workflow

1. **Data generation** — creation of the 1,000-row synthetic dataset with seeded randomness.
2. **Data validation** — inspection of dataset shape, structure, and data types.
3. **Preference distribution** — response counts and preference share (%) per category, visualized with a pie chart.
4. **App interest analysis** — cross-tabulation of app interest level by lifestyle preference, visualized with a grouped bar chart.
5. **Budget analysis** — average monthly activity budget by category, visualized with a bar chart.
6. **Export** — charts saved as PNG files and the dataset exported to CSV.

## Visualizations

| Chart | Output file |
|---|---|
| Lifestyle preference share (pie chart) | `charts/preference_pie_chart.png` |
| App interest level by lifestyle preference | `charts/app_interest_by_category.png` |
| Average monthly activity budget by category | `charts/budget_by_category.png` |

## Project Structure

```
miami-lifestyle-analysis/
├── charts/
│   ├── preference_pie_chart.png
│   ├── app_interest_by_category.png
│   └── budget_by_category.png
├── data/
│   └── miami_lifestyle_synthetic_survey.csv
├── notebooks/
│   └── miami_lifestyle_analysis.ipynb
└── README.md
```

## Key Findings

1. **Fitness** ranked as the strongest preference category among the simulated respondents.
2. **Beach activities** ranked second, showing strong interest in outdoor and lifestyle-based social experiences.
3. **Day Weekend Activities** ranked third, suggesting potential demand for daytime social plans such as restaurants, museums, brunch, and cultural activities.
4. **Trips Outside Miami** ranked fourth, showing moderate interest in short-distance travel and weekend escapes.
5. **Nightlife** ranked last, suggesting this audience may be less focused on party-centered social experiences compared to wellness, beach, and daytime activities.

## Business Recommendation

Based on the preference ranking, a future niche-based social connection app targeting adults aged 30–35 in Miami-Dade County should prioritize **Fitness**, **Beach**, and **Day Weekend Activities** as its first core communities.

A strong initial product strategy could focus on helping users connect through fitness groups, beach activities, brunch plans, daytime restaurant meetups, museum visits, cultural activities, and short weekend trips outside Miami. Nightlife could be included as a secondary category, but it should not be the main positioning of the app based on this analysis.

## How to Run

1. Install the dependencies:

   ```bash
   pip install pandas numpy matplotlib jupyter
   ```

2. Launch the notebook from the project root:

   ```bash
   jupyter notebook notebooks/miami_lifestyle_analysis.ipynb
   ```

3. Run all cells. The notebook writes outputs to `../charts/` and `../data/`, so make sure both folders exist at the project root before running.

## Disclaimer

All information in this analysis was provided by a third party responsible for data collection via interactive advertisements. The content consists of statistics derived from that data; the recommendations and conclusions presented are based on information provided by the data contributor, and no specific results or definitive facts are guaranteed. Any actions taken based on this analysis are the sole and exclusive responsibility of the person taking such action.
