## Probing the phonetic and phonological knowledge of tones in Mandarin TTS models 
[link to pdf](https://arxiv.org/abs/1912.10915)

### Data

Audio samples can be found here: [online demo](https://lingjzhu.github.io/TTS_and_Tone_demo/)

All synthesized stimuli can be accessed [here](https://drive.google.com/drive/folders/1AX0jqPnigC2s2CSuDbWhNwVRwcFg8dmM?usp=sharing).


### Demo
#### Online Colab demo.  
You can directly run the TTS models (Tacotron2 and WaveGlow) on Google Colab (with a powerful GPU).  
  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lingjzhu/probing-TTS-models/blob/master/TTS_colab_demo.ipynb)  
  
#### Runing locally.  
torch == 1.1.0
1. Download pre-trained Mandarin models at this [folder](https://drive.google.com/drive/folders/1Sf9t4IzMVGAgcznoTIn2mRNlcVkZuE3w?usp=sharing).
2. Download [pre-trained Chinese BERT](https://github.com/ymcui/Chinese-BERT-wwm) (`BERT-wwm-ext, Chinese`).
3. Run ``inference_bert.ipynb''   
Or:  
   Use the following command line.  
```
python synthesize.py --text ./stimuli/tone3_stimuli --use_bert --bert_folder path_to_bert_folder 
--tacotron_path path_to_pre-trained_tacotron2 --waveglow_path path_to_pre-trained_waveglow 
--out_dir path_output_dir
```

Note. The current implementation is based on the Nvidia's public implementation of Tacotron2 and Waveglow
### References
This project has benefited immensely from the following works.  
[Pre-Trained Chinese BERT with Whole Word Masking](https://github.com/ymcui/Chinese-BERT-wwm)  
[Tacotron 2 - PyTorch implementation with faster-than-realtime inference](https://github.com/NVIDIA/tacotron2)  
[WaveGlow: a Flow-based Generative Network for Speech Synthesis](https://github.com/NVIDIA/waveglow)  
[A Demo of MTTS Mandarin/Chinese Text to Speech FrontEnd](https://github.com/Jackiexiao/MTTS)  
[Open-source mandarin speech synthesis data](https://www.data-baker.com/open_source.html)  
[只用同一声调的字可以造出哪些句子？](https://www.zhihu.com/question/27733544)  
