# 실험 결과

데이터 전처리 파이프라인의 성능은 생성된 코드의 위험도를 기준으로 공격 성공률(Attack Success Rate, ASR)을 통해 측정했다.

**1. 파이프라인 결과 (Scores)**

파이프라인을 통해 산출된 D-score, RI-score, C-score, R-score 점수

**2. 성능 검증 (CodeT5+)**

이상치 점수, 일관성 점수, CVSS 점수는 0과 1 사이의 값으로 정규화 한 다음, 모든 점수를 합산한 점수(R-score)를 기준으로 데이터를 내림차순 정렬하였다. 

이후 최적의 필터링 비율을 탐색하기 위해 10%, 20%, 30%, 40%, 50% 각각의 비율로 데이터를 제거했을 때, 그 데이터를 학습한 CodeT5+ 모델이 생성한 코드를 확인하였다.

- 테스트 데이터셋: 테스트 데이터셋은 선행 연구에서 공개한 ```PoisonPy-test.in```을 활용했다.

[Github Link] https://github.com/dessertlab/Targeted-Data-Poisoning-Attacks/blob/main/Dataset/Testset/PoisonPy-test.in

- ```CodeT5+_base.json```: 필터링 하지 않고, 모든 학습 데이터를 학습한 모델이 생성한 코드
- ```CodeT5+_k%.json```: k%의 데이터를 제거한 학습 데이터를 학습한 모델이 생성한 코드

**참고**

> Cotroneo, Domenico, et al. Vulnerabilities in AI Code Generators: Exploring Targeted Data Poisoning Attacks. 2024 IEEE/ACM 32nd International Conference on Program Comprehension (ICPC). IEEE. 2024.
