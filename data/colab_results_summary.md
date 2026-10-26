# Colab results summary

- Source rows loaded: 43,018
- Terpene features analyzed: 26
- Strain-name proxy: `strain_name_analysis` (original column preserved as `strain_name_original`)
- Replication threshold for inferential strain tests: n >= 5

## Terpedia Terpotype Classifier (TTC-7)

- Core terpene features: 9
- Complete chemistry profiles classified: 32,050
- Selected number of terpotypes: 7
- Silhouette score: 0.278
- Final-model evaluation silhouette: 0.279
- Negative-silhouette fraction: 0.036
- Median assignment strength: 0.418
- Mean 80% subsample ARI: 0.650
- Minimum leave-one-terpene-out ARI: 0.468
- Median strain-label purity: 0.400
- Weighted strain-label purity: 0.406
- Chance-adjusted weighted purity: 0.134
- Label/terpotype normalized mutual information: 0.112

| terpotype_id   |   n_profiles | terpotype_name   | terpotype_label    |   beta-Myrcene |   beta-Pinene |   delta-Limonene |   alpha-Pinene |   beta-Caryophyllene |   Terpinolene |   alpha-Humulene |   Linalool |   Caryophyllene Oxide |
|:---------------|-------------:|:-----------------|:-------------------|---------------:|--------------:|-----------------:|---------------:|---------------------:|--------------:|-----------------:|-----------:|----------------------:|
| T1             |         5268 | Lavender Pine    | T1 Lavender Pine   |    0.0778391   |   0.000174973 |        0.0439784 |    0.145465    |          0.110105    |   0.00644801  |        0.0938099 | 0.43769    |             0.0844894 |
| T2             |         2765 | Velvet Pepper    | T2 Velvet Pepper   |    0.0790888   |   0.000294436 |        0.0498738 |    0.000183337 |          0.151147    |   0.00953928  |        0.105693  | 0.496758   |             0.107423  |
| T3             |         2410 | Green Comet      | T3 Green Comet     |    0.0732793   |   0.000398537 |        0.0407058 |    0.0838407   |          0.234617    |   0.269261    |        0.225649  | 0.0303543  |             0.0418939 |
| T4             |         2386 | Hopwood Pine     | T4 Hopwood Pine    |    0.184035    |   0.00104198  |        0.0415881 |    0.195732    |          0.000673255 |   0.038214    |        0.432671  | 0.0333087  |             0.0727357 |
| T5             |         4339 | Dry Pepperwood   | T5 Dry Pepperwood  |    0.000325234 |   0.000567741 |        0.0333131 |    0.151301    |          0.377093    |   0.000887663 |        0.395209  | 0.00491458 |             0.0363885 |
| T6             |         5317 | Deep Pepperwood  | T6 Deep Pepperwood |    0.161098    |   0.000546152 |        0.0178004 |    0.173502    |          0.270479    |   0.000419961 |        0.345634  | 0.00145198 |             0.0290686 |
| T7             |         9565 | Citrus Loam      | T7 Citrus Loam     |    0.256049    |   0.0419644   |        0.186439  |    0.0647613   |          0.24562     |   0.0499794   |        0.0803119 | 0.0648664  |             0.0100084 |

## Robustness diagnostics

| terpotype_id   | terpotype_name   |   n_profiles |   mean_assignment_strength |   median_assignment_strength |   q25_assignment_strength |   q75_assignment_strength |   fraction_below_0_10 |   fraction_below_0_20 |
|:---------------|:-----------------|-------------:|---------------------------:|-----------------------------:|--------------------------:|--------------------------:|----------------------:|----------------------:|
| T1             | Lavender Pine    |         5268 |                   0.386937 |                     0.372852 |                  0.231925 |                  0.557111 |             0.059795  |              0.192103 |
| T2             | Velvet Pepper    |         2765 |                   0.352547 |                     0.325917 |                  0.220207 |                  0.525139 |             0.0969259 |              0.213382 |
| T3             | Green Comet      |         2410 |                   0.280209 |                     0.252485 |                  0.133615 |                  0.424873 |             0.171784  |              0.400415 |
| T4             | Hopwood Pine     |         2386 |                   0.278728 |                     0.326798 |                  0.134477 |                  0.399463 |             0.184409  |              0.361274 |
| T5             | Dry Pepperwood   |         4339 |                   0.388972 |                     0.451604 |                  0.264742 |                  0.489898 |             0.0974879 |              0.191749 |
| T6             | Deep Pepperwood  |         5317 |                   0.414636 |                     0.422509 |                  0.259041 |                  0.585545 |             0.0951664 |              0.195411 |
| T7             | Citrus Loam      |         9565 |                   0.475069 |                     0.518951 |                  0.328178 |                  0.640958 |             0.0903293 |              0.161004 |

