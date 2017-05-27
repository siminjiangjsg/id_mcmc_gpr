# id_mcmc_gpr
---
## objective
groundwater (pollution) source identification using modified MCMC technique

#### Ref：
1. Zhang, Jiangjiang, et al. "An adaptive Gaussian process‐based method for efficient Bayesian experimental design in groundwater contaminant source identification problems." Water Resources Research 52.8 (2016): 5971-5984.
2. Harbaugh, Arlen W., et al. "MODFLOW-2000, The U. S. Geological Survey Modular Ground-Water Model-User Guide to Modularization Concepts and the Ground-Water Flow Process." Open-file Report. U. S. Geological Survey 92 (2000): 134.

## Key features：
1. Gaussian Process regression
2. DRAM MCMC
3. source identification
4. random K-field

## Realization techniques:
1. GPR in matlab (*fitrgp* and *predict*)
2. [DRAM toolbox](http://www.helsinki.fi/~mjlaine/mcmc/)
3. modified MODFLOW/MT3DMS
4. K-L expansion technique (from Jiangjiang)

---
## todo list
1. K-field in mf/mt （k-l expansion first）
2. not ijk but coordinate for pollution source 
    1. adaptive modify the gridline(FDM) for each source and run mf/mt, then overlapping the results, or
    2. basis function (in FEM) is adopted to allocate the quantity of each source the adjacent meshs
3. Rewrite Input files (needed to modify in each runs) for running (Array Reading Utility Modules, p86 in Ref.2)

## Having finished

