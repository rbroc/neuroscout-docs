# Select Predictors

```{admonition} Note
You can browse all predictors available on Neuroscout [here](https://neuroscout.org/predictors).
```

In this tab, you can browse and search from hundreds of automatically extracted `predictors` to include in your model.

![Select predictors](img/predictors.png)

Predictors each have a unique `Name`, and belong to a `Source`. They are also given a human readable `Description`.

In the above example, we have selected the `building` predictor, that has the source `ClarifaiAPIImageExtractor`.
This is an example of a `predictor` that was extracted from experimental stimuli. This `predictor` encodes the probability of a building in a given frame, according to the [`Clarifai` Image Recognition API](https://www.clarifai.com/models/image-recognition-ai).

You can use the search bar to filter `predictors` across all three columns. For example, here we searched for "image recognition", resulting in 67 matches.

As you select `predictors`, they are displayed in the top right, helping you keep track of `predictors` not in the current search.
You can click on the `x` on the right of each label to unselect that `predictor`.

```{hint} Tip
The `predictor` interface is your sole interface for adding predictors to the `design matrix`, including "confounds".

Since all datasets are pre-processed with `fmriprep`, use that as a search term to display available `confounds`. In this example, we have already selected six `fmriprep` `confounds` to include in the model (`6 rigid-body transforms`, such as `rot_x`).

See the [fmriprep documentation](https://fmriprep.readthedocs.io/en/stable/outputs.html#confounds) for in-depth information about these `confound` variables.
```

```{warning} Danger
Very large models with dozens of predictors may be slow to compile and fit. We recommend starting with smaller models and building up to larger models as you've gained experience.
```

```{note} Note
In order to simplify the interface, Neuroscout only displays the newest version of each predictor (determined by unique name).
If extractors received a major update, we may re-extract a predictor. In this instance, an older analysis would refer to an older version of the Predictor, while a newly created analysis would refer to the latest version.

If you require precise control over the predictor version, you may need to directly access the Neuroscout API using [pyNS](../python_api/overview.md).
```
