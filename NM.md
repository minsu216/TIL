# Sequence to Sequence model
- 글자나 단어 이미지의 피처 이런 것들의 아이템 시퀀스받아 
__새로운 시퀀스 생성__

- 입력에 해당하는 시퀀스에 대한 처리가 끝나면 인코더 쪽에서는 context를 디코더 쪽으로 보낸다.

- decoder쪽에서는 출력을 해야될 output을 출력!
- 전부 RNN구조인 특징을 가지고 있다.

# context 벡터
- context 벡터는 실수형태의 값들이 있는 벡터임
- context 벡터의 크기를 설정하고자 할때, 입력 데이터에 대한 정보라고 할 수 있다.
- RNN의 출력 인 hidden Units를 일정하게 한다.
__보통 사이즈는 256,512,1024 정도이다__

- 2개의 입력은 RNN에 들어가려면 VECTOR 형태로 표현
- 따라서 <span style="color:red">워드 임베딩</span> 방법을 사용해 단어를 벡터 변환!

# decoder 구동

- 첫번째로 인코더에서 전달 받은 전체 히든스테이츠를 확인
- 각각 인코더 히든 스테이츠들이 바로 이전 단어에 대한 어떤 정보를 포함하고 있지만 현재 입력된 단어와도 연관성이 있다.
- 히든 스테이츠마다 스코어를 계산한다.

- 계산된 점수들에 대해 softmax를 구하고 각각의 timestep에 해당되는 히든 스테이츠에 곱한다.
- 그리고 높은 점수에 해당되는 걸 선택



# Ex 예측

1. context 정보가 올라감
2. encoder에 각각단어마다 hidden state가 있고
3. 어떤 hidden state에 집중하고 있는지 확인

# Transformer
seq2seq의 구조인 인코더-디코더를 따르면서도, Attention만으로 구현한 모델입니다. RNN을 사용하지 않고, 인코더-디코더 구조를 설계하였음에도 번역 성능에서도 RNN보다 우수한 성능을 보임.


# self attention layer

인코더 쪽에서 어떤 하나의 특정 단어를 인코딩하기 위해서 input sentence에 있는 다른 단어와의 관계를 살펴본다.

# Transformer 주요 파라미터
- 512 차원을 주로 사용함.

# 