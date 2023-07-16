# 1차 미팅 질문

**enum 열거체 활용 예제**<br>
대표적으로 switch case 문과 함께 활용할수 있다.<br>
아래는 간단한 코드 게임 예시이다.<br>
```cpp
enum Action {
  Attack = 1, //Attack = 1, Move = 2, Jump = 3, Hide = 4 와 같이 값이 할당됨
  Move,
  Jump,
  Hide
};

void main()
{
  enum Action skill;
  cout << "Attack : 공격, Move : 움직이기, Jump : 점프하기, Hide : 숨기 (취할 행동을 입력해 주세요.)" << endl;
  cin >> skill

  switch(skill)
  {
    case Attack:
      printf("공격하셨습니다.");
      break;
    case Move:
      printf("움직이셨습니다.");
      break;
    case Jump:
      printf("점프하셨습니다.");
    case Hide:
      printf("숨으셨습니다.");
      break;
    default:
      break;
  }
}
```

**포인터 활용 예제**<br>
포인터를 사용하면 간결하고 효율적인 표현과 처리가 가능하고 더 빠른 기계어 코드를 생성할 수 있으며,<br>
복잡한 자료 구조와 함수의 쉬운 접근이 가능하다.<br>
[본문](https://oper6210.tistory.com/160)

아래는 포인터를 통한 변수 접근 예제이다.<br>
```cpp

void swap(int *pa, int *pb)

void main(){
  int a = 10, b =20;
  swap(&a,&b);
  cout << "a :" << a << "b :" << b; 
}

void swap(int *pa, int *pb){
  int temp;
  temp = *pa; // temp 에 pa 가 가르키는 값 저장
  *pa = *pb; // pa 가 가르키는 변수에 pb 값 저장
  *pb = temp; // pb 가 가르키는 변수에 temp 값 저장 
}
```
위 코드 실행시 아래와 같은 결과가 나온다
```
a : 20, b : 10
```
교환 작업은 swap에서 일어나지만 포인터를 통해 실제로 바뀌는 값은 main 함수의 변수 a,b 가 변하게 된다.<br>
