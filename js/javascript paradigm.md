# 절차 지향 프로그래밍(Procedural Programming)

절차 지향 프로그래밍은 프로그램을 일련의 순차적인 절차로 보고, 이러한 절차를 함수로 구현하여 프로그램의 흐름을 제어하는 방식이다. 자바스크립트에서 절차 지향 프로그래밍은 간단한 스크립트나 알고리즘 구현에 주로 사용된다. 예를 들어 특정 작업을 수행하는 함수를 정의하고 필요에 따라 이러한 함수들을 순차적으로 호출하는 방시으로 프로그램을 구성할 수 있다.

- 핵심 개념: 프로그램을 일련의 순차적인 절차(함수 또는 명령의 집합)로 보고, 그 절차들을 순서에 따라 실행하여 원하는 결과를 얻는 방식이다.

- 특징: 
    - 각 절차는 데이터를 입력 받아 처리하고 결과를 출력할 수 있다.
    - 코드의 재사용성이 낮고, 유지보수가 어려울 수 있다.


```javascript
const calculateArea = (width,height)=>{
    return width * height;
}

const  printArea = (area) => {
    console.log(`Area: ${area}`);
}

const area =  calculateArea(5,4);
printArea(area);
```

# 객체 지향 프로그래밍 (Object-Oriented Programming, OOP)

객체 지향 프로그래밍은 데이터(속성)와 그 데이터를 처리하는 함수(메서드)를 객체로 묶어서 다루는 방식입니다. 자바스크립트에서 프로토타입(prototype) 기반 상속을 통해 객체 지향 프로그래밍을 구현한다. 클래스 문법(ES6 이후)을 사용하여 객체를 정의하고, 인스턴스화하여 사용할 수 있다.

- 핵심 개념: 프로그램을 객체들의 집합으로 파악하며, 각 객체는 데이터와 그 데이터를 처리하는 함수(메서드)를 포함한다. 

- 특징: 
    - 캡슐화, 상속 다향성, 추상화 같은 기본 원칙을 따릅니다.
    - 코드 재사용성과 유지보수성이 높아진다. 

```javascript
class Rectangle{
    constructor(width,height){
        this.width = width;
        this.height = heoght;
    }

    calculateArea = () =>{
        return this.width * this.height;
    }

    printArea = () =>{
        console.log(`Area: ${this.calculateArea()}`);
    }
}

const rectangle = new Rectangle(5,4);

rectangle.printArea();
```

# 함수형 프로그래밍(Functional Programing)

함수형 프로그래밍은 "힘수"를 일급 겍체로 취급하며 불변성(immutability), 순수 함수(Pure Functions), 고차 함수(High-Order-Functions) 등의 개념을 중심으로 프로그램을 구성하는 패러다임이다. 자바스크립트에서 함수형 프로그래밍은 데이터 변형을 최소화하고, 부작용을 피하며 코드의 재사용성과 테스트 용이성을 높이는 데에 초점을 마춘다.

- 핵심 개념: 계산을 수학적 함수의 평가로 간주하고, 상태 변경이나 가변 데이터를 피하는 방식이다. 

- 특징: 
    - "순수 함수"와 "불변성"이 중요한 개념이다. 순수 함수란 동일한 입력에 대해 항상 동일한 출력을 반환하며 부작용(side effect)이 없는 함수를 말한다. 

    - 함수의 고차 함수(higher-order-function) 사용을 장려합니다. 고차 함수는 다른 함수를 입력으로 받거나 함수를 결과로 반환하는 함수입니다. 

    - 코드의 가독성과 모듈성이 높아진다. 

```javascript
const numbers = [1,2,3,4,5];

// 순수 함수 예시 
const double = number => number * 2

// 고차 함수 예시 
const doubledNumbers = numbers.map(double);

console.log(doubledNumbers); //[2,4,6,8,10]

```