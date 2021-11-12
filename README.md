# SG-GAN-TF2
Semantic Segmentation on real-world urban images for autonomouse driving task using Generative Adversarial Network model architectures.

### Dataset
The images used to train the models are extracted form [The Cityscapes Dataset](https://www.cityscapes-dataset.com/), a large-scale dataset that contains a diverse set of stereo video sequences recorded in street scenes.  
The whole dataset contains images sequences acquired in urban scenarios from 50 different cities, with high quality pixel-level annotations of 5 000 frames in addition to a larger set of 20 000 weakly annotated frames.

### Installation Procedure
Install dependences running the command:
```
pip3 install -r requirements_VP_project.txt
```

### File Structure

### Documentation
The project shows the improvements in semantic segmentation on a dataset of real-world urban images for autonomouse driving task, using recent Generative Adversarial Network model architectures (such as Grad-GAN and Pix2Pix) which can produce better results against the traditional fully-connected and convolutional discriminative models.  

Methodology: Dataset adopted and architecture of the network with related loss functions	
Implementation: Changes made throughout the development process, partial results during training and contingency decisions
Experiments and Results: Plots and predictions obtained during parameters tuning

### Execution of the code
- **Data sampling**  
Run the script [prepare_data.py](prepare_data.py) to sample labeled images and segmentation data from the whole dataset into two distinct directories *trainA* and *trainA_seg*.
- **Training**  
Run the script [main.py](main.py) with the argument `phase = "train"`:
```
python3 main.py --phase "train"
```
Additional training arguments allows to set the number of epochs, the input batch size, the shape of input images, enabling augmentation, set hyperparameters for the neural network models (more info by running the script [main.py](main.py) passing the argument `--help`: `python3 main.py --help`

### Limitations
