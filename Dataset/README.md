# 실험에 사용한 데이터셋

**1. CVSS 점수 평가표 (CVSS scores.csv)**

각 코드의 위험도를 정량화하기 위해 FIRST.org에서 제공하는 CVSS v3.1 프레임워크를 사용해 점수를 직접 산정하였다. 

평가는 기본 평가 지표에 해당하는 8가지 항목에 따라 CWE에 대한 CVSS 점수를 산정했다. 

8가지 기준은 공격 경로(Attack Vector), 공격의 복잡도(Attack Complexity), 필요 권한(Privileges Required), 사용자 관여(User Interaction), 범위(Scope), 기밀성(Confidentiality), 무결성(Integrity), 가용성(Availability)이다.


**2. 훈련데이터 (data.json)**


**3. 테스트 데이터**

테스트 데이터셋은 선행 연구에서 공개한 PoisonPy-test.in을 활용했다.

[Github Link] https://github.com/dessertlab/Targeted-Data-Poisoning-Attacks/blob/main/Dataset/Testset/PoisonPy-test.in

**Reference**
>  Cotroneo, Domenico, et al. Vulnerabilities in AI Code Generators: Exploring Targeted Data Poisoning Attacks. 2024 IEEE/ACM 32nd International Conference on Program Comprehension (ICPC). IEEE. 2024. 
