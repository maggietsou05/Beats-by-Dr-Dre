<img src="https://github.com/user-attachments/assets/11233608-f2cc-4944-ae09-4519bb68a4b2" width="200"/>

# Project Background
This project was completed as part of a qualitative & quantitative insights externship with **Beats by Dre**, based in California.

Beats by Dr. Dre is an audio brand founded in 2006 by Dr. Dre and Jimmy Iovine, offering premium headphones, earphones, and speakers. Beats has gained significant market share through celebrity endorsements, particularly in the higher-priced audio market, and became known for its stylish designs and strong connection to music culture. 

The company wanted to analyze customer reviews to guide product development and strategy for Beats' Pill Wireless Speakers. The dataset for this project was sourced/scraped from Amazon product reviews for various Beats by Dre audio devices. The dataset contains key information like review text, rating, helpful count, verified purchase status, and product attributes, used for sentiment analysis and insights into consumer experiences.

Key areas of this experience include:
- Leveraging web scrapers to collect consumer feedback from Amazon. Data was collected using the Oxylabs Scraper API, with a custom Python script to scrape and structure Amazon product reviews. [> full code](Amazon_Review_Scraper.ipynb)<br>
- Cleaning the scraped data. [> full code](Beats_Data_Cleaning.ipynb)<br>
- Utilizing **visualization tools** like Matplotlib and Seaborn to uncover trends, outliers, and correlations in the dataset. [> full code](Beats_Visualizations.ipynb)<br>
- Performing **sentiment analysis** using TextBlob to classify and analyze brand perception. [> full code](Sentiment_Analysis.ipynb)<br>
- Translating data into **strategic recommendations**<br><br>

# Executive Summary
### Overview of Findings

- 76% of Beats product reviews are 5-star ratings, reflecting high customer satisfaction. The polarity score confirms this: reviews are skewed positive, with a few negative outliers.
- Sound quality is a core value driver for satisfied buyers, particularly for its bass strength and clarity. The lightweight design is also frequently highlighted as positive aspects.
- Themes of gifting, celebration, and personal value are strong in reviews with high sentiment. (polarity > 0.65)
- Product reliability is a key pain point for low-rated reviews, frequently mentioning charging issues, Bluetooth disconnection, and non-working product upon receiving it. 

![dcds](https://github.com/user-attachments/assets/da557b49-3b30-43b1-bfd0-8a2ba8e8c960)


# Insights Deep Dive
### Competitive Analysis (Wireless Speakers)
- Beats ratings fluctuate over time, dipping around 2023 (to ~4.2) before rebounding in 2025.
- Amazon Echo's late entry in 2024 was rated highly (~4.7), which is a rising threat for Beats Speakers, especially in budget or bundled smart-home audio.
- JBL Speakers leads with both strong ratings and loyalty, while Beats enjoys higher emotional pull despite mixed consistency. Amazon Echo and LG lag behind as functional but less emotionally resonant brands.
- Beats' speakers has a solid average rating (4.62), but exhibits the highest standard deviation among brands, indicating risk of churn due to inconsistency across customer experiences.
  
![dfdsjfld](https://github.com/user-attachments/assets/501ba66e-f193-4176-a031-d59c3b357746)

### Sentiment Scores
- Beats’ reviews are notably more positive in comparison to its competitors, but not the most expressive, which may imply customer satisfaction without strong emotional attachment.
- JBL and LG drive stronger emotional responses, which can be powerful for brand loyalty.
- Sony’s lower polarity and subjectivity signals a more performance-focused perception, and not as beloved.<br><br>

![image](https://github.com/user-attachments/assets/c2c28f92-90ac-4988-b026-a3dc394a85fc)

### High-rated Beats Products
- Sound quality is the standout driver of satisfaction. This is reinforced by the word cloud, where terms like “sound,” “music,” “bass,” and “quality” are visually dominant.
- Battery (long-lastig performance) is in second place, and design & looks and connectivity trail closely behind
- Emotional and usability-driven words such as “love,” “great,” “easy,” “use,” and “comfortable.” suggests that users not only appreciate technical specs but also value how intuitive and enjoyable the product is. <br><br>

The following six key factors are based on industry knowledge of what consumers typically value in audio devices, and were used to extract factor-specific word frequencies from the reviews:


1. Sound Quality -
 `sound`, `audio`, `bass`, `clarity`, `loud`, `volume`, `noise`, `distortion`, `treble`

2. Design & Looks -
 `design`, `look`, `color`, `style`, `aesthetic`, `sleek`, `compact`, `small`, `size`, `portable`, `lightweight`

3. Battery -
 `battery`, `charge`, `charging`, `power`, `long-lasting`, `recharge`, `life`

4. Connectivity -
 `bluetooth`, `wifi`, `connect`, `connection`, `pair`, `airplay`, `apple`, `android`, `wireless`

5. Durability -
 `durable`, `sturdy`, `rugged`, `solid`, `built`, `build quality`, `waterproof`, `shock`, `reliable`


6. Price & Value -
 `price`, `cost`, `value`, `worth`, `cheap`, `expensive`, `deal`, `affordable`<br>

<img width="1037" alt="image" src="https://github.com/user-attachments/assets/82e21576-0634-4487-a372-85bdc98794a1" />


### Low-rated Beats Products
- Battery-related keywords dominate 1-star reviews
- Sound quality and connectivity are the next most frequently criticized features. Mentions like “weak,” “bass,” “tooth,” “compete,” and “speakers,” further point to sound distortion and Bluetooth issues.
- Price appears as a frustration factor, despite being mentioned less often.
- Though qualitative analysis showed broken products, the low frequency of durability complaints implies products often fail early in use, rather than degrading over time.

<img width="970" alt="image" src="https://github.com/user-attachments/assets/66899d3e-d691-4875-a8cc-4bd566ffe222" />

# Recommendations
Based on the uncovered insights, the following recommendations are provided:<br><br>
**Anchor product strategy in sound quality and aesthetic appeal**<br>
- The new speaker line should highlight two core strengths: exceptional audio performance and bold, fashion-forward aesthetics. Survey results and review analysis confirm that sound quality is the top priority for users—mentioned nearly twice as often as any other feature in positive reviews.
- While many competitors focus on voice assistants or smart features, Beats has an opportunity to differentiate by enhancing the listening experience itself, such as through speakers that use AI to adapt to the room’s acoustics for consistently rich, immersive sound.

**Build emotional loyalty through culture, community, and gifting**
- Reviews show a high prevalence of positive sentiment around gifting experiences. Position the product as a shared music experience—ideal for holidays, concerts, and social gatherings. Support this through:
  - Seasonal bundles and co-branded editions with pop artists
  - Personalization options (e.g. engraving, color packs)
  - A karaoke mode and mini mic accessories to enhance shared enjoyment

**Strengthen post-purchase experience through better reliability & customer support**
- Low-rated reviews consistently cite hardware issues and poor customer service. Without raising prices, prioritize:
  - Tightened quality control during manufacturing
  - Clearer return/replacement policies and responsive customer service

**Emotionally reposition the brand to deepen loyalty**
- Beats lags behind JBL in emotional pull despite strong brand recognition. Marketing should focus less on specs and more on connecting music to personal identity and relationships—through storytelling, user-generated content, and influencers within music subcultures, especially given the connection Beats has with pop culture.





## Assumptions and Caveats
Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:

- All reviews are from American consumers.
- Reviews are honest and reflective of actual behavior. (No response bias)
- Stated reviews translate into real purchasing decisions.






