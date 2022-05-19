# PCP Data Processor 

## Steps for Loading and Processing PCP Data Archive

1. Determine which performance metrics are present in a file:

```
pminfo -a <archive file>
```

2. Load an archive into Redis for subsequent query via pmseries:

```
pmseries --load <archive file>
```

3. Query pmseries for the latest # values of a particular metric:

```
pmseries '<metric-name>[count:#]'
```
