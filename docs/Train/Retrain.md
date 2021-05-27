# `clinicadl train from_json` - Launch a new network training based on a JSON file

This command allows to train a network defined in a `commandline.json` generated by 
[`clinicadl train`](Introduction.md) or 
[`clinicadl random-search generate`](../RandomSearch.md#clinicadl-random-search-generate--train-random-models-sampled-from-a-defined-hyperparameter-space).

This is particularly useful for outputs of random search, as the random architecture
produced my be not straightforward to implement.

!!! note "JSON file generation"
    JSON files that may be used by `clinicadl train from_json` can be generated
    by filling the options of [`clinicadl train`](Introduction.md#running-the-task).
    The undefined values of optional parameters will be automatically replaced by their default value.
    You can also reuse (and modify) the `commandline.json` files automatically generated by other `clincadl train`
    modes!

## Prerequisites

Please check which preprocessing needs to be performed in the JSON file used as input. 
If it has not been performed, execute the preprocessing pipeline as well as `clinicadl
preprocessing extract-tensor` to obtain the tensor versions of the images.

## Running the task
This task can be run with the following command line:
```Text
clinicadl train from_json <json_path> <output_dir>

```
where 
- `json_path` (str) is a path to the JSON file used to build the model.
- `output_dir` (str) is a path to the folder of the new model that will be trained.

## Outputs

The outputs correspond to the ones obtained using [`clinicadl train`](Introduction.md#outputs).