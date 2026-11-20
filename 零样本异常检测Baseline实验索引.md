# 零样本异常检测 Baseline 实验索引

注意：此任务为零样本跨域，例如使用mvtec整个数据集中的数据训练，然后在其他数据集上进行测试，包含医学。而mvtec上的测试，则是使用visa数据集训练。

查到所需的**评测层级、数据集和方法**后，请向老师索取对应指标的原始结果。**先确认能否复用，再决定是否重跑。** 申请时注明数据集版本或划分；同名数据集或同名指标不一定使用同一评测设置。

[像素级](#像素级) · [图像级](#图像级) · [参考文献](#参考文献)

表格只登记原表已有记录的**指标名称**，不展示任何实验数值。`—` 或未列出的组合表示本索引未收录，不代表没有跑过。

## 像素级

| 领域 | 数据集 | [AnomalyCLIP](#ref-anomalyclip)（ICLR 2024） | [AdaCLIP](#ref-adaclip)（ECCV 2024） | [AA-CLIP](#ref-aa-clip)（CVPR 2025） | [FAPrompt](#ref-faprompt)（ICCV 2025） | [VisualAD](#ref-visualad)（CVPR 2026） | [MoECLIP](#ref-moeclip)（CVPR 2026） |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 工业 | MVTecAD | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO |
| 工业 | VisA | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO |
| 工业 | BTAD | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO |
| 工业 | MPDD | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO |
| 医学 | CVC-ColonDB | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO |
| 医学 | CVC-ClinicDB | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO |
| 医学 | Kvasir | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO |
| 医学 | BraTS | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO | AUROC、PRO |

## 图像级

| 领域 | 数据集 | [AnomalyCLIP](#ref-anomalyclip)（ICLR 2024） | [AdaCLIP](#ref-adaclip)（ECCV 2024） | [AA-CLIP](#ref-aa-clip)（CVPR 2025） | [FAPrompt](#ref-faprompt)（ICCV 2025） | [VisualAD](#ref-visualad)（CVPR 2026） | [MoECLIP](#ref-moeclip)（CVPR 2026） |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 工业 | MVTecAD | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP |
| 工业 | VisA | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP |
| 工业 | BTAD | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP |
| 工业 | MPDD | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP |
| 工业 | AITEX | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP |
| 医学 | HeadCT | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP |
| 医学 | Br35H | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP |

**索取示例**：老师，我想复用图像级 VisA 上 AdaCLIP 的 AUROC 和 AP，请问现有结果对应的是哪个数据版本和划分？

**更新方式**：新结果归档后，在对应层级补上数据集、方法和已有的指标名称。分数及原始记录继续单独保管。

## 参考文献

表头显示会议届次和年份。AdaCLIP 参加的是 **ECCV 2024**；其 Springer 会议论文集正式引文采用 **2025**，所以 APA 条目使用 2025。

<a name="ref-adaclip"></a>

Cao, Y., Zhang, J., Frittoli, L., Cheng, Y., Shen, W., & Boracchi, G. (2025). AdaCLIP: Adapting CLIP with hybrid learnable prompts for zero-shot anomaly detection. In A. Leonardis, E. Ricci, S. Roth, O. Russakovsky, T. Sattler, & G. Varol (Eds.), *Computer vision – ECCV 2024* (pp. 55–72). Springer. [DOI](https://doi.org/10.1007/978-3-031-72761-0_4)

<a name="ref-visualad"></a>

Hou, Y., Li, P., Liu, Z., Wang, Y., Ruan, Y., Qiu, J., & Xu, K. (2026). VisualAD: Language-free zero-shot anomaly detection via vision transformer. In *Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)* (pp. 21346–21356). IEEE. [官方论文页](https://openaccess.thecvf.com/content/CVPR2026/html/Hou_VisualAD_Language-Free_Zero-Shot_Anomaly_Detection_via_Vision_Transformer_CVPR_2026_paper.html)

<a name="ref-aa-clip"></a>

Ma, W., Zhang, X., Yao, Q., Tang, F., Wu, C., Li, Y., Yan, R., Jiang, Z., & Zhou, S. K. (2025). AA-CLIP: Enhancing zero-shot anomaly detection via anomaly-aware CLIP. In *Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)* (pp. 4744–4754). IEEE. [官方论文页](https://openaccess.thecvf.com/content/CVPR2025/html/Ma_AA-CLIP_Enhancing_Zero-Shot_Anomaly_Detection_via_Anomaly-Aware_CLIP_CVPR_2025_paper.html)

<a name="ref-moeclip"></a>

Park, J. Y., Seo, J., Kang, M., & Park, Y. R. (2026). MoECLIP: Patch-specialized experts for zero-shot anomaly detection. In *Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)* (pp. 35534–35544). IEEE. [官方论文页](https://openaccess.thecvf.com/content/CVPR2026/html/Park_MoECLIP_Patch-Specialized_Experts_for_Zero-shot_Anomaly_Detection_CVPR_2026_paper.html)

<a name="ref-anomalyclip"></a>

Zhou, Q., Pang, G., Tian, Y., He, S., & Chen, J. (2024). AnomalyCLIP: Object-agnostic prompt learning for zero-shot anomaly detection. In *Proceedings of the International Conference on Learning Representations (ICLR)*. [官方论文页](https://proceedings.iclr.cc/paper_files/paper/2024/hash/d7b50b8ac2c781a12f26155f48310d8d-Abstract-Conference.html)

<a name="ref-faprompt"></a>

Zhu, J., Ong, Y.-S., Shen, C., & Pang, G. (2025). Fine-grained abnormality prompt learning for zero-shot anomaly detection. In *Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)* (pp. 22241–22251). IEEE. [官方论文页](https://openaccess.thecvf.com/content/ICCV2025/html/Zhu_Fine-grained_Abnormality_Prompt_Learning_for_Zero-shot_Anomaly_Detection_ICCV_2025_paper.html)
