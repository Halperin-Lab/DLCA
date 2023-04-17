# DLCA

Compiled DLCA program for Windows.

Running the program will ask you for initial parameters. Hit enter after each prompt to set parameter

- L.x, L.y, and L.z: final dimensions of the box size. 
    
    type = double-precision float

- Linit.x, Linit.y, and Linit.z: initial dimension of the box size. While these can be different from final size, we have found it doesnt lead to anything interesting so all results have kept L.x = LInit.x, L.y = LInit.y, and L.z = LInit.z.
    
    type = double-precision float

- N is the total number of particles.
    
    type = positive integer
    
- mu: mean particle size. mu is the first moment of the distribution of radii, not the standard mu (location) parameter for a Log-normal distribution.
    
    type = double-precision float
    
- sigma: standard deviation of the distribution of particle radii. Again, this is the actual square root of second moment of Log-normal distribution, not the sigma (scale) parameter for a Log-normal distribution.
    
    type = double-precision float
      
- alpha: diffusion powerlaw. Diffusivity ~ m^(-alpha) where m is the size of the cluster and alpha is the diffusion powerlaw 
    
    type = double-precision float
    
- paramLogNormal: choice between using a LogNormal distribution (1) or Normal distribution (0) for the particle radii
    
    type = bool 
    
- rConstants.x, rConstants.y, rConstants.z: step size in each direction. For anisotropic aerogel rConstants.z =/= rConstants.x = rConstants.y
   
   type = double-precision float
    
- cConstants.x, cConstants.y, cConstants.z: offset for step direction. Almost always set to 0 so that the particle steps from previous position.
    
    type = double-precision float
    
- File location: File location and name.


Once all parameters are initialize, the program will generate an initial sample of randomly positioned spheres in the initial box. Simulation begins when the sample is fully generated. Program will output the current number of clusters. The program will run until the number of clusters = 1. 

Final aerogel structure will be output into a list (csv format) with the 3-D coordinate and radii of each particle. File will include a header with simulation parameters used. 
