# Turning Dross Into Gold Loss: Is BERT4Rec really better than SASRec?

This repository contains code for ACM RecSys 2023 paper ["Turning Dross Into Gold Loss: Is BERT4Rec really better than SASRec?"](https://arxiv.org/abs/2309.07602) by Anton Klenitskiy and Alexey Vasilev.

## patience 늘리고, head수 4, 8일때 

**MovieLens-1m**

| **Model**          | **HitRate@10**     | **NDCG@10**        | **Training time** | **Best epoch** |
|--------------------|--------------------|--------------------|-------------------|----------------|
| BERT4Rec (head=8)  | 0.             | 0.             |               |             |
| BERT4Rec (head=8)  | 0.             | 0.             |                |              |
| SASRec+3000(head=4)| 0.3141             | 0.1836             | 5092              | 376            |
| SASRec+3000(head=8)| **0.3159**         | **0.1866**         | 6203              | 433            |



## head = 1일때

**MovieLens-1m**

| **Model**          | **HitRate@10**     | **NDCG@10**        | **Training time** | **Best epoch** |
|--------------------|--------------------|--------------------|-------------------|----------------|
| BERT4Rec           | 0.2843             | 0.1537             | 1409              | 197            |
| SASRec             | 0.2500             | 0.1341             | 486               | 53             |
| SASRec+ (our)      | 0.3152             | 0.1821             | 540               | 63             |
| SASRec+ 3000 (our) | **0.3159**         | **0.1857**         | 769               | 85             |

**MovieLens-20m**

| **Model**          | **HitRate@10**     | **NDCG@10**        | **Training time** | **Best epoch** |
|--------------------|--------------------|--------------------|-------------------|----------------|
| BERT4Rec           | 0.2816             | 0.1703             | 14758             | 68             |
| SASRec             | 0.2001             | 0.1067             | 2495              | 30             |
| SASRec+ (our)      | 0.2983             | 0.1833             | 9959              | 46             |
| SASRec+ 3000 (our) | **0.3090**         | **0.1872**         | 4125              | 39             |

**Steam**

| **Model**          | **HitRate@10**     | **NDCG@10**        | **Training time** | **Best epoch** |
|--------------------|--------------------|--------------------|-------------------|----------------|
| BERT4Rec           | **0.1242**         | **0.0662**         | 4893              | 74             |
| SASRec             | 0.0981             | 0.0506             | 2140              | 39             |
| SASRec+ (our)      | 0.1191             | 0.0641             | 1262              | 16             |
| SASRec+ 3000 (our) | 0.1206             | 0.0652             | 1226              | 14             |


## Citing

If this work was useful in your research, please consider citing our paper:
```
@inproceedings{klenitskiy2023turning,
  title={Turning Dross Into Gold Loss: is BERT4Rec really better than SASRec?},
  author={Klenitskiy, Anton and Vasilev, Alexey},
  booktitle={Proceedings of the 17th ACM Conference on Recommender Systems},
  pages={1120--1125},
  year={2023}
}
```
