# GANMetalCover

Final project for GAN course from opencampus.sh https://edu.opencampus.sh/courses/212

## Installation

* Create a virtual environement

```
python -m venv GanMetalCover
```

* Install requirements.txt
```
pip install -r requirements.txt
```

* Add environement to kernel
```
python -m pip install --upgrade pip
python -m ipykernel install --user --name=GanMetalCover
```
If you have trouble setting the venv up you may also check this repo here: https://github.com/nicknochnack/TFODCourse

## Description

This repository allows you to generate your own metal album covers. We used a Wasserstein GAN for that based on the GAN course from coursera.org (https://www.coursera.org/learn/build-basic-generative-adversarial-networks-gans/home/welcome). The model has been altered to fit our needs and work on RGB images. As our kaggle.com dataset was rather large and fans of Mastodon, we chose to only train the model on the main genre "Progressive" from the dataset.

We also built a conditional GAN, that also learn the label and would eventually be able to generate an image based on the music genre with 128x128 images. Unfortunately our computational power was not big enough to have any results on this. There has been improvement after 24h of training, but not sufficient to justify longer training, especially compared to the training time, that has already been used on the 64x64. So if you are able to let that run on a more powerful machine, let us know.

## Run the model

In order to run the model please follow these steps:

* Clone the repository
* Open the notebook
* Scroll to the very bottom "Save and Load Model"
* Uncomment the paths and run the cell
* Uncomment the load model and run the cell
* Uncomment the generate fake image and run the cell

The 28x28 model has been trained for 1000 epochs, which took around 6h on an RTX2060 and the 64x64 model has been trained 5000 epochs, which took about 50h on an RTX2060.

## Train from scratch

If you feel especially fantastic and want to run the model yourself please follow these steps:

* Clone the repository
* Open the notebook
* Run all
* NOTE: The save/load part is commented out, to not overwrite the existing model

PS: You could also use the model with your own images and see what happens.


## Results

Here are some generated images from our model. Some of the 64x64 images look almost real. Though with the discolored pixel you can still easily distinguish between real and fake images. For the 28x28 the same is true, but with this small resolution it was also almost impossible to see anything on the real images. The loss development on the 64x64 model indicates, that a longer training time would probably improve the model outcome. Further results can be found in the "resources" folder.

64x64
![generatedFake](https://user-images.githubusercontent.com/9366108/145720727-059d7b9d-60ba-45b5-a3f1-a8c086fcfd00.png)
![index59](https://user-images.githubusercontent.com/9366108/145720734-0825ee9e-c62b-4640-a880-6763580c0bfd.png)

28x28
![index](https://user-images.githubusercontent.com/9366108/145720753-832305e5-800a-4ac1-a497-196e320611fb.png)
![2index](https://user-images.githubusercontent.com/9366108/145720765-214a9aff-d158-4ff9-ae6c-9711a1304083.png)
