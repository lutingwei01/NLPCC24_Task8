# NLPCC2024 Shared Task 8: Multi-Modal Entity Set Expansion

## Task Introduction

The Multi-Modal Entity Set Expansion task aims to expand a small set of seed entities with new entities belonging to the same fine-grained semantic class. To achieve this objective, the model must effectively leverage textual and visual modal information to comprehend entities and grasp the fine-grained semantic classes of the initial seed entity set.

The baseline [MESED](https://ojs.aaai.org/index.php/AAAI/article/view/28715), published in AAAI 2024, serves primarily as a reference. Detailed information about the dataset and the corresponding code is available on [GitHub](https://github.com/THUKElab/MESED) for academic and research purposes.

## Updates

All updates about this shared task will be posted on this page.

## Important Dates

- 2024/03/25: registration open;
- 2024/04/15: release of detailed task guidelines & training data;
- 2024/05/25: registration deadline;
- 2024/06/11: release of test data;
- 2024/06/20: participants’ results submission deadline;
- 2024/06/30: evaluation results release and call for system reports and conference paper;
- 2024/07/20: conference paper submission deadline (only for shared tasks);
- 2024/08/09: conference paper accept/reject notification;
- 2024/08/23: camera-ready paper submission deadline.

## Data Description

We provide a Multi-Modal Entity Set Expansion benchmark named, MESED, distinguished by its Fine-grained Semantic Classes and Hard Negative Entities. This benchmark represents the first multi-modal ESE dataset meticulously calibrated through manual efforts. It comprises 14,489 entities sourced from Wikipedia, along with 434,675 image-sentence pairs. The 70 fine-grained semantic classes in MESED contain an average of 82 entities with a minimum of 23 and a maximum of 362. Each fine-grained class is structured to include 5 queries, each accompanied by three seed entities, and another 5 queries each with five seed entities.

Download file from [this link](https://cloud.tsinghua.edu.cn/d/a6562215250c43bfb760/) and run:


```
cat dataset* > dataset.tar.gz
tar zxvf dataset.tar.gz
```

to get dataset used in our experiments.

For more information related to this dataset, please refer to the README.md file on [GitHub](https://github.com/THUKElab/MESED).



## Submission & Evaluation

For submission, the following materials should be packaged as one `zip` file and sent to [ltw23@mails.tsinghua.edu.cn](mailto:ltw23@mails.tsinghua.edu.cn):

- Submission File: The expanded entities for a query is individually written into one text file named, in the format of "class_i_j.txt". Here, "class" represents the name of the semantic class, "i" is the index of the query within the semantic class, with possible values ranging from 0 to 4, and "j" denotes the number of initial entities in the seed set, |Seed|, with options being either 3 or 5.
- Code: The code folder should contain all the codes of data augmentation, data processing, model training and model inference.
- Document:
  - Implementation Method: This document should detail the methodologies used to tackle the task, including data processing, data augmentation, and the architecture of the model. If necessary, formulas and pseudocode could be provided to facilitate understanding.
  - Code Reproduction Process: The submitted code may be checked and reproduced by us, so please briefly explain the process of reproducing the code in the document.

**For evaluation**, we employ both MAP@K metrics and P@K metrics mentioned in [MESED](https://ojs.aaai.org/index.php/AAAI/article/view/28715).



## Contact & Citation

If your publication employs our dataset, please cite the following article:

```
@article{li2024mesed, 
	title={MESED: A Multi-Modal Entity Set Expansion Dataset with Fine-Grained Semantic Classes and Hard Negative Entities},
	author={Li, Yangning and Lu, Tingwei and Zheng, Hai-Tao and Li, Yinghui and Huang, Shulin and Yu, Tianyu and Yuan, Jun and Zhang, Rui},
	journal={Proceedings of the AAAI Conference on Artificial Intelligence},
	url={https://ojs.aaai.org/index.php/AAAI/article/view/28715},
	DOI={10.1609/aaai.v38i8.28715},
	volume={38},
	number={8},
	year={2024},
	month={Mar.},
	pages={8697-8706} 
}
```

If you have any questions about this task, please email to [ltw23@mails.tsinghua.edu.cn](mailto:ltw23@mails.tsinghua.edu.cn) (C.C. [yn-li23@mails.tsinghua.edu.cn](mailto:yn-li23@mails.tsinghua.edu.cn), [zheng.haitao@sz.tsinghua.edu.cn](mailto:zheng.haitao@sz.tsinghua.edu.cn)).