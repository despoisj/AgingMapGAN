## AgingMapGAN (AMGAN): High-Resolution Controllable Face Aging with Spatially-Aware Conditional GANs

<div>
    <h2><a style="width: 30%;margin: 5%;" href="https://www.linkedin.com/in/juliendespois/" target="_blank">Julien Despois</a><a style="width: 30%;margin: 5%;" href="https://www.linkedin.com/in/frederic-flament-ph-d-b8aa212/" target="_blank">Frederic Flament</a><a style="width: 30%;margin: 5%;" href="https://www.linkedin.com/in/matthieu-perrot-225ab01b/" target="_blank">Matthieu Perrot</a></h2>
</div>


<p align="center">
  <img width="40%" src="img/loreal_research.png">
</p>

## Video Summary
<iframe style="display: block; margin: auto;" width="840" height="472" src="https://www.youtube.com/embed/HMZiSVKXkWo" frameborder="0" allow="encrypted-media; picture-in-picture" allowfullscreen></iframe>

## Abstract
Existing approaches and datasets for face aging produce results skewed towards the mean, with individual variations and expression wrinkles often invisible or overlooked in favor of global patterns such as the fattening of the face. Moreover, they over little to no control over the way the faces are aged and can difficultly be scaled to large images, thus preventing their usage in many real-world applications. To address these limitations, we present an approach to change the appearance of a high-resolution image using ethnicity-specific aging information and weak spatial supervision to guide the aging process. We demonstrate the advantage of our proposed method in terms of quality, control, and how it can be used on high-definition images while limiting the computational overhead.

## Model
![model](img/model_hd.jpg)

## Training
![training](img/training_hd.jpg)


## Results
We recommend viewing the videos in full-screen to see the generated HD images (1024px).
<div>
    <video style="margin: 0 auto; width: 49%" controls>
      <source src="img/cau.mov">
    Your browser does not support the video tag.
    </video>
    <video style="margin: 0 auto; width: 49%" controls>
      <source src="img/ind.mov">
    Your browser does not support the video tag.
    </video>
    <video style="margin: 0 auto; width: 49%" controls>
      <source src="img/aam.mov">
    Your browser does not support the video tag.
    </video>
    <video style="margin: 0 auto; width: 49%" controls>
      <source src="img/chi.mov">
    Your browser does not support the video tag.
    </video>
</div>

### Supervised: High-Resolution Standardized Dataset
![chi1](img/ours_chi1_cropped.jpg)
![afr1](img/ours_afr1_cropped.jpg)

### Weakly-Supervised: FFHQ
![ffhq](img/ffhq_block.jpg)

### Paper & Supplementary Materials
TBD: Waiting for ECCV 2020 Proceedings