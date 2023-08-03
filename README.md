# Smart-Lya

### Description:
The goal of the PINN model is to predict the flux and absorption coefficient to satisfy the Radiative Transfer Equation below: <br />
  **∂I/∂x = -α(x) * I(x) where I(x) = F(x) / (c * λ)** <br />
  ∂I/∂x: change in intensity *(erg/s/cm²/Å)* <br />
  I(x): intensity *(erg/s/cm²/Å)* <br />
  F(x): flux *(erg/s/cm²/Å)* <br />
  α(x): absorption coefficient *(1/cm)* <br />
  c: speed of light *(Å)* <br />
  λ: wavelength of Lyman-alpha line *(Å)* <br />

The absorption coefficient is a learnable parameter, so the model will simultaneously predict the flux and adjust the absorption coefficient to satisfy the equation above. 

 ### Model Details:
 Input: normalized wavelengths that cover the Lyman-alpha line </br>
 Prediction: predicts the corresponding flux for that wavelength </br>
 Absorption Coefficient: adjusts the absorption coefficient during training to satisfy the radiative transfer equation </br>
 Intensity Prediction: calculates the intensity </br>
 Radiative Transfer Equation: calculates the left hand side of the equation, and the right hand side </br>
 Physics Constraint: the model minimizes the difference between both the left-hand and right-hand side through loss </br>
 Training: adjusts parameters to minimize the data-driven and physics-constraint loss </br>
 Reconstruction: after training, it can be used to predict the flux across the normalized wavelengths, with the prediction being a plot of the Lyman-alpha line reconstruction. </br>
 
 
