# Awesome-Mixup

 [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) ![GitHub stars](https://img.shields.io/github/stars/Westlake-AI/Awesome-Mixup?color=green) ![GitHub forks](https://img.shields.io/github/forks/Westlake-AI/Awesome-Mixup?color=yellow&label=Fork) ![visitors](https://visitor-badge.glitch.me/badge?page_id=Westlake-AI/Awesome-Mixup)

## Introduction

**We summarize awesome mixup data augmentation methods for visual representation learning in various scenarios.**

The list of awesome mixup augmentation methods is summarized in chronological order and is on updating. The main branch is modified according to [Awesome-Mixup](https://github.com/Westlake-AI/openmixup/docs/en/awesome_mixups) in [OpenMixup](https://github.com/Westlake-AI/openmixup). We first summarize fundermental mixup methods from two aspects: *sample mixup policy* and *label mixup policy*. Then, we summarize mixup techniques used in downstream tasks. Currently, we are working on a survey of mixup methods.


## Fundermental Methods

### Sample Mixup Methods

#### **Pre-defined Policies**

* **MixUp**: Hongyi Zhang, Moustapha Cisse, Yann N. Dauphin, David Lopez-Paz.
   - mixup: Beyond Empirical Risk Minimization. [[ICLR'2018](https://arxiv.org/abs/1710.09412)] [[code](https://github.com/facebookresearch/mixup-cifar10)]
* **BC**: Yuji Tokozume, Yoshitaka Ushiku, Tatsuya Harada.
   - Between-class Learning for Image Classification. [[CVPR'2018](https://arxiv.org/abs/1711.10284)] [[code](https://github.com/mil-tokyo/bc_learning_image)]
* **AdaMixup**: Hongyu Guo, Yongyi Mao, Richong Zhang.
   - MixUp as Locally Linear Out-Of-Manifold Regularization. [[AAAI'2019](https://arxiv.org/abs/1809.02499)]
* **CutMix**: Sangdoo Yun, Dongyoon Han, Seong Joon Oh, Sanghyuk Chun, Junsuk Choe, Youngjoon Yoo.
   - CutMix: Regularization Strategy to Train Strong Classifiers with Localizable Features. [[ICCV'2019](https://arxiv.org/abs/1905.04899)] [[code](https://github.com/clovaai/CutMix-PyTorch)]
* **ManifoldMix**: Vikas Verma, Alex Lamb, Christopher Beckham, Amir Najafi, Ioannis Mitliagkas, David Lopez-Paz, Yoshua Bengio.
   - Manifold Mixup: Better Representations by Interpolating Hidden States. [[ICML'2019](https://arxiv.org/abs/1806.05236)] [[code](https://github.com/vikasverma1077/manifold_mixup)]
* **FMix**: Ethan Harris, Antonia Marcu, Matthew Painter, Mahesan Niranjan, Adam Prügel-Bennett, Jonathon Hare.
   - FMix: Enhancing Mixed Sample Data Augmentation. [[Arixv'2020](https://arxiv.org/abs/2002.12047)] [[code](https://github.com/ecs-vlc/FMix)]
* **SmoothMix**: Jin-Ha Lee, Muhammad Zaigham Zaheer, Marcella Astrid, Seung-Ik Lee.
   - SmoothMix: a Simple Yet Effective Data Augmentation to Train Robust Classifiers. [[CVPRW'2020](https://arxiv.org/abs/2002.12047)] [[code](https://github.com/Westlake-AI/openmixup)]
* **PatchUp**: Mojtaba Faramarzi, Mohammad Amini, Akilesh Badrinaaraayanan, Vikas Verma, Sarath Chandar.
   - PatchUp: A Regularization Technique for Convolutional Neural Networks. [[Arxiv'2020](https://arxiv.org/abs/2006.07794)] [[code](https://github.com/chandar-lab/PatchUp)]
* **GridMixup**: Kyungjune Baek, Duhyeon Bang, Hyunjung Shim.
   - GridMix: Strong regularization through local context mapping. [[Pattern Recognition'2021](https://www.sciencedirect.com/science/article/pii/S0031320320303976)] [[code](https://github.com/IlyaDobrynin/GridMixup)]
* **ResizeMix**: Jie Qin, Jiemin Fang, Qian Zhang, Wenyu Liu, Xingang Wang, Xinggang Wang.
   - ResizeMix: Mixing Data with Preserved Object Information and True Labels. [[Arixv'2020](https://arxiv.org/abs/2012.11101)] [[code](https://github.com/Westlake-AI/openmixup)]
* **FocusMix**: Jiyeon Kim, Ik-Hee Shin, Jong-Ryul, Lee, Yong-Ju Lee.
   - Where to Cut and Paste: Data Regularization with Selective Features. [[ICTC'2020](https://ieeexplore.ieee.org/abstract/document/9289404)]
* **AugMix**: Dan Hendrycks, Norman Mu, Ekin D. Cubuk, Barret Zoph, Justin Gilmer, Balaji Lakshminarayanan.
   - AugMix: A Simple Data Processing Method to Improve Robustness and Uncertainty. [[ICLR'2020](https://arxiv.org/abs/1912.02781)] [[code](https://github.com/google-research/augmix)]
* **DJMix**: Ryuichiro Hataya, Hideki Nakayama.
   - DJMix: Unsupervised Task-agnostic Augmentation for Improving Robustness. [[Arxiv'2021](https://openreview.net/pdf?id=0n3BaVlNsHI)]
* **PixMix**: Dan Hendrycks, Andy Zou, Mantas Mazeika, Leonard Tang, Bo Li, Dawn Song, Jacob Steinhardt.
   - PixMix: Dreamlike Pictures Comprehensively Improve Safety Measures. [[Arxiv'2021](https://arxiv.org/abs/2112.05135)] [[code](https://github.com/andyzoujm/pixmix)]
* **StyleMix**: Minui Hong, Jinwoo Choi, Gunhee Kim.
   - StyleMix: Separating Content and Style for Enhanced Data Augmentation. [[CVPR'2021](https://openaccess.thecvf.com/content/CVPR2021/papers/Hong_StyleMix_Separating_Content_and_Style_for_Enhanced_Data_Augmentation_CVPR_2021_paper.pdf)] [[code](https://github.com/alsdml/StyleMix)]
* **MixStyle**: Kaiyang Zhou, Yongxin Yang, Yu Qiao, Tao Xiang.
   - Domain Generalization with MixStyle. [[ICLR'2021](https://openreview.net/forum?id=6xHJ37MVxxp)] [[code](https://github.com/KaiyangZhou/mixstyle-release)]
* **MoEx**: Boyi Li, Felix Wu, Ser-Nam Lim, Serge Belongie, Kilian Q. Weinberger.
   - On Feature Normalization and Data Augmentation. [[CVPR'2021](https://arxiv.org/abs/2002.11102)] [[code](https://github.com/Boyiliee/MoEx)]
* **k-Mixup**: Kristjan Greenewald, Anming Gu, Mikhail Yurochkin, Justin Solomon, Edward Chien.
   - k-Mixup Regularization for Deep Learning via Optimal Transport. [[ArXiv'2021](https://arxiv.org/abs/2106.02933)]
* **NFM**: Soon Hoe Lim, N. Benjamin Erichson, Francisco Utrera, Winnie Xu, Michael W. Mahoney.
   - Noisy Feature Mixup. [[ICLR'2022](https://arxiv.org/abs/2110.02180)] [[code](https://github.com/erichson/NFM)]
* **LocalMix**: Raphael Baena, Lucas Drumetz, Vincent Gripon.
   - Preventing Manifold Intrusion with Locality: Local Mixup. [[EUSIPCO'2022](https://arxiv.org/abs/2201.04368)] [[code](https://github.com/raphael-baena/Local-Mixup)]
* **RandomMix**: Xiaoliang Liu, Furao Shen, Jian Zhao, Changhai Nie.
   - RandomMix: A mixed sample data augmentation method with multiple mixed modes. [[ArXiv'2022](https://arxiv.org/abs/2205.08728)]
* **SuperpixelGridCut**: Karim Hammoudi, Adnane Cabani, Bouthaina Slika, Halim Benhabiles, Fadi Dornaika, Mahmoud Melkemi.
   - SuperpixelGridCut, SuperpixelGridMean and SuperpixelGridMix Data Augmentation. [[ArXiv'2022](https://arxiv.org/abs/2204.08458)] [[code](https://github.com/hammoudiproject/SuperpixelGridMasks)]
* **AugRmixAT**: Xiaoliang Liu, Furao Shen, Jian Zhao, Changhai Nie.
   - AugRmixAT: A Data Processing and Training Method for Improving Multiple Robustness and Generalization Performance. [[ICME'2022](https://arxiv.org/abs/2207.10290)]
* **MSDA**: Chanwoo Park, Sangdoo Yun, Sanghyuk Chun.
   - A Unified Analysis of Mixed Sample Data Augmentation: A Loss Function Perspective. [[NIPS'2022](https://arxiv.org/abs/2208.09913)] [[code](https://github.com/naver-ai/hmix-gmix)]
* **RegMixup**: Francesco Pinto, Harry Yang, Ser-Nam Lim, Philip H.S. Torr, Puneet K. Dokania.
   - RegMixup: Mixup as a Regularizer Can Surprisingly Improve Accuracy and Out Distribution Robustness. [[NIPS'2022](https://arxiv.org/abs/2206.14502)] [[code](https://github.com/FrancescoPinto/RegMixup)]


#### **Saliency-guided Policies**

* **SaliencyMix**: A F M Shahab Uddin and Mst. Sirazam Monira and Wheemyung Shin and TaeChoong Chung and Sung-Ho Bae
   - SaliencyMix: A Saliency Guided Data Augmentation Strategy for Better Regularization. [[ICLR'2021](https://arxiv.org/abs/2006.01791)] [[code](https://github.com/SaliencyMix/SaliencyMix)]
* **AttentiveMix**: Devesh Walawalkar, Zhiqiang Shen, Zechun Liu, Marios Savvides.
   - Attentive CutMix: An Enhanced Data Augmentation Approach for Deep Learning Based Image Classification. [[ICASSP'2020](https://arxiv.org/abs/2003.13048)] [[code](https://github.com/xden2331/attentive_cutmix)]
* **SnapMix**: Shaoli Huang, Xinchao Wang, Dacheng Tao.
   - SnapMix: Semantically Proportional Mixing for Augmenting Fine-grained Data. [[AAAI'2021](https://arxiv.org/abs/2012.04846)] [[code](https://github.com/Shaoli-Huang/SnapMix)]
* **AttributeMix**: Hao Li, Xiaopeng Zhang, Hongkai Xiong, Qi Tian.
   - Attribute Mix: Semantic Data Augmentation for Fine Grained Recognition. [[Arxiv'2020](https://arxiv.org/abs/2004.02684)]
* **AutoMix**: Jianchao Zhu, Liangliang Shi, Junchi Yan, Hongyuan Zha.
   - AutoMix: Mixup Networks for Sample Interpolation via Cooperative Barycenter Learning. [[ECCV'2020](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123550630.pdf)]
* **Pani VAT**: Ke Sun, Bing Yu, Zhouchen Lin, Zhanxing Zhu.
   - Patch-level Neighborhood Interpolation: A General and Effective Graph-based Regularization Strategy. [[ArXiv'2019](https://arxiv.org/abs/1911.09307)]
* **PuzzleMix**: Jang-Hyun Kim, Wonho Choo, Hyun Oh Song.
   - Puzzle Mix: Exploiting Saliency and Local Statistics for Optimal Mixup. [[ICML'2020](https://arxiv.org/abs/2009.06962)] [[code](https://github.com/snu-mllab/PuzzleMix)]
* **CoMixup**: Jang-Hyun Kim, Wonho Choo, Hosan Jeong, Hyun Oh Song.
   - Co-Mixup: Saliency Guided Joint Mixup with Supermodular Diversity. [[ICLR'2021](https://arxiv.org/abs/2102.03065)] [[code](https://github.com/snu-mllab/Co-Mixup)]
* **SuperMix**: Ali Dabouei, Sobhan Soleymani, Fariborz Taherkhani, Nasser M. Nasrabadi.
   - SuperMix: Supervising the Mixing Data Augmentation. [[CVPR'2021](https://arxiv.org/abs/2003.05034)] [[code](https://github.com/alldbi/SuperMix)]
* **PatchMix**: Paola Cascante-Bonilla, Arshdeep Sekhon, Yanjun Qi, Vicente Ordonez.
   - Evolving Image Compositions for Feature Representation Learning. [[BMVC'2021](https://arxiv.org/pdf/2106.09011.pdf)]
* **StackMix**: John Chen, Samarth Sinha, Anastasios Kyrillidis.
   - StackMix: A complementary Mix algorithm. [[Arxiv'2021](https://arxiv.org/abs/2011.12618)]
* **AlignMix**: Shashanka Venkataramanan, Ewa Kijak, Laurent Amsaleg, Yannis Avrithis.
   - AlignMix: Improving representation by interpolating aligned features. [[CVPR'2022](https://arxiv.org/abs/2103.15375)] [[code](https://github.com/shashankvkt/AlignMixup_CVPR22)]
* **AutoMix**: Zicheng Liu, Siyuan Li, Di Wu, Zihan Liu, Zhiyuan Chen, Lirong Wu, Stan Z. Li.
   - AutoMix: Unveiling the Power of Mixup for Stronger Classifiers. [[ECCV'2022](https://arxiv.org/abs/2103.13027)] [[code](https://github.com/Westlake-AI/openmixup)]
* **SAMix**: Siyuan Li, Zicheng Liu, Di Wu, Zihan Liu, Stan Z. Li.
   - Boosting Discriminative Visual Representation Learning with Scenario-Agnostic Mixup. [[Arxiv'2021](https://arxiv.org/abs/2111.15454)] [[code](https://github.com/Westlake-AI/openmixup)]
* **ScoreMix**: Thomas Stegmüller, Behzad Bozorgtabar, Antoine Spahr, Jean-Philippe Thiran.
   - ScoreNet: Learning Non-Uniform Attention and Augmentation for Transformer-Based Histopathological Image Classification. [[Arxiv'2022](https://arxiv.org/abs/2202.07570)]
* **RecursiveMix**: Lingfeng Yang, Xiang Li, Borui Zhao, Renjie Song, Jian Yang.
   - RecursiveMix: Mixed Learning with History. [[NIPS'2022](https://arxiv.org/abs/2203.06844)] [[code](https://github.com/implus/RecursiveMix-pytorch)]


### Label Mixup Methods

* **MixUp**: Hongyi Zhang, Moustapha Cisse, Yann N. Dauphin, David Lopez-Paz.
   - mixup: Beyond Empirical Risk Minimization. [[ICLR'2018](https://arxiv.org/abs/1710.09412)] [[code](https://github.com/facebookresearch/mixup-cifar10)]
* **CutMix**: Sangdoo Yun, Dongyoon Han, Seong Joon Oh, Sanghyuk Chun, Junsuk Choe, Youngjoon Yoo.
   - CutMix: Regularization Strategy to Train Strong Classifiers with Localizable Features. [[ICCV'2019](https://arxiv.org/abs/1905.04899)] [[code](https://github.com/clovaai/CutMix-PyTorch)]
* **MetaMixup**: Zhijun Mai, Guosheng Hu, Dexiong Chen, Fumin Shen, Heng Tao Shen.
   - Metamixup: Learning adaptive interpolation policy of mixup with metalearning. [[TNNLS'2021](https://arxiv.org/abs/1908.10059)]
* **mWH**: Hao Yu, Huanyu Wang, Jianxin Wu.
   - Mixup Without Hesitation. [[Pattern Recognition'2022](https://arxiv.org/abs/2101.04342)] [[code](https://github.com/yuhao318/mwh)]
* **CAMixup**: Yeming Wen, Ghassen Jerfel, Rafael Muller, Michael W. Dusenberry, Jasper Snoek, Balaji Lakshminarayanan, Dustin Tran.
   - Combining Ensembles and Data Augmentation can Harm your Calibration. [[ICLR'2021](https://arxiv.org/abs/2010.09875)] [[code](https://github.com/google/edward2/tree/main/experimental/marginalization_mixup)]
* **Saliency Grafting**: Joonhyung Park, June Yong Yang, Jinwoo Shin, Sung Ju Hwang, Eunho Yang.
   - Saliency Grafting: Innocuous Attribution-Guided Mixup with Calibrated Label Mixing. [[AAAI'2022](https://arxiv.org/abs/2112.08796)]
* **TransMix**: Jie-Neng Chen, Shuyang Sun, Ju He, Philip Torr, Alan Yuille, Song Bai.
   - TransMix: Attend to Mix for Vision Transformers. [[CVPR'2022](https://arxiv.org/abs/2111.09833)] [[code](https://github.com/Beckschen/TransMix)]
* **GenLabel**: Yeming Wen, Ghassen Jerfel, Rafael Muller, Michael W. Dusenberry, Jasper Snoek, Balaji Lakshminarayanan, Dustin Tran.
   - GenLabel: Mixup Relabeling using Generative Models. [[ArXiv'2022](https://arxiv.org/abs/2201.02354)]
* **DecoupleMix**: Zicheng Liu, Siyuan Li, Ge Wang, Cheng Tan, Lirong Wu, Stan Z. Li.
   - Decoupled Mixup for Data-efficient Learning. [[Arxiv'2022](https://arxiv.org/abs/2203.10761)] [[code](https://github.com/Westlake-AI/openmixup)]
* **TokenMix**: Jihao Liu, Boxiao Liu, Hang Zhou, Hongsheng Li, Yu Liu.
   - TokenMix: Rethinking Image Mixing for Data Augmentation in Vision Transformers. [[ECCV'2022](https://arxiv.org/abs/2207.08409)] [[code](https://github.com/Sense-X/TokenMix)]


## Mixup Methods for Self-supervised Learning

* **MixCo**: Sungnyun Kim, Gihun Lee, Sangmin Bae, Se-Young Yun.
   - MixCo: Mix-up Contrastive Learning for Visual Representation. [[NIPSW'2020](https://arxiv.org/abs/2010.06300)] [[code](https://github.com/Lee-Gihun/MixCo-Mixup-Contrast)]
* **MoCHi**: Yannis Kalantidis, Mert Bulent Sariyildiz, Noe Pion, Philippe Weinzaepfel, Diane Larlus.
   - Hard Negative Mixing for Contrastive Learning. [[NIPS'2020](https://arxiv.org/abs/2010.01028)] [[code](https://europe.naverlabs.com/mochi)]
* **i-Mix**: Kibok Lee, Yian Zhu, Kihyuk Sohn, Chun-Liang Li, Jinwoo Shin, Honglak Lee.
   - i-Mix A Domain-Agnostic Strategy for Contrastive Representation Learning. [[ICLR'2021](https://arxiv.org/abs/2010.08887)] [[code](https://github.com/kibok90/imix)]
* **Un-Mix**: Zhiqiang Shen, Zechun Liu, Zhuang Liu, Marios Savvides, Trevor Darrell, Eric Xing.
   - Un-Mix: Rethinking Image Mixtures for Unsupervised Visual Representation. [[AAAI'2022](https://arxiv.org/abs/2003.05438)] [[code](https://github.com/szq0214/Un-Mix)]
* **BSIM**: Xiangxiang Chu, Xiaohang Zhan, Xiaolin Wei.
   - Beyond Single Instance Multi-view Unsupervised Representation Learning. [[Arxiv'2020](https://arxiv.org/abs/2011.13356)]
* **FT**: Rui Zhu, Bingchen Zhao, Jingen Liu, Zhenglong Sun, Chang Wen Chen.
   - Improving Contrastive Learning by Visualizing Feature Transformation. [[ICCV'2021](https://arxiv.org/abs/2108.02982)] [[code](https://github.com/DTennant/CL-Visualizing-Feature-Transformation)]
* **m-Mix**: Shaofeng Zhang, Meng Liu, Junchi Yan, Hengrui Zhang, Lingxiao Huang, Pinyan Lu, Xiaokang Yang.
   - m-mix: Generating hard negatives via multiple samples mixing for contrastive learning. [[Arxiv'2021](https://openreview.net/forum?id=lsljy2bG3n)]
* **PCEA**: Jingwei Liu, Yi Gu, Shentong Mo, Zhun Sun, Shumin Han, Jiafeng Guo, Xueqi Cheng.
   - Piecing and Chipping: An effective solution for the information-erasing view generation in Self-supervised Learning. [[OpenReview'2021](https://openreview.net/forum?id=DnG8f7gweH4)]
* **CoMix**: Aadarsh Sahoo, Rutav Shah, Rameswar Panda, Kate Saenko, Abir Das.
   - Contrast and Mix: Temporal Contrastive Video Domain Adaptation with Background Mixing. [[NIPS'2021](https://proceedings.neurips.cc/paper/2021/file/c47e93742387750baba2e238558fa12d-Paper.pdf)] [[code](https://cvir.github.io/projects/comix)]
* **SAMix**: Siyuan Li, Zicheng Liu, Di Wu, Zihan Liu, Stan Z. Li.
   - Boosting Discriminative Visual Representation Learning with Scenario-Agnostic Mixup. [[Arxiv'2021](https://arxiv.org/abs/2111.15454)] [[code](https://github.com/Westlake-AI/openmixup)]
* **MixSiam**: Xiaoyang Guo, Tianhao Zhao, Yutian Lin, Bo Du.
   - MixSiam: A Mixture-based Approach to Self-supervised Representation Learning. [[OpenReview'2021](https://arxiv.org/abs/2111.02679)]
* **MixSSL**: Yichen Zhang, Yifang Yin, Ying Zhang, Roger Zimmermann.
   - Mix-up Self-Supervised Learning for Contrast-agnostic Applications. [[ICME'2021](https://arxiv.org/abs/2204.00901)]
* **CLIM**: Hao Li, Xiaopeng Zhang, Hongkai Xiong.
   - Center-wise Local Image Mixture For Contrastive Representation Learning. [[BMVC'2021](https://arxiv.org/abs/2011.02697)]
* **Metrix**: Shashanka Venkataramanan, Bill Psomas, Ewa Kijak, Laurent Amsaleg, Konstantinos Karantzalos, Yannis Avrithis.
   - It Takes Two to Tango: Mixup for Deep Metric Learning. [[ICLR'2022](https://arxiv.org/abs/2106.04990)] [[code](https://github.com/billpsomas/Metrix_ICLR22)]
* **SDMP**: Sucheng Ren, Huiyu Wang, Zhengqi Gao, Shengfeng He, Alan Yuille, Yuyin Zhou, Cihang Xie.
   - A Simple Data Mixing Prior for Improving Self-Supervised Learning. [[CVPR'2022](https://arxiv.org/abs/2206.07692)] [[code](https://github.com/oliverrensu/sdmp)]
* **VLMixer**: Teng Wang, Wenhao Jiang, Zhichao Lu, Feng Zheng, Ran Cheng, Chengguo Yin, Ping Luo.
   - VLMixer: Unpaired Vision-Language Pre-training via Cross-Modal CutMix. [[ICML'2022](https://arxiv.org/abs/2206.08919)]
* **CropMix**: Junlin Han, Lars Petersson, Hongdong Li, Ian Reid.
   - CropMix: Sampling a Rich Input Distribution via Multi-Scale Cropping. [[ArXiv'2022](https://arxiv.org/abs/2205.15955)] [[code](https://github.com/JunlinHan/CropMix)]


## Mixup Methods for Semi-supervised Learning

* **MixMatch**: David Berthelot, Nicholas Carlini, Ian Goodfellow, Nicolas Papernot, Avital Oliver, Colin Raffel.
   - MixMatch: A Holistic Approach to Semi-Supervised Learning. [[NIPS'2019](https://arxiv.org/abs/1905.02249)] [[code](https://github.com/google-research/mixmatch)]
* **Pani VAT**: Ke Sun, Bing Yu, Zhouchen Lin, Zhanxing Zhu.
   - Patch-level Neighborhood Interpolation: A General and Effective Graph-based Regularization Strategy. [[ArXiv'2019](https://arxiv.org/abs/1911.09307)]
* **ReMixMatch**: David Berthelot, dberth@google.com, Nicholas Carlini, Ekin D. Cubuk, Alex Kurakin, Kihyuk Sohn, Han Zhang, Colin Raffel.
   - ReMixMatch: Semi-Supervised Learning with Distribution Matching and Augmentation Anchoring. [[ICLR'2020](https://openreview.net/forum?id=HklkeR4KPB)] [[code](https://github.com/google-research/remixmatch)]
* **Core-Tuning**: Yifan Zhang, Bryan Hooi, Dapeng Hu, Jian Liang, Jiashi Feng.
   - Unleashing the Power of Contrastive Self-Supervised Visual Models via Contrast-Regularized Fine-Tuning. [[NIPS'2021](https://arxiv.org/abs/2102.06605)] [[code](https://github.com/vanint/core-tuning)]
* **DFixMatch**: Zicheng Liu, Siyuan Li, Ge Wang, Cheng Tan, Lirong Wu, Stan Z. Li.
   - Decoupled Mixup for Data-efficient Learning. [[Arxiv'2022](https://arxiv.org/abs/2203.10761)] [[code](https://github.com/Westlake-AI/openmixup)]


## Analysis of Mixup

* Muthu Chidambaram, Xiang Wang, Yuzheng Hu, Chenwei Wu, Rong Ge.
   - Towards Understanding the Data Dependency of Mixup-style Training. [[ICLR'2022](https://openreview.net/pdf?id=ieNJYujcGDO)] [[code](https://github.com/2014mchidamb/Mixup-Data-Dependency)]
* Linjun Zhang, Zhun Deng, Kenji Kawaguchi, James Zou.
   - When and How Mixup Improves Calibration. [[ICML'2022](https://arxiv.org/abs/2102.06289)]


## Survey

* An overview of mixing augmentation methods and augmentation strategies.
   - A Survey on Masked Autoencoder for Self-supervised Learning in Vision and Beyond. [[Artificial Intelligence Review'2022](https://link.springer.com/article/10.1007/s10462-022-10227-z)]


## Contribution

Feel free to send [pull requests](https://github.com/Westlake-AI/openmixup/pulls) to add more links with the following Markdown format. Note that the Abbreviation and the code link are optional attributes.

```markdown
* **Abbreviation**: Author List.
  - Paper Name. [[Conference'Year](link)] [[code](link)]
```

Current contributors include: Siyuan Li ([@Lupin1998](https://github.com/Lupin1998)), Zicheng Liu ([@pone7](https://github.com/pone7)), Zedong Wang ([@Jacky1128](https://github.com/Jacky1128)). We thank all contributors for `Awesome-Mixup`!


## Related Project

- [OpenMixup](https://github.com/Westlake-AI/openmixup): CAIRI Supervised, Semi- and Self-Supervised Visual Representation Learning Toolbox and Benchmark.
- [Awesome-Mixup](https://github.com/Westlake-AI/openmixup/docs/en/awesome_mixups): Awesome list of mixup augmentation methods for supervised, semi-, and self-supervised visual representation learning.
- [awesome-mixup](https://github.com/demoleiwang/awesome-mixup): A collection of awesome papers about mixup.
