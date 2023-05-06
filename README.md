# Kohya LoRA model training example

We used [Kohya LoRA Dreambooth](https://colab.research.google.com/github/Linaqruf/kohya-trainer/blob/main/kohya-LoRA-dreambooth.ipynb) 
and [Cagliostro Colab UI](https://colab.research.google.com/github/Linaqruf/sd-notebook-collection/blob/main/cagliostro-colab-ui.ipynb) for the purpose of this training.

> 59 images were used  to create this training set. **Ideally you want to utilize a set of 100+ images for training.** 
  Click on *rename, select 512 x 512 px, and save as zip* using [Birme](https://www.birme.net/?target_width=512&target_height=512&rename=x&rename_start=119)
  
 > Please note there is 2 batches of images. Images generated with prompt 1 will give you an idea of mixing various LoRA files, adding vae etc. Prompt 1 and prompt 2 are not the same. That wil give you a lot of room to experiment.

> **Kohya LoRA Dreambooth settings to choose and run:**

>    1.1 Install Dependencies. Make sure to ✅ *install_xformers and ✅ mount_drive*  in this section

>    1.2 Skipped

>    2.1 Download Available Model. Set modelName to *Stable-Diffusion-v1-5*.

>    2.2 Skipped

>    2.3 Download Available VAE(Optional). Choose vaeName as *stableddiffusion_v1_5*.

>    3.1 Run *Locating Train Data Directory* as is.

>    3.2. Unzip Dataset. Click on icon folder in Kohya LoRA (top left), select the **drive** folder. Select *Copy path* option for your zip files and paste it into *zipfile_url*.

>    3.3 Skipped

>    4.1 Skipped

>    4.2.1 Run *Blip Captioning* section as is.The content will appear in **train_data** folder.

>    4.2.2 and 4.2.3 Skipped

>    5.1  Model Config. Name your *project_name*. Select *Copy path* option for your Stable-Diffusion-v1-5.safetensors (under pretrained_model folder) and paste it into *vae*. And ✅ *output_to_drive*.

>    5.2  Dataset Config. Name your *class_token*. Select *Copy path* option for your train_data and paste it into *train_data*.

>    5.3  LoRA config. Set *conv_dim* to 8, *conv_alpha* to 1, *network_dim* to 16, and *network_aplha* to 1. Then proceed with changing *unet_lr* to 5e-4, *text_encoder_lr* to 1e-4, *lr_scheduler* to cosine_with_restarts, and *lg_warmup_steps* to 0.05.  **This will give us a learning rate of approximately 950 steps.**

>    5.4 Training Config. Only change *train_batch_size* to 2 and let it run.

>    :watch: Run the 5.5 Start Training section. It might take 40 minutes.Your files should be save in your Google Drive in your LoRA folder. Let`s now get to the next step.

> Skipped 5.5 and the whole VI section.

> **Cagliostro Colab UI settings to choose and run:**
Download your LoRA files and upload to stable-diffusion-webui -> model -> LoRA files. Settings are described in CCUI1.png and CCUI2.png files. The rest of the code must be run unchanged. Click on one of the 3 links in Start Cagliostro Colab section to get to the UI page.

> In UI, find Lora panel to make sure your files are saved.Here you can test your models one by one.Once clicked, it appears there. Add a short prompt.

> Example:point_right:  \<lora:Sample-000001:1> RAW photo of the GIRL,(high detailed:1.2), 8K UHD, DSLR,soft lightning,high quality, film grain, Fujifilm XT3, masterpiece, best quality.

> Add a negative prompt as well. Example:point_right: (worst quality, low quality, deformed iris, deformed pupils, semi-realistic, cgi, 3d, render,sketch,cartoon,drawing, anime: 1:4), text, close up, cropped, out of frame, worst quality, low quality, jpeg artifacts, ugly, duplicate, morbid, mutilated, extra fingers, mutated hands, poorly drawn hands, poorly drawn face, mutation, deformed, blurry, dehydrated, bad anatomy, bad proportions, extra limbs, cloned face, disfigured, malformed limbs, missing arms, extra arms, extra legs, fused fingers, too many fingers, long neck.

> Sampling methois set to DPM++ SDE, sampling steps set to 25, Width/Height :768, Batch count/batch size: 1, CFG Scale: 6, Denoising strength: 0.11, seed: -1.

> In control Model, nothing is changed besides ✅Enable, and setting Preprocessor: hed, Model: control_sd15_hed[fef5e48e].

> Now, Control Model-1 was also set to ✅Enable, Preprocessor:canny, Model: control_sd15_canny[fef5e48e].

> At this point we are ready to click the Generate button and enjoy the results!















  


