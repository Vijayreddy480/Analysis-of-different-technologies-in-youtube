# 🎥 Analysis of Different Technologies in YouTube

> 📊 **Analyzing the popularity of technologies and programming languages on YouTube using YouTube Data API v3**

![GitHub Repo Stars](https://img.shields.io/github/stars/Vijayreddy480/Analysis-of-different-technologies-in-youtube?style=social)
![GitHub Forks](https://img.shields.io/github/forks/Vijayreddy480/Analysis-of-different-technologies-in-youtube?style=social)

---

## 📌 Project Overview

This project explores how different **technologies** and **programming languages** are received on YouTube by analyzing:

- 📺 Views
- 👍 Likes
- 👥 Subscriber count
- ⏱️ Video length
- 📅 Publish date
- 📣 Channel name

> **API Used:** [YouTube Data API v3](https://developers.google.com/youtube/v3)

---

## 🛠️ Implementation Details

### 🔗 API Request Setup
- Used the `requests` library to send **GET** requests to the YouTube Search API.
- Parameters passed:
  - `q="Python programming"`
  - `maxResults=50`
  - `part="snippet"`
- Extracted video IDs from the response JSON.

### 📊 Fetching Video Statistics
- Used `videos().list()` to retrieve:
  - Views
  - Likes
  - Duration
  - Other video-level metrics

### 🧹 Data Processing
- Parsed responses into a structured **Pandas DataFrame**.
- Applied **dynamic filtering** for precise extraction and quality control.

### ⚠️ Challenges & Solutions
- **KeyError: 'videoId'** resolved by filtering out non-video results.
- Handled **pagination** to retrieve 500+ results using `nextPageToken`.
- Implemented robust error-handling:
  - Invalid API key fallback
  - Rate-limit detection

---

## 📁 Directory Structure

```bash
📦Analysis-of-different-technologies-in-youtube
 ┣ 📂datasets/             # Raw and processed YouTube video data
 ┣ 📂notebooks/            # Jupyter notebooks for EDA
 ┣ 📂power BI plots/       # Charts and graphs
 ┣ 📜README.md             # Project README

