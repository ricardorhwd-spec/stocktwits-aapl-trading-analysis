# Talking Before Trading
## Are StockTwits comments linked to Apple’s trading volume?

A BA780 team project analyzing the relationship between investor discussion on StockTwits and AAPL trading activity. This repository presents the original analysis and presentation as part of Ricardo Huang Wei Di’s portfolio.

### Overview
The notebook reports an analysis of **914,962 comments** and **543 trading days** from January 2020 to February 2022. It combines StockTwits posts with Yahoo Finance market data, cleans nested text fields, aligns timestamps with trading sessions, and explores comment activity, sentiment, earnings announcements, and trading volume.

### Main findings reported in the notebook
- Comment counts correlate more strongly with same-day volume (**0.65**) than next-day volume (**0.35**).
- Above-average comment activity is associated with next-day volume approximately **15–23% above normal** in the analyzed comparisons.
- Comment counts have a stronger relationship with next-day volume than sentiment tags.
- Comment activity spikes in the session following earnings announcements.

These are exploratory associations, not causal evidence or a validated trading forecast. The notebook proposes further regression analysis and out-of-sample testing. The figures above summarize the supplied notebook; they have not been independently recomputed for this repository.

### Files
| File | Contents |
|---|---|
| `analysis.ipynb` | Original notebook, including existing outputs and team attribution |
| `presentation.pptx` | Project presentation |
| `requirements.txt` | Python dependencies; versions are not a tested environment lock |

### Run the analysis
**Google Colab is the simplest option.** Open [Google Colab](https://colab.research.google.com/), select **File → Upload notebook**, and upload `analysis.ipynb`.

Install dependencies in a new cell before running the notebook:
```python
%pip install pandas yfinance "seaborn>=0.13" matplotlib scipy
```
Then run the notebook cells in order. The existing code uses `/content/stocktwits`, which is designed for Colab. For local Jupyter use, install `requirements.txt` and replace the `/content/stocktwits` and `/content/stocktwits.zip` paths with writable local paths first.

Internet access is required. The notebook downloads 62 CSV files from the team’s existing GitHub release and retrieves AAPL data through yfinance. Raw data is not bundled. External availability and package changes may affect reruns; this packaged copy has not been executed end to end.

### Data sources
- [StockTwits raw dataset on Kaggle](https://www.kaggle.com/datasets/frankcaoyun/stocktwits-2020-2022-raw)
- [Team-hosted data archive](https://github.com/aliciamorac96/ba780-fall26-b08/releases/download/v1/stocktwits.zip)
- [AAPL historical data on Yahoo Finance](https://finance.yahoo.com/quote/AAPL/history/)

### Team and contributions
**Team B08:** Alicia Mora, Almira Lazim, Ricardo Huang Wei Di, and Pakaporn (Zoe) Leetrairong.

As documented in the notebook, Ricardo contributed **Section 4.3: comment timing, including activity between earnings announcements and the next market opening**, and shared responsibility for the introduction, data cleaning, and conclusion. Other team members’ contributions and the original AI-use disclosure remain in the notebook.

### Reuse
This repository does not add a license to the team’s work or third-party datasets. Refer to original source terms and obtain appropriate permission before redistribution or reuse.
