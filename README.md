# Assignment 4 - Natasha Carpio Castellanos

This repository contains a Tableau dashboard and an accompanying narrative for exploring the moralization of self improvement.

## Research Questions

1) To what degree is moral language present when talking about self improvement?

2) How does the usage of moral language associate with different emotions in the context of self-improvement?

## Data

Submissions and comments from the subreddit r/selfimprovement were analyzed to obtain scores of moralization language according to two different dictionaries: The Moral Foundations Dictionary 2.0 (MFD) and the LIWC Dictionary. The same was done with other two subreddits: r/investing and r/homeowners. Then, some feature engineering was done to obtain aggregated scores and word frequencies to facilitate Tableau visualization. Code for this manipulation can be find in the [data-prep notebook](data-prep.ipynb). The data and a more detailed explanation are available in the [data folder](data).

## Tableau Dashboard

* [Link to the public dashboard]
* A [PDF] with the static (non interactive) images.

## Narrative: Moralization Language in r/selfimprovement

This Tableau dashboard explores the use of moralization language on the subreddit r/selfimprovement, comparing it with two other subreddits and providing details within r/selfimprovement itself.

### Moralization Language Across Documents (Leftmost Graph)

The first graph consists of two bar plots, one above the other, highlighting the moralization language in r/selfimprovement relative to the other subreddits. The comparison uses two measurement tools: the MFD and the LIWC Dictionary. The goal is to strengthen the argument by showing consistent results with different methods. Bar plots were chosen for their ability to clearly convey these differences.

The MFD theory is based on the idea that morality is made up of distinct “foundations". The stacked bar plot illustrates these foundations, making it easy to see the differences of each of them across subreddits. However, by excluding foundation labels, the emphasis remains on the overall score and interactivity allows users to hover over each foundation to explore the specific foundations details. For example, hovering over the light blue section reveals that the "Care" foundation shows the largest difference between r/selfimprovement and the other subreddits. The color choices aim to represent each foundation's values while ensuring accessibility.

The LIWC bars are more straightforward, representing a single score. Hovering over them reveals the mean values for each subreddit. Future updates could include quantile values in the tooltip for deeper insights.

### Virtue vs. Vice Language (Upper Right Pie Chart)

The pie chart compares the distribution of Virtue and Vice language according to the MFD. This dictionary distinguishes between language that praises ("honest") and criticizes ("dishonest"). A pie chart choice helps to compare proportions of the whole, and with only two categories it remains easy to interpret. The chart shows that about ~75% of the moral language in r/selfimprovement focuses on positive virtues, while the remaining ~25% uses negative connotations. This could explain why moralization scores do not correlate with negative emotional scores, as explored in a previous assignment. The tooltip provides the exact proportion, and in future versions, I could display the most common virtue and vice words along with their frequencies.

### Top Moralization Words (Lower Right Packed Bubbles Plot)
The packed bubbles plot highlights the most frequently used moralization words. While this design does not perfectly show the differences in word frequencies, it adds an engaging visual contrast to the other two straightforward plots. The goal is to showcase popular moralization words in a visually appealing way, without an immediate need for specific frequencies. However, hovering over each bubble will reveal each word’s frequency if that is of interest to the reader. Furthermore, the distribution of the bubbles in the space was set to put the most frequent words in the middle to keep the focus on them. Moreover, the color of each bubble reflects the mean overall emotional balance (positive minus negative emotions score) of the posts in which the word appears, and the outline of each bubble helps to distinguish the white ones that have a neutral value —because they are used almost equally in both positive and negative contexts. For a more nuanced interpretation, the tooltip also displays raw positive and negative emotion scores, as well as the specific overall emotional balance score.

### Conclusion
This dashboard provides a general overview of the presence and use of moralization language in r/selfimprovement, with insights into how it is framed.
