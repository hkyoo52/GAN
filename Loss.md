## 기본 이해
#### 확률 vs 가능도
* 확률 함수(Pr(x|Θ)) : 파라미터(Θ)가 주어졌을 때(어떤 데이터 분포가 주어졌을 때) 관측 데이터가 나올 가능성, 파라미터 값 고정!!

Ex. 동전 앞면이 나올 가능성은 0.5( = Θ)이다.(분포가 생성) 3번을 던졌을 때 앞면 2번 나올 확률은?(x)

* 가능도(L(Θ|x)) : 어떤 데이터가 주어졌을 때 이 데이터가 나타날려면 분포가 어떨까?(파라미터는 무엇일까?)

Ex. 앞면 2번 뒷면 1번(데이터 분포) 나올 확률이 3/8(정답)일때 앞면 나올 확률이 0.5(Θ)일 가능성은?

![image](https://user-images.githubusercontent.com/63588046/198891904-ae9b0d3a-9212-4426-8b36-a57003d01724.png)


* AI는 데이터와 정답이 주어졌고 분포를 찾는 과정 -> 가능도를 구하는 것이다.

![image](https://user-images.githubusercontent.com/63588046/198891714-fcc0402e-c3cc-4e29-bc07-c361ec00142d.png)

![image](https://user-images.githubusercontent.com/63588046/198891721-7385d1e4-7813-41d8-a826-6c1f51a528ff.png)


#### 베르누이 분포
* 2가지 선택중에서 1가지 결과만 나오는 분포이다. 이항분포라고도 한다.
![image](https://user-images.githubusercontent.com/63588046/198892136-33a86a24-dbce-4d6e-9c05-0d6805fa7c3a.png)

* 베르누이 분포의 로그 가능도
![image](https://user-images.githubusercontent.com/63588046/198893107-b91da010-26d6-42f9-a2c5-d69259c9a533.png)

#### 엔트로피
* 엔트로피 : 발생할 가능성이 적은 정도 + 그것을 표현하기 위한 자원량

![image](https://user-images.githubusercontent.com/63588046/198893892-6dd74d75-c15b-4654-a194-61fe7828743e.png)

#### 크로스 엔트로피
* 다른 확률 분포가 같은 사건에 대해 가지는 정보량
![image](https://user-images.githubusercontent.com/63588046/198893222-0f779f2d-ce4c-4494-bebf-1fe973669404.png)


## BCE Loss(Binary Cross Entropy Loss)
![image](https://user-images.githubusercontent.com/63588046/198890853-9d422507-3fb8-4a57-aeaa-0bdda342869d.png)

#### 유도
![image](https://user-images.githubusercontent.com/63588046/198893416-4d1102ab-e655-474d-8f7c-a550c5debffb.png)

## KL Divergence
* 정보량의 차이에 대한 기댓값 (p->q로 근사할때 얼마나 많은 정보량을 잃어버리는가)
![image](https://user-images.githubusercontent.com/63588046/198893509-14fee7d8-7ad1-4519-bc01-eb0d80280fcf.png)

![image](https://user-images.githubusercontent.com/63588046/198893569-e0a49f5c-a557-4bae-a11c-284d2becf1ec.png)

## BCE와 KL과의 관계
![image](https://user-images.githubusercontent.com/63588046/198893610-42c4f3c4-c45c-4a1b-a9a5-e275437dc966.png)


