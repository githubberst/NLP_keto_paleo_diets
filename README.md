# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3 - Reddit API Scraping and Binary Classification Problem

### Problem Statement

We are members of a data science team working for a specialised diet food company.
As such, understanding the customers' diets of interest and the unique preferences of specific diet groups is key to driving effective marketing, targeted advertisements, product development, and profit generation. The purposes of this project are twofold. 

Firstly, by leveraging NLP techniques, we aim to generate valuable insights on the characteristics and preferences of the Keto and Paleo communities. By thoroughly analysing the collected data, we aim to identify key patterns, trends, and distinguishing features of each community. We have chosen these two communities because despite rising interest in these two diets, there is a lack of goods and services targeted at them and this is a gap in the market that we hope to fill.

Secondly, we aim to create a robust binary classifier that can effectively differentiate between posts from these two communities. To do this, we will make use of the posts from the two subreddits, r\keto and r\paleo. This will serve as the foundation for our classification model.

Ultimately, the developed model will empower our company's product and marketing teams to precisely identify the needs and preferences of our clientele, helping us to tailor our offerings to Keto or Paleo diet followers. This data-driven, personalised marketing strategy will enhance customer satisfaction and drive business growth.

Throughout the project, we will undertake crucial steps such as preprocessing the subreddit posts and conducting Exploratory Data Analysis (EDA). Finally, the performance of our models will be evaluated based on the highest f1 score, ensuring the accuracy and effectiveness of our classification approach.
Goals

---

### Datasets

Scraped from Reddit: 
* [`keto.csv`](./datasets/'keto.csv'): Raw file scraped from r/keto(www.reddit.com/r/keto) containing 2943 rows and 113 columns.
* [`paleo.csv`](./datasets/'paleo.csv'): Raw file scraped from r/paleo(www.reddit.com/r/paleo) containing 2484 rows and 118 columns.
* [`keto2.csv`](./datasets/'keto2.csv'): Modified version of keto.csv containing 976 rows and 113 columns.
* [`paleo2.csv`](./datasets/'paleo2.csv'): Modified version of paleo.csv containing 929 rows and 118 columns.
* [`combined.csv`](./datasets/'combined.csv'): Combination of keto2.csv and paleo2.csv containing 1905 rows and 8 columns.
---

### Data Dictionary
*this data dictionary is for the dataset named `combined.csv`*

|**Feature**| **Datatype**|**Description**|
|:-|:-:|:-|
|<b>redditlabel</b>|*integer*| The numeric boolean representation of our two classes. 0 means Keto and 1 means Paleo.|
|<b>title</b>| *string*| The subject title of the Reddit post.|
|<b>selftext</b>|*string*| The content of the Reddit post.|
|<b>titletext</b>| *string*| The combined text from 'title' and 'selftext'.|
|<b>text_clean</b>| *string*| The text from 'titletext'  in lowercase and with the punctuation removed.|
|<b>char_count</b>| *integer*| The number of characters in 'text_clean' (including spaces).|
|<b>word_count</b>| *integer*| The number of words in 'text_clean' (not including spaces).|
|<b>text_lemma</b>|*string*| The lemmatized text from 'text_clean'.|
---

### Conclusion

In summary:
<br><br>
1) <b>Differing Focus</b>

    - The two communities exhibit distinct priorities, with the Keto community placing significant emphasis on macronutrient composition and micronutrients, whereas the Paleo community directs its attention towards ingredient choices.

2) <b>Shared Themes</b>

    - The prevalence of the terms ‘weight loss’ and ‘low carb’ in both communities suggests that weight management and adopting a low-carbohydrate dietary approach are central themes and objectives within both communities.

3) <b>Navigating Uncertainty</b>

    - Within both the Keto and Paleo communities, a considerable number of users express confusion regarding specific dietary details. The presence of confusion suggests that users may encounter challenges in understanding and implementing the intricate nuances associated with these dietary approaches.

<br><br>

Upon revisiting the problem statement, we are reminded of our two primary objectives:

