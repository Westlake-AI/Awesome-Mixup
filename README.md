# Awesome-Mixup

 [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) ![GitHub stars](https://img.shields.io/github/stars/Westlake-AI/Awesome-Mixup?color=green) ![GitHub forks](https://img.shields.io/github/forks/Westlake-AI/Awesome-Mixup?color=yellow&label=Fork) ![visitors](https://visitor-badge.glitch.me/badge?page_id=Westlake-AI/Awesome-Mixup)

## Introduction

**We summarize awesome mixup data augmentation methods for visual representation learning in various scenarios.**

The list of awesome mixup augmentation methods is summarized in chronological order and is on updating. The main branch is modified according to [Awesome-Mixup](https://github.com/Westlake-AI/openmixup/docs/en/awesome_mixups) in [OpenMixup](https://github.com/Westlake-AI/openmixup), and we will add more papers according to [Awesome-Mix](https://github.com/ChengtaiCao/Awesome-Mix). We first summarize fundermental mixup methods from two aspects: *sample mixup policy* and *label mixup policy*. Then, we summarize mixup techniques used in downstream tasks.

* To find related papers and their relationships, check out [Connected Papers](https://www.connectedpapers.com/), which visualizes the academic field in a graph representation.
* To export BibTeX citations of papers, check out [ArXiv](https://arxiv.org/) or [Semantic Scholar](https://www.semanticscholar.org/) of the paper for professional reference formats.

## Table of Contents

- [Awesome-Mixup](#awesome-mixup)
  - [Introduction](#introduction)
  - [Table of Contents](#table-of-contents)
  - [Fundermental Methods](#fundermental-methods)
    - [Sample Mixup Methods](#sample-mixup-methods)
      - [**Pre-defined Policies**](#pre-defined-policies)
      - [**Saliency-guided Policies**](#saliency-guided-policies)
    - [Label Mixup Methods](#label-mixup-methods)
  - [Mixup for Self-supervised Learning](#mixup-for-self-supervised-learning)
  - [Mixup for Semi-supervised Learning](#mixup-for-semi-supervised-learning)
  - [Analysis of Mixup](#analysis-of-mixup)
  - [Natural Language Processing](#natural-language-processing)
  - [Survey](#survey)
  - [Contribution](#contribution)
  - [License](#license)
  - [Acknowledgement](#acknowledgement)
  - [Related Project](#related-project)


## Fundermental Methods

### Sample Mixup Methods

#### **Pre-defined Policies**

* **MixUp**: Hongyi Zhang, Moustapha Cisse, Yann N. Dauphin, David Lopez-Paz.
   - mixup: Beyond Empirical Risk Minimization. [[ICLR'2018](https://arxiv.org/abs/1710.09412)] [[code](https://github.com/facebookresearch/mixup-cifar10)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204561478-80b77110-21a4-480f-b369-d2f0656b5382.png" /></p>
* **BC**: Yuji Tokozume, Yoshitaka Ushiku, Tatsuya Harada.
   - Between-class Learning for Image Classification. [[CVPR'2018](https://arxiv.org/abs/1711.10284)] [[code](https://github.com/mil-tokyo/bc_learning_image)]
   <p align="center"><img width="70%" src="https://user-images.githubusercontent.com/44519745/204563476-15e638ad-6c25-4ab6-9bb6-4c5be74c625f.png" /></p>
* **AdaMixup**: Hongyu Guo, Yongyi Mao, Richong Zhang.
   - MixUp as Locally Linear Out-Of-Manifold Regularization. [[AAAI'2019](https://arxiv.org/abs/1809.02499)]
   <p align="center"><img width="85%" src="https://user-images.githubusercontent.com/44519745/204563766-4a49b4d9-fb1e-46d7-8443-bff37a527ee1.png" /></p>
* **CutMix**: Sangdoo Yun, Dongyoon Han, Seong Joon Oh, Sanghyuk Chun, Junsuk Choe, Youngjoon Yoo.
   - CutMix: Regularization Strategy to Train Strong Classifiers with Localizable Features. [[ICCV'2019](https://arxiv.org/abs/1905.04899)] [[code](https://github.com/clovaai/CutMix-PyTorch)]
   <p align="center"><img width="75%" src="https://user-images.githubusercontent.com/44519745/204564166-49707535-43f9-4d15-af89-d1a5a302db24.png" /></p>
* **ManifoldMix**: Vikas Verma, Alex Lamb, Christopher Beckham, Amir Najafi, Ioannis Mitliagkas, David Lopez-Paz, Yoshua Bengio.
   - Manifold Mixup: Better Representations by Interpolating Hidden States. [[ICML'2019](https://arxiv.org/abs/1806.05236)] [[code](https://github.com/vikasverma1077/manifold_mixup)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204565193-c5416185-ed98-4b86-bc7c-f5b6cc2f839b.png" /></p>
* **MixedExamples**: Cecilia Summers, Michael J. Dinneen.
   - Improved Mixed-Example Data Augmentation. [[WACV'2019](https://arxiv.org/abs/1805.11272)] [[code](https://github.com/ceciliaresearch/MixedExample)]
   <p align="center"><img width="70%" src="https://user-images.githubusercontent.com/44519745/232355479-8a53714f-5a6f-4c8e-b808-cc73f6d0f669.png" /></p>
* **FMix**: Ethan Harris, Antonia Marcu, Matthew Painter, Mahesan Niranjan, Adam Prügel-Bennett, Jonathon Hare.
   - FMix: Enhancing Mixed Sample Data Augmentation. [[Arixv'2020](https://arxiv.org/abs/2002.12047)] [[code](https://github.com/ecs-vlc/FMix)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204564909-8d20a405-141d-4fe6-ae72-581fc24222f8.png" /></p>
* **SmoothMix**: Jin-Ha Lee, Muhammad Zaigham Zaheer, Marcella Astrid, Seung-Ik Lee.
   - SmoothMix: a Simple Yet Effective Data Augmentation to Train Robust Classifiers. [[CVPRW'2020](https://openaccess.thecvf.com/content_CVPRW_2020/html/w45/Lee_SmoothMix_A_Simple_Yet_Effective_Data_Augmentation_to_Train_Robust_CVPRW_2020_paper.html)] [[code](https://github.com/Westlake-AI/openmixup)]
   <p align="center"><img width="75%" src="https://user-images.githubusercontent.com/44519745/204565814-fd528402-2a57-482b-b608-1ee3096984b0.png" /></p>
* **PatchUp**: Mojtaba Faramarzi, Mohammad Amini, Akilesh Badrinaaraayanan, Vikas Verma, Sarath Chandar.
   - PatchUp: A Regularization Technique for Convolutional Neural Networks. [[Arxiv'2020](https://arxiv.org/abs/2006.07794)] [[code](https://github.com/chandar-lab/PatchUp)]
   <p align="center"><img width="95%" src="https://user-images.githubusercontent.com/44519745/204566319-f2c67e8a-c10b-4ede-a57f-8c6ddf85e013.png" /></p>
* **GridMixup**: Kyungjune Baek, Duhyeon Bang, Hyunjung Shim.
   - GridMix: Strong regularization through local context mapping. [[Pattern Recognition'2021](https://www.sciencedirect.com/science/article/pii/S0031320320303976)] [[code](https://github.com/IlyaDobrynin/GridMixup)]
   <p align="center"><img width="95%" src="https://user-images.githubusercontent.com/44519745/204566566-b345e409-da4a-4f3b-b1bd-43e7c767d26a.png" /></p>
* **ResizeMix**: Jie Qin, Jiemin Fang, Qian Zhang, Wenyu Liu, Xingang Wang, Xinggang Wang.
   - ResizeMix: Mixing Data with Preserved Object Information and True Labels. [[Arixv'2020](https://arxiv.org/abs/2012.11101)] [[code](https://github.com/Westlake-AI/openmixup)]
   <p align="center"><img width="55%" src="https://user-images.githubusercontent.com/44519745/204566840-69782b04-4645-41b3-a6eb-428977c63881.png" /></p>
* **FocusMix**: Jiyeon Kim, Ik-Hee Shin, Jong-Ryul, Lee, Yong-Ju Lee.
   - Where to Cut and Paste: Data Regularization with Selective Features. [[ICTC'2020](https://ieeexplore.ieee.org/abstract/document/9289404)]
* **AugMix**: Dan Hendrycks, Norman Mu, Ekin D. Cubuk, Barret Zoph, Justin Gilmer, Balaji Lakshminarayanan.
   - AugMix: A Simple Data Processing Method to Improve Robustness and Uncertainty. [[ICLR'2020](https://arxiv.org/abs/1912.02781)] [[code](https://github.com/google-research/augmix)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204567137-f71b0437-9267-4f99-b7dc-911ffa4f8b73.png" /></p>
* **DJMix**: Ryuichiro Hataya, Hideki Nakayama.
   - DJMix: Unsupervised Task-agnostic Augmentation for Improving Robustness. [[Arxiv'2021](https://openreview.net/pdf?id=0n3BaVlNsHI)]
   <p align="center"><img width="80%" src="https://user-images.githubusercontent.com/44519745/204567516-3d058e8c-4232-4af4-b7a8-efa3a1298a1b.png" /></p>
* **PixMix**: Dan Hendrycks, Andy Zou, Mantas Mazeika, Leonard Tang, Bo Li, Dawn Song, Jacob Steinhardt.
   - PixMix: Dreamlike Pictures Comprehensively Improve Safety Measures. [[Arxiv'2021](https://arxiv.org/abs/2112.05135)] [[code](https://github.com/andyzoujm/pixmix)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204567828-b434c118-0be1-475d-a0f3-9834e39b4507.png" /></p>
* **StyleMix**: Minui Hong, Jinwoo Choi, Gunhee Kim.
   - StyleMix: Separating Content and Style for Enhanced Data Augmentation. [[CVPR'2021](https://openaccess.thecvf.com/content/CVPR2021/papers/Hong_StyleMix_Separating_Content_and_Style_for_Enhanced_Data_Augmentation_CVPR_2021_paper.pdf)] [[code](https://github.com/alsdml/StyleMix)]
   <p align="center"><img width="65%" src="https://user-images.githubusercontent.com/44519745/204567999-6d0263c2-111c-4335-92b5-66486bb0fea0.png" /></p>
* **MixStyle**: Kaiyang Zhou, Yongxin Yang, Yu Qiao, Tao Xiang.
   - Domain Generalization with MixStyle. [[ICLR'2021](https://openreview.net/forum?id=6xHJ37MVxxp)] [[code](https://github.com/KaiyangZhou/mixstyle-release)]
   <p align="center"><img width="80%" src="https://user-images.githubusercontent.com/44519745/204568994-eb45528e-e83b-4ac5-bed9-642da987ec89.png" /></p>
* **MoEx**: Boyi Li, Felix Wu, Ser-Nam Lim, Serge Belongie, Kilian Q. Weinberger.
   - On Feature Normalization and Data Augmentation. [[CVPR'2021](https://arxiv.org/abs/2002.11102)] [[code](https://github.com/Boyiliee/MoEx)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204569196-3641255a-56f3-407a-986a-209b5c7eeff6.png" /></p>
* **GIF**: Chen Chen, Jingfeng Zhang, Xilie Xu, Tianlei Hu, Gang Niu, Gang Chen, Masashi Sugiyama.
   - Guided Interpolation for Adversarial Training. [[ArXiv'2021](https://arxiv.org/abs/2102.07327)]
   <p align="center"><img width="85%" src="https://user-images.githubusercontent.com/44519745/230494660-e99cf522-8fd7-4aa4-a4e4-d0385f82d032.png" /></p>
* **DCutMix**: Joonhyun Jeong, Sungmin Cha, Youngjoon Yoo, Sangdoo Yun, Taesup Moon, Jongwon Choi.
   - Observations on K-image Expansion of Image-Mixing Augmentation for Classification. [[IEEE Access'2021](https://arxiv.org/abs/2110.04248)] [[code](https://github.com/yjyoo3312/DCutMix-PyTorch)]
   <p align="center"><img width="75%" src="https://user-images.githubusercontent.com/44519745/230492924-e9008de1-913f-44f5-ac2e-3d21f07d1b7f.png" /></p>
* **NFM**: Soon Hoe Lim, N. Benjamin Erichson, Francisco Utrera, Winnie Xu, Michael W. Mahoney.
   - Noisy Feature Mixup. [[ICLR'2022](https://arxiv.org/abs/2110.02180)] [[code](https://github.com/erichson/NFM)]
   <p align="center"><img width="45%" src="https://user-images.githubusercontent.com/44519745/204569704-7de07797-b607-4750-9a46-c4387a539ac0.png" /></p>
* **LocalMix**: Raphael Baena, Lucas Drumetz, Vincent Gripon.
   - Preventing Manifold Intrusion with Locality: Local Mixup. [[EUSIPCO'2022](https://arxiv.org/abs/2201.04368)] [[code](https://github.com/raphael-baena/Local-Mixup)]
   <p align="center"><img width="85%" src="https://user-images.githubusercontent.com/44519745/204570088-fdf2e115-caee-4808-bf2b-709ac27f2251.png" /></p>
* **RandomMix**: Xiaoliang Liu, Furao Shen, Jian Zhao, Changhai Nie.
   - RandomMix: A mixed sample data augmentation method with multiple mixed modes. [[ArXiv'2022](https://arxiv.org/abs/2205.08728)]
   <p align="center"><img width="70%" src="https://user-images.githubusercontent.com/44519745/204570320-2785207c-aced-4d94-a33e-98acfcbbaa3f.png" /></p>
* **SuperpixelGridCut**: Karim Hammoudi, Adnane Cabani, Bouthaina Slika, Halim Benhabiles, Fadi Dornaika, Mahmoud Melkemi.
   - SuperpixelGridCut, SuperpixelGridMean and SuperpixelGridMix Data Augmentation. [[ArXiv'2022](https://arxiv.org/abs/2204.08458)] [[code](https://github.com/hammoudiproject/SuperpixelGridMasks)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204570617-090cc5a7-508c-49e7-9e5f-df7ec018f540.png" /></p>
* **AugRmixAT**: Xiaoliang Liu, Furao Shen, Jian Zhao, Changhai Nie.
   - AugRmixAT: A Data Processing and Training Method for Improving Multiple Robustness and Generalization Performance. [[ICME'2022](https://arxiv.org/abs/2207.10290)]
   <p align="center"><img width="80%" src="https://user-images.githubusercontent.com/44519745/204571167-748828be-a1f6-46ac-bc13-37cccfa72515.png" /></p>
* **MSDA**: Chanwoo Park, Sangdoo Yun, Sanghyuk Chun.
   - A Unified Analysis of Mixed Sample Data Augmentation: A Loss Function Perspective. [[NIPS'2022](https://arxiv.org/abs/2208.09913)] [[code](https://github.com/naver-ai/hmix-gmix)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204571363-f0b1a960-54f9-4462-855d-59e90f284cfe.png" /></p>
* **RegMixup**: Francesco Pinto, Harry Yang, Ser-Nam Lim, Philip H.S. Torr, Puneet K. Dokania.
   - RegMixup: Mixup as a Regularizer Can Surprisingly Improve Accuracy and Out Distribution Robustness. [[NIPS'2022](https://arxiv.org/abs/2206.14502)] [[code](https://github.com/FrancescoPinto/RegMixup)]
   <p align="center"><img width="80%" src="https://user-images.githubusercontent.com/44519745/204571630-e8407bd7-ca27-44de-baca-5d88ca2004a6.png" /></p>

<p align="right">(<a href="#top">back to top</a>)</p>

#### **Saliency-guided Policies**

* **SaliencyMix**: A F M Shahab Uddin and Mst. Sirazam Monira and Wheemyung Shin and TaeChoong Chung and Sung-Ho Bae
   - SaliencyMix: A Saliency Guided Data Augmentation Strategy for Better Regularization. [[ICLR'2021](https://arxiv.org/abs/2006.01791)] [[code](https://github.com/SaliencyMix/SaliencyMix)]
   <p align="center"><img width="95%" src="https://user-images.githubusercontent.com/44519745/204571915-624d3e5e-7678-4ba3-a08c-09ca2741bf72.png" /></p>
* **AttentiveMix**: Devesh Walawalkar, Zhiqiang Shen, Zechun Liu, Marios Savvides.
   - Attentive CutMix: An Enhanced Data Augmentation Approach for Deep Learning Based Image Classification. [[ICASSP'2020](https://arxiv.org/abs/2003.13048)] [[code](https://github.com/xden2331/attentive_cutmix)]
   <p align="center"><img width="75%" src="https://user-images.githubusercontent.com/44519745/204572493-a8c816c9-2be5-43b6-bf35-580cfab8716f.png" /></p>
* **SnapMix**: Shaoli Huang, Xinchao Wang, Dacheng Tao.
   - SnapMix: Semantically Proportional Mixing for Augmenting Fine-grained Data. [[AAAI'2021](https://arxiv.org/abs/2012.04846)] [[code](https://github.com/Shaoli-Huang/SnapMix)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204572296-2035c6b4-c477-4484-a8e6-7ad9ad415045.png" /></p>
* **AttributeMix**: Hao Li, Xiaopeng Zhang, Hongkai Xiong, Qi Tian.
   - Attribute Mix: Semantic Data Augmentation for Fine Grained Recognition. [[VCIP'2020](https://arxiv.org/abs/2004.02684)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204573220-13a3b90e-73f8-4277-a997-67dddb15dd1c.png" /></p>
* **AMR**: Christopher Beckham, Sina Honari, Vikas Verma, Alex Lamb, Farnoosh Ghadiri, R Devon Hjelm, Yoshua Bengio, Christopher Pal.
   - On Adversarial Mixup Resynthesis. [[NIPS'2019](https://arxiv.org/abs/1903.02709)] [[code](https://github.com/christopher-beckham/amr)]
   <p align="center"><img width="70%" src="https://user-images.githubusercontent.com/44519745/232315897-2a5fb2c5-d0ce-4c01-b6cd-21ec54bd9e49.png" /></p>
* **AutoMix**: Jianchao Zhu, Liangliang Shi, Junchi Yan, Hongyuan Zha.
   - AutoMix: Mixup Networks for Sample Interpolation via Cooperative Barycenter Learning. [[ECCV'2020](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123550630.pdf)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204572771-e09246ca-b88b-4755-8d8a-f99053244610.png" /></p>
* **Pani VAT**: Ke Sun, Bing Yu, Zhouchen Lin, Zhanxing Zhu.
   - Patch-level Neighborhood Interpolation: A General and Effective Graph-based Regularization Strategy. [[ArXiv'2019](https://arxiv.org/abs/1911.09307)]
   <p align="center"><img width="80%" src="https://user-images.githubusercontent.com/44519745/204572993-8b3fa627-8c36-4763-a2a6-c9a90c5f0fc2.png" /></p>
* **PuzzleMix**: Jang-Hyun Kim, Wonho Choo, Hyun Oh Song.
   - Puzzle Mix: Exploiting Saliency and Local Statistics for Optimal Mixup. [[ICML'2020](https://arxiv.org/abs/2009.06962)] [[code](https://github.com/snu-mllab/PuzzleMix)]
   <p align="center"><img width="85%" src="https://user-images.githubusercontent.com/44519745/204573527-75f28e86-9b0e-4b14-bd21-ef89de52dd5f.png" /></p>
* **CoMixup**: Jang-Hyun Kim, Wonho Choo, Hosan Jeong, Hyun Oh Song.
   - Co-Mixup: Saliency Guided Joint Mixup with Supermodular Diversity. [[ICLR'2021](https://arxiv.org/abs/2102.03065)] [[code](https://github.com/snu-mllab/Co-Mixup)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204573653-68ce31e8-fa01-4cf8-9493-c2311fd99e13.png" /></p>
* **SuperMix**: Ali Dabouei, Sobhan Soleymani, Fariborz Taherkhani, Nasser M. Nasrabadi.
   - SuperMix: Supervising the Mixing Data Augmentation. [[CVPR'2021](https://arxiv.org/abs/2003.05034)] [[code](https://github.com/alldbi/SuperMix)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204573912-47ae05f3-8d78-4ef7-b3a9-15d54bffa20a.png" /></p>
* **PatchMix**: Paola Cascante-Bonilla, Arshdeep Sekhon, Yanjun Qi, Vicente Ordonez.
   - Evolving Image Compositions for Feature Representation Learning. [[BMVC'2021](https://arxiv.org/abs/2106.09011)]
   <p align="center"><img width="95%" src="https://user-images.githubusercontent.com/44519745/204574267-8e53783d-ea54-4399-8c32-86c8ac2520bd.png" /></p>
* **StackMix**: John Chen, Samarth Sinha, Anastasios Kyrillidis.
   - StackMix: A complementary Mix algorithm. [[UAI'2022](https://arxiv.org/abs/2011.12618)]
   <p align="center"><img width="95%" src="https://user-images.githubusercontent.com/44519745/204574552-fb5e9865-86b0-4d51-977c-82a840d81a18.png" /></p>
* **SalfMix**: Jaehyeop Choi, Chaehyeon Lee, Donggyu Lee, Heechul Jung.
   - SalfMix: A Novel Single Image-Based Data Augmentation Technique Using a Saliency Map. [[Sensor'2021](https://pdfs.semanticscholar.org/1db9/c80edeed50858783c69237aeba764750e8b7.pdf?_ga=2.182064935.1813772674.1674154381-1810295069.1625160008)]
   <p align="center"><img width="80%" src="https://user-images.githubusercontent.com/44519745/213535188-5255eb4c-83c8-40ca-86b9-44459b84d9a8.png" /></p>
* **k-Mixup**: Kristjan Greenewald, Anming Gu, Mikhail Yurochkin, Justin Solomon, Edward Chien.
   - k-Mixup Regularization for Deep Learning via Optimal Transport. [[ArXiv'2021](https://arxiv.org/abs/2106.02933)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204569488-d4862400-3304-488d-ad24-06eff4e0c0b2.png" /></p>
* **AlignMix**: Shashanka Venkataramanan, Ewa Kijak, Laurent Amsaleg, Yannis Avrithis.
   - AlignMix: Improving representation by interpolating aligned features. [[CVPR'2022](https://arxiv.org/abs/2103.15375)] [[code](https://github.com/shashankvkt/AlignMixup_CVPR22)]
   <p align="center"><img width="95%" src="https://user-images.githubusercontent.com/44519745/204574666-fcb694b0-c6bf-438a-bbd0-020635fe4b51.png" /></p>
* **AutoMix**: Zicheng Liu, Siyuan Li, Di Wu, Zihan Liu, Zhiyuan Chen, Lirong Wu, Stan Z. Li.
   - AutoMix: Unveiling the Power of Mixup for Stronger Classifiers. [[ECCV'2022](https://arxiv.org/abs/2103.13027)] [[code](https://github.com/Westlake-AI/openmixup)]
   <p align="center"><img width="95%" src="https://user-images.githubusercontent.com/44519745/174272662-19ce57ad-7b08-4e73-81b1-3bb81fee2fe5.png" /></p>
* **SAMix**: Siyuan Li, Zicheng Liu, Di Wu, Zihan Liu, Stan Z. Li.
   - Boosting Discriminative Visual Representation Learning with Scenario-Agnostic Mixup. [[Arxiv'2021](https://arxiv.org/abs/2111.15454)] [[code](https://github.com/Westlake-AI/openmixup)]
   <p align="center"><img width="80%" src="https://user-images.githubusercontent.com/44519745/174272657-fb662377-b7c3-4faa-8d9b-ea6f1e08549e.png" /></p>
* **ScoreMix**: Thomas Stegmüller, Behzad Bozorgtabar, Antoine Spahr, Jean-Philippe Thiran.
   - ScoreNet: Learning Non-Uniform Attention and Augmentation for Transformer-Based Histopathological Image Classification. [[Arxiv'2022](https://arxiv.org/abs/2202.07570)]
   <p align="center"><img width="95%" src="https://user-images.githubusercontent.com/44519745/204576297-e97ea9c4-ee17-4ec3-a672-3f088ededb72.png" /></p>
* **RecursiveMix**: Lingfeng Yang, Xiang Li, Borui Zhao, Renjie Song, Jian Yang.
   - RecursiveMix: Mixed Learning with History. [[NIPS'2022](https://arxiv.org/abs/2203.06844)] [[code](https://github.com/implus/RecursiveMix-pytorch)]
   <p align="center"><img width="95%" src="https://user-images.githubusercontent.com/44519745/204576092-5fd92410-c12a-4691-8f7b-01901445f2a4.png" /></p>
* **SciMix** Rémy Sun, Clément Masson, Gilles Hénaff, Nicolas Thome, Matthieu Cord.
   - Swapping Semantic Contents for Mixing Images. [[ICPR'2022](https://arxiv.org/abs/2205.10158)]
   <p align="center"><img width="85%" src="https://user-images.githubusercontent.com/44519745/204575557-ddc6644e-a5e4-49ae-a95d-59856cc99a25.png" /></p>
* **TransformMix** Tsz-Him Cheung, Dit-Yan Yeung.
   - TransformMix: Learning Transformation and Mixing Strategies for Sample-mixing Data Augmentation. [[OpenReview'2022](https://openreview.net/forum?id=-1vpxBUtP0B)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204575385-0b2d7470-0ffd-4b6b-977b-ef28b1617954.png" /></p>
* **R-Mix and RL-Mix**: Minh-Long Luu, Zeyi Huang, Eric P.Xing, Yong Jae Lee, Haohan Wang.
   - Expeditious Saliency-guided Mix-up through Random Gradient Thresholding. [[2nd Practical-DL Workshop @ AAAI'23](https://arxiv.org/abs/2212.04875)] [[code](https://github.com/minhlong94/Random-Mixup)]
   <p align="center"><img width="85%" src="https://raw.githubusercontent.com/minhlong94/Random-Mixup/main/assets/Mixups.png" /></p>
* **MixPro** Qihao Zhao, Yangyu Huang, Wei Hu, Fan Zhang, Jun Liu.
   - MixPro: Data Augmentation with MaskMix and Progressive Attention Labeling for Vision Transformer. [[ICLR'2023](https://openreview.net/forum?id=dRjWsd3gwsm)]
   <p align="center"><img width="85%" src="https://user-images.githubusercontent.com/44519745/224795935-afb936b2-fc77-4018-a681-72887f96fa59.png" /></p>
* **SMMix** Mengzhao Chen, Mingbao Lin, ZhiHang Lin, Yuxin Zhang, Fei Chao, Rongrong Ji.
   - SMMix: Self-Motivated Image Mixing for Vision Transformers. [[Arxiv'2022](https://arxiv.org/abs/2212.12977)] [[code](https://github.com/chenmnz/smmix)]
   <p align="center"><img width="85%" src="https://user-images.githubusercontent.com/44519745/213537624-7359689e-b5af-4db1-a4ad-07876dd44089.png" /></p>
* **MultiMix** Shashanka Venkataramanan, Ewa Kijak, Laurent Amsaleg, Yannis Avrithis.
   - Teach me how to Interpolate a Myriad of Embeddings. [[Arxiv'2022](https://arxiv.org/abs/2206.14868)]
   <p align="center"><img width="85%" src="https://user-images.githubusercontent.com/44519745/224786198-a85b76b9-0f8b-434d-be59-bbc41438aac9.png" /></p>

<p align="right">(<a href="#top">back to top</a>)</p>

### Label Mixup Methods

* **MixUp**: Hongyi Zhang, Moustapha Cisse, Yann N. Dauphin, David Lopez-Paz.
   - mixup: Beyond Empirical Risk Minimization. [[ICLR'2018](https://arxiv.org/abs/1710.09412)] [[code](https://github.com/facebookresearch/mixup-cifar10)]
* **CutMix**: Sangdoo Yun, Dongyoon Han, Seong Joon Oh, Sanghyuk Chun, Junsuk Choe, Youngjoon Yoo.
   - CutMix: Regularization Strategy to Train Strong Classifiers with Localizable Features. [[ICCV'2019](https://arxiv.org/abs/1905.04899)] [[code](https://github.com/clovaai/CutMix-PyTorch)]
* **MetaMixup**: Zhijun Mai, Guosheng Hu, Dexiong Chen, Fumin Shen, Heng Tao Shen.
   - Metamixup: Learning adaptive interpolation policy of mixup with metalearning. [[TNNLS'2021](https://arxiv.org/abs/1908.10059)]
   <p align="center"><img width="70%" src="https://user-images.githubusercontent.com/44519745/204576802-4aa83a66-61ac-40fd-8904-3b4f9eda62ef.png" /></p>
* **mWH**: Hao Yu, Huanyu Wang, Jianxin Wu.
   - Mixup Without Hesitation. [[ICIG'2022](https://arxiv.org/abs/2101.04342)] [[code](https://github.com/yuhao318/mwh)]
* **CAMixup**: Yeming Wen, Ghassen Jerfel, Rafael Muller, Michael W. Dusenberry, Jasper Snoek, Balaji Lakshminarayanan, Dustin Tran.
   - Combining Ensembles and Data Augmentation can Harm your Calibration. [[ICLR'2021](https://arxiv.org/abs/2010.09875)] [[code](https://github.com/google/edward2/tree/main/experimental/marginalization_mixup)]
   <p align="center"><img width="85%" src="https://user-images.githubusercontent.com/44519745/204577092-06b2c74a-47cc-44f5-8423-9f37b1d0cbdc.png" /></p>
* **TokenLabeling**: Zihang Jiang, Qibin Hou, Li Yuan, Daquan Zhou, Yujun Shi, Xiaojie Jin, Anran Wang, Jiashi Feng.
   - Combining Ensembles and Data Augmentation can Harm your Calibration. [[NIPS'2021](https://arxiv.org/abs/2104.10858)] [[code](https://github.com/zihangJiang/TokenLabeling)]
   <p align="center"><img width="80%" src="https://user-images.githubusercontent.com/44519745/204577372-f679ab10-a65f-4319-9a40-8393c20ad0fa.png" /></p>
* **Saliency Grafting**: Joonhyung Park, June Yong Yang, Jinwoo Shin, Sung Ju Hwang, Eunho Yang.
   - Saliency Grafting: Innocuous Attribution-Guided Mixup with Calibrated Label Mixing. [[AAAI'2022](https://arxiv.org/abs/2112.08796)]
   <p align="center"><img width="80%" src="https://user-images.githubusercontent.com/44519745/204577555-7ffe34ed-74c1-4dff-95e8-f5a9e385f50c.png" /></p>
* **TransMix**: Jie-Neng Chen, Shuyang Sun, Ju He, Philip Torr, Alan Yuille, Song Bai.
   - TransMix: Attend to Mix for Vision Transformers. [[CVPR'2022](https://arxiv.org/abs/2111.09833)] [[code](https://github.com/Beckschen/TransMix)]
   <p align="center"><img width="60%" src="https://user-images.githubusercontent.com/44519745/204577728-8d59ad5f-0204-4943-aae7-dca6c48022ce.png" /></p>
* **GenLabel**: Jy-yong Sohn, Liang Shang, Hongxu Chen, Jaekyun Moon, Dimitris Papailiopoulos, Kangwook Lee.
   - GenLabel: Mixup Relabeling using Generative Models. [[ArXiv'2022](https://arxiv.org/abs/2201.02354)]
   <p align="center"><img width="85%" src="https://user-images.githubusercontent.com/44519745/204578083-3212ed98-6f1b-422b-8764-0276a65bce8e.png" /></p>
* **DecoupleMix**: Zicheng Liu, Siyuan Li, Ge Wang, Cheng Tan, Lirong Wu, Stan Z. Li.
   - Decoupled Mixup for Data-efficient Learning. [[Arxiv'2022](https://arxiv.org/abs/2203.10761)] [[code](https://github.com/Westlake-AI/openmixup)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204578387-4be9567c-963a-4d2d-8c1f-c7c5ade527b8.png" /></p>
* **TokenMix**: Jihao Liu, Boxiao Liu, Hang Zhou, Hongsheng Li, Yu Liu.
   - TokenMix: Rethinking Image Mixing for Data Augmentation in Vision Transformers. [[ECCV'2022](https://arxiv.org/abs/2207.08409)] [[code](https://github.com/Sense-X/TokenMix)]
   <p align="center"><img width="70%" src="https://user-images.githubusercontent.com/44519745/204578736-7b2dd349-7214-4d49-ade8-30b1caa2f1ea.png" /></p>
* **GDPMix**: Donghao Li, Yang Cao, Yuan Yao.
   - Optimizing Random Mixup with Gaussian Differential Privacy. [[arXiv'2022](https://arxiv.org/abs/2202.06467)]
* **TokenMixup**: Hyeong Kyu Choi, Joonmyung Choi, Hyunwoo J. Kim.
   - TokenMixup: Efficient Attention-guided Token-level Data Augmentation for Transformers. [[NIPS'2022](https://arxiv.org/abs/2210.07562)] [[code](https://github.com/mlvlab/TokenMixup)]
   <p align="center"><img width="85%" src="https://user-images.githubusercontent.com/44519745/204578884-b9d7d466-b26b-4e4b-8a23-22199a6dca26.png" /></p>
* **TL-Align**: Han Xiao, Wenzhao Zheng, Zheng Zhu, Jie Zhou, Jiwen Lu.
   - Token-Label Alignment for Vision Transformers. [[arXiv'2022](https://arxiv.org/abs/2210.06455)] [[code](https://github.com/Euphoria16/TL-Align)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204579080-3b7c9352-8fb3-49bd-99f5-ce4f72d722d8.png" /></p>
* **LUMix**: Shuyang Sun, Jie-Neng Chen, Ruifei He, Alan Yuille, Philip Torr, Song Bai.
   - LUMix: Improving Mixup by Better Modelling Label Uncertainty. [[arXiv'2022](https://arxiv.org/abs/2211.15846)] [[code](https://github.com/kevin-ssy/LUMix)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/205531445-dc4b7790-e0b7-4c41-b9d2-708efa5e4198.png" /></p>
* **MixupE**: Vikas Verma, Sarthak Mittal, Wai Hoh Tang, Hieu Pham, Juho Kannala, Yoshua Bengio, Arno Solin, Kenji Kawaguchi.
   - MixupE: Understanding and Improving Mixup from Directional Derivative Perspective. [[arXiv'2022](https://arxiv.org/abs/2212.13381)]
   <p align="center"><img width="85%" src="https://user-images.githubusercontent.com/44519745/209991074-3dd41cdf-4e64-42e2-8bf4-ebc60e8212d0.png" /></p>

<p align="right">(<a href="#top">back to top</a>)</p>

## Mixup for Self-supervised Learning

* **MixCo**: Sungnyun Kim, Gihun Lee, Sangmin Bae, Se-Young Yun.
   - MixCo: Mix-up Contrastive Learning for Visual Representation. [[NIPSW'2020](https://arxiv.org/abs/2010.06300)] [[code](https://github.com/Lee-Gihun/MixCo-Mixup-Contrast)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204580767-c0730ac6-802f-40bc-92a8-4b7abe0acb99.png" /></p>
* **MoCHi**: Yannis Kalantidis, Mert Bulent Sariyildiz, Noe Pion, Philippe Weinzaepfel, Diane Larlus.
   - Hard Negative Mixing for Contrastive Learning. [[NIPS'2020](https://arxiv.org/abs/2010.01028)] [[code](https://europe.naverlabs.com/mochi)]
   <p align="center"><img width="40%" src="https://user-images.githubusercontent.com/44519745/204580935-80ebaaaa-2761-4da4-9b58-7755a0dc15c6.png" /></p>
* **i-Mix**: Kibok Lee, Yian Zhu, Kihyuk Sohn, Chun-Liang Li, Jinwoo Shin, Honglak Lee.
   - i-Mix A Domain-Agnostic Strategy for Contrastive Representation Learning. [[ICLR'2021](https://arxiv.org/abs/2010.08887)] [[code](https://github.com/kibok90/imix)]
   <p align="center"><img width="85%" src="https://user-images.githubusercontent.com/44519745/204581084-5460bd37-4adb-4f01-b7af-fc88ceb2683e.png" /></p>
* **Un-Mix**: Zhiqiang Shen, Zechun Liu, Zhuang Liu, Marios Savvides, Trevor Darrell, Eric Xing.
   - Un-Mix: Rethinking Image Mixtures for Unsupervised Visual Representation. [[AAAI'2022](https://arxiv.org/abs/2003.05438)] [[code](https://github.com/szq0214/Un-Mix)]
   <p align="center"><img width="75%" src="https://user-images.githubusercontent.com/44519745/204581434-dfbc11f8-e300-4dd7-bc84-adbe5a53dbf4.png" /></p>
* **BSIM**: Xiangxiang Chu, Xiaohang Zhan, Xiaolin Wei.
   - Beyond Single Instance Multi-view Unsupervised Representation Learning. [[BMVC'2022](https://arxiv.org/abs/2011.13356)]
   <p align="center"><img width="95%" src="https://user-images.githubusercontent.com/44519745/204581834-3ead412b-359c-40ba-86ea-3ab54ead2c96.png" /></p>
* **FT**: Rui Zhu, Bingchen Zhao, Jingen Liu, Zhenglong Sun, Chang Wen Chen.
   - Improving Contrastive Learning by Visualizing Feature Transformation. [[ICCV'2021](https://arxiv.org/abs/2108.02982)] [[code](https://github.com/DTennant/CL-Visualizing-Feature-Transformation)]
   <p align="center"><img width="80%" src="https://user-images.githubusercontent.com/44519745/204582514-426efca3-4e8b-48b8-b69a-ecebb94b7fa8.png" /></p>
* **PCEA**: Jingwei Liu, Yi Gu, Shentong Mo, Zhun Sun, Shumin Han, Jiafeng Guo, Xueqi Cheng.
   - Piecing and Chipping: An effective solution for the information-erasing view generation in Self-supervised Learning. [[OpenReview'2021](https://openreview.net/forum?id=DnG8f7gweH4)]
   <p align="center"><img width="75%" src="https://user-images.githubusercontent.com/44519745/204582781-b54c4472-67eb-4e78-9362-44b990bbafa3.png" /></p>
* **CoMix**: Aadarsh Sahoo, Rutav Shah, Rameswar Panda, Kate Saenko, Abir Das.
   - Contrast and Mix: Temporal Contrastive Video Domain Adaptation with Background Mixing. [[NIPS'2021](https://arxiv.org/abs/2011.02697)] [[code](https://cvir.github.io/projects/comix)]
   <p align="center"><img width="95%" src="https://user-images.githubusercontent.com/44519745/204583146-fc363695-6889-46cd-93f1-236bec9d5fb5.png" /></p>
* **SAMix**: Siyuan Li, Zicheng Liu, Di Wu, Zihan Liu, Stan Z. Li.
   - Boosting Discriminative Visual Representation Learning with Scenario-Agnostic Mixup. [[Arxiv'2021](https://arxiv.org/abs/2111.15454)] [[code](https://github.com/Westlake-AI/openmixup)]
   <p align="center"><img width="80%" src="https://user-images.githubusercontent.com/44519745/174272657-fb662377-b7c3-4faa-8d9b-ea6f1e08549e.png" /></p>
* **MixSiam**: Xiaoyang Guo, Tianhao Zhao, Yutian Lin, Bo Du.
   - MixSiam: A Mixture-based Approach to Self-supervised Representation Learning. [[OpenReview'2021](https://arxiv.org/abs/2111.02679)]
   <p align="center"><img width="60%" src="https://user-images.githubusercontent.com/44519745/204583448-8c1890fd-ce95-488a-9570-f7393a4d140a.png" /></p>
* **MixSSL**: Yichen Zhang, Yifang Yin, Ying Zhang, Roger Zimmermann.
   - Mix-up Self-Supervised Learning for Contrast-agnostic Applications. [[ICME'2021](https://arxiv.org/abs/2204.00901)]
   <p align="center"><img width="75%" src="https://user-images.githubusercontent.com/44519745/204583625-58632669-05f0-445b-bd41-60aa37b515d4.png" /></p>
* **CLIM**: Hao Li, Xiaopeng Zhang, Hongkai Xiong.
   - Center-wise Local Image Mixture For Contrastive Representation Learning. [[BMVC'2021](https://arxiv.org/abs/2011.02697)]
   <p align="center"><img width="85%" src="https://user-images.githubusercontent.com/44519745/204583930-15ab3916-9d8b-4adf-9a79-e40eabbbc255.png" /></p>
* **Mixup** Xin Zhang, Minho Jin, Roger Cheng, Ruirui Li, Eunjung Han, Andreas Stolcke.
   - Contrastive-mixup Learning for Improved Speaker Verification. [[ICASSP'2022](https://arxiv.org/abs/2202.10672)]
   <p align="center"><img width="75%" src="https://user-images.githubusercontent.com/44519745/204584821-5ef0cdd9-37bf-437a-a139-d21068452be1.png" /></p>
* **Metrix**: Shashanka Venkataramanan, Bill Psomas, Ewa Kijak, Laurent Amsaleg, Konstantinos Karantzalos, Yannis Avrithis.
   - It Takes Two to Tango: Mixup for Deep Metric Learning. [[ICLR'2022](https://arxiv.org/abs/2106.04990)] [[code](https://github.com/billpsomas/Metrix_ICLR22)]
   <p align="center"><img width="45%" src="https://user-images.githubusercontent.com/44519745/204584574-9f090728-29c6-4c06-8e50-8344c789983f.png" /></p>
* **ProGCL** Jun Xia, Lirong Wu, Ge Wang, Jintao Chen, Stan Z.Li.
   - ProGCL: Rethinking Hard Negative Mining in Graph Contrastive Learning. [[ICML'2022](https://arxiv.org/abs/2110.02027)] [[code](https://github.com/junxia97/ProGCL)]
   <p align="center"><img width="70%" src="https://user-images.githubusercontent.com/44519745/204584450-e31a6c9f-0f1c-4342-b907-1b80cae547ab.png" /></p>
* **M-Mix** Shaofeng Zhang, Meng Liu, Junchi Yan, Hengrui Zhang, Lingxiao Huang, Pinyan Lu, Xiaokang Yang.
   - M-Mix: Generating Hard Negatives via Multi-sample Mixing for Contrastive Learning. [[KDD'2022](https://sherrylone.github.io/assets/KDD22_M-Mix.pdf)] [[code](https://github.com/Sherrylone/m-mix)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204582292-eef1f644-f39f-46ae-98ba-313501bdb515.png" /></p>
* **SDMP**: Sucheng Ren, Huiyu Wang, Zhengqi Gao, Shengfeng He, Alan Yuille, Yuyin Zhou, Cihang Xie.
   - A Simple Data Mixing Prior for Improving Self-Supervised Learning. [[CVPR'2022](https://arxiv.org/abs/2206.07692)] [[code](https://github.com/oliverrensu/sdmp)]
   <p align="center"><img width="95%" src="https://user-images.githubusercontent.com/44519745/204585207-6fee3174-224d-44e6-bbd1-514d6697d128.png" /></p>
* **ScaleMix**: Xiao Wang, Haoqi Fan, Yuandong Tian, Daisuke Kihara, Xinlei Chen.
   - On the Importance of Asymmetry for Siamese Representation Learning. [[CVPR'2022](https://arxiv.org/abs/2204.00613)] [[code](https://github.com/facebookresearch/asym-siam)]
   <p align="center"><img width="95%" src="https://user-images.githubusercontent.com/44519745/204585304-03b6aa42-205c-4650-9d90-ecfc0928734e.png" /></p>
* **VLMixer**: Teng Wang, Wenhao Jiang, Zhichao Lu, Feng Zheng, Ran Cheng, Chengguo Yin, Ping Luo.
   - VLMixer: Unpaired Vision-Language Pre-training via Cross-Modal CutMix. [[ICML'2022](https://arxiv.org/abs/2206.08919)]
   <p align="center"><img width="60%" src="https://user-images.githubusercontent.com/44519745/204585605-f60ae9af-b7af-4af4-ac46-28bac51c7a02.png" /></p>
* **CropMix**: Junlin Han, Lars Petersson, Hongdong Li, Ian Reid.
   - CropMix: Sampling a Rich Input Distribution via Multi-Scale Cropping. [[ArXiv'2022](https://arxiv.org/abs/2205.15955)] [[code](https://github.com/JunlinHan/CropMix)]
   <p align="center"><img width="75%" src="https://user-images.githubusercontent.com/44519745/204585732-680295fe-4768-4199-af72-bda10edda644.png" /></p>
* **MixMIM**: Jihao Liu, Xin Huang, Yu Liu, Hongsheng Li.
   - MixMIM: Mixed and Masked Image Modeling for Efficient Visual Representation Learning. [[ArXiv'2022](https://arxiv.org/abs/2205.13137)] [[code](https://github.com/Sense-X/MixMIM)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204315480-5c59ed60-7b5f-4da9-85fb-551a961fd731.png" /></p>
* **MixedAE**: Kai Chen, Zhili Liu, Lanqing Hong, Hang Xu, Zhenguo Li, Dit-Yan Yeung.
   - Mixed Autoencoder for Self-supervised Visual Representation Learning. [[CVPR'2023](https://arxiv.org/abs/2303.17152)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/229929023-1ea53237-ebfb-4203-8b93-dd761d937b27.png" /></p>

<p align="right">(<a href="#top">back to top</a>)</p>

## Mixup for Semi-supervised Learning

* **MixMatch**: David Berthelot, Nicholas Carlini, Ian Goodfellow, Nicolas Papernot, Avital Oliver, Colin Raffel.
   - MixMatch: A Holistic Approach to Semi-Supervised Learning. [[NIPS'2019](https://arxiv.org/abs/1905.02249)] [[code](https://github.com/google-research/mixmatch)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204580441-1fd71bf7-63f3-4935-9332-287642e0bcc8.png" /></p>
* **Pani VAT**: Ke Sun, Bing Yu, Zhouchen Lin, Zhanxing Zhu.
   - Patch-level Neighborhood Interpolation: A General and Effective Graph-based Regularization Strategy. [[ArXiv'2019](https://arxiv.org/abs/1911.09307)]
   <p align="center"><img width="80%" src="https://user-images.githubusercontent.com/44519745/204572993-8b3fa627-8c36-4763-a2a6-c9a90c5f0fc2.png" /></p>
* **ReMixMatch**: David Berthelot, dberth@google.com, Nicholas Carlini, Ekin D. Cubuk, Alex Kurakin, Kihyuk Sohn, Han Zhang, Colin Raffel.
   - ReMixMatch: Semi-Supervised Learning with Distribution Matching and Augmentation Anchoring. [[ICLR'2020](https://openreview.net/forum?id=HklkeR4KPB)] [[code](https://github.com/google-research/remixmatch)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204579631-529bb505-a858-441f-9030-4a9b44273330.png" /></p>
* **DivideMix**: Junnan Li, Richard Socher, Steven C.H. Hoi.
   - DivideMix: Learning with Noisy Labels as Semi-supervised Learning. [[ICLR'2020](https://arxiv.org/abs/2002.07394)] [[code](https://github.com/LiJunnan1992/DivideMix)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/230495626-f0f3f52e-9f8a-472d-8ff2-b33356993e09.png" /></p>
* **Core-Tuning**: Yifan Zhang, Bryan Hooi, Dapeng Hu, Jian Liang, Jiashi Feng.
   - Unleashing the Power of Contrastive Self-Supervised Visual Models via Contrast-Regularized Fine-Tuning. [[NIPS'2021](https://arxiv.org/abs/2102.06605)] [[code](https://github.com/vanint/core-tuning)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204580135-ed6ba8b7-b69c-4683-90f0-9aa9cdd530bc.png" /></p>
* **MUM**: JongMok Kim, Jooyoung Jang, Seunghyeon Seo, Jisoo Jeong, Jongkeun Na, Nojun Kwak.
   - MUM : Mix Image Tiles and UnMix Feature Tiles for Semi-Supervised Object Detection. [[CVPR'2022](https://user-images.githubusercontent.com/44519745/225082975-4143e7f5-8873-433c-ab6f-6caa615f7120.png)] [[code](https://github.com/jongmokkim/mix-unmix)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/225082975-4143e7f5-8873-433c-ab6f-6caa615f7120.png" /></p>
* **DFixMatch**: Zicheng Liu, Siyuan Li, Ge Wang, Cheng Tan, Lirong Wu, Stan Z. Li.
   - Decoupled Mixup for Data-efficient Learning. [[Arxiv'2022](https://arxiv.org/abs/2203.10761)] [[code](https://github.com/Westlake-AI/openmixup)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204578387-4be9567c-963a-4d2d-8c1f-c7c5ade527b8.png" /></p>
* **LaserMix**: Lingdong Kong, Jiawei Ren, Liang Pan, Ziwei Liu.
   - LaserMix for Semi-Supervised LiDAR Semantic Segmentation. [[CVPR'2023](https://arxiv.org/abs/2207.00026)] [[code](https://github.com/ldkong1205/LaserMix)] [[project](https://ldkong.com/LaserMix)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/209255964-69cab84b-ae54-4e74-be4f-a23a836c665c.png" /></p>


<p align="right">(<a href="#top">back to top</a>)</p>

## Analysis of Mixup

* Sunil Thulasidasan, Gopinath Chennupati, Jeff Bilmes, Tanmoy Bhattacharya, Sarah Michalak.
   - On Mixup Training: Improved Calibration and Predictive Uncertainty for Deep Neural Networks. [[NIPS'2019](https://arxiv.org/abs/1905.11001)] [[code](https://github.com/paganpasta/onmixup)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/204825679-ee39834f-7346-4465-b58e-c4909dec767f.png" /></p>
* Luigi Carratino, Moustapha Cissé, Rodolphe Jenatton, Jean-Philippe Vert.
   - On Mixup Regularization. [[ArXiv'2020](https://arxiv.org/abs/2006.06049)]
   <p align="center"><img width="75%" src="https://user-images.githubusercontent.com/44519745/204826066-62a66221-b023-462d-a9b7-89bbd7614425.png" /></p>
* Linjun Zhang, Zhun Deng, Kenji Kawaguchi, Amirata Ghorbani, James Zou.
   - How Does Mixup Help With Robustness and Generalization? [[ICLR'2021](https://arxiv.org/abs/2010.04819)]
   <p align="center"><img width="80%" src="https://user-images.githubusercontent.com/44519745/204826319-9ae701af-ad99-4780-85a6-492839c5bcbf.png" /></p>
* Muthu Chidambaram, Xiang Wang, Yuzheng Hu, Chenwei Wu, Rong Ge.
   - Towards Understanding the Data Dependency of Mixup-style Training. [[ICLR'2022](https://openreview.net/pdf?id=ieNJYujcGDO)] [[code](https://github.com/2014mchidamb/Mixup-Data-Dependency)]
   <p align="center"><img width="65%" src="https://user-images.githubusercontent.com/44519745/204826671-e012b918-5a14-4b5f-929b-b2f079b79d3f.png" /></p>
* Linjun Zhang, Zhun Deng, Kenji Kawaguchi, James Zou.
   - When and How Mixup Improves Calibration. [[ICML'2022](https://arxiv.org/abs/2102.06289)]
   <p align="center"><img width="50%" src="https://user-images.githubusercontent.com/44519745/204827323-b854f0a0-803f-46f8-9b74-44970998b311.png" /></p>
* Zixuan Liu, Ziqiao Wang, Hongyu Guo, Yongyi Mao.
   - Over-Training with Mixup May Hurt Generalization. [[ICLR'2023](https://openreview.net/forum?id=JmkjrlVE-DG)]
   <p align="center"><img width="90%" src="https://user-images.githubusercontent.com/44519745/216831436-704b0427-61a0-42ff-b4e6-ab361be8b634.png" /></p>
* Junsoo Oh, Chulhee Yun.
   - Provable Benefit of Mixup for Finding Optimal Decision Boundaries. [[ICML'2023](https://chulheeyun.github.io/publication/oh2023provable/)]
* Soyoun Won, Sung-Ho Bae, Seong Tae Kim.
   - Analyzing Effects of Mixed Sample Data Augmentation on Model Interpretability. [[arXiv'2023](https://arxiv.org/abs/2303.14608)]

<p align="right">(<a href="#top">back to top</a>)</p>

## Natural Language Processing

* Hongyu Guo, Yongyi Mao, Richong Zhang.
   - Augmenting Data with Mixup for Sentence Classification: An Empirical Study. [[arXiv'2019](https://arxiv.org/abs/1905.08941)] [[code](https://github.com/dsfsi/textaugment)]
* **Mixup-Transformer** Lichao Sun, Congying Xia, Wenpeng Yin, Tingting Liang, Philip S. Yu, Lifang He.
   - Mixup-Transformer: Dynamic Data Augmentation for NLP Tasks. [[COLING'2020](https://arxiv.org/abs/2010.02394)]
* **Calibrated-BERT-Fine-Tuning** Lingkai Kong, Haoming Jiang, Yuchen Zhuang, Jie Lyu, Tuo Zhao, Chao Zhang.
   - Calibrated Language Model Fine-Tuning for In- and Out-of-Distribution Data. [[EMNLP'2020](https://arxiv.org/abs/2010.11506)] [[code](https://github.com/Lingkai-Kong/Calibrated-BERT-Fine-Tuning)]
* **EMix**: Amit Jindal, Arijit Ghosh Chowdhury, Aniket Didolkar, Di Jin, Ramit Sawhney, Rajiv Ratn Shah.
   - Augmenting NLP Models using Latent Feature Interpolations. [[COLING'2020](https://aclanthology.org/2020.coling-main.611/)]
* **MixText**: Jiaao Chen, Zichao Yang, Diyi Yang.
   - MixText: Linguistically-informed Interpolation of Hidden Space for Semi-Supervised Text Classification. [[ACL'2020](https://arxiv.org/abs/2004.12239)] [[code](https://github.com/GT-SALT/MixText)]
* **TreeMix**: Le Zhang, Zichao Yang, Diyi Yang.
   - TreeMix: Compositional Constituency-based Data Augmentation for Natural Language Understanding. [[NAALC'2022](https://arxiv.org/abs/2205.06153)] [[code](https://github.com/magiccircuit/treemix)]
* **STEMM** Qingkai Fang, Rong Ye, Lei Li, Yang Feng, Mingxuan Wang.
   - STEMM: Self-learning with Speech-text Manifold Mixup for Speech Translation. [[ACL'2022](https://arxiv.org/abs/2010.02394)] [[code](https://github.com/ictnlp/STEMM)]
* **X-Mixup** Huiyun Yang, Huadong Chen, Hao Zhou, Lei Li.
   - Enhancing Cross-lingual Transfer by Manifold Mixup. [[ICLR'2022](https://arxiv.org/abs/2205.04182)] [[code](https://github.com/yhy1117/x-mixup)]

<p align="right">(<a href="#top">back to top</a>)</p>

## Survey

* Connor Shorten and Taghi Khoshgoftaar.
   - A survey on Image Data Augmentation for Deep Learning. [[Journal of Big Data'2019](https://www.researchgate.net/publication/334279066_A_survey_on_Image_Data_Augmentation_for_Deep_Learning)]
* Humza Naveed, Saeed Anwar, Munawar Hayat, Kashif Javed, Ajmal Mian.
   - Survey: Image Mixing and Deleting for Data Augmentation. [[ArXiv'2021](https://arxiv.org/abs/2106.07085)] [[code](https://github.com/humza909/survery-image-mixing-and-deleting-for-data-augmentation)]
* Dominik Lewy and Jacek Ma ́ndziuk.
   - An overview of mixing augmentation methods and augmentation strategies. [[Artificial Intelligence Review'2022](https://link.springer.com/article/10.1007/s10462-022-10227-z)]
* Suorong Yang, Weikang Xiao, Mengcheng Zhang, Suhan Guo, Jian Zhao, Furao Shen.
   - Image Data Augmentation for Deep Learning: A Survey. [[ArXiv'2022](https://arxiv.org/abs/2204.08610)]
* Chengtai Cao, Fan Zhou, Yurou Dai, Jianping Wang.
   - A Survey of Mix-based Data Augmentation: Taxonomy, Methods, Applications, and Explainability. [[ArXiv'2022](https://arxiv.org/abs/2212.10888)] [[code](https://github.com/ChengtaiCao/Awesome-Mix)]

<p align="right">(<a href="#top">back to top</a>)</p>

## Contribution

Feel free to send [pull requests](https://github.com/Westlake-AI/openmixup/pulls) to add more links with the following Markdown format. Notice that the Abbreviation, the code link, and the figure link are optional attributes.

```markdown
* **Abbreviation**: Author List.
  - Paper Name. [[Conference'Year](link)] [[code](link)]
  <p align="center"><img width="90%" src="link_to_image" /></p>
```

Current contributors include: Siyuan Li ([@Lupin1998](https://github.com/Lupin1998)), Zicheng Liu ([@pone7](https://github.com/pone7)), Zedong Wang ([@Jacky1128](https://github.com/Jacky1128)). We thank all contributors for `Awesome-Mixup`!

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
