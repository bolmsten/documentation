## Users

* Access Groups - Access is locked down
* Users

## Datasets



### Datablocks

A Dataset can contain many datablocks, which then contains the actual datafiles. When a Dataset is sent to the backup system, the datafiles are split up into Datablocks \(for size limitations\). These are mirrored in the database, but not visible to end users. In order to retrieve the files associated with a Dataset, queries must go through the Datablock API.

#### Relations

 It should be noted that the relation is not fulfilled in Loopback. An endpoint for `datasets/id/datablocks` is auto generated by Loopback but the relation is not fulfilled. To access datablocks,  the loopback query syntax must be used in the Datablock API.

I.e.

```
dataBlockService.find({"where":{"datasetId":"201"}})
```


