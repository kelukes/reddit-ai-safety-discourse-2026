# Data

## Overview

This folder contains a small anonymized sample of the dataset used in the analysis.  
The full corpus (6,374 posts) is not included in this repository.

| File | Description |
|---|---|
| `sample.csv` | 200-post stratified sample across all clusters |

---

## Sample structure

The sample is stratified by cluster — approximately 8 posts per cluster plus a small number of noise-assigned posts. It includes the following columns:

| Column | Description |
|---|---|
| `title` | Post title |
| `body` | Post body, truncated to 280 characters |
| `communityName` | Subreddit name |
| `upVotes` | Upvote count at time of collection |
| `commentsCount` | Comment count at time of collection |
| `createdAt` | Post creation timestamp |
| `searchTerm` | Search query used to retrieve this post |
| `post_type` | `full` (title + body) or `title_only` |
| `detected_lang` | Detected language of the post |
| `umap_x`, `umap_y` | UMAP coordinates in 2D embedding space |
| `cluster_hdb` | HDBSCAN cluster ID (`-1` = noise) |
| `cluster_prob` | HDBSCAN membership probability |
| `cluster_label` | Human-assigned thematic label |
| `discourse_framing` | Final adjudicated discourse framing |
| `sentiment_label` | `positive` / `neutral` / `negative` |
| `sentiment_valence` | Continuous sentiment score |

---

## Data collection

Posts were collected between **29 January 2026 and 1 March 2026** using a third-party scraping tool via keyword-based search across all of Reddit (not limited to specific subreddits). After collection, subreddits clearly unrelated to the topic were manually filtered out.

### Search terms used (40 total)

| | | |
|---|---|---|
| AI safety | AI risks | AI alignment |
| AI policy | AI regulation | AI bill |
| AI pause | AI moratorium | AI existential risk |
| AI replace jobs | AI automation | AI agents risk |
| AI fairness | AI rights | AI accountability |
| AI governance ethics | AI guardrails | AI sentience ethics |
| AI moral alignment | AI moratorium | responsible AI |
| ethical AI | explainable AI | machine learning fairness |
| machine learning ethics | misaligned AI | deceptive alignment AI |
| build AGI | AGI safety | ASI AGI |
| scalable oversight AI | superintelligence risk | International AI Safety Report |
| LLM safety | jailbreak LLM | prompt injections |
| red teaming LLM | EU AI Act | pro-growth AI |
| accelerate AI | AI progress | |

---

## Ethical considerations

- Data was collected at the aggregate level; **no usernames or personal identifiers are included**
- All source posts are publicly available on Reddit
- The sample is intended for educational and portfolio purposes only
