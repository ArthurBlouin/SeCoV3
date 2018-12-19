# SeCoV3
Software calculating overpressure generation in 1D due to sedimentation. 

1- Change the parameters in the in-file ("name.dat"). Example given: "in_modif13.dat"

line 1: number of cells in the vertical direction;
line 2: time step for calculations in years;
line 3: number of different soil types/layers;
line 4-5: properties of layer 1
line 4: compressibility law with initial void ratio e0, compression index lambda and the initial vertical effective stress. 
line 5: hydraulic conductivity law with a and b the parameters of the equation k = exp(ae+b) where k is the hydraulic conductivity, e the void ratio. 
Both laws can be obtained from standard oedometric tests;
Repeat lines 4-5 for each defined layer;
line 14: bulk compressibility, fluid compressibility, specific sediment weight, specific weight of water;
line 15: number of different sedimentation rates;
line 16-17-1-19-20: Each sedimentation stages particularities. sedimentation rate in m/1000 years, first year of the stage, last year of the stage, number of the layer with this particular sedimentation rate. Starts with the deepest layer;
line 21: viscosity of the pore fluid in kPa*s;
line 22: step for writing in the outfile;

2- run SeCo_V3.exe

enter the input file name ("name.dat")
enter the output file name ("outname.dat")

3- plot the results using a software like grapher. The results are presented as groups of lines. Each group corresponds to a particular time of calculation. The last group corresponds to the final calculation stage.

j = cell position (1 stands for the shallowest cell);
time;
depth;
Du = overpressure;
sigv = vertical stress;
sigve = vertical effective stress;
Phi = porosity;
e = void ratio;
Gamma = specific weight;
Kz = vertical hydraulic conductivity;
Cv = coefficient of consolidation;
Gib_fact = Gibson factor;
Du/(Du_b+sigve_b) =;
z/h(t) =;
SAR = ;
soil_type;
depthi = initial depth before consolidation;
j_top = ;
zi_top =;
z_top


WARNINGS: 
You may need to repeat several times the process by correcting the sedimentation rates if the initial sedimentation rates input is derived from present thicknesses in order to take into account the compaction process. 
The relationship K*dt/(dz)² < 0.5, whereas model will diverge with dz = z/nz (z = max depth)
