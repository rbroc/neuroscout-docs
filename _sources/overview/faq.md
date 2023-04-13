# Frequently Asked Questions



```{admonition} Is this service free to use?
:class: note, dropdown
Yes! Note, however, that Neuroscout is a web-based engine for fMRI analysis specification; at the moment,
we don't provide free computing resources for the execution of the resulting analysis bundles. 
Analyses can be run on Google Colab—a demo notebook is provided [here](https://colab.research.google.com/github/neuroscout/neuroscout-cli/blob/master/examples/Neuroscout_Colab_Demo_NoMount.ipynb).
```

```{admonition} I plan to publish results I've obtained using Neuroscout. How do I cite it?
:class: note, dropdown
After you generate an analysis, a "Bibliography" tab will be shown which will auto-generate a reference list for
the dataset, feature extractors, and scientific software used for that analysis. In addition to these references,
be sure to include the unique analysis ID associated with any results.

Also, be sure to cite the Neuroscout platform as follows:

*Neuroscout, a unified platform for generalizable and reproducible fMRI research.* Alejandro de la Vega, Roberta Rocca, Ross W. Blair, Christopher J. Markiewicz, Jeff Mentch, James D. Kent, Peer Herholz, Satrajit S. Ghosh, Russell A. Poldrack, Tal Yarkoni.
bioRxiv 2022.04.05.487222; doi: https://doi.org/10.1101/2022.04.05.487222 
```

```{admonition} Are there any restrictions on analyses I've created?
:class: note, dropdown
Yes. By using Neuroscout, you agree that once you have finalized and "compiled" an analysis, the analysis
can no longer be deleted from our system. If you wish to 'edit' an analysis, you may clone the analysis,
and make any desired changed on the forked version. Although analyses are by default not searchable by
other users, any user with the private analysis ID may view your analysis.

Also, in the event that you publish any results generated using the NeuroScout interface, you *MUST* provide
a link to the corresponding analysis page(s) on the NeuroScout website.
```


```{admonition} I have a naturalistic study I'd like to share on Neuroscout. How do I do so?
:class: note, dropdown

Due to the cost of extracting features from multi-modal stimuli using external APIs, the set of
datasets we support is manually curated. However, we are continually expanding the list of supported
datasets, and we encourage researchers to contact us if they want to make their data available for use in
Neuroscout. Note that it is much easier for us to ingest datasets that are already deposited in the
<a href="https://openneuro.org"> OpenNeuro</a> repository, and we we strongly recommend uploading your
dataset to <a href="https://openneuro.org"> OpenNeuro</a> whether or not it eventually ends up in
Neuroscout.

```


```{admonition} I want to make changes to an analysis I already ran, but it is locked. How can I edit it?
:class: note, dropdown
Once an analysis has been run, it is permanently locked and archived for provenance. You may "clone" your
analysis, and make changes to this new copy of your analysis. This iterative workflow ensures the provenance of existing analyses, while allowing users the flexibility to continue to modify and improve models. 
```


```{admonition} I want to make one of my "private" analyses public, but the website says the analysis is "locked"!
:class: note, dropdown
When an analysis is locked, you can no longer make any substantive changes that affect model specification.
However, you can always edit the name, description, and public/private status. So go ahead and make your
analysis public!
```


```{admonition} How do you automatically extract features from naturalistic datasets?
:class: note, dropdown
The original stimuli presented to users are submitted to various machine learning algorithms and services
to extract novel feature timecourses. To facility this process, we have developed a Python library for
multimodal feature extraction called pliers.
Pliers allows us to extract a wide-variety of features across modalities using various external content
analysis services with ease. For example, we are able to use Google Vision API to encode various
aspects of the visual elements of movie frames, such as when a face is present. 

In addition, pliers
allows us to easily link up various feature extraction services; for example, we can use the IBM Watson
Speech to Text API to transcribe the speech in a movie into words with precise onsets, and then use a
predefined dictionary of lexical norms to extract lexical norms for each word, such as frequency. We can
then generate timecourses for each of these extracted features, creating novel predictors of brain
activity.  

For more information of pliers, please see the [GitHub repository](https://github.com/tyarkoni/pliers) and the following
paper:

> McNamara, Q., De La Vega, A., & Yarkoni, T. (2017, August). Developing a comprehensive framework for
> multimodal feature extraction. In Proceedings of the 23rd ACM SIGKDD International Conference on Knowledge
> Discovery and Data Mining (pp. 1567-1574). ACM.
```

```{admonition} Am I restricted to mass univariate GLMs, or can I use Neuroscout to specify other kinds of analyses?
:class: note, dropdown
Currently, that is the primary analysis mode of Neuroscout. However, the underlying BIDS-StatsModel is designed with more complex models in mind, such as predictive and linear-mixed effect models. 

In addition, using pyNS, users are free to access the Neuroscout API and develop novel analysis workflows using extracted Predictors and Datasets. The Neuroscout team is also actively expanding the types of models that can be created to including predictive encoding and decoding multivariate models.
```

```{admonition} Can I contribute my own predictors to Neuroscout?
:class: note, dropdown
Yes! Using the "My Predictors" function, you can create custom collections of predictors to add to your analyses.
Simply navigate to [My Predictors](https://neuroscout.org/mycollections) and click on "Add New Predictors".

For more information, see the guide on [Upload Predictors](../web/upload.md)
```