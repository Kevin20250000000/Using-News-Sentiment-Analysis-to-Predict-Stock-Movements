# Using-News-Sentiment-Analysis-to-Predict-Stock-Movements

## Introduction

In recent years, Generative Adversarial Networks (GANs) have achieved remarkable success in generating realistic images and videos, as well as transforming data across modalities. However, their application to stock price forecasting—a complex time series problem—remains an emerging area of research. The inherent volatility of stock markets and the significant influence of investor sentiment present unique challenges for accurate prediction.

Recent studies have begun to explore the integration of sentiment analysis into GAN-based models to enhance stock price prediction. For instance, the FB-GAN model combines historical stock data with sentiment scores derived from news articles using BERT, demonstrating improved predictive performance across major equities like Amazon and Apple . Similarly, sentiment-guided adversarial learning frameworks incorporate social media sentiment data, leading to more accurate forecasts compared to traditional models such as ARIMA and LSTM .

In this notebook, I develop a model to forecast Tesla (TSLA) stock prices by integrating historical data and technical indicators with external factors like trader sentiment and brand reputation, as reflected in social media posts. This comprehensive approach aims to capture the multifaceted dynamics of the market, potentially leading to more accurate and robust stock price predictions.

### Table of contents
1. [Importing Necessary Libraries](#section-one)
2. [Get weekly sentiment for stock ticker](#section-two)
3. [Get final dataset for training](#section-three)
4. [Build GAN model](#section-four)
5. [Train and test model](#section-five)
6. [Conclusions](#section-six)

**1. Importing Necessary Libraries**



**2. Get weekly sentiment for stock ticker**

Stock price movements are influenced by more than just historical data; external factors like social media sentiment can have significant impacts. Notable examples include Elon Musk's tweets, which have been shown to cause substantial fluctuations in Tesla's stock price. For instance, in August 2018, Musk tweeted about taking Tesla private at 420𝑝𝑒𝑟𝑠ℎ𝑎𝑟𝑒,𝑙𝑒𝑎𝑑𝑖𝑛𝑔𝑡𝑜𝑎𝑚𝑜𝑟𝑒𝑡ℎ𝑎𝑛614 billion drop in Tesla's market value .

Research indicates a significant relationship between Twitter sentiment and stock returns. Studies have found that peaks in Twitter activity and sentiment can lead to abnormal stock returns . This suggests that analyzing the tone of social media posts, particularly on platforms like Twitter, can provide valuable insights into market dynamics.

In this notebook, we will incorporate sentiment analysis of Twitter posts to assess the mood of stock market participants. By integrating this external indicator with traditional financial data, we aim to enhance the accuracy and robustness of stock price predictions.

**3. Get final dataset for training**

![image](https://github.com/user-attachments/assets/648e7508-8e6e-41dd-a0ce-56842de780ba)

![image](https://github.com/user-attachments/assets/87f3abb7-e675-48cc-bf99-ae0be41c2698)

**4. Build GAN model**
We build a GAN model architecture, where the generator has 5 LSTM blocks and the discriminator has 5 convolutional and 3 dense layers with sigmoid activation function.


**5. Train and test model**

![image](https://github.com/user-attachments/assets/cf361942-2e78-4a9f-a197-e4f957dc49da)


**6. Conclusions**

Generative Adversarial Networks (GANs) have shown promise in modeling time series data like stock prices, particularly when combined with technical indicators and sentiment analysis from platforms such as Twitter. For widely followed stocks like Tesla, the abundance of tweet volumes provides rich sentiment data, enhancing prediction accuracy.

However, for less-discussed stocks, limited social media activity can result in sparse or noisy sentiment inputs, potentially diminishing model performance. A study by Anjaneyulu et al. (2024) highlights that low-popularity stocks present challenges due to restricted data availability and increased volatility. The research suggests that while GANs can improve predictions for high-volume tickers, their effectiveness may be constrained for stocks with limited sentiment data .
eudoxuspress.com

Therefore, while GANs are promising for stock forecasting, their efficacy is influenced by the availability and quality of sentiment data. In scenarios with limited social media activity, alternative approaches or enhanced data augmentation techniques may be necessary to maintain predictive performance.
