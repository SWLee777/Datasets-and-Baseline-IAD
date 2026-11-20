# 课题组已有数据集

这份清单用于查找组内已登记的数据集。先按领域看数据集名称、图像内容和标注类型；确定候选后，再展开查看划分、文件大小和原始资料。清单记录不等于已核验数据包可取用或已获使用授权，开始实验前请向组内维护者确认版本、获取方式和许可。

**目录更新：2026-11-20** · [工业图像](#工业图像) · [医学图像](#医学图像) · [视频数据](#视频数据) · [划分与来源](#划分与来源) · [多分类标签](#多分类标签) · [如何更新](#如何更新)

## 工业图像

### 工业二分类

| 数据集／版本 | 图像内容 | 类别数 | 总图数 | 标注类型 |
| --- | --- | ---: | ---: | --- |
| MVTec AD | 工业产品与纹理 | 15 | 5,354 | 像素掩膜 |
| VisA | 工业产品、食品与电路板 | 12 | 10,821 | 像素掩膜 |
| BTAD | 工业零件表面 | 3 | 2,540 | 像素掩膜 |
| AITEX | 纺织面料表面 | 1 | 247 | 像素掩膜 |
| KolektorSDD（SDD） | 电机换向器塑封表面微裂纹等缺陷，含 50 个工件的多个视图。 | 1 | 399 | 像素掩膜 |
| DTD-Synthetic | 合成纹理缺陷 | 12 | 2,504 | 像素掩膜 |
| MPDD | 金属零件表面 | 6 | 1,346 | 像素掩膜 |
| MVTec LOCO AD | 工业产品与逻辑异常 | 5 | 3,651 | 像素掩膜 |
| MVTec AD 2 | 工业产品与表面 | 8 | 8,004 | 公开测试集像素掩膜 |
| MVTec 3D-AD RGB | 工业产品三维采集的RGB图像 | 10 | 3,853 | 像素掩膜 |
| Real-IAD | 工业零件表面缺陷 | 30 | 151,050 | 像素掩膜 |
| CableInspect-AD | 电缆缺陷 | 3 | 1,282 | 像素掩膜 |
| AeBAD-S | 航空发动机叶片表面 | 1 | 2,160 | 像素掩膜 |
| ELPV | 太阳能电池片电致发光 | 2 | 2,624 | 图像级标签 |
| DAGM（2007） | 工业表面检测的合成灰度纹理图。10 个纹理子类模拟不同的表面和缺陷。 | 10 | 16,100 | 像素掩膜（椭圆弱标注） |

### 工业多分类

点击数据集名称可跳到对应的异常标签明细。

| 数据集／版本 | 图像内容 | 类别数 | 总图数 | 标注类型 |
| --- | --- | ---: | ---: | --- |
| [visa_extended](#visa-extended-labels) | 工业外观图像，覆盖印刷电路板、胶囊、蜡烛、腰果、口香糖、通心粉和两类 Fryum 零食。 | 12 | 10,821 | 像素级 （分类型掩码） |
| [MAD-Real](#mad-real-labels) | 真实场景拍摄的多姿态 LEGO 动物玩具图像；本地版本的异常为部件缺失和污渍。 | 10 | 761 | 像素级（缺陷掩码） |
| [MAD-Sim](#mad-sim-labels) | 多姿态 LEGO 动物玩具的仿真渲染图像；异常包括毛刺、部件缺失和污渍。 | 20 | 9,789 | 像素级（缺陷掩码） |
| [MPDD](#mpdd-labels) | 工业金属零件外观检测图像，覆盖三种支架、连接件、金属板和管件。 | 6 | 1,346 | 像素级（缺陷掩码） |

- **VisA / visa_extended**：原版与扩展版分别登记。两者记录的总图数相同，但划分和标注不同；做对比实验时应明确用的是哪一版。
- **MPDD**：同一组图像在两处登记，既可查看正常／异常统计，也可查看对象与缺陷标签。不要当成两套独立样本。

## 医学图像

| 数据集／版本 | 图像内容 | 类别数 | 总图数 | 标注类型 |
| --- | --- | ---: | ---: | --- |
| BrainTumor | 脑肿瘤 MRI | 1 | 253 | 图像级标签 |
| BrainMRI | 脑部 MRI 病灶 | 1 | 11,215 | 像素掩膜 |
| LiverCT | 肝脏 CT 病灶 | 1 | 3,035 | 像素掩膜 |
| RESC（RetinaOCT） | RESC 来源的视网膜 OCT 切片，用于定位黄斑水肿相关病灶，如视网膜下液（SRF）和色素上皮脱离（PED）。 | 1 | 6,217 | 像素掩膜（病灶） |
| HeadCT | 头颅CT出血 | 1 | 200 | 图像级标签 |
| CVC-ClinicDB | 结肠内镜息肉 | 1 | 612 | 像素掩膜 |
| CVC-ColonDB | 结肠内镜息肉 | 1 | 380 | 像素掩膜 |
| Kvasir（Kvasir-SEG） | 结肠内镜息肉 | 1 | 1,000 | 像素掩膜 |
| Endo（EndoTect 2020 测试集） | 结直肠内镜息肉，EndoTect 2020 分割任务。 | 1 | 200 | 像素掩膜（息肉）及边界框 |
| ISBI（ISIC 2016 Part 1） | ISBI 2016 / ISIC Part 1 的皮肤镜图像，用于分割皮肤病灶。 | 1 | 379 | 像素掩膜（皮肤病灶） |

## 视频数据

这一节按视频帧计数，不是视频条数。

| 数据集／版本 | 图像内容 | 类别数 | 总图数 | 标注类型 |
| --- | --- | ---: | ---: | --- |
| UCSD Ped2 | 行人监控视频 | 1 | 4,560 | 像素掩膜 |
| AeBAD-V | 航空发动机叶片视频帧 | 1 | 2,952 | 图像级标签 |

## 划分与来源

数字沿用组内清单的口径，并不一定等于官方发布版。「类别数」为原表的类别字段，**不是**一律指缺陷类别数。表中 `—` 表示原表未列数值，不视为 0；「未标」指该划分没有可直接使用的逐图标签（不代表无法从公开资料获知汇总量）。文件大小沿用原表，可能是整包或指定目录的大小，见各条统计说明。公开资料是参考入口，不一定指向组内使用的数据副本。

<details>
<summary>展开：工业二分类的划分、文件大小与说明</summary>

| 数据集／版本 | 训练／验证 | 测试：正常／异常／未标 | 全量：正常／异常 | 文件大小 | 公开资料 |
| --- | ---: | ---: | ---: | ---: | --- |
| MVTec AD | 3,629 / 0 | 467 / 1,258 / 0 | 4,096 / 1,258 | 4.91 GiB | [MVTec AD 官方页面](https://www.mvtec.com/research-teaching/datasets/mvtec-ad) |
| VisA | 8,659 / 0 | 962 / 1,200 / 0 | 9,621 / 1,200 | 1.79 GiB | [VisA 官方说明](https://registry.opendata.aws/visa/) |
| BTAD | 1,799 / 0 | 451 / 290 / 0 | 2,250 / 290 | 5.58 GiB | [BTAD 作者项目](https://github.com/pankajmishra000/VT-ADL) |
| AITEX | — / 0 | 141 / 106 / 0 | 141 / 106 | 168.1 MiB | [AITEX 官方发布页](https://www.aitex.es/afid/) |
| KolektorSDD（SDD） | 0 / 0 | 347 / 52 / 0 | 347 / 52 | 96.8 MiB | [KolektorSDD 官方说明](https://www.vicos.si/resources/kolektorsdd/) |
| DTD-Synthetic | 1,200 / 0 | 357 / 947 / 0 | 1,557 / 947 | 349.4 MiB | [DTD 原版纹理库](https://www.robots.ox.ac.uk/~vgg/data/dtd/) |
| MPDD | 888 / 0 | 176 / 282 / 0 | 1,064 / 282 | 1.70 GiB | [MPDD 作者项目](https://github.com/stepanje/MPDD) |
| MVTec LOCO AD | 1,778 / 305 | 575 / 993 / 0 | 2,658 / 993 | 5.71 GiB | [LOCO 镜像统计](https://datasetninja.com/mvtec-loco-ad) |
| MVTec AD 2 | 2,528 / 302 | 379 / 705 / 4,090 | 4,705 / 3,299 | 30.49 GiB | [MVTec AD 2 论文表 IV](https://arxiv.org/html/2503.21622v1#S3.T4) |
| MVTec 3D-AD RGB | 2,656 / 0 | 249 / 948 / 0 | 2,905 / 948 | 2.20 GiB | [MVTec 官方数据说明](https://www.mvtec.com/research-teaching/datasets/mvtec-3d-ad) |
| Real-IAD | 36,465 / 0 | 63,256 / 51,329 / 0 | 99,721 / 51,329 | 54.86 GiB | [Real-IAD 论文](https://openaccess.thecvf.com/content/CVPR2024/papers/Wang_Real-IAD_A_Real-World_Multi-View_Dataset_for_Benchmarking_Versatile_Industrial_Anomaly_CVPR_2024_paper.pdf) |
| CableInspect-AD | 0 / 0 | 603 / 679 / 0 | 603 / 679 | 3.30 GiB | [CableInspect 作者项目](https://mila-iqia.github.io/cableinspect-ad/) |
| AeBAD-S | 521 / 0 | 490 / 1,149 / 0 | 1,011 / 1,149 | 1.27 GiB | [AeBAD 作者项目](https://github.com/zhangzilongc/MMR) |
| ELPV | 1,206 / 0 | 302 / 1,116 / 0 | 1,508 / 1,116 | 86.1 MiB | [ELPV 标注分布](https://www.dmi.unict.it/ortis/download.php?file=85182507500.pdf&name=2024_EELPV.pdf) |
| DAGM（2007） | 8,050 / 0 | 6,996 / 1,054 / 0 | 14,000 / 2,100 | 5.49 GiB | [DAGM 2007 官方说明](https://hci.iwr.uni-heidelberg.de/content/weakly-supervised-learning-industrial-optical-inspection) |

**本地统计说明**

- **MVTec AD**：本地 meta.json 的训练图均标为正常。
- **VisA**：采用原版 VisA 的 1cls.csv 划分。扩展版的训练、测试划分及分类型掩膜见本页工业多分类部分。
- **BTAD**：本地 btad.zip 的训练原图均在 ok 目录。
- **AITEX**：本地 meta.json 只收录测试图，共 247 张。AITEX 官方原版列 245 张，本行采用本地版本。
- **KolektorSDD（SDD）**：按原清单，399 张全部列作测试图。本地 fold_0 训练 264 张（正常 230、异常 34），测试 135 张（正常 117、异常 18）。SDD.zip 整包 465.9 MiB，含膨胀掩膜及框标注，原精细掩膜子包不完整。
- **DTD-Synthetic**：本地合成版的 12 个纹理类别各有 100 张正常训练图。公开资料链接至原版 DTD 纹理库。
- **MPDD**：本地训练集有 888 张正常图。本页多分类标签部分列出这批零件的类别和异常类型。
- **MVTec LOCO AD**：采用 3,651 张镜像。训练与验证均为正常图。比原论文多的 7 张均在连接器类（训练 6 张、验证 1 张）。
- **MVTec AD 2**：论文表 IV 汇总两份私有测试集，各有正常 748 张、异常 1,297 张。逐图标签由评测服务器保管。Kaggle 镜像的总数和划分与本行一致。
- **MVTec 3D-AD RGB**：本行只计参考清单收录的 RGB 图像。发布方将训练图标为无缺陷。
- **Real-IAD**：按单幅视角图像计数。总图数 151,050 与作者论文一致，正常总数包含训练和测试的正常图。
- **CableInspect-AD**：本行按原清单收录的 1,282 张测试图统计。作者项目发布的完整版本为 4,798 张。
- **AeBAD-S**：作者发布的训练划分为 good 类。
- **ELPV**：按原清单的二分类计数，缺陷概率为 0 的 1,508 张归入正常，其余 1,116 张归入异常。
- **DAGM（2007）**：据 Labels.txt，训练图中正常 7,004 张、异常 1,046 张。压缩包的两套副本只计一份。椭圆掩膜标出缺陷的大致位置。

</details>

<details>
<summary>展开：工业多分类的划分、文件大小与说明</summary>

| 数据集／版本 | 训练／验证 | 测试：正常／异常／未标 | 全量：正常／异常 | 文件大小 | 公开资料 |
| --- | ---: | ---: | ---: | ---: | --- |
| visa_extended | 7,694 / 0 | 1,927 / 1,200 / 0 | 9,621 / 1,200 | 1.78 GiB | [VisA 官方数据说明](https://registry.opendata.aws/visa/) |
| MAD-Real | 490 / 0 | 50 / 221 / 0 | 540 / 221 | 2.19 GiB | [PAD / MAD 论文](https://arxiv.org/html/2310.07716#S3) |
| MAD-Sim | 4,200 / 0 | 638 / 4,951 / 0 | 4,838 / 4,951 | 969.9 MiB | [PAD / MAD 论文](https://arxiv.org/html/2310.07716#S3) |
| MPDD | 888 / 0 | 176 / 282 / 0 | 1,064 / 282 | 1.70 GiB | [MPDD 作者项目](https://github.com/stepanje/MPDD) |

**本地统计说明**

- **visa_extended**：测试 3,127 张（正常 1,927 / 异常 1,200）。按本地 meta.json 计数。1,200 张异常原图对应 1,389 个掩码；179 张图有多种异常。 扩展版采用分类型掩膜和本地划分，原版 VisA 的划分见本页工业二分类部分。
- **MAD-Real**：测试 271 张（正常 50 / 异常 221）。只计 train 和 test 中的原图；221 张异常图均有配对掩码。
- **MAD-Sim**：测试 5,589 张（正常 638 / 异常 4,951）。只计 train 和 test 中的原图；不计缺陷掩码和相机位姿文件。
- **MPDD**：测试 458 张（正常 176 / 异常 282）。只计 train 和 test 中的原图。管件仅有 anomalous 异常标签，包内未再细分。

</details>

<details>
<summary>展开：医学图像的划分、文件大小与说明</summary>

| 数据集／版本 | 训练／验证 | 测试：正常／异常／未标 | 全量：正常／异常 | 文件大小 | 公开资料 |
| --- | ---: | ---: | ---: | ---: | --- |
| BrainTumor | 0 / 0 | 98 / 155 / 0 | 98 / 155 | 8.3 MiB | [BrainTumor 公开数据](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection) |
| BrainMRI | 7,500 / 0 | 640 / 3,075 / 0 | 8,140 / 3,075 | 386.1 MiB | [BMAD 基准论文](https://arxiv.org/html/2306.11876) |
| LiverCT | 1,542 / 0 | 833 / 660 / 0 | 2,375 / 660 | 37.0 MiB | [BMAD 基准论文](https://arxiv.org/html/2306.11876) |
| RESC（RetinaOCT） | 4,297 / 115 | 1,041 / 764 / 0 | 5,383 / 834 | 2.01 GiB | [BMAD 基准论文](https://arxiv.org/abs/2306.11876) |
| HeadCT | 60 / 0 | 40 / 100 / 0 | 100 / 100 | 24.5 MiB | [Head CT 公开数据](https://www.kaggle.com/datasets/felipekitamura/head-ct-hemorrhage) |
| CVC-ClinicDB | 0 / 0 | 0 / 612 / 0 | 0 / 612 | 52.6 MiB | [CVC 数据发布页](https://pages.cvc.uab.es/CVC-Colon/index.php/databases/) |
| CVC-ColonDB | 0 / 0 | 0 / 380 / 0 | 0 / 380 | 91.3 MiB | [CVC 数据发布页](https://pages.cvc.uab.es/CVC-Colon/index.php/databases/) |
| Kvasir（Kvasir-SEG） | 0 / 0 | 0 / 1,000 / 0 | 0 / 1,000 | 412.6 MiB | [Kvasir-SEG 论文](https://arxiv.org/abs/1911.07069) |
| Endo（EndoTect 2020 测试集） | 0 / 0 | 0 / 200 / 0 | 0 / 200 | 66.1 MiB | [EndoTect 2020 项目](https://github.com/simula/icpr-endotect-2020) |
| ISBI（ISIC 2016 Part 1） | 0 / 0 | 0 / 379 / 0 | 0 / 379 | 231.0 MiB | [ISIC 2016 官方挑战](https://challenge.isic-archive.com/landing/2016/) |

**本地统计说明**

- **BrainTumor**：原清单将 253 张 MRI 均列为测试图。公开版有肿瘤与无肿瘤两类图像级标签。
- **BrainMRI**：全量按参考清单收录的训练、测试图计算。BMAD 的训练集为正常切片。
- **LiverCT**：全量按参考清单收录的训练、测试图计算。BMAD 以正常肝脏切片构成训练集。
- **RESC（RetinaOCT）**：原清单为 6,102 张、1.97 GiB，仅含训练和测试。本地 RetinaOCT.zip 另有 115 张验证图（正常 45、异常 70），本行按完整版本计数。
- **HeadCT**：本地 labels.csv 的 200 张 CT 中，出血与无出血各 100 张。
- **CVC-ClinicDB**：本地 meta.json 只有测试集。612 帧均为息肉图像，每帧均有配对的像素掩膜。
- **CVC-ColonDB**：本地 meta.json 只有测试集。380 帧均为息肉图像，每帧均有配对的像素掩膜。
- **Kvasir（Kvasir-SEG）**：这 1,000 张息肉图在原清单中列为测试图，也是 Endo 的完整训练集。两条记录合计时只在本行计入。
- **Endo（EndoTect 2020 测试集）**：Endo.zip 完整版含 1,200 张息肉图。训练 1,000 张已计入 Kvasir，本行只计 200 张测试图。文件大小为包内测试目录的文件合计，含辅助标注；整包为 226.3 MiB。
- **ISBI（ISIC 2016 Part 1）**：本地只收录分割测试集。meta.json 将 379 张病灶图全部标为异常，标签表示有病灶，良恶性另属其他任务。

</details>

<details>
<summary>展开：视频数据的划分、文件大小与说明</summary>

| 数据集／版本 | 训练／验证 | 测试：正常／异常／未标 | 全量：正常／异常 | 文件大小 | 公开资料 |
| --- | ---: | ---: | ---: | ---: | --- |
| UCSD Ped2 | 2,550 / 0 | 362 / 1,648 / 0 | 2,912 / 1,648 | 276.1 MiB | [UCSD 数据集论文](https://www.svcl.ucsd.edu/publications/journal/2013/pami.anomaly/pami_anomaly.pdf) |
| AeBAD-V | 707 / 0 | 707 / 1,538 / 0 | 1,414 / 1,538 | 272.1 MiB | [AeBAD 作者项目](https://github.com/zhangzilongc/MMR) |

**本地统计说明**

- **UCSD Ped2**：按视频帧计数。训练集以正常行人活动为基准。
- **AeBAD-V**：按视频帧计数。作者发布的训练划分为 good 类。

</details>

## 多分类标签

「异常图像数」按对象统计；同一图像可带多个标签，因此**类型计数相加可能大于异常图像数**。「异常标签组数」按原表归并口径保留（例如原始标签 `leak` 和 `leak_mask` 可归在同一组），不要用它代替原始标签数。

<a name="visa-extended-labels"></a>

<details>
<summary>展开：visa_extended 的异常标签</summary>

| 对象类别（原名） | 对象说明 | 异常图像数 | 异常标签组数 | 异常类型（图像数） | 包内原始标签（图像数） |
| --- | --- | ---: | ---: | --- | --- |
| candle | 蜡烛 | 100 | 7 | 破损（25）；多余部件或材料（9）；熔合（13）； 缺失（15）；颗粒异物（17）；斑点（22）； 烛芯异常（11） | damaged (25); extra (9); melded (13); missing (15); particles (17); spot (22); weird_wick (11) |
| capsules | 胶囊 | 100 | 5 | 气泡（49）；破损（20）；变色（15）；泄漏（20）； 划痕（15） | bubble (49); damaged (20); discolor (15); leak (19); leak_mask (1); scratch (15) |
| cashew | 腰果 | 100 | 6 | 断裂（25）；焦痕（15）；孔洞（21）；划痕（16）； 斑点（25）；黏连（6） | broken (25); burnt (15); hole (1); holes (20); scratch (16); spot (25); stuck (6) |
| chewinggum | 口香糖 | 100 | 4 | 裂纹（28）；缺失（70）；划痕（14）；斑点（25） | crack (28); missing (70); scratch (14); spot (25) |
| fryum | Fryum 零食 | 100 | 5 | 断裂（30）；焦痕（9）；划痕（9）；斑点（36）； 黏连（20） | broken (30); burnt (9); scratch (9); spot (36); stuck (20) |
| macaroni1 | 通心粉 1 | 100 | 5 | 断裂（10）；缺口（25）；裂纹（14）；划痕（27）； 斑点（37） | broken (10); chip (25); crack (14); scratch (27); spot (37) |
| macaroni2 | 通心粉 2 | 100 | 5 | 断裂（10）；缺口（25）；裂纹（12）；划痕（25）； 斑点（35） | broken (10); chip (25); crack (12); scratch (25); spot (35) |
| pcb1 | 印刷电路板 1 | 100 | 4 | 弯曲（15）；熔化（52）；缺失（20）；划痕（21） | bent (15); melt (52); missing (20); scratch (21) |
| pcb2 | 印刷电路板 2 | 100 | 4 | 弯曲（15）；熔化（54）；缺失（19）；划痕（19） | bent (15); melt (54); missing (19); scratch (19) |
| pcb3 | 印刷电路板 3 | 100 | 4 | 弯曲（20）；熔化（41）；缺失（20）；划痕（25） | bent (20); melt (41); missing (20); scratch (25) |
| pcb4 | 印刷电路板 4 | 100 | 7 | 焦痕（8）；损伤（19）；污垢（39）； 多余部件或材料（26）；缺失（33）；划痕（17）； 错位（12） | burnt (8); damage (19); dirt (39); extra (26); missing (33); scratch (17); wrong_place (12) |
| pipe_fryum | 管状 Fryum 零食 | 100 | 6 | 断裂（25）；焦痕（16）；裂纹（10）；划痕（22）； 斑点（31）；黏连（10） | broken (25); burnt (16); crack (10); scratch (22); spot (31); stuck (10) |

</details>

<a name="mad-real-labels"></a>

<details>
<summary>展开：MAD-Real 的异常标签</summary>

| 对象类别（原名） | 对象说明 | 异常图像数 | 异常标签组数 | 异常类型（图像数） | 包内原始标签（图像数） |
| --- | --- | ---: | ---: | --- | --- |
| Bear | 熊 | 24 | 1 | 污渍（24） | Stains (24) |
| Bird | 鸟 | 22 | 1 | 部件缺失（22） | Missing (22) |
| Elephant | 大象 | 18 | 1 | 部件缺失（18） | Missing (18) |
| Parrot | 鹦鹉 | 23 | 1 | 部件缺失（23） | Missing (23) |
| Pig | 猪 | 17 | 1 | 部件缺失（17） | Missing (17) |
| Puppy | 小狗 | 20 | 1 | 污渍（20） | Stains (20) |
| Scorpion | 蝎子 | 23 | 1 | 部件缺失（23） | Missing (23) |
| Turtle | 龟 | 21 | 1 | 污渍（21） | Stains (21) |
| Unicorn | 独角兽 | 21 | 1 | 部件缺失（21） | Missing (21) |
| Whale | 鲸 | 32 | 1 | 污渍（32） | Stains (32) |

</details>

<a name="mad-sim-labels"></a>

<details>
<summary>展开：MAD-Sim 的异常标签</summary>

| 对象类别（原名） | 对象说明 | 异常图像数 | 异常标签组数 | 异常类型（图像数） | 包内原始标签（图像数） |
| --- | --- | ---: | ---: | --- | --- |
| 01Gorilla | 大猩猩 | 239 | 3 | 毛刺（67）；部件缺失（137）；污渍（35） | Burrs (67); Missing (137); Stains (35) |
| 02Unicorn | 独角兽 | 222 | 3 | 毛刺（55）；部件缺失（132）；污渍（35） | Burrs (55); Missing (132); Stains (35) |
| 03Mallard | 绿头鸭 | 217 | 3 | 毛刺（27）；部件缺失（157）；污渍（33） | Burrs (27); Missing (157); Stains (33) |
| 04Turtle | 龟 | 197 | 3 | 毛刺（32）；部件缺失（130）；污渍（35） | Burrs (32); Missing (130); Stains (35) |
| 05Whale | 鲸 | 251 | 3 | 毛刺（71）；部件缺失（127）；污渍（53） | Burrs (71); Missing (127); Stains (53) |
| 06Bird | 鸟 | 251 | 3 | 毛刺（51）；部件缺失（160）；污渍（40） | Burrs (51); Missing (160); Stains (40) |
| 07Owl | 猫头鹰 | 200 | 3 | 毛刺（41）；部件缺失（115）；污渍（44） | Burrs (41); Missing (115); Stains (44) |
| 08Sabertooth | 剑齿兽 | 241 | 3 | 毛刺（58）；部件缺失（136）；污渍（47） | Burrs (58); Missing (136); Stains (47) |
| 09Swan | 天鹅 | 250 | 3 | 毛刺（66）；部件缺失（143）；污渍（41） | Burrs (66); Missing (143); Stains (41) |
| 10Sheep | 绵羊 | 252 | 3 | 毛刺（39）；部件缺失（150）；污渍（63） | Burrs (39); Missing (150); Stains (63) |
| 11Pig | 猪 | 284 | 3 | 毛刺（76）；部件缺失（138）；污渍（70） | Burrs (76); Missing (138); Stains (70) |
| 12Zalika | Zalika 玩具 | 243 | 3 | 毛刺（56）；部件缺失（130）；污渍（57） | Burrs (56); Missing (130); Stains (57) |
| 13Pheonix | 凤凰 | 305 | 3 | 毛刺（86）；部件缺失（150）；污渍（69） | Burrs (86); Missing (150); Stains (69) |
| 14Elephant | 大象 | 276 | 3 | 毛刺（72）；部件缺失（149）；污渍（55） | Burrs (72); Missing (149); Stains (55) |
| 15Parrot | 鹦鹉 | 202 | 3 | 毛刺（29）；部件缺失（131）；污渍（42） | Burrs (29); Missing (131); Stains (42) |
| 16Cat | 猫 | 307 | 3 | 毛刺（98）；部件缺失（151）；污渍（58） | Burrs (98); Missing (151); Stains (58) |
| 17Scorpion | 蝎子 | 235 | 3 | 毛刺（61）；部件缺失（121）；污渍（53） | Burrs (61); Missing (121); Stains (53) |
| 18Obesobeso | Obesobeso 玩具 | 285 | 3 | 毛刺（101）；部件缺失（123）；污渍（61） | Burrs (101); Missing (123); Stains (61) |
| 19Bear | 熊 | 259 | 3 | 毛刺（88）；部件缺失（112）；污渍（59） | Burrs (88); Missing (112); Stains (59) |
| 20Puppy | 小狗 | 235 | 3 | 毛刺（63）；部件缺失（125）；污渍（47） | Burrs (63); Missing (125); Stains (47) |

</details>

<a name="mpdd-labels"></a>

<details>
<summary>展开：MPDD 的异常标签</summary>

| 对象类别（原名） | 对象说明 | 异常图像数 | 异常标签组数 | 异常类型（图像数） | 包内原始标签（图像数） |
| --- | --- | ---: | ---: | --- | --- |
| bracket_black | 黑色支架 | 47 | 2 | 孔洞（12）；划痕（35） | hole (12); scratches (35) |
| bracket_brown | 棕色支架 | 51 | 2 | 弯曲并伴部件不匹配（17）；部件不匹配（34） | bend_and_parts_mismatch (17); parts_mismatch (34) |
| bracket_white | 白色支架 | 30 | 2 | 涂装缺陷（13）；划痕（17） | defective_painting (13); scratches (17) |
| connector | 连接件 | 14 | 1 | 部件不匹配（14） | parts_mismatch (14) |
| metal_plate | 金属板 | 71 | 3 | 明显锈蚀（14）；划痕（34）；全面锈蚀（23） | major_rust (14); scratches (34); total_rust (23) |
| tubes | 管件 | 69 | 1 | 异常（未细分）（69） | anomalous (69) |

</details>

## 如何更新

在 GitHub 上编辑本页并提交 Pull Request（PR），由组内维护者核对。**以后以本 README 为目录，Excel 仅作初始来源**，不需要两边重复维护。

1. **必填速查行**：在合适的分区新增或更新一行，写清数据集名／版本、图像内容、类别数、总图数和标注类型；未知字段填 `待核实`。同名数据先确认是新版本、新划分，还是已有条目，不要直接重复登记。
2. **已知再填详情**：在对应折叠区添加或修改划分、大小、公开来源和口径说明；有异常标签明细时再补标签表。改划分时顺手检查速查总数和说明是否一致。数据有重叠、仅有测试划分、计数单位不同、缺少逐图标签或需要申请访问时，写在说明里。
3. 更新顶部日期，预览表格，并检查公开链接和权限说明。**不要提交原始图像、压缩包、组内存储路径或访问凭据。** 只供组内使用时，请保持仓库为私有。

可复制行模板（分别填入速查表和对应折叠区）：

```markdown
| 数据集／版本 | 图像内容 | 类别数 | 总图数 | 标注类型 |
| 数据集／版本 | 训练数 / 验证数 | 测试正常 / 测试异常 / 测试未标 | 全量正常 / 全量异常 | 文件大小 | [公开资料](https://example.org/) |
```

初始来源：`二分类数据集清单.xlsx` 的「数据集汇总」，以及 `多分类数据集清单.xlsx` 的「数据集汇总」「类别异常明细」。本页只转录这些清单中的统计和链接，未重新盘点数据包或核验外链可用性。
