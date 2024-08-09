# boostcamp.github.io
안녕하세요. 부스트 캠퍼 AI Tech 7기 이인구 입니다.
제가 처음으로 학습과 관련된 Github Page를 처음으로 만들어봤습니다. 앞으로도 학습과 프로젝트 등 꾸준히 올리는 습관을 길러 성장하도록 하겠습니다.


## 1주차 : PyTorch
#### 정수형 : 소수 부분이 없는 숫자를 저장하는 데 사용되는 데이터 타입
- 8비트 부호 없는 정수 : 0 ~ 255 => dtype = torch.uint8
- 8비트 부호 없는 정수 : -128 ~ 127 => dtype = torch.int8

- 16비트 부호 있는 정수 : -32,768 ~ 32,767 => dtype = torch.int16 또는 dtype = torch.short
- 32비트 부호 있는 정수 : -2,147,483,648 ~ 2,147,483,647 => dtype = torch.int32 또는 dtype = torch.int
   - 대부분의 프로그래밍에서 표준적인 정수 크기로 사용
- 64비트 부호 있는 정수 : -9,223,372,036,854,775,808 ~ -9,223,372,036,854,775,807 => dtype = torch.int64 또는 torch.long

#### 실수형 : 실수형 데이터 타입들은 신경망의 수치 계산
- 32비트 부동 소수점 수 : 부호1bit, 지수부8bit, 가수부23bit dtype = torch.float32 또는 dtype = torch.float
- 64비트 부동 소수점 수 : 부호1bit, 지수부11bit, 가수부52bit dtype = torch.float64 또는 dtype = torch.double

#### 타입 캐스팅 : 한 데이터 타입을 다른 데이터 타입으로 변환하는 것
i = torch.tensor([2,3,4], dtype = torch.int8) 이런식으로 Tensor를 생성했을 때,
j = i.float(), k = i,double()

#### Tensor의 요소를 반환하거나 계산하는 함수의 코드 표현
 torch.sum(), torch.prod(), torch.mean(), torch.var(), torch.std()
#### Tensor의 특성을 확인하는 메서드의 코드 표현
- Tensor 'l'의 차원의 수를 확인 : ㅣ.dim()
- Tensor 'l'의 크기(모양)를 확인 : l.size() 또는 l.shape (메서드가 아닌 속성)
- Tensor 'l'에 있는 요소의 총 개수를 확인 : l.numel()

### 크기와 자료형이 같은 0 또는 1로 초기화된 Tensor로 표현
- g = torch.zeros_like(e), h = torch.ones_like(b)
- 특징 : 메모리주소가 변하지 않는다.(중요하다), AI 에서 메모리는 모델의 성능과도 연결이 되기 때문이다.

### [0, 1] 구간의 연속균등분포 난수 Tensor 생성하는 코드 표현
- i = torch.rand(3), j = torch.rand([2,3])
- 이 함수는 머신러닝과 딥러닝모델에서 파라미터 초기화나 무작위데이터를 사용하기 때문에 중요한 코드표현
