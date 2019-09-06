# sivreg
 (Adaptive) Lasso with some invalid instruments

## Description
 `sivreg` estimates a linear instrumental variables regression where some of the instruments fail the
    exclusion restriction and are thus invalid.  The LARS algorithm (Efron et al., 2004) is applied as
    long as the Hansen statistic (OID test) rejects. The results report the instruments, which are
    identified as invalid, and report the Post-Lasso estimate from a 2SLS regression applying the
    (adaptive) Lasso selection.  For general information about adaptive Lasso see Zou (2006).
    
 `sivreg` uses the moremata package. If it is not already installed, type "ssc install moremata" in
    Stata.

## Installing `sivreg``
 The easiest way to install `sivreg` is via the Stata module `github`. Type the following code in Stata:
 
 1. ```{js}
    net install github, from("https://haghish.github.io/github/")
    ```
 2. ```{js}
    github install farbmacher/sivreg
    ```

 Alternatively, copy the sivreg.ado and sivreg.sthlp files into your personal ado folder or the working directory.

## Example
 Let y be the outcome, d an endogenous regressor, x an exogenous control variable and z1 z2 z3 a set of
    potentially exogenous instruments, then the adaptive Lasso regression would be
        
        ```
        sivreg y d x, endog(d) exog(x z1 z2 z3) adaptive
        ```
        
## Reference
 * Windmeijer, F. et al. (2018): On the Use of the Lasso for Instrumental Variables Estimation with Some
             Invalid Instruments, *Journal of the American Statistical Association*, forthcoming.
 * Zou, H. (2006): The Adaptive Lasso and Its Oracle Properties, *Journal of the American Statistical
             Association* 101, 1418-1429.
 * Efron, B. et al. (2004): Least Angle Regression, *Annals of Statistics* 32, 407-499.
