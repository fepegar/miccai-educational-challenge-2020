*This is my submission to the [MICCAI Educational Challenge 2020](https://miccai-sb.github.io/challenge.html).*

*You can run the notebook on [Google Colab](https://colab.research.google.com/drive/1tI35u7V1ogDTKzaraXwwZRMebBIYiqOe?usp=sharing).*

<a href="https://colab.research.google.com/github/fepegar/miccai-educational-challenge-2020/blob/master/Data_preprocessing_and_augmentation_using_TorchIO_a_tutorial.ipynb"
   target="_parent">
   <img align="left"
      src="https://colab.research.google.com/assets/colab-badge.svg">
</a>

<!-- <a href="https://nbviewer.jupyter.org/github/fepegar/miccai-educational-challenge-2020/blob/master/Data_preprocessing_and_augmentation_using_TorchIO_a_tutorial.ipynb?flush_cache=true"
   target="_parent">
   <img align="right"
      src="https://raw.githubusercontent.com/jupyter/design/master/logos/Badges/nbviewer_badge.png"
      width="109" height="20">
</a> -->

<br />

---

# Data preprocessing and augmentation using TorchIO: a tutorial

Preprocessing and augmentation are always overlooked in papers, but these are extremely important and therefore the software and parameters used should be correctly reported. Most importantly, papers will be more easily reproducible if researchers can share the tools they use for these tasks.

![One does not simply throw data into a U-Net](https://i.imgflip.com/4b1gac.jpg)

Transforms are callable Python objects that take data and modify it. In the context of deep learning for medical images, they can be used to pre- or post-process the images, or for data augmentation.

[TorchIO](https://torchio.readthedocs.io/index.html) transforms support 4D tensors (and therefore also 2D and 3D), so it can be used to process most types of medical images: X-rays, CT, 4D ultrasound, structural MRI, diffusion MRI, functional MRI, PET, SPECT, multispectral, RGB, histology...

In this tutorial, we will go through most of the transforms and show some usage examples, including a typical composition of transforms for training and testing.

Some important concepts of medical imaging are also explained, so it will be helpful for students, researchers or clinicians who are getting started in the field.
