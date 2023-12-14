# Image-to-image translation for large images

This code adds the automatic mosaicking and de-mosaicking steps to the conventional U-net and Pix2pix networks.  
The [U-net](https://arxiv.org/abs/1505.04597) largerly builds upon the [fastai1 pytroch library](https://fastai1.fast.ai/vision.data.html).  
The [pix2pix](https://arxiv.org/abs/1611.07004) implementation borrows from [tensorflow library](https://www.tensorflow.org/tutorials/generative/pix2pix).  
  
Implimented for the article: ['Optical tomography in a single camera frame using fringe-encoded deep-learning full-field OCT'](https://opg.optica.org/boe/fulltext.cfm?uri=boe-15-1-222&id=544484).  
The U-net weights trained on full-field optical coherence tomography images (google drive link): [U-net](https://drive.google.com/drive/folders/1KjkT6XgEwGce16uyky5umfMB9ajSaoTt?usp=drive_link)  
The pix2pix weights trained on full-field optical coherence tomography images (google drive link): [pix2pix](https://drive.google.com/drive/folders/1LdHZj7OzdrGsDW-ciQ3G15gXaQiPKrHd?usp=drive_link)  

## Features:  
- Forms large dataset from a few large images (e.g. each 2560 x 2560 pixels microscopy image is augmented into 100 unique training sub-images of 256 x 256 pixels)  
- Automatic full image inference  

## Installation and Running
1. Create conda environment from the provided environment files: CondaEnvironment_Unet.yml' (for U-net) or CondaEnvironment_Pix2pix.yml (for Pix2pix).

  conda env create -f CondaEnvironment_Unet.yml

2. Activate environment and launch jupyter notebook

  conda activate CondaEnvironment_Unet  
  jupyter notebook
  
3. Load notebok 'Unet notebook model.ipynb' or 'Pix2pix notebook model.ipynb'
  
4. Specify two folders (IN folder and OUT folder) for input -> output conversion. Images should be .jpg or .png and have matching names in IN and OUT folder.

5. Proceed with the training and inference

## Citing this work

Viacheslav Mazlin, "Optical tomography in a single camera frame using fringe-encoded deep-learning full-field OCT," Biomed. Opt. Express 15, 222-236 (2024)
https://doi.org/10.1364/BOE.506664

## License

MIT licence for mosaicking and de-mosaicking codes.  
Third party software (e.g. pytorch, tensorflow, other libraries) may have different licences.  
The training weights are available under the terms of the Creative Commons Attribution 4.0 International (CC BY 4.0) license.
