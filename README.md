# SC-qMAS-Data-JMR-2019
Diffusion data used in JMR, Vol 300 (2019), p. 84-94. Doi: 10.1016/j.jmr.2019.01.007 

A description of the .mat files contents can be found below. Feel free to 
use the included data but please cite 

Sune Nørhøj Jespersen, Jonas Lynge Olesen, Andrada Ianuş, Noam Shemesh,
Effects of nongaussian diffusion on “isotropic diffusion” measurements: An ex-vivo microimaging and simulation study,
Journal of Magnetic Resonance,
Volume 300,
2019,
Pages 84-94,
ISSN 1090-7807,
https://doi.org/10.1016/j.jmr.2019.01.007.

Description:

Data was acquired used a rat cervical spinal cord using standard perfusion 
procedures. That is deep anesthetization with pentobarbital followed by 
transcardial perfusion. After fixation, the tissue was immersed in 4% PFA 
for 24h post-mortem, and then placed in a PBS solution for additional 24h. 
Acquisition was performed using a 5 mm NMR tube filled with Fluorinert 
(Sigma Aldrich, Lisbon, Portugal). 

Imaging was performed on a 16.4T Bruker Aeon Ascend magnet interfaced with 
an AVANCE IIIHD console, and equipped with a micro5 probe with gradients 
capable of producing up to 3000 mT/m in all directions. A birdcage coil 
with inner diameter of 5 mm, tuned for 1H was used for both transmission 
and signal reception. A spin-echo EPI sequence was modified to accommodate 
isotropic diffusion encoding gradient waveforms (which were generated 
according to Nillsson et al., Magn. Reson. Med. 2017 and Topgaard et al., 
Phys. Chem. Chem. Phys. 2018) with a duration of 7.5 ms and separation of 
1.15 ms. The following acquisition parameters were used: EPI bandwidth = 
441kHz, 2-shots, matrix size 80 by 60 with, in-plane resolution = 75 by 75, 
slice thickness = 1.8 mm, number of averages = 4, and TR/TE = 3750 / 41 ms. 
The isotropic diffusion gradient sequence was acquired with 20 b-values 
ranging linearly from 0 to 3 ms/, and 12 different orientations were 
acquired for each b-value. This scheme was then repeated 4 times to allow 
comparison of variability over orientations with measurement uncertainty. 

Additionally, supporting SDE data was acquired using similar parameters 
with 4 ms pulse duration, 9 ms seperation, and 21 b-shells with b-values 
ranging linearly from 0 to 3 and 30 directions.


Mat file contents:

data:
60x80x20x12x4 array containing the 60x80 isotropically diffusion weighted
images for 20 weightings, 12 directions, and 4 repetitions.

b:
The 20 b-values.

grads:
Gradient profiles (3x937) along the laboratory frame's x, y, and z axes and
a time resolution resulting in 937 time points. Such a profile is provided
for each weighting, orientation, and repetition resulting in total in a 
3x937x20x12x4 array.

phi, theta, zeta:
Euler angles defining the gradient orientation -- XZX rotations.

dataSDE:
60x80x630 array containing SDE data sorted as 21 shells x 30 directionss =
630 weightings.

B:
SDE diffusion weighting tensors (3x3x630).
