# MRC
MRC 프로젝트의 데이터셋을 이용해서 EDA를 표현해봤습니다.

## train DataFrame
![image](https://github.com/user-attachments/assets/6a71d4ee-f6a9-451b-835c-b9abce89ab20)

판다스를 이용하여 데이터프레임을 뽑아냈습니다.



데이터프레임을 보고 EDA를 뽑아낼 수 있는지 찾아보던중 컬럼 'id'에서 'MRC-0'과 'MRC-1'을 발견하여 EDA를 표현해봤습니다.
![image](https://github.com/user-attachments/assets/06265ed2-49b0-4bc4-b297-a792392137f8)

'mrc-1' 개수: 995, 'mrc-0' 개수: 2957


그리고 타이틀의 탑5에 대해서도 EDA를 표현해봤습니다.
![image](https://github.com/user-attachments/assets/82fbd18b-8ff0-40a1-b3fe-4136cb2d15e4)

그래프에서 한글이 깨져있어 밑에 표현한 값과 비교하면 되겠습니다.


## validation DataFrame
![image](https://github.com/user-attachments/assets/fda68cd4-531c-411f-8fac-b845d289ee4e)

판다스를 이용하여 데이터프레임을 뽑아냈습니다.

![image](https://github.com/user-attachments/assets/5b975b36-c0f0-40a3-96e2-2480b051fe99)

마찬가지로 타이틀의 탑5에 대해서도 EDA를 표현해봤습니다.
![image](https://github.com/user-attachments/assets/282779d3-c259-4270-8333-9fc924cd79af)

하지만 train과 다르게 중복된 단어가 큰 차이가 없다는 것을 볼 수가 있습니다.
