# boostcamp.github.io
안녕하세요. 부스트 캠퍼 AI Tech 7기 이인구 입니다.
제가 처음으로 학습과 관련된 Github Page를 처음으로 만들어봤습니다. 앞으로도 학습과 프로젝트 등 꾸준히 올리는 습관을 길러 성장하도록 하겠습니다.


# PyTorch
## 메모리 타입
#### 정수형
- 8비트 부호가 없는 정수 : 0 ~ 255 => dtype = torch.uint8
- 8비트 부호가 있는 정수 : -128 ~ 127 => dtype = torch.int8

- 16비트 부호가 있는 정수 : -32,768 ~ 32,767 => dtype = torch.int16 또는 dtype = torch.short
- 32비트 부호가 있는 정수 : -2,147,483,648 ~ 2,147,483,647 => dtype = torch.int32 또는 dtype = torch.int
- 64비트 부호 있는 정수 : -9,223,372,036,854,775,808 ~ -9,223,372,036,854,775,807 => dtype = torch.int64 또는 torch.long

#### 실수형
- 32비트 소수점 수 : 부호1bit, 지수부8bit, 가수부23bit => dtype = torch.float32 또는 dtype = torch.float
- 64비트 소수점 수 : 부호1bit, 지수부11bit, 가수부52bit => dtype = torch.float64 또는 dtype = torch.double

#### 요소를 반환이나 계산하는 함수의 코드
 torch.sum(), torch.prod(), torch.mean(), torch.var(), torch.std()
 
#### 특성을 확인하는 메서드
- Tensor 'l'의 차원의 수를 확인 : ㅣ.dim()
- Tensor 'l'의 크기(모양)를 확인 : l.size() 또는 l.shape (메서드가 아닌 속성)
- Tensor 'l'에 있는 요소의 총 개수를 확인 : l.numel()

### 크기와 자료형이 같은 0 또는 1로 초기화
- g = torch.zeros_like(e), h = torch.ones_like(b)
- 특징 : 메모리주소가 변하지 않는다.(중요), AI 에서 메모리는 모델의 성능과도 연결이 되기 때문이다.

### 연속균등분포 난수 생성하는 코드
- i = torch.rand(3), j = torch.rand([2,3])
- 이 함수는 머신러닝과 딥러닝모델에서 파라미터 초기화나 무작위데이터를 사용하기 때문에 중요한 코드표현

## 선형 회귀 활용 예시
- 임금 예측 :연차에 따른 연봉
- 부동산 가격 예측 : 방의 개수, 교육환경, 범죄율 등에 따른 주택의 가격
- 공식 : y = Wx + b의 기울기(가중치) w와 y절편(바이어스) b
