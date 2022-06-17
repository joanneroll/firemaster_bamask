# firemaster_bamask

Showcasing the issue when working with the burned area mask and ndvi difference data

- burned area mask: rasterized burned_area_composites.gpk data with variables
    - burned_bin: binarized burned area of true burned area (1) and true no burned area / buffer (0)
    - *((ba_mask: rasterized polygons including a 200m buffer with assigned value 1 for multiplication))*
    - *((burn_severity: pixel containing the original (mean) burn severity values of burned_area_composites.gpk))*

- ndvi difference:
    - computed from ndvi timeseries (ndvi difference = ndvi post - ndvi pre)
    - containing nan values and value 0 where ndvi post and ndvi pre with same ndvi value
    - nan values of ndvi difference differ to burned area mask nan/valid values
