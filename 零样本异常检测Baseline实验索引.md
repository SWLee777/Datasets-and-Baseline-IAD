# 零样本异常检测 Baseline 实验索引

查到所需的**评测层级、数据集和方法**后，请向老师索取对应指标的原始结果。**先确认能否复用，再决定是否重跑。** 申请时注明数据集版本或划分；同名数据集或同名指标不一定使用同一评测设置。

[像素级](#像素级) · [图像级](#图像级)

表格只登记原表已有记录的**指标名称**，不展示任何实验数值。`—` 或未列出的组合表示本索引未收录，不代表没有跑过。

## 像素级

| 领域 | 数据集 | Anomaly CLIP | Ada-CLIP | AA-CLIP | FA Prompt | Visual AD | MoE CLIP |
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

| 领域 | 数据集 | Anomaly CLIP | Ada-CLIP | AA-CLIP | FA Prompt | Visual AD | MoE CLIP |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 工业 | MVTecAD | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP |
| 工业 | VisA | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP |
| 工业 | BTAD | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP |
| 工业 | MPDD | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP |
| 工业 | AITEX | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP |
| 医学 | HeadCT | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP |
| 医学 | Br35H | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP | AUROC、AP |

**索取示例**：老师，我想复用图像级 VisA 上 Ada-CLIP 的 AUROC 和 AP，请问现有结果对应的是哪个数据版本和划分？

**更新方式**：新结果归档后，在对应层级补上数据集、方法和已有的指标名称。分数及原始记录继续单独保管。
