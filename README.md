# Project 03 (Final)

This is the final project for the Lede Program.  
**Link to the project**: [https://kenshokuremoto.github.io/Lede2025/](https://kenshokuremoto.github.io/Lede2025/)

## Title

### *The Algorithm Election Comes to Japan*  
*A data-driven look at how two breakout parties—DPP and Sanseito—rose together in the election, but only one dominated YouTube by turning outrage into attention*

---

## Aim

In the July 2025 Upper House election in Japan, the ruling coalition lost its majority while two smaller parties—the Democratic Party for the People (DPP) and Sanseito—made significant gains.  
Both parties are highly active online, but how do they differ in the YouTube space?  
This project analyzes that difference using data collected through the YouTube API.  
For more details, see the **Process** section below.

---

## Findings

- Although both parties had a similar number of related videos on YouTube, **Sanseito received three times more total views** than DPP.
- Analyzing the channels that uploaded these videos revealed that **Sanseito had a higher proportion of user-generated content**, compared to DPP.
- A close look at the video titles showed a clear contrast:  
  - **DPP-related videos** often focused on **policy issues** and **candidates**,  
  - whereas **Sanseito-related videos** frequently promoted **anti-immigrant narratives**, **criticism of mainstream media**, and **attacks on established political parties**—a strategy that fueled its online dominance.

---

## Process

### 1. Data Collection  
We used the YouTube API to retrieve videos containing the names of parties or party leaders in their titles or descriptions.  
We recorded the following attributes: video ID, title, description, upload date, view count, and duration.  
To broaden the dataset, we also scraped videos from 7 major news organizations and 19 politically affiliated YouTube channels, linking all data using video IDs.

### 2. Quantitative Analysis  
Using `pandas`, we calculated total and average views per video.  
Videos under 60 seconds were flagged as Shorts.  
Each uploader was manually categorized (e.g., official, user-generated, media), and genre data was merged back into the dataset.  
We visualized performance and genre trends using **Observable Plot**, referencing a notebook by *tsurezure lab*.

### 3. Title Analysis  
We used the Japanese tokenizer **Janome** to extract nouns, verbs, and adjectives from video titles.  
Stopwords and irrelevant terms were removed.  
To explore thematic structures, we visualized **co-occurrence networks** of frequently appearing words to reveal how certain terms clustered together across party-related content.

---
