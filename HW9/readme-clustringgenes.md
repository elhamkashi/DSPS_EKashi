I chose the in-class-clusteringGenes scattering matrix plot, as I remembered the caption of the plot: It's a mess! the data is too high dimensional for a regular visualization!

***  DETAILED EXPLANATIONS ON THE PLOTS AND CODING ARE GIVEN IN THE NOOTEBOOK, BELOW EACH CELL****

Original Plot:

A pd.plotting.scatter_matrix displaying all pairwise relationships among 84 gene features.
While comprehensive, it produced thousands of small, redundant plots that were impossible to interpret.
![Original scatterplot matrix showing gene expression data](https://github.com/elhamkashi/DSPS_EKashi/raw/main/HW9/original%20bad%20plot.png)

# Evaluation of the Scatter Matrix

**Overall Issue**
Visual clutter dominates, preventing identification of meaningful gene correlations. The viewer focuses on repetitive design elements rather than data relationships.

**Critical Failures**

**1. Ambiguity & Distraction**

    * No title and unreadable overlapping labels
    * Too many tiny subplots (3,486 pairs for 84 genes)
    * Impossible to interpret specific relationships
    * Design noise overwhelms meaningful data patterns


**2. Distortion & Lie Factor**

    * All relationships appear equally noisy due to small plot sizes
    * Cannot distinguish strong from weak correlations
    * Visual representation doesn't scale with actual effect sizes
    * Lie factor << 1: weak visual representation of true correlations


**3. Poor Data-Ink Ratio**

    * Excessive ink on gridlines and repeated axes
    * Each gene pair shown twice (upper/lower triangle)
    * Diagonal self-correlations add no information
    * Data-ink ratio << 1: more decoration than data communication


***Recommended Solution***

Replace with a **correlation heatmap ** that:

    * Uses color to directly represent Pearson correlation values
    * Eliminates redundancy by masking one triangle
    * Provides clear color scale and clustering
    * Maximizes data-ink ratio by removing chart junk
    * Makes correlation patterns immediately visible


Final Plots:

Two complementary correlation visualizations:

1-Clustered correlation heatmap with hierarchical dendrograms.
![Clustered correlation heatmap of gene expressions](https://github.com/elhamkashi/DSPS_EKashi/raw/main/HW9/Clustered%20correlation%20matrix.png)
2-Masked correlation heatmap showing only the lower triangle to remove duplication.
![Masked correlation heatmap eliminating redundancy](https://github.com/elhamkashi/DSPS_EKashi/raw/main/HW9/Masked%20correlation%20matrix.png)




What Changes Made and Why:

1. Replaced Scatterplot Matrix with Correlation Heatmaps

Problem: The scatterplot matrix generated 3,486 subplots, each too small to show meaningful trends.

Solution: Heatmaps encode correlation strength and direction through color, allowing relationships to be seen at a glance.

Tufte Principle: Show data variation, not design variation.

2-Removed Redundancy

Problem: Each pairwise comparison appeared twice (above and below the diagonal).

Solution: The masked heatmap hides the upper triangle, eliminating duplicate information.

Tufte Principle: Avoid redundancy in communication.

3. Introduced Hierarchical Clustering

Problem: The alphabetical gene order obscured biological patterns.

Solution: Clustering groups similar genes together, revealing natural co-expression structures.

Tufte Principle: Use informative orderings and small multiples effectively.

4. Improved Data–Ink Ratio

Problem: The scatterplot matrix wasted visual space on axes, grids, and repeated frames.

Solution: Heatmaps focus visual ink on meaningful data, with a single unified color scale.

Tufte Principle: Maximize the data–ink ratio.

5. Reduced Label Clutter

Problem: Overlapping gene names made the original plot unreadable.

Solution: Simplified labels and focused on global correlation patterns rather than individual feature names.

Tufte Principle: Eliminate chart junk to clarify meaning.







