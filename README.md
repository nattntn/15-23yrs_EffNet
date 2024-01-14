# 15-23yrs_EffNet
Unflipped training using panoramic radiograph images of patients aged between 15-23 yrs.
**Training Dataset**

|  Age  | Male(People)  | Female(People)  | Sum(People)  |  Sum(Images) |
|:-----:|:-------------:|:---------------:|:------------:|:------------:|
|  15   |      58       |       60        |      118     |      227     |
|  16   |      61       |       61        |      122     |      230     |
|  17   |      55       |       57        |      112     |      219     |
|  18   |      53       |       73        |      126     |      232     |
|  19   |      59       |       62        |      121     |      222     |
|  20   |      56       |       54        |      110     |      204     |
|  21   |      60       |       52        |      112     |      207     |
|  22   |      58       |       55        |      113     |      202     |
|  23   |      54       |       58        |      112     |      209     |
|**Sum**|    **xxx**    |    **xxxxx**    |   **xxxxx**  |   **xxxxx**  |

## Google Drive
* **Transfer and Fine-tune with Duo**
  * [Drive: Model --> Unflipped_Multi_task(15-23))](https://drive.google.com/drive/u/0/folders/1_hdKLDWBX_E0QvL7J44P0DTG6xRfCxjW)
  * [Colab (train round24)](https://colab.research.google.com/drive/1cGdcc2TG4UnFWl8vpL8IIaQ4D_BI_YqA?usp=sharing)
  * [Colab (predict round24)](https://colab.research.google.com/drive/1GrPRzo9qlIRBH-3XHlfztdwYy_yjGOgW?usp=sharing)

* **Transfer with *Age* and Fine-tune with Duo**
  * [Drive: Model --> Unflipped_Regress_Age(15-23)]()
  * [Colab (train round24)]()
  * [Colab (predict round24)]()

* **Transfer with *Gender* and Fine-tune with Duo**
  * [Drive: Model --> Unflipped_Classification_Gender(15-23)](https://drive.google.com/drive/u/0/folders/1gSnNTp_DwS-gacctGDKAy0MGtKOMxsEk)


## Results (15-23 yrs)
|  Transfer learning  | Fine-tuning  | Age (RMSE)  | Gender(Accuracy)  |  Age (R^2) |   ROC  | Epochs |
| :------------------:|:------------:|:-----------:|:-----------------:|:----------:|:------:|:------:|
|         Duo         |      -       |     2.13    |      84.22%       |   32.29%   |  0.95  |  4,000 |
|         Duo         |      Duo     |     1.91    |      95.11%       |   45.81%   |  0.99  |  3,250 |
|         Age         |      -       |     2.31    |        -          |   77.80%   |  |3,250 |
|         Age         |   Duo(26)    |     1.67    |      86.70%       |   88.45%   |  |3,250 |
|        Gender       |      -       |      -      |      76.44%       |     -      |  0.92  | 2,250 |
|        Gender       |     Duo      |     1.90    |      92.67%       |   46.47%   |   0.98  |4,250 |

