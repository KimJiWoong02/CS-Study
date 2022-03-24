
# [CODE] Chapter2 : 이진 덧셈기 - 2022.03.25


### 덧셈은 연산에 있어서 가장 기본이 되는 동작이다.


------------

#### 이진수(1비트) 더하기 진리표
![image](https://user-images.githubusercontent.com/101077016/159968802-e88c2073-ee9d-4b24-a53b-afb02424ae71.png)

#### 앞자리에 0을 추거햐소 2비트 값으로 표현
![image](https://user-images.githubusercontent.com/101077016/159968876-973e8982-a2ba-467d-b600-01fa67123c5d.png)

#### 합(sum) 비트 표
![image](https://user-images.githubusercontent.com/101077016/159968906-f8fe5248-4e3d-4941-a6a3-8819a8b8b450.png)

#### 자리올림(carry) 비트 표
![image](https://user-images.githubusercontent.com/101077016/159968939-45d2ec03-1ca3-420c-a114-2e701729f884.png)

------------

#### 이진수의 덧셈도 가장 오른쪽 열부터 시작하여 각 자리수의 이진수를 하나씩 더해나간다.

![image](https://user-images.githubusercontent.com/101077016/159971368-2951f471-a903-4525-9ae0-c0e6f73baf8f.png)

------------

#### 자리올림표는 11장의 AND게이트 출력과 동일하다.

![image](https://user-images.githubusercontent.com/101077016/159971993-f8115704-229a-4843-bd36-75152bf801e0.png)

#### 합 비트표에서 OR게이트와 NAND게이트의 출력과 일부 동일하다.

![image](https://user-images.githubusercontent.com/101077016/159976892-7a0b284a-510d-402f-93fa-0e9a38a131a3.png)

#### 두 A, B 입력을 OR, NAND 게이트로 나눠져 입력 후, 두 게이트의 출력을 AND 게이트로 묶어 출력하여
#### 합 비트표를 구현

------------

#### 입력 A 혹은 B가 1인 경우 출력이 1이지만, 두 입력 모두가 1이 되는 경우에는 0이 되기 때문에
#### 상호배제적(Exclusive)인 OR 게이트 줄여서 XOR 게이트라고 한다.

![image](https://user-images.githubusercontent.com/101077016/159977356-9676452d-1d26-4f17-8c7f-a6f1ccf87af2.png)

![image](https://user-images.githubusercontent.com/101077016/159977763-741fa604-df2a-4b17-9b8c-9643f793567d.png)

------------

#### XOR와 AND게이트를 활용하여 A와 B라 지정된 두 이진수의 덧셈만들기.
#### 쉽게 그리기 위해 상자 형태의 기호를 사용한다.

![image](https://user-images.githubusercontent.com/101077016/159979447-785a4a97-4fd8-4ed4-b360-75850768dafc.png)

#### 하지만 아랫자리에서 덧셈을 통해 올라온 자리올림을 처리할 수 없다...
------------

#### 첫 번째 반가산기를 통해 출력된 합(SUM)과 이전 자리에서 올라온 자리비트값을 두 번째 반가산기에서 처리

![image](https://user-images.githubusercontent.com/101077016/159980197-c7881e62-2f4c-4be2-88b1-1bc1d45ab7d2.png)

#### 그림으로 쉽게 표현하고 전가산기(Full Adder)라고 부른다

![image](https://user-images.githubusercontent.com/101077016/159980518-e67253f4-586b-4ec9-8b99-50a72b9794ff.png)

------------

## 8비트 덧셈기를 만들기 위해서
#### - AND, OR, NAND게이트에는 각각 릴이가 2개씩 사용
#### - XOR 게이트는 6개의 릴레이로 구성
#### - 반가산기는 8개의 릴레이 (XOR, AND 각각 1개씩)
#### - 전가산기는 18개의 릴레이 (반가산기 2개, OR 1개)

### 8비트 덧셈기를 만들기 위해 8개의 전가산기를 사용하여
### 총 144개의 릴레이가 사용된다
<img width="784" alt="11" src="https://user-images.githubusercontent.com/101077016/158658144-0366a591-e075-41f5-aa68-1898d290574c.png">


