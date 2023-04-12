# DLCA

Compiled DLCA program

Running the program will ask you for initial parameters. Hit enter after each prompt to set parameter

- L.x, L.y, and L.z: final dimensions of the box size. 
    type = double-precision float

- Linit.x, Linit.y, and Linit.z: initial dimension of the box size.
    type = double-precision float
While these can be different we have found it doesnt lead to anything interesting so all final results have kept L.x = LInit.x, L.y = LInit.y, and L.z = LInit.z.

- N is the total number of particles.
    type = positive integer
    
- mu  is the mean particle size. 
    type = double-precision float
    
- sigma: variance of the distribution of particle sizes.
    type = double-precision float
      
- alpha: diffusion powerlaw. Larger 
    type = double-precision float
    
- paramLogNormal: choice between using a LogNormal distribution (1) or Normal distribution (0) for the particle radii
    type = bool 
    
- rConstants.x, rConstants.y, rConstants.z: step size in each direction
    type = double-precision float
    
- cConstants.x, cConstants.y, cConstants.z: offset for step direction. Almost always set to 0 so that the particle steps from previous position.
    type = double-precision float
    
File location: File location and name.


