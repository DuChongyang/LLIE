## [Low-Light Image and Video Enhancement Using Deep Learning: A Survey](https://arxiv.org/pdf/2104.10729.pdf)
![teaser](/teaser.jpg)

### 一些主流的方法
|学习策略|模型方法|文章名称|代码|平台|
|---|---|---|---|---|
|SL|LLNet|[LLNet: A deep autoencoder approach to natural low-light image enhancement](https://www.sciencedirect.com/science/article/abs/pii/S003132031630125X)|[Code](https://github.com/kglore/llnet_color)|Theano|
|SL|LightenNet|[LightenNet: A Convolutional Neural Network for weakly illuminated image enhancement](https://www.sciencedirect.com/science/article/abs/pii/S0167865518300163)||MATLAB|
|SL|Retinex-Net|[Deep Retinex Decomposition for Low-Light Enhancement](https://arxiv.org/abs/1808.04560)|[Code](https://github.com/weichen582/RetinexNet)|TensorFlow|
|SL|MBLLEN|[MBLLEN: Low-light Image/Video Enhancement Using CNNs](http://bmvc2018.org/contents/papers/0700.pdf)|[Code](https://github.com/Lvfeifan/MBLLEN)|TensorFlow|
|SL|KinD|[Kindling the Darkness: A Practical Low-light Image Enhancer](https://arxiv.org/abs/1905.04161)|[Code](https://github.com/zhangyhuaee/KinD)|TensorFlow|
|SL|KinD++|[Beyond Brightening Low-light Images](https://link.springer.com/article/10.1007/s11263-020-01407-x)|[Code](https://github.com/zhangyhuaee/KinD_plus)|TensorFlow|
|SL|TBEFN|[TBEFN: A Two-Branch Exposure-Fusion Network for Low-Light Image Enhancement](https://ieeexplore.ieee.org/abstract/document/9261119)|[Code](https://github.com/lukun199/TBEFN)|TensorFlow|
|SL|DSLR|[DSLR: Deep Stacked Laplacian Restorer for Low-Light Image Enhancement](https://ieeexplore.ieee.org/abstract/document/9264763)|[Code](https://github.com/SeokjaeLIM/DSLR-release)|PyTorch|
|UL|EnlightenGAN|[EnlightenGAN: Deep Light Enhancement Without Paired Supervision](https://ieeexplore.ieee.org/abstract/document/9334429)|[Code](https://github.com/VITA-Group/EnlightenGAN)|PyTorch|
|SSL|DRBN|[From Fidelity to Perceptual Quality: A Semi-Supervised Approach for Low-Light Image Enhancement](https://openaccess.thecvf.com/content_CVPR_2020/html/Yang_From_Fidelity_to_Perceptual_Quality_A_Semi-Supervised_Approach_for_Low-Light_CVPR_2020_paper.html)|[Code](https://github.com/ymmshi/dark_infer_collections/tree/main/DRBN)|PyTorch|
|ZSL|ExCNet|[Zero-Shot Restoration of Back-lit Images Using Deep Internal Learning](https://dl.acm.org/doi/10.1145/3343031.3351069)|[Code](https://cslinzhang.github.io/ExCNet/)|PyTorch|
|ZSL|Zero-DCE|[Zero-Reference Deep Curve Estimation for Low-Light Image Enhancemen](https://openaccess.thecvf.com/content_CVPR_2020/html/Guo_Zero-Reference_Deep_Curve_Estimation_for_Low-Light_Image_Enhancement_CVPR_2020_paper.html)|[Code](https://github.com/Li-Chongyi/Zero-DCE)|PyTorch|
|ZSL|RRDNet|[ZERO-SHOT RESTORATION OF UNDEREXPOSED IMAGES VIA ROBUST RETINEX DECOMPOSITION](https://aaaaangel.github.io/RRDNet-Homepage/RRDNet_camera_ready.pdf)|[Code](https://github.com/aaaaangel/RRDNet)|PyTorch|



LLNet：数据集是从正常光照片变换得到的（高斯噪声+伽马校正）两种网络结构（同时学习和分模块学习

LightenNet：Retinex、输入低光照图片，输出照度图，然后对照度图进行去噪、伽马校正，得到正常光照图

Retinex-Net：三部分（分解、调整、重建）、LOL

MBLLEN：结构损失+内容损失+区域损失、3D卷积、合成数据集

KinD：Retinex、不同曝光下的照片、噪声也会收到光照的影响

KinD++：Retinex、

TBEFN：Retinex、

DSLR：拉普拉斯金字塔

EnlightenGAN：两个判别器、自我感知损失

DRBN：Gan、结构损失内容损失对抗损失

ExCNet：S曲线、输入亮度通道

Zero-DCE：输入低光、输出高阶曲线再恢复为低光图片、DCE-Net、LE曲线、非参考损失

RRDNet：Retinex、损失函数三部分组成




**———————————————————————————Original Content———————————————————————————**

This repository provides：

 **1)** a unified online platform, **LLIE-Platform http://mc.nankai.edu.cn/ll/**, that covers many popular deep learning-based LLIE methods, of which the results can be produced through a user-friendly web interface, contains a low-light image and video dataset.

 **2)** a new dataset **LLIV-Phone https://drive.google.com/file/d/1QS4FgT5aTQNYy-eHZ_A89rLoZgx_iysR/view?usp=sharing**, in which the images and videos are taken by various phones' cameras under diverse illumination conditions and scenes, and 

 **3)** collects deep learning-based low-light image and video enhancement **methods, datasets, and evaluation metrics**. 

More content and details can be found in our Survey Paper: [Low-Light Image and Video Enhancement Using Deep Learning: A Survey](https://arxiv.org/abs/2104.10729). 

我们提供中文翻译版：[基于深度学习的低照度图像与视频增强综述](https://li-chongyi.github.io/PDF/Low_Light_Image_and_Video_Enhancement_Using_Deep_Learning__A_Survey.pdf). 

We provide the comparison results on the real low-light videos taken by different mobile phones’ cameras at YouTube https://www.youtube.com/watch?v=Elo9TkrG5Oo&t=6s.

✌We will periodically update the content.  Welcome to let us know if we miss your work that is published in top-tier Journal or conference. We will add it.

✌Our **LLIE-Platform** supports the function of download. Please right click and then save the figure. 

✌ **If you use this dataset or platform, please cite our paper. Please hit the star at the top-right corner. Thanks!**


✌ **Please hit the star in the repo when you ask for any code. Thanks!**


## 📣News
1. The survey is accepted by TPAMI. 

2. We newly add the Zero-DCE++ to the **LLIE-Platform**. Have Fun!

Zero-DCE++: C. Li, C. Guo, and C. C. Loy, Learning to enhance low-light image via zero-reference deep curve estimation, TPAMI, 2021.



## 🌱Contents
1. [LLIE-Platform](#DarkPlatform)
3. [LLIV-Phone Dataset](#LLIVPhone)
4. [Methods](#Methods)
5. [Datasets](#Datasets)
6. [Metrics](#Metrics)
7. [Citation](#Citation)

### 📋LoLi-Platform
Currently, the LLIE-Platform covers 14 popular deep learning-based LLIE methods including LLNet, LightenNet, Retinex-Net, EnlightenGAN, MBLLEN, KinD, KinD++, TBEFN, DSLR, DRBN, ExCNet, Zero-DCE, Zero-DCE++, and RRDNet,  where the results of any inputs can be produced through a user-friendly web interface. Have fun: [LLIE-Platform](http://mc.nankai.edu.cn/ll/).

### 📋LLIV-Phone
![Overview](/dataset_samples.png)
LLIV-Phone dataset contains 120 videos (45,148 images) taken by 18 different phones' cameras including iPhone 6s, iPhone 7, iPhone7 Plus, iPhone8 Plus, iPhone 11, iPhone 11 Pro, iPhone XS, iPhone XR, iPhone SE, Xiaomi Mi 9, Xiaomi Mi Mix 3, Pixel 3, Pixel 4,  Oppo R17, Vivo Nex, LG M322, OnePlus 5T, Huawei Mate 20 Pro under diverse illumination conditions (e.g., weak illumination, underexposure, dark, extremely dark, back-lit, non-uniform light, color light sources, etc.) in the indoor and outdoor scenes. 

Anyone can access the LLIV-Phone dataset via 

Google Drive: https://drive.google.com/file/d/1QS4FgT5aTQNYy-eHZ_A89rLoZgx_iysR/view?usp=sharing or 

Baidu Cloud：https://pan.baidu.com/s/1-8PF3dfbtlHlmk9y5ZKx_w, Password: s0b9)

## 📋Methods
![Overview](/chronology.png)
|Date|Publication|Title|Abbreviation|Code|Platform|
|---|---|---|---|---|---|
|2017|PR|LLNet: A deep autoencoder approach to natural low-light image enhancement [paper](https://www.sciencedirect.com/science/article/abs/pii/S003132031630125X)|LLNet|[Code](https://github.com/kglore/llnet_color)|Theano|
|2018|PRL|LightenNet: A convolutional neural network for weakly illuminated image enhancement [paper](https://www.sciencedirect.com/science/article/abs/pii/S0167865518300163)|LightenNet|[Code](https://li-chongyi.github.io/proj_lowlight.html)|Caffe & MATLAB|
|2018|BMVC|Deep retinex decomposition for low-light enhancement [paper](https://arxiv.org/abs/1808.04560)|Retinex-Net|[Code](https://github.com/weichen582/RetinexNet)|TensorFlow|
|2018|BMVC|MBLLEN: Low-light image/video enhancement using CNNs [paper](http://bmvc2018.org/contents/papers/0700.pdf)|MBLLEN|[Code](https://github.com/Lvfeifan/MBLLEN)|TensorFlow|
|2018|TIP|Learning a deep single image contrast enhancer from multi-exposure images [paper](https://ieeexplore.ieee.org/abstract/document/8259342/)|SCIE|[Code](https://github.com/csjcai/SICE)|Caffe & MATLAB|
|2018|CVPR|Learning to see in the dark [paper](https://openaccess.thecvf.com/content_cvpr_2018/html/Chen_Learning_to_See_CVPR_2018_paper.html)|Chen et al.|[Code](https://github.com/cchen156/Learning-to-See-in-the-Dark)|TensorFlow|
|2018|NeurIPS|DeepExposure: Learning to expose photos with asynchronously reinforced adversarial learning [paper](https://dl.acm.org/doi/abs/10.5555/3326943.3327142)|DeepExposure| |TensorFlow|
|2019|ICCV|Seeing motion in the dark [paper](https://openaccess.thecvf.com/content_ICCV_2019/html/Chen_Seeing_Motion_in_the_Dark_ICCV_2019_paper.html)|Chen et al.|[Code](https://github.com/cchen156/Seeing-Motion-in-the-Dark)|TensorFlow|
|2019|ICCV|Learning to see moving object in the dark [paper](https://openaccess.thecvf.com/content_ICCV_2019/html/Jiang_Learning_to_See_Moving_Objects_in_the_Dark_ICCV_2019_paper.html)|Jiang and Zheng|[Code](https://github.com/MichaelHYJiang)|TensorFlow|
|2019|CVPR|Underexposed photo enhancement using deep illumination estimation [paper](https://openaccess.thecvf.com/content_CVPR_2019/html/Wang_Underexposed_Photo_Enhancement_Using_Deep_Illumination_Estimation_CVPR_2019_paper.html)|DeepUPE|[Code](https://github.com/Jia-Research-Lab/DeepUPE)|TensorFlow|
|2019|ACMMM|Kindling the darkness: A practical low-light image enhancer [paper](https://dl.acm.org/doi/abs/10.1145/3343031.3350926)|KinD|[Code](https://github.com/zhangyhuaee/KinD)|TensorFlow|
|2019|ACMMM (IJCV)|Kindling the darkness: A practical low-light image enhancer [paper](https://dl.acm.org/doi/abs/10.1145/3343031.3350926) (Beyond brightening low-light images [paper](https://link.springer.com/article/10.1007/s11263-020-01407-x))|KinD (KinD++)|[Code](https://github.com/zhangyhuaee/KinD)|TensorFlow|
|2019|ACMMM|Progressive retinex: Mutually reinforced illumination-noise perception network for low-light image enhancement [paper](https://dl.acm.org/doi/abs/10.1145/3343031.3350983)|Wang et al.| |Caffe|
|2019|TIP|Low-light image enhancement via a deep hybrid network [paper](https://ieeexplore.ieee.org/abstract/document/8692732/)|Ren et al.| |Caffe|
|2019(2021)|arXiv(TIP)|EnlightenGAN: Deep light enhancement without paired supervision [paper](https://ieeexplore.ieee.org/abstract/document/9334429/)  [arxiv](https://arxiv.org/pdf/1906.06972.pdf)|EnlightenGAN|[Code](https://github.com/VITA-Group/EnlightenGAN) |PyTorch|
|2019|ACMMM|Zero-shot restoration of back-lit images using deep internal learning [paper](https://dl.acm.org/doi/abs/10.1145/3343031.3351069)|ExCNet|[Code](https://cslinzhang.github.io/ExCNet/)|PyTorch|
|2020|CVPR|Zero-reference deep curve estimation for low-light image enhancement [paper](https://openaccess.thecvf.com/content_CVPR_2020/html/Guo_Zero-Reference_Deep_Curve_Estimation_for_Low-Light_Image_Enhancement_CVPR_2020_paper.html)|Zero-DCE|[Code](https://github.com/Li-Chongyi/Zero-DCE)|PyTorch|
|2020|CVPR|From fidelity to perceptual quality: A semi-supervised approach for low-light image enhancement [paper](https://openaccess.thecvf.com/content_CVPR_2020/html/Yang_From_Fidelity_to_Perceptual_Quality_A_Semi-Supervised_Approach_for_Low-Light_CVPR_2020_paper.html)|DRBN|[Code](https://github.com/flyywh/CVPR-2020-Semi-Low-Light)|PyTorch|
|2020|ACMMM|Fast enhancement for non-uniform illumination images using light-weight CNNs [paper](https://dl.acm.org/doi/abs/10.1145/3394171.3413925)|Lv et al.| |TensorFlow|
|2020|ACMMM|Integrating semantic segmentation and retinex model for low light image enhancement [paper](https://dl.acm.org/doi/abs/10.1145/3394171.3413757)|Fan et al.| | |
|2020|CVPR|Learning to restore low-light images via decomposition-and-enhancement [paper](https://openaccess.thecvf.com/content_CVPR_2020/html/Xu_Learning_to_Restore_Low-Light_Images_via_Decomposition-and-Enhancement_CVPR_2020_paper.html)|Xu et al.|[Code](https://drive.google.com/drive/folders/1L3RDbd3sk_TcMTrSmZXn8KLg8opjOjf0) |PyTorch|
|2020|AAAI|EEMEFN: Low-light image enhancement via edge-enhanced multi-exposure fusion network [paper](https://ojs.aaai.org/index.php/AAAI/article/view/7013)|EEMEFN| |PyTorch|
|2020|TIP|Lightening network for low-light image enhancement [paper](https://ieeexplore.ieee.org/abstract/document/9141197)|DLN| |PyTorch|
|2020|TMM|Luminance-aware pyramid network for low-light image enhancement [paper](https://ieeexplore.ieee.org/abstract/document/9186194)|LPNet| |PyTorch|
|2020|ECCV|Low light video enhancement using synthetic data produced with an intermediate domain mapping [paper](https://link.springer.com/chapter/10.1007/978-3-030-58601-0_7)|SIDGAN| |TensorFlow|
|2020|TMM|TBEFN: A two-branch exposure-fusion network for low-light image enhancement [paper](https://ieeexplore.ieee.org/abstract/document/9261119/)|TBEFN|[Code](https://github.com/lukun199/TBEFN) |TensorFlow|
|2020|ICME|Zero-shot restoration of underexposed images via robust retinex decomposition [paper](https://ieeexplore.ieee.org/abstract/document/9102962/)|RRDNet|[Code](https://aaaaangel.github.io/RRDNet-Homepage) |PyTorch|
|2020|TMM|DSLR: Deep stacked laplacian restorer for low-light image enhancement [paper](https://ieeexplore.ieee.org/abstract/document/9264763/)|DSLR|[Code](https://github.com/SeokjaeLIM/DSLR-release) |PyTorch|
|2021|TPAMI|Learning to enhance low-light image via zero-reference deep curve estimation [paper](https://arxiv.org/pdf/2103.00860.pdf)|Zero-DCE++ |[Code](https://github.com/Li-Chongyi/Zero-DCE_extension) |PyTorch|
|2021|CVPR|Retinex-inspired unrolling with cooperative prior architecture search for low-light image enhancement [paper](https://arxiv.org/abs/2012.05609)|RUAS |[Code](https://github.com/dut-media-lab/RUAS) |PyTorch|
|2021|CVPR|Learning temporal consistency for low light video enhancement from single images [paper](https://openaccess.thecvf.com/content/CVPR2021/papers/Zhang_Learning_Temporal_Consistency_for_Low_Light_Video_Enhancement_From_Single_CVPR_2021_paper.pdf)|Zhang et al. |[Code](https://github.com/zkawfanx/StableLLVE) |PyTorch|
|2021|CVPR|Nighttime visibility enhancement by increasing the dynamic range and suppression of light effects [paper](https://openaccess.thecvf.com/content/CVPR2021/papers/Sharma_Nighttime_Visibility_Enhancement_by_Increasing_the_Dynamic_Range_and_Suppression_CVPR_2021_paper.pdf)|Sharma and Tan |  | |
|2021|TCSVT|RetinexDIP: A unified deep framework for low-light image enhancement [paper](https://ieeexplore.ieee.org/document/9405649)|RetinexDIP|[Code](https://sites.google.com/view/tituszhao/home/retinexdip) |PyTorch|
|2021|TIP|Sparse gradient regularized deep retinex network for robust low-light image enhancement [paper](http://39.96.165.147/Pub%20Files/2021/ywh_tip21.pdf)|Retinex-Net| |PyTorch|
|2021|TCSVT|Low-light image enhancement via progressive-recursive network [paper](https://ieeexplore.ieee.org/abstract/document/9316686)|PRIEN |  |PyTorch |
|2021|TIP|Band representation-based semi-supervised low-light image enhancement: Bridging the gap between signal fidelity and perceptual quality [paper](http://39.96.165.147/Pub%20Files/2021/ywh_tip21_2.pdf)|DRBN |  |PyTorch |
|2021|ICCV|Adaptive unfolding total variation network for low-light image enhancement [paper](https://openaccess.thecvf.com/content/ICCV2021/papers/Zheng_Adaptive_Unfolding_Total_Variation_Network_for_Low-Light_Image_Enhancement_ICCV_2021_paper.pdf)|UTVNet |[Code](https://github.com/charliezcj/utvnet)  |PyTorch |
|2021|ICCV|Seeing dynamic scene in the dark: A high-quality video dataset with mechatronic alignment [paper](https://openaccess.thecvf.com/content/ICCV2021/papers/Wang_Seeing_Dynamic_Scene_in_the_Dark_A_High-Quality_Video_Dataset_ICCV_2021_paper.pdf)|Wang et al. |[Code](https://github.com/dvlab-research/SDSD)  |PyTorch |
|2022|CVPR|SNR-aware Low-Light Image Enhancement [paper](https://jiaya.me/papers/cvpr22_xiaogang.pdf)|SNR-Aware |[Code](https://github.com/dvlab-research/SNR-Aware-Low-Light-Enhance)  |PyTorch |
|2022|CVPR|Toward Fast, Flexible, and Robust Low-Light Image Enhancement [paper](https://openaccess.thecvf.com/content/CVPR2022/papers/Ma_Toward_Fast_Flexible_and_Robust_Low-Light_Image_Enhancement_CVPR_2022_paper.pdf)|SCI |[Code](https://github.com/vis-opt-group/SCI)  |PyTorch |
|2022|CVPR|URetinex-Net: Retinex-Based Deep Unfolding Network for Low-Light Image Enhancement [paper](https://openaccess.thecvf.com/content/CVPR2022/papers/Wu_URetinex-Net_Retinex-Based_Deep_Unfolding_Network_for_Low-Light_Image_Enhancement_CVPR_2022_paper.pdf)|URetinex-Net |[Code](https://github.com/AndersonYong/URetinex-Net/)  |PyTorch |


## 📋Datasets
|Abbreviation|Number|Format|Real/Synetic|Video|Paired/Unpaired/Application|Dataset|
|---|---|---|---|---|---|---|
|LOL [paper](https://arxiv.org/abs/1808.04560)|500|RGB|Real|No|Paired|[Dataset](https://daooshee.github.io/BMVC2018website/)|
|SCIE [paper](https://ieeexplore.ieee.org/abstract/document/8259342/)|4413|RGB|Real|No|Paired|[Dataset](https://github.com/csjcai/SICE)|
|MIT-Adobe FiveK [paper](http://people.csail.mit.edu/vladb/photoadjust/db_imageadjust.pdf)|5000|Raw|Real|No|Paired|[Dataset](https://data.csail.mit.edu/graphics/fivek/)|
|SID [paper](https://openaccess.thecvf.com/content_cvpr_2018/html/Chen_Learning_to_See_CVPR_2018_paper.html)|5094|Raw|Real|No|Paired|[Dataset](https://github.com/cchen156/Learning-to-See-in-the-Dark)|
|DRV [paper](https://openaccess.thecvf.com/content_ICCV_2019/html/Chen_Seeing_Motion_in_the_Dark_ICCV_2019_paper.html)|202|Raw|Real|Yes|Paired|[Dataset](https://github.com/cchen156/Seeing-Motion-in-the-Dark) |
|SMOID [paper](https://openaccess.thecvf.com/content_ICCV_2019/html/Jiang_Learning_to_See_Moving_Objects_in_the_Dark_ICCV_2019_paper.html)|179|Raw|Real|Yes|Paired|[Dataset](https://github.com/MichaelHYJiang) |
|SDSD [paper](https://openaccess.thecvf.com/content/ICCV2021/papers/Wang_Seeing_Dynamic_Scene_in_the_Dark_A_High-Quality_Video_Dataset_ICCV_2021_paper.pdf)|150|RGB|Real|Yes|Paired|[Dataset](https://github.com/dvlab-research/SDSD) |
|LIME [paper](https://ieeexplore.ieee.org/abstract/document/7782813)|10|RGB|Real|No|Unpaired|[Dataset](https://drive.google.com/file/d/0BwVzAzXoqrSXb3prWUV1YzBjZzg/view)|
|NPE [paper](https://ieeexplore.ieee.org/abstract/document/6512558)|84|RGB|Real|No|Unpaired|[Dataset](https://drive.google.com/drive/folders/1lp6m5JE3kf3M66Dicbx5wSnvhxt90V4T)|
|MEF [paper](https://ieeexplore.ieee.org/abstract/document/7120119)|17|RGB|Real|No|Unpaired|[Dataset](https://drive.google.com/drive/folders/1lp6m5JE3kf3M66Dicbx5wSnvhxt90V4T)|
|DICM [paper](https://ieeexplore.ieee.org/abstract/document/6467022)|64|RGB|Real|No|Unpaired|[Dataset](https://drive.google.com/drive/folders/1lp6m5JE3kf3M66Dicbx5wSnvhxt90V4T)|
|VV|24|RGB|Real|No|Unpaired|[Dataset](https://drive.google.com/drive/folders/1lp6m5JE3kf3M66Dicbx5wSnvhxt90V4T)|
|ExDARK [paper](https://www.sciencedirect.com/science/article/abs/pii/S1077314218304296)|7363|RGB|Real|No|Application (Object Detection)|[Dataset](https://github.com/cs-chan/Exclusively-Dark-Image-Dataset)|
|BBD-100K [paper](https://udparty.com/php/upload/20180627/153006477668ddb6563df254a8.pdf)|10,000|RGB|Real|Yes|Application (Driving with diverse kinds of annotations)|[Dataset](https://bdd-data.berkeley.edu/)|
|DARK FACE [paper](https://arxiv.org/abs/1904.04474)|6000|RGB|Real|No|Application (Face Recognition)|[Dataset](https://flyywh.github.io/CVPRW2019LowLight/)|
|NightCity [paper](https://arxiv.org/pdf/2003.06883.pdf)|4297|RGB|Real|No|Application (Semantic Segmentation)|[Dataset](https://dmcv.sjtu.edu.cn/people/phd/tanxin/NightCity/index.html/)|

## 📋Metrics
|Abbreviation|Full-/Non-Reference|Platform|Code|
|---|---|---|---|
|MAE (Mean Absolute Error)|Full-Reference| | |
|MSE (Mean Square Error)|Full-Reference| | |
|PSNR (Peak Signal-to-Noise Ratio)|Full-Reference| | |
|SSIM (Structural Similarity Index Measurement)|Full-Reference|MATLAB|[Code](http://www.cns.nyu.edu/~lcv/ssim/ssim_index.m) |
|LPIPS (Learned Perceptual Image Patch Similarity)|Full-Reference|PyTorch|[Code](https://github.com/richzhang/PerceptualSimilarity) |
|LOE (Lightness Order Error)|Non-Reference|MATLAB|[Code](https://drive.google.com/drive/folders/0B3YzCh6G4aubLUhQMzdzR05nSDg?usp=sharing) |
|NIQE (Naturalness Image Quality Evaluator)|Non-Reference|MATLAB|[Code](https://github.com/utlive/niqe)|
|PI (Perceptual Index)|Non-Reference|MATLAB|[Code](https://github.com/chaoma99/sr-metric)|
|SPAQ (Smartphone Photography Attribute and Quality)|Non-Reference|PyTorch|[Code](https://github.com/h4nwei/SPAQ)|
|NIMA (Neural Image Assessment)|Non-Reference|PyTorch/TensorFlow|[Code](https://github.com/kentsyx/Neural-IMage-Assessment)/[Code](https://github.com/titu1994/neural-image-assessment)|
|MUSIQ (Multi-scale Image Quality Transformer)|Non-Reference|TensorFlow|[Code](https://github.com/google-research/google-research/tree/master/musiq)|
## 📜</g-emoji>License
The code, platform, and dataset are made available for academic research purpose only. 

## 📚</g-emoji>Citation
If you find the repository helpful in your resarch, please cite the following paper.
```
@article{LoLi,
  title={Low-Light Image and Video Enhancement Using Deep Learning: A Survey},
  author={Li, Chongyi and Guo, Chunle and Han, Linghao and Jiang, Jun and Cheng, Ming-Ming and Gu, Jinwei and Loy, Chen Change},
  journal={IEEE Transactions on Pattern Analysis and Machine Intelligence},
  year={2021}
}
```
## 📋Paper
[Official Version](https://ieeexplore.ieee.org/document/9609683)

[arXiv Version](https://arxiv.org/pdf/2104.10729.pdf)

[Chinese Version](https://li-chongyi.github.io/PDF/Low_Light_Image_and_Video_Enhancement_Using_Deep_Learning__A_Survey.pdf)

## 📭Contact

```
lichongyi25@gmail.com; guochunle@nankai.edu.cn
```
