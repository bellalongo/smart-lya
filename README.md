# Smart-Lya

## Description:
The goal of the PINN model is to predict the flux and adjust the absorption coefficient to satisfy the Radiative Transfer Equation below: <br />

  &nbsp; **∂I/∂x = -α(x) * I(x) where I(x) = F(x) / (c * λ)** <br />
  
  &ensp; &ensp; ∂I/∂x: change in intensity *(erg/s/cm²/Å)* <br />
  &ensp; &ensp; I(x): intensity *(erg/s/cm²/Å)* <br />
  &ensp; &ensp; F(x): flux *(erg/s/cm²/Å)* <br />
  &ensp; &ensp; α(x): absorption coefficient *(1/cm)* <br />
  &ensp; &ensp; c: speed of light *(Å)* <br />
  &ensp; &ensp; λ: wavelength of Lyman-alpha line *(Å)* <br />

 ## Model Details:
   <ins>Input</ins>: normalized wavelengths that cover the Lyman-alpha line </br>
   
   <ins>Prediction</ins>: predicts the corresponding flux and intensity for that wavelength </br>
   
   <ins>Radiative Transfer Equation</ins>: calculates the left-hand side of the equation to be used in the physics-constraint loss term </br>
   
   <ins>Physics Constraint Loss</ins>: the model minimizes the difference between both the left-hand and right-hand side </br>
   
   <ins>Training</ins>: adjusts parameters to minimize the data-driven and physics-constraint loss </br>
   
   <ins>Reconstruction</ins>: after training, it can be used to predict the flux across the normalized wavelengths, with the prediction being a plot of the Lyman-alpha line reconstruction. </br>
 
 
