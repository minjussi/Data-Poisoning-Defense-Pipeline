# 실험에 사용한 데이터셋

**1. CVSS 점수 평가표 (CVSS scores.csv)**

각 코드의 위험도를 정량화하기 위해 FIRST.org에서 제공하는 CVSS v3.1 프레임워크를 사용해 점수를 직접 산정하였다. 

- ```CWE```
- ```Attack Vector (AV)```
- ```Attack Complexity (AC)```
- ```Privileges Required (PR)```
- ```User Interaction (UI)```
- ```Scope (S)```
- ```Confidentiality (C)```
- ```Integrity (I)```
- ```Availability (A)```
- ```CVSS 점수```
- ```시나리오```



**2. 훈련데이터 (data.json)**

[Kaggle Link] https://www.kaggle.com/datasets/thedevastator/python-code-instruction-dataset

[Github Link] https://github.com/dessertlab/Targeted-Data-Poisoning-Attacks/blob/main/Dataset/Unsafe%20samples%20with%20Safe%20implementation/120_poisoned.json



**3. 테스트 데이터**

테스트 데이터셋은 선행 연구에서 공개한 PoisonPy-test.in을 활용했다.

[Github Link] https://github.com/dessertlab/Targeted-Data-Poisoning-Attacks/blob/main/Dataset/Testset/PoisonPy-test.in

**Reference**
> The Devastator. Python Code Instruction Dataset: Training Data with Instruction, Input, Output, and Prompt Columns. Kaggle Dataset.
>  Cotroneo, Domenico, et al. Vulnerabilities in AI Code Generators: Exploring Targeted Data Poisoning Attacks. 2024 IEEE/ACM 32nd International Conference on Program Comprehension (ICPC). IEEE. 2024. 
