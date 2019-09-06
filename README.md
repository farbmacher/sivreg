# sivreg
 (Adaptive) Lasso with some invalid instruments

## Description
 sivreg estimates a linear instrumental variables regression where some of the instruments fail the
    exclusion restriction and are thus invalid.  The LARS algorithm (Efron et al., 2004) is applied as
    long as the Hansen statistic (OID test) rejects. The results report the instruments, which are
    identified as invalid, and report the Post-Lasso estimate from a 2SLS regression applying the
    (adaptive) Lasso selection.  For general information about adaptive Lasso see Zou (2006).
    
 sivreg uses the moremata package. If it is not already installed, type "ssc install moremata" in
    Stata.
