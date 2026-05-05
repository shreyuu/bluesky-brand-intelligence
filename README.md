# Wired vs The Verge: Bluesky Brand Analytics

A social media analytics project comparing **Wired** and **The Verge** on Bluesky using data collection, cleaning, exploratory analysis, sentiment analysis, topic modelling, keyword networks, micro-influencer scoring, and perceptual mapping.

## Project Overview

This project analyses Bluesky posts related to two technology media brands: **Wired** and **The Verge**. The aim is to understand how both brands are discussed online and how they differ in audience engagement, sentiment, topic themes, network structure, and brand positioning.

The workflow is split into multiple notebooks, with each notebook handling a specific stage of the analytics pipeline. The project produces cleaned datasets, summary tables, visualisations, topic models, network outputs, micro-influencer recommendations, and perceptual map data.

## Objectives

- Collect Bluesky posts and profile data for Wired and The Verge.
- Clean and prepare raw post/profile datasets.
- Compare posting volume, engagement, hashtags, linked domains, and author activity.
- Analyse sentiment using labelled sentiment outputs.
- Identify themes using topic modelling and keyword analysis.
- Build keyword and network-based analytics outputs.
- Recommend potential micro-influencers for each brand.
- Create a perceptual map comparing brand positioning.
- Generate figures and tables for coursework reporting.

## Project Structure

```text
.
├── brief-material
│   └── BUSI4370_2025_26_CW2_specifications.pdf
├── data
│   ├── processed
│   │   ├── analysis_summary.json
│   │   ├── cleaning_audit.json
│   │   ├── cleaning_summary.json
│   │   ├── eda_summary.json
│   │   ├── huggingface_profiles_clean.csv
│   │   ├── influencer_recommendations.json
│   │   ├── perceptual_map_data.json
│   │   ├── sample_comparison_summary.csv
│   │   ├── sentiment_summary.json
│   │   ├── The Verge_profiles_clean.csv
│   │   ├── topic_keyword_summary.json
│   │   ├── topics_summary.json
│   │   ├── verge_posts_clean.csv
│   │   ├── verge_posts_sentiment.csv
│   │   ├── verge_posts_topics.csv
│   │   ├── verge_profiles_clean.csv
│   │   ├── wired_posts_clean.csv
│   │   ├── wired_posts_sentiment.csv
│   │   ├── wired_posts_topics.csv
│   │   └── wired_profiles_clean.csv
│   └── raw
│       ├── collection_metadata.json
│       ├── theverge_posts_raw.csv
│       ├── theverge_profiles_raw.csv
│       ├── wired_posts_raw.csv
│       └── wired_profiles_raw.csv
├── LICENSE
├── notebooks
│   ├── 01_data_collection.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_analysis.ipynb
│   ├── 04_sentiment.ipynb
│   ├── 05_topics_keywords.ipynb
│   ├── 06_network_influencer.ipynb
│   ├── 07_perceptual_map.ipynb
│   └── final_notebook.ipynb
├── outputs
│   ├── figures
│   │   ├── 02_weekly_volume.png
│   │   ├── 03_engagement_distribution_log.png
│   │   ├── 03b_posting_hour_distribution.png
│   │   ├── 03c_posting_weekday_heatmap.png
│   │   ├── 04_zero_engagement_share.png
│   │   ├── 05_engagement_composition.png
│   │   ├── 05_top_hashtags.png
│   │   ├── 06b_engagement_logit_forest.png
│   │   ├── 07_engagement_by_post_length.png
│   │   ├── 08_sentiment_distribution.png
│   │   ├── 09_15day_sentiment.png
│   │   ├── 10_engagement_by_sentiment.png
│   │   ├── 11_top_keywords.png
│   │   ├── 12_lda_coherence.png
│   │   ├── 13_wired_topic_wordclouds.png
│   │   ├── 14_verge_topic_wordclouds.png
│   │   ├── 15_verge_keyword_network.png
│   │   ├── 15_wired_keyword_network.png
│   │   ├── 16_perceptual_map.png
│   │   ├── 16_verge_micro_candidates.png
│   │   └── 16_wired_micro_candidates.png
│   └── tables
│       ├── 00_figure_index.csv
│       ├── 02_monthly_volume.csv
│       ├── 03_engagement_summary.csv
│       ├── 03c_weekday_share.csv
│       ├── 04_verge_author_summary.csv
│       ├── 04_wired_author_summary.csv
│       ├── 04_zero_engagement_share.csv
│       ├── 05_engagement_composition.csv
│       ├── 05_top_hashtags.csv
│       ├── 06_top_linked_domains.csv
│       ├── 06b_engagement_logit.csv
│       ├── 07_post_type_engagement.csv
│       ├── 08_sentiment_label_share.csv
│       ├── 08_sentiment_summary.csv
│       ├── 09_15day_sentiment.csv
│       ├── 09_engagement_by_sentiment.csv
│       ├── 10_verge_author_sentiment.csv
│       ├── 10_wired_author_sentiment.csv
│       ├── 11_top_keywords.csv
│       ├── 11_verge_network_centrality_candidates.csv
│       ├── 11_verge_network_centrality.csv
│       ├── 11_wired_network_centrality_candidates.csv
│       ├── 11_wired_network_centrality.csv
│       ├── 12_lda_coherence_by_k.csv
│       ├── 12_verge_micro_influencer_scores.csv
│       ├── 12_wired_micro_influencer_scores.csv
│       ├── 13_lda_topic_terms.csv
│       ├── 13_lda_topics.csv
│       ├── 14_topic_sentiment_engagement.csv
│       ├── 15_verge_keyword_network_nodes.csv
│       └── 15_wired_keyword_network_nodes.csv
├── README.md
├── report
│   └── report.pdf
└── requirements.txt
```

