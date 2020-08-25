## AgingMapGAN (AMGAN): High-Resolution Controllable Face Aging with Spatially-Aware Conditional GANs

<div>
    <h2><a style="width: 30%;margin: 5%;" href="https://www.linkedin.com/in/juliendespois/" target="_blank">Julien Despois</a><a style="width: 30%;margin: 5%;" href="https://www.linkedin.com/in/frederic-flament-ph-d-b8aa212/" target="_blank">Frederic Flament</a><a style="width: 30%;margin: 5%;" href="https://www.linkedin.com/in/matthieu-perrot-225ab01b/" target="_blank">Matthieu Perrot</a></h2>
</div>


<p align="center">
  <img width="40%" src="img/loreal_research.png">
</p>

## Video Summary
<iframe style="display: block; margin: auto;" width="840" height="472.5" src="https://www.youtube.com/embed/HMZiSVKXkWo" frameborder="0" allow="encrypted-media; picture-in-picture" allowfullscreen></iframe>

## Abstract
Existing approaches and datasets for face aging produce results skewed towards the mean, with individual variations and expression wrinkles often invisible or overlooked in favor of global patterns such as the fattening of the face. Moreover, they offer little to no control over the way the faces are aged and can difficultly be scaled to large images, thus preventing their usage in many real-world applications. To address these limitations, we present an approach to change the appearance of a high-resolution image using ethnicity-specific aging information and weak spatial supervision to guide the aging process. We demonstrate the advantage of our proposed method in terms of quality, control, and how it can be used on high-definition images while limiting the computational overhead.

### Paper & Supplementary Materials
<div align="center" style="display:flex; margin-bottom:50px; margin-top: 30px;">
    <div style="width:20%;display: inline-block;">     
        <a href="TODO" target="_blank">
            <img class="layered-paper-big" style="max-height:200px" src="img/paper_thumbnail.jpg">
        </a>
    </div>
    <div style="width:70%;display: flex; align-items: center; margin-left: 5%;">
        <div style="text-align: left;">
            <span style="font-size:12pt">J. Despois, F. Flament, M. Perrot</span><br>
            <span style="font-size:12pt">
                <b>AgingMapGAN (AMGAN): High-Resolution Controllable Face Aging with Spatially-Aware Conditional GANs.</b>
            </span>
            <br>
            <span style="font-size:12pt">ECCV, 2020 (AIM Workshop Oral)</span>
            <span style="font-size:12pt"><a href="TODO" target="_blank">[arXiv]</a>&nbsp;<a href="bibtex.txt" target="_blank">[BibTeX]</a></span>
        </div>
    </div>
</div>

## Model
Our model takes a patch *p* from input image *I*, a target aging map *A*, and two orthonogal gradient images *X* and *Y*. The image patch *I<sub>p</sub>* is then transformed according to the local aging information contained in the map *A<sub>p</sub>*, while the orthogonal gradients *X<sub>p</sub>* and *Y<sub>p</sub>* provide the coordinates of the patch in a fully-convolutional manner. The conditions are injected in the generator via the SPADE block to preserve the spatial information. Finally, the generator uses an attention mechanism to only change relevant parts of the image, thus preserving the clothes, earrings and other facial features unrelated to aging.

<p align="center">
  <img width="70%" src="img/model_hd.jpg">
</p>

## Training
To train our model, we use four different losses: *L<sub>Age</sub>* to penalize the aging map estimation, *L<sub>Loc</sub>* for the patch localization, *L<sub>WGAN</sub>* for the realism of the generated images, and *L<sub>Cyc</sub>* for the fidelity to the original image.

<p align="center">
  <img width="70%" src="img/training_hd.jpg">
</p>


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
We recommend opening the images in a new tab to see the details.
<p align="center">
  <img width="100%" src="img/ours_chi1_cropped.jpg">
</p>
<p align="center">
  <img width="100%" src="img/ours_cau1_cropped.jpg">
</p>

### Weakly-Supervised: FFHQ
We recommend opening the images in a new tab to see the details.
<p align="center">
  <img width="49%" src="img/ffhq_cau1.jpg">
  <img width="49%" src="img/ffhq_chi1.jpg">
</p>
<p align="center">
  <img width="49%" src="img/ffhq_afr1.jpg">
  <img width="49%" src="img/ffhq_cau5.jpg">
</p>
<p align="center">
  <img width="49%" src="img/ffhq_cau3.jpg">
  <img width="49%" src="img/ffhq_afr2.jpg">
</p>

### Other works
Check out our other paper presented at AIM (ECCV 2020): <a href="https://robinkips.github.io/CA-GAN/" target="_blank">https://robinkips.github.io/CA-GAN/</a>
