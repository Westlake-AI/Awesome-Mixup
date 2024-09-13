# Awesome-Mixup


<p align="center">
<img src="https://github.com/user-attachments/assets/b13d34e3-55e8-4bfa-b592-86922563d372" width=90% height=90% 
class="center">
</p>

 [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) ![GitHub stars](https://img.shields.io/github/stars/Westlake-AI/Awesome-Mixup?color=green) ![GitHub forks](https://img.shields.io/github/forks/Westlake-AI/Awesome-Mixup?color=yellow&label=Fork)
 <!-- ![visitors](https://visitor-badge.glitch.me/badge?page_id=Westlake-AI/Awesome-Mixup) -->

Welcome to Awesome-Mixup, a carefully curated survey of **Mixup** algorithms implemented in the PyTorch library, aiming to meet various needs of the research community. **Mixup** is a kind of methods that focus on alleviating model overfitting and poor generalization. As a *"data-centric"* way, Mixup can be applied to various training paradigms and data modalities.

If this repository has been helpful to you, please consider giving it a ⭐️ to show your support. Your support helps us reach more researchers and contributes to the growth of this resource. Thank you! 

## Introduction

**We summarize awesome mixup data augmentation methods for visual representation learning in various scenarios from 2018 to 2024.**

The list of awesome mixup augmentation methods is summarized in chronological order and is on updating. The main branch is modified according to [Awesome-Mixup](https://github.com/Westlake-AI/openmixup/docs/en/awesome_mixups) in [OpenMixup](https://github.com/Westlake-AI/openmixup) and [Awesome-Mix](https://github.com/ChengtaiCao/Awesome-Mix), and we are working on a comperhensive survey on mixup augmentations. You can read our survey: [**A Survey on Mixup Augmentations and Beyond**](https://arxiv.org/abs/2409.05202) see more detailed information.

* To find related papers and their relationships, check out [Connected Papers](https://www.connectedpapers.com/), which visualizes the academic field in a graph representation.
* To export BibTeX citations of papers, check out [ArXiv](https://arxiv.org/) or [Semantic Scholar](https://www.semanticscholar.org/) of the paper for professional reference formats.

<p align="center">
<img src="https://github.com/user-attachments/assets/32dd37e1-0b49-4ddb-a253-fc176a241253" width=90% height=90% 
class="center">
</p>

## Figuer of Contents

You can see the figuer of mixup augmentation methods deirtly that we summarized.

<p align="center">
<img src="https://github.com/user-attachments/assets/366a6def-9193-4c8b-ac3f-b220e3102f4e" width=90% height=90% 
class="center">
</p>

## Table of Contents

- [Awesome-Mixup](#awesome-mixup)
  - [Introduction](#introduction)
  - [Table of Contents](#table-of-contents)
  - [Sample Mixup Policies in SL](#sample-mixup-policies-in-sl)
      - [**Static Linear**](#static-linear)
      - [**Feature-based**](#feature-based)
      - [**Cutting-based**](#cutting-based)
      - [**K Samples Mixup**](#k-samples-mixup)
      - [**Random Policies**](#random-policies)
      - [**Style-based**](#style-based)
      - [**Saliency-based**](#saliency-based)
      - [**Attention-based**](#attention-based)
      - [**Generating Samples**](#generating-samples)
  - [Label Mixup Policies in SL](#label-mixup-policies-in-sl)
      - [**Optimizing Calibration**](#optimizing-calibration)
      - [**Area-based**](#area-based)
      - [**Loss Object**](#loss-object)
      - [**Random Label Policies**](#random-label-policies)
      - [**Optimizing Mixing Ratio**](#optimizing-mixing-ratio)
      - [**Generating Label**](#generating-label)
      - [**Attention Score**](#attention-score)
      - [**Saliency Token**](#saliency-token)
  - [Self-Supervised Learning](#self-supervised-learning)
      - [**Contrastive Learning**](#contrastive-learning)
      - [**Masked Image Modeling**](#masked-image-modeling)
  - [Semi-Supervised Learning](#semi-supervised-learning)
  - [CV Downstream Tasks](#cv-downstream-tasks)
      - [**Regression**](#regression)
      - [**Long tail distribution**](#long-tail-distribution)
      - [**Segmentation**](#segmentation)
      - [**Object Detection**](#object-detection)
  - [Training Paradigms](#training-paradigms)
      - [**Federated Learning**](#federated-learning)
      - [**Adversarial Attack and Adversarial Training**](#adversarial-attack-and-adversarial-training)
      - [**Domain Adaption**](#domain-adaption)
      - [**Knowledge Distillation**](#knowledge-distillation)
      - [**Multi-Modal**](#multi-modal)
  - [Beyond Vision](#beyond-vision)
      - [**NLP**](#nlp)
      - [**GNN**](#gnn)
      - [**3D Point**](#3d-point)
      - [**Other**](#other)
  - [Analysis and Theorem](#analysis-and-theorem)
  - [Survey](#survey)
  - [Benchmark](#benchmark)
  - [Classification Results on Datasets](#classification-results-on-datasets)
  - [Related Datasets Link](#related-datasets-link)
  - [Contribution](#contribution)
  - [License](#license)
  - [Acknowledgement](#acknowledgement)
  - [Related Project](#related-project)

### Sample Mixup Policies in SL

<p align="center">
<img src="https://github.com/user-attachments/assets/16482af9-90c2-4413-87e5-e0df70a7a0cc" width=100% height=100% 
class="center">
</p>

#### **Static Linear**

* **mixup: Beyond Empirical Risk Minimization**<br>
*Hongyi Zhang, Moustapha Cisse, Yann N. Dauphin, David Lopez-Paz*<br>
ICLR'2018 [[Paper](https://arxiv.org/abs/1710.09412)]
[[Code](https://github.com/facebookresearch/mixup-cifar10)]
   <details close>
   <summary>MixUp Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204561478-80b77110-21a4-480f-b369-d2f0656b5382.png" /></p>
   </details>

* **Between-class Learning for Image Classification**<br>
*Yuji Tokozume, Yoshitaka Ushiku, Tatsuya Harada*<br>
CVPR'2018 [[Paper](https://arxiv.org/abs/1711.10284)]
[[Code](https://github.com/mil-tokyo/bc_learning_image)]
   <details close>
   <summary>BC Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204563476-15e638ad-6c25-4ab6-9bb6-4c5be74c625f.png" /></p>
   </details>

* **Preventing Manifold Intrusion with Locality: Local Mixup**<br>
*Raphael Baena, Lucas Drumetz, Vincent Gripon*<br>
EUSIPCO'2022 [[Paper](https://arxiv.org/abs/2201.04368)]
   <details close>
   <summary>LocalMixup Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/ce8cd7a2-486c-4f6d-98d3-358c1ba42285" /></p>
   </details>

* **AugMix: A Simple Data Processing Method to Improve Robustness and Uncertainty**<br>
*Dan Hendrycks, Norman Mu, Ekin D. Cubuk, Barret Zoph, Justin Gilmer, Balaji Lakshminarayanan*<br>
ICLR'2020 [[Paper](https://arxiv.org/abs/1912.02781)]
[[Code](https://github.com/google-research/augmix)]
   <details close>
   <summary>AugMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204567137-f71b0437-9267-4f99-b7dc-911ffa4f8b73.png" /></p>
   </details>

* **DJMix: Unsupervised Task-agnostic Augmentation for Improving Robustness**<br>
*Ryuichiro Hataya, Hideki Nakayama*<br>
arXiv'2021 [[Paper](https://openreview.net/pdf?id=0n3BaVlNsHI)]
   <details close>
   <summary>DJMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204567516-3d058e8c-4232-4af4-b7a8-efa3a1298a1b.png" /></p>
   </details>

* **PixMix: Dreamlike Pictures Comprehensively Improve Safety Measures**<br>
*Dan Hendrycks, Andy Zou, Mantas Mazeika, Leonard Tang, Bo Li, Dawn Song, Jacob Steinhardt*<br>
CVPR'2022 [[Paper](https://arxiv.org/abs/2112.05135)]
[[Code](https://github.com/andyzoujm/pixmix)]
   <details close>
   <summary>PixMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204567828-b434c118-0be1-475d-a0f3-9834e39b4507.png" /></p>
   </details>

* **IPMix: Label-Preserving Data Augmentation Method for Training Robust Classifiers**<br>
*Zhenglin Huang, Xiaoan Bao, Na Zhang, Qingqi Zhang, Xiaomei Tu, Biao Wu, Xi Yang*<br>
NIPS'2023 [[Paper](https://arxiv.org/abs/2310.04780)]
[[Code](https://github.com/hzlsaber/IPMix)]
   <details close>
   <summary>IPMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/55c1ce2d-5372-4821-a123-74723df7fc8d" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>
 
#### **Feature-based**

* **Manifold Mixup: Better Representations by Interpolating Hidden States**<br>
*Vikas Verma, Alex Lamb, Christopher Beckham, Amir Najafi, Ioannis Mitliagkas, David Lopez-Paz, Yoshua Bengio*<br>
ICML'2019 [[Paper](https://arxiv.org/abs/1806.05236)]
[[Code](https://github.com/vikasverma1077/manifold_mixup)]
   <details close>
   <summary>ManifoldMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204565193-c5416185-ed98-4b86-bc7c-f5b6cc2f839b.png" /></p>
   </details>

* **PatchUp: A Regularization Technique for Convolutional Neural Networks**<br>
*Mojtaba Faramarzi, Mohammad Amini, Akilesh Badrinaaraayanan, Vikas Verma, Sarath Chandar*<br>
arXiv'2020 [[Paper](https://arxiv.org/abs/2006.07794)]
[[Code](https://github.com/chandar-lab/PatchUp)]
   <details close>
   <summary>PatchUp Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204566319-f2c67e8a-c10b-4ede-a57f-8c6ddf85e013.png" /></p>
   </details>

* **On Feature Normalization and Data Augmentation**<br>
*Boyi Li, Felix Wu, Ser-Nam Lim, Serge Belongie, Kilian Q. Weinberger*<br>
CVPR'2021 [[Paper](https://arxiv.org/abs/2002.11102)]
[[Code](https://github.com/Boyiliee/MoEx)]
   <details close>
   <summary>MoEx Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204569196-3641255a-56f3-407a-986a-209b5c7eeff6.png" /></p>
   </details>

* **Catch-Up Mix: Catch-Up Class for Struggling Filters in CNN**<br>
*Minsoo Kang, Minkoo Kang, Suhyun Kim*<br>
AAAI'2024 [[Paper](https://arxiv.org/abs/2401.13193)]
   <details close>
   <summary>Catch-Up-Mix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/Westlake-AI/Awesome-Mixup/assets/44519745/459a5d2b-cc74-4bd0-8cd2-46313652a9b8" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

#### **Cutting-based**

* **CutMix: Regularization Strategy to Train Strong Classifiers with Localizable Features**<br>
*Sangdoo Yun, Dongyoon Han, Seong Joon Oh, Sanghyuk Chun, Junsuk Choe, Youngjoon Yoo*<br>
ICCV'2019 [[Paper](https://arxiv.org/abs/1905.04899)]
[[Code](https://github.com/clovaai/CutMix-PyTorch)]
   <details close>
   <summary>CutMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204564166-49707535-43f9-4d15-af89-d1a5a302db24.png" /></p>
   </details>

* **Improved Mixed-Example Data Augmentation**<br>
*Cecilia Summers, Michael J. Dinneen*<br>
WACV'2019 [[Paper](https://arxiv.org/abs/1805.11272)]
[[Code](https://github.com/ceciliaresearch/MixedExample)]
   <details close>
   <summary>MixedExamples Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/232355479-8a53714f-5a6f-4c8e-b808-cc73f6d0f669.png" /></p>
   </details>

* **Patch-level Neighborhood Interpolation: A General and Effective Graph-based Regularization Strategy**<br>
*Ke Sun, Bing Yu, Zhouchen Lin, Zhanxing Zhu*<br>
arXiv'2019 [[Paper](https://arxiv.org/abs/1911.09307)]
   <details close>
   <summary>Pani VAT Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204572993-8b3fa627-8c36-4763-a2a6-c9a90c5f0fc2.png" /></p>
   </details>

* **FMix: Enhancing Mixed Sample Data Augmentation**<br>
*Ethan Harris, Antonia Marcu, Matthew Painter, Mahesan Niranjan, Adam Prügel-Bennett, Jonathon Hare*<br>
arXiv'2020 [[Paper](https://arxiv.org/abs/2002.12047)]
[[Code](https://github.com/ecs-vlc/FMix)]
   <details close>
   <summary>FMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204564909-8d20a405-141d-4fe6-ae72-581fc24222f8.png" /></p>
   </details>

* **SmoothMix: a Simple Yet Effective Data Augmentation to Train Robust Classifiers**<br>
*Jin-Ha Lee, Muhammad Zaigham Zaheer, Marcella Astrid, Seung-Ik Lee*<br>
CVPRW'2020 [[Paper](https://openaccess.thecvf.com/content_CVPRW_2020/html/w45/Lee_SmoothMix_A_Simple_Yet_Effective_Data_Augmentation_to_Train_Robust_CVPRW_2020_paper.html)]
[[Code](https://github.com/Westlake-AI/openmixup)]
   <details close>
   <summary>SmoothMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204565814-fd528402-2a57-482b-b608-1ee3096984b0.png" /></p>
   </details>

* **GridMix: Strong regularization through local context mapping**<br>
*Kyungjune Baek, Duhyeon Bang, Hyunjung Shim*<br>
Pattern Recognition'2021 [[Paper](https://www.sciencedirect.com/science/article/pii/S0031320320303976)]
[[Code](https://github.com/IlyaDobrynin/GridMixup)]
   <details close>
   <summary>GridMixup Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204566566-b345e409-da4a-4f3b-b1bd-43e7c767d26a.png" /></p>
   </details>

* **ResizeMix: Mixing Data with Preserved Object Information and True Labels**<br>
*Jie Qin, Jiemin Fang, Qian Zhang, Wenyu Liu, Xingang Wang, Xinggang Wang*<br>
arXiv'2020 [[Paper](https://arxiv.org/abs/2012.11101)]
[[Code](https://github.com/Westlake-AI/openmixup)]
   <details close>
   <summary>ResizeMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204566840-69782b04-4645-41b3-a6eb-428977c63881.png" /></p>
   </details>

* **StackMix: A complementary Mix algorithm**<br>
*John Chen, Samarth Sinha, Anastasios Kyrillidis*<br>
UAI'2022 [[Paper](https://arxiv.org/abs/2011.12618)]
   <details close>
   <summary>StackMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204574552-fb5e9865-86b0-4d51-977c-82a840d81a18.png" /></p>
   </details>

* **SuperpixelGridCut, SuperpixelGridMean and SuperpixelGridMix Data Augmentation**<br>
*Karim Hammoudi, Adnane Cabani, Bouthaina Slika, Halim Benhabiles, Fadi Dornaika, Mahmoud Melkemi*<br>
arXiv'2022 [[Paper](https://arxiv.org/abs/2204.08458)]
[[Code](https://github.com/hammoudiproject/SuperpixelGridMasks)]
   <details close>
   <summary>SuperpixelGridCut Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204570617-090cc5a7-508c-49e7-9e5f-df7ec018f540.png" /></p>
   </details>

* **A Unified Analysis of Mixed Sample Data Augmentation: A Loss Function Perspective**<br>
*Chanwoo Park, Sangdoo Yun, Sanghyuk Chun*<br>
NIPS'2022 [[Paper](https://arxiv.org/abs/2208.09913)]
[[Code](https://github.com/naver-ai/hmix-gmix)]
   <details close>
   <summary>MSDA Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204571363-f0b1a960-54f9-4462-855d-59e90f284cfe.png" /></p>
   </details>

* **You Only Cut Once: Boosting Data Augmentation with a Single Cut**<br>
*Junlin Han, Pengfei Fang, Weihao Li, Jie Hong, Mohammad Ali Armin, Ian Reid, Lars Petersson, Hongdong Li*<br>
ICML'2022 [[Paper](https://arxiv.org/abs/2201.12078)]
[[Code](https://github.com/JunlinHan/YOCO)]
   <details close>
   <summary>YOCO Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/c7040d23-6dd5-4634-9022-d26529810307" /></p>
   </details>

* **StarLKNet: Star Mixup with Large Kernel Networks for Palm Vein Identification**<br>
*Xin Jin, Hongyu Zhu, Mounîm A.El Yacoubi, Hongchao Liao, Huafeng Qin, Yun Jiang*<br>
arXiv'2024 [[Paper](https://arxiv.org/abs/2405.12721)]
   <details close>
   <summary>StarMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/44dbc86b-f7cd-4836-a93e-835f78d21ec8" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

#### **K Samples Mixup**

* **You Only Look Once: Unified, Real-Time Object Detection**<br>
*Joseph Redmon, Santosh Divvala, Ross Girshick, Ali Farhadi*<br>
CVPR'2016 [[Paper](https://arxiv.org/abs/1506.02640)]
[[Code](https://pjreddie.com/darknet/yolo/#google_vignette)]
   <details close>
   <summary>Mosaic</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/11824bd1-befc-4edd-8d0d-d8199b123e4b" /></p>
   </details>

* **Data Augmentation using Random Image Cropping and Patching for Deep CNNs**<br>
*Ryo Takahashi, Takashi Matsubara, Kuniaki Uehara*<br>
IEEE TCSVT'2020 [[Paper](https://arxiv.org/abs/1811.09030)]
   <details close>
   <summary>RICAP</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/d8fae235-ae35-4fbe-9454-6a8f3b8fce12" /></p>
   </details>

* **k-Mixup Regularization for Deep Learning via Optimal Transport**<br>
*Kristjan Greenewald, Anming Gu, Mikhail Yurochkin, Justin Solomon, Edward Chien*<br>
arXiv'2021 [[Paper](https://arxiv.org/abs/2106.02933)]
   <details close>
   <summary>k-Mixup Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204569488-d4862400-3304-488d-ad24-06eff4e0c0b2.png" /></p>
   </details>

* **Observations on K-image Expansion of Image-Mixing Augmentation for Classification**<br>
*Joonhyun Jeong, Sungmin Cha, Youngjoon Yoo, Sangdoo Yun, Taesup Moon, Jongwon Choi*<br>
IEEE Access'2021 [[Paper](https://arxiv.org/abs/2110.04248)]
[[Code](https://github.com/yjyoo3312/DCutMix-PyTorch)]
   <details close>
   <summary>DCutMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/230492924-e9008de1-913f-44f5-ac2e-3d21f07d1b7f.png" /></p>
   </details>

* **MixMo: Mixing Multiple Inputs for Multiple Outputs via Deep Subnetworks**<br>
*Alexandre Rame, Remy Sun, Matthieu Cord*<br>
ICCV'2021 [[Paper](https://arxiv.org/abs/2103.06132)]
   <details close>
   <summary>MixMo Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/37af64e6-ab18-49fe-84a6-5a5104a3f81a" /></p>
   </details>

* **Cut-Thumbnail: A Novel Data Augmentation for Convolutional Neural Network**<br>
*Tianshu Xie, Xuan Cheng, Minghui Liu, Jiali Deng, Xiaomin Wang, Ming Liu*<br>
ACM MM;2021 [[Paper](https://arxiv.org/abs/2103.05342)]
   <details close>
   <summary>Cut-Thumbnail</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/450da799-0fdd-47e7-bcc4-5fcc5f186462" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

#### **Random Policies**

* **RandomMix: A mixed sample data augmentation method with multiple mixed modes**<br>
*Xiaoliang Liu, Furao Shen, Jian Zhao, Changhai Nie*<br>
arXiv'2022 [[Paper](https://arxiv.org/abs/2205.08728)]
   <details close>
   <summary>RandomMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204570320-2785207c-aced-4d94-a33e-98acfcbbaa3f.png" /></p>
   </details>

* **AugRmixAT: A Data Processing and Training Method for Improving Multiple Robustness and Generalization Performance**<br>
*Xiaoliang Liu, Furao Shen, Jian Zhao, Changhai Nie*<br>
ICME'2022 [[Paper](https://arxiv.org/abs/2207.10290)]
   <details close>
   <summary>AugRmixAT Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204571167-748828be-a1f6-46ac-bc13-37cccfa72515.png" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

#### **Style-based**

* **StyleMix: Separating Content and Style for Enhanced Data Augmentation**<br>
*Minui Hong, Jinwoo Choi, Gunhee Kim*<br>
CVPR'2021 [[Paper](https://openaccess.thecvf.com/content/CVPR2021/papers/Hong_StyleMix_Separating_Content_and_Style_for_Enhanced_Data_Augmentation_CVPR_2021_paper.pdf)]
[[Code](https://github.com/alsdml/StyleMix)]
   <details close>
   <summary>StyleMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204567999-6d0263c2-111c-4335-92b5-66486bb0fea0.png" /></p>
   </details>

* **Domain Generalization with MixStyle**<br>
*Kaiyang Zhou, Yongxin Yang, Yu Qiao, Tao Xiang*<br>
ICLR'2021 [[Paper](https://openreview.net/forum?id=6xHJ37MVxxp)]
[[Code](https://github.com/KaiyangZhou/mixstyle-release)]
   <details close>
   <summary>MixStyle Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204568994-eb45528e-e83b-4ac5-bed9-642da987ec89.png" /></p>
   </details>

* **AlignMix: Improving representation by interpolating aligned features**<br>
*Shashanka Venkataramanan, Ewa Kijak, Laurent Amsaleg, Yannis Avrithis*<br>
CVPR'2022 [[Paper](https://arxiv.org/abs/2103.15375)]
[[Code](https://github.com/shashankvkt/AlignMixup_CVPR22)]
   <details close>
   <summary>AlignMixup Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204574666-fcb694b0-c6bf-438a-bbd0-020635fe4b51.png" /></p>
   </details>

<!-- * **Teach me how to Interpolate a Myriad of Embeddings**<br> -->
* **Embedding Space Interpolation Beyond Mini-Batch, Beyond Pairs and Beyond Examples**<br>
*Shashanka Venkataramanan, Ewa Kijak, Laurent Amsaleg, Yannis Avrithis*<br>
NIPS'2023 [[Paper](https://arxiv.org/abs/2206.14868)]
   <details close>
   <summary>MultiMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/224786198-a85b76b9-0f8b-434d-be59-bbc41438aac9.png" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

#### **Saliency-based**

* **SaliencyMix: A Saliency Guided Data Augmentation Strategy for Better Regularization**<br>
*A F M Shahab Uddin and Mst. Sirazam Monira and Wheemyung Shin and TaeChoong Chung and Sung-Ho Bae*<br>
ICLR'2021 [[Paper](https://arxiv.org/abs/2006.01791)]
[[Code](https://github.com/SaliencyMix/SaliencyMix)]
   <details close>
   <summary>SaliencyMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204571915-624d3e5e-7678-4ba3-a08c-09ca2741bf72.png" /></p>
   </details>

* **Attentive CutMix: An Enhanced Data Augmentation Approach for Deep Learning Based Image Classification**<br>
*Devesh Walawalkar, Zhiqiang Shen, Zechun Liu, Marios Savvides*<br>
ICASSP'2020 [[Paper](https://arxiv.org/abs/2003.13048)]
[[Code](https://github.com/xden2331/attentive_cutmix)]
   <details close>
   <summary>AttentiveMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204572493-a8c816c9-2be5-43b6-bf35-580cfab8716f.png" /></p>
   </details>

* **SnapMix: Semantically Proportional Mixing for Augmenting Fine-grained Data**<br>
*Shaoli Huang, Xinchao Wang, Dacheng Tao*<br>
AAAI'2021 [[Paper](https://arxiv.org/abs/2012.04846)]
[[Code](https://github.com/Shaoli-Huang/SnapMix)]
   <details close>
   <summary>SnapMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204572296-2035c6b4-c477-4484-a8e6-7ad9ad415045.png" /></p>
   </details>

* **Attribute Mix: Semantic Data Augmentation for Fine Grained Recognition**<br>
*Hao Li, Xiaopeng Zhang, Hongkai Xiong, Qi Tian*<br>
VCIP'2020 [[Paper](https://arxiv.org/abs/2004.02684)]
   <details close>
   <summary>AttributeMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204573220-13a3b90e-73f8-4277-a997-67dddb15dd1c.png" /></p>
   </details>

* **Where to Cut and Paste: Data Regularization with Selective Features**<br>
*Jiyeon Kim, Ik-Hee Shin, Jong-Ryul, Lee, Yong-Ju Lee*<br>
ICTC'2020 [[Paper](https://ieeexplore.ieee.org/abstract/document/9289404)]
[[Code](https://github.com/google-research/augmix)]
   <details close>
   <summary>FocusMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204567137-f71b0437-9267-4f99-b7dc-911ffa4f8b73.png" /></p>
   </details>

* **PuzzleMix: Exploiting Saliency and Local Statistics for Optimal Mixup**<br>
*Jang-Hyun Kim, Wonho Choo, Hyun Oh Song*<br>
ICML'2020 [[Paper](https://arxiv.org/abs/2009.06962)]
[[Code](https://github.com/snu-mllab/PuzzleMix)]
   <details close>
   <summary>PuzzleMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204573527-75f28e86-9b0e-4b14-bd21-ef89de52dd5f.png" /></p>
   </details>

* **Co-Mixup: Saliency Guided Joint Mixup with Supermodular Diversity**<br>
*Jang-Hyun Kim, Wonho Choo, Hosan Jeong, Hyun Oh Song*<br>
ICLR'2021 [[Paper](https://arxiv.org/abs/2102.03065)]
[[Code](https://github.com/snu-mllab/Co-Mixup)]
   <details close>
   <summary>Co-Mixup Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204573653-68ce31e8-fa01-4cf8-9493-c2311fd99e13.png" /></p>
   </details>

* **SuperMix: Supervising the Mixing Data Augmentation**<br>
*Ali Dabouei, Sobhan Soleymani, Fariborz Taherkhani, Nasser M. Nasrabadi*<br>
CVPR'2021 [[Paper](https://arxiv.org/abs/2003.05034)]
[[Code](https://github.com/alldbi/SuperMix)]
   <details close>
   <summary>SuperMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204573912-47ae05f3-8d78-4ef7-b3a9-15d54bffa20a.png" /></p>
   </details>

* **AutoMix: Unveiling the Power of Mixup for Stronger Classifiers**<br>
*Zicheng Liu, Siyuan Li, Di Wu, Zihan Liu, Zhiyuan Chen, Lirong Wu, Stan Z. Li*<br>
ECCV'2022 [[Paper](https://arxiv.org/abs/2103.13027)]
[[Code](https://github.com/Westlake-AI/openmixup)]
   <details close>
   <summary>AutoMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/174272662-19ce57ad-7b08-4e73-81b1-3bb81fee2fe5.png" /></p>
   </details>

* **Boosting Discriminative Visual Representation Learning with Scenario-Agnostic Mixup**<br>
*Siyuan Li, Zicheng Liu, Di Wu, Zihan Liu, Stan Z. Li*<br>
arXiv'2021 [[Paper](https://arxiv.org/abs/2111.15454)]
[[Code](https://github.com/Westlake-AI/openmixup)]
   <details close>
   <summary>SAMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/174272657-fb662377-b7c3-4faa-8d9b-ea6f1e08549e.png" /></p>
   </details>

* **RecursiveMix: Mixed Learning with History**<br>
*Lingfeng Yang, Xiang Li, Borui Zhao, Renjie Song, Jian Yang*<br>
NIPS'2022 [[Paper](https://arxiv.org/abs/2203.06844)]
[[Code](https://github.com/implus/RecursiveMix-pytorch)]
   <details close>
   <summary>RecursiveMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204576092-5fd92410-c12a-4691-8f7b-01901445f2a4.png" /></p>
   </details>

* **TransformMix: Learning Transformation and Mixing Strategies for Sample-mixing Data Augmentation**<br>
*Tsz-Him Cheung, Dit-Yan Yeung*<br>
OpenReview'2023 [[Paper](https://openreview.net/forum?id=-1vpxBUtP0B)]
   <details close>
   <summary>TransformMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204575385-0b2d7470-0ffd-4b6b-977b-ef28b1617954.png" /></p>
   </details>

* **GuidedMixup: An Efficient Mixup Strategy Guided by Saliency Maps**<br>
*Minsoo Kang, Suhyun Kim*<br>
AAAI'2023 [[Paper](https://arxiv.org/abs/2306.16612)]
[[Code](https://github.com/3neutronstar/GuidedMixup)]
   <details close>
   <summary>GuidedMixup Framework</summary>
   <p align="center"><img width="50%" src="https://github-production-user-asset-6210df.s3.amazonaws.com/44519745/250170540-97434afd-790c-4148-81dc-ff7129ca3f7c.png" /></p>
   </details>

* **GradSalMix: Gradient Saliency-Based Mix for Image Data Augmentation**<br>
*Tao Hong, Ya Wang, Xingwu Sun, Fengzong Lian, Zhanhui Kang, Jinwen Ma*<br>
ICME'2023 [[Paper](https://ieeexplore.ieee.org/abstract/document/10219625)]
   <details close>
   <summary>GradSalMix Framework</summary>
   <p align="center"><img width="50%" src="https://github-production-user-asset-6210df.s3.amazonaws.com/44519745/264142659-b8e2eef2-f6ea-4b03-bc03-0d2c08212f3a.png" /></p>
   </details>

* **LGCOAMix: Local and Global Context-and-Object-Part-Aware Superpixel-Based Data Augmentation for Deep Visual Recognition**<br>
*Fadi Dornaika, Danyang Sun*<br>
TIP'2023 [[Paper](https://ieeexplore.ieee.org/document/10348509)]
[[Code](https://github.com/DanielaPlusPlus/LGCOAMix)]
   <details close>
   <summary>LGCOAMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/Westlake-AI/Awesome-Mixup/assets/44519745/802bdd05-dd5d-4d84-a66a-18d0fe9f2fa9" /></p>
   </details>

* **Adversarial AutoMixup**<br>
*Huafeng Qin, Xin Jin, Yun Jiang, Mounim A. El-Yacoubi, Xinbo Gao*<br>
ICLR'2024 [[Paper](https://arxiv.org/abs/2312.11954)]
[[Code](https://github.com/jinxins/adversarial-automixup)]
   <details close>
   <summary>AdAutoMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/Westlake-AI/openmixup/assets/44519745/cdf24e60-e262-4d69-88a6-d1544e625679" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

#### **Attention-based**

* **TokenMix: Rethinking Image Mixing for Data Augmentation in Vision Transformers**<br>
*Jihao Liu, Boxiao Liu, Hang Zhou, Hongsheng Li, Yu Liu*<br>
ECCV'2022 [[Paper](https://arxiv.org/abs/2207.08409)]
[[Code](https://github.com/Sense-X/TokenMix)]
   <details close>
   <summary>TokenMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204578736-7b2dd349-7214-4d49-ade8-30b1caa2f1ea.png" /></p>
   </details>

* **TokenMixup: Efficient Attention-guided Token-level Data Augmentation for Transformers**<br>
*Hyeong Kyu Choi, Joonmyung Choi, Hyunwoo J. Kim*<br>
NIPS'2022 [[Paper](https://arxiv.org/abs/2210.07562)]
[[Code](https://github.com/mlvlab/TokenMixup)]
   <details close>
   <summary>TokenMixup Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204578884-b9d7d466-b26b-4e4b-8a23-22199a6dca26.png" /></p>
   </details>

* **ScoreNet: Learning Non-Uniform Attention and Augmentation for Transformer-Based Histopathological Image Classification**<br>
*Thomas Stegmüller, Behzad Bozorgtabar, Antoine Spahr, Jean-Philippe Thiran*<br>
WACV'2023  [[Paper](https://arxiv.org/abs/2202.07570)]
   <details close>
   <summary>ScoreMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204576297-e97ea9c4-ee17-4ec3-a672-3f088ededb72.png" /></p>
   </details>

* **MixPro: Data Augmentation with MaskMix and Progressive Attention Labeling for Vision Transformer**<br>
*Qihao Zhao, Yangyu Huang, Wei Hu, Fan Zhang, Jun Liu*<br>
ICLR'2023 [[Paper](https://openreview.net/forum?id=dRjWsd3gwsm)]
[[Code](https://github.com/fistyee/MixPro)]
   <details close>
   <summary>MixPro Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/224795935-afb936b2-fc77-4018-a681-72887f96fa59.png" /></p>
   </details>

* **SMMix: Self-Motivated Image Mixing for Vision Transformers**<br>
*Mengzhao Chen, Mingbao Lin, ZhiHang Lin, Yuxin Zhang, Fei Chao, Rongrong Ji*<br>
ICCV'2023 [[Paper](https://arxiv.org/abs/2212.12977)]
[[Code](https://github.com/chenmnz/smmix)]
   <details close>
   <summary>SMMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/213537624-7359689e-b5af-4db1-a4ad-07876dd44089.png" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

#### **Generating Samples**

* **Data Augmentation via Latent Space Interpolation for Image Classification**<br>
*Xiaofeng Liu, Yang Zou, Lingsheng Kong, Zhihui Diao, Junliang Yan, Jun Wang, Site Li, Ping Jia, Jane You<br>
ICPR'2018 [[Paper](https://ieeexplore.ieee.org/abstract/document/8545506)]
   <details close>
   <summary>AEE Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/378e9d22-3031-4874-9dd0-09544c2c8324" /></p>
   </details>

* **On Adversarial Mixup Resynthesis**<br>
*Christopher Beckham, Sina Honari, Vikas Verma, Alex Lamb, Farnoosh Ghadiri, R Devon Hjelm, Yoshua Bengio, Christopher Pal*<br>
NIPS'2019 [[Paper](https://arxiv.org/abs/1903.02709)]
[[Code](https://github.com/christopher-beckham/amr)]
   <details close>
   <summary>AMR Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/232315897-2a5fb2c5-d0ce-4c01-b6cd-21ec54bd9e49.png" /></p>
   </details>

* **AutoMix: Mixup Networks for Sample Interpolation via Cooperative Barycenter Learning**<br>
*Jianchao Zhu, Liangliang Shi, Junchi Yan, Hongyuan Zha*<br>
ECCV'2020 [[Paper](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123550630.pdf)]
   <details close>
   <summary>AutoMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204572771-e09246ca-b88b-4755-8d8a-f99053244610.png" /></p>
   </details>

* **VarMixup: Exploiting the Latent Space for Robust Training and Inference**<br>
*Puneet Mangla, Vedant Singh, Shreyas Jayant Havaldar, Vineeth N Balasubramanian*<br>
CVPRW'2021 [[Paper](https://arxiv.org/abs/2003.06566v1)]
   <details close>
   <summary>VarMixup Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/050d0000-16c9-4bf5-afd7-cb23fe4d6cd0" /></p>
   </details>

* **DiffuseMix: Label-Preserving Data Augmentation with Diffusion Models**<br>
*Khawar Islam, Muhammad Zaigham Zaheer, Arif Mahmood, Karthik Nandakumar*<br>
CVPR'2024 [[Paper](https://arxiv.org/abs/2405.14881)]
[[Code](https://github.com/khawar-islam/diffuseMix)]
   <details close>
   <summary>DiffuseMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/8478e528-a96f-45af-81dc-a3469a6f84bd" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

### Label Mixup Policies in SL

<p align="center">
<img src="https://github.com/user-attachments/assets/214c6969-6b69-48db-99b6-ffe276eb4ca4" width=100% height=100% 
class="center">
</p>

### **Optimizing Calibration**

* **Combining Ensembles and Data Augmentation can Harm your Calibration**<br>
*Yeming Wen, Ghassen Jerfel, Rafael Muller, Michael W. Dusenberry, Jasper Snoek, Balaji Lakshminarayanan, Dustin Tran*<br>
ICLR'2021 [[Paper](https://arxiv.org/abs/2010.09875)]
[[Code](https://github.com/google/edward2/tree/main/experimental/marginalization_mixup)]
   <details close>
   <summary>CAMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204577092-06b2c74a-47cc-44f5-8423-9f37b1d0cbdc.png" /></p>
   </details>

* **RankMixup: Ranking-Based Mixup Training for Network Calibration**<br>
*Jongyoun Noh, Hyekang Park, Junghyup Lee, Bumsub Ham*<br>
ICCV'2023 [[Paper](https://arxiv.org/abs/2308.11990)]
[[Code](https://cvlab.yonsei.ac.kr/projects/RankMixup)]
   <details close>
   <summary>RankMixup Framework</summary>
   <p align="center"><img width="50%" src="https://github-production-user-asset-6210df.s3.amazonaws.com/44519745/264144742-051304d2-4f64-4bd7-9e70-12074c2215e4.png" /></p>
   </details>

* **SmoothMix: Training Confidence-calibrated Smoothed Classifiers for Certified Robustness**<br>
*Jongheon Jeong, Sejun Park, Minkyu Kim, Heung-Chang Lee, Doguk Kim, Jinwoo Shin*<br>
NIPS'2021 [[Paper](https://arxiv.org/abs/2111.09277)]
[[Code](https://github.com/jh-jeong/smoothmix)]
   <details close>
   <summary>SmoothMixup Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/ea280849-dda3-465c-959b-31d10a0cf54c" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

### **Area-based**

* **TransMix: Attend to Mix for Vision Transformers**<br>
*Jie-Neng Chen, Shuyang Sun, Ju He, Philip Torr, Alan Yuille, Song Bai*<br>
CVPR'2022 [[Paper](https://arxiv.org/abs/2111.09833)]
[[Code](https://github.com/Beckschen/TransMix)]
   <details close>
   <summary>TransMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204577728-8d59ad5f-0204-4943-aae7-dca6c48022ce.png" /></p>
   </details>

* **Data Augmentation using Random Image Cropping and Patching for Deep CNNs**<br>
*Ryo Takahashi, Takashi Matsubara, Kuniaki Uehara*<br>
IEEE TCSVT'2020 [[Paper](https://arxiv.org/abs/1811.09030)]
   <details close>
   <summary>RICAP</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/d8fae235-ae35-4fbe-9454-6a8f3b8fce12" /></p>
   </details>

* **RecursiveMix: Mixed Learning with History**<br>
*Lingfeng Yang, Xiang Li, Borui Zhao, Renjie Song, Jian Yang*<br>
NIPS'2022 [[Paper](https://arxiv.org/abs/2203.06844)]
[[Code](https://github.com/implus/RecursiveMix-pytorch)]
   <details close>
   <summary>RecursiveMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204576092-5fd92410-c12a-4691-8f7b-01901445f2a4.png" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

### **Loss Object**

* **Harnessing Hard Mixed Samples with Decoupled Regularizer**<br>
*Zicheng Liu, Siyuan Li, Ge Wang, Cheng Tan, Lirong Wu, Stan Z. Li*<br>
NIPS'2023 [[Paper](https://arxiv.org/abs/2203.10761)]
[[Code](https://github.com/Westlake-AI/openmixup)]
   <details close>
   <summary>DecoupledMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204578387-4be9567c-963a-4d2d-8c1f-c7c5ade527b8.png" /></p>
   </details>

* **MixupE: Understanding and Improving Mixup from Directional Derivative Perspective**<br>
*Vikas Verma, Sarthak Mittal, Wai Hoh Tang, Hieu Pham, Juho Kannala, Yoshua Bengio, Arno Solin, Kenji Kawaguchi*<br>
UAI'2023 [[Paper](https://arxiv.org/abs/2212.13381)]
[[Code](https://github.com/onehuster/mixupe)]
   <details close>
   <summary>MixupE Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/209991074-3dd41cdf-4e64-42e2-8bf4-ebc60e8212d0.png" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

### **Random Label Policies**

* **Mixup Without Hesitation**<br>
*Hao Yu, Huanyu Wang, Jianxin Wu*<br>
ICIG'2022 [[Paper](https://arxiv.org/abs/2101.04342)]
[[Code](https://github.com/yuhao318/mwh)]

* **RegMixup: Mixup as a Regularizer Can Surprisingly Improve Accuracy and Out Distribution Robustness**<br>
*Francesco Pinto, Harry Yang, Ser-Nam Lim, Philip H.S. Torr, Puneet K. Dokania*<br>
NIPS'2022 [[Paper](https://arxiv.org/abs/2206.14502)]
[[Code](https://github.com/FrancescoPinto/RegMixup)]
   <details close>
   <summary>RegMixup Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204571630-e8407bd7-ca27-44de-baca-5d88ca2004a6.png" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

### **Optimizing Mixing Ratio**

* **MixUp as Locally Linear Out-Of-Manifold Regularization**<br>
*Hongyu Guo, Yongyi Mao, Richong Zhang*<br>
AAAI'2019 [[Paper](https://arxiv.org/abs/1809.02499)]
   <details close>
   <summary>AdaMixup Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204563766-4a49b4d9-fb1e-46d7-8443-bff37a527ee1.png" /></p>
   </details>

* **RegMixup: Mixup as a Regularizer Can Surprisingly Improve Accuracy and Out Distribution Robustness**<br>
*Francesco Pinto, Harry Yang, Ser-Nam Lim, Philip H.S. Torr, Puneet K. Dokania*<br>
NIPS'2022 [[Paper](https://arxiv.org/abs/2206.14502)]
[[Code](https://github.com/FrancescoPinto/RegMixup)]
   <details close>
   <summary>RegMixup Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204571630-e8407bd7-ca27-44de-baca-5d88ca2004a6.png" /></p>
   </details>

* **Metamixup: Learning adaptive interpolation policy of mixup with metalearning**<br>
*Zhijun Mai, Guosheng Hu, Dexiong Chen, Fumin Shen, Heng Tao Shen*<br>
IEEE TNNLS'2021 [[Paper](https://arxiv.org/abs/1908.10059)]
   <details close>
   <summary>MetaMixup Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204576802-4aa83a66-61ac-40fd-8904-3b4f9eda62ef.png" /></p>
   </details>

* **LUMix: Improving Mixup by Better Modelling Label Uncertainty**<br>
*Shuyang Sun, Jie-Neng Chen, Ruifei He, Alan Yuille, Philip Torr, Song Bai*<br>
ICASSP'2024 [[Paper](https://arxiv.org/abs/2211.15846)]
[[Code](https://github.com/kevin-ssy/LUMix)]
   <details close>
   <summary>LUMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/205531445-dc4b7790-e0b7-4c41-b9d2-708efa5e4198.png" /></p>
   </details>

* **SUMix: Mixup with Semantic and Uncertain Information**<br>
*Huafeng Qin, Xin Jin, Hongyu Zhu, Hongchao Liao, Mounîm A. El-Yacoubi, Xinbo Gao*<br>
ECCV'2024 [[Paper](https://arxiv.org/abs/2407.07805)]
[[Code](https://github.com/JinXins/SUMix)]
   <details close>
   <summary>SUMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/JinXins/SUMix/assets/124172716/1725dfb7-ab1e-4429-a34b-0dfdd3bc2a6f" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

### **Generating Label**

* **GenLabel: Mixup Relabeling using Generative Models**<br>
*Jy-yong Sohn, Liang Shang, Hongxu Chen, Jaekyun Moon, Dimitris Papailiopoulos, Kangwook Lee*<br>
ICML'2022  [[Paper](https://arxiv.org/abs/2201.02354)]
   <details close>
   <summary>GenLabel Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204578083-3212ed98-6f1b-422b-8764-0276a65bce8e.png" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

### **Attention Score**

* **All Tokens Matter: Token Labeling for Training Better Vision Transformers**<br>
*Zihang Jiang, Qibin Hou, Li Yuan, Daquan Zhou, Yujun Shi, Xiaojie Jin, Anran Wang, Jiashi Feng*<br>
NIPS'2021 [[Paper](https://arxiv.org/abs/2104.10858)]
[[Code](https://github.com/zihangJiang/TokenLabeling)]
   <details close>
   <summary>Token Labeling Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204577372-f679ab10-a65f-4319-9a40-8393c20ad0fa.png" /></p>
   </details>

* **TokenMix: Rethinking Image Mixing for Data Augmentation in Vision Transformers**<br>
*Jihao Liu, Boxiao Liu, Hang Zhou, Hongsheng Li, Yu Liu*<br>
ECCV'2022 [[Paper](https://arxiv.org/abs/2207.08409)]
[[Code](https://github.com/Sense-X/TokenMix)]
   <details close>
   <summary>TokenMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204578736-7b2dd349-7214-4d49-ade8-30b1caa2f1ea.png" /></p>
   </details>

* **TokenMixup: Efficient Attention-guided Token-level Data Augmentation for Transformers**<br>
*Hyeong Kyu Choi, Joonmyung Choi, Hyunwoo J. Kim*<br>
NIPS'2022 [[Paper](https://arxiv.org/abs/2210.07562)]
[[Code](https://github.com/mlvlab/TokenMixup)]
   <details close>
   <summary>TokenMixup Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204578884-b9d7d466-b26b-4e4b-8a23-22199a6dca26.png" /></p>
   </details>

* **MixPro: Data Augmentation with MaskMix and Progressive Attention Labeling for Vision Transformer**<br>
*Qihao Zhao, Yangyu Huang, Wei Hu, Fan Zhang, Jun Liu*<br>
ICLR'2023 [[Paper](https://openreview.net/forum?id=dRjWsd3gwsm)]
[[Code](https://github.com/fistyee/MixPro)]
   <details close>
   <summary>MixPro Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/224795935-afb936b2-fc77-4018-a681-72887f96fa59.png" /></p>
   </details>

* **Token-Label Alignment for Vision Transformers**<br>
*Han Xiao, Wenzhao Zheng, Zheng Zhu, Jie Zhou, Jiwen Lu*<br>
ICCV'2023 [[Paper](https://arxiv.org/abs/2210.06455)]
[[Code](https://github.com/Euphoria16/TL-Align)]
   <details close>
   <summary>TL-Align Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204579080-3b7c9352-8fb3-49bd-99f5-ce4f72d722d8.png" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

### **Saliency Token**

* **SnapMix: Semantically Proportional Mixing for Augmenting Fine-grained Data**<br>
*Shaoli Huang, Xinchao Wang, Dacheng Tao*<br>
AAAI'2021 [[Paper](https://arxiv.org/abs/2012.04846)]
[[Code](https://github.com/Shaoli-Huang/SnapMix)]
   <details close>
   <summary>SnapMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204572296-2035c6b4-c477-4484-a8e6-7ad9ad415045.png" /></p>
   </details>

* **Saliency Grafting: Innocuous Attribution-Guided Mixup with Calibrated Label Mixing**<br>
*Joonhyung Park, June Yong Yang, Jinwoo Shin, Sung Ju Hwang, Eunho Yang*<br>
AAAI'2022 [[Paper](https://arxiv.org/abs/2112.08796)]
   <details close>
   <summary>Saliency Grafting Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204577555-7ffe34ed-74c1-4dff-95e8-f5a9e385f50c.png" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

## Self-Supervised Learning

### **Contrastive Learning**

* **MixCo: Mix-up Contrastive Learning for Visual Representation**<br>
*Sungnyun Kim, Gihun Lee, Sangmin Bae, Se-Young Yun*<br>
NIPSW'2020 [[Paper](https://arxiv.org/abs/2010.06300)]
[[Code](https://github.com/Lee-Gihun/MixCo-Mixup-Contrast)]
   <details close>
   <summary>MixCo Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204580767-c0730ac6-802f-40bc-92a8-4b7abe0acb99.png" /></p>
   </details>

* **Hard Negative Mixing for Contrastive Learning**<br>
*Yannis Kalantidis, Mert Bulent Sariyildiz, Noe Pion, Philippe Weinzaepfel, Diane Larlus*<br>
NIPS'2020 [[Paper](https://arxiv.org/abs/2010.01028)]
[[Code](https://europe.naverlabs.com/mochi)]
   <details close>
   <summary>MoCHi Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204580935-80ebaaaa-2761-4da4-9b58-7755a0dc15c6.png" /></p>
   </details>

* **i-Mix A Domain-Agnostic Strategy for Contrastive Representation Learning**<br>
*Kibok Lee, Yian Zhu, Kihyuk Sohn, Chun-Liang Li, Jinwoo Shin, Honglak Lee*<br>
ICLR'2021 [[Paper](https://arxiv.org/abs/2010.08887)]
[[Code](https://github.com/kibok90/imix)]
   <details close>
   <summary>i-Mix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204581084-5460bd37-4adb-4f01-b7af-fc88ceb2683e.png" /></p>
   </details>

* **Beyond Single Instance Multi-view Unsupervised Representation Learning**<br>
*Xiangxiang Chu, Xiaohang Zhan, Xiaolin Wei*<br>
BMVC'2022 [[Paper](https://arxiv.org/abs/2011.13356)]
   <details close>
   <summary>BSIM Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204581834-3ead412b-359c-40ba-86ea-3ab54ead2c96.png" /></p>
   </details>

* **Improving Contrastive Learning by Visualizing Feature Transformation**<br>
*Rui Zhu, Bingchen Zhao, Jingen Liu, Zhenglong Sun, Chang Wen Chen*<br>
ICCV'2021 [[Paper](https://arxiv.org/abs/2108.02982)]
[[Code](https://github.com/DTennant/CL-Visualizing-Feature-Transformation)]
   <details close>
   <summary>FT Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204582514-426efca3-4e8b-48b8-b69a-ecebb94b7fa8.png" /></p>
   </details>

* **Mix-up Self-Supervised Learning for Contrast-agnostic Applications**<br>
*Yichen Zhang, Yifang Yin, Ying Zhang, Roger Zimmermann*<br>
ICME'2021 [[Paper](https://arxiv.org/abs/2204.00901)]
   <details close>
   <summary>MixSSL Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204583625-58632669-05f0-445b-bd41-60aa37b515d4.png" /></p>
   </details>

* **Unleashing the Power of Contrastive Self-Supervised Visual Models via Contrast-Regularized Fine-Tuning**<br>
*Yifan Zhang, Bryan Hooi, Dapeng Hu, Jian Liang, Jiashi Feng*<br>
NIPS'2021 [[Paper](https://arxiv.org/abs/2102.06605)]
[[Code](https://github.com/Vanint/Core-tuning)]
   <details close>
   <summary>Co-Tuning Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/4f43b519-4781-4e4b-b57f-47ae96af7d80" /></p>
   </details>

* **Center-wise Local Image Mixture For Contrastive Representation Learning**<br>
*Hao Li, Xiaopeng Zhang, Hongkai Xiong*<br>
BMVC'2021 [[Paper](https://arxiv.org/abs/2011.02697)]
   <details close>
   <summary>CLIM Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204583930-15ab3916-9d8b-4adf-9a79-e40eabbbc255.png" /></p>
   </details>

* **Piecing and Chipping: An effective solution for the information-erasing view generation in Self-supervised Learning**<br>
*Jingwei Liu, Yi Gu, Shentong Mo, Zhun Sun, Shumin Han, Jiafeng Guo, Xueqi Cheng*<br>
OpenReview'2021 [[Paper](https://openreview.net/forum?id=DnG8f7gweH4)]
   <details close>
   <summary>PCEA Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204582781-b54c4472-67eb-4e78-9362-44b990bbafa3.png" /></p>
   </details>

* **Boosting Discriminative Visual Representation Learning with Scenario-Agnostic Mixup**<br>
*Siyuan Li, Zicheng Liu, Di Wu, Zihan Liu, Stan Z. Li*<br>
arXiv'2021 [[Paper](https://arxiv.org/abs/2111.15454)]
[[Code](https://github.com/Westlake-AI/openmixup)]
   <details close>
   <summary>SAMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/174272657-fb662377-b7c3-4faa-8d9b-ea6f1e08549e.png" /></p>
   </details>

* **MixSiam: A Mixture-based Approach to Self-supervised Representation Learning**<br>
*Xiaoyang Guo, Tianhao Zhao, Yutian Lin, Bo Du*<br>
OpenReview'2021 [[Paper](https://arxiv.org/abs/2111.02679)]
   <details close>
   <summary>MixSiam Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204583448-8c1890fd-ce95-488a-9570-f7393a4d140a.png" /></p>
   </details>
 
* **Contrast and Mix: Temporal Contrastive Video Domain Adaptation with Background Mixing**<br>
*Aadarsh Sahoo, Rutav Shah, Rameswar Panda, Kate Saenko, Abir Das*<br>
NIPS'2021 [[Paper](https://arxiv.org/abs/2011.02697)]
[[Code](https://cvir.github.io/projects/comix)]
   <details close>
   <summary>CoMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204583146-fc363695-6889-46cd-93f1-236bec9d5fb5.png" /></p>
   </details>

* **Un-Mix: Rethinking Image Mixtures for Unsupervised Visual Representation**<br>
*Zhiqiang Shen, Zechun Liu, Zhuang Liu, Marios Savvides, Trevor Darrell, Eric Xing*<br>
AAAI'2022 [[Paper](https://arxiv.org/abs/2003.05438)]
[[Code](https://github.com/szq0214/Un-Mix)]
   <details close>
   <summary>Un-Mix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204581434-dfbc11f8-e300-4dd7-bc84-adbe5a53dbf4.png" /></p>
   </details>

* **m-Mix: Generating Hard Negatives via Multi-sample Mixing for Contrastive Learning**<br>
*Shaofeng Zhang, Meng Liu, Junchi Yan, Hengrui Zhang, Lingxiao Huang, Pinyan Lu, Xiaokang Yang*<br>
KDD'2022 [[Paper](https://sherrylone.github.io/assets/KDD22_M-Mix.pdf)]
[[Code](https://github.com/Sherrylone/m-mix)]
   <details close>
   <summary>m-Mix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204582292-eef1f644-f39f-46ae-98ba-313501bdb515.png" /></p>
   </details>
   
* **A Simple Data Mixing Prior for Improving Self-Supervised Learning**<br>
*Sucheng Ren, Huiyu Wang, Zhengqi Gao, Shengfeng He, Alan Yuille, Yuyin Zhou, Cihang Xie*<br>
CVPR'2022 [[Paper](https://arxiv.org/abs/2206.07692)]
[[Code](https://github.com/oliverrensu/sdmp)]
   <details close>
   <summary>SDMP Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204585207-6fee3174-224d-44e6-bbd1-514d6697d128.png" /></p>
   </details>

* **CropMix: Sampling a Rich Input Distribution via Multi-Scale Cropping**<br>
*Junlin Han, Lars Petersson, Hongdong Li, Ian Reid*<br>
arXiv'2022 [[Paper](https://arxiv.org/abs/2205.15955)]
[[Code](https://github.com/JunlinHan/CropMix)]
   <details close>
   <summary>CropMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204585732-680295fe-4768-4199-af72-bda10edda644.png" /></p>
   </details>

* **Mixing up contrastive learning: Self-supervised representation learning for time series**<br>
*Kristoffer Wickstrøm, Michael Kampffmeyer, Karl Øyvind Mikalsen, Robert Jenssen*<br>
PR Letter'2022 [[Paper](https://www.sciencedirect.com/science/article/pii/S0167865522000502)]
   <details close>
   <summary>MCL Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/f3a7dc05-e125-4ac4-97c4-81b644e1e97c" /></p>
   </details>

* **Towards Domain-Agnostic Contrastive Learning**<br>
*Vikas Verma, Minh-Thang Luong, Kenji Kawaguchi, Hieu Pham, Quoc V. Le*<br>
ICML'2021 [[Paper](https://arxiv.org/abs/2011.04419)]
   <details close>
   <summary>DACL Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/Westlake-AI/MogaNet/assets/44519745/19c8e3cb-db6f-463f-a765-c243b2f9e45a" /></p>
   </details>

* **ProGCL: Rethinking Hard Negative Mining in Graph Contrastive Learning**<br>
*Jun Xia, Lirong Wu, Ge Wang, Jintao Chen, Stan Z.Li*<br>
ICML'2022 [[Paper](https://arxiv.org/abs/2110.02027)]
[[Code](https://github.com/junxia97/ProGCL)]
   <details close>
   <summary>ProGCL Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204584450-e31a6c9f-0f1c-4342-b907-1b80cae547ab.png" /></p>
   </details>

* **Evolving Image Compositions for Feature Representation Learning**<br>
*Paola Cascante-Bonilla, Arshdeep Sekhon, Yanjun Qi, Vicente Ordonez*<br>
BMVC'2021 [[Paper](https://arxiv.org/abs/2106.09011)]
   <details close>
   <summary>PatchMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204574267-8e53783d-ea54-4399-8c32-86c8ac2520bd.png" /></p>
   </details>

* **On the Importance of Asymmetry for Siamese Representation Learning**<br>
*Xiao Wang, Haoqi Fan, Yuandong Tian, Daisuke Kihara, Xinlei Chen*<br>
CVPR'2022 [[Paper](https://arxiv.org/abs/2204.00613)]
[[Code](https://github.com/facebookresearch/asym-siam)]
   <details close>
   <summary>ScaleMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204585304-03b6aa42-205c-4650-9d90-ecfc0928734e.png" /></p>
   </details>

* **Geodesic Multi-Modal Mixup for Robust Fine-Tuning**<br>
*Changdae Oh, Junhyuk So, Hoyoon Byun, YongTaek Lim, Minchul Shin, Jong-June Jeon, Kyungwoo Song*<br>
NIPS'2023 [[Paper](https://arxiv.org/abs/2203.03897)]
[[Code](https://github.com/changdaeoh/multimodal-mixup)]
   <details close>
   <summary>m2-Mix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/ad6ca047-f04b-463b-9954-eaa15336d4ce" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

### **Masked Image Modeling**

* **i-MAE: Are Latent Representations in Masked Autoencoders Linearly Separable**<br>
*Kevin Zhang, Zhiqiang Shen*<br>
arXiv'2022 [[Paper](https://arxiv.org/abs/2210.11470)]
[[Code](https://github.com/vision-learning-acceleration-lab/i-mae)]
   <details close>
   <summary>i-MAE Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/211220785-5031f97c-c9a3-4ade-b344-48db01fc3760.png" /></p>
   </details>

* **MixMAE: Mixed and Masked Autoencoder for Efficient Pretraining of Hierarchical Vision Transformers**<br>
*Jihao Liu, Xin Huang, Jinliang Zheng, Yu Liu, Hongsheng Li*<br>
CVPR'2023 [[Paper](https://arxiv.org/abs/2205.13137)]
[[Code](https://github.com/Sense-X/MixMIM)]
   <details close>
   <summary>MixMAE Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204315480-5c59ed60-7b5f-4da9-85fb-551a961fd731.png" /></p>
   </details>

* **Mixed Autoencoder for Self-supervised Visual Representation Learning**<br>
*Kai Chen, Zhili Liu, Lanqing Hong, Hang Xu, Zhenguo Li, Dit-Yan Yeung*<br>
CVPR'2023 [[Paper](https://arxiv.org/abs/2303.17152)]
   <details close>
   <summary>MixedAE Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/229929023-1ea53237-ebfb-4203-8b93-dd761d937b27.png" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

### Semi-Supervised Learning

* **MixMatch: A Holistic Approach to Semi-Supervised Learning**<br>
*David Berthelot, Nicholas Carlini, Ian Goodfellow, Nicolas Papernot, Avital Oliver, Colin Raffel*<br>
NIPS'2019 [[Paper](https://arxiv.org/abs/1905.02249)]
[[Code](https://github.com/google-research/mixmatch)]
   <details close>
   <summary>MixMatch Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204580441-1fd71bf7-63f3-4935-9332-287642e0bcc8.png" /></p>
   </details>

* **ReMixMatch: Semi-Supervised Learning with Distribution Matching and Augmentation Anchoring**<br>
*David Berthelot, Nicholas Carlini, Ekin D. Cubuk, Alex Kurakin, Kihyuk Sohn, Han Zhang, Colin Raffel*<br>
ICLR'2020 [[Paper](https://openreview.net/forum?id=HklkeR4KPB)]
[[Code](https://github.com/google-research/remixmatch)]
   <details close>
   <summary>ReMixMatch Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204579631-529bb505-a858-441f-9030-4a9b44273330.png" /></p>
   </details>

* **DivideMix: Learning with Noisy Labels as Semi-supervised Learning**<br>
*Junnan Li, Richard Socher, Steven C.H. Hoi*<br>
ICLR'2020 [[Paper](https://arxiv.org/abs/2002.07394)]
[[Code](https://github.com/LiJunnan1992/DivideMix)]
   <details close>
   <summary>DivideMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/230495626-f0f3f52e-9f8a-472d-8ff2-b33356993e09.png" /></p>
   </details>

* **MixPUL: Consistency-based Augmentation for Positive and Unlabeled Learning**<br>
*Tong Wei, Feng Shi, Hai Wang, Wei-Wei Tu. Yu-Feng Li*<br>
arXiv'2020 [[Paper](https://arxiv.org/abs/2004.09388)]
   <details close>
   <summary>MixPUL Framework</summary>
<!--    <p align="center"><img width="50%" src="https://github-production-user-asset-6210df.s3.amazonaws.com/44519745/283528510-1f3b643c-0edd-416e-9979-110f3d2be6b6.png" /></p> -->
   </details>

* **Milking CowMask for Semi-Supervised Image Classification**<br>
*Geoff French, Avital Oliver, Tim Salimans*<br>
NIPS'2020 [[Paper](https://arxiv.org/abs/2003.12022)]
[[Code](https://github.com/google-research/google-research/tree/master/milking_cowmask)]
   <details close>
   <summary>CowMask Framework</summary>
    <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/aa05ab9c-107e-4c3f-bec0-d93ddcd54bb1" /></p>
   </details>

* **Epsilon Consistent Mixup: Structural Regularization with an Adaptive Consistency-Interpolation Tradeoff**<br>
*Vincent Pisztora, Yanglan Ou, Xiaolei Huang, Francesca Chiaromonte, Jia Li*<br>
arXiv'2021 [[Paper](https://arxiv.org/abs/2104.09452)]
   <details close>
   <summary>Epsilon Consistent Mixup (ϵmu) Framework</summary>
   <p align="center"><img width="50%" src="https://github-production-user-asset-6210df.s3.amazonaws.com/44519745/283528510-1f3b643c-0edd-416e-9979-110f3d2be6b6.png" /></p>
   </details>

* **Who Is Your Right Mixup Partner in Positive and Unlabeled Learning**<br>
*Changchun Li, Ximing Li, Lei Feng, Jihong Ouyang*<br>
ICLR'2021 [[Paper](https://openreview.net/forum?id=NH29920YEmj)]
   <details close>
   <summary>P3Mix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/472870f9-e6f8-4b63-8c05-040db0e255ef" /></p>
   </details>

* **Interpolation Consistency Training for Semi-Supervised Learning**<br>
*Vikas Verma, Kenji Kawaguchi, Alex Lamb, Juho Kannala, Arno Solin, Yoshua Bengio, David Lopez-Paz*<br>
NN'2022 [[Paper](https://arxiv.org/abs/1903.03825)]
   <details close>
   <summary>ICT Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/912458fa-9631-4746-8ba4-8c57ecad476b" /></p>
   </details>

* **Dual-Decoder Consistency via Pseudo-Labels Guided Data Augmentation for Semi-Supervised Medical Image Segmentation**<br>
*Yuanbin Chen, Tao Wang, Hui Tang, Longxuan Zhao, Ruige Zong, Tao Tan, Xinlin Zhang, Tong Tong*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2308.16573)]
   <details close>
   <summary>DCPA Framework</summary>
   <p align="center"><img width="50%" src="https://github-production-user-asset-6210df.s3.amazonaws.com/44519745/268410560-a45c03d9-beb1-4b74-a34b-4d1ecd356de9.png" /></p>
   </details>

* **MUM: Mix Image Tiles and UnMix Feature Tiles for Semi-Supervised Object Detection**<br>
*JongMok Kim, Jooyoung Jang, Seunghyeon Seo, Jisoo Jeong, Jongkeun Na, Nojun Kwak*<br>
CVPR'2022 [[Paper](https://user-images.githubusercontent.com/44519745/225082975-4143e7f5-8873-433c-ab6f-6caa615f7120.png)]
[[Code](https://github.com/jongmokkim/mix-unmix)]
   <details close>
   <summary>MUM Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/225082975-4143e7f5-8873-433c-ab6f-6caa615f7120.png" /></p>
   </details>

* **Harnessing Hard Mixed Samples with Decoupled Regularizer**<br>
*Zicheng Liu, Siyuan Li, Ge Wang, Cheng Tan, Lirong Wu, Stan Z. Li*<br>
NIPS'2023 [[Paper](https://arxiv.org/abs/2203.10761)]
[[Code](https://github.com/Westlake-AI/openmixup)]
   <details close>
   <summary>DFixMatch Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204578387-4be9567c-963a-4d2d-8c1f-c7c5ade527b8.png" /></p>
   </details>

* **Manifold DivideMix: A Semi-Supervised Contrastive Learning Framework for Severe Label Noise**<br>
*Fahimeh Fooladgar, Minh Nguyen Nhat To, Parvin Mousavi, Purang Abolmaesumi*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2308.06861)]
[[Code](https://github.com/Fahim-F/ManifoldDivideMix)]
   <details close>
   <summary>MixEMatch Framework</summary>
   <p align="center"><img width="50%" src="https://github-production-user-asset-6210df.s3.amazonaws.com/44519745/268411562-4263ccd5-a31c-4020-9281-ba4bc3d9fc54.png" /></p>
   </details>

* **LaserMix for Semi-Supervised LiDAR Semantic Segmentation**<br>
*Lingdong Kong, Jiawei Ren, Liang Pan, Ziwei Liu*<br>
CVPR'2023 [[Paper](https://arxiv.org/abs/2207.00026)]
[[Code](https://github.com/ldkong1205/LaserMix)] [[project](https://ldkong.com/LaserMix)]
   <details close>
   <summary>LaserMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/209255964-69cab84b-ae54-4e74-be4f-a23a836c665c.png" /></p>
   </details>
   
* **PCLMix: Weakly Supervised Medical Image Segmentation via Pixel-Level Contrastive Learning and Dynamic Mix Augmentation**<br>
*Yu Lei, Haolun Luo, Lituan Wang, Zhenwei Zhang, Lei Zhang*<br>
arXiv'2024 [[Paper](https://arxiv.org/abs/2405.06288)]
[[Code](https://github.com/Torpedo2648/PCLMix)]
   <details close>
   <summary>PCLMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/Lupin1998/Awesome-MIM/assets/44519745/e41b7e65-962b-49fa-b1be-6e789e8b244e" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

## CV Downstream Tasks

### **Regression**

* **RegMix: Data Mixing Augmentation for Regression**<br>
*Seong-Hyeon Hwang, Steven Euijong Whang*<br>
arXiv'2021 [[Paper](https://arxiv.org/abs/2106.03374)]
   <details close>
   <summary>MixRL Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/6849a6a4-a6cf-4bfc-b483-dd84589de6dc" /></p>
   </details>

* **C-Mixup: Improving Generalization in Regression**<br>
*Huaxiu Yao, Yiping Wang, Linjun Zhang, James Zou, Chelsea Finn*<br>
NIPS'2022 [[Paper](https://arxiv.org/abs/2210.05775)]
[[Code](https://github.com/huaxiuyao/C-Mixup)]
   <details close>
   <summary>C-Mixup Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/721e55da-cdda-4b22-9f72-968d954c6485" /></p>
   </details>

* **ExtraMix: Extrapolatable Data Augmentation for Regression using Generative Models**<br>
*Kisoo Kwon, Kuhwan Jeong, Sanghyun Park, Sangha Park, Hoshik Lee, Seung-Yeon Kwak, Sungmin Kim, Kyunghyun Cho*<br>
OpenReview'2022 [[Paper](https://openreview.net/forum?id=NgEuFT-SIgI)]
   <details close>
   <summary>SupReMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/72a6c717-ab7c-480a-b840-c7b789ae4277" /></p>
   </details>

* **Rank-N-Contrast: Learning Continuous Representations for Regression**<br>
*Kaiwen Zha, Peng Cao, Jeany Son, Yuzhe Yang, Dina Katabi*<br>
NIPS'2023 [[Paper](https://arxiv.org/abs/2210.01189)]
[[Code](https://github.com/kaiwenzha/Rank-N-Contrast)]

* **Anchor Data Augmentation**<br>
*Nora Schneider, Shirin Goshtasbpour, Fernando Perez-Cruz*<br>
NIPS'2023 [[Paper](https://arxiv.org/abs/2311.06965)]

* **Mixup Your Own Pairs**<br>
*Yilei Wu, Zijian Dong, Chongyao Chen, Wangchunshu Zhou, Juan Helen Zhou*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2309.16633)]
[[Code](https://github.com/yilei-wu/supremix)]
   <details close>
   <summary>SupReMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/8510f3d8-7ba9-490a-bdbf-439a69ff4bd6" /></p>
   </details>

* **Tailoring Mixup to Data using Kernel Warping functions**<br>
*Quentin Bouniot, Pavlo Mozharovskyi, Florence d'Alché-Buc*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2311.01434)]
[[Code](https://github.com/ENSTA-U2IS/torch-uncertainty)]
   <details close>
   <summary>Warped Mixup Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/061f5f2b-ff56-415b-9f58-68e895fdad3f" /></p>
   </details>

* **OmniMixup: Generalize Mixup with Mixing-Pair Sampling Distribution**<br>
*Anonymous*<br>
Openreview'2023 [[Paper](https://openreview.net/forum?id=6Uc7Fgwrsm)]

* **Augment on Manifold: Mixup Regularization with UMAP**<br>
*Yousef El-Laham, Elizabeth Fons, Dillon Daudert, Svitlana Vyetrenko*<br>
ICASSP'2024 [[Paper](https://arxiv.org/abs/2210.01189)]

<p align="right">(<a href="#top">back to top</a>)</p>

### **Long tail distribution**

* **Remix: Rebalanced Mixup**<br>
*Hsin-Ping Chou, Shih-Chieh Chang, Jia-Yu Pan, Wei Wei, Da-Cheng Juan*<br>
ECCVW'2020 [[Paper](https://arxiv.org/abs/2007.03943)]
   <details close>
   <summary>Remix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/c776fc89-559f-4e7b-b43a-3e154f3b87c6" /></p>
   </details>

* **Towards Calibrated Model for Long-Tailed Visual Recognition from Prior Perspective**<br>
*Zhengzhuo Xu, Zenghao Chai, Chun Yuan*<br>
NIPS'2021 [[Paper](https://arxiv.org/abs/2111.03874)]
[[Code](https://github.com/XuZhengzhuo/Prior-LT)]
   <details close>
   <summary>UniMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/3d7819d1-c2b8-488f-8a6d-8583a66c7f00" /></p>
   </details>

* **Label-Occurrence-Balanced Mixup for Long-tailed Recognition**<br>
*Shaoyu Zhang, Chen Chen, Xiujuan Zhang, Silong Peng*<br>
ICASSP'2022 [[Paper](https://arxiv.org/abs/2110.04964)]
   <details close>
   <summary>OBMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/89ce6cd5-8f4a-442f-ab05-4549b04e4cb9" /></p>
   </details>

* **DBN-Mix: Training Dual Branch Network Using Bilateral Mixup Augmentation for Long-Tailed Visual Recognition**<br>
*Jae Soon Baik, In Young Yoon, Jun Won Choi*<br>
PR'2024 [[Paper](https://arxiv.org/abs/2110.04964)]
   <details close>
   <summary>DBN-Mix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/ee7988d0-022e-4155-ac69-5e3feaad4ed9" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

### **Segmentation**

* **ClassMix: Segmentation-Based Data Augmentation for Semi-Supervised Learning**<br>
*Viktor Olsson, Wilhelm Tranheden, Juliano Pinto, Lennart Svensson*<br>
WACV'2021 [[Paper](https://arxiv.org/abs/2007.07936)]
[[Code](https://github.com/WilhelmT/ClassMix)]
   <details close>
   <summary>ClassMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/a87397e1-c730-4ef6-a48a-3b2189462582" /></p>
   </details>

* **ChessMix: Spatial Context Data Augmentation for Remote Sensing Semantic Segmentation**<br>
*Matheus Barros Pereira, Jefersson Alex dos Santos*<br>
SIBGRAPI'2021 [[Paper](https://arxiv.org/abs/2108.11535)]
   <details close>
   <summary>ChessMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/07b0d09d-8d38-4f1a-bb1c-bd5b54dfe770" /></p>
   </details>

* **CycleMix: A Holistic Strategy for Medical Image Segmentation from Scribble Supervision**<br>
*Ke Zhang, Xiahai Zhuang*<br>
CVPR'2022 [[Paper](https://arxiv.org/abs/2203.01475)]
[[Code](https://github.com/BWGZK/CycleMix)]
   <details close>
   <summary>CyclesMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/21ee4b1f-255b-4888-a2ec-fb46b7e69122" /></p>
   </details>

* **InsMix: Towards Realistic Generative Data Augmentation for Nuclei Instance Segmentation**<br>
*Yi Lin, Zeyu Wang, Kwang-Ting Cheng, Hao Chen*<br>
MICCAI'2022 [[Paper](https://arxiv.org/abs/2206.15134)]
[[Code](https://github.com/hust-linyi/insmix)]
   <details close>
   <summary>InsMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/4dc23fe3-9bf3-4a83-94fc-b03770e414d5" /></p>
   </details>

* **LaserMix for Semi-Supervised LiDAR Semantic Segmentation**<br>
*Lingdong Kong, Jiawei Ren, Liang Pan, Ziwei Liu*<br>
CVPR'2023 [[Paper](https://arxiv.org/abs/2207.00026)]
[[Code](https://github.com/ldkong1205/LaserMix)] [[project](https://ldkong.com/LaserMix)]
   <details close>
   <summary>LaserMix Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/209255964-69cab84b-ae54-4e74-be4f-a23a836c665c.png" /></p>
   </details>

* **Dual-Decoder Consistency via Pseudo-Labels Guided Data Augmentation for Semi-Supervised Medical Image Segmentation**<br>
*Yuanbin Chen, Tao Wang, Hui Tang, Longxuan Zhao, Ruige Zong, Tao Tan, Xinlin Zhang, Tong Tong*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2308.16573)]
   <details close>
   <summary>DCPA Framework</summary>
   <p align="center"><img width="50%" src="https://github-production-user-asset-6210df.s3.amazonaws.com/44519745/268410560-a45c03d9-beb1-4b74-a34b-4d1ecd356de9.png" /></p>
   </details>

* **SA-MixNet: Structure-aware Mixup and Invariance Learning for Scribble-supervised Road Extraction in Remote Sensing Images**<br>
*Jie Feng, Hao Huang, Junpeng Zhang, Weisheng Dong, Dingwen Zhang, Licheng Jiao*<br>
arXiv'2024 [[Paper](https://arxiv.org/abs/2403.01381)]
[[Code](https://github.com/xdu-jjgs/SA-MixNet-for-Scribble-based-Road-Extraction)]
   <details close>
   <summary>SA-MixNet Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/a4a564f0-9032-4605-9eee-6f2a4337a94b" /></p>
   </details>

* **Constructing and Exploring Intermediate Domains in Mixed Domain Semi-supervised Medical Image Segmentation**<br>
*Qinghe Ma, Jian Zhang, Lei Qi, Qian Yu, Yinghuan Shi, Yang Gao*<br>
CVPR'2024 [[Paper](https://arxiv.org/abs/2404.08951)]
[[Code](https://github.com/MQinghe/MiDSS)]
   <details close>
   <summary>MiDSS Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/1080c789-5dc0-43eb-8e66-61c5eeba2c2f" /></p>
   </details>

* **UniMix: Towards Domain Adaptive and Generalizable LiDAR Semantic Segmentation in Adverse Weather**<br>
*Haimei Zhao, Jing Zhang, Zhuo Chen, Shanshan Zhao, Dacheng Tao*<br>
CVPR'2024 [[Paper](https://arxiv.org/abs/2404.05145)]
[[Code](https://github.com/sunnyHelen/UniMix)]

* **ModelMix: A Holistic Strategy for Medical Image Segmentation from Scribble Supervision**<br>
*Ke Zhang, Vishal M. Patel*<br>
MICCAI'2024 [[Paper](https://arxiv.org/abs/2406.13237)]
   <details close>
   <summary>ModelMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/9b7a31eb-ddd1-4cad-b15b-52dffb6b52c3" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

### **Object Detection**

* **MUM: Mix Image Tiles and UnMix Feature Tiles for Semi-Supervised Object Detection**<br>
*JongMok Kim, Jooyoung Jang, Seunghyeon Seo, Jisoo Jeong, Jongkeun Na, Nojun Kwak*<br>
CVPR'2022 [[Paper](https://arxiv.org/abs/2111.10958)]
[[Code](https://github.com/jongmokkim/mix-unmix)]
   <details close>
   <summary>MUM Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/225082975-4143e7f5-8873-433c-ab6f-6caa615f7120.png" /></p>
   </details>

* **Mixed Pseudo Labels for Semi-Supervised Object Detection**<br>
*Zeming Chen, Wenwei Zhang, Xinjiang Wang, Kai Chen, Zhi Wang*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2312.07006)]
[[Code](https://github.com/czm369/mixpl)]
   <details close>
   <summary>MixPL Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/Westlake-AI/Awesome-Mixup/assets/44519745/c1ac594f-18bb-465b-b0e7-e96249231e2c" /></p>
   </details>

* **MS-DETR: Efficient DETR Training with Mixed Supervision**<br>
*Chuyang Zhao, Yifan Sun, Wenhao Wang, Qiang Chen, Errui Ding, Yi Yang, Jingdong Wang*<br>
arXiv'2024 [[Paper](https://arxiv.org/abs/2401.03989)]
[[Code](https://github.com/Atten4Vis/MS-DETR)]
   <details close>
   <summary>MS-DETR Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/user-attachments/assets/5efea70c-d4f6-4ff8-819b-f68b99fa3c08" /></p>
   </details>

<p align="right">(<a href="#top">back to top</a>)</p>

## Other Applications

<p align="center">
<img src="https://github.com/user-attachments/assets/06c614aa-86ee-4ac7-a2b9-83c3c9fb2087" width=100% height=100% 
class="center">
</p>


## Training Paradigms

### **Federated Learning**

* **XOR Mixup: Privacy-Preserving Data Augmentation for One-Shot Federated Learning**<br>
*MyungJae Shin, Chihoon Hwang, Joongheon Kim, Jihong Park, Mehdi Bennis, Seong-Lyun Kim*<br>
ICML'2020 [[Paper](https://arxiv.org/abs/2111.05073)]
[[Code](https://github.com/ihooni/XOR-Mixup)]

* **FedMix: Approximation of Mixup Under Mean augmented Federated Learning**<br>
*Tehrim Yoon, Sumin Shin, Sung Ju Hwang, Eunho Yang*<br>
ECCV'2022 [[Paper](https://arxiv.org/abs/2107.00233)]
[[Code](https://github.com/DevPranjal/fedmix)]

* **Mix2FLD: Downlink Federated Learning After Uplink Federated Distillation With Two-Way Mixup**<br>
*Seungeun Oh, Jihong Park, Eunjeong Jeong, Hyesung Kim, Mehdi Bennis, Seong-Lyun Kim*<br>
IEEE Communications Letters'2020 [[Paper](https://ieeexplore.ieee.org/document/9121290)]

* **StatMix: Data augmentation method that relies on image statistics in federated learning**<br>
*Dominik Lewy, Jacek Mańdziuk, Maria Ganzha, Marcin Paprzycki*<br>
ICONIP'2022 [[Paper](https://link.springer.com/chapter/10.1007/978-981-99-1639-9_48)]

<p align="right">(<a href="#top">back to top</a>)</p>

### **Adversarial Attack and Adversarial Training**

* **Addressing Neural Network Robustness with Mixup and Targeted Labeling Adversarial Training**<br>
*Alfred Laugros, Alice Caplier, Matthieu Ospici*<br>
ECCV'2020 [[Paper](https://arxiv.org/abs/2008.08384)]

* **Mixup Inference: Better Exploiting Mixup to Defend Adversarial Attacks**<br>
*Tianyu Pang, Kun Xu, Jun Zhu*<br>
ICLR'2020 [[Paper](https://arxiv.org/abs/1909.11515)]
[[Code](https://github.com/P2333/Mixup-Inference)]

* **Adversarial Vertex Mixup: Toward Better Adversarially Robust Generalization**<br>
*Saehyung Lee, Hyungyu Lee, Sungroh Yoon*<br>
CVPR'2020 [[Paper](https://arxiv.org/abs/2003.02484)]
[[Code](https://github.com/Saehyung-Lee/cifar10_challenge)]

* **Adversarial Mixing Policy for Relaxing Locally Linear Constraints in Mixup**<br>
*Guang Liu, Yuzhao Mao, Hailong Huang, Weiguo Gao, Xuan Li*<br>
EMNLP'2021 [[Paper](https://arxiv.org/abs/2109.07177)]

* **Adversarially Optimized Mixup for Robust Classification**<br>
*Jason Bunk, Srinjoy Chattopadhyay, B. S. Manjunath, Shivkumar Chandrasekaran*<br>
arXiv'2021 [[Paper](https://arxiv.org/abs/2103.11589)]

* **Better Robustness by More Coverage: Adversarial and Mixup Data Augmentation for Robust Finetuning**<br>
*Guillaume P. Archambault, Yongyi Mao, Hongyu Guo, Richong Zhang*<br>
ACL'2021 [[Paper](https://aclanthology.org/2021.findings-acl.137/)]

* **Interpolated Adversarial Training: Achieving Robust Neural Networks without Sacrificing Too Much Accuracy**<br>
*Alex Lamb, Vikas Verma, Kenji Kawaguchi, Alexander Matyasko, Savya Khosla, Juho Kannala, Yoshua Bengio*<br>
NN'2021 [[Paper](https://arxiv.org/abs/1906.06784)]

* **Semi-supervised Semantics-guided Adversarial Training for Trajectory Prediction**<br>
*Ruochen Jiao, Xiangguo Liu, Takami Sato, Qi Alfred Chen, Qi Zhu*<br>
ICCV'2023 [[Paper](https://ieeexplore.ieee.org/document/10376952)]

* **Mixup as directional adversarial training**<br>
*Guillaume P. Archambault, Yongyi Mao, Hongyu Guo, Richong Zhang*<br>
NIPS'2019 [[Paper](https://arxiv.org/abs/1906.06875)]
[[Code](https://github.com/mixupAsDirectionalAdversarial/mixup_as_dat)]

* **On the benefits of defining vicinal distributions in latent space**<br>
*Puneet Mangla, Vedant Singh, Shreyas Jayant Havaldar, Vineeth N Balasubramanian*<br>
CVPRW'2021 [[Paper](https://arxiv.org/abs/2003.06566)]

<p align="right">(<a href="#top">back to top</a>)</p>

### **Domain Adaption**

* **Mix-up Self-Supervised Learning for Contrast-agnostic Applications**<br>
*Yichen Zhang, Yifang Yin, Ying Zhang, Roger Zimmermann*<br>
ICDE'2022 [[Paper](https://arxiv.org/abs/2204.00901)]

* **Contrast and Mix: Temporal Contrastive Video Domain Adaptation with Background Mixing**<br>
*Aadarsh Sahoo, Rutav Shah, Rameswar Panda, Kate Saenko, Abir Das*<br>
NIPS'2021 [[Paper](https://arxiv.org/abs/2110.15128)]
[[Code](https://github.com/CVIR/CoMix)]

* **Virtual Mixup Training for Unsupervised Domain Adaptation**<br>
*Xudong Mao, Yun Ma, Zhenguo Yang, Yangbin Chen, Qing Li*<br>
arXiv'2019 [[Paper](https://arxiv.org/abs/1905.04215)]
[[Code](https://github.com/xudonmao/VMT)]

* **Improve Unsupervised Domain Adaptation with Mixup Training**<br>
*Shen Yan, Huan Song, Nanxiang Li, Lincan Zou, Liu Ren*<br>
arXiv'2020 [[Paper](https://arxiv.org/abs/2001.00677)]

* **Adversarial Domain Adaptation with Domain Mixup**<br>
*Minghao Xu, Jian Zhang, Bingbing Ni, Teng Li, Chengjie Wang, Qi Tian, Wenjun Zhang*<br>
AAAI'2020 [[Paper](https://arxiv.org/abs/1912.01805)]
[[Code](https://github.com/ChrisAllenMing/Mixup_for_UDA)]

* **Dual Mixup Regularized Learning for Adversarial Domain Adaptation**<br>
*Yuan Wu, Diana Inkpen, Ahmed El-Roby*<br>
ECCV'2020 [[Paper](https://arxiv.org/abs/2007.03141)]
[[Code](https://github.com/YuanWu3/Dual-Mixup-Regularized-Learning-for-Adversarial-Domain-Adaptation)]

* **Select, Label, and Mix: Learning Discriminative Invariant Feature Representations for Partial Domain Adaptation**<br>
*Aadarsh Sahoo, Rameswar Panda, Rogerio Feris, Kate Saenko, Abir Das*<br>
WACV'2023 [[Paper](https://arxiv.org/abs/2012.03358)]
[[Code](https://github.com/CVIR/SLM)]

* **Spectral Adversarial MixUp for Few-Shot Unsupervised Domain Adaptation**<br>
*Jiajin Zhang, Hanqing Chao, Amit Dhurandhar, Pin-Yu Chen, Ali Tajer, Yangyang Xu, Pingkun Yan*<br>
MICCAI'2023 [[Paper](https://arxiv.org/abs/2309.01207)]
[[Code](https://github.com/RPIDIAL/SAMix)]

<p align="right">(<a href="#top">back to top</a>)</p>

### **Knowledge Distillation**

* **MixACM: Mixup-Based Robustness Transfer via Distillation of Activated Channel Maps**<br>
*Muhammad Awais, Fengwei Zhou, Chuanlong Xie, Jiawei Li, Sung-Ho Bae, Zhenguo Li*<br>
NIPS'2021 [[Paper](https://arxiv.org/abs/2111.05073)]

* **MixSKD: Self-Knowledge Distillation from Mixup for Image Recognition**<br>
*Chuanguang Yang, Zhulin An, Helong Zhou, Linhang Cai, Xiang Zhi, Jiwen Wu, Yongjun Xu, Qian Zhang*<br>
ECCV'2022 [[Paper](https://arxiv.org/abs/2208.05768)]

* **Understanding the Role of Mixup in Knowledge Distillation: An Empirical Study**<br>
*Chuanguang Yang, Zhulin An, Helong Zhou, Linhang Cai, Xiang Zhi, Jiwen Wu, Yongjun Xu, Qian Zhang*<br>
WACV'2023 [[Paper](https://arxiv.org/abs/2211.03946)]

<p align="right">(<a href="#top">back to top</a>)</p>

### **Multi-Modal**

* **MixGen: A New Multi-Modal Data Augmentation**<br>
*Xiaoshuai Hao, Yi Zhu, Srikar Appalaraju, Aston Zhang, Wanqian Zhang, Bo Li, Mu Li*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2206.08358)]
[[Code](https://github.com/amazon-research/mix-generation)]

* **VLMixer: Unpaired Vision-Language Pre-training via Cross-Modal CutMix**<br>
*Teng Wang, Wenhao Jiang, Zhichao Lu, Feng Zheng, Ran Cheng, Chengguo Yin, Ping Luo*<br>
ICML'2022 [[Paper](https://arxiv.org/abs/2206.08919)]
   <details close>
   <summary>VLMixer Framework</summary>
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204585605-f60ae9af-b7af-4af4-ac46-28bac51c7a02.png" /></p>
   </details>

* **Geodesic Multi-Modal Mixup for Robust Fine-Tuning**<br>
*Changdae Oh, Junhyuk So, Hoyoon Byun, YongTaek Lim, Minchul Shin, Jong-June Jeon, Kyungwoo Song*<br>
NIPS'2023 [[Paper](https://arxiv.org/abs/2203.03897)]
[[Code](https://github.com/changdaeoh/multimodal-mixup)]

* **PowMix: A Versatile Regularizer for Multimodal Sentiment Analysis**<br>
*Efthymios Georgiou, Yannis Avrithis, Alexandros Potamianos*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2312.12334)]
   <details close>
   <summary>PowMix Framework</summary>
   <p align="center"><img width="50%" src="https://github.com/Westlake-AI/openmixup/assets/44519745/272e44b8-1872-4cdf-9a69-71e48cc428cd" /></p>
   </details>

* **Enhance image classification via inter-class image mixup with diffusion model**<br>
*Efthymios Georgiou, Yannis Avrithis, Alexandros Potamianos*<br>
CVPR'2024 [[Paper](https://arxiv.org/abs/2312.12334)]
[[Code](https://github.com/Zhicaiwww/Diff-Mix)]
   
<p align="right">(<a href="#top">back to top</a>)</p>

## Beyond Vision

### **NLP**

* **Augmenting Data with Mixup for Sentence Classification: An Empirical Study**<br>
*Hongyu Guo, Yongyi Mao, Richong Zhang*<br>
arXiv'2019 [[Paper](https://arxiv.org/abs/1905.08941)]
[[Code](https://github.com/dsfsi/textaugment)]

* **Adversarial Mixing Policy for Relaxing Locally Linear Constraints in Mixup**<br>
*Guang Liu, Yuzhao Mao, Hailong Huang, Weiguo Gao, Xuan Li*<br>
EMNLP'2021 [[Paper](https://arxiv.org/abs/2109.07177)]

* **SeqMix: Augmenting Active Sequence Labeling via Sequence Mixup**<br>
*Hongyu Guo, Yongyi Mao, Richong Zhang*<br>
EMNLP'2020 [[Paper](https://aclanthology.org/2020.emnlp-main.691/)]
[[Code](https://github.com/rz-zhang/SeqMix)]

* **Mixup-Transformer: Dynamic Data Augmentation for NLP Tasks**<br>
*Lichao Sun, Congying Xia, Wenpeng Yin, Tingting Liang, Philip S. Yu, Lifang He*<br>
COLING'2020 [[Paper](https://arxiv.org/abs/2010.02394)]

* **Calibrated Language Model Fine-Tuning for In- and Out-of-Distribution Data**<br>
*Lingkai Kong, Haoming Jiang, Yuchen Zhuang, Jie Lyu, Tuo Zhao, Chao Zhang*<br>
EMNLP'2020 [[Paper](https://arxiv.org/abs/2010.11506)]
[[Code](https://github.com/Lingkai-Kong/Calibrated-BERT-Fine-Tuning)]

* **Augmenting NLP Models using Latent Feature Interpolations**<br>
*Amit Jindal, Arijit Ghosh Chowdhury, Aniket Didolkar, Di Jin, Ramit Sawhney, Rajiv Ratn Shah*<br>
COLING'2020 [[Paper](https://aclanthology.org/2020.coling-main.611/)]

* **MixText: Linguistically-informed Interpolation of Hidden Space for Semi-Supervised Text Classification**<br>
*Jiaao Chen, Zichao Yang, Diyi Yang*<br>
ACL'2020 [[Paper](https://arxiv.org/abs/2004.12239)]
[[Code](https://github.com/GT-SALT/MixText)]

* **Sequence-Level Mixed Sample Data Augmentation**<br>
*Jiaao Chen, Zichao Yang, Diyi Yang*<br>
EMNLP'2020 [[Paper](https://aclanthology.org/2020.emnlp-main.447/)]
[[Code](https://github.com/dguo98/seqmix)]

* **AdvAug: Robust Adversarial Augmentation for Neural Machine Translation**<br>
*Yong Cheng, Lu Jiang, Wolfgang Macherey, Jacob Eisenstein*<br>
ACL'2020 [[Paper](https://aclanthology.org/2020.acl-main.529.pdf)]
[[Code](https://github.com/dguo98/seqmix)]

* **Local Additivity Based Data Augmentation for Semi-supervised NER**<br>
*Jiaao Chen, Zhenghui Wang, Ran Tian, Zichao Yang, Diyi Yang*<br>
ACL'2020 [[Paper](https://aclanthology.org/2020.emnlp-main.95/)]
[[Code](https://github.com/SALT-NLP/LADA)]

* **Mixup Decoding for Diverse Machine Translation**<br>
*Jicheng Li, Pengzhi Gao, Xuanfu Wu, Yang Feng, Zhongjun He, Hua Wu, Haifeng Wang*<br>
 EMNLP'2021 [[Paper](https://arxiv.org/abs/2109.03402)]

* **TreeMix: Compositional Constituency-based Data Augmentation for Natural Language Understanding**<br>
*Le Zhang, Zichao Yang, Diyi Yang*<br>
NAALC'2022 [[Paper](https://arxiv.org/abs/2205.06153)]
[[Code](https://github.com/magiccircuit/treemix)]

* **STEMM: Self-learning with Speech-text Manifold Mixup for Speech Translation**<br>
*Qingkai Fang, Rong Ye, Lei Li, Yang Feng, Mingxuan Wang*<br>
ACL'2022 [[Paper](https://arxiv.org/abs/2010.02394)]
[[Code](https://github.com/ictnlp/STEMM)]

* **AdMix: A Mixed Sample Data Augmentation Method for Neural Machine Translation**<br>
*Chang Jin, Shigui Qiu, Nini Xiao, Hao Jia*<br>
IJCAI'2022 [[Paper](https://www.ijcai.org/proceedings/2022/0579.pdf)]

* **Enhancing Cross-lingual Transfer by Manifold Mixup**<br>
*Huiyun Yang, Huadong Chen, Hao Zhou, Lei Li*<br>
ICLR'2022 [[Paper](https://arxiv.org/abs/2205.04182)]
[[Code](https://github.com/yhy1117/x-mixup)]

* **Multilingual Mix: Example Interpolation Improves Multilingual Neural Machine Translation**<br>
*Yong Cheng, Ankur Bapna, Orhan Firat, Yuan Cao, Pidong Wang, Wolfgang Macherey*<br>
ACL'2022 [[Paper](https://aclanthology.org/2022.acl-long.282/)]

<p align="right">(<a href="#top">back to top</a>)</p>

### **GNN**

* **Node Augmentation Methods for Graph Neural Network based Object Classification**<br>
*Yifan Xue; Yixuan Liao; Xiaoxin Chen; Jingwei Zhao*<br>
CDS'2021 [[Paper](https://ieeexplore.ieee.org/document/9463199/authors#authors)]

* **Mixup for Node and Graph Classification**<br>
*Yiwei Wang, Wei Wang, Yuxuan Liang, Yujun Cai, Bryan Hooi*<br>
WWW'2021 [[Paper](https://dl.acm.org/doi/10.1145/3442381.3449796)]
[[Code](https://github.com/vanoracai/MixupForGraph)]

* **Graph Mixed Random Network Based on PageRank**<br>
*Qianli Ma, Zheng Fan, Chenzhi Wang, Hongye Tan*<br>
Symmetry'2022 [[Paper](https://www.mdpi.com/2073-8994/14/8/1678)]

* **GraphSMOTE: Imbalanced Node Classification on Graphs with Graph Neural Networks**<br>
*Tianxiang Zhao, Xiang Zhang, Suhang Wang*<br>
WSDM'2021 [[Paper](https://arxiv.org/abs/2103.08826)]

* **GraphMix: Improved Training of GNNs for Semi-Supervised Learning**<br>
*Vikas Verma, Meng Qu, Kenji Kawaguchi, Alex Lamb, Yoshua Bengio, Juho Kannala, Jian Tang*<br>
AAAI'2021 [[Paper](https://arxiv.org/abs/1909.11715)]
[[Code](https://github.com/vikasverma1077/GraphMix)]

* **GraphMixup: Improving Class-Imbalanced Node Classification on Graphs by Self-supervised Context Prediction**<br>
*Lirong Wu, Haitao Lin, Zhangyang Gao, Cheng Tan, Stan.Z.Li*<br>
ECML-PKDD'2022 [[Paper](https://link.springer.com/chapter/10.1007/978-3-031-19818-2_34)]
[[Code](https://github.com/LirongWu/GraphMixup)]

* **Graph Transplant: Node Saliency-Guided Graph Mixup with Local Structure Preservation**<br>
*Joonhyung Park, Hajin Shim, Eunho Yang*<br>
AAAI'2022 [[Paper](https://arxiv.org/abs/2111.05639)]
[[Code](https://github.com/shimazing/Graph-Transplant)]

* **G-Mixup: Graph Data Augmentation for Graph Classification**<br>
*Xiaotian Han, Zhimeng Jiang, Ninghao Liu, Xia Hu*<br>
ICML'2022 [[Paper](https://arxiv.org/abs/2202.07179)]

* **Fused Gromov-Wasserstein Graph Mixup for Graph-level Classifications**<br>
*Xinyu Ma, Xu Chu, Yasha Wang, Yang Lin, Junfeng Zhao, Liantao Ma, Wenwu Zhu*<br>
NIPS'2023 [[Paper](https://arxiv.org/abs/2306.15963)]
[[code](https://github.com/ArthurLeoM/FGWMixup)]

* **iGraphMix: Input Graph Mixup Method for Node Classification**<br>
*Jongwon Jeong, Hoyeop Lee, Hyui Geon Yoon, Beomyoung Lee, Junhee Heo, Geonsoo Kim, Kim Jin Seon*<br>
ICLR'2024 [[Paper](https://openreview.net/forum?id=a2ljjXeDcE)]

<p align="right">(<a href="#top">back to top</a>)</p>

### **3D Point**

* **PointMixup: Augmentation for Point Clouds**<br>
*Yunlu Chen, Vincent Tao Hu, Efstratios Gavves, Thomas Mensink, Pascal Mettes, Pengwan Yang, Cees G.M. Snoek*<br>
ECCV'2020 [[Paper](https://arxiv.org/abs/2008.06374)]
[[Code](https://github.com/yunlu-chen/PointMixup/)]

* **PointCutMix: Regularization Strategy for Point Cloud Classification**<br>
*Jinlai Zhang, Lyujie Chen, Bo Ouyang, Binbin Liu, Jihong Zhu, Yujing Chen, Yanmei Meng, Danfeng Wu*<br>
Neurocomputing'2022 [[Paper](https://arxiv.org/abs/2101.01461)]
[[Code](https://github.com/cuge1995/PointCutMix)]

* **Regularization Strategy for Point Cloud via Rigidly Mixed Sample**<br>
*Dogyoon Lee, Jaeha Lee, Junhyeop Lee, Hyeongmin Lee, Minhyeok Lee, Sungmin Woo, Sangyoun Lee*<br>
CVPR'2021 [[Paper](https://arxiv.org/abs/2102.01929)]
[[Code](https://github.com/dogyoonlee/RSMix)]

* **Part-Aware Data Augmentation for 3D Object Detection in Point Cloud**<br>
*Jaeseok Choi, Yeji Song, Nojun Kwak*<br>
IROS'2021 [[Paper](https://arxiv.org/abs/2007.13373)]
[[Code](https://github.com/sky77764/pa-aug.pytorch)]

* **Point MixSwap: Attentional Point Cloud Mixing via Swapping Matched Structural Divisions**<br>
*Ardian Umam, Cheng-Kun Yang, Yung-Yu Chuang, Jen-Hui Chuang, Yen-Yu Lin*<br>
ECCV'2022 [[Paper](https://link.springer.com/chapter/10.1007/978-3-031-19818-2_34)]
[[Code](https://github.com/ardianumam/PointMixSwap)]
   
<p align="right">(<a href="#top">back to top</a>)</p>

### **Other**

* **Embedding Expansion: Augmentation in Embedding Space for Deep Metric Learning**<br>
*Byungsoo Ko, Geonmo Gu*<br>
CVPR'2020 [[Paper](https://arxiv.org/abs/2003.02546)]
[[Code](https://github.com/clovaai/embedding-expansion)]

* **SalfMix: A Novel Single Image-Based Data Augmentation Technique Using a Saliency Map**<br>
*Jaehyeop Choi, Chaehyeon Lee, Donggyu Lee, Heechul Jung*<br>
Sensor'2021 [[Paper](https://pdfs.semanticscholar.org/1db9/c80edeed50858783c69237aeba764750e8b7.pdf?_ga=2.182064935.1813772674.1674154381-1810295069.1625160008)]

* **Octave Mix: Data Augmentation Using Frequency Decomposition for Activity Recognition**<br>
*Tatsuhito Hasegawa*<br>
IEEE Access'2021 [[Paper](https://ieeexplore.ieee.org/document/9393911)]

* **Guided Interpolation for Adversarial Training**<br>
*Chen Chen, Jingfeng Zhang, Xilie Xu, Tianlei Hu, Gang Niu, Gang Chen, Masashi Sugiyama*<br>
arXiv'2021 [[Paper](https://arxiv.org/abs/2102.07327)]

* **Recall@k Surrogate Loss with Large Batches and Similarity Mixup**<br>
*Yash Patel, Giorgos Tolias, Jiri Matas*<br>
CVPR'2022 [[Paper](https://arxiv.org/abs/2108.11179)]
[[Code](https://github.com/yash0307/RecallatK_surrogate)]

* **Contrastive-mixup Learning for Improved Speaker Verification**<br>
*Xin Zhang, Minho Jin, Roger Cheng, Ruirui Li, Eunjung Han, Andreas Stolcke*<br>
ICASSP'2022 [[Paper](https://arxiv.org/abs/2202.10672)]

* **Noisy Feature Mixup**<br>
*Soon Hoe Lim, N. Benjamin Erichson, Francisco Utrera, Winnie Xu, Michael W. Mahoney*<br>
ICLR'2022 [[Paper](https://arxiv.org/abs/2110.02180)]
[[Code](https://github.com/erichson/NFM)]

* **It Takes Two to Tango: Mixup for Deep Metric Learning**<br>
*Shashanka Venkataramanan, Bill Psomas, Ewa Kijak, Laurent Amsaleg, Konstantinos Karantzalos, Yannis Avrithis*<br>
ICLR'2022 [[Paper](https://arxiv.org/abs/2106.04990)]
[[Code](https://github.com/billpsomas/metrix)]

* **Representational Continuity for Unsupervised Continual Learning**<br>
*Divyam Madaan, Jaehong Yoon, Yuanchun Li, Yunxin Liu, Sung Ju Hwang*<br>
ICLR'2022 [[Paper](https://arxiv.org/abs/2110.06976)]
[[Code](https://github.com/divyam3897/UCL)]

* **Expeditious Saliency-guided Mix-up through Random Gradient Thresholding**<br>
*Remy Sun, Clement Masson, Gilles Henaff, Nicolas Thome, Matthieu Cord.*<br>
ICPR'2022 [[Paper](https://arxiv.org/abs/2205.10158)]

* **Guarding Barlow Twins Against Overfitting with Mixed Samples**<br>
*Wele Gedara Chaminda Bandara, Celso M. De Melo, Vishal M. Patel*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2312.02151)]
[[Code](https://github.com/wgcban/mix-bt)]

* **Infinite Class Mixup**<br>
*Thomas Mensink, Pascal Mettes*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2305.10293)]

* **Semantic Equivariant Mixup**<br>
*Zongbo Han, Tianchi Xie, Bingzhe Wu, Qinghua Hu, Changqing Zhang*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2308.06451)]

* **G-Mix: A Generalized Mixup Learning Framework Towards Flat Minima**<br>
*Xingyu Li, Bo Tang*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2308.03236)]

* **Inter-Instance Similarity Modeling for Contrastive Learning**<br>
*Chengchao Shen, Dawei Liu, Hao Tang, Zhe Qu, Jianxin Wang*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2306.12243)]
[[Code](https://github.com/visresearch/patchmix)]

* **Single-channel speech enhancement using learnable loss mixup**<br>
*Oscar Chang, Dung N. Tran, Kazuhito Koishida*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2312.17255)]

* **Selective Volume Mixup for Video Action Recognition**<br>
*Yi Tan, Zhaofan Qiu, Yanbin Hao, Ting Yao, Xiangnan He, Tao Mei*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2309.09534)]

* **Rethinking Data Augmentation for Image Super-resolution: A Comprehensive Analysis and a New Strategy**<br>
*Jaejun Yoo, Namhyuk Ahn, Kyung-Ah Sohn*<br>
CVPR'2020 & IJCV'2024 [[Paper](https://arxiv.org/abs/2110.06976)]
[[Code](https://github.com/clovaai/cutblur)]

* **DNABERT-S: Learning Species-Aware DNA Embedding with Genome Foundation Models**<br>
*Zhihan Zhou, Weimin Wu, Harrison Ho, Jiayi Wang, Lizhen Shi, Ramana V Davuluri, Zhong Wang, Han Liu*<br>
arXiv'2024 [[Paper](https://ieeexplore.ieee.org/document/9156551)]
[[Code](https://github.com/MAGICS-LAB/DNABERT_S)]

* **ContextMix: A context-aware data augmentation method for industrial visual inspection systems**<br>
*Hyungmin Kim, Donghun Kim, Pyunghwan Ahn, Sungho Suh, Hansang Cho, Junmo Kim*<br>
EAAI'2024 [[Paper](https://arxiv.org/abs/2401.10050)]

* **Robust Image Denoising through Adversarial Frequency Mixup**<br>
*Donghun Ryou, Inju Ha, Hyewon Yoo, Dongwan Kim, Bohyung Han*<br>
CVPR'2024 [[Paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Ryou_Robust_Image_Denoising_through_Adversarial_Frequency_Mixup_CVPR_2024_paper.pdf)]
[[Code](https://github.com/dhryougit/AFM)]

<p align="right">(<a href="#top">back to top</a>)</p>

## Analysis and Theorem

* **Understanding Mixup Training Methods**<br>
*Daojun Liang, Feng Yang, Tian Zhang, Peter Yang*<br>
NIPS'2019 [[Paper](https://ieeexplore.ieee.org/document/8478159/authors#authors)]

* **MixUp as Locally Linear Out-Of-Manifold Regularization**<br>
*Hongyu Guo, Yongyi Mao, Richong Zhang*<br>
AAAI'2019 [[Paper](https://arxiv.org/abs/1809.02499)]

* **MixUp as Directional Adversarial Training**<br>
*Chanwoo Park, Sangdoo Yun, Sanghyuk Chun*<br>
NIPS'2019 [[Paper](https://arxiv.org/abs/1906.06875)]

* **On Mixup Training: Improved Calibration and Predictive Uncertainty for Deep Neural Networks**<br>
*Sunil Thulasidasan, Gopinath Chennupati, Jeff Bilmes, Tanmoy Bhattacharya, Sarah Michalak*<br>
NIPS'2019 [[Paper](https://arxiv.org/abs/1905.11001)]
[[Code](https://github.com/paganpasta/onmixup)]

* **On Mixup Regularization**<br>
*Luigi Carratino, Moustapha Cissé, Rodolphe Jenatton, Jean-Philippe Vert*<br>
arXiv'2020 [[Paper](https://arxiv.org/abs/2006.06049)]

* **Mixup Training as the Complexity Reduction**<br>
*Masanari Kimura*<br>
arXiv'2021 [[Paper](https://arxiv.org/abs/1906.06875)]

* **How Does Mixup Help With Robustness and Generalization**<br>
*Linjun Zhang, Zhun Deng, Kenji Kawaguchi, Amirata Ghorbani, James Zou*<br>
ICLR'2021 [[Paper](https://arxiv.org/abs/2010.04819)]

* **Mixup Without Hesitation**<br>
*Hao Yu, Huanyu Wang, Jianxin Wu*<br>
ICIG'2022 [[Paper](https://arxiv.org/abs/2101.04342)]
[[Code](https://github.com/yuhao318/mwh)]

* **RegMixup: Mixup as a Regularizer Can Surprisingly Improve Accuracy and Out Distribution Robustness**<br>
*Francesco Pinto, Harry Yang, Ser-Nam Lim, Philip H.S. Torr, Puneet K. Dokania*<br>
NIPS'2022 [[Paper](https://arxiv.org/abs/2206.14502)]
[[Code](https://github.com/FrancescoPinto/RegMixup)]

* **A Unified Analysis of Mixed Sample Data Augmentation: A Loss Function Perspective**<br>
*Chanwoo Park, Sangdoo Yun, Sanghyuk Chun*<br>
NIPS'2022 [[Paper](https://arxiv.org/abs/2208.09913)]
[[Code](https://github.com/naver-ai/hmix-gmix)]

* **Towards Understanding the Data Dependency of Mixup-style Training**<br>
*Muthu Chidambaram, Xiang Wang, Yuzheng Hu, Chenwei Wu, Rong Ge*<br>
ICLR'2022 [[Paper](https://openreview.net/pdf?id=ieNJYujcGDO)]
[[Code](https://github.com/2014mchidamb/Mixup-Data-Dependency)]

* **When and How Mixup Improves Calibration**<br>
*Linjun Zhang, Zhun Deng, Kenji Kawaguchi, James Zou*<br>
ICML'2022 [[Paper](https://arxiv.org/abs/2102.06289)]

* **Provable Benefit of Mixup for Finding Optimal Decision Boundaries**<br>
*Junsoo Oh, Chulhee Yun*<br>
ICML'2023 [[Paper](https://chulheeyun.github.io/publication/oh2023provable/)]

* **On the Pitfall of Mixup for Uncertainty Calibration**<br>
*Deng-Bao Wang, Lanqing Li, Peilin Zhao, Pheng-Ann Heng, Min-Ling Zhang*<br>
CVPR'2023 [[Paper](https://openaccess.thecvf.com/content/CVPR2023/papers/Wang_On_the_Pitfall_of_Mixup_for_Uncertainty_Calibration_CVPR_2023_paper.pdf)]

* **Understanding the Role of Mixup in Knowledge Distillation: An Empirical Study**<br>
*Hongjun Choi, Eun Som Jeon, Ankita Shukla, Pavan Turaga*<br>
WACV'2023 [[Paper](https://arxiv.org/abs/2211.03946)]
[[Code](https://github.com/hchoi71/mix-kd)]

* **Over-Training with Mixup May Hurt Generalization**<br>
*Zixuan Liu, Ziqiao Wang, Hongyu Guo, Yongyi Mao*<br>
ICLR'2023 [[Paper](https://openreview.net/forum?id=JmkjrlVE-DG)]

* **Analyzing Effects of Mixed Sample Data Augmentation on Model Interpretability**<br>
*Soyoun Won, Sung-Ho Bae, Seong Tae Kim*<br>
arXiv'2023 [[Paper](https://arxiv.org/abs/2303.14608)]

* **Selective Mixup Helps with Distribution Shifts, But Not (Only) because of Mixup**<br>
*Damien Teney, Jindong Wang, Ehsan Abbasnejad*<br>
ICML'2024 [[Paper](https://arxiv.org/abs/2305.16817)]

* **Pushing Boundaries: Mixup's Influence on Neural Collapse**<br>
*Quinn Fisher, Haoming Meng, Vardan Papyan*<br>
ICLR'2024 [[Paper](https://arxiv.org/abs/2402.06171)]

<p align="right">(<a href="#top">back to top</a>)</p>

## Survey

* **A survey on Image Data Augmentation for Deep Learning**<br>
*Connor Shorten and Taghi Khoshgoftaar*<br>
Journal of Big Data'2019 [[Paper](https://www.researchgate.net/publication/334279066_A_survey_on_Image_Data_Augmentation_for_Deep_Learning)]

* **An overview of mixing augmentation methods and augmentation strategies**<br>
*Dominik Lewy and Jacek Ma ́ndziuk*<br>
Artificial Intelligence Review'2022 [[Paper](https://link.springer.com/article/10.1007/s10462-022-10227-z)]

* **Image Data Augmentation for Deep Learning: A Survey**<br>
*Suorong Yang, Weikang Xiao, Mengcheng Zhang, Suhan Guo, Jian Zhao, Furao Shen*<br>
arXiv'2022 [[Paper](https://arxiv.org/abs/2204.08610)]

* **A Survey of Mix-based Data Augmentation: Taxonomy, Methods, Applications, and Explainability**<br>
*Chengtai Cao, Fan Zhou, Yurou Dai, Jianping Wang*<br>
arXiv'2022 [[Paper](https://arxiv.org/abs/2212.10888)]
[[Code](https://github.com/ChengtaiCao/Awesome-Mix)]

* **A Survey of Automated Data Augmentation for Image Classification: Learning to Compose, Mix, and Generate**<br>
*Tsz-Him Cheung, Dit-Yan Yeung*<br>
IEEE TNNLS'2023 [[Paper](https://ieeexplore.ieee.org/abstract/document/10158722)]

* **Survey: Image Mixing and Deleting for Data Augmentation**<br>
*Humza Naveed, Saeed Anwar, Munawar Hayat, Kashif Javed, Ajmal Mian*<br>
EAAI'2024 [[Paper](https://arxiv.org/abs/2106.07085)]

* **A Survey on Mixup Augmentations and Beyond**<br>
*Xin Jin, Hongyu Zhu, Siyuan Li, Zedong Wang, Zecheng Liu, Chang Yu, Huafeng Qin, Stan. Z. Li*<br>
arXiv'2024 [[Paper](https://arxiv.org/abs/2409.05202)]

## Benchmark

* **OpenMixup: A Comprehensive Mixup Benchmark for Visual Classification**<br>
*Siyuan Li, Zedong Wang, Zicheng Liu, Di Wu, Cheng Tan, Weiyang Jin, Stan Z. Li*<br>
arXiv'2024 [[Paper](https://arxiv.org/abs/2209.04851)]
[[Code](https://github.com/Westlake-AI/openmixup)]

<p align="right">(<a href="#top">back to top</a>)</p>

## Classification Results on Datasets

**Mixup methods classification results on general datasets: CIFAR10 \ CIFAR100, TinyImageNet, and ImageNet-1K. $(\cdot)$ denotes training epochs based on ResNet18 (R18), ResNet50 (R50), ResNeXt50 (RX50), PreActResNet18 (PreActR18), and Wide-ResNet28 (WRN28-10, WRN28-8).**

| Method   | Publish  | CIFAR10 | CIFAR100  | CIFAR100 | CIFAR100   | CIFAR100   | CIFAR100 | Tiny-ImageNet| Tiny-ImageNet | ImageNet-1K | ImageNet-1K |
|:--------:|:--------:|:-------:|:---------:|:--------:|:----------:|:----------:|:--------:|:------------:|:-------------:|:-----------:|:-----------:|
|          |          | R18     | R18       | RX50     | PreActR18  | WRN28-10   | WRN28-8  | R18          | RX50          | R18         | R50         |
| MixUp    | ICLR'2018| 96.62(800) | 79.12(800) | 82.10(800) | 78.90(200) | 82.50(200)  | 82.82(400) | 63.86(400) | 66.36(400) | 69.98(100) | 77.12(100) |
| CutMix   | ICCV'2019| 96.68(800) | 78.17(800) | 78.32(800) | 76.80(1200)| 83.40(200)  | 84.45(400) | 65.53(400) | 66.47(400) | 68.95(100) | 77.17(100) |
| Manifold Mixup | ICML'2019 | 96.71(800) | 80.35(800) | 82.88(800) | 79.66(1200) | 81.96(1200) | 83.24(400) | 64.15(400) | 67.30(400) | 69.98(100) | 77.01(100) |
| FMix     | arXiv'2020  | 96.18(800) | 79.69(800) | 79.02(800) | 79.85(200) | 82.03(200)  | 84.21(400) | 63.47(400) | 65.08(400) | 69.96(100) | 77.19(100) |
| SmoothMix | CVPRW'2020 | 96.17(800) | 78.69(800) | 78.95(800)  | - | - | 82.09(400) | - | - | - | 77.66(300) |
| GridMix  | PR'2020     | 96.56(800) | 78.72(800) | 78.90(800)  | - | - | 84.24(400) | 64.79(400) | - | - | - |
| ResizeMix | arXiv'2020 | 96.76(800) | 80.01(800) | 80.35(800)  | - | 85.23(200)  | 84.87(400) | 63.47(400) | 65.87(400) | 69.50(100) | 77.42(100) |
| SaliencyMix | ICLR'2021  | 96.20(800)   | 79.12(800)  | 78.77(800) | 80.31(300) | 83.44(200)  | 84.35(400) | 64.60(400) | 66.55(400) | 69.16(100) | 77.14(100) |
| Attentive-CutMix | ICASSP'2020 | 96.63(800)n| 78.91(800) | 80.54(800) | - | - | 84.34(400) | 64.01(400) | 66.84(400) | - | 77.46(100) |
| Saliency Grafting | AAAI'2022 | - | 80.83(800) | 83.10(800) | - | 84.68(300)  | - | 64.84(600) | 67.83(400) | - | 77.65(100) |
| PuzzleMix | ICML'2020 | 97.10(800) | 81.13(800) | 82.85(800) | 80.38(1200) | 84.05(200)  | 85.02(400) | 65.81(400) | 67.83(400) | 70.12(100) | 77.54(100) |
| Co-Mix | ICLR'2021 | 97.15(800) | 81.17(800) | 82.91(800) | 80.13(300) | - | 85.05(400) | 65.92(400) | 68.02(400) | - | 77.61(100) |
| SuperMix | CVPR'2021 | - | - | - | 79.07(2000) | 93.60(600)  | - | - | - | - | 77.60(600) |
| RecursiveMix | NIPS'2022 | - | 81.36(200) | - | 80.58(2000) | - | - | - | - | - | 79.20(300) |
| AutoMix | ECCV'2022 | 97.34(800) | 82.04(800) | 83.64(800) | - | - | 85.18(400) | 67.33(400) | 70.72(400) | 70.50(100) | 77.91(100) |
| SAMix | arXiv'2021 | 97.50(800) | 82.30(800) | 84.42(800) | - | - | 85.50(400) | 68.89(400) | 72.18(400) | 70.83(100) | 78.06(100) |
| AlignMixup | CVPR'2022 | - | - | - | 81.71(2000) | - | - | - | - | - | 78.00(100) |
| MultiMix | NIPS'2023 | - | - | - | 81.82(2000) | - | - | - | - | - | 78.81(300) |
| GuidedMixup | AAAI'2023 | - | - | - | 81.20(300) | 84.02(200)  | - | - | - | - | 77.53(100) |
| Catch-up Mix | AAAI'2023 | - | 82.10(400) | 83.56(400) | 82.24(2000) | - | - | 68.84(400) | - | - | 78.71(300) |
| LGCOAMix | TIP'2024 | - | 82.34(800) | 84.11(800) | - | - | - | 68.27(400) | 73.08(400) | - | - |
| AdAutoMix | ICLR'2024 | 97.55(800) | 82.32(800) | 84.42(800) | - | - | 85.32(400) | 69.19(400) | 72.89(400) | 70.86(100) | 78.04(100) |

**Mixup methods classification results on ImageNet-1K dataset use ViT-based models: DeiT, Swin Transformer (Swin), Pyramid Vision Transformer (PVT), and ConvNext trained 300 epochs.**

| Method     | Publish | ImageNet-1K | ImageNet-1K | ImageNet-1K | ImageNet-1K | ImageNet-1K | ImageNet-1K | ImageNet-1K |
|:----------:|:-------:|:-----------:|:-----------:|:-----------:|:-----------:|:-----------:|:-----------:|:-----------:|
|            |         | DieT-Tiny   | DieT-Small | DieT-Base | Swin-Tiny | PVT-Tiny | PVT-Small | ConvNeXt-Tiny |
| MixUp  | ICLR'2018 | 74.69 | 77.72 | 78.98 | 81.01 | 75.24 | 78.69 | 80.88 |
| CutMix | ICCV'2019 | 74.23 | 80.13 | 81.61 | 81.23 | 75.53 | 79.64 | 81.57 |
| FMix   | arXiv'2020 | 74.41 | 77.37 | - | 79.60 | 75.28 | 78.72 | 81.04 |
| ResizeMix | arXiv'2020 | 74.79 | 78.61 | 80.89 | 81.36 | 76.05 | 79.55 | 81.64 |
| SaliencyMix  | ICLR'2021 | 74.17 | 79.88 | 80.72 | 81.37 | 75.71 | 79.69 | 81.33 |
| Attentive-CutMix | ICASSP'2020 | 74.07 | 80.32 | 82.42 | 81.29 | 74.98 | 79.84 | 81.14 |
| PuzzleMix | ICML'2020 | 73.85 | 80.45 | 81.63 | 81.47 | 75.48 | 79.70 | 81.48 |
| AutoMix   | ECCV'2022 | 75.52 | 80.78 | 82.18 | 81.80 | 76.38 | 80.64 | 82.28 |
| SAMix     | arXiv'2021 | 75.83 | 80.94 | 82.85 | 81.87 | 76.60 | 80.78 | 82.35 |
| TransMix  | CVPR'2022 | 74.56 | 80.68 | 82.51 | 81.80 | 75.50 | 80.50 | - |
| TokenMix  | ECCV'2022 | 75.31 | 80.80 | 82.90 | 81.60 | 75.60 | - | 73.97 |
| TL-Align  | ICCV'2023 | 73.20 | 80.60 | 82.30 | 81.40 | 75.50 | 80.40 | - |
| SMMix     | ICCV'2023 | 75.56 | 81.10 | 82.90 | 81.80 | 75.60 | 81.03 | - |
| Mixpro    | ICLR'2023 | 73.80 | 81.30 | 82.90 | 82.80 | 76.70 | 81.20 | - |
| LUMix     | ICASSP'2024 | - | 80.60 | 80.20 | 81.70 | - | - | 82.50 |


<p align="right">(<a href="#top">back to top</a>)</p>


## Related Datasets Link

**Summary of datasets for mixup methods tasks. Link to dataset websites is provided.**

| Dataset | Type | Label | Task | Total data number | Link |
|:-------:|:----:|:-----:|:----:|:-----------------:|:----:|
| MINIST | Image | 10 | Classification | 70,000 | [MINIST](https://yann.lecun.com/exdb/mnist/) |
| Fashion-MNIST | Image | 10 | Classification | 70,000 | [Fashion-MINIST](https://github.com/zalandoresearch/fashion-mnist) |
| CIFAR10 | Image | 10 | Classification | 60,000 | [CIFAR10](https://www.cs.toronto.edu/~kriz/cifar.html) |
| CIFAR100 | Image | 100 | Classification | 60,000 | [CIFAR100](https://www.cs.toronto.edu/~kriz/cifar.html) |
| SVHN | Image | 10 | Classification | 630,420 | [SVHN](http://ufldl.stanford.edu/housenumbers/) |
| GTSRB | Image | 43 | Classification | 51,839 | [GTSRB](https://benchmark.ini.rub.de/gtsrb_dataset.html) |
| STL10 | Image | 10 | Classification | 113,000 | [STL10](https://cs.stanford.edu/~acoates/stl10/) |
| Tiny-ImageNet | Image | 200 | Classification | 100,000 | [Tiny-ImageNet](http://cs231n.stanford.edu/tiny-imagenet-200.zip) |
| ImageNet-1K | Image | 1,000 | Classification | 1,431,167 | [ImageNet-1K](https://image-net.org/challenges/LSVRC/2012/)|
| CUB-200-2011 | Image | 200 | Classification, Object Detection | 11,788 | [CUB-200-2011](https://www.vision.caltech.edu/datasets/cub_200_2011/) |
| FGVC-Aircraft | Image | 102 | Classification | 10,200 | [FGVC-Aircraft](https://www.robots.ox.ac.uk/~vgg/data/fgvc-aircraft/) |
| StanfordCars | Image | 196 | Classification | 16,185 | [StanfordCars](https://ai.stanford.edu/$/sim20jkrause/cars/car_dataset.html) |
| Oxford Flowers | Image | 102 | Classification | 8,189 | [Oxford Flowers](https://www.robots.ox.ac.uk/~vgg/data/flowers/102/) |
| Caltech101 | Image | 101 | Classification | 9,000 | [Caltech101](https://data.caltech.edu/records/mzrjq-6wc02) |
| SOP | Image | 22,634 | Classification | 120,053 | [SOP](https://cvgl.stanford.edu/projects/lifted_struct/) |
| Food-101 | Image | 101 | Classification | 101,000 | [Food-101](https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/) |
| SUN397 | Image | 899 | Classification | 130,519 | [SUN397](https://vision.princeton.edu/projects/2010/SUN//) |
| iNaturalist | Image | 5,089 | Classification | 675,170 | [iNaturalist](https://github.com/visipedia/inat_comp/tree/master/2017) |
| CIFAR-C | Image | 10,100 | Corruption Classification | 60,000 | [CIFAR-C](https://github.com/hendrycks/robustness/) |
| CIFAR-LT | Image | 10,100 | Long-tail Classification | 60,000 | [CIFAR-LT](https://github.com/hendrycks/robustness/) |
| ImageNet-1K-C | Image | 1,000 | Corruption Classification | 1,431,167 | [ImageNet-1K-C](https://github.com/hendrycks/robustness/) |
| ImageNet-A | Image | 200 | Classification | 7,500 | [ImageNet-A](https://github.com/hendrycks/natural-adv-examples) |
| Pascal VOC 102 | Image | 20 | Object Detection | 33,043 | [Pascal VOC 102](http://host.robots.ox.ac.uk/pascal/VOC/) |
| MS-COCO Detection | Image | 91 | Object Detection | 164,062 | [MS-COCO Detection](https://cocodataset.org/detection-eval) |
| DSprites | Image | 737,280*6 | Disentanglement | 737,280 | [DSprites](https://github.com/google-deepmind/dsprites-dataset) |
| Place205 | Image | 205 | Recognition | 2,500,000 | [Place205](http://places.csail.mit.edu/downloadData.html) |
| Pascal Context | Image | 459 | Segmentation | 10,103 | [Pascal Context](http://places.csail.mit.edu/downloadData.html) |
| ADE20K | Image | 3,169 | Segmentation | 25,210 | [ADE20K](https://groups.csail.mit.edu/vision/datasets/ADE20K/) |
| Cityscapes | Image | 19 | Segmentation | 5,000 | [Cityscapes](https://deepmind.google/) |
| StreetHazards | Image | 12 | Segmentation | 7,656 | [StreetHazards](https://www.v7labs.com/open-datasets/streethazards-dataset) |
| PACS | Image | 7*4 | Domain Classification | 9,991 | [PACS](https://domaingeneralization.github.io/) |
| BRACS | Medical Image | 7 | Classification | 4,539 | [BRACS](https://www.bracs.icar.cnr.it/) |
| BACH | Medical Image | 4 | Classification | 400 | [BACH](https://iciar2018-challenge.grand-challenge.org/) |
| CAME-Lyon16 | Medical Image   | 2 | Anomaly Detection | 360 | [CAME-Lyon16](https://camelyon16.grand-challenge.org/) |
| Chest X-Ray | Medical Image   | 2 | Anomaly Detection | 5,856 | [Chest X-Ray](https://data.mendeley.com/datasets/rscbjbr9sj/2) |
| BCCD | Medical Image | 4,888 | Object Detection | 364 | [BCCD](https://github.com/Shenggan/BCCD_Dataset) |
| TJU600 | Palm-Vein Image | 600 | Classification | 12,000 | [TJU600](https://cslinzhang.github.io/ContactlessPalm/) |
| VERA220 | Palm-Vein Image | 220 | Classification | 2,200 | [VERA220](https://www.idiap.ch/en/scientific-research/data/vera-palmvein) |
| CoNLL2003 | Text | 4 | Classification | 2,302 | [CoNLL2003](https://data.deepai.org/conll2003.zip) |
| 20 Newsgroups | Text | 20 | OOD Detection | 20,000 | [20 Newsgroups](http://qwone.com/~jason/20Newsgroups/) |
| WOS | Text | 134 | OOD Detection | 46,985 | [WOS](http://archive.ics.uci.edu/index.php) |
| SST-2 | Text | 2 | Sentiment Understanding | 68,800 | [SST-2](https://github.com/YJiangcm/SST-2-sentiment-analysis) |
| Cora | Graph | 7 | Node Classification | 2,708 | [Cora](https://github.com/phanein/deepwalk) |
| Citeseer | Graph | 6 | Node Classification | 3,312 | [Citeseer](https://csxstatic.ist.psu.edu/) |
| PubMed | Graph | 3 | Node Classification | 19,717 | [PubMed](https://pubmed.ncbi.nlm.nih.gov) |
| BlogCatalog | Graph | 39 | Node Classification | 10,312 | [BlogCatalog](https://figshare.com/articles/dataset/BlogCatalog_dataset/11923611?file=22349970) |
| Google Commands | Speech | 30 | Classification | 65,000 | [Google Commands](https://research.google/blog/launching-the-speech-commands-dataset/) |
| VoxCeleb2 | Speech | 6,112 | Sound Classification | 1,000,000+ | [VoxCeleb2](https://www.robots.ox.ac.uk/~vgg/data/voxceleb/) |
| VCTK | Speech | 110 | Enhancement | 44,000 | [VCTK](https://datashare.ed.ac.uk/handle/10283/2791) |
| ModelNet40 | 3D Point Cloud  | 40 | Classification | 12,311 | [ModelNet40](https://modelnet.cs.princeton.edu/) |
| ScanObjectNN | 3D Point Cloud  | 15 | Classification | 15,000 | [ScanObjectNN](https://hkust-vgd.github.io/scanobjectnn/) |
| ShapeNet | 3D Point Cloud  | 16 | Recognition, Classification | 16,880 | [ShapeNet](https://shapenet.org/) |
| KITTI360 | 3D Point Cloud  | 80,256 | Detection, Segmentation | 14,999 | [KITTI360](https://www.cvlibs.net/datasets/kitti/) |
| UCF101 | Video | 101 | Action Recognition | 13,320 | [UCF101](https://www.crcv.ucf.edu/research/data-sets/ucf101/) |
| Kinetics400 | Video | 400 | Action Recognition | 260,000 | [Kinetics400](https://deepmind.google/) |
| Airfoil | Tabular | - | Regression | 1,503 | [Airfoil](https://archive.ics.uci.edu/dataset/291/airfoil+self+noise) |
| NO2 | Tabular | - | Regression | 500 | [NO2](https://drive.google.com/drive/folders/1pTRT7fA-hq6p1F7ZX5oJ0tg_I1RRG6OW) |
| Exchange-Rate | Timeseries | - | Regression | 7,409 | [Exchange-Rate](https://github.com/laiguokun/multivariate-time-series-data) |
| Electricity | Timeseries | - | Regression | 26,113 | [Electricity](https://github.com/laiguokun/multivariate-time-series-data) |

<p align="right">(<a href="#top">back to top</a>)</p>

## Contribution

Feel free to send [pull requests](https://github.com/Westlake-AI/openmixup/pulls) to add more links with the following Markdown format. Note that the abbreviation, the code link, and the figure link are optional attributes.

```markdown
* **TITLE**<br>
*AUTHER*<br>
PUBLISH'YEAR [[Paper](link)] [[Code](link)]
   <details close>
   <summary>ABBREVIATION Framework</summary>
   <p align="center"><img width="90%" src="link_to_image" /></p>
   </details>
```

## Citation

If you feel that our work has contributed to your research, please cite it, thanks. 🥰

```markdown
@article{jin2024survey,
  title={A Survey on Mixup Augmentations and Beyond},
  author={Jin, Xin and Zhu, Hongyu and Li, Siyuan and Wang, Zedong and Liu, Zicheng and Yu, Chang and Qin, Huafeng and Li, Stan Z},
  journal={arXiv preprint arXiv:2409.05202},
  year={2024}
}
```

Current contributors include: Siyuan Li ([@Lupin1998](https://github.com/Lupin1998)), Xin Jin ([@JinXins](https://github.com/JinXins)), Zicheng Liu ([@pone7](https://github.com/pone7)), and Zedong Wang ([@Jacky1128](https://github.com/Jacky1128)). We thank all contributors for `Awesome-Mixup`!

<p align="right">(<a href="#top">back to top</a>)</p>

## License

This project is released under the [Apache 2.0 license](LICENSE).

## Acknowledgement

This repository is built using the [OpenMixup](https://github.com/Westlake-AI/openmixup) library and [Awesome README](https://github.com/matiassingers/awesome-readme) repository.

## Related Project

- [OpenMixup](https://github.com/Westlake-AI/openmixup): CAIRI Supervised, Semi- and Self-Supervised Visual Representation Learning Toolbox and Benchmark.
- [Awesome-Mix](https://github.com/ChengtaiCao/Awesome-Mix): An awesome list of papers for `A Survey of Mix-based Data Augmentation: Taxonomy, Methods, Applications, and Explainability, we categorize them based on our proposed taxonomy`.
- [survery-image-mixing-and-deleting-for-data-augmentation](https://github.com/humza909/survery-image-mixing-and-deleting-for-data-augmentation): An awesome list of papers for `Survey: Image Mixing and Deleting for Data Augmentation`.
- [awesome-mixup](https://github.com/demoleiwang/awesome-mixup): A collection of awesome papers about mixup.
- [awesome-mixed-sample-data-augmentation](https://github.com/JasonZhang156/awesome-mixed-sample-data-augmentation): A collection of awesome things about mixed sample data augmentation.
- [data-augmentation-review](https://github.com/AgaMiko/data-augmentation-review): List of useful data augmentation resources.
- [Awesome-Mixup](https://arxiv.org/abs/2409.05202): An awesome list of papers for `A Survey on Mixup Augmentations and Beyond`.
