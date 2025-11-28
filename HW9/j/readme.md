# TASK 1: plots from our class

I chose the in-class-clusteringGenes scattering matrix plot, as I remembered the caption of the plot: It's a mess! the data is too high dimensional for a regular visualization!

*** MORE DETAILED EXPLANATIONS ON THE PLOTS AND CODING ARE GIVEN IN THE NOOTEBOOK, BELOW EACH CELL****

Original Plot:

A pd.plotting.scatter_matrix displaying all pairwise relationships among 84 gene features. While comprehensive, it produced thousands of small, 
redundant plots that were impossible to interpret.
![Original bad plot](https://github.com/elhamkashi/DSPS_EKashi/blob/main/HW9/j/original%20bad%20plot.png?raw=true)


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

1-Clustered correlation heatmap with hierarchical dendrograms:

![Clustered correlation matrix](https://github.com/elhamkashi/DSPS_EKashi/blob/main/HW9/j/Task1/Clustered%20correlation%20matrix.png?raw=true)


2-Masked correlation heatmap showing only the lower triangle to remove duplication:

![Masked correlation matrix](https://github.com/elhamkashi/DSPS_EKashi/blob/main/HW9/j/Task1/Masked%20correlation%20matrix.png?raw=true)




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

# TASK 2: arbitrary plots

![alp bad plot](https://github.com/elhamkashi/DSPS_EKashi/blob/main/HW9/j/alp-bad.png?raw=true)


This figure shows current experimental limits (solid lines), future projections (dashed lines), and theoretical regions for axions and axion-like particles as functions of their mass and photon coupling strength. It effectively compiles a large amount of data but struggles with visual clarity. The overlapping shaded regions, dense color palette, and angled experiment labels create ambiguity, making it difficult to distinguish between experiments or interpret the data without the caption. The logarithmic axes accurately represent the parameter space , so no numerical distortion. The figure’s visualization leads to high distraction — visual noise from redundant lines, text, and gradients draws attention away from the main message. Its data-to-ink ratio is low, with much of the visual space devoted to design elements rather than new information. Several Tufte principles are violated, especially no-chart-junk and data/ink >> 1, A clearer presentation could use simplified color schemes, consistent labeling, and multiple smaller panels (for current limits, projections, and theoretical regions separately). Overall, while the figure is data-rich, its visual complexity reduces interpretability and hides the most important insights. How to make it better: Splitting the information into multiple simpler plots (e.g., current vs. projected experiments) and use consistent, non-overlapping color coding. Reduce redundant labels and gradients so the viewer can clearly identify experimental sensitivities and theoretical regions without needing to rely on the caption.

# Improvement suggestions: 
1- Using flat fills — a single uniform color with slight transparency (alpha) instead of fading tones. Example( matplot): ax.fill_between(x, y1, y2, color='gold', alpha=0.15)


2-Setting z-order: theory (1–2), projections (4), current (5). Example: *zorder=1 → theory region sits in the background *zorder=4 → projections are above theory *zorder=5 → current limits are drawn last and appear on top

As an improved example of this plot one can consider the following figure:

![axionphoton good plot](https://github.com/elhamkashi/DSPS_EKashi/blob/main/HW9/j/axionphoton-good.png?raw=true)



This figure shows the experimental limits and sensitivities for axion and axion-like particle searches as a function of their mass and photon coupling strength, the same data as the above plot.

The visualization is effective because it communicates a large amount of information clearly and without overwhelming the viewer. It uses consistent color coding — green for astrophysical bounds, blue for haloscope experiments, and yellow for theoretical predictions — allowing the reader to quickly distinguish between categories without being lost in colors! The logarithmic axes are correctly scaled, avoiding numerical distortion, and the data relationships are proportional to the actual physical parameters, maintaining an effect size ≈ 1. The plot avoids unnecessary chart junk: there are no redundant gradients, excessive decorative elements, or overlapping transparency effects that distract from the data. Labels are neatly aligned, minimal, and mostly horizontal, improving readability.

The figure also respects data/ink efficiency — almost every visual element conveys information (either experimental limits, theoretical models, or frequency conversion). By keeping the layout simple and color-balanced, the figure directs attention toward the core insight: how experimental sensitivities cover the theoretically predicted axion region.

Finally, it succeeds in avoiding redundancy and ambiguity and each experiment is labeled well. Compared to previous cluttered versions, this plot exemplifies Tufte’s principle of graphical clarity, showing complex scientific data with effective proportionality, and precision. While figure does not have a legend, it still works well because the color coding and labeling are self-explanatory