### Leave-one-terpene-out sensitivity

| omitted_terpene     |   ARI_vs_full_panel |
|:--------------------|--------------------:|
| Linalool            |            0.468292 |
| beta-Pinene         |            0.50618  |
| alpha-Humulene      |            0.553734 |
| Caryophyllene Oxide |            0.562513 |
| beta-Myrcene        |            0.570826 |
| delta-Limonene      |            0.676445 |
| alpha-Pinene        |            0.742488 |
| Terpinolene         |            0.77118  |
| beta-Caryophyllene  |            0.821573 |

## Most variable terpene endpoints

| feature           |      cv |
|:------------------|--------:|
| cis-Nerolidol     | 2.44949 |
| Terpinolene       | 2.32951 |
| beta-Pinene       | 2.25009 |
| p-Cymene          | 2.2447  |
| Isopulegol        | 2.2317  |
| Eucalyptol        | 2.14385 |
| trans-Nerolidol 2 | 2.03341 |
| delta-Limonene    | 2.01508 |
| gamma-Terpinene   | 1.99212 |
| 3-Carene          | 1.91427 |

## Strain-name omnibus tests

| feature             |   groups |    n |        H |      p_value |   epsilon_squared |      q_value |
|:--------------------|---------:|-----:|---------:|-------------:|------------------:|-------------:|
| beta-Pinene         |      752 | 9542 | 3191.68  | 5.89356e-297 |         0.277666  | 1.47339e-295 |
| alpha-Humulene      |      752 | 9542 | 2219.56  | 7.04312e-145 |         0.167072  | 8.8039e-144  |
| delta-Limonene      |      752 | 9542 | 2181.03  | 2.34893e-139 |         0.162688  | 1.95744e-138 |
| beta-Caryophyllene  |      752 | 9542 | 2108.68  | 3.99789e-129 |         0.154458  | 2.49868e-128 |
| alpha-Pinene        |      752 | 9541 | 1971.86  | 2.62163e-110 |         0.138907  | 1.31082e-109 |
| beta-Myrcene        |      752 | 9542 | 1943.97  | 1.45125e-106 |         0.135719  | 6.04688e-106 |
| Terpinolene         |      752 | 9541 | 1799.83  | 8.98655e-88  |         0.119334  | 3.20948e-87  |
| 3-Carene            |      379 | 1716 |  982.168 | 2.75586e-55  |         0.451883  | 8.61206e-55  |
| Linalool            |      752 | 9542 | 1477.17  | 9.07797e-50  |         0.0826135 | 2.52166e-49  |
| alpha-Terpinene     |      379 | 1716 |  931.656 | 1.29619e-48  |         0.414103  | 3.24048e-48  |
| Ocimene             |      427 | 1970 |  951.106 | 4.13031e-42  |         0.340315  | 9.38707e-42  |
| Caryophyllene Oxide |      750 | 9288 | 1395.57  | 1.55059e-41  |         0.0757282 | 3.23039e-41  |
| gamma-Terpinene     |      379 | 1716 |  827.707 | 1.15785e-35  |         0.336355  | 2.22663e-35  |
| Guaiol              |      379 | 1716 |  736.458 | 2.44067e-25  |         0.268106  | 4.35833e-25  |
| trans-Nerolidol 1   |      186 |  441 |  366.5   | 4.6532e-14   |         0.711763  | 7.75533e-14  |
| alpha-Bisabolol     |      379 | 1715 |  607.242 | 6.31369e-13  |         0.171588  | 9.28484e-13  |
| p-Cymene            |      379 | 1716 |  607.424 | 6.09525e-13  |         0.171596  | 9.28484e-13  |
| Camphene            |      379 | 1716 |  598.888 | 3.11007e-12  |         0.165212  | 4.31954e-12  |
| Geraniol            |      379 | 1716 |  568.201 | 7.96616e-10  |         0.14226   | 1.04818e-09  |
| Eucalyptol          |      379 | 1716 |  565.728 | 1.21803e-09  |         0.14041   | 1.52254e-09  |

## Interpretation

All records are treated as *Cannabis sativa*; no between-species effect is estimable. A strain-name association is not evidence of genotype without matched genetic data.