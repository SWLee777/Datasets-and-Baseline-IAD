# 异常检测 Baseline 实验索引：源域少样本训练 → 目标域零样本测试

这份索引只使用汇总工作簿的「有训练」工作表。只登记已有结果的实验组合和指标名称，**不公开分数、均值、标准差或排名**。查到所需组合后请先向老师索取结果，不用先重跑。

[任务区别](#任务区别) · [少样本主实验](#少样本主实验) · [其他零样本记录](#其他零样本记录) · [参考文献](#参考文献)

## 任务区别

**两种设置都在目标域零样本测试；区别是训练时用了多少源域数据。**

| 设置 | 源域训练 | 目标域测试 |
| --- | --- | --- |
| **本索引：源域少样本训练** | 每个源域类别取 1／2／4 张正常图，用于训练或适配。 | 在另一数据集上测试，不使用目标域样本训练，也不提供目标域正常支持图。 |
| **对照：源域全量训练** | 使用源数据集的完整**训练划分**，不把源域测试集混入训练。 | 同样在另一数据集上零样本测试，不使用目标域样本训练或作正常支持图。 |

例如，原表的 **MVTec AD → VisA** 设置从 MVTec AD 每类取 1／2／4 张正常图。MVTec AD 有 15 个源类别，对应总计 **15／30／60 张**源域正常训练图；VisA 只作目标测试集。反向设置以 VisA 训练，12 个源类别对应 **12／24／48 张**。这里的 shot 是**每个源域类别**的正常图数量，不是整套数据的总张数，也不是目标域的 shot 数。个别方法会基于这些源图生成合成异常或提示，因此计数指原始正常图，不包含派生样本。

「全量源域训练」是这里的对照设置，不是所有零样本方法的定义。比较少量与全量的效果时，应固定训练方法、源／目标方向、目标测试划分和指标口径，避免把协议差异误当成样本量的影响。

## 少样本主实验

以下六种方法在下表**每一条训练 → 测试方向**上均有 **1-shot、2-shot、4-shot** 记录。原表将这些设置标为跨数据集适配（**非原论文协议**）；引用原论文是为了说明方法出处，不表示使用了论文的原始训练设置。

| 方法 | 发表会议与年份 |
| --- | --- |
| [CoPS](#ref-cops) | CVPR Findings 2026 |
| [MoECLIP](#ref-moeclip) | CVPR 2026 |
| [AdaptCLIP](#ref-adaptclip) | AAAI 2026 |
| [MultiADS](#ref-multiads) | ICCV 2025 |
| [Bayes-PFL](#ref-bayes-pfl) | CVPR 2025 |
| [InCTRL](#ref-inctrl) | CVPR 2024 |

AdaptCLIP 在原表标为 arXiv 2025；上表更新为正式发表的 AAAI 2026。这个更新仅涉及文献出处，不代表本组原运行所用的代码或配置发生改变。

`I-` 表示图像级，`P-` 表示像素级。此处「图像级＋像素级」指 `I-AUROC`、`I-AP`、`P-AUROC`、`P-AP`；「仅图像级」指 `I-AUROC`、`I-AP`。已有记录不包含 `I-F1-max`、`P-F1-max` 或 `P-AUPRO`。表中的 `Real-IAD (C1)` 是原表的单视角配置，不能当作全视角或未限定配置的 Real-IAD 结果。

| 源域训练集 | 目标域测试集 | 目标域领域 | 已有指标 |
| --- | --- | --- | --- |
| MVTec AD | VisA | 工业 | 图像级＋像素级 |
| MVTec AD | BTAD | 工业 | 图像级＋像素级 |
| MVTec AD | MPDD | 工业 | 图像级＋像素级 |
| MVTec AD | DTD-Synthetic | 合成 | 图像级＋像素级 |
| MVTec AD | AITEX | 工业 | 图像级＋像素级 |
| MVTec AD | KSDD | 工业 | 图像级＋像素级 |
| MVTec AD | MVTec 3D-AD RGB | 工业 | 图像级＋像素级 |
| MVTec AD | MVTec LOCO AD | 工业 | 图像级＋像素级 |
| MVTec AD | Real-IAD (C1) | 工业 | 图像级＋像素级 |
| MVTec AD | UCSD Ped2 | 视频 | 图像级＋像素级 |
| MVTec AD | BrainMRI | 医学 | 图像级＋像素级 |
| MVTec AD | LiverCT | 医学 | 图像级＋像素级 |
| MVTec AD | RESC | 医学 | 图像级＋像素级 |
| MVTec AD | Brain Tumor | 医学 | 仅图像级 |
| VisA | MVTec AD | 工业 | 图像级＋像素级 |

## 其他零样本记录

[VisualAD](#ref-visualad)（CVPR 2026）在原表标为 **0-shot**，对应目标域零样本；原表另有源域训练集记录，但**没有注明源域训练用了多少张图**。因此单独列在这里，不计入 1／2／4-shot 主实验，也不认定为源域全量训练。

本节「图像级＋像素级」指 `I-AUROC`、`I-AP`、`I-F1-max`、`P-AUROC`、`P-AP`、`P-F1-max`、`P-AUPRO`。

| 源域训练集 | 目标域测试集 | 已有指标 |
| --- | --- | --- |
| VisA | MVTec AD | 图像级＋像素级 |
| MVTec AD | VisA | 图像级＋像素级 |
| VisA | BTAD | 图像级＋像素级 |
| VisA | AITEX | 图像级＋像素级 |
| VisA | KSDD | 图像级＋像素级 |

**如何索取**：请告诉老师「方法＋源域 → 目标域＋源域 shot＋需要的指标」。例如：「我需要 MoECLIP 的 MVTec AD → VisA 2-shot 结果，指标是 I-AUROC 和 P-AP。」复用前核对版本、训练取样和目标测试划分。未列出的组合表示原表未收录可用记录，不等于没有跑过。

**如何更新**：仅补充已归档的覆盖信息，明确源域训练规模和目标域是否使用支持图；新增组合若不覆盖全部方法或全部 shot，应单独写明，不能直接套用主表规则。不要把实验分数上传到索引。

初始来源：`免训练复现方法汇总.xlsx` 的「有训练」工作表。

## 参考文献

<a name="ref-cops"></a>

Chen, Q., Qu, Z., Luo, W., Yao, H., Cao, Y., Jiang, Y., Duan, Y., Luo, H., Lv, C., & Zhang, Z. (2026). CoPS: Conditional prompt synthesis for zero-shot anomaly detection. In *Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR) Findings* (pp. 8554–8563). IEEE. [官方论文页](https://openaccess.thecvf.com/content/CVPR2026F/html/Chen_CoPS_Conditional_Prompt_Synthesis_for_Zero-Shot_Anomaly_Detection_CVPRF_2026_paper.html)

<a name="ref-adaptclip"></a>

Gao, B.-B., Zhou, Y., Yan, J., Cai, Y., Zhang, W., Wang, M., Liu, J., Liu, Y., Wang, L., & Wang, C. (2026). AdaptCLIP: Adapting CLIP for universal visual anomaly detection. *Proceedings of the AAAI Conference on Artificial Intelligence, 40*(6), 4095–4103. [DOI](https://doi.org/10.1609/aaai.v40i6.42404)

<a name="ref-visualad"></a>

Hou, Y., Li, P., Liu, Z., Wang, Y., Ruan, Y., Qiu, J., & Xu, K. (2026). VisualAD: Language-free zero-shot anomaly detection via vision transformer. In *Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)* (pp. 21346–21356). IEEE. [官方论文页](https://openaccess.thecvf.com/content/CVPR2026/html/Hou_VisualAD_Language-Free_Zero-Shot_Anomaly_Detection_via_Vision_Transformer_CVPR_2026_paper.html)

<a name="ref-moeclip"></a>

Park, J. Y., Seo, J., Kang, M., & Park, Y. R. (2026). MoECLIP: Patch-specialized experts for zero-shot anomaly detection. In *Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)* (pp. 35534–35544). IEEE. [官方论文页](https://openaccess.thecvf.com/content/CVPR2026/html/Park_MoECLIP_Patch-Specialized_Experts_for_Zero-shot_Anomaly_Detection_CVPR_2026_paper.html)

<a name="ref-bayes-pfl"></a>

Qu, Z., Tao, X., Gong, X., Qu, S., Chen, Q., Zhang, Z., Wang, X., & Ding, G. (2025). Bayesian prompt flow learning for zero-shot anomaly detection. In *Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)* (pp. 30398–30408). IEEE. [官方论文页](https://openaccess.thecvf.com/content/CVPR2025/html/Qu_Bayesian_Prompt_Flow_Learning_for_Zero-Shot_Anomaly_Detection_CVPR_2025_paper.html)

<a name="ref-multiads"></a>

Sadikaj, Y., Zhou, H., Halilaj, L., Schmid, S., Staab, S., & Plant, C. (2025). MultiADS: Defect-aware supervision for multi-type anomaly detection and segmentation in zero-shot learning. In *Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)* (pp. 22978–22988). IEEE. [官方论文页](https://openaccess.thecvf.com/content/ICCV2025/html/Sadikaj_MultiADS_Defect-aware_Supervision_for_Multi-type_Anomaly_Detection_and_Segmentation_in_ICCV_2025_paper.html)

<a name="ref-inctrl"></a>

Zhu, J., & Pang, G. (2024). Toward generalist anomaly detection via in-context residual learning with few-shot sample prompts. In *Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)* (pp. 17826–17836). IEEE. [官方论文页](https://openaccess.thecvf.com/content/CVPR2024/html/Zhu_Toward_Generalist_Anomaly_Detection_via_In-context_Residual_Learning_with_Few-shot_CVPR_2024_paper.html)
