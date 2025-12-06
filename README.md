# ML_Project
추가된 파일:
1. raw_data_gerate: 폰트 증강을 적용하지 않은 colored 순정 데이터 생성
->colored_mnist_train_raw.npz , colored_mnist_val_raw.npz 두 개의 데이터셋 생성

2. model_selection(raw_data): 순정 데이터로 SVM과 기존 3종 모델 학습 및 학습시간/성능 비교
-> 학습시간이 더 짧고, 성능이 더 좋은 트리기반 앙상블 모델 3종으로 선정

3. [가설1 검증]: 
3-1. 80k_data_generate.ipynb: 학습데이터 6만개에서 8만개까지 늘림
->colored_mnist_train_80k.npz, colored_mnist_val_80k.npz 두 파일 생성
3-2. 기존 model.ipynb 모델 학습을 훈련/검증 데이터셋 경로만 바꿔서 진행
-> 80k_model.ipynb로 사본 생성

4. [가설2 검증]: data_agumentation: Hard Example Mining 기법으로 모델 3종 증강 및 성능 비교
Hard Example Mining 기법 : 폰트 증강 적용된 훈련 데이터셋에서 오분류한 데이터와 비슷한 유형을 증강(회전/이동)
-> 유의미한 성능 향상 보이지 못 함
*기존 model.ipynb 파일에서 오분류 데이터 추출과 그레이스케일 적용 전 추가적 데이터 증강 적용 진행함.
유의미한 성능 향상 보이지 못 했으므로 가설2에 대한 예측을 검증.

(선택) model_pure_vs_font.ipynb : 3종 모델로 순정 데이터 vs 폰트 적용 데이터 성능 비교
순정 데이터에 대한 성능 측정은 model_selection 부분에서 진행했으니(SVM포함 모델 4종) 필요하면 넣고 필요없으면 빼도 될 듯
