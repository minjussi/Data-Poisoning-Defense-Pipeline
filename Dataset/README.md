# 실험에 사용한 데이터셋

**1. CVSS 점수 평가표 (cvss_scores.csv)**

각 코드의 위험도를 정량화하기 위해 FIRST.org에서 제공하는 CVSS v3.1 프레임워크를 사용해 점수를 직접 산정하였다. 

- ```CWE```
- ```Attack Vector (AV)```: 공격 경로
- ```Attack Complexity (AC)```: 공격 복잡도
- ```Privileges Required (PR)```: 필요 권한
- ```User Interaction (UI)```: 사용자 관여
- ```Scope (S)```: 범위
- ```Confidentiality (C)```: 기밀성
- ```Integrity (I)```: 무결성
- ```Availability (A)```: 가용성
- ```CVSS 점수```: 8가지 항목에 따라 산출된 점수
- ```시나리오```: 예상되는 코드의 문맥을 정의하여 그에 맞는 점수 산출


**2. 훈련데이터 (data.json)**

본 연구에서는 CVSS 점수 구간을 0, 0.1-3.9, 4-6.9, 7-8.9, 9-10으로 나눈 다음, 각 위험도 구간에 대한 파이프라인의 유효성을 검증하기 위해 구간 별로 데이터를 20개씩을 선정하여 총 100개의 데이터로 데이터셋을 구성하였다. 

기본적으로 Kaggle의 오픈 소스 코드 데이터셋에서 총 93개의 샘플을 수집하였다. 상대적으로 4~6.9 점수 구간의 데이터가 부족하여 해당 구간에는 Cotroneo et al.의 120_poisoned.json 데이터셋의 샘플을 추가하였다. 

데이터셋은 자연어(text), 자연어에 따라 AI 코드 생성기가 생성한 코드(code), 생성한 코드의 CVSS 점수(vulnerable), 생성한 코드의 CWE 유형(cwe)로 구성되어 있다. 

[Kaggle Link] https://www.kaggle.com/datasets/thedevastator/python-code-instruction-dataset

[Github Link] https://github.com/dessertlab/Targeted-Data-Poisoning-Attacks/blob/main/Dataset/Unsafe%20samples%20with%20Safe%20implementation/120_poisoned.json


**Reference**
> The Devastator. Python Code Instruction Dataset: Training Data with Instruction, Input, Output, and Prompt Columns. Kaggle Dataset.
> Cotroneo, Domenico, et al. Vulnerabilities in AI Code Generators: Exploring Targeted Data Poisoning Attacks. 2024 IEEE/ACM 32nd International Conference on Program Comprehension (ICPC). IEEE. 2024. 
