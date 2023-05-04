# Kohya LoRA model training example

We used [Kohya LoRA Dreamboot](https://colab.research.google.com/github/Linaqruf/kohya-trainer/blob/main/kohya-LoRA-dreambooth.ipynb) 
and [Cagliostro Colab UI](https://colab.research.google.com/github/Linaqruf/sd-notebook-collection/blob/main/cagliostro-colab-ui.ipynb) for the purpose of this training.

> 59 images were used  to create this training set. **Ideally you want to utilize a set of 100+ images for training.** 
  Click on *rename, select 512 x 512 px, and save as zip* using [Birme](https://www.birme.net/?target_width=512&target_height=512&rename=x&rename_start=119)

> Kohya LoRA Dreambooth settings to choose and run:

:exclamation: If section is not mentioned here, it only means we skipped it.

>    1.1 Install Dependencies. Make sure to ✅ *install_xformers and ✅ mount_drive*  in this section.

>    2.1 Download Avaialble Mode. Set modelName to *Stable-Diffusion-v1-5*.

>    2.3 Download Available VAE(Optional). Choose vaeName as *stableddiffusion_v1_5*.

>    3.1. Just run the *Locating Train Data Directory* section.

>    3.2. Unzip Dataset. Click on icon folder in Kohya LoRA (top left), select the **drive** folder. Select *Copy path* option for your zip files and paste it into *zipfile_url*.

>    4.2.1 Run the *Blip Captioning* section without any changes.The content will appear in **train_data** folder.

>    5.1. Model Config. Name your *project_name*. Select *Copy path* option for your Stable-Diffusion-v1-5.safetensors (under pretrained_model folder) and paste it into *vae*. And ✅ *output_to_drive*.

>    5.2  Dataset Config. Name your *class_token*. Select *Copy path* option for your train_data and paste it into *train_data*.

>    5.3  LoRA config. Set *conv_dim* to 8, *conv_alpha* to 1, *network_dim* to 16, and *network_aplha* to 1. Then proceed with changing *unet_lr* to 5e-4, *text_encoder_lr* to 1e-4, *lr_scheduler* to cosine_with_restarts, and *lg_warmup_steps* to 0.05.  **This will give us a learning rate of approximately 950 steps.**

>    5.4 Training Config. Only change *train_batch_size* to 2 and let it run.

>    :watch: Run the 5.5 Start Training section. It might take 40 minutes.



