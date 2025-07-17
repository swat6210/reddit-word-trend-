# reddit-word-trend-
reddit word trend analyser using nltk library,textblob,praw
# reddit-word-trend

A simple Python script to analyze word trends on Reddit over time and visualize the results.

## ⚙️ Overview

`reddit-word-trend` fetches Reddit post/comment data from a specified subreddit, processes the text to calculate word frequencies or TF–IDF scores across time windows, and generates visualizations to highlight trends.

## 🧰 Technologies

- **Python 3** — core scripting language  
- **praw** — Reddit API client  
- **nltk** — text preprocessing (tokenizing, stop-word removal)  
- **scikit-learn** — TF–IDF vectorization  
- **matplotlib / seaborn** — plotting word frequency and trend charts  
- *(Optional)* `wordcloud` — generate word clouds of top words

## 🚀 Installation

```bash
git clone https://github.com/swat6210/reddit-word-trend.git
cd reddit-word-trend
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
[reddit]
client_id = YOUR_CLIENT_ID
client_secret = YOUR_CLIENT_SECRET
user_agent = reddit-word-trend-script
python reddit_trend.py \
  --subreddit technology \
  --limit 500 \
  --time-window week \
  --metric tfidf \
  --output results/
