---
layout: page
title: "What Influences a Pregnant Mother's Intention to Breastfeed?"
date: 2024-01-21
header:
  image: /assets/ChatGPT Image Mar 27, 2025, 11_06_19 AM.png
#categories: [Projects, Public Health]
#tags: [data-analysis, R, survival-analysis, maternal-health]
permalink: /projects/2024-01-21-breastfeeding-intention-analysis.md/
---
<img src="/assets/ChatGPT Image Mar 27, 2025, 11_06_19 AM.png" alt="woman breastfeeding baby" width="400" />

*How I used R to analyze intention and behavior around breastfeeding among pregnant women in Wales.*


## 👋 Background

As part of my postgraduate work in health data science, I had the opportunity to explore a dataset collected from pregnant women in Wales. The goal was to investigate what influences a mother’s **intention to breastfeed**, and how these intentions connect to actual behaviors over time.  

This wasn’t just an academic exercise, but an opportunity to follow a full data science workflow, applying real-world analytical techniques to a meaningful topic in maternal and infant health.

---

## 📊 Data and Workflow Overview

The dataset included a mix of **demographic**, **clinical**, and **psychosocial variables**. I began with a raw CSV file, which required cleaning, recoding, and organizing before any meaningful analysis could be done.

### 🧹 Step 1: Data Cleaning & Preparation  
- Converted date formats using `lubridate`  
- Calculated BMI from height and weight  
- Removed irrelevant columns  
- Recoded categorical variables for analysis  

### 🔎 Step 2: Exploratory Data Analysis (EDA)  
Using packages like `table1`, `gtsummary`, and base R, I explored the distribution of variables, identified missing data, and focused on the variable of interest: **breastfeeding intent**.

### 🌳 Step 3: Predictive Modeling  
To predict intention to breastfeed, I built a **decision tree** using the `rpart` package.  
- Split data 80/20 into training and test sets  
- Visualized the tree with `rpart.plot`  
- Evaluated performance using a **confusion matrix** from the `caret` package

### ⏳ Step 4: Survival Analysis  
The dataset also included follow-up data—perfect for **time-to-event analysis**. I used:
- **Kaplan-Meier survival curves** to visualize time to breastfeeding cessation  
- **Cox proportional hazards regression** (`survival` and `survminer` packages) to identify predictors of early breastfeeding cessation

---

## 🔍 Key Insights

- **Intent to breastfeed** was strongly predicted by BMI, maternal age, and socioeconomic status.
- **Survival analysis** revealed that mothers experiencing high stress or with lower income had significantly shorter breastfeeding durations.
- On the other hand, **older mothers with healthier BMI profiles** were more likely to breastfeed for longer—suggesting potential areas for targeted intervention.

---

## 🧠 Why This Matters

Maternal health behavior is shaped by a complex web of influences. This project helped me see how combining predictive and survival models can offer a more complete picture—one that moves from intention to real-world outcomes.  

In public health, this kind of insight can inform **tailored interventions**, helping providers offer the right support to the mothers who need it most.

---

## 🧰 Tools and Packages Used

- `tidyverse` – for data wrangling and visualization  
- `lubridate` – for handling date-time fields  
- `rpart`, `rpart.plot` – for decision tree modeling  
- `caret` – for model evaluation  
- `survival`, `survminer` – for time-to-event and Cox regression  
- `table1`, `gtsummary` – for professional reporting tables  

---

## 💬 Final Thoughts

This project not only strengthened my R skills but also deepened my understanding of how data can drive better public health strategies. As someone passionate about maternal and child health, I’m excited to keep exploring how data can guide more compassionate, effective policy and programming.

You can check out the full code and data workflow on [GitHub](#).

---

