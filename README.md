# GoFundMe-Campaign-Success
This project investigates how visual content, campaign timing, and textual framing influence fundraising success on GoFundMe. Using data from 1,000 campaigns in the Animal category, the analysis combines computer vision, natural language processing, and predictive modeling to uncover what differentiates high-performing campaigns from the rest.

### [Data Collection & Feature Extraction](GoFundMe%20Scraping.ipynb)

- Built a custom Python pipeline using Selenium and BeautifulSoup to scrape 1,000 GoFundMe campaigns
- Collected structured attributes including total funds raised, campaign duration, and campaign descriptions
- Processed each campaign’s primary image using the Google Vision API to extract high-level visual concepts (e.g., animals, environments, expressions)

### [Predictive Modeling](Predictive%20Modeling.ipynb)

- Defined a binary outcome variable classifying campaigns as high-earning or low-earning, based on the median amount raised
- Trained multiple logistic regression models to compare the predictive value of:
  Image-derived features
  Textual descriptions
  Campaign duration
- The strongest model combined text features and duration, achieving 70.5% accuracy, highlighting the importance of campaign longevity in fundraising outcomes

### [Topic Modeling & Insights](Topic%20Modeling.ipynb)

- Applied Latent Dirichlet Allocation (LDA) to image-derived labels to identify seven dominant visual themes
- Compared topic prevalence across the top and bottom fundraising quartiles
- Found that campaigns featuring dogs and positive facial expressions were significantly more common among top performers, while cat-focused imagery appeared more frequently in lower-performing campaigns
