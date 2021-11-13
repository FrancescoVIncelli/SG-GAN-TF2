# SG-GAN-TF2
Semantic Segmentation on real-world urban images for autonomouse driving task using Generative Adversarial Networks.

### Dataset
The images used to train the models are extracted form [The Cityscapes Dataset](https://www.cityscapes-dataset.com/), a large-scale dataset that contains a diverse set of stereo video sequences recorded in street scenes.  
The whole dataset contains images sequences acquired in urban scenarios from 50 different cities, with high quality pixel-level annotations of 5 000 frames in addition to a larger set of 20 000 weakly annotated frames.

### Installation Procedure
Install dependences running the command:
```
pip3 install -r requirements_VP_project.txt
```

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
Additional training arguments allows to set the number of epochs, the input batch size, the shape of input images, enabling augmentation, set hyperparameters for the neural network models (more info by running the script [main.py](main.py) passing the argument `--help`:
```
python3 main.py --help
```
- **Testing**  
Run the script [main.py](main.py) with the argument `phase = "test"` and keeping the same values of models hyperparameters set for the train phase:
```
python3 main.py --phase "test"
```
### Limitations and Future works
The data augmentation algorithms increses the computational demand for the training process, requiring a graphic unit equipped with a huge memory space.  
Reducing the size of the source image reduces the resources required for its training but limits the effectiveness achieved.  
  
Potential for improvement given better conditions in the data source and computational resources, such as more classes predicted and more detail in the generated image.

