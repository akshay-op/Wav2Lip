# **Wav2Lip**: *Accurately Lip-syncing Videos In The Wild*

For commercial requests, please contact us at radrabha.m@research.iiit.ac.in or prajwal.k@research.iiit.ac.in. We have an HD model ready that can be used commercially.

This code is part of the paper: _A Lip Sync Expert Is All You Need for Speech to Lip Generation In the Wild_ published at ACM Multimedia 2020. 

[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/a-lip-sync-expert-is-all-you-need-for-speech/lip-sync-on-lrs2)](https://paperswithcode.com/sota/lip-sync-on-lrs2?p=a-lip-sync-expert-is-all-you-need-for-speech)
[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/a-lip-sync-expert-is-all-you-need-for-speech/lip-sync-on-lrs3)](https://paperswithcode.com/sota/lip-sync-on-lrs3?p=a-lip-sync-expert-is-all-you-need-for-speech)
[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/a-lip-sync-expert-is-all-you-need-for-speech/lip-sync-on-lrw)](https://paperswithcode.com/sota/lip-sync-on-lrw?p=a-lip-sync-expert-is-all-you-need-for-speech)

|📑 Original Paper|📰 Project Page|🌀 Demo|⚡ Live Testing|📔 Colab Notebook
|:-:|:-:|:-:|:-:|:-:|
[Paper](http://arxiv.org/abs/2008.10010) | [Project Page](http://cvit.iiit.ac.in/research/projects/cvit-projects/a-lip-sync-expert-is-all-you-need-for-speech-to-lip-generation-in-the-wild/) | [Demo Video](https://youtu.be/0fXaDCZNOJc) | [Interactive Demo](https://bhaasha.iiit.ac.in/lipsync) | [Colab Notebook](https://colab.research.google.com/github/justinjohn0306/Wav2Lip/blob/master/Wav2Lip_simplified_v5.ipynb)

 <img src="https://drive.google.com/uc?export=view&id=1Wn0hPmpo4GRbCIJR8Tf20Akzdi1qjjG9"/>

----------
**Highlights**
----------
 - Weights of the visual quality disc has been updated in readme!
 - Lip-sync videos to any target speech with high accuracy :100:. Try our [interactive demo](https://bhaasha.iiit.ac.in/lipsync).
 - :sparkles: Works for any identity, voice, and language. Also works for CGI faces and synthetic voices.
 - Complete training code, inference code, and pretrained models are available :boom:
 - Or, quick-start with the Google Colab Notebook: [Link](https://colab.research.google.com/drive/1tZpDWXz49W6wDcTprANRGLo2D_EbD5J8?usp=sharing). Checkpoints and samples are available in a Google Drive [folder](https://drive.google.com/drive/folders/1I-0dNLfFOSFwrfqjNa-SXuwaURHE5K4k?usp=sharing) as well. There is also a [tutorial video](https://www.youtube.com/watch?v=Ic0TBhfuOrA) on this, courtesy of [What Make Art](https://www.youtube.com/channel/UCmGXH-jy0o2CuhqtpxbaQgA). Also, thanks to [Eyal Gruss](https://eyalgruss.com), there is a more accessible [Google Colab notebook](https://j.mp/wav2lip) with more useful features. A tutorial collab notebook is present at this [link](https://colab.research.google.com/drive/1IjFW1cLevs6Ouyu4Yht4mnR4yeuMqO7Y#scrollTo=MH1m608OymLH).  
 - :fire: :fire: Several new, reliable evaluation benchmarks and metrics [[`evaluation/` folder of this repo]](https://github.com/Rudrabha/Wav2Lip/tree/master/evaluation) released. Instructions to calculate the metrics reported in the paper are also present.

--------
**Disclaimer**
--------
All results from this open-source code or our [demo website](https://bhaasha.iiit.ac.in/lipsync) should only be used for research/academic/personal purposes only. As the models are trained on the <a href="http://www.robots.ox.ac.uk/~vgg/data/lip_reading/lrs2.html">LRS2 dataset</a>, any form of commercial use is strictly prohibhited. For commercial requests please contact us directly!

Prerequisites
-------------
- `Python 3.6` 
- ffmpeg: `sudo apt-get install ffmpeg`
- Install necessary packages using `pip install -r requirements.txt`. Alternatively, instructions for using a docker image is provided [here](https://gist.github.com/xenogenesi/e62d3d13dadbc164124c830e9c453668). Have a look at [this comment](https://github.com/Rudrabha/Wav2Lip/issues/131#issuecomment-725478562) and comment on [the gist](https://gist.github.com/xenogenesi/e62d3d13dadbc164124c830e9c453668) if you encounter any issues. 
- Face detection [pre-trained model](https://www.adrianbulat.com/downloads/python-fan/s3fd-619a316812.pth) should be downloaded to `face_detection/detection/sfd/s3fd.pth`. Alternative [link](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/prajwal_k_research_iiit_ac_in/EZsy6qWuivtDnANIG73iHjIBjMSoojcIV0NULXV-yiuiIg?e=qTasa8) if the above does not work.

Getting the weights
----------
| Model  | Description |  Link to the model | 
| :-------------: | :---------------: | :---------------: |
| Wav2Lip  | Highly accurate lip-sync | [Link](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/radrabha_m_research_iiit_ac_in/Eb3LEzbfuKlJiR600lQWRxgBIY27JZg80f7V9jtMfbNDaQ?e=TBFBVW)  |
| Wav2Lip + GAN  | Slightly inferior lip-sync, but better visual quality | [Link](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/radrabha_m_research_iiit_ac_in/EdjI7bZlgApMqsVoEUUXpLsBxqXbn5z8VTmoxp55YNDcIA?e=n9ljGW) |
| Expert Discriminator  | Weights of the expert discriminator | [Link](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/radrabha_m_research_iiit_ac_in/EQRvmiZg-HRAjvI6zqN9eTEBP74KefynCwPWVmF57l-AYA?e=ZRPHKP) |
| Visual Quality Discriminator  | Weights of the visual disc trained in a GAN setup | [Link](https://iiitaphyd-my.sharepoint.com/:u:/g/personal/radrabha_m_research_iiit_ac_in/EQVqH88dTm1HjlK11eNba5gBbn15WMS0B0EZbDBttqrqkg?e=ic0ljo) |

Lip-syncing videos using the pre-trained models (Inference)
-------
You can lip-sync any video to any audio:
```bash
python inference.py --checkpoint_path <ckpt> --face <video.mp4> --audio <an-audio-source> 
```
The result is saved (by default) in `results/result_voice.mp4`. You can specify it as an argument,  similar to several other available options. The audio source can be any file supported by `FFMPEG` containing audio data: `*.wav`, `*.mp3` or even a video file, from which the code will automatically extract the audio.

##### Tips for better results:
- Experiment with the `--pads` argument to adjust the detected face bounding box. Often leads to improved results. You might need to increase the bottom padding to include the chin region. E.g. `--pads 0 20 0 0`.
- If you see the mouth position dislocated or some weird artifacts such as two mouths, then it can be because of over-smoothing the face detections. Use the `--nosmooth` argument and give another try. 
- Experiment with the `--resize_factor` argument, to get a lower resolution video. Why? The models are trained on faces which were at a lower resolution. You might get better, visually pleasing results for 720p videos than for 1080p videos (in many cases, the latter works well too). 
- The Wav2Lip model without GAN usually needs more experimenting with the above two to get the most ideal results, and sometimes, can give you a better result as well.



