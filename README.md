# Internet Rabbit Hole Dataset

A dataset of **50,000 Wikipedia rabbit hole sessions** derived from real human
click behavior, showing how users drift across topics while browsing.

## What is a Rabbit Hole?

A rabbit hole session captures a chain of Wikipedia article clicks:
- Starts on one topic (e.g. *Aerodynamics*)
- Drifts through connected articles
- Ends somewhere surprisingly different (e.g. *Roman Empire taxation*)

## Dataset

| Field | Type | Description |
|-------|------|-------------|
| session_id | string | Unique session identifier |
| month | string | Source clickstream month (2026-05) |
| start_article | string | First Wikipedia article |
| end_article | string | Final Wikipedia article |
| path | list | Full sequence of articles visited |
| path_length | int | Number of hops (4–20) |
| drift_score | float | Mean cosine distance between consecutive hops (0–1) |
| max_step_drift | float | Largest single topic jump in path (0–1) |
| semantic_spread | float | Mean distance from path centroid (0–1) |

## Source

Derived from the [Wikimedia Clickstream dataset](https://dumps.wikimedia.org/other/clickstream/)
for English Wikipedia, May 2026. Licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).

## Repository Structure

## Preview

![EDA Overview](https://raw.githubusercontent.com/vansh-kumar-007/Internet-Rabbit-Hole-Dataset/main/assets/eda_overview.png)