## Folder Description

| Folder             | Description                                                                                            |
| ------------------ | ------------------------------------------------------------------------------------------------------ |
| `brief-material/`  | Coursework specification PDF for BUSI4370 Coursework 2.                                                |
| `data/raw/`        | Raw Bluesky posts and profile datasets collected for Wired and The Verge.                              |
| `data/processed/`  | Cleaned datasets, sentiment outputs, topic outputs, analysis summaries, and recommendation JSON files. |
| `notebooks/`       | Main notebook pipeline, separated by analysis stage.                                                   |
| `outputs/figures/` | Generated visualisations used for reporting and interpretation.                                        |
| `outputs/tables/`  | Generated CSV summary tables used in the analysis and report.                                          |
| `report/`          | Final report PDF for the coursework submission.                                                        |

## Notebook Pipeline

| Notebook                      | Purpose                                                                                               |
| ----------------------------- | ----------------------------------------------------------------------------------------------------- |
| `01_data_collection.ipynb`    | Collects raw Bluesky post and profile data.                                                           |
| `02_data_cleaning.ipynb`      | Cleans raw posts/profiles and creates processed datasets.                                             |
| `03_analysis.ipynb`           | Performs exploratory analysis on volume, engagement, posting behaviour, hashtags, and linked domains. |
| `04_sentiment.ipynb`          | Applies sentiment analysis and compares sentiment patterns between brands.                            |
| `05_topics_keywords.ipynb`    | Performs topic modelling, keyword extraction, and topic-level analysis.                               |
| `06_network_influencer.ipynb` | Builds network metrics and scores potential micro-influencer candidates.                              |
| `07_perceptual_map.ipynb`     | Creates brand positioning and perceptual map outputs.                                                 |
| `final_notebook.ipynb`        | Consolidated final notebook version containing the completed coursework workflow.                     |

## Key Outputs

### Figures

The project generates visual outputs such as:

- Weekly volume trends
- Engagement distribution plots
- Posting hour and weekday heatmaps
- Zero-engagement comparison
- Engagement composition charts
- Top hashtag charts
- Sentiment distribution and sentiment-over-time charts
- Engagement by sentiment
- LDA coherence plot
- Topic word clouds
- Keyword networks
- Micro-influencer candidate plots
- Brand perceptual map

### Tables and Data Files

The project also produces structured outputs such as:

- Engagement summaries
- Monthly volume tables
- Author summaries
- Sentiment summaries
- Topic summaries
- LDA topic terms
- Network centrality scores
- Micro-influencer scores
- Perceptual map data
- Final recommendation JSON files
- Final report PDF in `report/report.pdf`

## Methods Used

- Social media data collection
- Data cleaning and preprocessing
- Exploratory data analysis
- Engagement analytics
- Sentiment analysis
- Topic modelling with LDA
- Keyword frequency analysis
- Keyword network analysis
- Network centrality analysis
- Micro-influencer scoring
- Perceptual mapping
- Data visualisation

## Tools and Technologies

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- NLTK / VADER-style sentiment analysis
- Gensim / LDA topic modelling
- NetworkX
- WordCloud
- JSON and CSV processing

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/shreyuu/bluesky-brand-intelligence
   cd bluesky-brand-intelligence
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Run the notebooks in order:

   ```text
   notebooks/01_data_collection.ipynb
   notebooks/02_data_cleaning.ipynb
   notebooks/03_analysis.ipynb
   notebooks/04_sentiment.ipynb
   notebooks/05_topics_keywords.ipynb
   notebooks/06_network_influencer.ipynb
   notebooks/07_perceptual_map.ipynb
   ```

5. Review generated outputs in:

   ```text
   outputs/figures/
   outputs/tables/
   data/processed/
   ```

## Notes

- The cleaned repository excludes local macOS `.DS_Store` files and keeps only the relevant coursework, data, notebook, output, report, and dependency files.
- Raw and processed datasets are included for reproducibility.
- The project is structured as a coursework analytics pipeline and can also be presented as a social listening / brand intelligence portfolio project.

## Author

**Shreyash Meshram**  
MSc Business Analytics  
University of Nottingham

## Module

**BUSI4370 – Analytics Specializations and Applications**  
Coursework 2
