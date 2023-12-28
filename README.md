# Tooth Caries Segmentation

## What's this repo about:

This was a job interview task, that was the task statement
```
we are going to send you an image segmentation task,
so you can apply carries detection on the attached files,
so we got a pounding box for the caries on each tooth.
```
I was provided with exactly 6 images, 3 were teeth with no pounding boxes and 3 with pounding boxes.

<img src="https://github.com/Aml-Hassan-Abd-El-hamid/tooth-carries-segmentation/assets/66205928/2e8e6af2-4583-429c-b6d1-35e034f7ad49" width="140" height="140" >
<img src="https://github.com/Aml-Hassan-Abd-El-hamid/tooth-carries-segmentation/assets/66205928/6da4bb31-6548-4db1-b1db-12ddfe3637b0" width="140" height="140" >
<img src="https://github.com/Aml-Hassan-Abd-El-hamid/tooth-carries-segmentation/assets/66205928/51c22866-7f2f-49f0-87ce-1777fde518cc" width="140" height="140" ><br>
<img src="https://github.com/Aml-Hassan-Abd-El-hamid/tooth-carries-segmentation/assets/66205928/90c52ca3-d0f4-40be-86b8-0b14d6118555" width="140" height="140" >
<img src="https://github.com/Aml-Hassan-Abd-El-hamid/tooth-carries-segmentation/assets/66205928/59173f54-970d-46a1-9479-7fca9f4b2177" width="140" height="140" >
<img src="https://github.com/Aml-Hassan-Abd-El-hamid/tooth-carries-segmentation/assets/66205928/b26edf6a-579a-4c1e-b84b-b005158eb019" width="140" height="140" >

## How I did the task:

I first started by defining the kind of task and what kind of image segmentation task it is. I framed this task as a semantic segmentation which is a computer vision task in which the goal is to categorize each pixel in an image into a class or object. Here we have 2 classes: background and Caries.

Given the amount of data that I was provided with, the lack of time and resources to collect more data, and the lack of proper computational power, the first method that came to my mind to finish such a task was to use a strong model that's already trained and ready to go.<be>

I experimented with multiple models but the 2 models that gave the best results were the following ones:


**caries-detection-euzne from Roboflow**: Roboflow has amazing pre-trained models there, those models are trained on a variety of tasks, and there were a lot of models trained to conduct segmentation on tooth caries, I experimented with some of them and picked the best possible one, here's a [link](https://universe.roboflow.com/digital-health-bg/caries-detection-euzne) to the model's page.<be>
Of Course the model needed more training and fin-tuning to catch the caries from the images in a better way so I intend to collect more data to work with it in the future.

**SAM**: According to META, SAM is a promotable segmentation system with zero-shot generalization to unfamiliar objects and images, without the need for additional training, so of course I was tempted to try such a model on those images, but it's still didn't catch all the carries!

You can see the results of the 2 models inside this [notebook](https://github.com/Aml-Hassan-Abd-El-hamid/tooth-carries-segmentation/blob/main/tooth-caries-segmentation.ipynb).



