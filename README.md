## Comparative study of Moirai and Chronos vs Naive and SeasonalNaive method

This repo contains 3 notebooks, each associated with a method.
The notebooks are organized as follows :
- For each dataset/time series (M4, Finance, Istanbul Traffic, ERCOT) we perform inference
- We calculate the reported MAE

### Chronos

The notebook is in chronos-forecasting/src. We perform inference with the small model, by choosing a certain context length (it depends on the dataset)

### Moirai

The notebook is in uni2ts/src. We perform inference with the small model, by choosing a certain context length (it depends on the dataset)

### Seaonal Naive/Naive

The notebook is on the root file

Naive method consists in predicting the next value by observing the value before, that means $\forall i \le h, Y_{t+i} = Y_{t}$ (where h is the horizon)

SeasonalNaive consists in predicting the next value by observing the value a season before (24 for an hour, 7 for a day, 4 for a week and so on...)

## Data

|                        | M4   | Finance | Traffic | ERCOT |
|------------------------|------|---------|---------|-------|
| **Frequency**           | H    | D       | Min     | H     |
| **Context length**      | 72   | 62      | 900     | 744   |
| **Prediction length**   | 12   | 31      | 100     | 24    |
| **Number of time series** | 5   | 3       | 10       | 3     |


# Reference

## Amazon Chronos
Github : https://github.com/amazon-science/chronos-forecasting

Article : https://arxiv.org/abs/2403.07815

## Moirai
Github : https://github.com/SalesforceAIResearch/uni2ts

Article : https://arxiv.org/abs/2402.02592
