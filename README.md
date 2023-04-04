# MTvC_app

##### Description

`MTvC_app` is an application that provides an easy to use interface to the statistical analysis of data were multiple (categorical) treatment conditions are compared to a single control condition.

##### Details

* App that provides an easy to use interface to the statistical analysis of data were multiple (categorical) treatment conditions are compared to a single control condition. E.g. the analysis of the effect of 3 different compounds on kinase activity relative to the vehicle control (e.g. the effect of spiking in a compound in the sample). It tests for significant effects anywhere between the treatments (including control) and for significant effect between all separate control-treatment pairs. In addition, peptides with similar response to the treatments will be grouped using a clustering approach.
* This is suitable for the analysis of experimental designs where sample treatments are balanced over experimental units such as PamChips or PS-12 runs.
If so, systematic variation between experimental units will be accounted for in the analysis, by modeling the two main effects "Treatment"and "Experimental Unit" in a 2-way ANOVA (without interaction). If this is not applicable the Experimental Unit term can be omitted from the analysis and 1-way ANOVA will be applied.
* This App is implemented in the C1-T1-T2-T3 workflow, a PS12 workflow that may provide a good starting point for using this app.
* volcano plot visualization to inspect the overall results of the control versus treatment tests.
* Clusters of peptides with similar response to treatment are shown in cluster plots like the ones shown here.
* Treatment effects are visualized using a ratio map, with the peptides organized in clusters.
* The basal data is visualized using a heatmap with the peptides sorted according to their mean over all treatments.
* There is a basic version of this PamApp that lacks the peptide clustering functionality but has the possibility to analyse multiple samples at the same time.

The input data is the [MTvC dataset]()

This workflow has 6 operators:

* [log_cutoff_operator](https://github.com/tercen/log_cutoff_operator)
* [mean_operator](https://github.com/tercen/mean_operator)
* [zscore_scaling_operator](https://github.com/tercen/zscore_scaling_operator)
* [rank_by_row_mean_operator](https://github.com/tercen/rank_by_row_mean_operator)
* [model_based_clustering_operator](https://github.com/model_based_clustering_operator)
* [CvsT_operator](https://github.com/tercen/CvsT_operator)

This workflow has 5 views:

* Basal Data View
* Peptide Cluster View
* Ratio Map View
* Ratio Map for Significant Peptides
* Volcano Plot View

##### See Also

[MTvC_app](https://github.com/tercen/MTvC_app)
