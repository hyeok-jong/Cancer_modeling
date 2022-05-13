# Cancer Modeling  
Classification model for skin cancer   

Dataset is from [ISIC 2019](https://challenge.isic-archive.com/landing/2019/)   
And for prerequisite see [HERE](https://velog.io/@jj770206/ISIC-dataset)  

# 1. Data Preprocessing  
Note that, first of all, for training we need to convert image to numpy or torch.Tensor.   

See `preprocessing.ipynb`.  
To save time, I saved the images into numpy in advance.  
So in `dataloader.py` there is no `cv2.imread` or `Image.open` instead, I used `np.load`.  

Doing so is more effective the more you experiment and large dataset or huge epochs.    

And because I was going to use image with 224 size, I saved numpy as 224.

I did an experiments to measure time for transformation.  

Conclusion is doing image augmentation with Tensor is slower than numpy.  
So, I didn't used torch.transformation instead customed that.  

After running `preprocessing.ipynb` one can get labeled image numpy.


# 2. Model  

![feature_extract](https://user-images.githubusercontent.com/78862026/168215494-d3adf281-4004-49f8-aa19-5b89d5a30267.png)

# 3. Test  
[Pre-trainined](https://drive.google.com/file/d/1I1CV3I-Jg6Nfi4K6yKwrU3L6wCysBr4f/view?usp=sharing)