1) <b>Objective 1</b>

    - Our first objective was to create a highly robust binary classifier with the ability to discern posts and content that are relevant to the Keto and Paleo diets. 

     - With an impressive F1-Score of 0.93, our model empowers our company's product and marketing teams to accurately ascertain the needs and preferences of our valued clientele. This invaluable insight enables us to tailor our offerings in accordance with the evolving requirements of our customers. By adopting this data-driven and personalized marketing approach, we anticipate an elevation in customer satisfaction levels, leading to substantial business growth.

2) <b>Objective 2</b>

    - Our second objective was to extract valuable insights pertaining to the characteristics and preferences of the Keto and Paleo communities. 

    - Through meticulous analysis of the gathered data, we successfully identified crucial insights that have played a pivotal role in guiding our marketing initiatives and product. 
---

### Recommendations


1) <b>Dynamic Tracking</b>

    - By utilizing our final binary classifier, we can conduct an in-depth analysis of the user's historical comments and reviews. Leveraging this analysis, our website will seamlessly generate personalized product recommendations, meticulously curated to match their distinctive requirements and preferences. By understanding their ever changing preferences, we can develop and suggest products that align with their individual, and evolving requirements, ensuring a more satisfying and customized experience. 

        * Based on our insights, the Keto audience is likely to find products that offer convenient, high-fat, low-carb meal options attractive. We can focus on developing and promoting meals designed to include a combination of macronutrients in appropriate proportions, whilst incorporating a variety of nutrient-dense foods as well as supplements with a focus on micronutrients to ensure our customers are getting a wide range of essential vitamins, minerals, and antioxidants. 

        * The Paleo audience on the other hand will find products using high-quality, unprocessed ingredients that are aligned with ancestral diet principles more appealing. Following this insight, we can place more emphasis on sourcing and recommending organically and locally grown produce, grass-fed meats, wild-caught fish, pasture-raised eggs, etc.

2) <b>Broaden Appeal</b>

    - By capitalizing on shared interests, we can leverage it to enhance the appeal of each product, catering to a wider customer base:
    
        * Example 1: Whenever possible, develop and promote products specifically tailored to support weight loss and low-carb diets. This can include meal replacement options, low-carb snacks, dietary supplements, or specialized recipe ingredients. Ensuring that the nutritional content aligns with the needs of both Keto and Paleo practitioners will appeal to a broader customer base.
        
        * Example 2: Since both the Keto and Paleo communities are concerned about weight loss, it is imperative to ensure that all products bear conspicuous calorie labeling, both on physical packaging and online platforms. This measure is designed to streamline the caloric tracking process for customers, making it effortless to accurately monitor their calorie intake.
        
        * Example 3: We can capitalize on the current trending topics within each community as a means to expand our customer base. One such example is the 'Keto Month Challenge,' an initiative aimed at motivating individuals to adopt the ketogenic diet for a month. By offering guidance, resources, and support to participants throughout their journey, we have the opportunity to introduce and showcase our products to this target audience. Successfully converting individuals to the ketogenic diet can lead to a significant increase in our customer base.

3) <b>Educational Content</b>

    - By taking advantage of the information-seeking behavior of both communities, an opportunity arises to consistently deliver compelling and relevant content. This, in turn, fosters customer loyalty and sustains an actively engaged customer base. 
    - We can offer educational resources, comprehensive guides, and informative content to cater to the different communities. By crafting targeted marketing campaigns and messaging that highlight the macronutrient composition requirements and micronutrients concerns of the Keto community and ingredient selection preferences of the Paleo community, our business will be able to resonate with the respective audiences. 
    - This can be accomplished through various mediums such as well-researched blog articles, instructive videos, and carefully curated recipes that not only elucidate the fundamental principles underlying these dietary approaches but also offer practical tips for successful implementation. 



### Next steps

We should look into two general future steps: gathering information on the ground in Singapore, instead of relying purely on information from Reddit, and in expanding our classification model to other types of diets.  





