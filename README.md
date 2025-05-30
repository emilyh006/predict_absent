# Clustering Youth Risk Behavior Data

This repository contains a comprehensive clustering analysis of youth survey responses using both the full dataset and domain-specific subsets (mental health, home environment, social relations, and physical activity). The goal is to identify meaningful participant clusters based on response patterns.

## Domain-Wise Clustering
We begin by clustering mental health indicators together with one contextual domain at a time:
- Home Environment + Mental Health
- Social Environment+ Mental Health
- Physical Activity + Mental Health

This approach allows for targeted exploration of how each context relates to mental health patterns.

## Full-Model Clustering 
We are currently developing a model that clusters across all domains simultaneously, including:
- Mental Health
- Home Environment
- Social Environment
- Physical Activity
- Other factors

## Comparison Goals
We aim to:
- Identify whether similar subgroups emerge across domains
- Evaluate if full-model clustering reveals additional nuance
- Determine which strategy yields clearer and more actionable subgroup distinctions

## 📁 Data

The full dataset utilized in this project is available at the following link:[Dataset Access Link](https://www.cdc.gov/yrbs/data/index.html)  

**Note**: To fully interpret the clustering results, please refer to the   `data_dictionary.md` provided in data folder. The document has been customized specifically for the purposes of this project. For the official data dictionary, please refer to `2023_National_YRBS_Data_Users_Guide.pdf`. 
