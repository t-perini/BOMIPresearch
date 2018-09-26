# BOMIPresearch
BOMIP algorithms and instances

## Generated Instances 
Rand & Bent instances are generated according to the procedure published in "Boxed Line Method" (Perini et. al. 2018).
All instances are given as .lp files where the LAST constraint is the SECOND objective function.

Bent instances have a bent line segment with n NDPs along with associated cones.
Procedure is given in XXX
Bent instances are generally harder for BLM than the Rand instances.
Filename format: bentNUM.VMILP.lp where NUM is the number of NDPs dominating the bent line segment and V is the version (A-E)

Rand instances are generated with a straight line segment along with n NDPs and associated cones dominating the line segment. 
Procedure given in Perini et. al. 2018
Rand instances are generally easier for BLM than the Bent instances.
Filename format: Rand.NUM.V.MILP.lp where NUM is the number of NDPs dominating the line segment and V is the version (A-E)

---------------------------------------------------------------------------------------------------------------------------

## Historical Instances 
These instances are the first published set of standard BOMIP instances.
Instances were published in the Triangle Splitting Algorithm paper by Boland et al. (2015),
but the original procedure was proposed by Mavrotas and Diakoulaki (1998).
The number for the folder represents the relative size, i.e. C20 are the smallest instances and C320 are the largest.
Instances per class:
C20: 1dat.lp, ..., 5dat.lp
C40: 6dat.lp, ..., 10dat.lp
C80: 11dat.lp, ..., 15dat.lp
C160: 16dat.lp, ..., 20dat.lp
C320: 21dat.lp, ..., 25dat.lp

These instances are available in the original file formats, as published by Boland et al. (2015) at 
http://hdl.handle.net/1959.13/1036183
Note that the original format was specifically for the fomat of the BOMIPs being solved, where the parameters were listed in arrays in a .txt file.
These files require a specific reader for commercial solvers, which we do not provide here.
Instead, we have provided the instances converted into .lp files where the FINAL constraint (left hand side) is the SECOND objective.

The procedure for generating these instances can be summarized in the following way (see Mavrotas and Diakoulaki 1998 for more detail):
The class # identifies the number of constraints, e.g. C320 has 320 constraints.
The number of vairables is equal to the number of constraints; half of the variables are binary, and half are continuous.
Objective function coefficients for continuous variables: Uniform(-10,10)
Objective function coefficients for binary variables: Uniform(-200,200)
RHS values for constraints: Uniform(50,100)
Coefficients for constraints: Uniform(-1,20)
