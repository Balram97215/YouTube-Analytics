# YouTube Video Popularity Prediction

A data mining project analyzing factors that drive YouTube video popularity in the USA.

---

## Project Description

This project aims to analyze trending YouTube videos in the US and identify key drivers of video popularity. We leverage predictive modeling to provide actionable recommendations for advertisers and content creators. The analysis uses multiple models including linear regression, logistic regression, decision tree, and neural networks.

---

## Business Questions

- What factors play a role in the popularity of YouTube videos?
- What video categories achieve the most views?
- How can advertisers choose the best videos for promoting their products?

---

## Dataset

A sample of ~10,000 trending YouTube video records was used, containing variables such as:

- **Title**: Video title  
- **Tags**: Keywords describing the video  
- **Category ID**: Video category  
- **Views, Likes, Dislikes, Comments**  
- **Publish time**: Month and AM/PM  
- **Engagement flags**: comments/ratings disabled  

---

## Data Preprocessing

- Random sampling of 10,000 rows from 40,950 records  
- Removed missing description data  
- Transformed text variables to numeric (e.g., title word count)  
- Separated publish date into month + time of day  
- Normalized skewed variables using log transformations  
- Identified outliers but retained them as meaningful data points  

---

## Predictive Models

1. **Linear Regression**  
   - Modeled view count (log-transformed)  
   - Showed that fewer title words and higher tags correlate with higher views  

2. **Logistic Regression**  
   - Classified videos as *Popular* or *Not Popular*  
   - Category, tags, and publish month were significant predictors  

3. **Decision Tree**  
   - Created rules for video popularity based on category and publish month  
   - Found music, gaming, film, travel, and comedy most successful  

4. **Neural Network**  
   - Explored non-linear patterns  
   - Provided moderate results with AUC ~0.52, limited by feature complexity  

---

## Key Findings

- Videos with concise titles and more relevant tags performed better  
- Videos published between **March and June** showed higher view counts  
- Music, Gaming, Film, Travel & Events, and Comedy categories were top-performing  
- Videos with comments/ratings enabled had higher median views  
- Advertisers should target popular videos in the above categories, especially in spring and early summer  

---

## Recommendations

- Focus advertising on **March–June** videos  
- Target the top categories (Music, Film, Gaming, Travel & Events, Comedy)  
- Prioritize videos with:  
  - fewer than 10 words in the title  
  - 20–25 tags  
  - comments and ratings enabled  

---

## References

- YouTube Trending Dataset (public source)  
- [Scikit-learn Documentation](https://scikit-learn.org/stable/)  
- [XL Miner](https://www.solver.com/xlminer-data-mining)  

---

