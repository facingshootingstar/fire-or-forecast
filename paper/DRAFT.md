# Fire or Forecast? Does Wildfire Risk ML Learn Fire Signals or Seasonal Proxies?

## Abstract
Wildfire classifiers often mix fire-proximal cues (fuel, ignition) with seasonal and geographic proxies (day-of-year, temperature, VPD). We ask whether standard models mostly "smell summer." On a controlled public-style experiment with three feature sets—full, proxies-only, and stripped-proxies—proxy-only models nearly match full AUC while stripped models collapse, indicating seasonal leakage.

## Results (notebook run, seed 42)
```
     feature_set model      auc       ap
            full   HGB 0.605580 0.024288
            full    LR 0.712208 0.045269
    proxies_only   HGB 0.535029 0.017466
    proxies_only    LR 0.620633 0.023427
stripped_proxies   HGB 0.583532 0.022963
stripped_proxies    LR 0.713399 0.085436
```

## Conclusion
If proxies-only ≈ full AUC, deployment metrics may track climate calendars more than ignition physics. Strip proxies before claiming fire-intelligence.

## Code
`notebook/fire-or-forecast-proxy-strip.ipynb` — independent repository.
