# kohya_lora_training example

We used [Kohya LoRA Dreamboot](https://github.com/Linaqruf/kohya-trainer/blob/main/kohya-LoRA-dreambooth.ipynb) 
and [Cagliostro Colab UI]( https://github.com/Linaqruf/sd-notebook-collection/blob/main/cagliostro-colab-ui.ipynbcolabs) for the purpose of this training.

> 59 images used  to create the training set. They were renamed and saved as zip using [Birme](https://www.birme.net/?target_width=512&target_height=512&rename=x&rename_start=119)

> Kohya LoRA Dreambooth settings:

:exclamation: If section is not mentioned here, it only means we skipped it.

>    1.1 Install Dependencies. Make sure to ✅ *install_xformers and ✅ mount_drive*  in this section.

>    2.1 Download Avaialble Mode. Set modelName to *Stable-Diffusion-v1-5*.

>    2.3 Download Available VAE(Optional). Choose vaeName as *stableddiffusion_v1_5*.

>    3.1. Just run the *Locating Train Data Directory* section.

>    3.2. Unzip Dataset. Click on icon folder in Kohya LoRA (top left), select the **drive** folder. Select *Copy path* option for your zip files and the paste it into *zipfile_url*.
