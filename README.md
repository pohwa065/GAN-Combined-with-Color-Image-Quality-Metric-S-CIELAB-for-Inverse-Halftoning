# GAN-Combined-with-Color-Image-Quality-Metric-S-CIELAB-for-Inverse-Halftoning
## Introduction
S-CIELAB is an extension of the CIE Lab* Delta E color difference formula and provides human spatial sensitivity difference between a reference and a corresponding test image. The proposed work is to use S-CIELAB delta E maps as generator perceptual loss in GAN to incorporate human spatial color sensitivity during model training. 

## Feature map
**VGG19:** Pre-trained deep convolutional neural network  <br>
**S-CIELAB:** Consisted of color transformation and spatial filtering steps for pattern-color separation

*(a) VGG19 3rd convolution layer in 3rd block*
![Picture1](https://user-images.githubusercontent.com/65942005/147321996-bfb501b2-216d-4055-993a-b77f044ad7f8.png)
<br>
*(b) S-CIELAB*<br>
<img src="https://user-images.githubusercontent.com/65942005/147322068-7886ff52-6916-4126-b23c-5bf58564e481.png" width='550' height='300'>


## Model and sample description
**- Describable Textures Dataset (DTD) (training/validation: 4350/500)** <br>
**- Generate halftone version of images for training** <br>
**- SRGAN is implemented as baseline** <br>

![Picture3](https://user-images.githubusercontent.com/65942005/147322184-16586287-fe09-4169-88d4-339671ae4a15.png)


## Model performance with different content loss
Difficult to make training progress with S-CIELAB alone <br>
<br>
![Picture4](https://user-images.githubusercontent.com/65942005/147322235-ac4c6074-2eb6-4fe0-b7f9-ca44a639ae9e.png)<br>
<br>
<img src="https://user-images.githubusercontent.com/65942005/147322318-8490f600-d104-4d0c-9e1f-81f5962a2fdb.png" width='650' height='200'>


## Comparison of S-CIELAB and VGG19 feature maps
**- Half toned pattern are preserved in S-CIELAB representation, i.e., not negligible to human eye** <br>
**- The VGG19 feature maps are quite similar to images filter at different spatial frequencies** <br>
<br>
<br>
*(a) Halftoned pattern is not decoupled from the images using S-CIELAB*
<br>
![Picture6](https://user-images.githubusercontent.com/65942005/147322388-ef2097d3-f976-43fa-a093-4b94449fe833.png) <br>
<br>
*(b) Halftoned pattern can be separated from the images using VGG19*
<br>
![Picture7](https://user-images.githubusercontent.com/65942005/147322452-a701b08a-e32e-449e-881e-fa7d9aa861cc.png) <br>
<br>
*(c)Halftoned signatures are not captured by the combined feature extraction*
<br>
![Picture8](https://user-images.githubusercontent.com/65942005/147322478-67e045ac-9bee-4846-94e1-9266f31e12cc.png) <br>
<br>
## Recovered images from the validation dataset
<img src="https://user-images.githubusercontent.com/65942005/147322502-1aa40f35-9483-4300-ab78-1da135d51884.png" width='650' height='200'> <br>
<br>
![Picture10a1](https://user-images.githubusercontent.com/65942005/147322815-f2ede7c1-1bd5-4afc-b08a-9cc16b75bc04.png)
![Picture10a2](https://user-images.githubusercontent.com/65942005/147322850-2009b0ac-8304-42c9-be97-226e456260b3.png)
![Picture10b](https://user-images.githubusercontent.com/65942005/147322881-2de2214e-b558-4eeb-b450-4f193738e50d.png)
<br>
![Picture11](https://user-images.githubusercontent.com/65942005/147322904-b0000aa1-f66c-4242-8750-e291a6c4b009.png)<br>

