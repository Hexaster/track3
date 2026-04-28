# Course Project: Cigarette Constituent Prediction

## 1 Project Background

In this project, you will act like a real scientific researcher,
exploring limited yet high-dimensional data, and receive the challenge
of unseen data.

Cigarette smoke chemistry is affected by both physical cigarette design
and puff-by-puff airflow behavior. In practice, laboratories measure
important smoke constituents such as tar, carbon monoxide, and phenol
through experiments, but these experiments are expensive and
time-consuming.

Your job in this project is to predict cigarette smoke constituents from
physical measurements and puff-level air intake records.

## 2 Dataset Description

You are provided with experimental cigarette data. The released data
contain input features and target values for three smoke constituents:
tar, CO, and phenol.

The feature columns include three groups of puff-level airflow
measurements:

| **Feature group** | **Columns**                                | **Description**                                               |
|-------------------|--------------------------------------------|---------------------------------------------------------------|
| Cone air intake   | ConeAir_puff_01_mL to ConeAir_puff_10_mL   | Air entering through the burning cone for each of 10 puffs    |
| Paper air intake  | PaperAir_puff_01_mL to PaperAir_puff_10_mL | Air entering through the cigarette paper for each of 10 puffs |
| Vent air intake   | VentAir_puff_01_mL to VentAir_puff_10_mL   | Air entering through filter ventilation for each of 10 puffs  |

The dataset also contains physical cigarette measurements:

| **Column**                 | **Description**                           |
|----------------------------|-------------------------------------------|
| Circumference_cm           | Cigarette circumference                   |
| FilterBeforeVent_cm        | Filter length before the ventilation zone |
| FilterAfterVent_cm         | Filter length after the ventilation zone  |
| TobaccoRodResistance_Pa_cm | Tobacco rod draw resistance               |
| FilterResistance_Pa_cm     | Filter draw resistance                    |
| NumPuffs                   | Number of puffs recorded for the sample   |

## 3 Objective

For each row in the test set, predict the following three values:

| **Target**              |
|-------------------------|
| Tar_mg_per_cigarette    |
| CO_mg_per_cigarette     |
| Phenol_ug_per_cigarette |

Your submission file should contain exactly these columns:

| **Column**              |
|-------------------------|
| SampleID                |
| Tar_mg_per_cigarette    |
| CO_mg_per_cigarette     |
| Phenol_ug_per_cigarette |

Predictions should be numeric values. Do not submit confidence intervals
or hard categories.

Submissions will be evaluated using the average of $R^{2}$ scores of the
three constituents.
