# ACA-Net

Additional requirement:
  speechbrain==0.5.11

## Training config
- Feature: 80-dim fbank, mean normalization, speed perturb
- Training: lr [0.0001, 0.1], batch_size 256, 4 gpu(Tesla V100), additive angular margin
- Metrics: EER(%), MinDCF

## Voxceleb Results
- Train set: Voxceleb2-dev, 5994 speakers
- Test set: Voxceleb-O

| Model | Params | EER(%) | MinDCF |
|:-----:|:------:|:------:|:------:|
| ACANet |   |  |  |

<!-- ## pretrained model
Pretrained models are accessible on [ModelScope](). -->

<!-- - Voxceleb: [speech_campplus_sv_en_voxceleb_16k](https://modelscope.cn/models/damo/speech_campplus_sv_en_voxceleb_16k/summary) -->
<!-- - 200k labeled speakers: [speech_campplus_sv_zh-cn_16k-common](https://www.modelscope.cn/models/damo/speech_campplus_sv_zh-cn_16k-common/summary) -->

<!-- Here is a simple example for directly extracting embeddings. It downloads the pretrained model from [ModelScope](https://www.modelscope.cn/models) and extracts embeddings.
``` sh
# Install modelscope
pip install modelscope
# CAM++ trained on VoxCeleb
model_id=damo/speech_campplus_sv_en_voxceleb_16k
# CAM++ trained on 200k labeled speakers
model_id=damo/speech_campplus_sv_zh-cn_16k-common
# Run inference
python speakerlab/bin/infer_sv.py --model_id $model_id --wavs $wav_path
``` -->

## Citations
If you are using ACA-Net model in your research, please cite: 
```bibtex
@inproceedings{yip23_interspeech,
  author={Jia Qi Yip and Duc-Tuan Truong and Dianwen Ng and Chong Zhang and Yukun Ma and Trung Hieu Nguyen and Chongjia Ni and Shengkui Zhao and Eng Siong Chng and Bin Ma},
  title={{ACA-Net: Towards Lightweight Speaker Verification using Asymmetric Cross Attention}},
  year=2023,
  booktitle={Proc. INTERSPEECH 2023},
  pages={1938--1942},
  doi={10.21437/Interspeech.2023-1725}
}
```
