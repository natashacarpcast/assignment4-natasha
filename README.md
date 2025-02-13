# Assignment 4 - Natasha Carpio Castellanos

This repository contains a Tableau dashboard and an accompanying narrative for exploring the moralization of self improvement.

## Research Questions

1) To what degree is moral language present when talking about self improvement?

2) How does the usage of moral language associate with different emotions in the context of self-improvement?

## Data

Submissions and comments from the subreddit r/selfimprovement were analyzed to obtain scores of moralization language according to two different dictionaries: The Moral Foundations Dictionary 2.0 (MFD) and the LIWC Dictionary. The same was done with other two subreddits: r/investing and r/homeowners. Then, some feature engineering was done to obtain aggregated scores and word frequencies to facilitate Tableau visualization. Code for this manipulation can be find in the [data-prep notebook](data-prep.ipynb). The data and a more detailed explanation are available in the [data folder](data).

## Tableau Dashboard

* [Link to the public dashboard]
* A [PDF](PDFTableau.pdf) with the static (non interactive) images.

## Narrative: Moralization Language in r/selfimprovement

This Tableau dashboard explores the use of moralization language on the subreddit r/selfimprovement, comparing it with two other subreddits and providing details within r/selfimprovement itself.

### Moralization language across subreddits (Upper left bar charts)

The first graph consists of two bar plots, one above the other, highlighting the moralization language in r/selfimprovement relative to the other subreddits. The comparison uses two measurement tools: the MFD and the LIWC Dictionary. The goal is to strengthen the argument by showing consistent results with different methods. Bar plots were chosen for their ability to clearly convey these differences.

The MFD theory is based on the idea that morality is made up of distinct “foundations". The stacked bar plot illustrates these foundations, making it easy to see the differences of each of them across subreddits. However, by excluding foundation labels, the emphasis remains on the overall score and interactivity allows users to hover over each foundation to explore the specific foundations details. The color choices aim to represent each foundation's values while ensuring accessibility.

The LIWC bars are more straightforward, representing a single score. Hovering over them reveals the mean values for each subreddit. Future updates could include quantile values in the tooltip for deeper insights.

### Top LIWC moralization words  and their overall emotional balance on r/selfimprovement (Upper right packed bubbles plot)
The packed bubbles plot highlights the most frequently used moralization words. While this design does not perfectly show the differences in word frequencies, it adds an engaging visual contrast to the other three basic plots. The goal is to showcase popular moralization words in a visually appealing way, without an immediate need for specific frequencies. However, hovering over each bubble will reveal each word’s frequency if that is of interest to the reader. Furthermore, the distribution of the bubbles in the space was set to put the most frequent words in the middle to keep the focus on them. For a more nuanced interpretation, the tooltip also displays raw positive and negative emotion scores, as well as the specific overall emotional balance score.

### Moral foundations focus on r/selfimprovement (Lower left pie chart)
The pie chart compares the distribution of virtue and vice language according to the MFD. This dictionary distinguishes between language that praises ("honest") and criticizes ("dishonest"). A pie chart choice helps to compare proportions of the whole, and with only two categories it remains easy to interpret. The tooltip provides the exact proportion, and in future versions, I could display the most common virtue and vice words along with their frequencies.

### Moral language in r/selfimprovement's documents over time (Lower right line chart)
This plot illustrates the evolution of moral language using two dictionaries, demonstrating an increase over time. Data for years 2008-2011 were removed due to extremely low number of documents that weren't comparable with the rest of the years. The plots are faceted due to their inherent measurement differences: the MFD total score sums proportions across moral foundations, thus being typically higher than LIWC, which measures a single dimension. Regarding colors, the MFD line is colored to harmonize with the tones in the bar chart, while the LIWC moral scores are colored to match their corresponding bar chart color. They also keep the same order than in the bar chart.

### Conclusion
This dashboard provides a general overview of the presence and use of moralization language in r/selfimprovement, with insights into how it is framed.
